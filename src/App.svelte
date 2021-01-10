<script>
    import { onMount } from "svelte";
    let amount = 2000;
    // Create an instance of the Stripe object with your publishable API key
    let stripe;
    onMount(() => {
        stripe = Stripe(
            "pk_test_51I7ulLHX1rk5bSX1NWKzYasE7DIcdINuZNebzwx6ywnMypYfnlVLR0pVg6MuTc8I3GuMmY4Fcymhhqhw2pcO3w8g00yko2X1T2"
        );
    });
    function checkout() {
        fetch("http://api.gitbid.io/create/bounty", {
            method: "POST",
            headers: {
                "Content-Type": "application/json",
            },
            body: JSON.stringify({
                amount: amount,
                issue_id: 42,
            }),
        })
            .then(function (response) {
                console.log("RESPONSE", response)
                return response.json();
            })
            .then(function (session) {
                return stripe.redirectToCheckout({ sessionId: session.id });
            })
            .then(function (result) {
                console.log("RESULT", result)
                // If redirectToCheckout fails due to a browser or network
                // error, you should display the localized error message to your
                // customer using error.message.
                if (result.error) {
                    alert(result.error.message);
                }
            })
            .catch(function (error) {
                console.error("API Error:", error);
            });
    }
</script>

<section>
    <div class="product">
        <img
            src="https://i.imgur.com/EHyR2nP.png"
            alt="The cover of Stubborn Attachments" />
        <div class="description">
            <h3>Stubborn Attachments</h3>
            <input bind:value={amount}/>
        </div>
    </div>
    <button on:click={checkout}>Checkout</button>
</section>

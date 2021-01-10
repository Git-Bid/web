<style lang="scss">
    @import url("https://fonts.googleapis.com/css2?family=Montserrat:wght@700&display=swap");
    @import "@primer/css/utilities/index.scss";
    @import url("https://fonts.googleapis.com/css2?family=Inter&display=swap");

    hero {
        display: grid;
        grid-template-columns: 1fr 1fr;
        width: 100%;
        background-color: rgb(240, 240, 240);
        margin: 0;
        height: 38vh;
    }
    h1,
    h2 {
        font-family: "Montserrat", sans-serif;
        text-align: left;
        text-transform: uppercase;
        margin-left: 30pt;
        margin-bottom: 10pt;
    }
    h1 {
        font-size: 40pt;
    }
    h2 {
        text-align: center;
        font-size: 25pt;
    }
    h3 {
        text-align: left;
        font-size: 25pt;
    }
    p {
        display: block;
        text-align: center;
        margin-left: 30pt;
        margin-bottom: 10pt;
        font-size: 16pt;
    }
    p2 {
        display: block;
        text-align: left;
        margin-left: 30pt;
        margin-bottom: 10pt;
        font-size: 16pt;
    }
    .Box-header {
        padding: 16px;
        margin: -1px -1px 0;
        background-color: $bg-gray-dark;
        border: 1px solid grey;
        border-top-left-radius: 6px;
        border-top-right-radius: 6px;
    }

    .js-navigation-container {
        background-color: #161b22;
        border: 1px solid grey;
    }
    inlineFlex {
        display: inline-flex;
        align-items: center;
        height: 100%;
    }
    list {
        margin-bottom: 0;
        margin-top: auto;
    }
    .btn-link {
        color: white;
    }
    grid {
        display: grid;
        grid-template-columns: 1fr 1fr;
        margin: 80pt;
    }
    section {
        margin-top: 20pt;
    }
    left {
        margin-left: 30pt;
    }
</style>

<main>
    <hero>
        <inlineFlex>
            <div>
                <h1>GitBid</h1>
                <p>helping sustain open source development</p>
            </div>
        </inlineFlex>
        <list>
            <!-- <p>place a bountie on any issue on any repo</p> -->
            <div
                class="application-main "
                data-commit-hovercards-enabled=""
                data-discussion-hovercards-enabled=""
                data-issue-and-pr-hovercards-enabled="">
                <main id="js-pjax-container" data-pjax-container="">
                    <div
                        class="page-content position-relative container-lg p-responsive">
                        <div
                            class="Box Box--responsive hx_Box--firstRowRounded0"
                            id="js-issues-toolbar"
                            data-pjax="">
                            <div class="Box-header d-flex flex-justify-between">
                                <div
                                    class="table-list-filters flex-auto d-none d-md-block no-wrap">
                                    <div
                                        class="table-list-header-toggle states flex-auto pl-0">
                                        <span
                                            class="btn-link selected"
                                            data-ga-click="Issues, Table state, Open">
                                            <svg
                                                class="octicon octicon-issue-opened"
                                                viewBox="0 0 16 16"
                                                version="1.1"
                                                width="16"
                                                height="16"
                                                aria-hidden="true"><path
                                                    fill-rule="evenodd"
                                                    d="M8 1.5a6.5 6.5 0 100 13 6.5 6.5 0 000-13zM0 8a8 8 0 1116 0A8 8 0 010 8zm9 3a1 1 0 11-2 0 1 1 0 012 0zm-.25-6.25a.75.75 0 00-1.5 0v3.5a.75.75 0 001.5 0v-3.5z" /></svg>
                                            19 Open
                                        </span>

                                        <span
                                            class="btn-link "
                                            data-ga-click="Issues, Table state, Closed">
                                            <svg
                                                class="octicon octicon-check"
                                                viewBox="0 0 16 16"
                                                version="1.1"
                                                width="16"
                                                height="16"
                                                aria-hidden="true"><path
                                                    fill-rule="evenodd"
                                                    d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z" /></svg>
                                            10 Closed
                                        </span>
                                    </div>
                                </div>
                            </div>
                            <div
                                class="js-navigation-container js-active-navigation-container"
                                style="margin: -1px;">
                                <div
                                    class="Box-row Box-row--focus-gray p-0 mt-0 js-navigation-item js-issue-row navigation-focus svelte-w4vpom">
                                    <div
                                        class="d-flex Box-row--drag-hide position-relative svelte-w4vpom">
                                        <div
                                            class="flex-shrink-0 pt-2 pl-3 svelte-w4vpom">
                                            <span
                                                class="tooltipped tooltipped-e"
                                                aria-label="Open issue"><svg
                                                    class="octicon octicon-issue-opened open"
                                                    viewBox="0 0 16 16"
                                                    version="1.1"
                                                    width="16"
                                                    height="16"
                                                    aria-hidden="true"><path
                                                        fill-rule="evenodd"
                                                        d="M8 1.5a6.5 6.5 0 100 13 6.5 6.5 0 000-13zM0 8a8 8 0 1116 0A8 8 0 010 8zm9 3a1 1 0 11-2 0 1 1 0 012 0zm-.25-6.25a.75.75 0 00-1.5 0v3.5a.75.75 0 001.5 0v-3.5z" /></svg></span>
                                        </div>
                                        <div
                                            class="flex-auto min-width-0 p-2 pr-3 pr-md-2 svelte-w4vpom">
                                            <a
                                                class="v-align-middle muted-link h4 pr-1 svelte-w4vpom">gitbid/api</a>
                                            <a
                                                id="issue_4_dylantmarsh_monokai-vibrant_link"
                                                class="link-gray-dark v-align-middle no-underline h4 js-navigation-open svelte-w4vpom"
                                                data-hovercard-type="issue"
                                                data-hovercard-url="/dylantmarsh/monokai-vibrant/issues/4/hovercard"
                                                href="/dylantmarsh/monokai-vibrant/issues/4">Add
                                                querying option</a>
                                            <div
                                                class="mt-1 text-small text-gray svelte-w4vpom">
                                                <span class="opened-by">#4
                                                    opened
                                                    <relative-time
                                                        datetime="2020-12-11T07:23:18Z"
                                                        class="no-wrap svelte-w4vpom"
                                                        title="Dec 10, 2020, 11:23 PM PST">
                                                        on Dec 10, 2020
                                                    </relative-time>
                                                    by
                                                    <a
                                                        class="muted-link svelte-w4vpom"
                                                        title="Open issues created by JacobZwang"
                                                        href="/issues?q=is%3Aissue+is%3Aopen+author%3AJacobZwang">JacobZwang</a></span>
                                                <span
                                                    class="d-none d-md-inline svelte-w4vpom" />
                                            </div>
                                        </div>
                                    </div>
                                </div>
                            </div>
                            <div
                                class="js-navigation-container js-active-navigation-container"
                                style="margin: -1px;">
                                <div
                                    class="Box-row Box-row--focus-gray p-0 mt-0 js-navigation-item js-issue-row navigation-focus svelte-w4vpom">
                                    <div
                                        class="d-flex Box-row--drag-hide position-relative svelte-w4vpom">
                                        <div
                                            class="flex-shrink-0 pt-2 pl-3 svelte-w4vpom">
                                            <span
                                                class="tooltipped tooltipped-e"
                                                aria-label="Open issue"><svg
                                                    class="octicon octicon-issue-opened open"
                                                    viewBox="0 0 16 16"
                                                    version="1.1"
                                                    width="16"
                                                    height="16"
                                                    aria-hidden="true"><path
                                                        fill-rule="evenodd"
                                                        d="M8 1.5a6.5 6.5 0 100 13 6.5 6.5 0 000-13zM0 8a8 8 0 1116 0A8 8 0 010 8zm9 3a1 1 0 11-2 0 1 1 0 012 0zm-.25-6.25a.75.75 0 00-1.5 0v3.5a.75.75 0 001.5 0v-3.5z" /></svg></span>
                                        </div>
                                        <div
                                            class="flex-auto min-width-0 p-2 pr-3 pr-md-2 svelte-w4vpom">
                                            <span style="float: left;">
                                                <a
                                                    class="v-align-middle muted-link h4 pr-1 svelte-w4vpom">gitbid/api</a>
                                                <a
                                                    id="issue_4_dylantmarsh_monokai-vibrant_link"
                                                    class="link-gray-dark v-align-middle no-underline h4 js-navigation-open svelte-w4vpom"
                                                    data-hovercard-type="issue"
                                                    data-hovercard-url="/dylantmarsh/monokai-vibrant/issues/4/hovercard"
                                                    href="/dylantmarsh/monokai-vibrant/issues/4">Add
                                                    querying option</a>
                                                <div
                                                    class="mt-1 text-small text-gray svelte-w4vpom">
                                                    <span class="opened-by">#4
                                                        opened
                                                        <relative-time
                                                            datetime="2020-12-11T07:23:18Z"
                                                            class="no-wrap svelte-w4vpom"
                                                            title="Dec 10, 2020, 11:23 PM PST">
                                                            on Dec 10, 2020
                                                        </relative-time>
                                                        by
                                                        <a
                                                            class="muted-link svelte-w4vpom"
                                                            title="Open issues created by JacobZwang"
                                                            href="/issues?q=is%3Aissue+is%3Aopen+author%3AJacobZwang">JacobZwang</a></span>
                                                    <span
                                                        class="d-none d-md-inline svelte-w4vpom" />
                                                </div>
                                            </span>
                                            <div
                                                style="height: 14pt; background-color: green; float: right; width: 50pt; border-radius: 4pt;">
                                                <span
                                                    style="color: white; font-size: 10pt; font-weight: bold; text-align: center; display: block; margin-top: 1pt;">$30</span>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                            </div>
                            <div
                                class="js-navigation-container js-active-navigation-container"
                                style="margin: -1px;">
                                <div
                                    class="Box-row Box-row--focus-gray p-0 mt-0 js-navigation-item js-issue-row navigation-focus svelte-w4vpom">
                                    <div
                                        class="d-flex Box-row--drag-hide position-relative svelte-w4vpom">
                                        <div
                                            class="flex-shrink-0 pt-2 pl-3 svelte-w4vpom">
                                            <span
                                                class="tooltipped tooltipped-e"
                                                aria-label="Open issue"><svg
                                                    class="octicon octicon-issue-opened open"
                                                    viewBox="0 0 16 16"
                                                    version="1.1"
                                                    width="16"
                                                    height="16"
                                                    aria-hidden="true"><path
                                                        fill-rule="evenodd"
                                                        d="M8 1.5a6.5 6.5 0 100 13 6.5 6.5 0 000-13zM0 8a8 8 0 1116 0A8 8 0 010 8zm9 3a1 1 0 11-2 0 1 1 0 012 0zm-.25-6.25a.75.75 0 00-1.5 0v3.5a.75.75 0 001.5 0v-3.5z" /></svg></span>
                                        </div>
                                        <div
                                            class="flex-auto min-width-0 p-2 pr-3 pr-md-2 svelte-w4vpom">
                                            <a
                                                class="v-align-middle muted-link h4 pr-1 svelte-w4vpom">gitbid/api</a>
                                            <a
                                                id="issue_4_dylantmarsh_monokai-vibrant_link"
                                                class="link-gray-dark v-align-middle no-underline h4 js-navigation-open svelte-w4vpom"
                                                data-hovercard-type="issue"
                                                data-hovercard-url="/dylantmarsh/monokai-vibrant/issues/4/hovercard"
                                                href="/dylantmarsh/monokai-vibrant/issues/4">Add
                                                querying option</a>
                                            <div
                                                class="mt-1 text-small text-gray svelte-w4vpom">
                                                <span class="opened-by">#4
                                                    opened
                                                    <relative-time
                                                        datetime="2020-12-11T07:23:18Z"
                                                        class="no-wrap svelte-w4vpom"
                                                        title="Dec 10, 2020, 11:23 PM PST">
                                                        on Dec 10, 2020
                                                    </relative-time>
                                                    by
                                                    <a
                                                        class="muted-link svelte-w4vpom"
                                                        title="Open issues created by JacobZwang"
                                                        href="/issues?q=is%3Aissue+is%3Aopen+author%3AJacobZwang">JacobZwang</a></span>
                                                <span
                                                    class="d-none d-md-inline svelte-w4vpom" />
                                            </div>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </main>
            </div>
        </list>
    </hero>
    <grid>
        <div>
            <h2>Developers</h2>
            <p>make money for for fixing important issues</p>
        </div>
        <div>
            <h2>Creators</h2>
            <p>pay to get what they need fixed faster</p>
        </div>
    </grid>
    <grid>
        <div>
            <h2>github integration</h2>
            <p>
                we created a chrom extension so you can create <br/>a view issues
                directly in github
            </p>
        </div>
        <div>
            <h2>open source</h2>
            <p>
                exisitng solutions are not open source, Gitbid is itself open
                source <br/>to promote open source development
            </p>
        </div>
    </grid>
</main>

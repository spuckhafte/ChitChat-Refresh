<script>
    import LeftSidebar from "./chat/leftSidebar.svelte";
</script>

<main>
    <div class="main-container" id="mainContainer">
        <div class="main-content" id="selectAndChat">
            <div class="left-sidebar" id="selectChat">
                <LeftSidebar/>
            </div>
            <div class="center-portion" id="chatPlatform"></div>
        </div>
        <div class="right-sidebar" id="userList"></div>
    </div>
</main>
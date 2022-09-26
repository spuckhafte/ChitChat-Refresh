<script>
    import CreateNewModal from '../common/createNewModal.svelte'
    let currentTab = 'Chat';
    let showModal = false;

    const showChats = () => currentTab = 'Chat';
    const showCommunities = () => currentTab = 'Community';

    let friendsList = [
        "sample friend"
    ]

    // const createNew = () => {
        
    // }
</script>

<div class="ls-content">
    <div class="self-view">
        <img src="https://avatars.dicebear.com/api/bottts/:$carl jhonson.png" alt="avatar">
        <span class="ls-username">Carl Jhonson</span>
    </div>
    <div class="chat-community-menu"></div>
    <div class="ls-controller">
        <div class="chat"on:click={showChats}>Chats</div>
        <div class="community" on:click={showCommunities}>Communities</div>
        <div class="new-process" on:click={() => showModal = !showModal}>New {currentTab}</div>
    </div>
    {#if showModal}
        <CreateNewModal friendsList={friendsList} bind:modalActive={showModal} />
    {/if}
</div>
<script>
    let currentTab = 'Chat';

    const showChats = () => currentTab = 'Chat';
    const showCommunities = () => currentTab = 'Community';
</script>

<div class="ls-content">
    <div class="self-view">
        <img src="https://avatars.dicebear.com/api/pixel-art-neutral/:$spuckhafte.png" alt="avatar">
        <span class="ls-username">Carl Jhonson</span>
    </div>
    <div class="chat-community-menu"></div>
    <div class="ls-controller">
        <div class="chat" on:click={showChats}>Chats</div>
        <div class="community" on:click={showCommunities}>Communities</div>
        <div class="new-process">New {currentTab}</div>
    </div>
</div>
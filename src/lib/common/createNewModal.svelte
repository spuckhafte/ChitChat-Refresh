<script>
    import Icon from '@iconify/svelte';
    export let friendsList;
    export let modalActive;
    let buttonFormActive = false;

    const getDp = username => `https://avatars.dicebear.com/api/bottts/:$${username}.png`;
</script>

<div class="modal-create-new">
    <div class="title">Friends</div>
    <div class="user-list">
        {#each friendsList as friend}
            <div class="show-user">
                <img src={getDp(friend)} alt="">
                <span class="user-name">{friend}</span>
            </div>
        {/each}
    </div>
    <button class="new-friend-btn" on:click={() => buttonFormActive = !buttonFormActive}>ADD FRIEND</button>
    {#if buttonFormActive && modalActive}
        <div class="add-friend">
            <!-- svelte-ignore a11y-autofocus -->
            <input autofocus type="text" placeholder="unique id"/>
            <button class="added"><Icon icon="charm:tick" color="#339989" /></button>
            <button class="cancel"><Icon icon="charm:cross" color="#734760"/></button>
        </div>
    {/if}
</div>

<style>

</style>
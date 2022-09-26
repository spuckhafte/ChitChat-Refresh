<script>
  import Router from 'svelte-spa-router'

  import Chat from './lib/chat.svelte'
  import Load from './lib/load.svelte';
  import Login from './lib/log/login.svelte';
  import Signup from './lib/log/signup.svelte';
</script>

<Router routes={{
  '/#': Load,
  '/': Load,
  '/chat': Chat,
  '/new': Login,
  '/new/login': Login,
  '/new/signup': Signup
}}/>
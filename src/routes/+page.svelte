<script>
  import Navbar from '$lib/components/layout/Navbar.svelte'
  import Modal from '$lib/components/ui/Modal.svelte'

  let { children } = $props()
</script>

<Navbar />
<Modal />

{@render children()}
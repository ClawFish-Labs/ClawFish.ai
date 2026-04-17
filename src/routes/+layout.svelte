<script lang="ts">
  import "./layout.css";
  let { children } = $props();
</script>

<div class="min-h-screen bg-black text-slate-200">
  {@render children()}
</div>
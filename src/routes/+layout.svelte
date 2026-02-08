<!--
  This is the LAYOUT file.
  It wraps every page on your site.
  Use it for headers, footers, and navigation that appear on all pages.
-->
<script>
  // Import global styles
  import '../app.scss';
  
  // Import site-wide components
  import SiteHeader from '$lib/components/SiteHeader.svelte';
  import SiteFooter from '$lib/components/SiteFooter.svelte';

  // In Svelte 5, we use $props() to receive the page content
  let { children } = $props();

  // Navigation links for the header (matching real NYCity News Service)
  const navLinks = [
  
  ];
</script>

<SiteHeader {navLinks} />

<main>
  <!-- This renders the current page's content -->
  {@render children()}
</main>

<SiteFooter />

<style>
  /* Styles here only apply to this layout */
  main {
    min-height: calc(100vh - 200px); /* Ensure footer stays at bottom */
  }
</style>
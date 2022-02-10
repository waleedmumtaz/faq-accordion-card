<script>
  import MainContent from './lib/main-content.svelte'
  import Footer from './lib/footer.svelte'
</script>

<svelte:head>
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link
    rel="preconnect"
    href="https://fonts.gstatic.com"
    crossorigin="anonymous"
  />
  <link
    href="https://fonts.googleapis.com/css2?family=Kumbh+Sans:wght@400;700&display=swap"
    rel="stylesheet"
  />
</svelte:head>

<div
  class="min-h-screen bg-gradient-to-b from-cstm-primary-gradient-soft-violet to-cstm-primary-gradient-soft-blue font-kumbh-sans flex flex-col"
>
  <MainContent />
  <Footer />
</div>

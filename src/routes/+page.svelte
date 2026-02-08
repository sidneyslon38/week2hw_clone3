<!--
  This is your page!
-->
<script>
  // Import all the news furniture components
  import ArticleHeader from '$lib/components/ArticleHeader.svelte';
  import ArticleBody from '$lib/components/ArticleBody.svelte';
  import Image from '$lib/components/Image.svelte';
  import RelatedLinks from '$lib/components/RelatedLinks.svelte';

  // Article metadata
  let headline = 'This process is getting easier!';
  let byline = 'Sidney Slon';
  let pubDate = '2026-02-08';

  // Related stories
  const relatedStories = [
    { headline: 'Related stories are cool, but I have nothing else I want to link.' },
  ];
</script>

<!-- This sets the page title in the browser tab -->
<svelte:head>
  <title>{headline} | Sid's Coding HW</title>
  <meta name="description" content="For Week 2 HW from Ben Welsh's 'Coding The News' class, I am finally getting the hang of downloading repository templates and working within the svelte files." />
</svelte:head>

<!-- Your page content goes here -->
<div class="container">
  
  <!-- Article Header: Headline, byline, and publication date -->
  <ArticleHeader
    {headline}
    {byline}
    {pubDate}
  />

  <!-- Lead Image: Animated gif of students at the journalism school -->
  <Image
    src="/angry-at-computer.gif"
    alt="Guy gets angry at his computer."
    caption="A guy getting angry at his computer."
    credit="Reddit"
  />

  <!-- Article Body: The main story text with proper typography -->
  <ArticleBody>
    <p>
      For Week 2 HW from Ben Welsh's 'Coding The News' class, I am finally getting the hang of downloading repository templates and working within the svelte files.
    </p>

    <p>
      During my first repo clone, I accidentally copied the original repository instead of using the template to make my own, which caused my some problems down the line. I ended up having to completely remake that one. Check it out <a href="https://sidneyslon38.github.io/week2hw_clone1/">here</a>.
    </p>

    <p>
      Then, I followed the better, easier path for my second repository clone. I practiced changing the color scheme slightly, although I still left it blue.
    </p>

    <p>
      You can check out the second project <a href="https://sidneyslon38.github.io/week2hw_clone2/">here</a>.
    </p>

    <p>
      I also didn't realize at first I had to "install npm" every time either.
    </p>

    <p>
      Now I know for next time.
    </p>

    <p>
      Enjoy!
    </p>

  </ArticleBody>

  <!-- Related Stories: Links to other articles -->
  <RelatedLinks
    title="Related Stories"
    links={relatedStories}
  />

</div>

<style>
  /* Styles here only apply to this page */
  .container {
    padding: var(--spacing-lg) var(--spacing-md);
  }
</style>
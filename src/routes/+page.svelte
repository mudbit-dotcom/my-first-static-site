This is you page!
<script>
  // Import all the news furniture components
  import ArticleHeader from '$lib/components/ArticleHeader.svelte';
  import ArticleBody from '$lib/components/ArticleBody.svelte';
  import ImageWithCaption from '$lib/components/ImageWithCaption.svelte';
  import RelatedLinks from '$lib/components/RelatedLinks.svelte';

  // Article metadata
  let headline = 'Cats and dogs: A love story';
  let byline = 'Niya Doyle';
  let pubDate = '2026-02-09';

  // Related stories
  const relatedStories = [
    { headline: 'How America\'s top news organizations escape rigid publishing systems to design beautiful data-driven stories on deadline.', href: 'https://palewi.re/docs/coding-the-news/' },
    { headline: 'How to install, configure and use Visual Studio Code, GitHub and Copilot', href: 'https://palewi.re/docs/coding-the-news/scripts/week-1/' },
  ];
</script>

<!-- This sets the page title in the browser tab -->
<svelte:head>
  <title>{headline} | NYCity News Service</title>
  <meta name="description" content="At the Craig Newmark Graduate School of Journalism at the City University of New York, change is in our DNA. That comes of being born in 2006, as the digital revolution was transforming our profession in ways none of us could have imagined." />
</svelte:head>

<!-- Your page content goes here -->
<div class="container">
  
  <!-- Article Header: Headline, byline, and publication date -->
  <ArticleHeader
    {headline}
    {byline}
    {pubDate}
  />

  <!-- Lead Image: CUNY Journalism School building -->
  <ImageWithCaption
    src="Pride.png"
    alt="Students in class"
    caption="Pride parade"
    credit="Craig Newmark Graduate School of Journalism"
  />

  <!-- Article Body: The main story text with proper typography -->
  <ArticleBody>
    <p>
      I love cats!
    </p>

    <p>
      I also love dogs!
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
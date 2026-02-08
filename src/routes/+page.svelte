<!--
@component
This is your page!
-->
<script>
  // Import all the news furniture components
  import ArticleHeader from '$lib/components/ArticleHeader.svelte';
  import ArticleBody from '$lib/components/ArticleBody.svelte';
  import Image from '$lib/components/Image.svelte';
  import RelatedLinks from '$lib/components/RelatedLinks.svelte';

  // Article metadata
  let headline = 'Breaking News: This is my fourth attempt at the homework.';
  let byline = 'NYCity News Service';
  let pubDate = '2026-01-31';

  // Related stories
  const relatedStories = [
    { headline: 'How America\'s top news organizations escape rigid publishing systems to design beautiful data-driven stories on deadline.', href: 'https://palewi.re/docs/coding-the-news/' },
    { headline: 'How to install, configure and use Visual Studio Code, GitHub and Copilot', href: 'https://palewi.re/docs/coding-the-news/scripts/week-1/' },
    { headline: "How to publish a website with Node.JS and GitHub Actions", href:"https://palewi.re/docs/coding-the-news/scripts/week-2/"},
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

  <!-- Lead Image: Animated gif of students at the journalism school -->
  <Image
    src="/example-photo.gif"
    alt="The Craig Newmark Graduate School of Journalism is at 219 West 40th Street in Midtown Manhattan."
    caption="Bellow you will find the complete lyrics to the theme song of the children's TV show Spongebob Squarepants."
    credit="Craig Newmark Graduate School of Journalism"
  />

  <!-- Article Body: The main story text with proper typography -->
  <ArticleBody>
    <p> Who lives in a pineapple under the sea? </p>
    <p> SpongeBob SquarePants </p>
    <p> Absorbent and yellow and porous is he </p>
    <p> SpongeBob SquarePants </p>
    <p> If nautical nonsense be something you wish </p>
    <p> SpongeBob SquarePants</p>
    <p> Then drop on the deck and flop like a fish </p>
    <p> SpongeBob SquarePants (Ready?) </p> 
    <p> SpongeBob SquarePants </p> 
    <p> SpongeBob SquarePants </p> 
    <p> SpongeBob SquarePants </p> 
    <p> SpongeBob SquarePants </p> 
    <p> Ah-hah, ha-ha-ha </p>
    <p> Ah-hah, ha-ha-har </p>
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
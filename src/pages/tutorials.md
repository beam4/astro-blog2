---
import BaseHead from '../components/BaseHead.astro';
import Header from '../components/Header.astro';
import { SITE_TITLE, SITE_DESCRIPTION } from '../consts';
// 1. The frontmatter prop gives access to frontmatter and other data
const { frontmatter } = Astro.props;
---


<html lang="en">
	<head>
		<BaseHead title={title} description={description} />
		<style>
			.title {
				font-size: 2em;
				margin: 0.25em 0 0;
			}
			hr {
				border-top: 1px solid #ddd;
				margin: 1rem 0;
			}
			.last-updated-on {
				font-style: italic;
			}
		</style>
	</head>

  <body>
		<Header />
		<main>
      <slot />
		</main>
	</body>
</html>

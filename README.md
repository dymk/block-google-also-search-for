# "People also search for" Blocker

#### Blocks the "People also search for" and "People also ask" boxes in Google search using XPath queries.

## About

The "People also search for" box pops up dynamically, and after a slight delay, causing everything under it to reposition itself. This looks for those elements and removes them.

## How to Install

This is a userscript, so install using your favorite userscript host, such as Greasemonkey or Tampermonkey.

## Technical

The elements are queried using XPath, rather than using CSS class selectors. Many existing scripts and blockers for the "People also search for" box will fail after some time, as the CSS selector names that Google uses are minified/obfuscated/generated, and thus change over time.

Using an XPath query should prove more resilient, as it looks at the text of HTML attributes (which doesn't change, at least as often).

Google may decide to change the underlying structure of the HTML on the Search Results page, which may break this plugin in the future, but it should be a matter of "just" recomputing how many `div` elements to select upwards.

## Contributing

1. Fork the repository
2. Open a pull request
3. I'll merge it if it looks good

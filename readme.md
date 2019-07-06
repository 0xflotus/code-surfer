# Code Surfer <🏄/>

![](https://flat.badgen.net/npm/v/code-surfer) ![](https://flat.badgen.net/travis/pomber/code-surfer)

React component for scrolling, zooming and highlighting code.

> If you like this project consider [backing my open source work on Patreon!](https://patreon.com/pomber)  
> And follow [@pomber](https://twitter.com/pomber) on twitter for updates.

---

**Version 2 of Code Surfer is coming soon!**  
Check the demos [here](https://twitter.com/pomber/status/1140640434613555201) and [here](https://twitter.com/pomber/status/1144222078696136704). And the [v2 PR](https://github.com/pomber/code-surfer/pull/58).  
You can try it now with `npm init code-surfer-deck`.

---

## How to use with [mdx-deck](https://github.com/jxnblk/mdx-deck)

<div align="center">
<a href="https://code-surfer.netlify.com/sample/">
<img alt="sample" src="https://raw.githubusercontent.com/pomber/code-surfer/master/other/sample.gif" />
</a>
<div><a href="https://code-surfer.netlify.com/sample/">(demo)</a></div>
</div>

Add the dependency (and `raw-loader` if you want to load the code from a file):

```bash
$ yarn add --dev mdx-deck-code-surfer raw-loader
```

And then use it from your `.mdx`:

```jsx
---

import { CodeSurfer } from "mdx-deck-code-surfer"

<CodeSurfer
  title="Some Title"
  code={require("!raw-loader!./my-snippet.js")}
  lang="javascript"
  showNumbers={false}
  dark={false}
  steps={[
    { notes: "Start with this note"},
    { lines: [6], notes: "Note for the first step" },
    { range: [5, 9] },
    { tokens: { 9: [3, 4, 5] }, notes: "Note for the third step" }
  ]}
/>

---
```

A list of available languages can be found [here](https://github.com/FormidableLabs/prism-react-renderer/blob/master/src/vendor/prism/includeLangs.js) and it will default to `jsx`

More options:

- [Theming](https://code-surfer.netlify.com/theming/)

## Related / Credits

- [mdx-deck](https://github.com/jxnblk/mdx-deck)
- [prism-react-renderer](https://github.com/FormidableLabs/prism-react-renderer)
- [spectacle-code-slide](https://github.com/jamiebuilds/spectacle-code-slide)
- [prism](https://github.com/PrismJS/prism)

## Contributing

Release new versions with:

```bash
$ yarn build:packages
$ npx lerna publish
```

## License

Released under MIT license.

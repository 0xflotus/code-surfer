# Code Surfer <🏄/>

![](https://flat.badgen.net/npm/v/code-surfer)
[![Contribute with Forkbox](<https://flat.badgen.net/badge/PRs/ForkBox%20(experimental)/222>)](https://forkbox.co/f/pomber/code-surfer)

React component for scrolling, zooming and highlighting code.

## How to use with [mdx-deck](https://github.com/jxnblk/mdx-deck)

<div align="center">
<a href="https://mdx-deck-code-surfer.netlify.com/">
<img alt="sample" src="https://raw.githubusercontent.com/pomber/code-surfer/master/other/sample.gif" />
</a>
<div><a href="https://mdx-deck-code-surfer.netlify.com/">(demo)</a></div>
</div>

Add the dependency:

```bash
$ yarn add mdx-deck-code-surfer
```

And then use it from your `.mdx`:

```
import { CodeSurfer } from "mdx-deck-code-surfer";

<CodeSurfer
  title="Some Title"
  notes="Start with this note"
  code={require("raw-loader!./my-snippet.jsx")}
  showNumbers={true}
  steps={[
    { lines: [6], notes: "Note for the first step" },
    { range: [5, 9] },
    { tokens: { 9: [3, 4, 5] }, notes: "Note for the third step" }
  ]}
/>
```

## Related / Credits

- [mdx-deck](https://github.com/jxnblk/mdx-deck)
- [prism-react-renderer](https://github.com/FormidableLabs/prism-react-renderer)
- [spectacle-code-slide](https://github.com/jamiebuilds/spectacle-code-slide)
- [prism](https://github.com/PrismJS/prism)

## License

Released under MIT license.

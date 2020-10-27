# rehype-all-the-thumbs-obviate
Supporting [`rehype-all-the-thumbs`](https://github.com/ericdmoore/rehype-all-the-thumbs) by preventing needless work

> Obviate: (Great word right?) It's defined as : To keep from happening or render unnecessary. Which is what we are doing to the backlog of items.

## Overview

_Configuration_:
- read file closure ? 
- `{ read: async (s) => Promise<boolean> }`

_Input_:
- a HAST tree
- vfile with added `newAssets` key added to the object

_Output_:
- vfile with `newAssets` array filtered to only hold files that need to be generated based on the read function results

## Pairs Well With:

- [rehype-all-the-thumbs](https://github.com/ericdmoore/rehype-all-the-thumbs) ...like putting on velcro shoes
- [rehype-all-the-thumbs-curate](https://github.com/ericdmoore/rehype-all-the-thumbs-curate) (DOM -> data.srcs)
- [rehype-all-the-thumbs-create](https://github.com/ericdmoore/rehype-all-the-thumbs-create) (data.srcs -> data.newAssets)
- [rehype-all-the-thumbs-manipulate](https://github.com/ericdmoore/rehype-all-the-thumbs-manipulate) (data.newAssets -> DOM)
- [vfile-newAssets-generate](https://github.com/ericdmoore/vfile-newAssets-generate) (data.newAssets -> Side Effect Funtion to create the file)

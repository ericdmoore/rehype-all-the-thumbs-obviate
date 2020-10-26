# rehype-all-the-thumbs-obviate
Supporting [`rehype-all-the-thumbs`](https://github.com/ericdmoore/rehype-all-the-thumbs) by preventing needless work

## Overview

_Configuration_:
- read file closure ? 
- `{ read: async (s) => Promise<boolean> }`

_Input_:
- a HAST tree
- vfile with added `newAssets` key added to the object

_Output_:
- vfile with `newAssets` array filtered to only hold files that need to be generated based on the read function results

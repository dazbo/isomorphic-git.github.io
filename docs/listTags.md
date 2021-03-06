---
title: listTags
sidebar_label: listTags
---

List tags

| param           | type [= default]           | description                                                                                               |
| --------------- | -------------------------- | --------------------------------------------------------------------------------------------------------- |
| core            | string = 'default'         | The plugin core identifier to use for plugin injection                                                    |
| fs [deprecated] | FileSystem                 | The filesystem containing the git repo. Overrides the fs provided by the [plugin system](./plugin_fs.md). |
| dir             | string                     | The [working tree](dir-vs-gitdir.md) directory path                                                       |
| **gitdir**      | string = join(dir,'.git')  | The [git directory](dir-vs-gitdir.md) path                                                                |
| return          | Promise\<Array\<string\>\> | Resolves successfully with an array of tag names                                                          |

Example Code:

```js live
let tags = await git.listTags({ dir: '$input((/))' })
console.log(tags)
```

---
title: currentBranch
sidebar_label: currentBranch
---

Get the name of the branch currently pointed to by .git/HEAD

| param           | type [= default]              | description                                                                                               |
| --------------- | ----------------------------- | --------------------------------------------------------------------------------------------------------- |
| core            | string = 'default'            | The plugin core identifier to use for plugin injection                                                    |
| fs [deprecated] | FileSystem                    | The filesystem containing the git repo. Overrides the fs provided by the [plugin system](./plugin_fs.md). |
| dir             | string                        | The [working tree](dir-vs-gitdir.md) directory path                                                       |
| **gitdir**      | string = join(dir,'.git')     | The [git directory](dir-vs-gitdir.md) path                                                                |
| fullname        | boolean = false               | Return the full path (e.g. "refs/heads/master") instead of the abbreviated form.                          |
| return          | Promise\<(string|undefined)\> | The name of the current branch or undefined if the HEAD is detached.                                      |

Example Code:

```js live
// Get the current branch name
let branch = await git.currentBranch({ dir: '$input((/))', fullname: $input((false)) })
console.log(branch)
```

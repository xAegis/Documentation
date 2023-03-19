---
description: 'Here''s how to use the system namespace :'
---

# 💻 System

## Functions:

## exec

`system.exec(data: string)`

| Name     | Type       | Description |
| -------- | ---------- | ----------- |
| **data** | **string** | Cmd Command |

<pre class="language-lua"><code class="lang-lua">-> Usage
<strong>system.exec("start cmd.exe")
</strong></code></pre>

## `shellexec`

`system.shellexec(operation: string, file: string, parameters: string, directory: string, int: show)`

| Name      | Type   |                      |
| --------- | ------ | -------------------- |
| operation | string | Action name          |
| file      | string | Path                 |
| params    | string | Additional parameter |
| directory | string | Default path         |
| show      | int    | Console visibility   |

This function is basically a ShellExecuteA for more information click [here](https://www.delftstack.com/howto/cpp/cpp-shellexecute/).

```lua
--> Usage
system.shellexec("open", "calc.exe", nil, nil, 1)
```

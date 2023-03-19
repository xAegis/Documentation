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

```lua
system.exec("start cmd.exe")
```

## `shellexec`

`system.shellexec(operation: string, file: string, parameters: string, directory: string, show: int)`

| Name      | Type   |                      |
| --------- | ------ | -------------------- |
| operation | string | Action name          |
| file      | string | Path                 |
| params    | string | Additional parameter |
| directory | string | Default path         |
| show      | int    | Console visibility   |

This function is basically a ShellExecuteA for more information click [here](https://www.delftstack.com/howto/cpp/cpp-shellexecute/).

```lua
system.shellexec("open", "calc.exe", nil, nil, 1)
```

## delay

`system.delay(time: int)`

| Name     | Type    | Description                 |
| -------- | ------- | --------------------------- |
| **time** | **int** | The time to wait in seconds |

```lua
system.delay(3)
```

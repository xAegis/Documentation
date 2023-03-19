---
description: 'Here''s how to use the process namespace :'
---

# ⚙ Process

## Functions:

## getprocid

`local procID = process.getprocid(name: string)`

| Name     | Type       | Description  |
| -------- | ---------- | ------------ |
| **name** | **string** | Process Name |

```lua
local procID = process.getprocid("test.exe")
```

## gethprocess

`local hprocess = process.gethprocess(procID: int)`

| Name       | Type    | Description |
| ---------- | ------- | ----------- |
| **procID** | **int** | Process ID  |

```lua
local procID = process.getprocid("test.exe")
local hProcess = process.gethprocess(procID)
print.info(string.format("hProcess : %p", hProcess))
```

## getmodulebase

`local moduleBase = process.getmodulebase(procID: int, name: string)`

| Name       | Type    | Description  |
| ---------- | ------- | ------------ |
| **procID** | **int** | Process ID   |
| name       | string  | Process Name |

```lua
local procID = process.getprocid("gmod.exe")
local moduleBase = process.getmodulebase(procID, "client.dll")
```

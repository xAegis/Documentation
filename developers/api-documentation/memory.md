---
description: 'Here''s how to use the memory namespace :'
---

# 🔋 Memory

## Functions:

## patch

`memory.patch(dst: uint, src: string, size: int, hProcess: handle)`

| Name         | Type       |                                    |
| ------------ | ---------- | ---------------------------------- |
| **dst**      | **uint**   | Destination                        |
| **src**      | **string** | Instruction                        |
| **size**     | **int**    | Size                               |
| **hProcess** | **handle** | [hProcess](process.md#gethprocess) |

```lua
local procID = process.getprocid("example.exe")
local hProcess = process.gethprocess(procID)
local moduleBase = process.getmodulebase(procID, "example.dll")

memory.patch(moduleBase + 0x8c60, "\x65\x78\x61\x6D\x70\x6C\x65", 0x1f, hProcess)
```

## nop

`memory.nop(dst: uint, size: int , hprocess : handle)`

| Name         | Type       |                                    |
| ------------ | ---------- | ---------------------------------- |
| **dst**      | **uint**   | Destination                        |
| **size**     | **int**    | Size                               |
| **hProcess** | **handle** | [hProcess](process.md#gethprocess) |

```lua
local procID = process.getprocid("example.exe")
local hProcess = process.gethprocess(procID)
local moduleBase = process.getmodulebase(procID, "example.dll")

memory.nop(moduleBase + 0x8c60, 0x1f, hProcess)
```

## inject

`memory.inject(procID: int, file: string)`

| Name       | Type    |            |
| ---------- | ------- | ---------- |
| **procID** | **int** | Process ID |
| **file**   | **int** | DLL Path   |

---
description: 'A Basic Patcher example :'
---

# 🔧 Basic Patcher

```lua
local procID = process.getprocid("example.exe")

print.wait("Waiting for the process !")

repeat
    procID = process.getprocid("example.exe")
until( procID > 0 )

print.success("Process found !")

print.info("procid : " .. procID)

local hProcess = process.gethprocess(procID)
print.info(string.format("hProcess : %p", hProcess))

local mainModule = process.getmodulebase(procID, "example.dll")
print.info("MainModule : " .. mainModule)

memory.patch(mainModule + 0x8c60, "\x65\x78\x61\x6D\x70\x6C\x65", 0x1f, hProcess)
memory.nop(mainModule + 0x8c60, 0x5f, hProcess)
```

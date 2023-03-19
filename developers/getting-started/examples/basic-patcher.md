---
description: 'A Basic Patcher example :'
---

# 🔧 Basic Patcher

```lua
print.wait("Waiting for the process !")

local procID = process.getprocid("example.exe")
repeat
    procID = process.getprocid("example.exe")
until( procID > 0 )

print.success("Process found !")
print.info("Process ID : " .. procID)

local hProcess = process.gethprocess(procID)
print.info(string.format("hProcess : %p", hProcess))

print.wait("Waiting for the module !")

local mainModule = process.getmodulebase(procID, "example.dll")
repeat
    mainModule = process.getmodulebase(procID, "example.dll")
until( mainModule > 0 )

print.success("Module found !")
print.info("Module : " .. mainModule)

system.delay(1)

memory.patch(mainModule + 0x1337, "\x68\x65\x6C\x6C\x6F\x20\x75", 0x1337, hProcess)
print.success("Auth Bypassed !")
```

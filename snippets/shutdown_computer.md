---
title: shutdown_computer
tags: shellcommand,intermediate
---

Shutdown computer in a duration given by the user and message to be displayed stating the reason for shutdown.

Use ```success()``` to test and run the command if it's valid and prints an error message if it's not valid.

```jl
function shutdown_computer(time,message)
  command=`cmd /c shutdown/s /t $time /c $message`
  if success(command)==true
  return command
  else
  println("System error just occured!")
end
end
```

```jl
shutdown_computer(400,"Shutingdown") # Dialogue box appear showing "Shutingdown" and computer shutdown in 400sec.
```

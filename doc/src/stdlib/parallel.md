# Tasks and multi-threading

## Tasks

```@docs
Core.Task
Base.current_task
Base.istaskdone
Base.istaskstarted
Base.yield
Base.yieldto
Base.task_local_storage(::Any)
Base.task_local_storage(::Any, ::Any)
Base.task_local_storage(::Function, ::Any, ::Any)
Base.Condition
Base.notify
Base.schedule
Base.@schedule
Base.@task
Base.sleep
Base.Channel
Base.put!(::Channel, ::Any)
Base.take!(::Channel)
Base.isready(::Channel)
Base.fetch(::Channel)
Base.close(::Channel)
Base.bind(c::Channel, task::Task)
Base.asyncmap
Base.asyncmap!
```


## Multi-Threading

This experimental interface supports Julia's multi-threading capabilities. Types and functions
described here might (and likely will) change in the future.

```@docs
Base.Threads.threadid
Base.Threads.nthreads
Base.Threads.@threads
Base.Threads.Atomic
Base.Threads.atomic_cas!
Base.Threads.atomic_xchg!
Base.Threads.atomic_add!
Base.Threads.atomic_sub!
Base.Threads.atomic_and!
Base.Threads.atomic_nand!
Base.Threads.atomic_or!
Base.Threads.atomic_xor!
Base.Threads.atomic_max!
Base.Threads.atomic_min!
Base.Threads.atomic_fence
```

## ccall using a threadpool (Experimental)

```@docs
Base.@threadcall
```

## Synchronization Primitives

```@docs
Base.Threads.AbstractLock
Base.lock
Base.unlock
Base.trylock
Base.islocked
Base.ReentrantLock
Base.Threads.Mutex
Base.Threads.SpinLock
Base.Threads.RecursiveSpinLock
Base.Semaphore
Base.acquire
Base.release
```


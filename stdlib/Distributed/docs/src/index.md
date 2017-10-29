# Distributed Computing

```@docs
Base.addprocs
Base.nprocs
Base.nworkers
Base.procs()
Base.procs(::Integer)
Base.workers
Base.rmprocs
Base.interrupt
Base.myid
Base.pmap
Base.RemoteException
Base.Future
Base.RemoteChannel(::Integer)
Base.RemoteChannel(::Function, ::Integer)
Base.wait
Base.fetch(::Any)
Base.remotecall(::Any, ::Integer, ::Any...)
Base.remotecall_wait(::Any, ::Integer, ::Any...)
Base.remotecall_fetch(::Any, ::Integer, ::Any...)
Base.remote_do(::Any, ::Integer, ::Any...)
Base.put!(::RemoteChannel, ::Any...)
Base.put!(::Future, ::Any)
Base.take!(::RemoteChannel, ::Any...)
Base.isready(::RemoteChannel, ::Any...)
Base.isready(::Future)
Base.WorkerPool
Base.CachingPool
Base.default_worker_pool
Base.clear!(::CachingPool)
Base.remote
Base.remotecall(::Any, ::Base.Distributed.AbstractWorkerPool, ::Any...)
Base.remotecall_wait(::Any, ::Base.Distributed.AbstractWorkerPool, ::Any...)
Base.remotecall_fetch(::Any, ::Base.Distributed.AbstractWorkerPool, ::Any...)
Base.remote_do(::Any, ::Base.Distributed.AbstractWorkerPool, ::Any...)
Base.timedwait
Base.@spawn
Base.@spawnat
Base.@fetch
Base.@fetchfrom
Base.@async
Base.@sync
Base.@parallel
Base.@everywhere
Base.clear!(::Any, ::Any; ::Any)
Base.remoteref_id
Base.channel_from_id
Base.worker_id_from_socket
Base.cluster_cookie()
Base.cluster_cookie(::Any)
```

## Cluster Manager Interface

This interface provides a mechanism to launch and manage Julia workers on different cluster environments.
There are two types of managers present in Base: `LocalManager`, for launching additional workers on the
same host, and `SSHManager`, for launching on remote hosts via `ssh`. TCP/IP sockets are used to connect
and transport messages between processes. It is possible for Cluster Managers to provide a different transport.

```@docs
Base.launch
Base.manage
Base.kill(::ClusterManager, ::Int, ::WorkerConfig)
Base.connect(::ClusterManager, ::Int, ::WorkerConfig)
Base.init_worker
Base.start_worker
Base.process_messages
```

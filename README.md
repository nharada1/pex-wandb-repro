# Repro

To reproduce, run `./pants run src/main.py`

On my machine:

```
Traceback (most recent call last):
  File "/home/user/.cache/pants/named_caches/pex_root/venvs/e33dbad2e381237c2ef87dd830f8fbcc73be777f/7898379b30005666861db5e178f56a2477d285aa/lib/python3.9/site-packages/wandb/sdk/wandb_init.py", line 1075, in i
nit
    wi.setup(kwargs)
  File "/home/user/.cache/pants/named_caches/pex_root/venvs/e33dbad2e381237c2ef87dd830f8fbcc73be777f/7898379b30005666861db5e178f56a2477d285aa/lib/python3.9/site-packages/wandb/sdk/wandb_init.py", line 165, in se
tup
    self._wl = wandb_setup.setup()
  File "/home/user/.cache/pants/named_caches/pex_root/venvs/e33dbad2e381237c2ef87dd830f8fbcc73be777f/7898379b30005666861db5e178f56a2477d285aa/lib/python3.9/site-packages/wandb/sdk/wandb_setup.py", line 312, in s
etup
    ret = _setup(settings=settings)
  File "/home/user/.cache/pants/named_caches/pex_root/venvs/e33dbad2e381237c2ef87dd830f8fbcc73be777f/7898379b30005666861db5e178f56a2477d285aa/lib/python3.9/site-packages/wandb/sdk/wandb_setup.py", line 307, in _
setup
    wl = _WandbSetup(settings=settings)
  File "/home/user/.cache/pants/named_caches/pex_root/venvs/e33dbad2e381237c2ef87dd830f8fbcc73be777f/7898379b30005666861db5e178f56a2477d285aa/lib/python3.9/site-packages/wandb/sdk/wandb_setup.py", line 293, in _
_init__
    _WandbSetup._instance = _WandbSetup__WandbSetup(settings=settings, pid=pid)
  File "/home/user/.cache/pants/named_caches/pex_root/venvs/e33dbad2e381237c2ef87dd830f8fbcc73be777f/7898379b30005666861db5e178f56a2477d285aa/lib/python3.9/site-packages/wandb/sdk/wandb_setup.py", line 106, in _
_init__
    self._setup()
  File "/home/user/.cache/pants/named_caches/pex_root/venvs/e33dbad2e381237c2ef87dd830f8fbcc73be777f/7898379b30005666861db5e178f56a2477d285aa/lib/python3.9/site-packages/wandb/sdk/wandb_setup.py", line 234, in _
setup
    self._setup_manager()
  File "/home/user/.cache/pants/named_caches/pex_root/venvs/e33dbad2e381237c2ef87dd830f8fbcc73be777f/7898379b30005666861db5e178f56a2477d285aa/lib/python3.9/site-packages/wandb/sdk/wandb_setup.py", line 265, in _
setup_manager
    self._manager = wandb_manager._Manager(
  File "/home/user/.cache/pants/named_caches/pex_root/venvs/e33dbad2e381237c2ef87dd830f8fbcc73be777f/7898379b30005666861db5e178f56a2477d285aa/lib/python3.9/site-packages/wandb/sdk/wandb_manager.py", line 111, in
 __init__
    self._service.start()
  File "/home/user/.cache/pants/named_caches/pex_root/venvs/e33dbad2e381237c2ef87dd830f8fbcc73be777f/7898379b30005666861db5e178f56a2477d285aa/lib/python3.9/site-packages/wandb/sdk/service/service.py", line 119,
in start
    self._launch_server()
  File "/home/user/.cache/pants/named_caches/pex_root/venvs/e33dbad2e381237c2ef87dd830f8fbcc73be777f/7898379b30005666861db5e178f56a2477d285aa/lib/python3.9/site-packages/wandb/sdk/service/service.py", line 109,
in _launch_server
    internal_proc = subprocess.Popen(
  File "/home/user/Software/mambaforge/lib/python3.9/subprocess.py", line 951, in __init__
    self._execute_child(args, executable, preexec_fn, close_fds,
  File "/home/user/Software/mambaforge/lib/python3.9/subprocess.py", line 1821, in _execute_child
    raise child_exception_type(errno_num, err_msg, err_filename)
PermissionError: [Errno 13] Permission denied: '/tmp/pants-sandbox-6kYP6O/src.pex'
wandb: ERROR Abnormal program exit
```
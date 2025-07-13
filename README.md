Low Memory Monitor SELinux Policy
=================================

This is the SELinux policy for Low Memory Monitor.

## About Low Memory Monitor

The Low Memory Monitor is an early boot daemon that will monitor memory
pressure information coming from the kernel, and, when memory pressure means
that memory isn't as readily available and would cause interactivity problems, would:

- send D-Bus signals to user-space applications when memory is running low,
- if configured to do so and memory availability worsens, activate the kernel's
   [OOM](https://en.wikipedia.org/wiki/Out_of_memory) killer.

## Application Sources

See: https://gitlab.freedesktop.org/hadess/low-memory-monitor
See: https://src.fedoraproject.org/rpms/low-memory-monitor

## Building

```
$ cd /path/to/low-memory-monitor-selinux
$ make -f /usr/share/selinux/devel/Makefile
```

## To-do
 * Generate manpage
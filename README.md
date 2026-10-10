Your driver store is full of GPU packages you already replaced.
UtilDriver scans Windows' driver store with pnputil, finds every NVIDIA and AMD package sitting in it, and lets you remove the ones you don't need — without digging through Device Manager.
How it works
UtilDriver runs pnputil /enum-drivers and reads every published package, matching the provider name against NVIDIA and AMD, then deduplicating by INF filename.


Pick what to remove
Tick the packages you want gone. Each row shows the provider and the exact INF reference, so you know precisely what you're selecting.

After a confirmation prompt, UtilDriver calls pnputil /delete-driver /uninstall /force for each package and reports success or failure per item.

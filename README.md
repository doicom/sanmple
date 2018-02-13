# sanmple
I: Setting /OpenNetworkLinux/builds/amd64/rootfs/builds/rootfs-amd64.d/lib64 -> /OpenNetworkLinux/builds/amd64/rootfs/builds/rootfs-amd64.d/lib symbolic link.
Getting package lists: apt-get  -o Apt::Architecture=amd64 -o Dir::Etc::TrustedParts=/OpenNetworkLinux/builds/amd64/rootfs/builds/rootfs-amd64.d/etc/apt/trusted.gpg.d -o Dir::Etc::Trusted=/OpenNetworkLinux/builds/amd64/rootfs/builds/rootfs-amd64.d/etc/apt/trusted.gpg.d/trusted.gpg -o Apt::Get::AllowUnauthenticated=true -o Apt::Get::Download-Only=true -o Apt::Install-Recommends=false -o Dir=/OpenNetworkLinux/builds/amd64/rootfs/builds/rootfs-amd64.d/ -o Dir::Etc=/OpenNetworkLinux/builds/amd64/rootfs/builds/rootfs-amd64.d/etc/apt/ -o Dir::Etc::Parts=/OpenNetworkLinux/builds/amd64/rootfs/builds/rootfs-amd64.d/etc/apt/apt.conf.d/ -o Dir::Etc::PreferencesParts=/OpenNetworkLinux/builds/amd64/rootfs/builds/rootfs-amd64.d/etc/apt/preferences.d/ -o APT::Default-Release=* -o Dir::State=/OpenNetworkLinux/builds/amd64/rootfs/builds/rootfs-amd64.d/var/lib/apt/ -o Dir::State::Status=/OpenNetworkLinux/builds/amd64/rootfs/builds/rootfs-amd64.d/var/lib/dpkg/status -o Dir::Cache=/OpenNetworkLinux/builds/amd64/rootfs/builds/rootfs-amd64.d/var/cache/apt/ update
Ign copy: ./ InRelease
Ign copy: ./ InRelease
Ign copy: ./ Release.gpg                     
Ign copy: ./ Release.gpg                     
Ign copy: ./ Release                         
Ign copy: ./ Release                         
Get:1 copy: ./ Packages [8118 B]             
Ign copy: ./ Translation-en                                                    
Get:2 copy: ./ Packages [134 kB]
Ign copy: ./ Translation-en                        
Ign http://127.0.0.1:3142 jessie InRelease                          
Ign http://127.0.0.1:3142 unstable InRelease
Ign http://127.0.0.1:3142 jessie Release.gpg
Ign http://127.0.0.1:3142 unstable Release.gpg
Ign http://127.0.0.1:3142 jessie Release
Ign http://127.0.0.1:3142 unstable Release
Err http://127.0.0.1:3142 jessie/main amd64 Packages                           
  401  Unauthorized
Ign http://127.0.0.1:3142 jessie/main Translation-en       
Err http://127.0.0.1:3142 unstable/main amd64 Packages
  401  Unauthorized
Ign http://127.0.0.1:3142 unstable/main Translation-en
Fetched 142 kB in 0s (710 kB/s)
W: Failed to fetch http://127.0.0.1:3142/mirrors.kernel.org/debian/dists/jessie/main/binary-amd64/Packages  401  Unauthorized

W: Failed to fetch http://127.0.0.1:3142/apt.opennetlinux.org/debian/dists/unstable/main/binary-amd64/Packages  401  Unauthorized

E: Some index files failed to download. They have been ignored, or old ones used instead.
apt update failed. Exit value: 100
DEBUG:onlrfs:Executing:sudo mount -t devtmpfs dev rootfs-amd64.d/dev
DEBUG:onlrfs:Executing:sudo mount -t proc proc rootfs-amd64.d/proc
mount: mount point rootfs-amd64.d/proc does not exist
DEBUG:onlrfs:Executing:sudo umount -l rootfs-amd64.d/dev rootfs-amd64.d/proc
umount: rootfs-amd64.d/proc: mountpoint not found
ERROR:onlrfs:Could not mount proc in new filesystem.
/OpenNetworkLinux/make/rfs.mk:36: recipe for target 'RFS' failed
make[3]: *** [RFS] Error 1
Traceback (most recent call last):
  File "/OpenNetworkLinux/tools/onlpm.py", line 1265, in <module>
    pm.build(p)
  File "/OpenNetworkLinux/tools/onlpm.py", line 951, in build
    products = pg.build(dir_=dir_)
  File "/OpenNetworkLinux/tools/onlpm.py", line 610, in build
    self.gmake_locked("", 'Build')
  File "/OpenNetworkLinux/tools/onlpm.py", line 585, in gmake_locked
    ex=OnlPackageError('%s failed.' % operation))
  File "/OpenNetworkLinux/tools/onlu.py", line 70, in execute
    raise ex
onlpm.OnlPackageError: 'Build failed.'
/OpenNetworkLinux/make/pkg.mk:30: recipe for target 'pkgall' failed
make[2]: *** [pkgall] Error 1
/OpenNetworkLinux/make/subdirs.mk:15: recipe for target 'all' failed
make[1]: *** [all] Error 1
make[1]: Leaving directory '/OpenNetworkLinux/builds/amd64'
Makefile:23: recipe for target 'amd64' failed
make: *** [amd64] Error 2



















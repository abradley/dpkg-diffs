`dpkg-diffs performs what Redhat's `rpm --verify` does and a bit more.

The script will assure that the installed package files are
identical to its downloaded or cached package.

Also, it will show any new or uncontrolled files in directories made by such package(s).

Example run of dpkg-diffs against Chrony time server package.

    # ./dpkg-diffs -d chrony
    No package matching "chrony" found in cache.
    [Working] Get:1 http://ftp-nyc.osuosl.org/debian bullseye/main amd64 chrony amd64 4.0-8 [286 kB]
    chrony 14.4 kB/286 kB
    Fetched 286 kB in 0s (2,683 kB/s)
    Not present: /etc/chrony/conf.d
    Not present: /etc/chrony/conf.d/README
    Not present: /etc/chrony/sources.d
    Not present: /etc/chrony/sources.d/README
    Current file is symlink but package file is not: /lib
    Exists but cannot read: /usr/share/chrony/chrony.keys
    #
    echo $?
    0


# btrfs property

> Get, set, or list properties for a BTRFS filesystem object (files, directories, subvolumes, filesystems, or devices).
> More information: <https://btrfs.readthedocs.io/en/latest/btrfs-property.html>.

- List available properties (and descriptions) for the given btrfs object:

`sudo btrfs {{[p|property]}} {{[l|list]}} {{path/to/btrfs_object}}`

- Get all properties for the given btrfs object:

`sudo btrfs {{[p|property]}} {{[g|get]}} {{path/to/btrfs_object}}`

- Get the `label` property for the given btrfs filesystem or device:

`sudo btrfs {{[p|property]}} {{[g|get]}} {{path/to/btrfs_filesystem}} label`

- Get all object type-specific properties for the given btrfs filesystem or device:

`sudo btrfs {{[p|property]}} {{[g|get]}} -t {{subvol|filesystem|inode|device}} {{path/to/btrfs_filesystem}}`

- Set the `compression` property for a given btrfs inode (either a file or directory):

`sudo btrfs {{[p|property]}} {{[s|set]}} {{path/to/btrfs_inode}} compression {{zstd|zlib|lzo|none}}`

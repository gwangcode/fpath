# fpath
a convenient lib for path &amp; file name operations

usage:
# import fpath
import fpath 

# create fpath object with a path
p=fpath.fpath('~/Documents/abc.def')

# p.path records the current path of your input
# you may change p.path to operate a new path
> p.path
Output: ~/Documents/abc.def

# get the absolute full path of the path in p.path
> p.full()
Output: /Users/gangwang/Documents/abc.def

# get the base name of the file in p.path
> p.base()
Output: abc

# get the extension of the file in p.path
> p.extension()
Output: .def

# split the directory path
# The output is a list
> p.split_dir()
Output: ['', 'Users', 'gangwang', 'Documents']

# check if the path is a file and exists
# Output: Bool
> p.is_file()
Output: False

# check if the path is a directory and exists
# Output: Bool
> p.is_dir()
Output: False

# get the parent directory of the p.path
> p.pdir()
Output: /Users/gangwang/Documents

# list the paths matching the p.path
# equivalent to glob.glob(p.path)
> p.glob()
Output: [/Users/gangwang/Documents]

# list all the subfiles & subdirectories of p.path
# equivalent to os.walk(f.path)
> p.walk()

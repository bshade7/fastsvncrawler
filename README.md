# fast-svn-crawler / fastsvncrawler - A tool for listing SVN repository content

Import of [the "fast svn crawler" found on SourceForge
here](https://sourceforge.net/projects/fastsvncrawler/) created by Dmitry
Pavlenko.

From the SourceForge page;

> Unlike "svn ls --depth infinity" command it performs only 1 SVN request,
> hence saves time. As a bonus it obtains md5 checksums of the files.

[This blog post documents how much faster this code was originally
](http://vcs.atspace.co.uk/2013/03/16/fast-listing-of-svn-repository-with-svn-crawler/).

## Installation

To compile the program, you will need the libsvn-dev, make, and cmake packages
```
$ sudo apt-get install libsvn-dev make cmake
```

Next, perform the standard steps for CMake project compilation
```
$ mkdir build
$ cd build
$ cmake ..
$ make
```

## Usage

For basic usage of the utility, show all files for a URL by running
```
$ ./svn-crawler <URL>
```

A couple of options are available to provide additional listing options
```
-r <REV>             Will crawl a specific revision at the provided URL
--print-dirs         Will also show folders in the output as tree items and a blank MD5
--non-interactive    Enables non-interactive mode
```

## Changes

The following changes have been made;

 * The cmake config has been fixed to compile with the latest subversion
   library.

 * A .gitignore file has been added.

 * This README.md file has been added.
 
 * Basic installation and usage instructions included for those wanting to use it.

## License

It is unclear what license this code is available under. As it was originally
hosted on SourceForge.net and they only really hosted open source software, it
is likely you can use it. I've sent Dmitry Pavlenko an email - will update if
he responds.

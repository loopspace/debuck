NAME
    debuck - change `$` and `$$`s in a LaTeX document into `\(..\)` and
    `\[..\]`s.

SYNOPSIS
     debuck file
     debuck < file

    Modify *file* changing `$` and `$$`s in a LaTeX document into `\(..\)`
    and `\[..\]`s.

     Options:
        --man              print man page
        -h, -?, --help     print basic help
        -V, --version      print version information
        -gpl               print GPL

DESCRIPTION
    debuck steps through a LaTeX file changing TeX-style maths delimiters
    into LaTeX-style ones. Providing there are no sneaky macros and the file
    LaTeX's correctly it does a reasonable job.

    If given a filename it makes a backup and then puts the new version in
    place of the original. If the file is piped, it prints the new version
    on standard output.

BUGS
    The TeX-style maths delimiters are robust whereas pre-2015 the LaTeX
    ones were fragile. Therefore using maths in section heads or footnotes
    with a pre-2015 release of LaTeX might not work correctly.

    If using dollars for other reasons than to demark mathematics then those
    will get changed. For example, TikZ/PGF uses dollars to demark
    complicated calculations on coordinates. (This program was written
    before TikZ existed.)

AUTHOR
    Andrew Stacey

LICENSE
    Copyright (C) 2008--2016 Andrew Stacey

    This program is free software; you can redistribute it and/or mod ify it
    under the terms of the GNU General Public License as published by the
    Free Software Foundation; either version 2 of the License, or any later
    version.

    This program is distributed in the hope that it will be useful, but
    WITHOUT ANY WARRANTY; without even the implied warranty of
    MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU General
    Public License for more details.

    You should have received a copy of the GNU General Public License along
    with this program; if not, write to the Free Software Foundation, Inc.,
    59 Temple Place - Suite 330, Boston, MA 02111-1307, USA.


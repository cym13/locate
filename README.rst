Description
===========

This is an  implementation of locate in bash. I believe it is consequently
faster than locate in all circumstances. This is based on a previous
analysis_ by Julia Evans.

.. _analysis: http://jvns.ca/blog/2015/03/05/how-the-locate-command-works-and-lets-rewrite-it-in-one-minute/

Documentation
=============

::

    Usage: locate [OPTION]... PATTERN...

    Options:
        -b, --basename          Match only the base name, opposite of --wholename
        -c, --count             Writes only the number of matching entries
        -d, --database DBPATH   Replace the default database path with DBPATH
        -e, --existing          Print only entries that refer to existing files
        -L, --follow            When checking whether files exist, follow symlinks
        -h, --help              Print this help and exist
        -i, --ignore-case       Ignore case distinction when matching patterns
        -l, --limit, -n LIMIT   Exit successfully after finding LIMIT entries
        -m, --mmap              Ignored, for compatibility with BSD and GNU locate
        -P, --nofollow, -H      Opposite of --follow
        -0, -null               Separate the entries on output with \0
        -S, --statistics        Write statistics about each read database
        -q, --quiet             Write no messages about error encountered
        -r, --regexp REGEXP     Search for a basic regexp
        --regex                 Interpret all PATTERNs as extended regexps, default
        -s, --stdio             Ignored, for compatibility with BSD and GNU locate
        -u, --update            Updates the database
        -V, --version           Write information about the version and license
        -w, --wholename         Match only the whole path name.

Dependencies
============

This version depends mostly on grep and find, those should be already
available on any unix system.

Install
=======

Simply copy `locate' to a directory in your path. You can update the database
using `locate -u`, but if you prefer the traditional way you can make a
symbolic link to locate named "updatedb" and use that link instead.

License
=======

This program is under the GPLv3 License.

You should have received a copy of the GNU General Public License
along with this program. If not, see <http://www.gnu.org/licenses/>.

Contact
=======

Main developper: Cédric Picard
Email:           cedric.picard@efrei.net

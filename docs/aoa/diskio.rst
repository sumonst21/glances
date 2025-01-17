.. _disk:

Disk I/O
========

.. image:: ../_static/diskio.png

Glances displays the disk I/O throughput. The unit is adapted
dynamically.

You can display:

- bytes per second (default behavor / Bytes/s, KBytes/s, MBytes/s, etc)
- requests per second (using --diskio-iops option or *B* hotkey)

There is no alert on this information.

It's possible to define:

- a list of disk to show (white list)
- a list of disks to hide
- aliases for disk name

under the ``[diskio]`` section in the configuration file.

For example, if you want to hide the loopback disks (loop0, loop1, ...)
and the specific ``sda5`` partition:

.. code-block:: ini

    [diskio]
    hide=sda5,loop.*

or another example:

.. code-block:: ini

    [diskio]
    show=sda.*

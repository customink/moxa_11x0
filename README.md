# Synopsis

This is an updated Moxa USB-to-RS232 U1100 series driver that will run on the
Linux 2.6.32 kernel (x86 or x64).

[Moxa](http://www.moxa.com/)'s last driver update was for the Linux 2.6.27
kernel.

# License

The Moxa driver is licensed under the GNU GPL (see doc/readme.txt).

# Compile

  cd driver
  make clean ; make ; sudo make install

Sanity check that it's working

  modprobe mxu11x0
  lsmod mxu11x0

# Run the tests

The test suite is written in ruby 1.9.2/1.9.3, and relies on the serialport
and progress_bar gems.  The test suite takes a long time to run.  To test:

  gem install serialport progress_bar

  cd test
  ruby test.rb


# Testing and Support

My ability to test the changes are limited to heavy usage on Ubuntu 10.04 (the
2.6.32 kernel). The one quirk I've found is that rebooting the machine with
the UPort 1130 adapter (possibly others in the 11xx family) leaves it in
a dirty state. Unplug and plug it back in fixes it.

# Bug fixes, changes, etc.

Submit a pull request with updated tests.

# Contact

For questions, comments, etc.: feuerbach@gmail.com
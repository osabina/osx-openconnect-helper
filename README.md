osx-openconnect-helper
======================

  This is not the version registered with PyPI, so you'll have to install it yourself.  (Happy to submit PR to original author if it will be accepted)

  This is a slightly cleaned up branch with TOTP token support added.

  The rest of this readme is mostly unaltered from the original, so not entirely sure about these instructions...

  This program is a tiny helper application to connect to different
  Cisco VPNs through openconnect on OS X.  It just wraps openconnect
  to add some basic profile support.

  As a prerequsite, you'll need to install openconnect:

    $ brew install openconnect

  I can't recall if I had to pass args to this to have it compiled with token support enabled, but if you want to use TOTP or RSA with this, you'll need that support enabled (check `openconnect --version`) for what is enabled after install.

  If you do not have vpnc-script you can download it:

    http://www.infradead.org/openconnect/vpnc-script.html

  To install place it in /etc/vpnc/vpnc-script and make sure it
  is executable.

  From that point onwards you can add a vpn:

    $ openconnect-helper add myvpn https://myvpn.invalid/ --user me

  And connect:

    $ sudo openconnect-helper connect myvpn

  It uses the OS X keychain to manage passwords.

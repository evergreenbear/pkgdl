# pkgdl
#### this is a modular bash script to ease and semi-automate the process of installing & upgrading packages your linux distro might not provide in their repositories

## how it works
### installing/upgrading pkgs
the pkgdl script will parse the given package name and match it to a file in the pkgfiles directory ($HOME/bin/pkgdl.d/pkgs by default), and then source this file if matched  
`pkgdl get foo`

it can also check for updates and send a notification if one is available  
`pkgdl get foo latest`
### configuration options
with `pkgdl config`, certain options can be changed without needing to manually edit the script  
such as the main pkgdl.d location and (soon) other things
### pkg file template
with `pkgdl template bar`, a template is made for package `bar`, put into `pkgdl.d/pkgs/`  
this eases the process of adding new pkgs because general configuration is already done, as well as version checking (to some extent, you'll still need to change variables so the current and latest versions are properly gotten)
## todo
allow to check updates for all packages at once  
make `pkgdl config` work for more than just MainDir (woops..)  
other stuff i will inevitably run into  
  
#### it may not be the best script in the world, but i hope it can prove useful to you in some way!

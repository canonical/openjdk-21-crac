# CRaC JDK 21 - Security Updates

This repository contains OpenJDK 21 security updates published at https://github.com/openjdk/jdk21u.

## Build

CRaC JDK have extended build procedure.

1. Build JDK as usual
```
bash configure
make images
mv build/linux-x86_64-server-release/images/jdk/ .
```
2. Download a build of [modified CRIU](https://github.com/CRaC/criu/releases/tag/release-1.4)
3. Extract and copy `criu` binary over a same named file in the JDK
```
cp criu-dist/sbin/criu jdk/lib/criu
```
Grant permissions to allow regular user to run it
```
sudo chown root:root jdk/lib/criu
sudo chmod u+s jdk/lib/criu
```

# JDK
=======
# Welcome to OpenJDK 21 Updates!

The JDK 21 Updates project uses two GitHub repositories.
Updates are continuously developed in the repository [jdk21u-dev](https://github.com/openjdk/jdk21u-dev). This is the repository usually targeted by contributors.
The [jdk21u](https://github.com/openjdk/jdk21u) repository is used for rampdown of the update releases of jdk21u and only accepts critical changes that must make the next release during rampdown. (You probably do not want to target jdk21u).

For more OpenJDK 21 updates specific information such as timelines and contribution guidelines see the [project wiki page](https://wiki.openjdk.org/display/JDKUpdates/JDK+21u/).

>>>>>>> jdk-21.0.6+7

For build instructions please see the
[online documentation](https://openjdk.org/groups/build/doc/building.html),
or either of these files:
- [doc/building.html](doc/building.html) (html version)
- [doc/building.md](doc/building.md) (markdown version)
See <https://openjdk.org/> for more information about the OpenJDK
Community and the JDK and see <https://bugs.openjdk.org> for JDK issue
tracking.

# Installation instructions

## pip

**Note that using pip outside virtualenv is not recommended since it ignores
your systems package manager. If you aren't comfortable debugging package
installation issues, this is not the option for you.**

Create and activate a virtualenv:

```bash
virtualenv dfwinregenv
cd dfwinregenv
source ./bin/activate
```

Upgrade pip and install dfWinReg dependencies:

```bash
pip install --upgrade pip
pip install dfwinreg
```

To deactivate the virtualenv run:

```bash
deactivate
```

## Ubuntu 18.04 and 20.04 LTS

To install dfWinReg from the [GIFT Personal Package Archive (PPA)](https://launchpad.net/~gift):

```bash
sudo add-apt-repository ppa:gift/stable
```

Update and install dfWinReg:

```bash
sudo apt-get update
sudo apt-get install python3-dfwinreg
```

## Windows

The [l2tbinaries](https://github.com/log2timeline/l2tbinaries) contains the
necessary packages for running dfWinReg. l2tbinaries provides the following
branches:

* main; branch intended for the "packaged release" of dfWinReg and dependencies;
* dev; branch intended for the "development release" of dfWinReg;
* testing; branch intended for testing newly created packages.

The l2tdevtools project provides [an update script](https://github.com/log2timeline/l2tdevtools/wiki/Update-script)
to ease the process of keeping the dependencies up to date.

The script requires [pywin32](https://github.com/mhammond/pywin32/releases) and
[Python WMI](https://pypi.org/project/WMI).

To install the release versions of the dependencies run:

```
set PYTHONPATH=.

C:\Python38\python.exe tools\update.py --preset dfwinreg
```

# Package Build Scripts

This repository contains build scripts for creating binary packages from source code for various Linux distributions, including Alpine Linux (aports) and Void Linux (templates). The scripts are designed to automate the process of building packages, making it easier to create binaries/packages.

## Usage

Add files under <package-name> to distro-pkgbuilder and create new or make changes to Build files, patches and init files etc.

Example commands below to make necessary changes before commiting these files.

### Alpine Linux Checksum

Build image:  
`docker build -t alpine-abuild .`

Run:  
`docker run -v /path/to/alpine/<package-name>:/build alpine-abuild`

### Void Linux

Build image:  
`docker build -t voidlinux-xbps .`

Run:  
`docker run -v /path/to/voidlinux/<package-name>:/build voidlinux-xbps`

## License

This repository is licensed under the MIT License.
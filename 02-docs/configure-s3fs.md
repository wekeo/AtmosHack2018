# Contents
* [Object Store](#obs)
* [S3FS](#s3fs)
* [S3CMD](#s3cmd)

# Object Store <a name="obs"></a>
Datasets for the AtmosHack event are available in an Amazon S3 (Simple Storage Service) compatible Object Store. Tools like [s3fs](https://github.com/s3fs-fuse/s3fs-fuse) and [s3cmd](https://s3tools.org/s3cmd) can be configured and used to access the datasets. Access Key (AK) and Secret Key (SK) are needed to use these tools for data access and the following keys are used.

AK = IXUCNIYQK5IXQ80TGTSA

SK = SurkPQ2Z2xrBWxe9nye2Wfbyd3UVZ2ebVntT8ViN

# S3FS Configuration <a name="s3fs"></a>
**Steps:**
1. Install s3fs: `~$ sudo apt-get install s3fs`
2. Verify installation: `~$ s3fs --version`
3. Create a password file (replace AK, SK with above values): `~$ echo AK:SK >  ~/.passwd-s3fs`
4. Update permission of the password file: `~$ chmod 600  ~/.passwd-s3fs`
5. Create a directory (say data) for the mount point of the bucket: `~$ mkdir data`
6. Mount the bucket:
  * entire bucket: `s3fs atmoshack data -o passwd_file=~/.passwd-s3fs -o url=http://obs.eu-de.otc.t-systems.com/ -o umask=0022`
  * partial objects (sub-directory): `~$ s3fs atmoshack:/02-UV_Index-AC_SAF/2010 data -o passwd_file=~/.passwd-s3fs -o url=http://obs.eu-de.otc.t-systems.com/ -o umask=0022`
7. Test the data access: `ls data`


# S3CMD Configuration <a name="s3cmd"></a>
**Steps:**

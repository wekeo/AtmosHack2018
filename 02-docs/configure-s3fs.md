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

# S3CMD Configuration <a name="s3cmd"></a>
**Steps:**

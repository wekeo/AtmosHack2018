# Object Store
Datasets for the AtmosHack event are available in an Amazon S3 (Simple Storage Service) compatible Object Store. Tools like [s3fs](https://github.com/s3fs-fuse/s3fs-fuse) and [s3cmd](https://s3tools.org/s3cmd) can be configured and used to access the datasets. Access Key (AK) and Secret Key (SK) are needed to use these tools for data access. 

# S3FS Configuration 

Steps:

1. Install s3fs: `~$ sudo apt-get install s3fs`
2. Verify installation: `~$ s3fs --version`


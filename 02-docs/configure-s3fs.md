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
1. Install s3cmd 
```
sudo apt-get install python-setuptools
wget https://sourceforge.net/projects/s3tools/files/s3cmd/2.0.2/s3cmd-2.0.2.tar.gz
tar xvfz s3cmd-2.0.2.tar.gz
cd s3cmd-2.0.2
sudo python setup.py install
```
2. Configure s3cmd to access object store `s3cmd --configure`
Use the following values for the various options: <br/>
  AK : see above <br/>
  SK : see above <br/>
  Region : `eu-de` <br/>
  S3 endpoint : `obs.eu-de.otc.t-systems.com` <br/>
  DNS-Style bucket+hostname: `%(bucket)s.obs.eu-de.otc.t-systems.com` <br/>
  Enter `n` to quit verifying the access key <br/>

3. Save the configuration in the last step. After the current configuration is saved, S3cmd will automatically generate file .s3cfg under directory $HOME. The file includes all configuration information about S3cmd.
4. Open the s3cmd config file `vi ~/.s3cfg`
5. Locate parameter website_endpoint at the end of the .s3cfg configuration file, and change the value as follows
`website_endpoint = http://%(bucket)s.obs-website.%(location)s.otc.t-systems.com`
6. Save the config file
7. Test the configuration: `s3cmd ls`


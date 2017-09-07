# Collaborative-Topic-Regression
Step 1: Install and config gsl library. 

Download latest version of gsl at: ftp://ftp.gnu.org/gnu/gsl/

Place the file in your home directory and unpack the file with the following command:

tar -zxvf gsl-*.*.tar.gz
This will create a directory called gsl-*.* in your home directory. Change to this directory.

cd gsl-1.7
The next step is to configure the installation and tell the system where to install the files. Create a directory to install your gsl package, say “/home/yourname/gsl” with the following command

mkdir /home/yourname/gsl
Now configure the installation and tell it to use your new directory. This step may take a few minutes.

./configure --prefix=/home/yourname/gsl
If there are no errors, compile the library. This step will take several minutes.

make
Now it is necessary to check and test the library before actually installing it. This step will take some time.

make check
If there are no errors, go ahead and install the library with:

make install

Then add gsl/lib to the ~/.bashrc:
vi ~/.bashrc
Then add following command to this file
export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:/user/yourname/gsl/lib      
Then source it: source ~/.bashrc
Done the first step.

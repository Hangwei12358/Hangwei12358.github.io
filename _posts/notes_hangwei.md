
During the installation following the steps in github

luarocks make hdf5-0-0.rockspec LIBHDF5_LIBDIR="/usr/lib/x86_64-linux-gnu/"

was run with --local added to the end of the cmd -> not working
add sudo -> done
add sudo to the next few installations


pip3 install:
sudo apt-get install python3-pip



locale.Error: unsupported locale setting

solution: 
$ export LC_ALL=C

https://stackoverflow.com/questions/36394101/pip-install-locale-error-unsupported-locale-setting
 

sudo apt-get remove python3-pip; sudo apt-get install python3-pip

data_reader.py run on server with cmd:
python3 datareader.py opportunity /home/bingshui/hangwei/dl_har_existing_codes/deepHAR/data

RNN/main.lua: working
RNN/main_brnn.lua: error
/usr/local/share/lua/5.1/nn/JoinTable.lua:27: attempt to call method 'dim' (a nil value)
the possible reason: 
https://github.com/nhammerla/deepHAR/issues/1
potential solution:
https://stackoverflow.com/questions/29248639/torch7-neural-network-training-error

table to tensor, solved

solved: need to concatenate tensor of different sizes
https://torch7.readthedocs.io/en/rtd/maths/
https://pytorch.org/docs/stable/torch.html
the problem is the dim = 0 or 1 in the torch.cat() function. The dimension direction is different in pytorch and luatorch, which wastes a lot of time... 
Finally I followed the 1st website's instruction instead of 2nd link.


Also, the github-er provides a neater solution with very quick reply, thank him a lot!!!
https://github.com/nhammerla/deepHAR/issues/1


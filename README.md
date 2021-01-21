### Cassandra libraries (pre-built) 

#### To use the libraries

```aidl
rm -rf /tmp/cassandra-library
mkdir -p /tmp/cassandra-library
(git clone https://github.com/neon-vortex/cassandra-library.git /tmp/cassandra-library && cd /tmp/cassandra-library && git checkout 2.11)
sudo cp /tmp/cassandra-library/mac/libcassandra.dylib /usr/local/lib/
sudo cp /tmp/cassandra-library/mac/libcassandra.2.dylib /usr/local/lib/
rm -rf /tmp/cassandra-library
```

#### To Generate these libraries on mac/linux
- Clone https://github.com/datastax/cpp-driver  
```aidl
cd cpp-driver
mkdir -p build
cmake ..
make
```

##### To update this repository after generating the files 
###### Mac/linux
- Copy the generated files libcassandra.{major-version}.dylib , libcassandra.{major.minor.patch-version}.dylib and libcassandra.dylib to your /usr/local/lib folder and replace the previous libraries if any  

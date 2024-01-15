# Zenoh-Protobuf-Python
## Istalling Zenoh
The Eclipse Zenoh Python binding details are available on eclipse-zenoh website. please refere the link below to install the Eclipse zenoh-python library:
```
https://github.com/eclipse-zenoh/zenoh-python
```

## Installing protoc:
```
PROTOC_ZIP=protoc-3.14.0-linux-x86_64.zip
curl -OL https://github.com/protocolbuffers/protobuf/releases/download/v3.14.0/$PROTOC_ZIP
sudo unzip -o $PROTOC_ZIP -d /usr/local bin/protoc
sudo unzip -o $PROTOC_ZIP -d /usr/local 'include/*'
rm -f $PROTOC_ZIP

```

## Compiling Your Protocol Buffers
```
protoc -I=$SRC_DIR --python_out=$DST_DIR $SRC_DIR/fms.proto
For example
sudo protoc -I=. --python_out=. fms.proto --experimental_allow_proto3_optional
```

## Run the Subscriber Code
```
python3 fms_z_sub.py -m "peer" -k "fms/vehicleStatus"
```

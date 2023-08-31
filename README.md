# Proto files and `Android.bp` for the RemotiveBroker Android (AAOS) Client

This repository is designed to be declared as a dependency within the `manifest.xml` of your Android (AAOS) project.

### Example of `manifest.xml`

```xml
<?xml version="1.0" encoding="UTF-8"?>
<manifest>
  <remote name="remotivelabs" fetch="https://github.com/remotivelabs" />
  <project path="example/path/to/directory/in/your/project" 
           name="remotive-broker-android-client-protos"
           remote="remotivelabs"
           revision="main" />
</manifest>
```

### Directory Structure

- `/protos`: Contains a copy of the official Remotive Broker gRPC API proto files that are kept in sync with [Remotive Broker gRPC API repository](https://github.com/remotivelabs/remotivelabs-apis).
- `Android.bp`: References only those gRPC services defined in the proto files that are relevant for AAOS builds.

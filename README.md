# Pravega-Analysis

```
├── for FOLDERS
└── for FILES
│ 
```
```
├── .github
│    ├── ISSUE_TEMPLATE
│    ├── workflows
│    └── CONTRIBUTING.md
│    └── ISSUE_TEMPLATE.md
│    └── PULL_REQUEST_TEMPLATE.md
├── bindings
│    ├── src
│        ├── main
│            ├── java
│                ├── io
│                    ├── pravega
│                        ├── storage
│                            ├── azure
│                                └── AzureBlobClientImpl.java
│                                └── AzureChunkStrorage.java
│                                └── AzureClient.java
│                                └── AzureSimpleStorageFactory.java
│                                └── AzureStorageConfig.java
│                                └── AzureStorageFactoryCreator.java
│                            ├── extendeds3
│                                └── ExtendedS3ChunkStorage.java
│                                └── ExtendedS3SimpleStorageFactory.java
│                                └── ExtendedS3StorageConfig.java
│                                └── ExtendedS3StorageFactoryCreator.java
│                            ├── filesystem
│                                └── FileSystemChunkStorage.java
│                                └── FileSystemSimpleStorageFactory.java
│                                └── FileSystemStorageConfig.java
│                                └── FileSystemStorageFactoryCreator.java
│                                └── FileSystemWrapper.java
│                            ├── gcp
│                                └── GCPChunkStorage.java
│                                └── GCPSimpleStorageFactory.java
│                                └── GCPStorageConfig.java
│                                └── GCPStorageFactoryCreator.java
│                            ├── hdfs
│                                └── HDFSChunkStorage.java
│                                └── HDFSSimpleStorageFactory.java
│                                └── HDFSStorageConfig.java
│                                └── HDFSStorageFactoryCreator.java
│                            ├── s3
│                                └── S3ChunkStorage.java
│                                └── S3SimpleStorageFactory.java
│                                └── S3StorageConfig.java
│                                └── S3StorageFactoryCreator.java
│            ├── resources
│                ├── META-INF
│                    ├── services
│                        └── io.pravega.segmentstore.storage.StorageFactoryCreator
│
│
│
│
│ 
│        ├── test
├── checkstyle
├── cli
├── client
├── common
├── common_server
├── config
├── controller
├── deployment
├── dist
├── docker
├── documentation
├── gradle
├── segmentstore
├── shared
├── standalone
├── test
```

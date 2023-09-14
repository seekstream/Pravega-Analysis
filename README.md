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
│        ├── test
│            ├── java
│                ├── io
│                    ├── pravega
│                        ├── storage
│                            ├── azure
│                                └── AzureBlobClientImplTestsWithMock.java
│                                └── AzureFactoryTests.java
│                                └── AzureSimpleStorageTests.java
│                                └── AzureStorageConfigTest.java
│                                └── AzureTestContext.java
│                                └── MockAzureClient.java
│                            ├── extendeds3
│                                └── ExtendedS3SimpleStorageTests.java
│                                └── ExtendedS3StorageConfigTest.java
│                                └── ExtendedS3StorageFactoryTests.java
│                                └── ExtendedS3TestContext.java
│                                └── S3ClientMock.java
│                                └── S3Mock.java
│                            ├── filesystem
│                                └── FileSystemChunkStorageMockTest.java
│                                └── FileSystemSimpleStorageTest.java
│                                └── FileSystemStorageFactoryTests.java
│                            ├── gcp
│                                └── GCPSimpleStorageTests.java
│                                └── GCPStorageConfigTest.java
│                                └── GCPStorageFactoryTests.java
│                                └── GCPTestContext.java
│                            ├── hdfs
│                                └── HDFSChunkStorageMockTest.java
│                                └── HDFSClusterHelpers.java
│                                └── HDFSSimpleStorageTest.java
│                                └── HDFSStorageFactoryTests.java
│                            ├── s3
│                                └── S3ClientMock.java
│                                └── S3Mock.java
│                                └── S3SimpleStorageTests.java
│                                └── S3StorageConfigTests.java
│                                └── S3StorageFactoryTests.java
│                                └── S3TestContext.java
│            ├── resources
│                ├── mockito-extensions
│                    └── org.mockito.plugins.MockMaker
├── checkstyle
│   └── checkstyle.xml
│   └── eclipse.xml
│   └── example.importorder
│   └── import-control-core.xml
│   └── import-control.xml
│   └── intelij.xml
│   └── spotbugs-exclude.xml
│   └── spotbugs-include.xml
│   └── suppressions.xml
├── cli
│   ├── admin
│       ├── src
│           ├── main
│               ├── java
│                   ├── io
│                       ├── pravega
│                           ├── cli
│                               ├── admin
│                                   ├── bookkeeper
│                                       └── BookKeeperCleanupCommand.java
│                                       └── BookKeeperCommand.java
│                                       └── BookKeeperDetailsCommand.java
│                                       └── BookKeeperDisableCommand.java
│                                       └── BookKeeperEnableCommand.java
│                                       └── BookKeeperListAllLedgersCommand.java
│                                       └── BookKeeperListCommand.java
│                                       └── BookKeeperLogReconcileCommand.java
│                                       └── BookKeeperDeleteLedgersCommand.java
│                                       └── ContainerCommand.java
│                                       └── ContainerContinuousRecoveryCommand.java
│                                       └── ContainerRecoverCommand.java
│                                   ├── cluster
│                                       └── ClusterCommand.java
│                                       └── GetClusterNodesCommand.java
│                                       └── GetSegmentStoreByContainerCommand.java
│                                       └── ListContainersCommand.java
│                                   ├── config
│                                       └── ConfigCommand.java
│                                       └── ConfigListCommand.java
│                                       └── ConfigSetCommand.java
│                                   ├── controller
│                                       ├── metadata
│                                           └── ControllerMetadataCommand.java
│                                           └── ControllerMetadataGetEntryCommand.java 
│                                           └── ControllerMetadataListEntriesCommand.java 
│                                           └── ControllerMetadataListKeysCommand.java
│                                           └── ControllerMetadataTablesInfoCommand.java
│                                           └── ControllerMetadataUpdateEntryCommand.java
│                                           └── ControllerMetadataViewPendingEventsCommand.java
│                                           └── ControllerMetadataViewReaderInfoCommand.java
│                                       └── ControllerCommand.java
│                                       └── ControllerDeleteReaderGroupCommand.java
│                                       └── ControllerDescribeReaderGroupCommand.java
│                                       └── ControllerDescribeScopeCommand.java
│                                       └── ControllerDescribeStreamCommand.java
│                                       └── ControllerListReaderGroupsInScopeCommand.java
│                                       └── ControllerListScopesCommand.java
│                                       └── ControllerListStreamInScopeCommand.java
│                                   ├── dataRecovery
│                                       └── DataRecoveryCommand.java
│                                       └── DurableDataLogRepairCommand.java
│                                       └── DurableLogInspectCommand.java
│                                       └── DurableLogRecoveryCommand.java
│                                       └── RecoverFromStorageCommand.java
│                                       └── StorageListSegmentsCommand.java
│                                       └── TableSegmentRecoveryCommand.java
│                                   ├── json
│                                       └── ControllerMetadataJsonSerializer.java
│                                   ├── password
│                                       └── PasswordFileCreatorCommand.java
│                                       └── PasswordFileEntryParser.java
│                                   ├── readerGroup
│                                       └── ParseReaderGroupStreamCommand.java
│                                   ├── segmentstore
│                                       ├── storage
│                                           └── ListChunksCommand.java
│                                           └── StorageCommand.java
│                                           └── StorageUpdateSnapshotCommand.java
│                                       ├── tableSegment
│                                           └── GetTableSegmentEntryCommand.java
│                                           └── GetTableSegmentInfoCommand.java
│                                           └── ListTableSegmentKeysCommand.java
│                                           └── ModifyTableSegmentEntry.java
│                                           └── PutTableSegmentEntryCommand.java
│                                           └── RemoveTableSegmentKeyCommand.java
│                                           └── SetSerializerCommand.java
│                                           └── TableSegmentCommand.java
│                                       └── ContainerCommand.java
│                                       └── CreateSegmentCommand.java
│                                       └── DeleteSegmentCommand.java
│                                       └── FlushtoStorageCommand.java
│                                       └── GetContainerIdOfSegmentCommand.java
│                                       └── GetSegmentAttributeCommand.java
│                                       └── GetSegmentInfoCommand.java
│                                       └── ReadSegmentRangeCommand.java
│                                       └── SegmentStoreCommand.java
│                                       └── UpdateSegmentAttributeCommand.java
│                                   ├── serializers
│                                   ├── utils
│                                   └── AdminCLIRunner.java
│                                   └── AdminCommand.java
│                                   └── AdminCommandState.java
│                                   └── CommandArgs.java
│                                   └── Parser.java
│           ├── test
│       └── README.md
│   ├── user
│   └── .gitignore
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

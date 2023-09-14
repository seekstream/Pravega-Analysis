# Pravega-Analysis

## Generals

```
├── for FOLDERS
└── for FILES
│ 
```

## .github

```
├── .github
│    ├── ISSUE_TEMPLATE
│    ├── workflows
│    └── CONTRIBUTING.md
│    └── ISSUE_TEMPLATE.md
│    └── PULL_REQUEST_TEMPLATE.md
```

## bindings

```
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
```

## checkstyle

```
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
```

## cli

```
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
│                                       ├── controller
│                                           └── ControllerKeySerializer.java
│                                           └── ControllerMetadataSerializer.java
│                                       └── AbstractSerializer.java
│                                       └── ContainerKeySerializer.java
│                                       └── ContainerMetadataSerializer.java
│                                       └── SltsKeySerializer.java
│                                       └── SltsMetadataSerializer.java
│                                   ├── utils
│                                       └── AdminSegmentHelper.java
│                                       └── CLIConfig.java
│                                       └── ConfigUtils.java
│                                       └── FileHelper.java
│                                       └── TableSegmentUtils.java
│                                       └── ZKConnectionFailedException.java
│                                       └── ZKHelper.java
│                                   └── AdminCLIRunner.java
│                                   └── AdminCommand.java
│                                   └── AdminCommandState.java
│                                   └── CommandArgs.java
│                                   └── Parser.java
│           ├── test
│               ├── java
│                   ├── io
│                       ├── pravega
│                           ├── cli
│                               ├── admin
│                                   ├── bookkeeper
│                                       └── BookkeeperCommandsTest.java
│                                   ├── cluster
│                                       └── ClusterCommandNoZKTests.java
│                                       └── ClusterCommandsTest.java
│                                   ├── config
│                                       └── ConfigCommandsTest.java
│                                   ├── controller
│                                       └── AbstractControllerMetadataCommandsTest.java
│                                       └── ControllerCommandsTest.java
│                                       └── SecureControllerCommandsTest.java
│                                   ├── dataRecovery
│                                       └── DataRecoveryTest.java
│                                   ├── json
│                                       └── ControllerMetadataJsonSerializerTest.java
│                                   ├── password
│                                       └── PasswordFileCreatorCommandTest.java
│                                       └── PasswordFileEntryParserTest.java
│                                   ├── readerGroup
│                                       └── ParseReaderGroupStreamCommandTest.java
│                                   ├── segmentstore
│                                       ├── storage
│                                           └── AbstractSegmentStoreCommandsTest.java
│                                           └── StorageCommandsTest.java
│                                   ├── serializers
│                                       ├── controller
│                                           └── ControllerKeySerializerTest.java
│                                           └── ControllerMetadataSerializerTest.java
│                                       └── ContainerKeySerializerTest.java
│                                       └── ContainerMetadataSerializerTest.java
│                                       └── SerializerTest.java
│                                       └── SltsKeySerializerTest.java
│                                       └── SltsMetadataSerializerTest.java
│                                   ├── utils
│                                       └── ConfigUtilsTest.java
│                                       └── FileHelperTest.java
│                                       └── TestUtils.java
│                                       └── ZKHelperTest.java
│                                   └── AbstractAdminCommandTest.java
│                                   └── AdminCLIRunnerTests.java
│                                   └── AdminCommandStateTest.java
│               ├── resources
│                   └── admin-cli.properties
│       └── README.md
│   ├── user
│       ├── src
│           ├── main
│               ├── java
│                   ├── io
│                       ├── pravega
│                           ├── cli
│                               ├── user
│                                   ├── config
│                                       └── ConfigCommand.java
│                                       └── InteractiveConfig.java
│                                   ├── kvs
│                                       └── KeyValueTableCommand.java
│                                   ├── scope
│                                       └── ScopeCommand.java
│                                   ├── stream
│                                       └── StreamCommand.java
│                                   ├── utils
│                                       └── BackgroundConsoleListener.java
│                                       └── Formatter.java
│                                   └── Command.java
│                                   └── CommandArgs.java
│                                   └── Parser.java
│                                   └── UserCLIRunner.java
│           ├── test
│               ├── java
│                   ├── io
│                       ├── pravega
│                           ├── cli
│                               ├── user
│                                   ├── config
│                                       └── ConfigCommandTest.java
│                                       └── InteractiveConfigCommandTest.java
│                                   ├── kvs
│                                       └── KVTCommandsTest.java
│                                       └── SecureKVTCommandsTest.java
│                                   ├── scope
│                                       └── ScopeCommandsTest.java
│                                   ├── stream
│                                       └── StreamCommandTest.java
│                                   ├── utils
│                                       └── BackgroundConsoleListenerTest.java
│                                       └── FormatterTest.java
│                                   └── TestUtils.java
│                                   └── UserCLIRunnerTest.java
│       └── README.md
│   └── .gitignore
```

## client (Continued)

```
├── client
│   ├── src
│       ├── main
│           ├── java
│               ├── io
│                   ├── pravega
│                       ├── client
│                           ├── admin
│                               ├── impl
│                                   └── KeyValueTableManagerImpl.java
│                                   └── ReaderGroupManagerImpl.java
│                                   └── StreamCutHelper.java
│                                   └── StreamManagerImpl.java
│                               └── KeyValueTableInfo.java
│                               └── KeyValueTableManager.java
│                               └── ReaderGroupManager.java
│                               └── StreamInfo.java
│                               └── StreamManager.java
│                           ├── batch
│                               ├── impl
│                                   └── BatchClientFactoryImpl.java
│                                   └── SegmentIteratorImpl.java
│                                   └── SegmentRangeImpl.java
│                                   └── StreamSegmentInfoImpl.java
│                               └── SegmentIterator.java
│                               └── SegmentRange.java
│                               └── StreamSegmentsIterator.java
│                           ├── bytestream
│                               ├── impl
│                                   └── BufferedByStreamWriterImpl.java
│                                   └── ByteStreamClientImpl.java
│                                   └── ByteStreamReaderImpl.java
│                                   └── ByteStreamWriterImpl.java
│                               └── ByteStreamReader.java
│                               └── ByteStreamWriter.java
│                           ├── connection
│                               ├── impl
│                                   └── AppendBatchSizeTrackerImpl.java
│                                   └── ClientConnection.java
│                                   └── CommandEncoder.java
│                                   └── ConnectionFactory.java
│                                   └── ConnectionPool.java
│                                   └── Flow.java
│                                   └── FlowClientConnection.java
│                                   └── FlowHandler.java
│                                   └── FlowToBatchSizeTracker.java
│                                   └── IoBuffer.java
│                                   └── RawClient.java
│                                   └── SocketConnectionFactoryImpl.java
│                                   └── TcpClientConnection.java
│                           ├── control
│                               ├── impl
│                                   └── CachedPravegaNodeUri.java
│                                   └── CancellableRequest.java
│                                   └── Controller.java
│                                   └── ControllerFailureException.java
│                                   └── ControllerImpl.java
│                                   └── ControllerImplConfig.java
│                                   └── ControllerResolverFactory.java
│                                   └── ModelHelper.java
│                                   └── PravegaCredentialsWrapper.java
│                                   └── ReaderGroupConfigRejectedException.java
│                                   └── SegmentCollection.java
│                           ├── security
│                               ├── auth
│                                   └── DelegationToken.java
│                                   └── DelegationTokenProvider.java
│                                   └── DelegationTokenProviderFactory.java
│                                   └── EmptyTokenProviderImpl.java
│                                   └── JwtTokenProvideImpl.java
│                                   └── StringTokenProviderImpl.java
│                           ├── segment
│                               ├── impl
│                                   └── AsyncSegmentInputStream.java
│                                   └── AsyncSegmentInputStreamImpl.java
│                                   └── ConditionalOutputStream.java
│                                   └── ConditionalOutputStreamFactory.java
│                                   └── ConditionalOutputStreamFactoryImpl.java
│                                   └── ConditionalOutputStreamImpl.java
│                                   └── EndOfSegmentException.java
│                                   └── EventSegmentReader.java
│                                   └── EventSegmentReaderImpl.java
│                                   └── NoSuchEventException.java
│                                   └── NoSuchSegmentException.java
│                                   └── Segment.java
│                                   └── SegmentAttribute.java
│                                   └── SegmentInfo.java
│                                   └── SegmentInputStream.java
│                                   └── SegmentInputStreamFactory.java
│                                   └── SegmentInputStreamFactoryImpl.java
│                                   └── SegmentInputStreamImpl.java
│                                   └── SegmentMetadataClient.java
│                                   └── SegmentMetadataClientFactory.java
│                                   └── SegmentMetadataClientFactoryImpl.java
│                                   └── SegmentMetadataClientImpl.java
│                                   └── SegmentOutputStream.java
│                                   └── SegmentOutputStreamFactory.java
│                                   └── SegmentOutputStreamFactoryImpl.java
│                                   └── SegmentOutputStreamImpl.java
│                                   └── SegmentSealedException.java
│                                   └── SegmentTruncatedException.java
│                                   └── ServerTimeoutException.java
│                           ├── state
│                               ├── impl
│                                   └── CorruptedStateException.java
│                                   └── RevisionImpl.java
│                                   └── RevisionedStreamClientImpl.java
│                                   └── StateSynchronizerImpl.java
│                                   └── UpdateOrInit.java
│                                   └── UpdateOrInitSerializer.java
│                               └── InitialUpdate.java
│                               └── Revision.java
│                               └── Revisioned.java
│                               └── RevisionedStreamClient.java
│                               └── StateSynchronizer.java
│                               └── SynchronizerConfig.java
│                               └── Update.java
│                           ├── stream
│                               ├── impl
│                                   └── AbstractClientFactoryImpl.java
│                                   └── ByteArraySerializer.java
│                                   └── ByteBufferSerializer.java
│                                   └── CheckpointFailedException.java
│                                   └── CheckpointImpl.java
│                                   └── CheckpointState.java
│                                   └── ClientFactoryImpl.java
│                                   └── ConnectionClosedException.java
│                                   └── Credentials.java
│                                   └── DefaultCredentials.java
│                                   └── EventPointerImpl.java
│                                   └── EventPointerInternal.java
│                                   └── EventReadImpl.java
│                                   └── EventSegmentReaderUtility.java
│                                   └── EventStreamReaderImpl.java
│                                   └── EventStreamWriterImpl.java
│                                   └──
│                                   └── 
│                                   └──
│                                   └──
│                                   └──
│                                   └── 
│                               ├── notifications
│                                   ├── notifier
│                                       └── AbstractNotifier.java
│                                       └── AbstractPollingNotifier.java
│                                       └── EndOfDataNotifier.java
│                                       └── SegmentNotifier.java
│                                   └── EndOfDataNotification.java
│                                   └── Listener.java
│                                   └── Notification.java
│                                   └── NotificationSystem.java
│                                   └── NotifierFactory.java
│                                   └── Observable.java
│                                   └── ReaderGroupNotificationListener.java
│                                   └── SegmentNotification.java
│                               └── Checkpoint.java
│                               └── ConfigMismatchException.java
│                               └── DeleteScopeFailedException.java
│                               └── EventPointer.java
│                               └── EventRead.java
│                               └── EventStreamReader.java
│                               └── EventStreamWriter.java
│                               └── EventWriterConfig.java
│                               └── IdempotentEventStreamWriter.java
│                               └── InvalidStreamException.java
│                               └── NoSuchScopeException.java
│                               └── PingFailedException.java
│                               └── Position.java
│                               └── ReaderConfig.java
│                               └── ReaderGroup.java
│                               └── ReaderGroupConfig.java
│                               └── ReaderGroupMetrics.java
│                               └── ReaderGroupNotFoundException.java
│                               └── ReaderNotInReaderGroupException.java
│                               └── ReaderSegmentDistribution.java
│                               └── ReinitializationRequiredException.java
│                               └── RetentionPolicy.java
│                               └── ScalingPolicy.java
│                               └── Sequence.java
│                               └── Serializer.java
│                               └── Stream.java
│                               └── StreamConfiguration.java
│                               └── StreamCut.java
│                               └── TimeWindow.java
│                               └── Transaction.java
│                               └── TransactionInfo.java
│                               └── TransactionalEventStreamWriter.java
│                               └── TruncatedDataException.java
│                               └── TxnFailedException.java
│                           ├── tables
│                               ├── impl
│                           ├── watermark
│                               ├── impl
│                           └── BatchClientFactory.java
│                           └── ByteStreamClientFactory.java
│                           └── ClientConfig.java
│                           └── EventStreamClientFactory.java
│                           └── KeyValueTableFactory.java
│                           └── SynchronizerClientFactory.java
│       ├── test
```

## common 

```
├── common
```

## common_server

```
├── common_server
```

## config

```
├── config
```

## controller

```
├── controller
```

## deployment

```
├── deployment
```

## dist

```
├── dist
```

## docker

```
├── docker
```

## documentation

```
├── documentation
```

## gradle

```
├── gradle
```

## segmentstore

```
├── segmentstore
```

## shared

```
├── shared
```

## standalone 

```
├── standalone
```

## test

```
├── test
```

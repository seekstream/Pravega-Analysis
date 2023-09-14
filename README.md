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
│                                   └── JavaSerializer.java
│                                   └── LargeEventWriter.java
│                                   └── MaxNumberOfCheckpointsExceededException.java
│                                   └── Orderer.java
│                                   └── PendingEvent.java
│                                   └── Pinger.java
│                                   └── PositionImpl.java
│                                   └── PositionInternal.java
│                                   └── ReaderGroupImpl.java
│                                   └── ReaderGroupState.java
│                                   └── ReaderGroupStateManager.java
│                                   └── SegmentSelector.java
│                                   └── SegmentTransaction.java
│                                   └── SegmentTransactionImpl.java
│                                   └── SegmentWithRange.java
│                                   └── StreamCutImpl.java
│                                   └── StreamCutInternal.java
│                                   └── StreamImpl.java
│                                   └── StreamInternal.java
│                                   └── StreamSegmentSuccessors.java
│                                   └── StreamSegments.java
│                                   └── StreamSegmentsWithPredecessors.java
│                                   └── TransactionInfoImpl.java
│                                   └── TransactionalEventStreamWriterImpl.java
│                                   └── TxnSegments.java
│                                   └── UTF8StringSerializer.java
│                                   └── WatermarkReaderImpl.java
│                                   └── WriterPosition.java
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
│                                   └── HashTableIteratorItem.java
│                                   └── KeyValueTableFactoryImpl.java
│                                   └── KeyValueTableImpl.java
│                                   └── KeyValueTableIteratorImpl.java
│                                   └── KeyValueTableSegments.java
│                                   └── SegmentIteratorArgs.java
│                                   └── SegmentSelector.java
│                                   └── TableEntryHelper.java
│                                   └── TableSegment.java
│                                   └── TableSegmentEntry.java
│                                   └── TableSegmentFactory.java
│                                   └── TableSegmentFactoryImpl.java
│                                   └── TableSegmentImpl.java
│                                   └── TableSegmentIterator.java
│                                   └── TableSegmentKey.java
│                                   └── TableSegmentKeyVersion.java
│                                   └── VersionImpl.java
│                           ├── watermark
│                               └── WatermarkSerializer.java
│                           └── BatchClientFactory.java
│                           └── ByteStreamClientFactory.java
│                           └── ClientConfig.java
│                           └── EventStreamClientFactory.java
│                           └── KeyValueTableFactory.java
│                           └── SynchronizerClientFactory.java
│       ├── test
│           ├── java
│               ├── io
│                   ├── pravega
│                       ├── client
│                           ├── admin
│                               ├── impl
│                                   └── KeyValueTableManagerImplTest.java
│                                   └── ReaderGroupManagerImplTest.java
│                                   └── StreamManagerImplTest.java
│                           ├── batch
│                               ├── impl
│                                   └── BatchClientImplTest.java
│                                   └── SegmentIteratorTest.java
│                                   └── SegmentRangeImplTest.java
│                               └── StreamSegmentsInfoTest.java
│                           ├── bytestream
│                               ├── impl
│                                   └── ByteStreanWriterImplTest.java
│                               └── ByteStreamReaderTest.java
│                               └── ByteStreamWriterTest.java
│                           ├── connection
│                               ├── impl
│                                   └── AppendBatchSizeTrackerTest.java
│                                   └── ClientConnectionTest.java
│                                   └── CommandEncoderTest.java
│                                   └── ConnectionFactoryImplTest.java
│                                   └── ConnectionPoolingTest.java
│                                   └── FlowHandlerTest.java
│                                   └── FlowToBatchSizeTrackerTest.java
│                                   └── IoBufferTest.java
│                                   └── MockServer.java
│                                   └── RawClientTest.java
│                                   └── SecureConnectionFactoryImplTest.java
│                                   └── TcpClientConnectionTest.java
│                           ├── control
│                               ├── impl
│                                   └── CancellableRequestTest.java
│                                   └── ControllerImplLBTest.java
│                                   └── ControllerImplTest.java
│                                   └── ModelHelperTest.java
│                                   └── SecureControllerImplTest.java
│                           ├── security
│                               ├── auth
│                                   └── DelegationTokenProviderFactoryTest.java
│                                   └── DelegationTokenTest.java
│                                   └── JwtTokenProviderImplTest.java
│                           ├── segment
│                               ├── impl
│                                   └── AsyncSegmentInputStreamTest.java
│                                   └── ConditionalOutputStreamTest.java
│                                   └── EventSegmentReaderImplTest.java
│                                   └── SegmentAttributeTest.java
│                                   └── SegmentInputStreamFactoryImplTest.java
│                                   └── SegmentInputStreamTest.java
│                                   └── SegmentMetadataClientTest.java
│                                   └── SegmentOutputStreamFactoryTest.java
│                                   └── SegmentOutputStreamTest.java
│                           ├── state
│                               ├── examples
│                                   └── MembershipSynchronizer.java
│                                   └── SetSynchronizer.java
│                               ├── impl
│                                   └── RevisionedStreamClientTest.java
│                                   └── SerializationTest.java
│                                   └── SynchronizerTest.java
│                               └── SynchronizerConfigTest.java
│                           ├── stream
│                               ├── impl
│                                   └── ByteSerializerTest.java
│                                   └── CancellableRequestTest.java
│                                   └── CheckpointStateTest.java
│                                   └── ClientFactoryTest.java
│                                   └── DefaultCredentialsTest.java
│                                   └── EventPointerTest.java
│                                   └── EventStreamReaderTest.java
│                                   └── EventStreamWriterTest.java
│                                   └── JavaSerializerTest.java
│                                   └── LargeEventWriterTest.java
│                                   └── OrdererTest.java
│                                   └── PingerTest.java
│                                   └── PositionImplTest.java
│                                   └── ReaderGroupImplTest.java
│                                   └── ReaderGroupStateManagerTest.java
│                                   └── ReaderGroupStateTest.java
│                                   └── SegmentSelectorTest.java
│                                   └── SegmentTransactionTest.java
│                                   └── SerializationTest.java
│                                   └── StreamSegmentsTest.java
│                                   └── TransactionalEventStreamWriterTest.java
│                                   └── UTF8StringSerializerTest.java
│                                   └── WatermarkReaderImplTest.java
│                               ├── mock
│                                   └── MockClientFactory.java
│                                   └── MockConnectionFactoryImpl.java
│                                   └── MockController.java
│                                   └── MockSegmentIoStreams.java
│                                   └── MockSegmentStreamFactory.java
│                                   └── MockStreamManager.java
│                               ├── notifications
│                                   └── CustomNotification.java
│                                   └── CustomNotifier.java
│                                   └── EndOfDataNotifierTest.java
│                                   └── NotificationFrameworkTest.java
│                                   └── SegmentNotifierTest.java
│                               └── EventWriterConfigTest.java
│                               └── ReaderGroupConfigTest.java
│                               └── ScalingPolicyTest.java
│                               └── StreamConfigurationTest.java
│                               └── StreamCutTest.java
│                           ├── tables
│                           ├──watermark
│                           └── ClientConfigTest.java
│                           └── CredentialsExtractorTest.java
│                           └── FlowTest.java
│           ├── resources
│               ├── META-INF
│                   ├── services
│                       └── io.pravega.client.stream.impl.Credentials
│                       └── io.pravega.shared.security.auth.Credentials
│               ├── mockito-extensions
│                   └── org.mockito.plugins.MockMaker
│               └── logback-test.xml
│               └── logback.xml
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

---
description: Hyper-v WMI 提供者的第2版是 Windows 8 和 Windows Server 2012 的新功能。
ms.assetid: A91ACF7A-AFE6-45B6-960C-C4AAA0083735
title: Hyper-v WMI 提供者有哪些新功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce222fd18955e88b9e33e1b706cf81ef5a806917
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850264"
---
# <a name="whats-new-in-hyper-v-wmi-provider"></a>Hyper-v WMI 提供者的新功能

Hyper-v WMI 提供者的第2版是 Windows 8 和 Windows Server 2012 的新功能。

## <a name="windows-10-version-1709"></a>Windows 10 (版本 1709)

新類別：

-   [**Msvm \_ 電池**](msvm-battery.md)
-   [**Msvm \_ BatterySettingData**](msvm-batterysettingdata.md)
-   [**Msvm \_ PersistentMemoryController**](msvm-persistentmemorycontroller.md)

新屬性：

-   [**Msvm \_CollectionReferencePointExportJob**](msvm-collectionreferencepointexportjob.md)： **ExportedGuestStateFilePaths**
-   [**Msvm \_EthernetSwitchHardwareOffloadData**](msvm-ethernetswitchhardwareoffloaddata.md)： **DefaultQueueVrssIndependentHostSpreading**、 **DefaultQueueVrssExcludePrimaryProcessor**、 **DefaultQueueVrssQueueSchedulingMode** 和 **DefaultQueueVrssMinQueuePairs**
-   [**Msvm \_EthernetSwitchHardwareOffloadSettingData**](msvm-ethernetswitchhardwareoffloadsettingdata.md)： **DefaultQueueVrssIndependentHostSpreading**、 **DefaultQueueVrssExcludePrimaryProcessor**、 **DefaultQueueVrssQueueSchedulingMode**、 **DefaultQueueVrssMinQueuePairs**、
-   [**Msvm \_EthernetSwitchPortOffloadData**](msvm-ethernetswitchportoffloaddata.md)： **VrssVmbusChannelAffinityPolicy**、 **VrssIndependentHostSpreading**、 **VrssExcludePrimaryProcessor**、 **VrssQueueSchedulingModes** 和 **VrssMinQueuePairs**
-   [**Msvm \_VirtualHardDiskSettingData**](msvm-virtualharddisksettingdata.md)： **DataAlignment**、 **PmemAddressAbstractionType** 和 **IsPmemCompatible**
-   [**Msvm \_VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md)： **DisableDifferentialOfIgnoredStorage** 和 **ExcludedVirtualHardDisks**
-   [**Msvm \_VirtualSystemManagementServiceSettingData**](msvm-virtualsystemmanagementservicesettingdata.md)： **HypervisorRootSchedulerEnabled**
-   [**Msvm \_VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md)： **CPUCappingMagnitude** 和 **CancelIfBlackoutThresholdExceeded**
-   [**Msvm \_VirtualSystemReferencePointExportJob**](msvm-virtualsystemreferencepointexportjob.md)： **ExportedGuestStateFilePath**
-   [**Msvm \_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)： **架構**、 **AutomaticSnapshotsEnabled**、 **IsAutomaticSnapshot**、 **GuestStateFile** 和 **GuestStateDataRoot**

## <a name="windows-10-version-1703"></a>Windows 10 (版本 1703)

新類別：

-   [**Msvm \_ AssignableDeviceDismountSettingData**](msvm-assignabledevicedismountsettingdata.md)
-   [**Msvm \_ AssignableDeviceService**](msvm-assignabledeviceservice.md)
-   [**Msvm \_ CollectionReferencePointExportJob**](msvm-collectionreferencepointexportjob.md)
-   [**Msvm \_ EthernetSwitchHardwareOffloadSettingData**](msvm-ethernetswitchhardwareoffloadsettingdata.md)
-   [**Msvm \_ EthernetSwitchPortMigrationQosSettingData**](msvm-ethernetswitchportmigrationqossettingdata.md)
-   [**Msvm \_ EthernetSwitchPortRdmaSettingData**](msvm-ethernetswitchportrdmasettingdata.md)
-   [**Msvm \_ EthernetSwitchPortTeamMappingSettingData**](msvm-ethernetswitchportteammappingsettingdata.md)
-   [**Msvm \_ GpuPartition**](msvm-gpupartition.md)
-   [**Msvm \_ GpuPartitionSettingData**](msvm-gpupartitionsettingdata.md)
-   [**Msvm \_ NetworkConnectionDiagnosticInformation**](msvm-networkconnectiondiagnosticinformation.md)
-   [**Msvm \_ NetworkConnectionDiagnosticSettingData**](msvm-networkconnectiondiagnosticsettingdata.md)
-   [**Msvm \_ PartitionableGpu**](msvm-partitionablegpu.md)
-   [**Msvm \_ PciExpress**](msvm-pciexpress.md)
-   [**Msvm \_ PciExpressSettingData**](msvm-pciexpresssettingdata.md)
-   [**Msvm \_ SecurityElement**](msvm-securityelement.md)
-   [**Msvm \_ SecurityService**](msvm-securityservice.md)
-   [**Msvm \_ SecuritySettingData**](msvm-securitysettingdata.md)
-   [**Msvm \_ StorageSettingData**](msvm-storagesettingdata.md)
-   [**Msvm \_ SummaryInformationBase**](msvm-summaryinformationbase.md)
-   [**Msvm \_ SystemComponentSettingData**](msvm-systemcomponentsettingdata.md)
-   [**Msvm \_ VirtualSystemReferencePointExportJob**](msvm-virtualsystemreferencepointexportjob.md)
-   [**Msvm \_ VirtualSystemReferencePointSettingData**](msvm-virtualsystemreferencepointsettingdata.md)

已移除的類別：

-   [**Msvm \_ TPMSettingData**](msvm-tpmsettingdata.md)

新方法：

-   [**Msvm \_CollectionSnapshotService**](msvm-collectionsnapshotservice.md)類別： [ **ApplySnapshot**](msvm-collectionsnapshotservice-applysnapshot.md)
-   [**Msvm \_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) 類別： [**AddSystemComponentSetting**](msvm-virtualsystemmanagementservice-addsystemcomponentsettings.md)、 [**DiagnoseNetworkConnection**](msvm-virtualsystemmanagementservice-diagnosenetworkconnection.md)、 [**ModifySystemComponentSettings**](msvm-virtualsystemmanagementservice-modifysystemcomponentsettings.md)和 [**RemoveSystemComponentSettings**](msvm-virtualsystemmanagementservice-removesystemcomponentsettings.md)
-   [**Msvm \_VirtualSystemReferencePointService**](msvm-virtualsystemreferencepointservice.md)類別： [ **ImportReferencePointMetadata**](msvm-virtualsystemreferencepointservice-importreferencepointmetadata.md)

新屬性：

-   [**Msvm \_EthernetSwitchHardwareOffloadData**](msvm-ethernetswitchhardwareoffloaddata.md)： **DefaultQueueVmmqQueuePairs**、 **DefaultQueueVmmqEnabled** 和 **DefaultQueueVrssEnabled**
-   [**Msvm \_EthernetSwitchPortOffloadData**](msvm-ethernetswitchportoffloaddata.md)： **VmmqQueuePairs**、 **VmmqEnabled** 和 **VrssEnabled**
-   [**Msvm \_EthernetSwitchPortOffloadSettingData**](msvm-ethernetswitchportoffloadsettingdata.md)： **VmmqQueuePairs**、 **VmmqEnabled** 和 **VrssEnabled**
-   [**Msvm \_GuestClusterInformation**](msvm-guestclusterinformation.md)： **LastResourceMoveTime**
-   [**Msvm \_KvpExchangeComponentSettingData**](msvm-kvpexchangecomponentsettingdata.md)： **DisableHostKVPItems**
-   [**Msvm \_MemorySettingData**](msvm-memorysettingdata.md)： **SgxSize** 和 **SgxEnabled**
-   [**Msvm \_Physical3dGraphicsProcessor**](msvm-physical3dgraphicsprocessor.md)： **CompatibleForVirtualization** 和 **DriverModelVersion**
-   [**Msvm \_ProcessorSettingData**](msvm-processorsettingdata.md)： **HwThreadsPerCoreCpuGroupId**、 **HideHypervisorPresent** 和 **ExposeVirtualizationExtensions**
-   [**Msvm \_SettingsDefineCapabilities**](msvm-settingsdefinecapabilities.md)： **SupportStatement**
-   [**Msvm \_StorageAllocationSettingData**](msvm-storageallocationsettingdata.md)： **WriteHardeningMethod**
-   [**Msvm \_SummaryInformation**](msvm-summaryinformation.md)： **受防護**
-   [**Msvm \_SyntheticEthernetPortSettingData**](msvm-syntheticethernetportsettingdata.md)： **AllowPacketDirect**
-   [**Msvm \_VirtualSystemCollection**](msvm-virtualsystemcollection.md)： **LastApplyConsistencyLevel**、 **LastApplyVirtualMachineIds**、 **LastApplyTime**、 **FailedOverReplicationType**、 **ReplicationMode** 和 **ReplicationState**
-   [**Msvm \_VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md)： **ExportForLiveMigration**
-   [**Msvm \_VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md)： **AvoidRemovingVHDs** 和 **AllowOverwriteExistingFile**
-   [**Msvm \_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)： **HighMmioGapSize**
-   [**Msvm \_VirtualSystemSnapshotSettingData**](msvm-virtualsystemsnapshotsettingdata.md)： **GuestBackupType**

移除的屬性：

-   [**Msvm \_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)： **ParentPackage**

## <a name="windows-10"></a>Windows 10

新類別：

-   [**CIM \_ CollectedMSEs**](cim-collectedmses.md)
-   [**CIM \_ 集合**](cim-collection.md)
-   [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md)
-   [**CIM \_ ElementView**](cim-elementview.md)
-   [**CIM \_ MemberOfCollection**](cim-memberofcollection.md)
-   [**CIM \_ TPM**](cim-tpm.md)
-   [**CIM \_ 視圖**](cim-view.md)
-   [**Msvm \_ CollectedCollections**](msvm-collectedcollections.md)
-   [**Msvm \_ CollectedReferencePoints**](msvm-collectedreferencepoints.md)
-   [**Msvm \_ CollectedSnapshots**](msvm-collectedsnapshots.md)
-   [**Msvm \_ CollectedVirtualSystems**](msvm-collectedvirtualsystems.md)
-   [**Msvm \_ CollectionManagementService**](msvm-collectionmanagementservice.md)
-   [**Msvm \_ CollectionReferencePointExportSettingData**](msvm-collectionreferencepointexportsettingdata.md)
-   [**Msvm \_ CollectionReferencePointService**](msvm-collectionreferencepointservice.md)
-   [**Msvm \_ CollectionReferencePointSettingData**](msvm-collectionreferencepointsettingdata.md)
-   [**Msvm \_ CollectionSettingData**](msvm-collectionsettingdata.md)
-   [**Msvm \_ CollectionSnapshotExportSettingData**](msvm-collectionsnapshotexportsettingdata.md)
-   [**Msvm \_ CollectionSnapshotService**](msvm-collectionsnapshotservice.md)
-   [**Msvm \_ ComputerSystemSummaryInformation**](msvm-computersystemsummaryinformation.md)
-   [**Msvm \_ EthernetSwitchPortVfpSettingData**](msvm-ethernetswitchportvfpsettingdata.md)
-   [**Msvm \_ GuestClusterInformation**](msvm-guestclusterinformation.md)
-   [**Msvm \_ GuestCommunicationService**](msvm-guestcommunicationservice.md)
-   [**Msvm \_ GuestCommunicationServiceSettingData**](msvm-guestcommunicationservicesettingdata.md)
-   [**Msvm \_ GuestServiceInterfaceSettingDataComponent**](msvm-guestserviceinterfacesettingdatacomponent.md)
-   [**Msvm \_ ManagementCollection**](msvm-managementcollection.md)
-   [**Msvm \_ MoveUnmanagedVhd**](msvm-moveunmanagedvhd.md)
-   [**Msvm \_ ReferencePointCollection**](msvm-referencepointcollection.md)
-   [**Msvm \_ ReferencePointOfVirtualSystem**](msvm-referencepointofvirtualsystem.md)
-   [**Msvm \_ ReferencePointOfVirtualSystemCollection**](msvm-referencepointofvirtualsystemcollection.md)
-   [**Msvm \_ ResourceDependentOnResource**](msvm-resourcedependentonresource.md)
-   [**Msvm \_ SerialPortSettingData**](msvm-serialportsettingdata.md)
-   [**Msvm \_ ServiceOfVssComponent**](msvm-serviceofvsscomponent.md)
-   [**Msvm \_ SnapshotCollection**](msvm-snapshotcollection.md)
-   [**Msvm \_ SnapshotOfVirtualSystemCollection**](msvm-snapshotofvirtualsystemcollection.md)
-   [**Msvm \_ StandaloneV2ElementConformsToProfile**](msvm-standalonev2elementconformstoprofile.md)
-   [**Msvm \_ SyntheticDisplayControllerSettingData**](msvm-syntheticdisplaycontrollersettingdata.md)
-   [**Msvm \_ SyntheticKeyboard**](msvm-synthetickeyboard.md)
-   [**Msvm \_ TPM**](msvm-tpm.md)
-   [**Msvm \_ TPMSettingData**](msvm-tpmsettingdata.md)
-   [**Msvm \_ VHDSetInformation**](msvm-vhdsetinformation.md)
-   [**Msvm \_ VHDSnapshotInformation**](msvm-vhdsnapshotinformation.md)
-   [**Msvm \_ VirtualEthernetSwitchNicTeamingMember**](msvm-virtualethernetswitchnicteamingmember.md)
-   [**Msvm \_ VirtualEthernetSwitchNicTeamingSettingData**](msvm-virtualethernetswitchnicteamingsettingdata.md)
-   [**Msvm \_ VirtualMachineToDisks**](msvm-virtualmachinetodisks.md)
-   [**Msvm \_ VirtualSystemCollection**](msvm-virtualsystemcollection.md)
-   [**Msvm \_ VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md)
-   [**Msvm \_ VirtualSystemReferencePointExportSettingData**](msvm-virtualsystemreferencepointexportsettingdata.md)
-   [**Msvm \_ VirtualSystemReferencePointService**](msvm-virtualsystemreferencepointservice.md)
-   [**Msvm \_ VirtualSystemReferencePointSettingData**](msvm-virtualsystemreferencepointsettingdata.md)
-   [**Msvm \_ VirtualSystemSnapshotSettingData**](msvm-virtualsystemsnapshotsettingdata.md)
-   [**Msvm \_ VssService**](msvm-vssservice.md)

已移除類別：

-   [**Msvm \_ ResourcePoolComponent**](msvm-resourcepoolcomponent.md)
-   [**Msvm \_ ResourcePoolRegistration**](msvm-resourcepoolregistration.md)
-   [**Msvm \_ ResourcePoolSettingData**](msvm-resourcepoolsettingdata.md)
-   [**Msvm \_ VirtualizationComponent**](msvm-virtualizationcomponent.md)
-   [**Msvm \_ VirtualizationComponentRegistration**](msvm-virtualizationcomponentregistration.md)

新屬性：

-   [**Msvm \_BootSourceSettingData**](msvm-bootsourcesettingdata.md)： **OptionalData**
-   [**Msvm \_EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md)： **LastKnownSwitchName** 和 **CompartmentGuid**
-   [**Msvm \_EthernetSwitchHardwareOffloadData**](msvm-ethernetswitchhardwareoffloaddata.md)： **PacketDirectInUse**
-   [**Msvm \_EthernetSwitchPortOffloadSettingData**](msvm-ethernetswitchportoffloadsettingdata.md)： **PacketDirectModerationInterval**、 **PacketDirectModerationCount**、 **PacketDirectNumProcs**、
-   [**Msvm \_EthernetSwitchPortSecuritySettingData**](msvm-ethernetswitchportsecuritysettingdata.md)： **EnableFixSpeed10G** 和 **Reserved**
-   [**Msvm \_GuestServiceInterfaceComponentSettingData**](msvm-guestserviceinterfacecomponentsettingdata.md)： **DefaultEnabledStatePolicy**
-   [**Msvm \_ProcessorSettingData**](msvm-processorsettingdata.md)： **EnableHostResourceProtection**
-   [**Msvm \_StorageAllocationSettingData**](msvm-storageallocationsettingdata.md)： **StorageQoSPolicyID**、 **CachingMode** 和 **SnapshotId**
-   [**Msvm \_SummaryInformation**](msvm-summaryinformation.md)： **InstanceID**、 **Version**、 **ThumbnailImageHeight**、 **ThumbnailImageWidth** 和 **HostComputerSystemName**
-   [**Msvm \_Synthetic3DDisplayControllerSettingData**](msvm-synthetic3ddisplaycontrollersettingdata.md)： **VRAMSizeBytes**
-   [**Msvm \_VirtualEthernetSwitchSettingData**](msvm-virtualethernetswitchsettingdata.md)： **TeamingEnabled** 和 **PacketDirectEnabled**
-   [**Msvm \_VirtualHardDiskSettingData**](msvm-virtualharddisksettingdata.md)： **ParentTimestamp** 和 **ParentIdentifier**
-   [**Msvm \_VirtualHardDiskState**](msvm-virtualharddiskstate.md)： **Timestamp**
-   [**Msvm \_VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md)： **BackupIntent** 和 **DifferentialBackupBase**
-   [**Msvm \_VirtualSystemManagementServiceSettingData**](msvm-virtualsystemmanagementservicesettingdata.md)： **DefaultVirtualHardDiskCachingMode**
-   [**Msvm \_VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md)： **RemoveSourceUnmanagedVhds** 和 **UnmanagedVhds**
-   [**Msvm \_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)： **UserSnapshotType**、 **GuestControlledCacheTypes**、 **LockOnDisconnect**、 **ParentPackage**、 **AutomaticCriticalErrorActionTimeout**、 **AutomaticCriticalErrorAction**、 **ConsoleMode** 和 **SecureBootTemplateId**

新方法：

-   [**Msvm \_ImageManagementService**](msvm-imagemanagementservice.md) 類別： [**ConvertVirtualHardDiskToVHDSet**](msvm-imagemanagementservice-convertvirtualharddisktovhdset.md)、 [**DeleteVHDSnapshot**](msvm-imagemanagementservice-deletevhdsnapshot.md)、 [**FindMountedStorageImageInstance**](msvm-imagemanagementservice-findmountedstorageimageinstance.md)、 [**GetVHDSetInformation**](msvm-imagemanagementservice-getvhdsetinformation.md)、 [**GetVHDSnapshotInformation**](msvm-imagemanagementservice-getvhdsnapshotinformation.md)、 [**GetVirtualDiskChanges**](msvm-imagemanagementservice-getvirtualdiskchanges.md)、 [**OptimizeVHDSet**](msvm-imagemanagementservice-optimizevhdset.md)和 [**SetVHDSnapshotInformation**](msvm-imagemanagementservice-setvhdsnapshotinformation.md)
-   [**Msvm \_ShutdownComponent**](msvm-shutdowncomponent.md)類別： [ **InitiateReboot**](msvm-shutdowncomponent-initiatereboot.md)
-   [**Msvm \_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)： [**AddBootSourceSettings**](msvm-virtualsystemmanagementservice-addbootsourcesettings.md)、 [**AddGuestServiceSettings**](msvm-virtualsystemmanagementservice-addguestservicesettings.md)、 [**DefinePlannedSystem**](msvm-virtualsystemmanagementservice-defineplannedsystem.md)、 [**ModifyGuestServiceSettings**](msvm-virtualsystemmanagementservice-modifyguestservicesettings.md)、 [**RemoveBootSourceSettings**](msvm-virtualsystemmanagementservice-removebootsourcesettings.md)、 [**RemoveGuesServiceSettings**](msvm-virtualsystemmanagementservice-removeguestservicesettings.md)、 [**SetInitialMachineConfigurationData**](msvm-virtualsystemmanagementservice-setinitialmachineconfigurationdata.md)和 [**UpgradeSystemVersion**](msvm-virtualsystemmanagementservice-upgradesystemversion.md)
-   [**Msvm \_VirtualSystemSnapshotService**](msvm-virtualsystemsnapshotservice.md)類別： [ **ConvertToReferencePoint**](msvm-virtualsystemsnapshotservice-converttoreferencepoint.md)

## <a name="windows-81-and-windows-server-2012-r2"></a>Windows 8.1 與 Windows Server 2012 R2

Windows 8.1 和 Windows Server 2012 R2 包含 Hyper-v WMI 提供者第2版的新功能。

-   **IOPSAllocationUnits**、 **IOPSLimit**、 **IOPSReservation** 和 **PersistentReservationsSupported** 屬性已新增至 [**Msvm \_ StorageAllocationSettingData**](msvm-storageallocationsettingdata.md)類別。
-   **VirtualDiskId** 屬性已新增至 [**Msvm \_ VirtualHardDiskSettingData**](msvm-virtualharddisksettingdata.md)類別。
-   存放裝置 QoS 的相關資訊已新增至 [**Msvm \_ LogicalDisk**](msvm-logicaldisk.md)和 [**Msvm \_ ResourcePool**](msvm-resourcepool.md)類別的 **OperationalStatus** 屬性。
-   [**Msvm \_StorageAlert**](msvm-storagealert.md) 類別
-   **ClusterMonitored** 屬性已新增至 [**Msvm \_ EmulatedEthernetPortSettingData**](msvm-emulatedethernetportsettingdata.md)和 [**Msvm \_ SyntheticEthernetPortSettingData**](msvm-syntheticethernetportsettingdata.md)類別。
-   **EnableCompression** 和 **EnableSmbTransport** 屬性已新增至 [**Msvm \_ VirtualSystemMigrationServiceSettingData**](msvm-virtualsystemmigrationservicesettingdata.md)類別。
-   **EnableCompression** 屬性已新增至 [**Msvm \_ VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md)類別。 **TransportType** 屬性包含有關即時移轉的資訊。
-   [**Msvm \_CopyFileToGuestJob**](msvm-copyfiletoguestjob.md) 類別
-   [**Msvm \_CopyFileToGuestSettingData**](msvm-copyfiletoguestsettingdata.md) 類別
-   [**Msvm \_GuestFileService**](msvm-guestfileservice.md) 類別
-   [**Msvm \_GuestService**](msvm-guestservice.md) 類別
-   [**Msvm \_GuestServiceInterfaceComponent**](msvm-guestserviceinterfacecomponent.md) 類別
-   [**Msvm \_GuestServiceInterfaceComponentSettingData**](msvm-guestserviceinterfacecomponentsettingdata.md) 類別
-   [**Msvm \_RegisteredGuestService**](msvm-registeredguestservice.md) 類別
-   **EnhancedSessionModeEnabled** 屬性已新增至 [**Msvm \_ VirtualSystemManagementServiceSettingData**](msvm-virtualsystemmanagementservicesettingdata.md)類別。
-   **EnhancedModeState** 屬性和 [**InjectNonMaskableInterrupt**](injectnonmaskableinterrupt-msvm-computersystem.md)方法已新增至 Msvm 的「工作 [**人員 \_ 」**](msvm-computersystem.md)類別。
-   **BootSourceOrder**、 **LowMmioGapSize**、 **NetworkBootPreferredProtocol**、 **PauseAfterBootFailure** 、 **SecureBootEnabled** 和 **VirtualSystemSubType** 屬性已新增至 [**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)類別。
-   [**Msvm \_BootSourceSettingData**](msvm-bootsourcesettingdata.md) 類別
-   [**Msvm \_BootSourceComponent**](msvm-bootsourcecomponent.md) 類別
-   [**Msvm \_LogicalIdentity**](msvm-logicalidentity.md) 類別
-   [**Msvm \_CompatibilityVector**](msvm-compatibilityvector.md) 類別
-   [**GetSystemCompatibilityVectors**](getsystemcompatibilityvectors-msvm-virtualsystemmigrationservice.md)方法已新增至 [**Msvm \_ VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md)類別。
-   **ReplicationStateEx**、 **ReplicationHealthEx**、 **EnhancedSessionModeState**、 **VirtualSwitchNames** 和 **VirtualSystemSubType** 屬性已新增至 [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md)類別。 **ReplicationState** 和 **ReplicationHealth** 屬性已被取代，並由 **ReplicationStateEx** 和 **ReplicationHealthEx** 屬性取代。
-   **PnpDevicePath** 屬性已新增至 [**Msvm \_ MountedStorageImage**](msvm-mountedstorageimage.md)類別。
-   **AllowedHashAlgorithms** 和 **TrustedIssuerCertificateHashes** 屬性已新增至 [**Msvm \_ TerminalServiceSettingData**](msvm-terminalservicesettingdata.md)類別。

Windows 8.1 和 Windows Server 2012 R2 包含虛擬機器複寫和容錯移轉復原的新功能。

-   [**Msvm \_ReplicationProvider**](msvm-replicationprovider.md) 類別
-   [**Msvm \_ReplicationRelationship**](msvm-replicationrelationship.md) 類別
-   [**ChangeReplicationModeToPrimary**](changereplicationmodetoprimary-msvm-replicationservice.md)、 [**GetReplicationStatisticsEx**](getreplicationstatisticsex-msvm-replicationservice.md)、 [**InitiateFailback**](initiatefailback-msvm-replicationservice.md)、 [**RemoveReplicationRelationshipEx**](removereplicationrelationshipex-msvm-replicationservice.md)和 [**ResetReplicationStatisticsEx**](resetreplicationstatisticsex-msvm-replicationservice.md)方法已加入至 [**Msvm \_ ReplicationService**](msvm-replicationservice.md)類別。 **GetReplicationStatisticsEx**、 **RemoveReplicationRelationshipEx** 和 **ResetReplicationStatisticsEx** 方法會取代 [**GetReplicationStatistics**](getreplicationstatistics-msvm-replicationservice.md)、 [**RemoveReplicationRelationship**](removereplicationrelationship-msvm-replicationservice.md)和 [**ResetReplicationStatistics**](resetreplicationstatistics-msvm-replicationservice.md)方法。
-   [**Msvm \_ SystemReplicationRelationship**](msvm-systemreplicationrelationship.md)類別會顯示虛擬機器和許多複寫關聯性之間的關聯。
-   **AdditionalSettings** 和 **ReplicationProvider** 屬性已新增至 [**Msvm \_ ReplicationSettingData**](msvm-replicationsettingdata.md)類別。
-   主機對主機提供者的相關資訊已新增至 [**Msvm \_ ReplicationService**](msvm-replicationservice.md)類別的 [**>createreplicationrelationship**](createreplicationrelationship-msvm-replicationservice.md)和 [**ModifyReplicationSettings**](modifyreplicationsettings-msvm-replicationservice.md)方法。
-   RequestReplicationStateChangeEx 方法已新增至 Msvm 的 [ [](msvm-requestreplicationstatechangeex-computersystem.md) ] 類別，並取代 [**RequestReplicationStateChange**](msvm-computersystem-requestreplicationstatechange.md)方法。 [**\_**](msvm-computersystem.md) **InstanceID** 屬性現在可以表示擴充複寫。 如需擴充複寫的詳細資訊，請參閱 [**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md)。
-   [**Msvm \_ReplicationSettingData**](msvm-replicationsettingdata.md) 和 [**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md) 實例具有1:1 的關聯性，您可以使用 [**Msvm \_ SettingsDefineState**](msvm-settingsdefinestate.md) 關聯來表示。

    | [**Msvm \_SettingsDefineState**](msvm-settingsdefinestate.md) 屬性名稱 | 值                                                                                                |
    |-----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
    | **ManagedElement**                                                          | 代表 [**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md) 物件          |
    | **SettingData**                                                             | 表示相關聯的 [**Msvm \_ ReplicationSettingData**](msvm-replicationsettingdata.md) 物件 |

    

     

-   [**Msvm \_ReplicationSettingData**](msvm-replicationsettingdata.md) 可以根據 **InstanceId** 或 **ReplicationRelationship** 屬性，區分複寫關聯性的設定實例。 因此，這些處理單一關聯性的方法不會變更其簽章：

    -   [**Msvm \_ ReplicationService：： >createreplicationrelationship**](createreplicationrelationship-msvm-replicationservice.md)
    -   [**Msvm \_ ReplicationService：： ModifyReplicationSettings**](modifyreplicationsettings-msvm-replicationservice.md)
    -   [**Msvm \_ ReplicationService：： Resync**](resynchronize-msvm-replicationservice.md)
    -   [**Msvm \_ ReplicationService：： >startreplication**](startreplication-msvm-replicationservice.md)

-   雖然您可以對主要關聯性使用 [**GetReplicationStatistics**](getreplicationstatistics-msvm-replicationservice.md)、 [**RemoveReplicationRelationship**](removereplicationrelationship-msvm-replicationservice.md)和 [**RequestReplicationStateChange**](msvm-computersystem-requestreplicationstatechange.md) ，但是建議您使用 [**GetReplicationStatisticsEx**](getreplicationstatisticsex-msvm-replicationservice.md)、 [**RemoveReplicationRelationshipEx**](removereplicationrelationshipex-msvm-replicationservice.md)和 [**RequestReplicationStateChangeEx**](msvm-requestreplicationstatechangeex-computersystem.md) ，因為它們可以處理主要和延伸複寫關聯性。 如需擴充複寫的詳細資訊，請參閱 [**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md)。
-   雖然 Msvm 的 [ [**] \_**](msvm-computersystem.md) 類別的這些屬性會繼續指出主要複寫關聯性的狀態，但請改用 [**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md) 物件的這些屬性來判斷主要和延伸複寫關聯性的目前狀態。

    | 屬性名稱                                | 類型        |
    |----------------------------------------------|-------------|
    | **ReplicationState**                         | Uint16 (RO)  |
    | **ReplicationHealth**                        | Uint16 (RO)  |
    | **LastReplicationTime**                      | Datetime    |
    | **FailedOverReplicationType**                | Uint16      |
    | **LastApplicationConsistentReplicationTime** | Datetime    |
    | **LastReplicationType**                      | Uint16      |

    

     

 

 




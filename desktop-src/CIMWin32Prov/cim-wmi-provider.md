---
description: 這些 WMI 類別是在 CimWin32 中宣告。
ms.assetid: 53122499-1CC0-4B48-AEA1-B70B7BBC3A99
ms.tgt_platform: multiple
title: CIM WMI 提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acb9a01e0771645cf6101171ce870be593181cb61d6118e627b9bf96b61994be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118420330"
---
# <a name="cim-wmi-provider"></a>CIM WMI 提供者

這些 WMI 類別是在 CimWin32 中宣告。

## <a name="in-this-section"></a>本節內容

<dl> <dt>

[**CIM \_ 動作**](cim-action.md)
</dt> <dd>

[**CIM \_ 動作**](cim-action.md)類別是一項作業，屬於進程的一部分，可在其下一個狀態下建立軟體專案，或刪除目前狀態中的 software 元素。

</dd> <dt>

[**CIM \_ ActionSequence**](cim-actionsequence.md)
</dt> <dd>

[**Cim \_ ActionSequence**](cim-actionsequence.md)關聯會定義一系列的作業，這些作業會將 [**CIM \_ SoftwareElementActions**](cim-softwareelementactions.md)) 關聯 (所參考的軟體專案轉換為下一個狀態，或從其目前的狀態中移除軟體元素。

</dd> <dt>

[**CIM \_ ActsAsSpare**](cim-actsasspare.md)
</dt> <dd>

[**CIM \_ ActsAsSpare**](cim-actsasspare.md)關聯會指出哪些專案可以是可替換的元素，或是取代其他匯總的元素。 備用可以依元素個別的指定，以「熱待命」模式運作。

</dd> <dt>

[**CIM \_ AdjacentSlots**](cim-adjacentslots.md)
</dt> <dd>

[**CIM \_ AdjacentSlots**](cim-adjacentslots.md)關聯描述主控電路板或介面卡卡上的位置版面配置。 資訊，例如位置之間的距離，以及它們是否為「共用」 (如果已填入，則無法使用另一個位置，) 會將它傳達為關聯屬性。

</dd> <dt>

[**CIM \_ AggregatePExtent**](cim-aggregatepextent.md)
</dt> <dd>

[**CIM \_ AggregatePExtent**](cim-aggregatepextent.md)類別提供有關可定址邏輯區塊的摘要資訊，這些區塊位於相同的儲存體冗余群組，且位於相同的實體媒體上。

</dd> <dt>

[**CIM \_ AggregatePSExtent**](cim-aggregatepsextent.md)
</dt> <dd>

[**CIM \_ AggregatePSExtent**](cim-aggregatepsextent.md)類別會定義單一儲存裝置上可定址的邏輯區塊數目，但不包括對應為檢查資料的邏輯區塊。 如果已定義磁片區集，則邏輯區塊會包含在單一磁片區集合中。 當只需要摘要資訊或使用自動設定時，這是 [**CIM \_ ProtectedSpaceExtent**](cim-protectedspaceextent.md)的替代群組。

</dd> <dt>

[**CIM \_ AggregateRedundancyComponent**](cim-aggregateredundancycomponent.md)
</dt> <dd>

[**CIM \_ AggregateRedundancyComponent**](cim-aggregateredundancycomponent.md)類別描述儲存體冗余群組中的匯總實體範圍。

</dd> <dt>

[**CIM \_ AlarmDevice**](cim-alarmdevice.md)
</dt> <dd>

[**CIM \_ AlarmDevice**](cim-alarmdevice.md)類別是一種警示裝置，可發出與問題狀況相關的聲音或可見指示。

</dd> <dt>

[**CIM \_ AllocatedResource**](cim-allocatedresource.md)
</dt> <dd>

[**CIM \_ AllocatedResource**](cim-allocatedresource.md)類別代表邏輯裝置與系統資源之間的關聯，並指出資源已指派給裝置。

</dd> <dt>

[**CIM \_ ApplicationSystem**](cim-applicationsystem.md)
</dt> <dd>

[**CIM \_ ApplicationSystem**](cim-applicationsystem.md)類別代表支援特定商務功能的應用程式或軟體系統，可作為獨立的單位來管理。 這類系統可使用 [**CIM \_ SoftwareFeature**](cim-softwarefeature.md) 類別分解為其功能性元件。 特定應用程式或軟體系統的軟體功能位於使用 [**CIM \_ ApplicationSystemSoftwareFeature**](cim-applicationsystemsoftwarefeature.md) 關聯。

</dd> <dt>

[**CIM \_ ApplicationSystemSoftwareFeature**](cim-applicationsystemsoftwarefeature.md)
</dt> <dd>

[**CIM \_ ApplicationSystemSoftwareFeature**](cim-applicationsystemsoftwarefeature.md)類別代表的關聯會識別組成特定應用程式系統的軟體功能。 軟體功能可以包含在不同的產品中。

</dd> <dt>

[**CIM \_ AssociatedAlarm**](cim-associatedalarm.md)
</dt> <dd>

[**CIM \_ AssociatedAlarm**](cim-associatedalarm.md)相依性會將警示與邏輯裝置產生關聯。

</dd> <dt>

[**CIM \_ AssociatedBattery**](cim-associatedbattery.md)
</dt> <dd>

[**CIM \_ AssociatedBattery**](cim-associatedbattery.md)相依性會將電池與邏輯裝置產生關聯。 您可以使用此關聯來建立個別電池的模型，使其成為 (UPS) 的不斷電供應系統供應。

</dd> <dt>

[**CIM \_ AssociatedCooling**](cim-associatedcooling.md)
</dt> <dd>

[**CIM \_ AssociatedCooling**](cim-associatedcooling.md)關聯會指出風扇或其他冷卻裝置特定于裝置 (與提供主機殼或封包冷卻) 。

</dd> <dt>

[**CIM \_ AssociatedMemory**](cim-associatedmemory.md)
</dt> <dd>

[**CIM \_ AssociateMemory**](cim-associatedmemory.md)類別會將已安裝或相關聯的記憶體（例如快取記憶體）與邏輯裝置產生關聯。

</dd> <dt>

[**CIM \_ AssociatedProcessorMemory**](cim-associatedprocessormemory.md)
</dt> <dd>

[**CIM \_ AssociatedProcessorMemory**](cim-associatedprocessormemory.md)類別會將處理器和系統記憶體或處理器的快取產生關聯。

</dd> <dt>

[**CIM \_ AssociatedSensor**](cim-associatedsensor.md)
</dt> <dd>

[**CIM \_ AssociatedSensor**](cim-associatedsensor.md)類別會將已安裝的感應器與邏輯裝置產生關聯。 感應器會測量重要的輸入和輸出屬性，並可包含在裝置內或安裝在附近。

</dd> <dt>

[**CIM \_ AssociatedSupplyCurrentSensor**](cim-associatedsupplycurrentsensor.md)
</dt> <dd>

[**CIM \_ AssociatedSupplyCurrentSensor**](cim-associatedsupplycurrentsensor.md)類別會將電源供應器與目前的 (amperage) 感應器建立關聯，以監視其輸入頻率。

</dd> <dt>

[**CIM \_ AssociatedSupplyVoltageSensor**](cim-associatedsupplyvoltagesensor.md)
</dt> <dd>

將電源供應器與監視其輸入電壓的電壓感應器產生關聯。

</dd> <dt>

[**CIM \_ BasedOn**](cim-basedon.md)
</dt> <dd>

[**CIM \_ BasedOn**](cim-basedon.md)類別代表一種關聯，描述如何從較低層級的範圍組合儲存區。 例如，實體範圍包含受保護的空間範圍。 因此，系統會從一或多個實體或受保護的空間範圍組合磁片區集合。 快取記憶體可以獨立定義並在實體元素中實現，也可以根據暫時性或非暫時性的儲存區。

</dd> <dt>

[**CIM \_ 電池**](cim-battery.md)
</dt> <dd>

「 [**CIM \_ 電池**](cim-battery.md) 」類別代表電池邏輯裝置的功能和管理。 此類別適用于膝上型電腦系統中的電池，以及其他內部和外部電池。

</dd> <dt>

[**CIM \_ BinarySensor**](cim-binarysensor.md)
</dt> <dd>

[**CIM \_ BinarySensor**](cim-binarysensor.md)類別提供布林輸出。 **CurrentState** 和 **PossibleStates** 屬性已新增至 sensoring，因此不再需要 **CIM \_ BinarySensor** 子類別，不過，它是為了回溯相容性而保留。 您可以具現化具有兩種可能狀態的感應器，以建立二進位感應器。

</dd> <dt>

[**CIM \_ BIOSElement**](cim-bioselement.md)
</dt> <dd>

[**CIM \_ BIOSElement**](cim-bioselement.md)類別代表載入至非暫時性儲存區中，用來啟動和設定電腦系統的低層級軟體。

</dd> <dt>

[**CIM \_ BIOSFeature**](cim-biosfeature.md)
</dt> <dd>

代表用來啟動及設定電腦系統的低層級軟體的功能。

</dd> <dt>

[**CIM \_ BIOSFeatureBIOSElements**](cim-biosfeaturebioselements.md)
</dt> <dd>

[**CIM \_ BIOSFeatureBIOSElements**](cim-biosfeaturebioselements.md)類別會將 BIOS 功能和其匯總的 bios 專案產生關聯。

</dd> <dt>

[**CIM \_ BIOSLoadedInNV**](cim-biosloadedinnv.md)
</dt> <dd>

[**CIM \_ BIOSLoadedInNV**](cim-biosloadedinnv.md)類別會將 BIOS 元素和載入它的非暫時性儲存區產生關聯。

</dd> <dt>

[**CIM \_ BootOSFromFS**](cim-bootosfromfs.md)
</dt> <dd>

[**CIM \_ BootOSFromFS**](cim-bootosfromfs.md)類別會將作業系統和載入作業系統的檔案系統產生關聯。 關聯是多對多;分散式作業系統可相依于數個檔案系統，以正確且完整的載入。

</dd> <dt>

[**CIM \_ BootSAP**](cim-bootsap.md)
</dt> <dd>

[**CIM \_ BootSAP**](cim-bootsap.md)類別代表開機服務的存取點。

</dd> <dt>

[**CIM \_ BootService**](cim-bootservice.md)
</dt> <dd>

[**CIM \_ BootService**](cim-bootservice.md)類別代表裝置或軟體所提供的功能，或由網路所提供的功能，可將作業系統載入到單一電腦系統上。

</dd> <dt>

[**CIM \_ BootServiceAccessBySAP**](cim-bootserviceaccessbysap.md)
</dt> <dd>

[**CIM \_ BootServiceAccessBySAP**](cim-bootserviceaccessbysap.md)類別會將開機服務及其存取點產生關聯。

</dd> <dt>

[**CIM \_ CacheMemory**](cim-cachememory.md)
</dt> <dd>

[**CIM \_ CacheMemory**](cim-cachememory.md)類別會定義快取記憶體的功能和管理。

</dd> <dt>

[**CIM \_ 卡片**](cim-card.md)
</dt> <dd>

「 [**CIM 記憶 \_ 卡**](cim-card.md) 」類別代表一種實體容器類型，可插入另一張卡片或主控電路板，或本身是底座中的主控電路板/主機板。 此類別包含任何能夠攜帶信號的封裝，並提供實體元件的掛接點，例如晶片或其他實體套件（例如其他卡片）。

</dd> <dt>

[**CIM \_ CardInSlot**](cim-cardinslot.md)
</dt> <dd>

[**CIM \_ CardInSlot**](cim-cardinslot.md)類別會將介面卡卡片與插入它的容器產生關聯。

</dd> <dt>

[**CIM \_ CardOnCard**](cim-cardoncard.md)
</dt> <dd>

[**CIM \_ CardOnCard**](cim-cardoncard.md)關聯描述的是可插入主機板/主機板、介面卡 daughtercards 或卡片的關聯性，以支援特殊的卡片型模組。

</dd> <dt>

[**CIM \_ CDROMDrive**](cim-cdromdrive.md)
</dt> <dd>

[**CIM \_ CDROMDrive**](cim-cdromdrive.md)類別代表電腦上的 cd-rom 光碟機。

</dd> <dt>

[**CIM \_ 底座**](cim-chassis.md)
</dt> <dd>

[**CIM \_ 底座**](cim-chassis.md)類別代表包含其他元素的實體元素，並提供可定義的功能，例如桌面、處理節點、UPS、磁片或磁帶存放裝置，或這些專案的組合。

</dd> <dt>

[**CIM \_ ChassisInRack**](cim-chassisinrack.md)
</dt> <dd>

[**CIM \_ ChassisInRack**](cim-chassisinrack.md)關聯代表機架與其包含的底座之間的「包含」關聯性。

</dd> <dt>

[**CIM \_ 檢查**](cim-check.md)
</dt> <dd>

[**Cim \_ 檢查**](cim-check.md)類別代表一種條件或特性，此條件或特性在定義的環境中應該是 true，或是由 [**cim 系統 \_ 環境**](cim-computersystem.md)類別的實例所設定的範圍。 與特定軟體專案相關聯的檢查會使用 [**CIM \_ SoftwareElementChecks**](cim-softwareelementchecks.md)關聯的 [**階段**] 屬性組織成兩個群組的其中一個。

</dd> <dt>

[**CIM \_ 晶片**](cim-chip.md)
</dt> <dd>

[**CIM \_ 晶片**](cim-chip.md)類別代表整合電路硬體的類型，包括 ASICs、處理器、記憶體晶片等等。

</dd> <dt>

[**CIM \_ ClusteringSAP**](cim-clusteringsap.md)
</dt> <dd>

[**CIM \_ ClusteringSAP**](cim-clusteringsap.md)類別代表叢集服務的存取點。

</dd> <dt>

[**CIM \_ ClusteringService**](cim-clusteringservice.md)
</dt> <dd>

[**CIM \_ ClusteringService**](cim-clusteringservice.md)類別代表叢集所提供的功能。 例如，容錯移轉功能可以模型化為容錯移轉叢集的服務。

</dd> <dt>

[**CIM \_ ClusterServiceAccessBySAP**](cim-clusterserviceaccessbysap.md)
</dt> <dd>

[**CIM \_ ClusterServiceAccessBySAP**](cim-clusterserviceaccessbysap.md)類別代表叢集服務與其存取點之間的關聯性。

</dd> <dt>

[**CIM \_ CollectedCollections**](cim-collectedcollections.md)
</dt> <dd>

[**CIM \_ CollectedCollections**](cim-collectedcollections.md)類別是一種匯總關聯，代表 mse 集合中所包含之受管理系統元素 (MSE) 。

</dd> <dt>

[**CIM \_ CollectedMSEs**](cim-collectedmses.md)
</dt> <dd>

[**CIM \_ CollectedMSEs**](cim-collectedmses.md)關聯類別代表群組物件的成員（ [**CollectionOfMSEs**](cim-collectionofmses.md)類別）。

</dd> <dt>

[**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md)
</dt> <dd>

[**Cim \_ CollectionOfMSEs**](cim-collectionofmses.md)物件允許將 [**cim \_ ManagedSystemElement**](cim-managedsystemelement.md)物件分組，以建立設定和設定的關聯性。 它是抽象的，需要在子類別中進行進一步的定義和語義改進。

</dd> <dt>

[**CIM \_ CollectionOfSensors**](cim-collectionofsensors.md)
</dt> <dd>

[**CIM \_ CollectionOfSensors**](cim-collectionofsensors.md)關聯代表組成 multistate 感應器的二元感應器。

</dd> <dt>

[**CIM \_ CollectionSetting**](cim-collectionsetting.md)
</dt> <dd>

[**Cim \_ CollectionSetting**](cim-collectionsetting.md)類別代表 [**cim \_ CollectionOfMSEs**](cim-collectionofmses.md)和為其定義的設定類別之間的關聯。

</dd> <dt>

[**CIM \_ CompatibleProduct**](cim-compatibleproduct.md)
</dt> <dd>

[**CIM \_ CompatibleProduct**](cim-compatibleproduct.md)類別代表產品之間的關聯，表示兩個參考的產品是否可互通，例如是否可以一起安裝，或是可以是另一個實體容器，依此類推。

</dd> <dt>

[**CIM \_ 元件**](cim-component.md)
</dt> <dd>

[**CIM \_ 元件**](cim-component.md)關聯表示 mse 之間關聯性的元件。

</dd> <dt>

[**CIM \_ 未進行**](cim-computersystem.md)
</dt> <dd>

[**Cim 非 \_**](cim-computersystem.md)實例類別代表 [**cim \_ ManagedSystemElement**](cim-managedsystemelement.md)實例的特殊集合。 此集合提供電腦功能，並可做為匯總點，以建立下列一或多個專案的關聯：檔案系統、作業系統、處理器和記憶體 (volatile 和非暫時性儲存) 。 此類別衍生自 [**CIM \_ 系統**](cim-system.md)。

</dd> <dt>

[**CIM \_ ComputerSystemDMA**](cim-computersystemdma.md)
</dt> <dd>

[**CIM \_ ComputerSystemDMA**](cim-computersystemdma.md)類別代表電腦系統與其可用的直接記憶體存取 (DMA) 通道之間的關聯。

</dd> <dt>

[**CIM \_ ComputerSystemIRQ**](cim-computersystemirq.md)
</dt> <dd>

[**CIM \_ ComputerSystemIRQ**](cim-computersystemirq.md)類別代表電腦系統與其可用的插斷要求 () 的 irq 之間的關聯。

</dd> <dt>

[**CIM \_ ComputerSystemMappedIO**](cim-computersystemmappedio.md)
</dt> <dd>

[**CIM \_ ComputerSystemMappedIO**](cim-computersystemmappedio.md)類別代表電腦系統與其可用記憶體對應 i/o 埠之間的關聯。

</dd> <dt>

[**CIM \_ ComputerSystemPackage**](cim-computersystempackage.md)
</dt> <dd>

[**CIM \_ ComputerSystemPackage**](cim-computersystempackage.md)類別代表一種關聯，可明確定義單一電腦系統與一或多個實體套件之間的關聯性。 關聯類似于實體元素實現邏輯裝置的方式。

</dd> <dt>

[**CIM \_ ComputerSystemResource**](cim-computersystemresource.md)
</dt> <dd>

[**CIM \_ ComputerSystemResource**](cim-computersystemresource.md)類別代表電腦系統與其可用系統資源之間的關聯。

</dd> <dt>

[**CIM \_ 設定**](cim-configuration.md)
</dt> <dd>

Cim 設定物件允許將 [**cim \_ 設定**](cim-setting.md)物件中 (定義的參數集群組) 和一個或多個 managed 系統專案的相依性。 [**\_**](cim-configuration.md)

</dd> <dt>

[**CIM \_ ConnectedTo**](cim-connectedto.md)
</dt> <dd>

[**CIM \_ ConnectedTo**](cim-connectedto.md)類別代表一種關聯，表示兩個或多個實體連接器已連線。

</dd> <dt>

[**CIM \_ ConnectorOnPackage**](cim-connectoronpackage.md)
</dt> <dd>

[**CIM \_ ConnectorOnPackage**](cim-connectoronpackage.md)類別代表的關聯，會明確指出連接器與封裝之間的內含專案關聯性。 實體套件包含連接器和其他實體元素。

</dd> <dt>

[**CIM \_ 容器**](cim-container.md)
</dt> <dd>

[**CIM \_ 容器**](cim-container.md)類別表示包含的實體元素與包含的實體專案之間的關聯。 包含的物件必須是實體封裝。

</dd> <dt>

[**CIM \_ ControlledBy**](cim-controlledby.md)
</dt> <dd>

[**CIM \_ ControlledBy**](cim-controlledby.md)關聯性會指出哪些裝置是由控制器邏輯裝置所發出或存取。

</dd> <dt>

[**CIM \_ 控制器**](cim-controller.md)
</dt> <dd>

[**CIM \_ 控制器**](cim-controller.md)類別是用來分組其他控制項相關裝置的父類別。 控制器的範例包括 SCSI 控制器、USB 控制器和串列控制器。

</dd> <dt>

[**CIM \_ CoolingDevice**](cim-coolingdevice.md)
</dt> <dd>

[**CIM \_ CoolingDevice**](cim-coolingdevice.md)類別代表冷卻裝置的功能和管理。

</dd> <dt>

[**CIM \_ CopyFileAction**](cim-copyfileaction.md)
</dt> <dd>

[**CIM \_ CopyFileAction**](cim-copyfileaction.md)類別代表將檔案從電腦系統移動或複製到新位置。

</dd> <dt>

[**CIM \_ CreateDirectoryAction**](cim-createdirectoryaction.md)
</dt> <dd>

[**CIM \_ CreateDirectoryAction**](cim-createdirectoryaction.md)類別會為要安裝在本機的軟體元素建立空的目錄。

</dd> <dt>

[**CIM \_ CurrentSensor**](cim-currentsensor.md)
</dt> <dd>

[**Cim \_ CurrentSensor**](cim-currentsensor.md)類別存在，可回溯相容于舊版 cim 架構定義。

</dd> <dt>

[**CIM \_ 資料檔案**](cim-datafile.md)
</dt> <dd>

[**CIM 資料 \_ 檔**](cim-datafile.md)類別代表資料的命名集合或可執行檔程式碼。 只會傳回本機固定磁片上的檔案實例

</dd> <dt>

[**CIM \_ 相依性**](cim-dependency.md)
</dt> <dd>

[**CIM 相依 \_**](cim-dependency.md)性類別代表在物件之間建立相依性關聯性的關聯。

</dd> <dt>

[**CIM \_ DependencyCoNtext**](cim-dependencycontext.md)
</dt> <dd>

[**Cim \_ DependencyCoNtext**](cim-dependencycontext.md)關聯性會將 [**cim \_**](cim-dependency.md)相依性類別與一個或多個 [**cim \_ 設定物件**](cim-configuration.md)產生關聯。 例如，電腦系統的相依性可能會根據系統所連接的網路而變更。

</dd> <dt>

[**CIM \_ DesktopMonitor**](cim-desktopmonitor.md)
</dt> <dd>

[**CIM \_ DesktopMonitor**](cim-desktopmonitor.md)類別代表桌面監視器 (CRT) 邏輯裝置的功能和管理。

</dd> <dt>

[**CIM \_ DeviceAccessedByFile**](cim-deviceaccessedbyfile.md)
</dt> <dd>

[**CIM \_ DeviceAccessedByFile**](cim-deviceaccessedbyfile.md)關聯類別會使用參考的 [**CIM \_ DeviceFile**](cim-devicefile.md)類別來指定存取的邏輯裝置。

</dd> <dt>

[**CIM \_ DeviceConnection**](cim-deviceconnection.md)
</dt> <dd>

[**CIM \_ DeviceConnection**](cim-deviceconnection.md)關聯類別代表兩個或多個已連線的裝置。

</dd> <dt>

[**CIM \_ DeviceErrorCounts**](cim-deviceerrorcounts.md)
</dt> <dd>

[**CIM \_ DeviceErrorCounts**](cim-deviceerrorcounts.md)類別是一個統計類別，其中包含邏輯裝置的錯誤相關計數器。 錯誤的類型是由 CCITT (Rec 733) 和 ISO (IEC 10164-4) 所定義。

</dd> <dt>

[**CIM \_ DeviceFile**](cim-devicefile.md)
</dt> <dd>

[**CIM \_ DeviceFile**](cim-devicefile.md)類別代表代表裝置的邏輯檔案類型。 此慣例適用于使用位元組串流 i/o 模型管理裝置的作業系統。 與此檔案相關聯的邏輯裝置是使用 [**CIM \_ DeviceAccessedByFile**](cim-deviceaccessedbyfile.md) 關聯性所指定。

</dd> <dt>

[**CIM \_ DeviceSAPImplementation**](cim-devicesapimplementation.md)
</dt> <dd>

[**CIM \_ DeviceSAPImplementation**](cim-devicesapimplementation.md)類別代表服務存取點 (SAP) 與其實作為方式之間的關聯。 當許多邏輯裝置與一個 SAP 相關聯時，這些專案會一起運作以提供存取點。 如果有不同的 SAP 執行，每個實施都會導致 SAP 物件的個別具現化。

</dd> <dt>

[**CIM \_ DeviceServiceImplementation**](cim-deviceserviceimplementation.md)
</dt> <dd>

[**CIM \_ DeviceServiceImplementation**](cim-deviceserviceimplementation.md)類別代表服務與其實作為方式之間的關聯。 當多個裝置與一個服務相關聯時，這些專案會一起運作，以提供服務。 如果有不同的服務執行，則每個執行都會導致服務物件的個別具現化。

</dd> <dt>

[**CIM \_ DeviceSoftware**](cim-devicesoftware.md)
</dt> <dd>

[**CIM \_ DeviceSoftware**](cim-devicesoftware.md)關聯性會識別與裝置相關聯的軟體，例如驅動程式、設定或應用程式軟體或固件。

</dd> <dt>

[**CIM \_ 目錄**](cim-directory.md)
</dt> <dd>

[**CIM \_ 目錄**](cim-directory.md)類別代表以邏輯方式分組其包含之資料檔案的檔案類型，並提供群組檔案的路徑資訊。

</dd> <dt>

[**CIM \_ DirectoryAction**](cim-directoryaction.md)
</dt> <dd>

[**CIM \_ DirectoryAction**](cim-directoryaction.md)抽象類別會管理目錄。 目錄建立是由 [**cim \_ CreateDirectoryAction**](cim-createdirectoryaction.md) 類別處理，而目錄移除則由 [**cim \_ RemoveDirectoryAction**](cim-removedirectoryaction.md) 類別處理。

</dd> <dt>

[**CIM \_ DirectoryContainsFile**](cim-directorycontainsfile.md)
</dt> <dd>

[**CIM \_ DirectoryContainsFile**](cim-directorycontainsfile.md)類別代表目錄和該目錄中包含的檔案之間的關聯。

</dd> <dt>

[**CIM \_ DirectorySpecification**](cim-directoryspecification.md)
</dt> <dd>

[**CIM \_ DirectorySpecification**](cim-directoryspecification.md)類別會捕捉 software 元素的主要目錄結構。 此類別是用來將軟體專案的檔案組織成可在電腦系統上重新置放的可管理單位。

</dd> <dt>

[**CIM \_ DirectorySpecificationFile**](cim-directoryspecificationfile.md)
</dt> <dd>

[**Cim \_ DirectorySpecificationFile**](cim-directoryspecificationfile.md)關聯代表包含透過參考 [**CIM \_ DirectorySpecification**](cim-directoryspecification.md)類別所指定之檔案的目錄。

</dd> <dt>

[**CIM \_ DiscreteSensor**](cim-discretesensor.md)
</dt> <dd>

[**CIM \_ DiscreteSensor**](cim-discretesensor.md)類別具有一組可以報告的合法字串值。 這些值會在感應器的 **PossibleValues** 屬性中列舉。 離散感應器一律會有對應至其中一個列舉值的目前讀取。

</dd> <dt>

[**CIM \_ DiskDrive**](cim-diskdrive.md)
</dt> <dd>

[**CIM \_ DiskDrive**](cim-diskdrive.md)類別代表作業系統所見的實體磁片磁碟機。 磁片磁碟機功能對應到磁片磁碟機的邏輯和管理特性，在某些情況下，可能不會反映裝置的實體特性。 實體磁片磁碟機的介面是此類別的成員。 不過，根據另一個邏輯裝置的物件不是此類別的成員。

</dd> <dt>

[**CIM \_ DisketteDrive**](cim-diskettedrive.md)
</dt> <dd>

[**CIM \_ DisketteDrive**](cim-diskettedrive.md)類別代表磁片磁碟機的功能和管理。

</dd> <dt>

[**CIM \_ DiskPartition**](cim-diskpartition.md)
</dt> <dd>

[**CIM \_ DiskPartition**](cim-diskpartition.md)類別代表由作業系統透過分割區的類型和子類型欄位識別的連續邏輯區塊範圍。 磁碟分割應由 [**CIM \_ RealizesDiskPartition**](cim-realizesdiskpartition.md) 關聯) 或建立于儲存磁片區的實體媒體 (直接實現。

</dd> <dt>

[**CIM \_ DiskSpaceCheck**](cim-diskspacecheck.md)
</dt> <dd>

[**CIM \_ DiskSpaceCheck**](cim-diskspacecheck.md)類別會檢查系統的可用磁碟空間量，並在 **AvailableDiskSpace** 屬性中指定它。 詳細資料會 [**與 cim \_**](cim-computersystem.md) FileSystem 物件（描述系統內容）相關聯之 [**Cim \_ FileSystem**](cim-filesystem.md)物件的 **AvailableSpace** 屬性中的值進行比較。 當 **AvailableSpace** 屬性的值大於或等於 **AvailableDiskSpace** 屬性中指定的值時，就會滿足條件。

</dd> <dt>

[**CIM \_ 顯示**](cim-display.md)
</dt> <dd>

[**CIM \_ 顯示**](cim-display.md)類別是用來分組其他顯示裝置的父類別。

</dd> <dt>

[**CIM \_ DMA**](cim-dma.md)
</dt> <dd>

[**CIM \_ DMA**](cim-dma.md)類別代表 (DMA) 的電腦架構直接記憶體存取。

</dd> <dt>

[**CIM \_ 停駐**](cim-docked.md)
</dt> <dd>

[**CIM 停 \_**](cim-docked.md)駐關聯表示兩個底座之間的關聯性。 例如，膝上型電腦 (一種底座) 可停駐在銜接站 (另一種類型的底座) 。 這是明確描述的一般關聯性。

</dd> <dt>

[**CIM \_ ElementCapacity**](cim-elementcapacity.md)
</dt> <dd>

[**Cim \_ ElementCapacity**](cim-elementcapacity.md)類別會將 [**cim \_ PhysicalCapacity**](cim-physicalcapacity.md)物件與一或多個實體元素產生關聯。 它會將最小和最大硬體需求的描述與所述的實體元素)  (或功能相關聯。

</dd> <dt>

[**CIM \_ ElementConfiguration**](cim-elementconfiguration.md)
</dt> <dd>

[**Cim \_ ElementConfiguration**](cim-elementconfiguration.md)關聯會將 [**cim \_ 設定**](cim-configuration.md)物件與一或多個受管理的系統元素產生關聯。 **Cim 設定 \_** 物件代表特定的行為，或相關聯之 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)所需的功能狀態。

</dd> <dt>

[**CIM \_ ElementSetting**](cim-elementsetting.md)
</dt> <dd>

[**CIM \_ ElementSetting**](cim-elementsetting.md)類別代表 managed 系統專案與其定義的設定類別之間的關聯。

</dd> <dt>

[**CIM \_ ElementsLinked**](cim-elementslinked.md)
</dt> <dd>

[**CIM \_ ElementsLinked**](cim-elementslinked.md)關聯表示以實體連結連接在一起的實體元素。

</dd> <dt>

[**CIM \_ ErrorCountersForDevice**](cim-errorcountersfordevice.md)
</dt> <dd>

[**Cim \_ ErrorCountersForDevice**](cim-errorcountersfordevice.md)類別會將 [**cim \_ DeviceErrorCounts**](cim-deviceerrorcounts.md)類別與它所套用的邏輯裝置產生關聯。

</dd> <dt>

[**CIM \_ ExecuteProgram**](cim-executeprogram.md)
</dt> <dd>

[**CIM \_ ExecuteProgram**](cim-executeprogram.md)類別代表可在已安裝 software 元素的系統上執行的檔案。

</dd> <dt>

[**CIM \_ 匯出**](cim-export.md)
</dt> <dd>

[**CIM \_ 匯出**](cim-export.md)類別代表本機檔案系統與其目錄之間的關聯，這表示指定的目錄可供掛接。 匯出整個檔案系統時，目錄應該參考檔案系統的最上層目錄。

</dd> <dt>

[**CIM \_ ExtraCapacityGroup**](cim-extracapacitygroup.md)
</dt> <dd>

[**CIM \_ ExtraCapacityGroup**](cim-extracapacitygroup.md)類別衍生自冗余群組，指出匯總專案的容量或功能比所需的還多。 這類冗余的範例是在系統中安裝 N + 1 電源供應器或風扇。

</dd> <dt>

[**CIM \_ 風扇**](cim-fan.md)
</dt> <dd>

[**CIM \_ 風扇**](cim-fan.md)類別代表風扇冷卻裝置的功能和管理。

</dd> <dt>

[**CIM \_ FileAction**](cim-fileaction.md)
</dt> <dd>

[**CIM \_ FileAction**](cim-fileaction.md)類別可讓作者找出使用者電腦上已存在的檔案，然後將這些檔案移動或複製到新的位置。

</dd> <dt>

[**CIM \_ FileSpecification**](cim-filespecification.md)
</dt> <dd>

[**CIM \_ FileSpecification**](cim-filespecification.md)類別代表系統上或關閉的檔案。 檔案位於 [**CIM \_ DirectorySpecificationFile**](cim-directoryspecificationfile.md) 關聯所識別的目錄中。 [**Invoke**](invoke-method-in-class-cim-filespecification.md)方法會使用此資訊來檢查檔案是否存在。 請注意，不會檢查具有 **Null** 值的屬性。

</dd> <dt>

[**CIM \_ FileStorage**](cim-filestorage.md)
</dt> <dd>

[**CIM \_ FileStorage**](cim-filestorage.md)關聯會連結檔案系統以及透過檔案系統定址的邏輯檔案。

</dd> <dt>

[**CIM \_ 檔案系統**](cim-filesystem.md)
</dt> <dd>

[**CIM \_ FileSystem**](cim-filesystem.md)類別代表電腦系統本機的檔案或資料集，或從檔案伺服器遠端掛接的檔案或資料集。

</dd> <dt>

[**CIM \_ FlatPanel**](cim-flatpanel.md)
</dt> <dd>

[**CIM \_ FlatPanel**](cim-flatpanel.md)類別代表平面化面板邏輯裝置的功能和管理。

</dd> <dt>

[**CIM \_ FromDirectoryAction**](cim-fromdirectoryaction.md)
</dt> <dd>

[**CIM \_ FromDirectoryAction**](cim-fromdirectoryaction.md)關聯會識別檔案動作的來原始目錄。 使用這個關聯時，假設來原始目錄是由先前的動作所建立。 此關聯無法與 [**CIM \_ FromDirectorySpecification**](cim-fromdirectoryspecification.md) 關聯存在; 檔案動作只能包含單一來原始目錄。

</dd> <dt>

[**CIM \_ FromDirectorySpecification**](cim-fromdirectoryspecification.md)
</dt> <dd>

[**CIM \_ FromDirectorySpecification**](cim-fromdirectoryspecification.md)關聯會識別檔案動作的來原始目錄。 使用這個關聯時，假設來原始目錄已經存在。 此關聯無法與 [**CIM \_ FromDirectoryAction**](cim-fromdirectoryaction.md) 關聯存在; 檔案動作只能包含單一來原始目錄。

</dd> <dt>

[**CIM \_ FRU**](cim-fru.md)
</dt> <dd>

[**CIM \_ FRU**](cim-fru.md)類別代表廠商定義的產品和實體元素集合，與現場可更換單元相關聯 (FRU) 在客戶的位置支援、維護或升級產品。

</dd> <dt>

[**CIM \_ FRUIncludesProduct**](cim-fruincludesproduct.md)
</dt> <dd>

[**CIM \_ FRUIncludesProduct**](cim-fruincludesproduct.md)類別指出現場可更換單元 (FRU) 可能由其他產品組成。

</dd> <dt>

[**CIM \_ FRUPhysicalElements**](cim-fruphysicalelements.md)
</dt> <dd>

[**CIM \_ FRUPhysicalElements**](cim-fruphysicalelements.md)類別代表組成現場可更換單元 (FRU) 的實體元素。

</dd> <dt>

[**CIM \_ HeatPipe**](cim-heatpipe.md)
</dt> <dd>

[**CIM \_ HeatPipe**](cim-heatpipe.md)類別代表熱度管道冷卻裝置的功能和管理。

</dd> <dt>

[**CIM \_ HostedAccessPoint**](cim-hostedaccesspoint.md)
</dt> <dd>

[**CIM \_ HostedAccessPoint**](cim-hostedaccesspoint.md)類別代表服務存取點 (SAP) 和提供它的系統之間的關聯。 每個系統可能會裝載許多 Sap。

</dd> <dt>

[**CIM \_ HostedBootSAP**](cim-hostedbootsap.md)
</dt> <dd>

[**Cim \_ HostedBootSAP**](cim-hostedbootsap.md)類別會定義 [**cim \_ BootSAP**](cim-bootsap.md)類別的裝載單一電腦系統。 由於此關聯性是從 [**cim \_ HostedAccessPoint**](cim-hostedaccesspoint.md)子類別化，因此它會繼承針對 [**cim \_ ServiceAccessPoint**](cim-serviceaccesspoint.md)定義的範圍/命名配置，其中存取點會延遲至其主機系統。 在此情況下， **CIM \_ BootSAP** 必須延後至其裝載的 [**CIM \_ UnitaryComputerSystem**](cim-unitarycomputersystem.md) 類別。

</dd> <dt>

[**CIM \_ HostedBootService**](cim-hostedbootservice.md)
</dt> <dd>

[**CIM \_ HostedBootService**](cim-hostedbootservice.md)類別會將主機系統和開機服務產生關聯。 由於此關聯性是從 [**CIM \_ HostedService**](cim-hostedservice.md)子類別化，因此它會繼承為服務定義的範圍/命名配置，其中服務會延遲至其主機系統。

</dd> <dt>

[**CIM \_ HostedFileSystem**](cim-hostedfilesystem.md)
</dt> <dd>

[**CIM \_ HostedFileSystem**](cim-hostedfilesystem.md)關聯代表電腦系統與電腦系統上所裝載之檔案系統之間的連結。

</dd> <dt>

[**CIM \_ HostedJobDestination**](cim-hostedjobdestination.md)
</dt> <dd>

[**CIM \_ HostedJobDestination**](cim-hostedjobdestination.md)類別代表作業目的地與其所在系統之間的關聯。 系統可能會裝載許多作業佇列。 作業目的地會延後到裝載系統。

</dd> <dt>

[**CIM \_ HostedService**](cim-hostedservice.md)
</dt> <dd>

[**CIM \_ HostedService**](cim-hostedservice.md)類別代表服務與功能所在系統之間的關聯。 系統可能會裝載許多服務，而這些服務會延後到裝載系統。 此模型不代表跨多個系統裝載的服務。

</dd> <dt>

[**CIM \_ InfraredController**](cim-infraredcontroller.md)
</dt> <dd>

[**CIM \_ InfraredController**](cim-infraredcontroller.md)類別代表紅外線控制器的功能和管理。

</dd> <dt>

[**CIM \_ InstalledOS**](cim-installedos.md)
</dt> <dd>

[**CIM \_ InstalledOS**](cim-installedos.md)關聯類別代表電腦系統與已安裝作業系統之間的連結。 作業系統會在電腦系統的儲存範圍內安裝 (例如，複製到磁片磁碟機或下載至記憶體) 。

</dd> <dt>

[**CIM \_ InstalledSoftwareElement**](cim-installedsoftwareelement.md)
</dt> <dd>

[**CIM \_ InstalledSoftwareElement**](cim-installedsoftwareelement.md)類別會將電腦系統與已安裝的軟體元素建立關聯。

</dd> <dt>

[**CIM \_ IRQ**](cim-irq.md)
</dt> <dd>

[**CIM \_ IRQ**](cim-irq.md)類別代表 Intel 架構中斷要求線路 (IRQ) 。

</dd> <dt>

[**CIM \_ 作業**](cim-job.md)
</dt> <dd>

[**CIM \_ 作業**](cim-job.md)類別代表系統的工作單位，例如列印工作。 作業與進程不同，因為可以排程工作。

</dd> <dt>

[**CIM \_ JobDestination**](cim-jobdestination.md)
</dt> <dd>

[**CIM \_ JobDestination**](cim-jobdestination.md)類別代表提交工作以進行處理的位置。 它可以參考包含零或多個作業的佇列，例如包含列印工作的列印佇列。 作業目的地裝載于系統上，類似于在系統上託管服務的方式。

</dd> <dt>

[**CIM \_ JobDestinationJobs**](cim-jobdestinationjobs.md)
</dt> <dd>

[**CIM \_ JobDestinationJobs**](cim-jobdestinationjobs.md)關聯描述提交作業以進行處理的位置， (也就是工作目的地) 。

</dd> <dt>

[**CIM \_ 鍵盤**](cim-keyboard.md)
</dt> <dd>

[**CIM \_ 鍵盤**](cim-keyboard.md)類別代表鍵盤邏輯裝置的功能和管理。

</dd> <dt>

[**CIM \_ LinkHasConnector**](cim-linkhasconnector.md)
</dt> <dd>

[**CIM \_ LinkHasConnector**](cim-linkhasconnector.md)類別會將用來作為實體連接器的纜線和連結（連接實體元素）相關聯。 此關聯會明確定義適用于 [**CIM \_ PhysicalLink**](cim-physicallink.md)之連接器的關聯性。

</dd> <dt>

[**CIM \_ LocalFileSystem**](cim-localfilesystem.md)
</dt> <dd>

[**CIM \_ LocalFileSystem**](cim-localfilesystem.md)類別代表由電腦系統透過本機所控制的檔案存放區，例如 (直接裝置驅動程式存取) 。 檔案存放區可以直接由電腦系統管理，而不需要另一部電腦作為檔案伺服器。 但是針對叢集檔案系統，檔案系統是本機的，因此會延遲到叢集。

</dd> <dt>

[**CIM \_ 位置**](cim-location.md)
</dt> <dd>

[**CIM \_ Location**](cim-location.md)類別代表實體元素的位置和位址。

</dd> <dt>

[**CIM \_ LogicalDevice**](cim-logicaldevice.md)
</dt> <dd>

[**CIM \_ LogicalDevice**](cim-logicaldevice.md)類別代表可能或可能不會在實體硬體中實現的硬體實體。

</dd> <dt>

[**CIM \_ LogicalDisk**](cim-logicaldisk.md)
</dt> <dd>

[**CIM \_ LogicalDisk**](cim-logicaldisk.md)類別代表由檔案系統透過磁片 **DeviceID** (key) 欄位識別的連續邏輯區塊範圍。 例如，在 Windows 環境中， **DeviceID** 欄位包含磁碟機號;在 UNIX 環境中，它包含存取路徑;在 NetWare 環境中，它包含磁片區名稱。

</dd> <dt>

[**CIM \_ LogicalDiskBasedOnPartition**](cim-logicaldiskbasedonpartition.md)
</dt> <dd>

[**CIM \_ LogicalDiskBasedOnPartition**](cim-logicaldiskbasedonpartition.md)類別會將邏輯磁片與其所在的磁碟分割建立關聯。

</dd> <dt>

[**CIM \_ LogicalDiskBasedOnVolumeSet**](cim-logicaldiskbasedonvolumeset.md)
</dt> <dd>

[**CIM \_ LogicalDiskBasedOnVolumeSet**](cim-logicaldiskbasedonvolumeset.md)關聯會將邏輯磁片與找到它們的磁片區相關聯。 邏輯磁片可根據單一磁片區 (例如，由軟體磁片區管理員) 或磁碟分割所公開。

</dd> <dt>

[**CIM \_ LogicalElement**](cim-logicalelement.md)
</dt> <dd>

[**CIM \_ LogicalElement**](cim-logicalelement.md)類別是代表抽象系統元件的所有系統元件的基類，例如設定檔、進程或系統功能（以邏輯裝置的形式）。

</dd> <dt>

[**CIM \_ LogicalFile**](cim-logicalfile.md)
</dt> <dd>

[**CIM \_ LogicalFile**](cim-logicalfile.md)類別代表資料的命名集合，可以是可執行程式碼，位於儲存區的檔案系統中。

</dd> <dt>

[**CIM \_ LogicalIdentity**](cim-logicalidentity.md)
</dt> <dd>

[**CIM \_ LogicalIdentity**](cim-logicalidentity.md)類別是抽象和泛型關聯，表示兩個邏輯元素代表相同基礎實體的不同層面。

</dd> <dt>

[**CIM \_ MagnetoOpticalDrive**](cim-magnetoopticaldrive.md)
</dt> <dd>

[**CIM \_ MagnetoOpticalDrive**](cim-magnetoopticaldrive.md)類別代表磁光磁片磁碟機的功能和管理，也就是媒體存取裝置的子類型。

</dd> <dt>

[**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)
</dt> <dd>

[**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)類別是 system 元素階層的基類。 任何可辨別的系統元件都是包含在這個類別中的候選。

</dd> <dt>

[**CIM \_ ManagementController**](cim-managementcontroller.md)
</dt> <dd>

[**CIM \_ ManagementController**](cim-managementcontroller.md)類別與管理控制器的功能和管理有關。

</dd> <dt>

[**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)
</dt> <dd>

[**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)類別代表存取一或多個媒體的能力，然後使用該媒體來儲存和取出資料。

</dd> <dt>

[**CIM \_ MediaPresent**](cim-mediapresent.md)
</dt> <dd>

[**CIM \_ MediaPresent**](cim-mediapresent.md)關聯描述必須透過媒體存取裝置存取儲存區的關聯性。

</dd> <dt>

[**CIM \_ 記憶體**](cim-memory.md)
</dt> <dd>

[**CIM \_ 記憶體**](cim-memory.md)類別代表記憶體相關邏輯裝置的功能和管理。

</dd> <dt>

[**CIM \_ MemoryCapacity**](cim-memorycapacity.md)
</dt> <dd>

[**CIM \_ MemoryCapacity**](cim-memorycapacity.md)類別代表可以安裝在實體元素上的記憶體，以及最小和最大的設定。 目前已安裝的記憶體和元素的最小和最大需求的資訊位於 [**CIM \_ PhysicalMemory**](cim-physicalmemory.md) 類別的實例中。

</dd> <dt>

[**CIM \_ MemoryCheck**](cim-memorycheck.md)
</dt> <dd>

[**CIM \_ MemoryCheck**](cim-memorycheck.md)類別會指定系統上必須可用的最小記憶體數量的條件。

</dd> <dt>

[**CIM \_ MemoryMappedIO**](cim-memorymappedio.md)
</dt> <dd>

[**CIM \_ MemoryMappedIO**](cim-memorymappedio.md)類別代表電腦架構記憶體對應 i/o。 此類別會解決記憶體和埠 i/o 資源。

</dd> <dt>

[**CIM \_ MemoryOnCard**](cim-memoryoncard.md)
</dt> <dd>

[**CIM \_ MemoryOnCard**](cim-memoryoncard.md)類別會將位於主機板、介面卡等上的實體記憶體相關聯。 此關聯會明確定義記憶體與卡片之間的關聯性。

</dd> <dt>

[**CIM \_ MemoryWithMedia**](cim-memorywithmedia.md)
</dt> <dd>

[**CIM \_ MemoryWithMedia**](cim-memorywithmedia.md)類別會將實體記憶體與實體媒體和其墨水匣產生關聯。 記憶體會提供媒體識別，並儲存使用者專屬的資料。

</dd> <dt>

[**CIM \_ ModifySettingAction**](cim-modifysettingaction.md)
</dt> <dd>

[**CIM \_ ModifySettingAction**](cim-modifysettingaction.md)類別代表針對特定專案（具有特定值）修改特定設定檔案的資訊。

</dd> <dt>

[**CIM \_ MonitorResolution**](cim-monitorresolution.md)
</dt> <dd>

[**CIM \_ MonitorResolution**](cim-monitorresolution.md)類別代表水準和垂直解析度之間的關聯性，以及桌面監視器的重新整理頻率和掃描模式。 影片控制器物件中指定了值。

</dd> <dt>

[**CIM \_ MonitorSetting**](cim-monitorsetting.md)
</dt> <dd>

[**CIM \_ MonitorSetting**](cim-monitorsetting.md)類別會將監視器解析度與其套用的桌面監視器產生關聯。

</dd> <dt>

[**CIM \_ 掛接**](cim-mount.md)
</dt> <dd>

[**CIM \_ 裝載**](cim-mount.md)類別代表檔案系統與其附加目錄之間的關聯。

</dd> <dt>

[**CIM \_ MultiStateSensor**](cim-multistatesensor.md)
</dt> <dd>

[**CIM \_ MultiStateSensor**](cim-multistatesensor.md)類別代表一組二元感應器的多重成員，其中每個二進位感應器都會報告布林結果。

</dd> <dt>

[**CIM \_ NetworkAdapter**](cim-networkadapter.md)
</dt> <dd>

[**CIM \_ NetworkAdapter**](cim-networkadapter.md)類別是一個抽象類別，用來定義一般網路硬體概念 (例如，) 的永久位址或速度。 這項資訊是使用 [**CIM \_ DeviceSAPImplementation**](cim-devicesapimplementation.md) 關聯來傳達。

</dd> <dt>

[**CIM \_ NFS**](cim-nfs.md)
</dt> <dd>

[**CIM \_ NFS**](cim-nfs.md)類別代表從電腦系統使用網路檔案系統 (NFS) 通訊協定掛接的遠端檔案系統。

</dd> <dt>

[**CIM \_ NonVolatileStorage**](cim-nonvolatilestorage.md)
</dt> <dd>

[**CIM \_ NonVolatileStorage**](cim-nonvolatilestorage.md)類別代表非暫時性儲存的功能和管理。 靜態記憶體原生包含 flash 和 ROM 存放裝置。

</dd> <dt>

[**CIM \_ NumericSensor**](cim-numericsensor.md)
</dt> <dd>

[**CIM \_ NumericSensor**](cim-numericsensor.md)類別代表會傳回數值讀數並選擇性支援臨界值設定的數值感應器。

</dd> <dt>

[**CIM \_ 作業系統**](cim-operatingsystem.md)
</dt> <dd>

[**CIM 作業系統 \_**](cim-operatingsystem.md)類別代表電腦作業系統，由軟體和固件組成，可讓電腦系統的硬體可用。

</dd> <dt>

[**CIM \_ OperatingSystemSoftwareFeature**](cim-operatingsystemsoftwarefeature.md)
</dt> <dd>

[**CIM \_ OperatingSystemSoftwareFeature**](cim-operatingsystemsoftwarefeature.md)類別代表組成作業系統的軟體功能。

</dd> <dt>

[**CIM \_ OSProcess**](cim-osprocess.md)
</dt> <dd>

[**CIM \_ OSProcess**](cim-osprocess.md)類別會將作業系統以及在作業系統環境中執行的一或多個處理常式產生關聯。

</dd> <dt>

[**CIM \_ OSVersionCheck**](cim-osversioncheck.md)
</dt> <dd>

[**CIM \_ OSVersionCheck**](cim-osversioncheck.md)類別會指定可支援軟體元素的作業系統版本。

</dd> <dt>

[**CIM \_ PackageAlarm**](cim-packagealarm.md)
</dt> <dd>

[**CIM \_ PackageAlarm**](/windows/desktop/SecCrypto/extendedproperties-newenum)關聯代表將警示裝置安裝為套件一部分的關聯性。 此安裝指出封裝環境的問題，也就是其安全性狀態或其整體健全狀況。

</dd> <dt>

[**CIM \_ PackageCooling**](cim-packagecooling.md)
</dt> <dd>

[**CIM \_ PackageCooling**](cim-packagecooling.md)關聯代表在套件中安裝冷卻裝置的關聯性（例如底座或機架），以協助封裝的冷卻。

</dd> <dt>

[**CIM \_ PackagedComponent**](cim-packagedcomponent.md)
</dt> <dd>

[**CIM \_ PackagedComponent**](cim-packagedcomponent.md)關聯表示一個明確的關聯性，其中元件通常包含在實體封裝中，例如底座或卡片。

</dd> <dt>

[**CIM \_ PackageInChassis**](cim-packageinchassis.md)
</dt> <dd>

[**CIM \_ PackageInChassis**](cim-packageinchassis.md)關聯代表底座可包含其他套件的關聯性，例如其他底座和卡片。

</dd> <dt>

[**CIM \_ PackageInSlot**](cim-packageinslot.md)
</dt> <dd>

[**CIM \_ PackageInSlot**](cim-packageinslot.md)關聯代表裝置卡與其掛接之底座之間的關聯性。

</dd> <dt>

[**CIM \_ PackageTempSensor**](cim-packagetempsensor.md)
</dt> <dd>

[**CIM \_ PackageTempSensor**](cim-packagetempsensor.md)關聯表示通常會在套件中安裝溫度感應器的關聯性，例如底座或機架，以監視封裝的環境。

</dd> <dt>

[**CIM \_ ParallelController**](cim-parallelcontroller.md)
</dt> <dd>

[**CIM \_ ParallelController**](cim-parallelcontroller.md)關聯與平行埠邏輯裝置的功能和管理有關。

</dd> <dt>

[**CIM \_ ParticipatesInSet**](cim-participatesinset.md)
</dt> <dd>

[**CIM \_ ParticipatesInSet**](cim-participatesinset.md)類別會識別應該一起取代的實體元素。

</dd> <dt>

[**CIM \_ PCIController**](cim-pcicontroller.md)
</dt> <dd>

[**CIM \_ PCIController**](cim-pcicontroller.md)類別代表 PCI 控制器的屬性和管理。 此類別中的屬性及其子類別會定義于 PCI SIG 所發佈的各種 PCI 規格中。

</dd> <dt>

[**CIM \_ PCMCIAController**](cim-pcmciacontroller.md)
</dt> <dd>

[**CIM \_ PCMCIAController**](cim-pcmciacontroller.md)類別代表個人電腦記憶卡國際協會 (PCMCIA) 控制器的功能和管理。

</dd> <dt>

[**CIM \_ PCVideoController**](cim-pcvideocontroller.md)
</dt> <dd>

[**CIM \_ PCVideoController**](cim-pcvideocontroller.md)代表個人電腦影片控制器的功能和管理，也就是影片控制器的子類型。

</dd> <dt>

[**CIM \_ PExtentRedundancyComponent**](cim-pextentredundancycomponent.md)
</dt> <dd>

[**CIM \_ PExtentRedundancyComponent**](cim-pextentredundancycomponent.md)類別代表參與儲存體冗余群組的實體範圍。

</dd> <dt>

[**CIM \_ PhysicalCapacity**](cim-physicalcapacity.md)
</dt> <dd>

[**CIM \_ PhysicalCapacity**](cim-physicalcapacity.md)類別是一種抽象類別，代表實體元素的最小和最大需求，以及其支援不同硬體類型的能力。 例如，最小和最大記憶體需求可以模型化為 **CIM \_ PhysicalCapacity** 的子類別。

</dd> <dt>

[**CIM \_ PhysicalComponent**](cim-physicalcomponent.md)
</dt> <dd>

[**CIM \_ PhysicalComponent**](cim-physicalcomponent.md)類別代表封裝內的低層級或基本元件。 不是連結、連接器或封裝的實體元素是此類別 (或成員) 的子系。

</dd> <dt>

[**CIM \_ PhysicalConnector**](cim-physicalconnector.md)
</dt> <dd>

[**CIM \_ PhysicalConnector**](cim-physicalconnector.md)類別代表用來連接到其他元素的任何實體元素。 任何可以連接及傳輸兩個或多個實體元素之間的信號或電源的物件，都是此類別的子系 (或成員) 。

</dd> <dt>

[**CIM \_ PhysicalElement**](cim-physicalelement.md)
</dt> <dd>

[**CIM \_ PhysicalElement**](cim-physicalelement.md)子類別會定義具有不同實體身分識別之系統的任何元件。 可以實體附加至物件的標籤可以定義這個類別的實例。

</dd> <dt>

[**CIM \_ PhysicalElementLocation**](cim-physicalelementlocation.md)
</dt> <dd>

[**Cim \_ PhysicalElementLocation**](cim-physicalelementlocation.md)類別會將實體元素與 [**CIM \_ 位置**](cim-location.md)物件產生關聯，以供清查或取代之用。

</dd> <dt>

[**CIM \_ PhysicalExtent**](cim-physicalextent.md)
</dt> <dd>

[**CIM \_ PhysicalExtent**](cim-physicalextent.md)類別代表 SCC RAID 的執行。 它會在單一存放裝置上定義連續可定址的區塊位址，這些位址會被視為相同 [**CIM \_ StorageRedundancyGroup**](cim-storageredundancygroup.md) 類別中的單一儲存區。 替代方式是使用自動設定時，是要具現化或擴充 [**CIM \_ AggregatePExtent**](cim-aggregatepextent.md) 類別。

</dd> <dt>

[**CIM \_ PhysicalFrame**](cim-physicalframe.md)
</dt> <dd>

[**CIM \_ PhysicalFrame**](cim-physicalframe.md)類別是機架、底座和其他框架主機殼的父類別，因為它們是在擴充類別中定義的。 **VisibleAlarm** 和 **AudibleAlarm** 等屬性，以及與安全性缺口相關的資料會包含在這個父類別中。

</dd> <dt>

[**CIM \_ PhysicalLink**](cim-physicallink.md)
</dt> <dd>

[**CIM \_ PhysicalLink**](cim-physicallink.md)類別代表實體元素的纜線。

</dd> <dt>

[**CIM \_ PhysicalMedia**](cim-physicalmedia.md)
</dt> <dd>

[**CIM \_ PhysicalMedia**](cim-physicalmedia.md)類別代表檔和儲存媒體的類型，例如磁帶、CD rom 等等。

</dd> <dt>

[**CIM \_ PhysicalMemory**](cim-physicalmemory.md)
</dt> <dd>

[**CIM \_ PhysicalMemory**](cim-physicalmemory.md)類別代表低層級的記憶體裝置，例如 simm、dimm、原始記憶體晶片等等。

</dd> <dt>

[**CIM \_ PhysicalPackage**](cim-physicalpackage.md)
</dt> <dd>

[**CIM \_ PhysicalPackage**](cim-physicalpackage.md)類別代表包含或裝載其他元件的實體元素。 範例包括機架主機殼或介面卡。

</dd> <dt>

[**CIM \_ PointingDevice**](cim-pointingdevice.md)
</dt> <dd>

[**CIM \_ PointingDevice**](cim-pointingdevice.md)類別代表指向顯示區域的裝置。 任何操作指標的裝置，或指向視覺效果顯示器上的區域，都是此類別的成員。 例如，滑鼠、手寫筆、觸控板或平板電腦。

</dd> <dt>

[**CIM \_ POTSModem**](cim-potsmodem.md)
</dt> <dd>

[**CIM \_ POTSModem**](cim-potsmodem.md)類別代表一種裝置，可透過連接到單純的舊電話系統 (POTS) 網路，將二進位資料轉譯成 wave modulations 進行音效型傳輸。

</dd> <dt>

[**CIM \_ 電源**](cim-powersupply.md)
</dt> <dd>

[**CIM 電源 \_ 供應器**](cim-powersupply.md)類別代表電源供應器邏輯裝置的功能和管理。

</dd> <dt>

[**CIM \_ 印表機**](cim-printer.md)
</dt> <dd>

[**CIM \_ 印表機**](cim-printer.md)類別代表印表機邏輯裝置的功能和管理。

</dd> <dt>

[**CIM \_ 進程**](cim-process.md)
</dt> <dd>

[**CIM \_ 進程**](cim-process.md)類別代表執行中程式的單一實例。 使用者通常會將進程視為應用程式或工作。

</dd> <dt>

[**CIM \_ ProcessExecutable**](cim-processexecutable.md)
</dt> <dd>

[**CIM \_ ProcessExecutable**](cim-processexecutable.md)類別代表進程和資料檔之間的連結，表示檔案參與處理常式的執行。

</dd> <dt>

[**CIM \_ 處理器**](cim-processor.md)
</dt> <dd>

[**CIM \_ 處理器**](cim-processor.md)類別代表處理器邏輯裝置的功能和管理。

</dd> <dt>

[**CIM \_ ProcessThread**](cim-processthread.md)
</dt> <dd>

[**CIM \_ ProcessThread**](cim-processthread.md)類別代表進程與進程內容中執行之執行緒之間的連結。

</dd> <dt>

[**CIM \_ 產品**](cim-product.md)
</dt> <dd>

[**CIM \_ Product**](cim-product.md)類別是代表實體元素集合、軟體功能和其他產品（以單位形式取得）的實體類別。 取得意味著供應商與消費者之間的合約，可能會影響產品授權、支援和擔保。

</dd> <dt>

[**CIM \_ ProductFRU**](cim-productfru.md)
</dt> <dd>

[**CIM \_ ProductFRU**](cim-productfru.md)類別代表產品與現場可更換單元之間的關聯 (FRU) ，其提供已被取代之產品元件的相關資訊。

</dd> <dt>

[**CIM \_ ProductParentChild**](cim-productparentchild.md)
</dt> <dd>

[**CIM \_ ProductParentChild**](cim-productparentchild.md)關聯會定義產品之間的父子式階層。 例如，產品可以與其他產品配套。

</dd> <dt>

[**CIM \_ ProductPhysicalElements**](cim-productphysicalelements.md)
</dt> <dd>

[**CIM \_ ProductPhysicalElements**](cim-productphysicalelements.md)類別代表組成產品的實體元素。

</dd> <dt>

[**CIM \_ ProductProductDependency**](cim-productproductdependency.md)
</dt> <dd>

[**CIM \_ ProductProductDependency**](cim-productproductdependency.md)類別代表兩項產品之間的關聯，這表示必須安裝或不存在才能讓另一個產品運作。 這在概念上相當於 [**CIM \_ ServiceServiceDependency**](cim-serviceservicedependency.md) 關聯。

</dd> <dt>

[**CIM \_ ProductSoftwareFeatures**](cim-productsoftwarefeatures.md)
</dt> <dd>

[**CIM \_ ProductSoftwareFeatures**](cim-productsoftwarefeatures.md)關聯會識別特定產品的軟體功能。

</dd> <dt>

[**CIM \_ ProductSupport**](cim-productsupport.md)
</dt> <dd>

[**CIM \_ ProductSupport**](cim-productsupport.md)類別代表產品與支援存取之間的關聯，可傳達如何取得產品的支援。 產品有各種類型的支援，相同的支持對象可以提供多項產品的協助。

</dd> <dt>

[**CIM \_ ProtectedSpaceExtent**](cim-protectedspaceextent.md)
</dt> <dd>

[**CIM \_ ProtectedSpaceExtent**](cim-protectedspaceextent.md)類別代表可定址的邏輯區塊位址，這些位址會被視為單一儲存範圍，但位於單一實體範圍。

</dd> <dt>

[**CIM \_ PSExtentBasedOnPExtent**](cim-psextentbasedonpextent.md)
</dt> <dd>

[**CIM \_ PSExtentBasedOnPExtent**](cim-psextentbasedonpextent.md)類別會將以實體範圍為基礎的受保護空間範圍產生關聯。

</dd> <dt>

[**CIM \_ 機架**](cim-rack.md)
</dt> <dd>

[**CIM \_ 機架**](cim-rack.md)類別代表機架 (實體框架或主機殼) 在其中儲存底座。 通常，機架代表主機殼;所有運作中的元件都會封裝在底座中。

</dd> <dt>

[**CIM \_ 意識**](cim-realizes.md)
</dt> <dd>

[**CIM \_ 認識**](cim-realizes.md)類別代表定義邏輯裝置與執行裝置之實體元件之間對應的關聯。

</dd> <dt>

[**CIM \_ RealizesAggregatePExtent**](cim-realizesaggregatepextent.md)
</dt> <dd>

[**Cim \_ RealizesAggregatePExtent**](cim-realizesaggregatepextent.md)關聯表示在實體媒體上實現 [**CIM \_ AggregatePExtent**](cim-aggregatepextent.md)類別的關聯性。

</dd> <dt>

[**CIM \_ RealizesDiskPartition**](cim-realizesdiskpartition.md)
</dt> <dd>

[**CIM \_ RealizesDiskPartition**](cim-realizesdiskpartition.md)類別代表實體媒體上的磁碟分割，此磁碟分割會建立原始 SCSI 或 IDE 磁片磁碟機上磁碟分割的建立模型。

</dd> <dt>

[**CIM \_ RealizesPExtent**](cim-realizespextent.md)
</dt> <dd>

[**CIM \_ RealizesPExtent**](cim-realizespextent.md)關聯表示在實體媒體上實現實體範圍的關聯性。 此外，也會指定實體媒體上實體範圍的起始位址。

</dd> <dt>

[**CIM \_ RebootAction**](cim-rebootaction.md)
</dt> <dd>

[**CIM \_ RebootAction**](cim-rebootaction.md)類別會導致系統重新開機，其中安裝了 software 元素。

</dd> <dt>

[**CIM \_ RedundancyComponent**](cim-redundancycomponent.md)
</dt> <dd>

[**CIM \_ RedundancyComponent**](cim-redundancycomponent.md)類別會將由受管理系統專案組成的複製群組產生關聯，並指出這些元素一起提供冗余。 在冗余群組中匯總的所有元素都應該是相同物件類別的具現化。

</dd> <dt>

[**CIM \_ RedundancyGroup**](cim-redundancygroup.md)
</dt> <dd>

[**CIM \_ RedundancyGroup**](cim-redundancygroup.md)類別代表 managed 系統專案的集合，這些元素表示匯總的元件會一起提供冗余。 在冗余群組中匯總的所有元素都應該是相同物件類別的具現化。

</dd> <dt>

[**CIM \_ 冷藏庫取出**](cim-refrigeration.md)
</dt> <dd>

[**CIM \_ 冷藏庫取出**](cim-refrigeration.md)類別代表冷藏庫取出冷卻裝置的功能和管理。

</dd> <dt>

[**CIM \_ RelatedStatistics**](cim-relatedstatistics.md)
</dt> <dd>

[**Cim \_ RelatedStatistics**](cim-relatedstatistics.md)關聯表示階層以及相關 [**CIM \_ StatisticalInformation**](cim-statisticalinformation.md)類別的相依性。

</dd> <dt>

[**CIM \_ RemoteFileSystem**](cim-remotefilesystem.md)
</dt> <dd>

[**CIM \_ RemoteFileSystem**](cim-remotefilesystem.md)類別代表透過網路相關服務來存取的遠端檔案系統。 在此情況下，檔案存放區是由電腦主控，作為檔案伺服器。

</dd> <dt>

[**CIM \_ RemoveDirectoryAction**](cim-removedirectoryaction.md)
</dt> <dd>

[**CIM \_ RemoveDirectoryAction**](cim-removedirectoryaction.md)類別會移除軟體元素的目錄。

</dd> <dt>

[**CIM \_ RemoveFileAction**](cim-removefileaction.md)
</dt> <dd>

[**CIM \_ RemoveFileAction**](cim-removefileaction.md)類別會卸載檔案。

</dd> <dt>

[**CIM \_ ReplacementSet**](cim-replacementset.md)
</dt> <dd>

[**CIM \_ ReplacementSet**](cim-replacementset.md)類別會匯總必須一起取代的實體元素。 例如，更換記憶卡時，也可以移除並取代元件記憶體晶片。 或者，這個關聯可以用來取代或升級一組記憶體晶片。

</dd> <dt>

[**CIM \_ ResidesOnExtent**](cim-residesonextent.md)
</dt> <dd>

[**CIM \_ ResidesOnExtent**](cim-residesonextent.md)類別代表檔案系統與其所在儲存區之間的關聯。 一般而言，檔案系統位於邏輯磁片上。

</dd> <dt>

[**CIM \_ RunningOS**](cim-runningos.md)
</dt> <dd>

[**CIM \_ RunningOS**](cim-runningos.md)類別代表目前正在執行的作業系統。 電腦系統上的任何時間最多可以執行一個作業系統;電腦系統目前可能無法開機，或其作業系統可能不明。

</dd> <dt>

[**CIM \_ SAPSAPDependency**](cim-sapsapdependency.md)
</dt> <dd>

[**CIM \_ SAPSAPDependency**](cim-sapsapdependency.md)類別是 (sap) 的兩個服務存取點之間的關聯，這表示第一個 sap 需要第二個 sap 才能與其服務連接。

</dd> <dt>

[**CIM \_ 掃描器**](cim-scanner.md)
</dt> <dd>

[**CIM \_ 掃描器**](cim-scanner.md)代表掃描器邏輯裝置的功能和管理。

</dd> <dt>

[**CIM \_ microsoft.hyperv.powershell.scsicontroller**](cim-scsicontroller.md)
</dt> <dd>

[**CIM \_ microsoft.hyperv.powershell.scsicontroller**](cim-scsicontroller.md)類別代表 SCSI 控制器邏輯裝置的功能和管理。

</dd> <dt>

[**CIM \_ SCSIInterface**](cim-scsiinterface.md)
</dt> <dd>

代表 [**CIM \_ ControlledBy**](cim-controlledby.md) 關聯性，指出哪些裝置可透過 SCSI 控制器和存取特性來存取。

</dd> <dt>

[**CIM \_ 感應器**](cim-sensor.md)
</dt> <dd>

[**CIM \_ 感應器**](cim-sensor.md)類別代表能夠測量實體屬性特性的硬體裝置 (例如，單一電腦系統) 的溫度或電壓特性。

</dd> <dt>

[**CIM \_ SerialController**](cim-serialcontroller.md)
</dt> <dd>

[**CIM \_ SerialController**](cim-serialcontroller.md)類別代表序列埠邏輯裝置的功能和管理。

</dd> <dt>

[**CIM \_ SerialInterface**](cim-serialinterface.md)
</dt> <dd>

[**Cim \_ SerialInterface**](cim-serialinterface.md)類別代表 [**cim \_ ControlledBy**](cim-controlledby.md)關聯性，指出哪些裝置可透過序列控制器存取，以及存取的特性。

</dd> <dt>

[**CIM \_ 服務**](cim-service.md)
</dt> <dd>

[**CIM \_ 服務**](cim-service.md)類別代表邏輯元素，其中包含的資訊可代表和管理裝置或軟體功能所提供的功能。 服務是一般用途的物件，用來設定及管理功能的執行;這並不是功能本身。

</dd> <dt>

[**CIM \_ ServiceAccessBySAP**](cim-serviceaccessbysap.md)
</dt> <dd>

[**CIM \_ ServiceAccessBySAP**](cim-serviceaccessbysap.md)關聯類別代表服務的存取點。 例如，您可以透過 NetWare、Macintosh 或 Windows 服務存取點來存取印表機， (sap) ，這些都可能裝載在不同的系統上。

</dd> <dt>

[**CIM \_ ServiceAccessPoint**](cim-serviceaccesspoint.md)
</dt> <dd>

[**CIM \_ ServiceAccessPoint**](cim-serviceaccesspoint.md)類別代表使用或叫用服務的能力。 存取點代表可供其他實體使用的服務。

</dd> <dt>

[**CIM \_ ServiceSAPDependency**](cim-servicesapdependency.md)
</dt> <dd>

[**CIM \_ ServiceSAPDependency**](cim-servicesapdependency.md)類別代表服務與服務存取點之間的關聯 (SAP) ，這表示服務會使用參考的 SAP 來提供其功能。

</dd> <dt>

[**CIM \_ ServiceServiceDependency**](cim-serviceservicedependency.md)
</dt> <dd>

[**CIM \_ ServiceServiceDependency**](cim-serviceservicedependency.md)類別代表兩個服務之間的關聯。

</dd> <dt>

[**CIM \_ 設定**](cim-setting.md)
</dt> <dd>

[**CIM \_ 設定**](cim-setting.md)類別代表一或多個受管理系統元素的設定相關和指令引數。

</dd> <dt>

[**CIM \_ SettingCheck**](cim-settingcheck.md)
</dt> <dd>

[**CIM \_ SettingCheck**](cim-settingcheck.md)類別會指定針對包含值等於指定值的特定專案檢查特定設定檔案所需的資訊。 所有的比較都會假設為不區分大小寫。

</dd> <dt>

[**CIM \_ SettingCoNtext**](cim-settingcontext.md)
</dt> <dd>

[**CIM \_ SettingCoNtext**](cim-settingcontext.md)類別會將設定物件與設定物件建立關聯。

</dd> <dt>

[**CIM \_ 位置**](cim-slot.md)
</dt> <dd>

[**CIM 位置 \_**](cim-slot.md)類別代表要插入封裝的連接器。

</dd> <dt>

[**CIM \_ SlotInSlot**](cim-slotinslot.md)
</dt> <dd>

[**CIM \_ SlotInSlot**](cim-slotinslot.md)關聯性代表特殊介面卡擴充現有插槽結構的能力，以啟用其他不相容的卡片來插入框架或主控面板。

</dd> <dt>

[**CIM \_ SoftwareElement**](cim-softwareelement.md)
</dt> <dd>

[**Cim \_ SoftwareElement**](cim-softwareelement.md)類別會將 [**cim \_ SoftwareFeature**](cim-softwarefeature.md)物件分解至特定平臺的一組個別可管理或可部署的元件中。 軟體專案的平臺是由其基礎硬體架構和作業系統來唯一識別。

</dd> <dt>

[**CIM \_ SoftwareElementActions**](cim-softwareelementactions.md)
</dt> <dd>

[**CIM \_ SoftwareElementActions**](cim-softwareelementactions.md)關聯會識別 software 元素的動作。

</dd> <dt>

[**CIM \_ SoftwareElementChecks**](cim-softwareelementchecks.md)
</dt> <dd>

[**CIM \_ SoftwareElementChecks**](cim-softwareelementchecks.md)關聯類別會將 software 元素與功能可能需要的條件或位置資訊產生關聯。

</dd> <dt>

[**CIM \_ SoftwareElementVersionCheck**](cim-softwareelementversioncheck.md)
</dt> <dd>

[**CIM \_ SoftwareElementVersionCheck**](cim-softwareelementversioncheck.md)類別代表必須存在於環境中的 software 元素類型。

</dd> <dt>

[**CIM \_ SoftwareFeature**](cim-softwarefeature.md)
</dt> <dd>

[**CIM \_ SoftwareFeature**](cim-softwarefeature.md)類別代表產品或應用程式系統的特定功能或功能。

</dd> <dt>

[**CIM \_ SoftwareFeatureSAPImplementation**](cim-softwarefeaturesapimplementation.md)
</dt> <dd>

[**CIM \_ SoftwareFeatureSAPImplementation**](cim-softwarefeaturesapimplementation.md)類別代表服務存取點之間的關聯 (SAP) 以及如何在軟體中執行。

</dd> <dt>

[**CIM \_ SoftwareFeatureServiceImplementation**](cim-softwarefeatureserviceimplementation.md)
</dt> <dd>

[**CIM \_ SoftwareFeatureServiceImplementation**](cim-softwarefeatureserviceimplementation.md)類別代表服務之間的關聯，以及它在軟體中的執行方式。

</dd> <dt>

[**CIM \_ SoftwareFeatureSoftwareElements**](cim-softwarefeaturesoftwareelements.md)
</dt> <dd>

[**CIM \_ SoftwareFeatureSoftwareElements**](cim-softwarefeaturesoftwareelements.md)關聯會識別組成特定軟體功能的軟體元素。

</dd> <dt>

[**CIM \_ SpareGroup**](cim-sparegroup.md)
</dt> <dd>

[**Cim \_ SpareGroup**](cim-sparegroup.md)類別衍生自 [**cim \_ RedundancyGroup**](cim-redundancygroup.md)類別，並指出一或多個匯總的元素可以被用。

</dd> <dt>

[**CIM \_ StatisticalInformation**](cim-statisticalinformation.md)
</dt> <dd>

[**CIM \_ StatisticalInformation**](cim-statisticalinformation.md)類別是適用于一或多個 managed 系統專案之統計資料或計量的任意集合的根類別。

</dd> <dt>

[**CIM \_ 統計資料**](cim-statistics.md)
</dt> <dd>

[**CIM \_ Statistics**](cim-statistics.md)類別代表關聯，可將 managed 系統專案與套用至這些專案的統計群組產生關聯。

</dd> <dt>

[**CIM \_ StorageDefect**](cim-storagedefect.md)
</dt> <dd>

[**CIM \_ StorageDefect**](cim-storagedefect.md)匯總會收集儲存區的儲存錯誤。

</dd> <dt>

[**CIM \_ StorageError**](cim-storageerror.md)
</dt> <dd>

[**CIM \_ StorageError**](cim-storageerror.md)類別代表因為錯誤而對應于使用中的媒體或記憶體空間區塊。 類別的索引鍵是錯誤中位元組的 **StartingAddress** 屬性。

</dd> <dt>

[**CIM \_ StorageExtent**](cim-storageextent.md)
</dt> <dd>

[**CIM \_ StorageExtent**](cim-storageextent.md)類別代表各種媒體的功能和管理，該媒體存在於儲存資料和允許資料抓取。 此父類別可代表 RAID (硬體或軟體) 的各種元件，或實體媒體上的原始邏輯範圍。

</dd> <dt>

[**CIM \_ StorageRedundancyGroup**](cim-storageredundancygroup.md)
</dt> <dd>

[**CIM \_ StorageRedundancyGroup**](cim-storageredundancygroup.md)類別代表大量儲存體相關的重複資訊。

</dd> <dt>

[**CIM \_ SupportAccess**](cim-supportaccess.md)
</dt> <dd>

[**CIM \_ SupportAccess**](cim-supportaccess.md)類別定義了如何取得產品的協助。

</dd> <dt>

[**CIM \_ SwapSpaceCheck**](cim-swapspacecheck.md)
</dt> <dd>

[**CIM \_ SwapSpaceCheck**](cim-swapspacecheck.md)類別會指定系統上必須可用的交換空間量。

</dd> <dt>

[**CIM \_ 系統**](cim-system.md)
</dt> <dd>

[**CIM \_ 系統**](cim-system.md)類別會匯總 managed 系統專案的可列舉集合。 匯總會以整體功能的形式運作。 在系統的任何特定子類別內，都有一個定義完善的 managed 系統專案類別清單，這些類別的實例必須加以匯總。

</dd> <dt>

[**CIM \_ SystemComponent**](cim-systemcomponent.md)
</dt> <dd>

通用訊息模型 (CIM) 關聯類別，可建立系統與其組成之 managed 系統元素之間的關聯性。

</dd> <dt>

[**CIM \_ SystemDevice**](cim-systemdevice.md)
</dt> <dd>

[**CIM \_ SystemDevice**](cim-systemdevice.md)關聯代表明確的關聯性，可讓系統匯總邏輯裝置。

</dd> <dt>

[**CIM \_ SystemResource**](cim-systemresource.md)
</dt> <dd>

[**CIM \_ SystemResource**](cim-systemresource.md)類別代表 BIOS 所管理的實體，或是可供軟體和邏輯裝置使用的作業系統。

</dd> <dt>

[**CIM \_ 流速**](cim-tachometer.md)
</dt> <dd>

[**Cim \_ 轉速計**](cim-tachometer.md)類別存在，可回溯相容于舊版 CIM 架構定義。

</dd> <dt>

[**CIM \_ disable-tapedrive**](cim-tapedrive.md)
</dt> <dd>

[**CIM \_ disable-tapedrive**](cim-tapedrive.md)類別代表系統上的磁帶機。 磁帶機主要是用來區別，因為它們只能依序存取。

</dd> <dt>

[**CIM \_ 溫度感應器**](cim-temperaturesensor.md)
</dt> <dd>

[**Cim \_ 溫度感應器**](cim-temperaturesensor.md)類別存在，可回溯相容于舊版 cim 架構定義。

</dd> <dt>

[**CIM \_ 執行緒**](cim-thread.md)
</dt> <dd>

[**CIM \_ 執行緒**](cim-thread.md)類別代表能夠以平行方式執行進程或工作的單位。 一個處理常式可以有許多執行緒，每個執行緒都是進程的弱式。

</dd> <dt>

[**CIM \_ ToDirectoryAction**](cim-todirectoryaction.md)
</dt> <dd>

[**CIM \_ ToDirectoryAction**](cim-todirectoryaction.md)關聯會識別檔案動作的目標目錄。

</dd> <dt>

[**CIM \_ ToDirectorySpecification**](cim-todirectoryspecification.md)
</dt> <dd>

[**CIM \_ ToDirectorySpecification**](cim-todirectoryspecification.md)關聯會識別檔案動作的目標目錄。

</dd> <dt>

[**CIM \_ UninterruptiblePowerSupply**](cim-uninterruptiblepowersupply.md)
</dt> <dd>

[**CIM \_ UninterruptiblePowerSupply**](cim-uninterruptiblepowersupply.md)類別代表 (UPS) 的不斷電供應系統供應器的功能和管理。

</dd> <dt>

[**CIM \_ UnitaryComputerSystem**](cim-unitarycomputersystem.md)
</dt> <dd>

[**CIM \_ UnitaryComputerSystem**](cim-unitarycomputersystem.md)類別代表桌上型電腦、行動裝置、網路電腦、伺服器或其他類型的單一節點電腦系統。

</dd> <dt>

[**CIM \_ USBController**](cim-usbcontroller.md)
</dt> <dd>

[**CIM \_ USBController**](cim-usbcontroller.md)類別代表 USB 控制器的功能和管理。

</dd> <dt>

[**CIM \_ USBControllerHasHub**](cim-usbcontrollerhashub.md)
</dt> <dd>

[**CIM \_ USBControllerHasHub**](cim-usbcontrollerhashub.md)類別定義了 USB 控制器下游的中樞。

</dd> <dt>

[**CIM \_ USBDevice**](cim-usbdevice.md)
</dt> <dd>

[**CIM \_ USBDevice**](cim-usbdevice.md)類別代表 USB 裝置的管理特性。

</dd> <dt>

[**CIM \_ USBHub**](cim-usbhub.md)
</dt> <dd>

[**CIM \_ USBHub**](cim-usbhub.md)類別代表 USB 集線器的功能和管理。

</dd> <dt>

[**CIM \_ UserDevice**](cim-userdevice.md)
</dt> <dd>

[**Cim \_ UserDevice**](cim-userdevice.md)類別是其他類別（例如 [**CIM \_ 鍵盤**](cim-keyboard.md)或 [**cim \_ DesktopMonitor**](cim-desktopmonitor.md)）下降的父類別。 使用者裝置是邏輯裝置，可讓電腦系統的使用者輸入、查看或聽到資料。

</dd> <dt>

[**CIM \_ VersionCompatibilityCheck**](cim-versioncompatibilitycheck.md)
</dt> <dd>

[**CIM \_ VersionCompatibilityCheck**](cim-versioncompatibilitycheck.md)類別會指定是否允許建立軟體元素的下一個狀態。

</dd> <dt>

[**CIM \_ VideoBIOSElement**](cim-videobioselement.md)
</dt> <dd>

[**CIM \_ VideoBIOSElement**](cim-videobioselement.md)類別代表載入至非暫時性存放裝置的低層級軟體，可用來設定及存取電腦系統的視訊控制器和顯示器。

</dd> <dt>

[**CIM \_ VideoBIOSFeature**](cim-videobiosfeature.md)
</dt> <dd>

[**CIM \_ VideoBIOSFeature**](cim-videobiosfeature.md)類別代表用來設定及存取電腦系統之視訊控制器和顯示器的低層級軟體的功能。

</dd> <dt>

[**CIM \_ VideoBIOSFeatureVideoBIOSElements**](cim-videobiosfeaturevideobioselements.md)
</dt> <dd>

[**CIM \_ VideoBIOSFeatureVideoBIOSElements**](cim-videobiosfeaturevideobioselements.md)類別會將影片 bios 功能與其匯總的影片 bios 專案產生關聯。

</dd> <dt>

[**CIM \_ VideoController**](cim-videocontroller.md)
</dt> <dd>

[**CIM \_ VideoController**](cim-videocontroller.md)類別代表影片控制器的功能和管理。

</dd> <dt>

[**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md)
</dt> <dd>

[**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md)類別代表影片控制器可支援的各種影片模式。

</dd> <dt>

[**CIM \_ VideoSetting**](cim-videosetting.md)
</dt> <dd>

[**Cim \_ VideoSetting**](cim-videosetting.md)類別會將 [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md)設定物件與其套用的控制器產生關聯。

</dd> <dt>

[**CIM \_ VolatileStorage**](cim-volatilestorage.md)
</dt> <dd>

[**CIM \_ VolatileStorage**](cim-volatilestorage.md)類別代表 volatile 儲存體的功能和管理。

</dd> <dt>

[**CIM \_ 電壓感應器**](cim-voltagesensor.md)
</dt> <dd>

[**Cim \_ 電壓感應器**](cim-voltagesensor.md)類別存在，可回溯相容于舊版 cim 架構定義。 在2.2 版中，有 [**cim \_ 感應器**](cim-sensor.md) 和 [**cim \_ NumericSensor**](cim-numericsensor.md) 類別的新增功能，不再需要。

</dd> <dt>

[**CIM \_ VolumeSet**](cim-volumeset.md)
</dt> <dd>

[**CIM \_ VolumeSet**](cim-volumeset.md)類別代表針對讀取和寫入使用者資料的作業環境所呈現的連續邏輯區塊範圍。

</dd> <dt>

[**CIM \_ WORMDrive**](cim-wormdrive.md)
</dt> <dd>

[**CIM \_ WORMDrive**](cim-wormdrive.md)類別代表 WORM 磁片磁碟機（媒體存取裝置的子類型）的功能和管理。

</dd> </dl>

 

 

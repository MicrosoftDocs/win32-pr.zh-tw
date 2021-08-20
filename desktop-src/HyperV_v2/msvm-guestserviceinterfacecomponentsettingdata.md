---
description: 代表來賓服務介面元件的設定狀態。
ms.assetid: 82B58459-9819-4F51-BEE5-AB57E444CF55
title: Msvm_GuestServiceInterfaceComponentSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestServiceInterfaceComponentSettingData
- Msvm_GuestServiceInterfaceComponentSettingData.ElementName
- Msvm_GuestServiceInterfaceComponentSettingData.InstanceID
- Msvm_GuestServiceInterfaceComponentSettingData.ResourceType
- Msvm_GuestServiceInterfaceComponentSettingData.OtherResourceType
- Msvm_GuestServiceInterfaceComponentSettingData.ResourceSubType
- Msvm_GuestServiceInterfaceComponentSettingData.PoolID
- Msvm_GuestServiceInterfaceComponentSettingData.ConsumerVisibility
- Msvm_GuestServiceInterfaceComponentSettingData.HostResource
- Msvm_GuestServiceInterfaceComponentSettingData.AllocationUnits
- Msvm_GuestServiceInterfaceComponentSettingData.VirtualQuantity
- Msvm_GuestServiceInterfaceComponentSettingData.Reservation
- Msvm_GuestServiceInterfaceComponentSettingData.Limit
- Msvm_GuestServiceInterfaceComponentSettingData.Weight
- Msvm_GuestServiceInterfaceComponentSettingData.AutomaticAllocation
- Msvm_GuestServiceInterfaceComponentSettingData.AutomaticDeallocation
- Msvm_GuestServiceInterfaceComponentSettingData.Parent
- Msvm_GuestServiceInterfaceComponentSettingData.Connection
- Msvm_GuestServiceInterfaceComponentSettingData.Address
- Msvm_GuestServiceInterfaceComponentSettingData.MappingBehavior
- Msvm_GuestServiceInterfaceComponentSettingData.EnabledState
- Msvm_GuestServiceInterfaceComponentSettingData.DefaultEnabledStatePolicy
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6e1171e5f303d5b122f0d2202978415206a26e94c15e69f09af73b811c33dcb2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118147804"
---
# <a name="msvm_guestserviceinterfacecomponentsettingdata-class"></a>Msvm \_ GuestServiceInterfaceComponentSettingData 類別

代表來賓服務介面元件的設定狀態。 此類別衍生自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) 類別。

下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GuestServiceInterfaceComponentSettingData : CIM_ResourceAllocationSettingData
{
  string  ElementName;
  string  InstanceID;
  uint16  ResourceType;
  string  OtherResourceType;
  string  ResourceSubType;
  string  PoolID;
  uint16  ConsumerVisibility;
  string  HostResource[];
  string  AllocationUnits;
  uint64  VirtualQuantity;
  uint64  Reservation;
  uint64  Limit;
  uint32  Weight;
  boolean AutomaticAllocation;
  boolean AutomaticDeallocation;
  string  Parent;
  string  Connection[];
  string  Address;
  uint16  MappingBehavior;
  uint16  EnabledState = 3;
  uint16  DefaultEnabledStatePolicy = 2;
};
```

## <a name="members"></a>成員

**Msvm \_ GuestServiceInterfaceComponentSettingData** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ GuestServiceInterfaceComponentSettingData** 類別具有這些屬性。

<dl> <dt>

**位址**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

資源的位址。 例如，乙太網路埠的 MAC 位址。

</dd> <dt>

**AllocationUnits**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

這個屬性會指定保留和限制屬性所使用的配置單位。 例如，當 ResourceType = Processor 時，AllocationUnits 可設定為 MHz。 當 ResourceType = Memory 時，AllocationUnits 可設定為 MB

</dd> <dt>

**AutomaticAllocation**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

這個屬性會指定是否要自動設定資源。 例如，設定為 true 時，當取用的虛擬電腦系統開機時，會配置此資源。 值為 false 表示必須明確配置資源。 例如，此設定可能代表卸載式媒體 (也就是 cdrom 或磁片) 在當時的電源上，媒體不存在。 需要明確操作才能配置資源。

</dd> <dt>

**AutomaticDeallocation**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

這個屬性會指定是否要自動解除配置資源。 例如，設定為 true 時，當取用的虛擬電腦系統電源關閉時，就會解除配置此資源。 當設定為 false 時，資源仍會保持配置，且必須明確解除配置。

</dd> <dt>

**[連接]**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

此資源所連接的目標。 例如，名為網路或交換器埠。

</dd> <dt>

**ConsumerVisibility**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

描述已配置資源的取用者可見度。



| 值                                                                                                                                                                                                                                                                  | 意義                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt>**未知**</dt>的 <dt>0</dt> </dl>                                            | 未知。<br/>                                                                                                                                                                                                                                         |
| <span id="Passed-Through"></span><span id="passed-through"></span><span id="PASSED-THROUGH"></span><dl> <dt>**傳遞至**</dt> <dt>2</dt> </dl>                | 基礎或主機資源會利用並傳遞給取用者（可能是使用資料分割）。 DeviceID 屬性中至少應該有一個專案。<br/>                                                                        |
| <span id="Virtualized"></span><span id="virtualized"></span><span id="VIRTUALIZED"></span><dl> <dt>**虛擬化**</dt> <dt>3</dt> </dl>                            | 資源已虛擬化，而且可能不會直接對應至基礎/主機資源。 某些實現可能會支援虛擬資源的特定指派，在這種情況下，會使用 DeviceID 屬性來公開主機資源 (的) 。<br/> |
| <span id="Not_represented"></span><span id="not_represented"></span><span id="NOT_REPRESENTED"></span><dl> <dt>**未表示**</dt> <dt>4</dt> </dl>            | 資源取用者的內容中不存在資源的標記法。<br/>                                                                                                                                                     |
| <span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> 已 <dt>**保留 DMTF**</dt> <dt></dt> </dl>                   |                                                                                                                                                                                                                                                             |
| <span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span><dl> <dt>**廠商保留**</dt>的 <dt>32767-65535</dt> </dl> |                                                                                                                                                                                                                                                             |



 

</dd> <dt>

**DefaultEnabledStatePolicy**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

預設會啟用和停用來賓通訊服務的狀態。

這是唯讀屬性，但是可以使用 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)類別的 [**ModifyResourceSettings**](cim-virtualsystemmanagementservice-modifyresourcesettings.md)方法來變更。

> [!Note]  
> 已在 Windows 10 中新增。

 

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**已啟用** (2) 


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**停用** (3) 


</dt> <dd></dd> </dl>

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

此 SettingData 實例的顯示名稱。 此外，顯示名稱可以當做搜尋或查詢的索引屬性使用。  (附注：名稱在命名空間中不一定是唯一的。 ) 

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

專案的已啟用和停用狀態。

這是唯讀屬性，但是可以使用 ModifyVirtualSystemResources 方法來變更，其方式是在 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)類別的 Windows 10 或更新版本) 中使用 [](/previous-versions/windows/desktop/virtual/modifyvirtualsystemresources-msvm-virtualsystemmanagementservice)方法 (或 [**ModifyResourceSettings**](cim-virtualsystemmanagementservice-modifyresourcesettings.md) 。

有效值為：

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**已啟用** (2) 


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**停用** (3) 


</dt> <dd></dd> </dl>

</dd> <dt>

**HostResource**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

這個屬性會公開特定指派給主機或基礎資源。 內嵌的實例應只包含索引鍵屬性，並被視為物件路徑。 如果虛擬資源可以針對一些基礎資源進行排程，則此屬性應該保持 **為 Null**。 在這種情況下，DeviceAllocatedFromPool 或 ResourceAllocationFromPool 關聯可以用來判斷可排程此虛擬資源的主機資源集區。 如果使用特定指派，此虛擬資源所使用的所有基礎資源都應列在此陣列中。 陣列通常會包含一個專案，但針對匯總配置（例如多個處理器），可能會指定多個主機資源。

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 **鍵**
</dt> </dl>

在具現化命名空間的範圍內，InstanceID 會以不透明和唯一的方式識別此類別的實例。 若要確保命名空間中的唯一性，InstanceID 的值應使用下列「慣用」演算法來建立： *OrgID*：*LocalID* ，其中 *OrgID* 和 *LocalID* 會以冒號 (： ) ，而且 *OrgID* 必須包含受著作權、商標或其他唯一名稱，而該名稱是由建立或定義 InstanceID 的商務實體所擁有，或是由可辨識的全域授權單位指派給商務實體的註冊識別碼。  (這項需求類似于架構類別名稱的 *SchemaName* \_ *ClassName* 結構。 ) 此外，為了確保唯一性， *OrgID* 不能包含冒號 (： ) 。 使用此演算法時，InstanceID 中出現的第一個冒號必須出現在 *OrgID* 和 *LocalID* 之間。 *LocalID* 由商務實體選擇，不應重複使用，以找出不同的基礎 (真實世界) 元素。 如果未使用上述的「慣用」演算法，則定義實體必須確保產生的 InstanceID 不會在這個實例的命名空間或其他提供者所產生的任何 InstanceIDs 上重複使用。 針對 DMTF 定義的實例，您必須使用「慣用」演算法搭配將 *OrgID* 設定為 CIM。

</dd> <dt>

**限制**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

這個屬性會指定將為此配置授與的上限或最大資源量。 例如，支援記憶體分頁的系統可能支援設定低於 VirtualQuantity 的記憶體配置限制，進而強制進行此配置的分頁。

</dd> <dt>

**MappingBehavior**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定此資源對應至基礎資源的方式。 如果 HostResource 陣列包含任何專案，則此屬性會反映資源對應至這些特定資源的方式。

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) 
</dt> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**不支援** (1) 
</dt> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**專用** (2) 
</dt> <dt>

<span id="Soft_Affinity"></span><span id="soft_affinity"></span><span id="SOFT_AFFINITY"></span>**軟親和性** (3) 
</dt> <dt>

<span id="Hard_Affinity"></span><span id="hard_affinity"></span><span id="HARD_AFFINITY"></span> (4) 的 **硬性親和性**
</dt> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) 
</dt> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**廠商保留** (32767. 65535) 
</dt> </dl>

</dd> <dt>

**OtherResourceType**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

描述資源類型的字串，當定義的值無法使用且 ResourceType 的值為 "Other" 時。

</dd> <dt>

**父系**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

資源的父系。 例如，目前配置的控制器。

</dd> <dt>

**PoolID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

這個屬性會指定資源目前配置來源的 ResourcePool，或在配置發生時要配置資源的 ResourcePool。

</dd> <dt>

**保留容量**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

這個屬性會指定保證可用於此配置的資源數量。 在支援過度使用資源的系統上，此值通常會用於許可控制，以防止系統接受配置，進而避免資源耗盡。

</dd> <dt>

**ResourceSubType**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

字串，描述此資源的執行特定子類型。 例如，這可用來區分相同資源類型的不同模型。

</dd> <dt>

**ResourceType**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

此配置設定所代表的資源類型。

<dl> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) 
</dt> <dt>

<span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**電腦系統** (2) 
</dt> <dt>

<span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**處理器** (3) 
</dt> <dt>

<span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**記憶體** (4) 
</dt> <dt>

<span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**IDE 控制器** (5) 
</dt> <dt>

<span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**平行 SCSI HBA** (6) 
</dt> <dt>

<span id="FC_HBA"></span><span id="fc_hba"></span>**FC HBA** (7) 
</dt> <dt>

<span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**ISCSI HBA** (8) 
</dt> <dt>

<span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9) 
</dt> <dt>

<span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**乙太網路介面卡** (10) 
</dt> <dt>

<span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**其他網路介面卡** (11) 
</dt> <dt>

<span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**I/o 插槽** (12) 
</dt> <dt>

<span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span> (13) 的 **I/o 裝置**
</dt> <dt>

<span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>**磁片磁碟機** (14) 
</dt> <dt>

<span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**CD 光碟機** (15) 
</dt> <dt>

<span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**DVD 光碟機** (16) 
</dt> <dt>

<span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**序列埠** (17) 
</dt> <dt>

<span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**平行埠** (18) 
</dt> <dt>

<span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**USB 控制器** (19) 
</dt> <dt>

<span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**圖形控制器** (20) 
</dt> <dt>

<span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**儲存體範圍** (21) 
</dt> <dt>

<span id="Disk"></span><span id="disk"></span><span id="DISK"></span>**磁片** (22) 
</dt> <dt>

<span id="Tape"></span><span id="tape"></span><span id="TAPE"></span>**磁帶** (23) 
</dt> <dt>

<span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**其他存放裝置** (24) 
</dt> <dt>

<span id="Firewire_Controller"></span><span id="firewire_controller"></span><span id="FIREWIRE_CONTROLLER"></span>**Firewire 控制器** (25) 
</dt> <dt>

<span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**可分割 Unit** (26) 
</dt> <dt>

<span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**基底可分割單位** (27) 
</dt> <dt>

<span id="Power_Supply"></span><span id="power_supply"></span><span id="POWER_SUPPLY"></span>**電源供應** 器 (28) 
</dt> <dt>

<span id="Cooling_Device"></span><span id="cooling_device"></span><span id="COOLING_DEVICE"></span>**冷卻裝置** (29) 
</dt> <dt>

<span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) 
</dt> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**廠商保留** (32767. 65535) 
</dt> </dl>

</dd> <dt>

**VirtualQuantity**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

這個屬性會指定向取用者呈現的資源數量。 例如，當 ResourceType = Processor 時，這個屬性會反映出給虛擬電腦系統的離散處理器數目。 當 ResourceType = Memory 時，這個屬性可能會反映回報給虛擬電腦系統的 MB 數。

</dd> <dt>

**Weight**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

這個屬性會指定此配置相對於相同 ResourcePool 中其他配置的相對優先權。 這個屬性沒有測量單位，而且只與其他爭用相同主機資源的配置有關。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8.1 \[僅限桌面應用程式\]<br/>                                                            |
| 最低支援的伺服器<br/> | Windows Server 2012\[僅限 R2 desktop 應用程式\]<br/>                                                 |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md)
</dt> <dt>

[**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> </dl>

 


---
description: 代表資源集區，這是主機系統提供來配置和指派資源的邏輯實體。
ms.assetid: c8e0b701-1814-4409-a073-017f8fea841a
title: CIM_ResourcePool 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePool
- CIM_ResourcePool.InstanceID
- CIM_ResourcePool.PoolID
- CIM_ResourcePool.Primordial
- CIM_ResourcePool.Capacity
- CIM_ResourcePool.Reserved
- CIM_ResourcePool.ResourceType
- CIM_ResourcePool.OtherResourceType
- CIM_ResourcePool.ResourceSubType
- CIM_ResourcePool.AllocationUnits
- CIM_ResourcePool.ConsumedResourceUnits
- CIM_ResourcePool.CurrentlyConsumedResource
- CIM_ResourcePool.MaxConsumableResource
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d87a78d5a8ea43cc8a1a59bbabf5b8091948d153420dbdf91ba7e14fc1616b7e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119980958"
---
# <a name="cim_resourcepool-class"></a>CIM \_ ResourcePool 類別

代表資源集區，這是主機系統提供來配置和指派資源的邏輯實體。

## <a name="syntax"></a>語法

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Resource"), AMENDMENT]
class CIM_ResourcePool : CIM_LogicalElement
{
  string  InstanceID;
  string  PoolID;
  boolean Primordial = FALSE;
  uint64  Capacity;
  uint64  Reserved;
  uint16  ResourceType;
  string  OtherResourceType;
  string  ResourceSubType;
  string  AllocationUnits;
  string  ConsumedResourceUnits = "count";
  uint64  CurrentlyConsumedResource;
  uint64  MaxConsumableResource;
};
```

## <a name="members"></a>成員

**CIM \_ ResourcePool** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**CIM \_ ResourcePool** 類別具有這些屬性。

<dl> <dt>

**AllocationUnits**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **IsPUnit**
</dt> </dl>

**保留** 和 **限制** 屬性所使用的配置單位。 例如，當 **ResourceType** 設定為 "Processor" 時， **AllocationUnits** 可以設定為 "赫茲 \* 10 ^ 6" 或 "percent"。 這個屬性的值應該是 *DSP0004 2.4* 或更新版本的附錄 C. 1 的程式設計單位辨識符號合法值。

</dd> <dt>

**容量**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

資源集區可支援的最大保留量。 **AllocationUnits** 屬性會指定單位類型。

</dd> <dt>

**ConsumedResourceUnits**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ ResourcePool**.**MaxConsumableResource**"，"**CIM \_ ResourcePool**.**CurrentlyConsumedResource**") ， **IsPUnit**
</dt> </dl>

**MaxConsumable** 的單位和已 **使用** 的屬性。

</dd> <dt>

**CurrentlyConsumedResource**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ ResourcePool**.**ConsumedResourceUnits**") 
</dt> </dl>

資源集區目前呈現給資源取用者的資源數量。 這個屬性與 **保留** 的屬性不同，因為它會描述資源的取用者觀點，而 **保留** 的屬性會描述資源的產生者觀點。

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "InstanceID" ) 
</dt> </dl>

在包含的命名空間範圍內唯一識別此類別的實例。

> [!IMPORTANT]
>
> 為了確保命名空間中的唯一性， **InstanceID** 屬性的值應該以下列模式來建立： *OrgID*：*LocalID*
>
> -   *OrgID* 必須包含受著作權、商標或其他唯一的名稱，該名稱是由定義 **InstanceID** 屬性的商業實體所擁有，或是由可辨識的全域授權單位指派的註冊識別碼。
> -   *OrgID* 不能包含冒號。 **InstanceID** 中的第一個冒號必須介於 *OrgID* 和 *LocalID* 之間。
> -   *LocalID* 是由商務實體所選擇，不應重新使用以識別不同的基礎現實世界元素。
> -   如果未使用上述模式，則定義實體必須確保產生的 **instanceid** 值不會重複用於這個提供者所產生之任何 **instanceid** 屬性或這個命名空間的其他提供者。
> -   針對已定義的 DMTF 實例，必須搭配 *OrgID* 設定為 "CIM" 的模式使用。

 

</dd> <dt>

**MaxConsumableResource**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ ResourcePool**.**ConsumedResourceUnits**") 
</dt> </dl>

資源集區可呈現給資源取用者的可耗用資源數量上限。 這個屬性與 [ **容量** ] 屬性不同，因為它會描述資源的取用者觀點，而 [ **容量** ] 屬性則會描述資源的生產者視圖。

</dd> <dt>

**OtherResourceType**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ ResourcePool**.**ResourceType**") 
</dt> </dl>

**ResourceType** 屬性設定為 "0" (其他) 的資源類型。

</dd> <dt>

**PoolID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md).**PoolId**") 
</dt> </dl>

集區不透明的識別碼。 這個屬性是用來在儲存和還原設定資料到基礎持續性儲存體時提供相互關聯。

</dd> <dt>

**原始**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

如果資源集區是原始的，**則為 true** 。 如果資源集區是實體資源集區，則 **為 false** 。 原始資源集區是資源的取用者未建立或刪除的資源集區。 資源配置服務可以更新實體資源集區。

</dd> <dt>

**已保留**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

從這個集區到所有使用中配置的目前保留數目。 在階層式設定中，這代表所有目前下階保留專案的總和。 **AllocationUnits** 屬性會指定單位類型。

</dd> <dt>

**ResourceSubType**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ ResourcePool**.**ResourceType**") 
</dt> </dl>

資源集區的執行特定子類型。 例如，這可用來區分相同資源類型的不同模型。

</dd> <dt>

**ResourceType**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ ResourcePool**.**OtherResourceType**"，"**CIM \_ ResourcePool**.**ResourceSubType**") 
</dt> </dl>

資源集區所配置的資源類型。

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**其他** (1) 


</dt> <dd></dd> <dt>

<span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>

**電腦系統** (2) 


</dt> <dd></dd> <dt>

<span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>

**處理器** (3) 


</dt> <dd></dd> <dt>

<span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>

**記憶體** (4) 


</dt> <dd></dd> <dt>

<span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>

**IDE 控制器** (5) 


</dt> <dd></dd> <dt>

<span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>

**平行 SCSI HBA** (6) 


</dt> <dd></dd> <dt>

<span id="FC_HBA"></span><span id="fc_hba"></span>

**FC HBA** (7) 


</dt> <dd></dd> <dt>

<span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>

**ISCSI HBA** (8) 


</dt> <dd></dd> <dt>

<span id="IB_HCA"></span><span id="ib_hca"></span>

**IB HCA** (9) 


</dt> <dd></dd> <dt>

<span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>

**乙太網路介面卡** (10) 


</dt> <dd></dd> <dt>

<span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>

**其他網路介面卡** (11) 


</dt> <dd></dd> <dt>

<span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>

**I/o 插槽** (12) 


</dt> <dd></dd> <dt>

<span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>

 (13) 的 **I/o 裝置**


</dt> <dd></dd> <dt>

<span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>

**磁片磁碟機** (14) 


</dt> <dd></dd> <dt>

<span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>

**CD 光碟機** (15) 


</dt> <dd></dd> <dt>

<span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>

**DVD 光碟機** (16) 


</dt> <dd></dd> <dt>

<span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>

**磁片磁碟機** (17) 


</dt> <dd></dd> <dt>

<span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>

**磁帶機** (18) 


</dt> <dd></dd> <dt>

<span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>

**儲存體範圍** (19) 


</dt> <dd></dd> <dt>

<span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>

**其他存放裝置** (20) 


</dt> <dd></dd> <dt>

<span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>

**序列埠** (21) 


</dt> <dd></dd> <dt>

<span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>

**平行埠** (22) 


</dt> <dd></dd> <dt>

<span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>

**USB 控制器** (23) 


</dt> <dd></dd> <dt>

<span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>

**圖形控制器** (24) 


</dt> <dd></dd> <dt>

<span id="IEEE_1394_Controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>

**IEEE 1394 控制器** (25) 


</dt> <dd></dd> <dt>

<span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>

**可分割 Unit** (26) 


</dt> <dd></dd> <dt>

<span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>

**基底可分割單位** (27) 


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

**Power** (28) 


</dt> <dd></dd> <dt>

<span id="Cooling_Capacity"></span><span id="cooling_capacity"></span><span id="COOLING_CAPACITY"></span>

**冷卻容量** (29) 


</dt> <dd></dd> <dt>

<span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>

**乙太網路交換器埠** (30) 


</dt> <dd></dd> <dt>

<span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>

**邏輯磁片** (31) 


</dt> <dd></dd> <dt>

<span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>

**儲存體 Volume** (32) 


</dt> <dd></dd> <dt>

<span id="Ethernet_Connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>

**Ethernet 連接** (33) 


</dt> <dd></dd> <dt>

<span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF 保留** ( .。。) 


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**廠商保留** (0x8000。0xFFFF) 


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8<br/>                                                                                    |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                                          |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ LogicalElement**](cim-logicalelement.md)
</dt> </dl>

 


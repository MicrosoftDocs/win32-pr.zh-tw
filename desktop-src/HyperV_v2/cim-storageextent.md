---
description: 描述儲存資料和允許抓取資料的媒體功能和管理。 此超級類別可用來代表軟體和硬體 RAID 元件，或實體媒體的原始邏輯範圍。
ms.assetid: 29d105fb-8c34-4824-8679-883aef02a0c9
title: 'CIM_StorageExtent 類別 (Hyper-v 管理) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_StorageExtent
- CIM_StorageExtent.DataOrganization
- CIM_StorageExtent.Purpose
- CIM_StorageExtent.Access
- CIM_StorageExtent.ErrorMethodology
- CIM_StorageExtent.BlockSize
- CIM_StorageExtent.NumberOfBlocks
- CIM_StorageExtent.ConsumableBlocks
- CIM_StorageExtent.IsBasedOnUnderlyingRedundancy
- CIM_StorageExtent.SequentialAccess
- CIM_StorageExtent.ExtentStatus
- CIM_StorageExtent.NoSinglePointOfFailure
- CIM_StorageExtent.DataRedundancy
- CIM_StorageExtent.PackageRedundancy
- CIM_StorageExtent.DeltaReservation
- CIM_StorageExtent.Primordial
- CIM_StorageExtent.Name
- CIM_StorageExtent.NameFormat
- CIM_StorageExtent.NameNamespace
- CIM_StorageExtent.OtherNameNamespace
- CIM_StorageExtent.OtherNameFormat
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2ce3126cf208032e4d43e9ce1866e1cd0ab42c17930684c98d4ad351de88713b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118647366"
---
# <a name="cim_storageextent-class-hyper-v-management"></a>CIM_StorageExtent 類別 (Hyper-v 管理) 

描述儲存資料和允許抓取資料的媒體功能和管理。 此超級類別可用來代表軟體和硬體 RAID 元件，或實體媒體的原始邏輯範圍。

## <a name="syntax"></a>語法

``` syntax
[Abstract, Version("2.13.0"), UMLPackagePath("CIM::Core::StorageExtent"), AMENDMENT]
class CIM_StorageExtent : CIM_LogicalDevice
{
  uint16  DataOrganization;
  string  Purpose;
  uint16  Access;
  string  ErrorMethodology;
  uint64  BlockSize;
  uint64  NumberOfBlocks;
  uint64  ConsumableBlocks;
  boolean IsBasedOnUnderlyingRedundancy;
  boolean SequentialAccess;
  uint16  ExtentStatus[];
  boolean NoSinglePointOfFailure;
  uint16  DataRedundancy;
  uint16  PackageRedundancy;
  uint8   DeltaReservation;
  boolean Primordial = FALSE;
  string  Name;
  uint16  NameFormat;
  uint16  NameNamespace;
  string  OtherNameNamespace;
  string  OtherNameFormat;
};
```

## <a name="members"></a>成員

**CIM \_ StorageExtent** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**CIM \_ StorageExtent** 類別具有這些屬性。

<dl> <dt>

**存取**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

媒體的讀取/寫入支援描述。

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 (0) 


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

**可讀取** 的 (1) 


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

可 **寫入** (2) 


</dt> <dd></dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

支援 (3) 的 **讀取/寫入**


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

**撰寫一次** (4) 


</dt> <dd></dd> </dl>

</dd> <dt>

**BlockSize**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：[**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Bytes" ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 主機儲存體 \| 001.4 "，" MIB。IETF \| 主機-RESOURCES-hrStorageAllocationUnits "，" MIF。DMTF \| 儲存體裝置 \| 001.5」 ) 
</dt> </dl>

形成儲存範圍之區塊的大小（以位元組為單位）。 如果使用變數區塊大小，則此屬性應指定最大區塊大小。 如果區塊大小未知或區塊概念無效 (例如，對於 **cim \_ AggregateExtent**、 [**cim \_ 記憶體**](cim-memory.md) 或 [**cim \_ LogicalDisk**](cim-logicaldisk.md)) ，則此屬性應該設為 "1" (未知) 。

</dd> <dt>

**ConsumableBlocks**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

當您使用 [**cim \_ BasedOn**](cim-basedon.md)類別關聯將 **cim \_ StorageExtent** 分層時，可使用的區塊數目上限。 這個屬性只有在 **CIM \_ BasedOn** 物件的 [ **Antecedent** ] 屬性中參考儲存範圍時才有意義。

</dd> <dt>

**DataOrganization**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

媒體所使用的資料組織類型。

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**其他** (0) 


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 (1) 


</dt> <dd></dd> <dt>

<span id="Fixed_Block"></span><span id="fixed_block"></span><span id="FIXED_BLOCK"></span>

**固定區塊** (2) 


</dt> <dd></dd> <dt>

<span id="Variable_Block"></span><span id="variable_block"></span><span id="VARIABLE_BLOCK"></span>

**變數區塊** (3) 


</dt> <dd></dd> <dt>

<span id="Count_Key_Data"></span><span id="count_key_data"></span><span id="COUNT_KEY_DATA"></span>

**計算索引鍵資料** (4) 


</dt> <dd></dd> </dl>

</dd> <dt>

**DataRedundancy**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ StorageSetting**](/previous-versions/windows/desktop/iscsitarg/cim-storagesetting).**DataRedundancyGoal**"，"**CIM \_ StorageSetting**.**DataRedundancyMax**"，"**CIM \_ StorageSetting**.**DataRedundancyMin**") 
</dt> </dl>

目前維護之資料的完整複本數目。

</dd> <dt>

**DeltaReservation**
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "百分比" ) 、 [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (1) 、 [**Int32.maxvalue (100**](/windows/desktop/WmiSdk/standard-qualifiers)) 、 [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ StorageSetting**](/previous-versions/windows/desktop/iscsitarg/cim-storagesetting)。**DeltaReservationGoal**"，"**CIM \_ StorageSetting**.**DeltaReservationMax**"，"**CIM \_ StorageSetting**.**DeltaReservationMin**") 
</dt> </dl>

Delta 保留的目前值。 這是一個百分比，可指定要在複本中保留以進行快取變更的空間量。

</dd> <dt>

**ErrorMethodology**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

儲存範圍所支援的錯誤偵測類型和修正。

</dd> <dt>

**ExtentStatus**
</dt> <dd> <dl> <dt>

資料類型： **uint16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

其他狀態資訊。

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**其他** (0) 


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 (1) 


</dt> <dd></dd> <dt>

<span id="None_Not_Applicable"></span><span id="none_not_applicable"></span><span id="NONE_NOT_APPLICABLE"></span>

**無/不適用** (2) 


</dt> <dd></dd> <dt>

<span id="Broken"></span><span id="broken"></span><span id="BROKEN"></span>

 (3) **中斷**


</dt> <dd></dd> <dt>

<span id="Data_Lost"></span><span id="data_lost"></span><span id="DATA_LOST"></span>

**資料遺失** (4) 


</dt> <dd></dd> <dt>

<span id="Dynamic_Reconfig"></span><span id="dynamic_reconfig"></span><span id="DYNAMIC_RECONFIG"></span>

**Dynamic 重新設定** (5) 


</dt> <dd></dd> <dt>

<span id="Exposed"></span><span id="exposed"></span><span id="EXPOSED"></span>

**公開** (6) 


</dt> <dd></dd> <dt>

<span id="Fractionally_Exposed"></span><span id="fractionally_exposed"></span><span id="FRACTIONALLY_EXPOSED"></span>

**Fractionally 公開** (7) 


</dt> <dd></dd> <dt>

<span id="Partially_Exposed"></span><span id="partially_exposed"></span><span id="PARTIALLY_EXPOSED"></span>

**部分公開** (8) 


</dt> <dd></dd> <dt>

<span id="Protection_Disabled"></span><span id="protection_disabled"></span><span id="PROTECTION_DISABLED"></span>

 (9) **停用保護**


</dt> <dd></dd> <dt>

<span id="Readying"></span><span id="readying"></span><span id="READYING"></span>

準備 **就緒** (10) 


</dt> <dd></dd> <dt>

<span id="Rebuild"></span><span id="rebuild"></span><span id="REBUILD"></span>

**重建** (11) 


</dt> <dd></dd> <dt>

<span id="Recalculate"></span><span id="recalculate"></span><span id="RECALCULATE"></span>

**重新計算** (12) 


</dt> <dd></dd> <dt>

<span id="Spare_in_Use"></span><span id="spare_in_use"></span><span id="SPARE_IN_USE"></span>

**使用中的備用** (13) 


</dt> <dd></dd> <dt>

<span id="Verify_In_Progress"></span><span id="verify_in_progress"></span><span id="VERIFY_IN_PROGRESS"></span>

**確認進行中** (14) 


</dt> <dd></dd> <dt>

<span id="In-Band_Access_Granted"></span><span id="in-band_access_granted"></span><span id="IN-BAND_ACCESS_GRANTED"></span>

**授與 (15) 的頻外存取**


</dt> <dd></dd> <dt>

<span id="Imported"></span><span id="imported"></span><span id="IMPORTED"></span>

匯 **入** (16) 


</dt> <dd></dd> <dt>

<span id="Exported"></span><span id="exported"></span><span id="EXPORTED"></span>

**匯出** (17) 


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF 保留** (18. 32767) 


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**廠商保留** (32768. 65535) 


</dt> <dd></dd> </dl>

</dd> <dt>

**IsBasedOnUnderlyingRedundancy**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

如果基礎儲存範圍是 [**CIM \_ StorageRedundancyGroup**](/windows/desktop/CIMWin32Prov/cim-storageredundancygroup)的成員，則 **為 true** ，否則為 **false**。

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "SPC。INCITS-T10 \| VPD 83、Association 0 \| 識別碼 ") 、 [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ StorageExtent**。**NameFormat**"，"**CIM \_ StorageExtent**.**NameNamespace**") 
</dt> </dl>

儲存區的唯一識別碼。 **NameFormat** 屬性會指定要在 **Name** 屬性中使用的命名格式。

</dd> <dt>

**NameFormat**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ StorageExtent**.**Name**"，"**CIM \_ StorageExtent**。**NameNamespace**"，"**CIM \_ StorageExtent**.**OtherNameFormat**") 
</dt> </dl>

**Name** 屬性的命名格式。

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 (0) 


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**其他** (1) 


</dt> <dd></dd> <dt>

<span id="VPD83NAA6"></span><span id="vpd83naa6"></span>

**VPD83NAA6** (2) 


</dt> <dd></dd> <dt>

<span id="VPD83NAA5"></span><span id="vpd83naa5"></span>

**VPD83NAA5** (3) 


</dt> <dd></dd> <dt>

<span id="VPD83Type2"></span><span id="vpd83type2"></span><span id="VPD83TYPE2"></span>

**VPD83Type2** (4) 


</dt> <dd></dd> <dt>

<span id="VPD83Type1"></span><span id="vpd83type1"></span><span id="VPD83TYPE1"></span>

**VPD83Type1** (5) 


</dt> <dd></dd> <dt>

<span id="VPD83Type0"></span><span id="vpd83type0"></span><span id="VPD83TYPE0"></span>

**VPD83Type0** (6) 


</dt> <dd></dd> <dt>

<span id="SNVM"></span><span id="snvm"></span>

**SNVM** (7) 


</dt> <dd></dd> <dt>

<span id="NodeWWN"></span><span id="nodewwn"></span><span id="NODEWWN"></span>

**NodeWWN** (8) 


</dt> <dd></dd> <dt>

<span id="NAA"></span><span id="naa"></span>

**NAA** (9) 


</dt> <dd></dd> <dt>

<span id="EUI64"></span><span id="eui64"></span>

**EUI64** (10) 


</dt> <dd></dd> <dt>

<span id="T10VID"></span><span id="t10vid"></span>

**T10VID** (11) 


</dt> <dd></dd> <dt>

<span id="OS_Device_Name"></span><span id="os_device_name"></span><span id="OS_DEVICE_NAME"></span>

**OS 裝置名稱** (12) 


</dt> <dd></dd> </dl>

</dd> <dt>

**NameNamespace**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "SPC。INCITS-T10 \| VPD 83、Association 0 \| 識別碼 ") 、 [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ StorageExtent**。**Name**"，"**CIM \_ StorageExtent**。**OtherNameNamespace**"，"**CIM \_ StorageExtent**.**NameFormat**") 
</dt> </dl>

Name 屬性的命名空間。

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 (0) 


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**其他** (1) 


</dt> <dd></dd> <dt>

<span id="VPD83Type3"></span><span id="vpd83type3"></span><span id="VPD83TYPE3"></span>

**VPD83Type3** (2) 


</dt> <dd></dd> <dt>

<span id="VPD83Type2"></span><span id="vpd83type2"></span><span id="VPD83TYPE2"></span>

**VPD83Type2** (3) 


</dt> <dd></dd> <dt>

<span id="VPD83Type1"></span><span id="vpd83type1"></span><span id="VPD83TYPE1"></span>

**VPD83Type1** (4) 


</dt> <dd></dd> <dt>

<span id="VPD80"></span><span id="vpd80"></span>

**VPD80** (5) 


</dt> <dd></dd> <dt>

<span id="NodeWWN"></span><span id="nodewwn"></span><span id="NODEWWN"></span>

**NodeWWN** (6) 


</dt> <dd></dd> <dt>

<span id="SNVM"></span><span id="snvm"></span>

**SNVM** (7) 


</dt> <dd></dd> <dt>

<span id="OS_Device_Namespace"></span><span id="os_device_namespace"></span><span id="OS_DEVICE_NAMESPACE"></span>

**OS 裝置命名空間** (8) 


</dt> <dd></dd> </dl>

</dd> <dt>

**NoSinglePointOfFailure**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ StorageSetting**](/previous-versions/windows/desktop/iscsitarg/cim-storagesetting).**NoSinglePointOfFailure**") 
</dt> </dl>

如果沒有任何單一失敗點，**則為 true** ;否則 **為 false**。

</dd> <dt>

**NumberOfBlocks**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 主機儲存體 \| 001.5 "，" MIB。IETF \| 主機-RESOURCES-hrStorageSize ") 
</dt> </dl>

形成儲存區的邏輯連續區塊總數。 儲存區的總大小是藉由 **NumberOfBlocks** 來乘以 **區塊** 來計算。 如果 **區塊** 值為 "1"，則此屬性為儲存區的總大小。

</dd> <dt>

**OtherNameFormat**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ StorageExtent**.**NameFormat**") 
</dt> </dl>

當 **NameFormat** 屬性設定為 "1" (其他) 時， **Name** 屬性的格式。

</dd> <dt>

**OtherNameNamespace**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ StorageExtent**.**NameNamespace**") 
</dt> </dl>

當 **NameNamespace** 屬性設定為 "1" (其他) 時， **Name** 屬性的命名空間描述。

</dd> <dt>

**PackageRedundancy**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ StorageSetting**](/previous-versions/windows/desktop/iscsitarg/cim-storagesetting).**PackageRedundancyGoal**"，"**CIM \_ StorageSetting**.**PackageRedundancyMax**"，"**CIM \_ StorageSetting**.**PackageRedundancyMin**") 
</dt> </dl>

在不遺失資料的情況下，可能失敗的目前實體封裝數目。 例如，在存放裝置網域中，這可能是磁片主軸的數目。

</dd> <dt>

**原始**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

如果儲存區是原始的，則為 **true** ;否則 **為 false**。

</dd> <dt>

**目的**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIB。IETF \| 主機-RESOURCES-hrStorageDescr ") 
</dt> </dl>

媒體使用方式的描述。

</dd> <dt>

**SequentialAccess**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

如果 [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)物件以順序存取儲存體，則 **為 true** ，否則為 **false**。

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

[**CIM \_ LogicalDevice**](cim-logicaldevice.md)
</dt> </dl>

 


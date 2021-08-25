---
description: 代表虛擬儲存體配置的設定。
ms.assetid: 128fd3e9-8759-4b2f-a881-d34e89c539ac
title: CIM_StorageAllocationSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_StorageAllocationSettingData
- CIM_StorageAllocationSettingData.VirtualResourceBlockSize
- CIM_StorageAllocationSettingData.VirtualQuantity
- CIM_StorageAllocationSettingData.VirtualQuantityUnits
- CIM_StorageAllocationSettingData.Access
- CIM_StorageAllocationSettingData.HostResourceBlockSize
- CIM_StorageAllocationSettingData.Reservation
- CIM_StorageAllocationSettingData.Limit
- CIM_StorageAllocationSettingData.HostExtentStartingAddress
- CIM_StorageAllocationSettingData.HostExtentName
- CIM_StorageAllocationSettingData.HostExtentNameFormat
- CIM_StorageAllocationSettingData.OtherHostExtentNameFormat
- CIM_StorageAllocationSettingData.HostExtentNameNamespace
- CIM_StorageAllocationSettingData.OtherHostExtentNameNamespace
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: fe380b03daced6ca98a44c189c52b5842862aa2e033bf66a04f8dd1466968449
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119899668"
---
# <a name="cim_storageallocationsettingdata-class"></a>CIM \_ StorageAllocationSettingData 類別

代表虛擬儲存體配置的設定。

## <a name="syntax"></a>語法

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Resource"), AMENDMENT]
class CIM_StorageAllocationSettingData : CIM_ResourceAllocationSettingData
{
  uint64 VirtualResourceBlockSize;
  uint64 VirtualQuantity;
  string VirtualQuantityUnits = "count(fixed size block)";
  uint16 Access;
  uint64 HostResourceBlockSize;
  uint64 Reservation;
  uint64 Limit;
  uint64 HostExtentStartingAddress;
  string HostExtentName;
  uint16 HostExtentNameFormat;
  string OtherHostExtentNameFormat;
  uint16 HostExtentNameNamespace;
  string OtherHostExtentNameNamespace;
};
```

## <a name="members"></a>成員

**CIM \_ StorageAllocationSettingData** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**CIM \_ StorageAllocationSettingData** 類別具有這些屬性。

<dl> <dt>

**存取**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ( "[**CIM \_ StorageExtent**](cim-storageextent.md).**存取**") 
</dt> </dl>

儲存體配置的讀取/寫入支援。

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

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF 保留** ( .。。) 


</dt> <dd></dd> </dl>

</dd> <dt>

**HostExtentName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ( "**CIM \_ StorageAllocationSettingData**.**HostExtentNameFormat**"，"**CIM \_ StorageAllocationSettingData**.**HostExtentNameNamespace**"，"[**CIM \_ StorageExtent**](cim-storageextent.md).**名稱**") 
</dt> </dl>

主機儲存區的唯一識別碼。

</dd> <dt>

**HostExtentNameFormat**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ( "**CIM \_ StorageAllocationSettingData**.**HostExtentName**"，"**CIM \_ StorageAllocationSettingData**.**OtherHostExtentNameFormat**"，"[**CIM \_ StorageExtent**](cim-storageextent.md).**NameFormat**") 
</dt> </dl>

**HostExtentName** 屬性值的格式。

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) 


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) 


</dt> <dd></dd> <dt>

<span id="SNVM"></span><span id="snvm"></span>

<span id="SNVM"></span><span id="snvm"></span>**SNVM** (7) 


</dt> <dd>

序號/廠商/模型 (SNVM) SNVM 是代表廠商名稱、廠商命名空間內的產品名稱，以及模型命名空間內序號的3個字串。 字串以 ' + ' 分隔。 可能包含空格，而且很重要。 序號是以十六進位大寫表示之序號的文字標記法。 這代表來自 SCSI 查詢資料的廠商和型號識別碼;廠商欄位必須是8個字元寬，而 product 欄位必須是16個字元寬。 例如

' ACME \_ \_ \_ \_ + SUPER DISK \_ \_ \_ \_ \_ \_ + 124437458 ' (\_ 是空白字元) 

</dd> <dt>

<span id="NAA"></span><span id="naa"></span>

<span id="NAA"></span><span id="naa"></span>**NAA** (9) 


</dt> <dd>

9 = NAA 為一般格式。 請參閱

https://standards.ieee.org/regauth/oui/tutorials/fibrecomp\_id.html. 格式化為16或32未分隔大寫十六進位字元 (每個二進位位元組) 2。

例如 ' 21000020372D3C73 '

</dd> <dt>

<span id="EUI64"></span><span id="eui64"></span>

<span id="EUI64"></span><span id="eui64"></span>**EUI64** (10) 


</dt> <dd>

EUI 作為一般格式 (EUI64) 參閱

https://standards.ieee.org/content/dam/ieee-standards/standards/web/documents/tutorials/eui.pdf.

</dd> <dt>

<span id="T10VID"></span><span id="t10vid"></span>

<span id="T10VID"></span><span id="t10vid"></span>**T10VID** (11) 


</dt> <dd>

T10 廠商識別碼格式，如 SCSI 查詢 VPD 頁面83、識別碼類型1所傳回。 請參閱 T10 SPC-3 規格。 這是 T10 登錄中的8位元組 ASCII 廠商識別碼，後面接著廠商特定的 ASCII 識別碼;允許使用空格。 若為非 SCSI 磁片區，' SNVM ' 可能是最適當的選擇。

</dd> <dt>

<span id="OS_Device_Name"></span><span id="os_device_name"></span><span id="OS_DEVICE_NAME"></span>

<span id="OS_Device_Name"></span><span id="os_device_name"></span><span id="OS_DEVICE_NAME"></span>**OS 裝置名稱** (12) 


</dt> <dd>

LogicalDisks) 的 OS 裝置名稱 (。 如需詳細資料，請參閱 LogicalDisk 名稱描述。

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) 


</dt> <dd></dd> </dl>

</dd> <dt>

**HostExtentNameNamespace**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ( "**CIM \_ StorageAllocationSettingData**.**HostExtentName**"，"**CIM \_ StorageAllocationSettingData**.**OtherHostExtentNameNamespace**"，"**CIM \_ StorageAllocationSettingData**.**HostExtentNameFormat**"，"[**CIM \_ StorageExtent**](cim-storageextent.md).**命名空間**") 
</dt> </dl>

**Name** 屬性的命名格式。

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


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF 保留** ( .。。) 


</dt> <dd></dd> </dl>

</dd> <dt>

**HostExtentStartingAddress**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ( "**CIM \_ StorageAllocationSettingData**.**HostResourceBlockSize**"，"[**CIM \_ BasedOn**](cim-basedon.md).**StartingAddress**") 
</dt> </dl>

主機儲存區的起始位址。 Null val; ue 表示虛擬儲存區和主機儲存區之間沒有直接對應。

</dd> <dt>

**HostResourceBlockSize**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ( "[**CIM \_ StorageExtent**](cim-storageextent.md).**區塊**") ， **PUnit** (" byte ") 
</dt> </dl>

在主機上配置給儲存體配置之區塊的大小（以位元組為單位）。 如果區塊大小為變數，則應該指定最大區塊大小（以位元組為單位）。 如果區塊大小未知或區塊概念未套用，則應該使用值 "1" (未知的) 。

</dd> <dt>

**限制**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](../wmisdk/standard-qualifiers.md) ( "Limit" ) ， [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ( "**CIM \_ StorageAllocationSettingData**。**HostResourceBlockSize**") 
</dt> </dl>

針對主機上的儲存體資源配置，將授與的區塊數目上限。 區塊大小是由 **HostResourceBlockSize** 屬性所指定。

</dd> <dt>

**OtherHostExtentNameFormat**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ( "**CIM \_ StorageAllocationSettingData**.**HostExtentNameFormat**") 
</dt> </dl>

如果屬性設定為 "1" (其他) ，則為 **HostExtentName** 屬性的格式。

</dd> <dt>

**OtherHostExtentNameNamespace**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ( "**CIM \_ StorageAllocationSettingData**.**HostExtentNameNamespace**") 
</dt> </dl>

字串，如果 **HostExtentNameNamespace** 屬性的值為 "1" (其他) ，則描述 **HostExtentName** 屬性的命名空間。

</dd> <dt>

**保留容量**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](../wmisdk/standard-qualifiers.md) ( "保留" ) ， [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ( "**CIM \_ StorageAllocationSettingData**。**HostResourceBlockSize**") 
</dt> </dl>

保證可供主機上的儲存體資源配置使用的區塊數量。 區塊大小是由 **HostResourceBlockSize** 屬性所指定。

</dd> <dt>

**VirtualQuantity**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](../wmisdk/standard-qualifiers.md) ( "VirtualQuantity" ) ， [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ( "[**CIM \_ StorageExtent**](cim-storageextent.md)。**NumberOfBlocks**"，"**CIM \_ StorageAllocationSettingData**.**VirtualQuantityUnits**") 
</dt> </dl>

儲存體配置向取用者呈現的區塊數目。

> [!Note]  
> **VirtualQuantity** 屬性可以指定 "1" 的區塊大小，即使 **VirtualResourceBlockSize** 是未知的。

 

</dd> <dt>

**VirtualQuantityUnits**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](../wmisdk/standard-qualifiers.md) ( "VirtualQuantityUnits" ) ， [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ( "**CIM \_ StorageAllocationSettingData**。**VirtualQuantity**") ， **IsPUnit**
</dt> </dl>

**VirtualQuantity** 屬性所使用的單位。 此值應該設定為「count (固定大社區塊) 」或「位元組」。 預設值 "count (fixed size block) " 應該用於固定區塊大小，而 "byte" 應該用於未知或變數區塊大小。

</dd> <dt>

**VirtualResourceBlockSize**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ( "[**CIM \_ StorageExtent**](cim-storageextent.md).**區塊**") ， **PUnit** (" byte ") 
</dt> </dl>

形成儲存體配置要求之區塊的大小（以位元組為單位）。 如果區塊大小為變數，則應該指定最大區塊大小。 如果區塊大小未知或區塊概念未套用，則區塊大小應該是 "1" (未知的) 。

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

[**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md)
</dt> </dl>

 


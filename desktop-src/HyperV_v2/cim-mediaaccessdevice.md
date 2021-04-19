---
description: 代表可以使用媒體來儲存和取出資料的裝置。
ms.assetid: c63b1731-dbc0-4e5e-acb8-cd91b5569dd2
title: 'CIM_MediaAccessDevice 類別 (Hyper-v 管理) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MediaAccessDevice
- CIM_MediaAccessDevice.Capabilities
- CIM_MediaAccessDevice.CapabilityDescriptions
- CIM_MediaAccessDevice.ErrorMethodology
- CIM_MediaAccessDevice.CompressionMethod
- CIM_MediaAccessDevice.NumberOfMediaSupported
- CIM_MediaAccessDevice.MaxMediaSize
- CIM_MediaAccessDevice.DefaultBlockSize
- CIM_MediaAccessDevice.MaxBlockSize
- CIM_MediaAccessDevice.MinBlockSize
- CIM_MediaAccessDevice.NeedsCleaning
- CIM_MediaAccessDevice.MediaIsLocked
- CIM_MediaAccessDevice.Security
- CIM_MediaAccessDevice.LastCleaned
- CIM_MediaAccessDevice.MaxAccessTime
- CIM_MediaAccessDevice.UncompressedDataRate
- CIM_MediaAccessDevice.LoadTime
- CIM_MediaAccessDevice.UnloadTime
- CIM_MediaAccessDevice.MountCount
- CIM_MediaAccessDevice.TimeOfLastMount
- CIM_MediaAccessDevice.TotalMountTime
- CIM_MediaAccessDevice.UnitsDescription
- CIM_MediaAccessDevice.MaxUnitsBeforeCleaning
- CIM_MediaAccessDevice.UnitsUsed
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 616148f6749f3ec00d019a903e8f9046d3aba602
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106986435"
---
# <a name="cim_mediaaccessdevice-class-hyper-v-management"></a>CIM_MediaAccessDevice 類別 (Hyper-v 管理) 

代表可以使用媒體來儲存和取出資料的裝置。

## <a name="syntax"></a>語法

``` syntax
[Abstract, Version("2.6.0"), UMLPackagePath("CIM::Device::StorageDevices"), AMENDMENT]
class CIM_MediaAccessDevice : CIM_LogicalDevice
{
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  string   ErrorMethodology;
  string   CompressionMethod;
  uint32   NumberOfMediaSupported;
  uint64   MaxMediaSize;
  uint64   DefaultBlockSize;
  uint64   MaxBlockSize;
  uint64   MinBlockSize;
  boolean  NeedsCleaning;
  boolean  MediaIsLocked;
  uint16   Security;
  datetime LastCleaned;
  uint64   MaxAccessTime;
  uint32   UncompressedDataRate;
  uint64   LoadTime;
  uint64   UnloadTime;
  uint64   MountCount;
  datetime TimeOfLastMount;
  uint64   TotalMountTime;
  string   UnitsDescription;
  uint64   MaxUnitsBeforeCleaning;
  uint64   UnitsUsed;
};
```

## <a name="members"></a>成員

**CIM \_ MediaAccessDevice** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**CIM \_ MediaAccessDevice** 類別具有這些方法。



| 方法                                               | 描述                                                            |
|:-----------------------------------------------------|:-----------------------------------------------------------------------|
| [**LockMedia**](cim-mediaaccessdevice-lockmedia.md) | 鎖定和解除鎖定媒體存取裝置中的卸載式媒體。<br/> |



 

### <a name="properties"></a>屬性

**CIM \_ MediaAccessDevice** 類別具有這些屬性。

<dl> <dt>

**Capabilities**
</dt> <dd> <dl> <dt>

資料類型： **uint16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已編制索引」 ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) (」 MIF。DMTF \| 儲存裝置 \| 001.9 "，" MIF。DMTF \| 儲存裝置 \| 001.11 "，" MIF。DMTF \| 儲存裝置 \| 001.12 "，" MIF。DMTF \| 磁片 \| 003.7 "，" MIF。DMTF \| 主機磁片 \| 001.2 "，" MIF。DMTF \| 主機磁片 \| 001.4 ") ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ MediaAccessDevice**。**CapabilityDescriptions**") 
</dt> </dl>

陣列，其中包含媒體存取裝置的功能。

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 (0) 


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**其他** (1) 


</dt> <dd></dd> <dt>

<span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>

**順序存取** (2) 


</dt> <dd></dd> <dt>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>

**隨機存取** (3) 


</dt> <dd></dd> <dt>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>

**支援寫入** (4) 


</dt> <dd></dd> <dt>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>

**加密** (5) 


</dt> <dd></dd> <dt>

<span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>

**壓縮** (6) 


</dt> <dd></dd> <dt>

<span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>

**支援卸除式媒體** (7) 


</dt> <dd></dd> <dt>

<span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>

**手動清除** (8) 


</dt> <dd></dd> <dt>

<span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>

**自動清除** (9) 


</dt> <dd></dd> <dt>

<span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>

**智慧型通知** (10) 


</dt> <dd></dd> <dt>

<span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>

**支援雙側媒體** (11) 


</dt> <dd></dd> <dt>

<span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>

**不需要 Predismount 退出** (12) 


</dt> <dd></dd> </dl>

</dd> <dt>

**CapabilityDescriptions**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Indexed" ) ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ MediaAccessDevice**。**功能**") 
</dt> </dl>

**功能** 陣列中專案的功能描述陣列。

</dd> <dt>

**CompressionMethod**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

裝置用來支援壓縮的演算法或工具的名稱。

如果未指定壓縮類型，則可以使用下列其中一個值：

-   「未知」壓縮支援不明或未指定。
-   支援「壓縮」壓縮，但類型未知或未指定。
-   「未壓縮」裝置不支援壓縮功能。

</dd> <dt>

**DefaultBlockSize**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Bytes" ) ， **PUnit** ( "byte" ) 
</dt> </dl>

裝置的預設區塊大小（以位元組為單位）。

</dd> <dt>

**ErrorMethodology**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

裝置支援的錯誤偵測類型和修正。

</dd> <dt>

**LastCleaned**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

上次清除裝置的日期和時間。

</dd> <dt>

**LoadTime**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "毫秒" ) ， **PUnit** ( "第 \* 10 ^-3" ) 
</dt> </dl>

裝置在裝置開始載入後，能夠讀取或寫入媒體所花費的時間（以毫秒為單位）。 例如，對於磁片磁碟機而言，這是磁片未切換至磁片的間隔，可供讀取/寫入作業。 針對磁帶機，這會在插入媒體時啟動，並在磁片磁碟機回報應用程式準備好時結束。 這通常是磁帶的磁帶 (BOT) 區域。

</dd> <dt>

**MaxAccessTime**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "毫秒" ) ， **PUnit** ( "第 \* 10 ^-3" ) 
</dt> </dl>

媒體的最大存取時間（以毫秒為單位）。 若是磁片磁碟機，這代表完整的搜尋和完整的旋轉延遲。 針對磁帶機，這代表從磁帶開頭到最遠距離點的搜尋。

</dd> <dt>

**MaxBlockSize**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Bytes" ) ， **PUnit** ( "byte" ) 
</dt> </dl>

裝置所存取媒體的最大區塊大小（以位元組為單位）。

</dd> <dt>

**MaxMediaSize**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 順序存取裝置 \| 001.2 "，" MIF。DMTF \| 主機磁片 \| 001.5」 ) 
</dt> </dl>

此裝置支援的媒體大小上限（以 kb 為單位）。

</dd> <dt>

**MaxUnitsBeforeCleaning**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ MediaAccessDevice**.**UnitsDescription**") 
</dt> </dl>

可以在裝置清理之前使用的單位數目上限。 **UnitsDescription** 會定義單位類型。

</dd> <dt>

**MediaIsLocked**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

如果媒體在裝置中鎖定且無法取出則為 **true** ;否則 **為 false**。 若為非卸載式裝置，此值應為 **true**。

</dd> <dt>

**MinBlockSize**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Bytes" ) ， **PUnit** ( "byte" ) 
</dt> </dl>

裝置所存取媒體的最社區塊大小（以位元組為單位）。

</dd> <dt>

**MountCount**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **計數器**
</dt> </dl>

裝載媒體以進行資料傳輸或清除裝置的次數。 如果裝置不支援卸載式媒體，則應該將此屬性設定為零。

</dd> <dt>

**NeedsCleaning**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

如果裝置需要清除，則 **為 true** ;否則 **為 false**。

> [!Note]  
> [ **功能** ] 屬性會指出是否可以手動或自動清除。

 

</dd> <dt>

**NumberOfMediaSupported**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

如果裝置支援多個個別媒體，則這個屬性會定義可支援或插入的最大數目。

</dd> <dt>

**安全性**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 磁片 \| 003.22 ") 
</dt> </dl>

裝置的營運安全性。

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**其他** (1) 


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 (2) 


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**無** (3) 


</dt> <dd></dd> <dt>

<span id="Read_Only"></span><span id="read_only"></span><span id="READ_ONLY"></span>

**唯讀** (4) 


</dt> <dd></dd> <dt>

<span id="Locked_Out"></span><span id="locked_out"></span><span id="LOCKED_OUT"></span>

**鎖定** (5) 


</dt> <dd></dd> <dt>

<span id="Boot_Bypass"></span><span id="boot_bypass"></span><span id="BOOT_BYPASS"></span>

**開機略過** (6) 


</dt> <dd></dd> <dt>

<span id="Boot_Bypass_and_Read_Only"></span><span id="boot_bypass_and_read_only"></span><span id="BOOT_BYPASS_AND_READ_ONLY"></span>

**開機略過和唯讀** (7) 


</dt> <dd></dd> </dl>

</dd> <dt>

**TimeOfLastMount**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

在裝置上掛接媒體的最新日期和時間。 只有支援卸載式媒體的裝置會使用此屬性。

</dd> <dt>

**TotalMountTime**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

載入媒體以進行資料傳輸或清除裝置的時間（以秒為單位）。 如果裝置不支援卸載式媒體，則應該將此屬性設定為零。

</dd> <dt>

**UncompressedDataRate**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「每秒的 kb」 ) ， **PUnit** ( "byte/Second \* 10 ^ 3" ) 
</dt> </dl>

裝置可以讀取和寫入媒體的持續性資料傳輸速率（以 kb 為單位）。 這是持續性的原始資料費率。 此屬性不應回報最大速率或使用壓縮的速率。

</dd> <dt>

**UnitsDescription**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ MediaAccessDevice**.**MaxUnitsBeforeCleaning**"，"**CIM \_ MediaAccessDevice**.**UnitsUsed**") 
</dt> </dl>

描述 **MaxUnitsBeforeCleaning** 和 **UnitsUsed** 屬性的單位類型。

</dd> <dt>

**UnitsUsed**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：量測 [**計、**](/windows/desktop/WmiSdk/standard-qualifiers) [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (」**CIM \_ MediaAccessDevice**。**UnitsDescription**"，"**CIM \_ MediaAccessDevice**.**MaxUnitsBeforeCleaning**") 
</dt> </dl>

裝置使用的單位數。 這個屬性是用來決定何時應該清除裝置。 **UnitsDescription** 會定義單位類型。

</dd> <dt>

**UnloadTime**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "毫秒" ) ， **PUnit** ( "第 \* 10 ^-3" ) 
</dt> </dl>

裝置從讀取或寫入媒體轉換成卸載時所花費的時間（以毫秒為單位）。 例如，對於磁片磁碟機而言，這是磁片在具有名義速度和沒有旋轉磁片之間的間隔時間。 針對磁帶機，這是媒體從其 BOT 進入完全退出並可供選擇器元素或人類操作的時間。

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

 


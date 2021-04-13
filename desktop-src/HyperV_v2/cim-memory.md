---
description: 代表記憶體相關邏輯裝置的功能和管理。
ms.assetid: 802c1c0e-7eab-4a17-9a29-6502ece6cb24
title: 'CIM_Memory 類別 (Hyper-v 管理) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Memory
- CIM_Memory.Volatile
- CIM_Memory.ErrorMethodology
- CIM_Memory.StartingAddress
- CIM_Memory.EndingAddress
- CIM_Memory.ErrorInfo
- CIM_Memory.OtherErrorDescription
- CIM_Memory.CorrectableError
- CIM_Memory.ErrorTime
- CIM_Memory.ErrorAccess
- CIM_Memory.ErrorTransferSize
- CIM_Memory.ErrorData
- CIM_Memory.ErrorDataOrder
- CIM_Memory.ErrorAddress
- CIM_Memory.SystemLevelAddress
- CIM_Memory.ErrorResolution
- CIM_Memory.AdditionalErrorData
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 410d580542421aee153b610726bed1f438efbcde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104513664"
---
# <a name="cim_memory-class-hyper-v-management"></a>CIM_Memory 類別 (Hyper-v 管理) 

代表記憶體相關邏輯裝置的功能和管理。

## <a name="syntax"></a>語法

``` syntax
[Abstract, Version("2.8.0"), UMLPackagePath("CIM::Device::Memory"), AMENDMENT]
class CIM_Memory : CIM_StorageExtent
{
  boolean  Volatile;
  string   ErrorMethodology;
  uint64   StartingAddress;
  uint64   EndingAddress;
  uint16   ErrorInfo;
  string   OtherErrorDescription;
  boolean  CorrectableError;
  datetime ErrorTime;
  uint16   ErrorAccess;
  uint32   ErrorTransferSize;
  uint8    ErrorData[];
  uint16   ErrorDataOrder;
  uint64   ErrorAddress;
  boolean  SystemLevelAddress;
  uint64   ErrorResolution;
  uint8    AdditionalErrorData[];
};
```

## <a name="members"></a>成員

**CIM \_ 記憶體** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**CIM \_ 記憶體** 類別具有這些屬性。

<dl> <dt>

**AdditionalErrorData**
</dt> <dd> <dl> <dt>

資料類型： **uint8** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ( "CIM \_ MemoryError. AdditionalErrorData" ) ， **OctetString**， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 記憶體裝置 \| 005.18 "，" MIF。DMTF \| 實體記憶體陣列 \| 001.13 ") 
</dt> </dl>

包含其他錯誤資訊的八位陣列。 例如，ECC 的症狀或使用以 CRC 為基礎的錯誤方法時，會傳回檢查位。 在後者的情況下，如果可辨識單一位錯誤，而且已知 CRC 演算法，就可以判斷失敗的確切位。

如果 **ErrorInfo** 屬性包含 "3" (確定) ，則不會使用這個屬性。

</dd> <dt>

**CorrectableError**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ( "CIM \_ MemoryError. CorrectableError" ) ， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 實體記憶體陣列 \| 001.8 ") 
</dt> </dl>

如果最新的錯誤可更正，則 **為 true** ;否則 **為 false**。 如果 **ErrorInfo** 屬性包含 "3" (確定) ，則不會使用這個屬性。

</dd> <dt>

**EndingAddress**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「kb」 ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) (」 MIF。DMTF \| 記憶體陣列對應位址 \| 001.4 "，" MIF。DMTF \| 記憶體裝置對應位址 \| 001.5 ") ， **PUnit** (" byte \* 10 ^ 3 ") 
</dt> </dl>

由應用程式或作業系統參考的結束位址，以及由記憶體物件的記憶體控制器所對應的結束位址。 結束位址是以 kb 來指定。

</dd> <dt>

**ErrorAccess**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ( "CIM \_ MemoryError. ErrorAccess" ) ， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 實體記憶體陣列 \| 001.10 ") 
</dt> </dl>

造成最後一個錯誤的記憶體存取作業。 如果 **ErrorInfo** 屬性包含 "3" (確定) ，則不會使用這個屬性。

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**其他** (1) 


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 (2) 


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

**閱讀** (3) 


</dt> <dd></dd> <dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

**撰寫** (4) 


</dt> <dd></dd> <dt>

<span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>

**部分寫入** (5) 


</dt> <dd></dd> </dl>

</dd> <dt>

**ErrorAddress**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ( "CIM \_ MemoryError. StartingAddress" ) ， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 記憶體裝置 \| 005.19 "，" MIF。DMTF \| 實體記憶體陣列 \| 001.14 ") 
</dt> </dl>

最後一個記憶體錯誤的位址。 錯誤的類型是由 **ErrorInfo** 屬性描述。 如果 **ErrorInfo** 屬性包含 "3" (確定) ，則不會使用這個屬性。

</dd> <dt>

**ErrorData**
</dt> <dd> <dl> <dt>

資料類型： **uint8** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ( "CIM \_ MemoryError. ErrorData" ) 、 **OctetString**、 [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( "INDEXED" ) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 實體記憶體陣列 \| 001.12 ") 
</dt> </dl>

陣列，其中包含最後一個錯誤記憶體存取期間所捕獲的資料。 資料會佔用陣列的前 n 個八位數位，以保存 **ErrorTransferSize** 屬性所指定的位數。

如果 **ErrorTransferSize** 屬性包含 "0" (確定) ，則不會使用這個屬性。

</dd> <dt>

**ErrorDataOrder**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ( "CIM \_ MemoryError. ErrorDataOrder" ) 
</dt> </dl>

儲存在 **ErrorData** 屬性中的資料排序。 「最小的位元組優先」 (值 = 1) 或「最重要的位元組優先」 (2) 可加以指定。 如果 **ErrorTransferSize** 屬性包含 "0" (確定) ，則不會使用這個屬性。

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 (0) 


</dt> <dd></dd> <dt>

<span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>

**最不重要的位元組先** (1) 


</dt> <dd></dd> <dt>

<span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>

**最重要的位元組先** (2) 


</dt> <dd></dd> </dl>

</dd> <dt>

**ErrorInfo**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ( 「CIM \_ MemoryError」 ) ， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (」 MIF。DMTF \| 記憶體裝置 \| 005.12 "，" MIF。DMTF \| 實體記憶體陣列 \| 001.8 ") ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ Memory**.**OtherErrorDescription**") 
</dt> </dl>

最後發生之錯誤的類型。

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**其他** (1) 


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 (2) 


</dt> <dd></dd> <dt>

<span id="OK"></span><span id="ok"></span>

**確定** (3) 


</dt> <dd></dd> <dt>

<span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>

**讀取** (4) 錯誤


</dt> <dd></dd> <dt>

<span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>

同位 **錯誤** (5) 


</dt> <dd></dd> <dt>

<span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>

**單一位錯誤** (6) 


</dt> <dd></dd> <dt>

<span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>

**雙位錯誤** (7) 


</dt> <dd></dd> <dt>

<span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>

**多位錯誤** (8) 


</dt> <dd></dd> <dt>

<span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>

**半位元組錯誤** (9) 


</dt> <dd></dd> <dt>

<span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>

總和 **檢查碼錯誤** (10) 


</dt> <dd></dd> <dt>

<span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>

**CRC 錯誤** (11) 


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

**未定義** 的 (12) 


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

**未定義** (13) 


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

**未定義** (14) 


</dt> <dd></dd> </dl>

</dd> <dt>

**ErrorMethodology**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "ErrorMethodology" ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 實體記憶體陣列 \| 001.7 ") 
</dt> </dl>

指出記憶體物件是否使用同位演算法、CRC 演算法、ECC 或其他機制。 也可以提供演算法的詳細資料。

</dd> <dt>

**ErrorResolution**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ( "CIM \_ MemoryError. ErrorResolution" ) ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Bytes" ) ， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 記憶體裝置 \| 005.21 "，" MIF。DMTF \| 實體記憶體陣列 \| 001.15 ") ， **PUnit** (" byte ") 
</dt> </dl>

可以解決最後一個錯誤的範圍（以位元組為單位）。 例如，如果錯誤位址解析為位11，例如一般頁面，然後，錯誤可以解析成4K 界限，而這個屬性會設定為 "4000"。 如果 **ErrorInfo** 屬性包含 "3" (確定) ，則不會使用這個屬性。

</dd> <dt>

**ErrorTime**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ( "CIM \_ MemoryError. ErrorTime" ) 
</dt> </dl>

上次發生記憶體錯誤的時間。 如果 **ErrorInfo** 屬性包含 "3" (確定) ，則不會使用這個屬性。

</dd> <dt>

**ErrorTransferSize**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ( "CIM \_ MemoryError. ErrorTransferSize" ) ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Bits" ) ， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 實體記憶體陣列 \| 001.11 ") ， **PUnit** (" bit ") 
</dt> </dl>

造成最後一個錯誤的資料傳輸大小（以位為單位）。 "0" 表示無錯誤。 如果 **ErrorInfo** 屬性包含 "3" (確定) ，則不會使用這個屬性。

</dd> <dt>

**OtherErrorDescription**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ( 「cim \_ MemoryError. OtherErrorDescription」 ) ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「**cim \_ 記憶體**」。**ErrorInfo**」 ) 
</dt> </dl>

錯誤類型的描述（當 **ErrorType** 屬性設定為 "1" (其他) 時）。

</dd> <dt>

**StartingAddress**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「kb」 ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) (」 MIF。DMTF \| 記憶體陣列對應位址 \| 001.3 "，" MIF。DMTF \| 記憶體裝置對應位址 \| 001.4 ") ， **PUnit** (" byte \* 10 ^ 3 ") 
</dt> </dl>

由應用程式或作業系統參考的起始位址，以及由記憶體物件的記憶體控制器所對應的起始位址。 起始位址的指定單位為 kb。

</dd> <dt>

**SystemLevelAddress**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ( "CIM \_MemoryError.SystemLevelAddress" ) 
</dt> </dl>

如果 **ErrorAddress** 屬性中的位址資訊是系統層級的位址，則為 **true** ，如果是實體位址，則為 **false** 。

</dd> <dt>

**揮發 性**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

如果記憶體是暫時性的，則 **為 true** ;否則 **為 false**。

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

[**CIM \_ StorageExtent**](cim-storageextent.md)
</dt> </dl>

 


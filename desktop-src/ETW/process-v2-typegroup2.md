---
description: 這個類別是處理常式計數器事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 7f1fa1c4-a2ff-4a1c-ac9d-e922a13c99a1
title: Process_V2_TypeGroup2 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Process_V2_TypeGroup2
- Process_V2_TypeGroup2.ProcessId
- Process_V2_TypeGroup2.PageFaultCount
- Process_V2_TypeGroup2.HandleCount
- Process_V2_TypeGroup2.Reserved
- Process_V2_TypeGroup2.PeakVirtualSize
- Process_V2_TypeGroup2.PeakWorkingSetSize
- Process_V2_TypeGroup2.PeakPagefileUsage
- Process_V2_TypeGroup2.QuotaPeakPagedPoolUsage
- Process_V2_TypeGroup2.QuotaPeakNonPagedPoolUsage
- Process_V2_TypeGroup2.VirtualSize
- Process_V2_TypeGroup2.WorkingSetSize
- Process_V2_TypeGroup2.PagefileUsage
- Process_V2_TypeGroup2.QuotaPagedPoolUsage
- Process_V2_TypeGroup2.QuotaNonPagedPoolUsage
- Process_V2_TypeGroup2.PrivatePageCount
api_type:
- NA
api_location: ''
ms.openlocfilehash: 284b77da03b53f9c2662c8729a7bf6606c45630a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851591"
---
# <a name="process_v2_typegroup2-class"></a>進程 \_ V2 \_ TypeGroup2 類別

這個類別是處理常式計數器事件的事件種類類別。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
[EventType{32, 33}, EventTypeName{"PerfCtr", PerfCtrRundown"}]
class Process_V2_TypeGroup2 : Process_V2
{
  uint32 ProcessId;
  uint32 PageFaultCount;
  uint32 HandleCount;
  uint32 Reserved;
  object PeakVirtualSize;
  object PeakWorkingSetSize;
  object PeakPagefileUsage;
  object QuotaPeakPagedPoolUsage;
  object QuotaPeakNonPagedPoolUsage;
  object VirtualSize;
  object WorkingSetSize;
  object PagefileUsage;
  object QuotaPagedPoolUsage;
  object QuotaNonPagedPoolUsage;
  object PrivatePageCount;
};
```

## <a name="members"></a>成員

**Process \_ V2 \_ TypeGroup2** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Process \_ V2 \_ TypeGroup2** 類別具有這些屬性。

<dl> <dt>

**HandleCount**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (3) 
</dt> </dl>

使用的控制碼計數。

</dd> <dt>

**PageFaultCount**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (2) 
</dt> </dl>

分頁錯誤的計數。

</dd> <dt>

**PagefileUsage**
</dt> <dd> <dl> <dt>

資料類型： **物件**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (12) ，副檔名 ( "SizeT" ) 
</dt> </dl>

目前的分頁檔案使用方式。

</dd> <dt>

**PeakPagefileUsage**
</dt> <dd> <dl> <dt>

資料類型： **物件**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (7) ，副檔名 ( "SizeT" ) 
</dt> </dl>

使用了最大的頁面檔案大小。

</dd> <dt>

**PeakVirtualSize**
</dt> <dd> <dl> <dt>

資料類型： **物件**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (5) ，副檔名 ( "SizeT" ) 
</dt> </dl>

使用的虛擬頁面大小最大。

</dd> <dt>

**PeakWorkingSetSize**
</dt> <dd> <dl> <dt>

資料類型： **物件**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (6) ，副檔名 ( "SizeT" ) 
</dt> </dl>

使用了最大的工作集大小。

</dd> <dt>

**PrivatePageCount**
</dt> <dd> <dl> <dt>

資料類型： **物件**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (15) ，副檔名 ( "SizeT" ) 
</dt> </dl>

目前的私人實體頁面計數。

</dd> <dt>

ProcessId
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (1) ，格式 ( "x" ) 
</dt> </dl>

您可以用來識別進程的全域處理序識別碼。 此值從建立進程到終止之前都有效。

</dd> <dt>

**QuotaNonPagedPoolUsage**
</dt> <dd> <dl> <dt>

資料類型： **物件**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (14) ，副檔名 ( "SizeT" ) 
</dt> </dl>

目前認可的非分頁式記憶體使用量。

</dd> <dt>

**QuotaPagedPoolUsage**
</dt> <dd> <dl> <dt>

資料類型： **物件**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (13) ，副檔名 ( "SizeT" ) 
</dt> </dl>

目前已認可的分頁記憶體使用量。

</dd> <dt>

**QuotaPeakNonPagedPoolUsage**
</dt> <dd> <dl> <dt>

資料類型： **物件**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (9) ，副檔名 ( "SizeT" ) 
</dt> </dl>

使用的最大認可非分頁式記憶體。

</dd> <dt>

**QuotaPeakPagedPoolUsage**
</dt> <dd> <dl> <dt>

資料類型： **物件**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (8) ，副檔名 ( "SizeT" ) 
</dt> </dl>

使用的最大認可分頁記憶體。

</dd> <dt>

**已保留**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (4) 
</dt> </dl>

保留的。

</dd> <dt>

**VirtualSize**
</dt> <dd> <dl> <dt>

資料類型： **物件**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (10) ，副檔名 ( "SizeT" ) 
</dt> </dl>

目前的虛擬頁面大小。

</dd> <dt>

**WorkingSetSize**
</dt> <dd> <dl> <dt>

資料類型： **物件**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (11) ，副檔名 ( "SizeT" ) 
</dt> </dl>

目前的工作集大小。

</dd> </dl>

## <a name="remarks"></a>備註

當進程結束時，會記錄這些事件。 此事件表示進程處理記憶體使用量的方式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**進程 \_ V2**](process-v2.md)
</dt> </dl>

 

 





---
description: Process_V2_TypeGroup1 類別-這個類別是處理事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: ff5c1f64-2087-4238-81f9-6283f0f0e68a
title: Process_V2_TypeGroup1 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Process_V2_TypeGroup1
- Process_V2_TypeGroup1.UniqueProcessKey
- Process_V2_TypeGroup1.ProcessId
- Process_V2_TypeGroup1.ParentId
- Process_V2_TypeGroup1.SessionId
- Process_V2_TypeGroup1.ExitStatus
- Process_V2_TypeGroup1.UserSID
- Process_V2_TypeGroup1.ImageFileName
- Process_V2_TypeGroup1.CommandLine
api_type:
- NA
api_location: ''
ms.openlocfilehash: b587a07f33b066cfd7dbeebc44d7277b33c6bee8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106306"
---
# <a name="process_v2_typegroup1-class"></a>進程 \_ V2 \_ TypeGroup1 類別

這個類別是處理事件的事件種類類別。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
[EventType{1, 2, 3, 4, 39}, EventTypeName{"Start", "End", "DCStart", "DCEnd", "Defunct"}]
class Process_V2_TypeGroup1 : Process_V2
{
  uint32 UniqueProcessKey;
  uint32 ProcessId;
  uint32 ParentId;
  uint32 SessionId;
  sint32 ExitStatus;
  object UserSID;
  string ImageFileName;
  string CommandLine;
};
```

## <a name="members"></a>成員

**Process \_ V2 \_ TypeGroup1** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Process \_ V2 \_ TypeGroup1** 類別具有這些屬性。

<dl> <dt>

CommandLine
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (8) 、StringTermination ( "NullTerminated" ) 、Format ( "w" ) 
</dt> </dl>

進程的完整命令列。

</dd> <dt>

ExitStatus
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (5) 
</dt> </dl>

已停止進程的結束狀態。

</dd> <dt>

ImageFileName
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (7) ，StringTermination ( "NullTerminated" ) 
</dt> </dl>

進程可執行檔的路徑。

</dd> <dt>

ParentId
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (3) ，格式 ( "x" ) 
</dt> </dl>

建立此進程之進程的唯一識別碼。 系統會重複使用處理序識別碼，因此它們只會在該進程的存留期內找出處理常式。 ParentProcessId 所識別的進程可能會終止，因此 ParentProcessId 可能不會參考執行中的進程。 ParentProcessId 也可能不正確地參考重複使用處理序識別碼的進程。

</dd> <dt>

ProcessId
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (2) ，格式 ( "x" ) 
</dt> </dl>

您可以用來識別進程的全域處理序識別碼。 此值從建立進程到終止之前都有效。

</dd> <dt>

SessionId
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (4) 
</dt> </dl>

作業系統在建立新的會話時所產生的唯一識別碼。 會話從登入到從特定系統登出的一段時間。

</dd> <dt>

UniqueProcessKey
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (1) ，指標
</dt> </dl>

核心中處理常式物件的位址。

</dd> <dt>

UserSID
</dt> <dd> <dl> <dt>

資料類型： **物件**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (6) ，副檔名 ( "Sid" ) 
</dt> </dl>

安全性識別元 (SID) 用於事件發生所在的使用者內容。

</dd> </dl>

## <a name="remarks"></a>備註

DCStart 和 DCEnd 事件種類會列舉目前正在執行的進程，包括每次核心會話開始和結束時的閒置和系統進程。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/> |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>       |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**進程 \_ V2**](process-v2.md)
</dt> </dl>

 

 





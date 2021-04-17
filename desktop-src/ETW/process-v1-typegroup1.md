---
description: 這個類別是處理事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: b114d7fd-c308-4f21-8f1a-ab27dc93abc5
title: Process_V1_TypeGroup1 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Process_V1_TypeGroup1
- Process_V1_TypeGroup1.PageDirectoryBase
- Process_V1_TypeGroup1.ProcessId
- Process_V1_TypeGroup1.ParentId
- Process_V1_TypeGroup1.SessionId
- Process_V1_TypeGroup1.ExitStatus
- Process_V1_TypeGroup1.UserSID
- Process_V1_TypeGroup1.ImageFileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: fc2308965de5c06a25858a138d4536763613a4d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320112"
---
# <a name="process_v1_typegroup1-class"></a>Process \_ V1 \_ TypeGroup1 類別

這個類別是處理事件的事件種類類別。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
[EventType{1, 2, 3, 4}, EventTypeName{"Start", "End", "DCStart", "DCEnd"}]
class Process_V1_TypeGroup1 : Process_V1
{
  uint32 PageDirectoryBase;
  uint32 ProcessId;
  uint32 ParentId;
  uint32 SessionId;
  sint32 ExitStatus;
  object UserSID;
  string ImageFileName;
};
```

## <a name="members"></a>成員

**Process \_ V1 \_ TypeGroup1** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Process \_ V1 \_ TypeGroup1** 類別具有這些屬性。

<dl> <dt>

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

PageDirectoryBase
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (1) ，指標
</dt> </dl>

保留的。

</dd> <dt>

ParentId
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (3) 
</dt> </dl>

建立此進程之進程的唯一識別碼。 系統會重複使用處理序識別碼，因此它們只會在該進程的存留期內找出處理常式。 ParentProcessId 所識別的進程可能會終止，因此 ParentProcessId 可能不會參考執行中的進程。 ParentProcessId 也可能不正確地參考重複使用處理序識別碼的進程。

**Windows Server 2003：** 包含 ( "x" ) 限定詞的格式。

</dd> <dt>

ProcessId
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (2) 
</dt> </dl>

您可以用來識別進程的全域處理序識別碼。 此值從建立進程到終止之前都有效。

**Windows Server 2003：** 包含 ( "x" ) 限定詞的格式。

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

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**進程 \_ V1**](process.md)
</dt> <dt>

[**進程 \_ V1**](process-v1.md)
</dt> </dl>

 

 





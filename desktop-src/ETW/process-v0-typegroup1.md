---
description: Process_V0_TypeGroup1 類別-這個類別是處理事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: fcf2897d-32b4-42b9-892c-f0106687d3c2
title: Process_V0_TypeGroup1 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Process_V0_TypeGroup1
- Process_V0_TypeGroup1.ProcessId
- Process_V0_TypeGroup1.ParentId
- Process_V0_TypeGroup1.UserSID
- Process_V0_TypeGroup1.ImageFileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 0d42ed4704eafcbb335b29c2c2d8d83e2ea82591c75855a6da096cb1e11a7572
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118394434"
---
# <a name="process_v0_typegroup1-class"></a>Process \_ V0 \_ TypeGroup1 類別

這個類別是處理事件的事件種類類別。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
[EventType{1, 2, 3, 4}, EventTypeName{"Start", "End", "DCStart", "DCEnd"}]
class Process_V0_TypeGroup1 : Process_V0
{
  uint32 ProcessId;
  uint32 ParentId;
  object UserSID;
  string ImageFileName;
};
```

## <a name="members"></a>成員

**Process \_ V0 \_ TypeGroup1** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Process \_ V0 \_ TypeGroup1** 類別具有這些屬性。

<dl> <dt>

ImageFileName
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (4) ，StringTermination ( "NullTerminated" ) 
</dt> </dl>

進程可執行檔的路徑。

</dd> <dt>

ParentId
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (2) ，指標
</dt> </dl>

建立進程之進程的唯一識別碼。 系統會重複使用處理序識別碼，因此它們只會在該進程的存留期內找出處理常式。 ParentProcessId 所識別的進程可能會終止，因此 ParentProcessId 可能不會參考執行中的進程。 ParentProcessId 也可能不正確地參考重複使用處理序識別碼的進程。

</dd> <dt>

ProcessId
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (1) ，指標
</dt> </dl>

您可以用來識別進程的全域處理序識別碼。 此值從建立進程到終止之前都有效。

</dd> <dt>

UserSID
</dt> <dd> <dl> <dt>

資料類型： **物件**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (3) ，副檔名 ( "Sid" ) 
</dt> </dl>

安全性識別元 (SID) 用於事件發生所在的使用者內容。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>          |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**進程 \_ V0**](process-v0.md)
</dt> </dl>

 

 





---
description: 從中衍生所有事件追蹤類別的抽象類別。
ms.assetid: 03eea902-5050-4ab2-8a72-9bff7777e234
title: EventTrace 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EventTrace
- EventTrace.EventSize
- EventTrace.ReservedHeaderField
- EventTrace.EventType
- EventTrace.TraceLevel
- EventTrace.TraceVersion
- EventTrace.ThreadId
- EventTrace.TimeStamp
- EventTrace.EventGuid
- EventTrace.KernelTime
- EventTrace.UserTime
- EventTrace.InstanceId
- EventTrace.ParentGuid
- EventTrace.ParentInstanceId
- EventTrace.MofData
- EventTrace.MofLength
api_type:
- NA
api_location: ''
ms.openlocfilehash: f04399942b39a2da5b746933884a436a65bb370c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690880"
---
# <a name="eventtrace-class"></a>EventTrace 類別

從中衍生所有事件追蹤類別的抽象類別。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
[abstract]
class EventTrace
{
  uint16 EventSize;
  uint16 ReservedHeaderField;
  uint8  EventType;
  uint8  TraceLevel;
  uint16 TraceVersion;
  uint64 ThreadId;
  uint64 TimeStamp;
  uint8  EventGuid[];
  uint32 KernelTime;
  uint32 UserTime;
  uint32 InstanceId;
  uint8  ParentGuid[];
  uint32 ParentInstanceId;
  uint32 MofData;
  uint32 MofLength;
};
```

## <a name="members"></a>成員

**EventTrace** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**EventTrace** 類別具有這些屬性。

<dl> <dt>

**EventGuid**
</dt> <dd> <dl> <dt>

資料類型： **uint8** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (8) ， **最大** (16) 
</dt> </dl>

此事件的事件追蹤類別 GUID。

</dd> <dt>

**EventSize**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (1) 
</dt> </dl>

事件的位元組總數。

</dd> <dt>

**EventType**
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (3) 
</dt> </dl>

提供者定義的事件種類。 告訴您要使用哪一個事件種類類別來解密提供者定義的事件資料 (**MofData** 所指向的資料。

</dd> <dt>

**InstanceId**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (11) 
</dt> </dl>

此事件實例的識別碼。

</dd> <dt>

**KernelTime**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (9) 
</dt> </dl>

核心模式指令的經過執行時間，以 CPU 滴答為單位。

</dd> <dt>

**MofData**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (14) ， **指標**
</dt> </dl>

提供者特定事件資料的指標。

</dd> <dt>

**MofLength**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (15) 
</dt> </dl>

提供者特定事件資料的長度。

</dd> <dt>

**ParentGuid**
</dt> <dd> <dl> <dt>

資料類型： **uint8** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (12) ， **最大** (16) 
</dt> </dl>

父實例的事件追蹤類別 GUID。

</dd> <dt>

**ParentInstanceId**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (13) 
</dt> </dl>

父實例資料的識別碼。

</dd> <dt>

**ReservedHeaderField**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (2) 
</dt> </dl>

保留的。

</dd> <dt>

**ThreadId**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (6) ， **指標**
</dt> </dl>

識別已產生事件的執行緒。

</dd> <dt>

**時間 戳**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (7) 
</dt> </dl>

包含發生事件的日期和時間。

</dd> <dt>

**TraceLevel**
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (4) 
</dt> </dl>

提供者定義的值，定義用來產生事件的嚴重性層級。

</dd> <dt>

**TraceVersion**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (5) 
</dt> </dl>

用來產生事件之事件追蹤類別的提供者定義版本號碼。

</dd> <dt>

**UserTime**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (10) 
</dt> </dl>

使用者模式指示的經過執行時間，以 CPU 滴答為單位。

</dd> </dl>

## <a name="remarks"></a>備註

請勿使用這些屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                         |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                               |
| MOF<br/>                      | <dl> <dt>Wmi. mof</dt> </dl> |



 

 





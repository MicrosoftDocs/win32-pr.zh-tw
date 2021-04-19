---
description: UPDATE \_ 事件結構會更新事件。 此結構會透過 NPP 的事件狀態回呼程式，傳回給呼叫的應用程式。
ms.assetid: 6896be5a-f986-44ff-a18b-010f7b9858aa
title: 'UPDATE_EVENT 結構 (Netmon) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UPDATE_EVENT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 3da45020a68114182a71b25ff9bba380d3f89eee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106978916"
---
# <a name="update_event-structure"></a>更新 \_ 事件結構

**UPDATE \_ 事件** 結構會更新事件。 此結構會透過 NPP 的事件狀態回呼程式，傳回給呼叫的應用程式。

## <a name="syntax"></a>語法


```C++
typedef struct _UPDATE_EVENT {
  USHORT       Event;
  DWORD        Action;
  DWORD        Status;
  DWORD        Value;
  __int64      TimeStamp;
  DWORD_PTR    lpUserContext;
  DWORD_PTR    lpReserved;
  UINT         FramesDropped;
  union {
    DWORD                        Reserved;
    LPFRAMETABLE                 lpFrameTable;
    DWORD_PTR                    lpPacketQueue;
    SECURITY_PERMISSION_RESPONSE SecurityResponse;
  };
  LPSTATISTICS lpFinalStats;
} UPDATE_EVENT, *PUPDATE_EVENT;
```



## <a name="members"></a>成員

<dl> <dt>

**事件**
</dt> <dd>

實際記錄的事件。

</dd> <dt>

**動作**
</dt> <dd>

採取的動作。

</dd> <dt>

**狀態**
</dt> <dd>

網路狀態指示。

</dd> <dt>

**值**
</dt> <dd>

輔助計數器變數。

</dd> <dt>

**時間 戳**
</dt> <dd>

標示的事件（以微秒為單位）。

</dd> <dt>

**lpUserCoNtext**
</dt> <dd>

應用程式所提供的使用者內容。

</dd> <dt>

**lpReserved**
</dt> <dd>

驅動程式或 NAL 使用。

</dd> <dt>

**FramesDropped**
</dt> <dd>

放在指定緩衝區中的 RTF 框架。

</dd> <dt>

**已保留**
</dt> <dd>

此切換選項不會傳回任何資料。

</dd> <dt>

**lpFrameTable**
</dt> <dd>

僅限 RTF。

</dd> <dt>

**lpPacketQueue**
</dt> <dd>

適用于傳輸。

</dd> <dt>

**SecurityResponse**
</dt> <dd>

遠端安全性監視器回應。

</dd> <dt>

**lpFinalStats**
</dt> <dd>

這只會填入非安全性相關的停止 (例如，觸發程式) 。

</dd> </dl>

## <a name="remarks"></a>備註

C + + 使用者應該注意，此回呼的宣告應該在標頭檔的公開部分中：

``` syntax
static WINAPI DWORD NetworkCallback( UPDATE_EVENT events);
```

此實應位於 .cpp 檔案的 protected 區段中：

``` syntax
DWORD WINAPI ClassName::NetworkCallback( UPDATE_EVENT events) {};
```

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl> |



 

 





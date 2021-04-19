---
description: 儲存共用記憶體區段的相關資訊。
ms.assetid: 73a650ee-110c-43f2-a5e2-783d52fd29ee
title: SHAREDMEMORY_HEADER 結構
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SHAREDMEMORY_HEADER
api_type:
- NA
api_location: ''
ms.openlocfilehash: 695f3ef09cb5e7e67de757ee3926df6fde7ddff5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997832"
---
# <a name="sharedmemory_header-structure"></a>SHAREDMEMORY \_ 標頭結構

儲存共用記憶體區段的相關資訊。

## <a name="syntax"></a>語法


```C++
typedef struct _SHAREDMEMORY_HEADER {
  DWORD             cbTotal;
  DWORD             cbOffsetSns;
  DWORD             idxEvent;
  DWORD             dwEvent;
  CURSOR_ID         cid;
  DWORD             sn;
  SYSTEM_EVENT      sysEvt;
  SYSTEM_EVENT_DATA sysEvtData;
  DWORD             cPackets;
  DWORD             cbPackets;
  BOOL              fSnsPresent;
} SHAREDMEMORY_HEADER, *PSHAREDMEMORY_HEADER;
```



## <a name="members"></a>成員

<dl> <dt>

**cbTotal**
</dt> <dd>

此標頭結構所參考之資料的大小（以位元組為單位）。

</dd> <dt>

**cbOffsetSns**
</dt> <dd>

序號與標頭結構之間的位移大小（以位元組為單位）。

</dd> <dt>

**idxEvent**
</dt> <dd>

事件索引。 此值會隨著連續的事件遞增。

</dd> <dt>

**dwEvent**
</dt> <dd>

與此標頭相關聯的事件。

</dd> <dt>

**Cid**
</dt> <dd>

共用記憶體標頭所參考的資料指標識別碼。

</dd> <dt>

**sn**
</dt> <dd>

共用記憶體標頭的序號。

</dd> <dt>

**sysEvt**
</dt> <dd>

\_ \* 與此標頭相關聯的系統事件（前置詞為 SE）。 如需詳細資訊，請參閱「備註」一節。

</dd> <dt>

**sysEvtData**
</dt> <dd>

與系統事件相關聯的 [**系統 \_ 事件 \_ 資料**](/windows/win32/api/tpcshrd/ns-tpcshrd-system_event_data) 結構。

</dd> <dt>

**cPackets**
</dt> <dd>

與目前共用記憶體區段關聯的封包計數。

</dd> <dt>

**cbPackets**
</dt> <dd>

與目前共用記憶體區段相關聯的封包大小（以位元組為單位）。

</dd> <dt>

**fSnsPresent**
</dt> <dd>

指出序號是否存在於目前的共用記憶體區段中的旗標。

</dd> </dl>

## <a name="remarks"></a>備註

下列是針對 **sysEvt** 成員定義的值。


```C++
#define SE_NONE                  0x00000000
#define SE_TAP                   0x00000010
#define SE_DBL_TAP               0x00000011
#define SE_RIGHT_TAP             0x00000012
#define SE_DRAG                  0x00000013
#define SE_RIGHT_DRAG            0x00000014
#define SE_HOLD_ENTER            0x00000015
#define SE_HOLD_LEAVE            0x00000016
#define SE_HOVER_ENTER           0x00000017
#define SE_HOVER_LEAVE           0x00000018
#define SE_FLICK                 0x0000001F
```



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**系統 \_ 事件 \_ 資料**](/windows/win32/api/tpcshrd/ns-tpcshrd-system_event_data)
</dt> </dl>

 

 




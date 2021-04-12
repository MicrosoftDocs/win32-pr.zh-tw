---
title: ORPC_INIT_ARGS 結構
description: ORPC INIT ARGS （引數） \_ \_ 結構包含用來初始化使用 IOrpcDebugNotify 介面進行遠端偵錯的資訊。
ms.assetid: be7646c7-3394-45ae-ae8f-9cee68bbc789
keywords:
- ORPC_INIT_ARGS 結構 COM
- LPORPC_INIT_ARGS 結構指標 COM
topic_type:
- apiref
api_name:
- ORPC_INIT_ARGS
api_location:
- N/A
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e7dca0209f745d5034bde2da852829b99d7dcb8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094204"
---
# <a name="orpc_init_args-structure"></a>ORPC \_ INIT \_ ARGS 變數結構

**ORPC \_ INIT \_ ARGS** （引數）結構包含用來初始化使用 [**IOrpcDebugNotify**](iorpcdebugnotify.md)介面進行遠端偵錯的資訊。

## <a name="syntax"></a>語法


```C++
typedef struct ORPC_INIT_ARGS {
  IOrpcDebugNotify *lpIntfOrpcDebug;
  void             *pvPSN;
  DWORD            *dwReserved1;
  DWORD            *dwReserved2;
} ORPC_INIT_ARGS, *LPORPC_INIT_ARGS;
```



## <a name="members"></a>成員

<dl> <dt>

**lpIntfOrpcDebug**
</dt> <dd>

[**IOrpcDebugNotify**](iorpcdebugnotify.md)介面的指標，可供同進程偵錯工具使用。 如果偵錯工具不在進程中或為 Macintosh 系統，此欄位必須是 **Null**。

</dd> <dt>

**pvPSN**
</dt> <dd>

偵錯工具之進程式號的指標。 如果偵錯工具不是 Macintosh 系統，此欄位必須是 **Null**。

</dd> <dt>

**dwReserved1**
</dt> <dd>

保留的。 必須是 0。

</dd> <dt>

**dwReserved2**
</dt> <dd>

保留的。 必須是 0。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                     |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                           |
| 標頭<br/>                   | <dl> <dt>N/A</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ORPC \_ DBG \_ ALL**](orpc-dbg-all.md)
</dt> <dt>

[**ORPC \_ DBG \_ 緩衝區**](orpc-dbg-buffer.md)
</dt> <dt>

[**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md)
</dt> <dt>

[**IOrpcDebugNotify**](iorpcdebugnotify.md)
</dt> </dl>

 

 






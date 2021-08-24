---
title: 'ICM_SET_STATUS_PROC 訊息 (Vfw .h) '
description: ICM \_ 設定 \_ 狀態程式 \_ 訊息提供狀態回呼函式，其狀態為冗長的作業。
ms.assetid: a1bcd840-b94b-487e-91d6-67411a8a3a2d
keywords:
- ICM_SET_STATUS_PROC 訊息 Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_SET_STATUS_PROC
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c02019bb6375aa18fd37ba34d2603839b37291d58822858b0b9cabc01e47d7b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678338"
---
# <a name="icm_set_status_proc-message"></a>ICM \_設定 \_ 狀態 \_ 進程訊息

**ICM \_ 設定 \_ 狀態 \_** 程式訊息提供狀態回呼函式，其狀態為冗長的作業。


```C++
ICM_SET_STATUS_PROC 
wParam = (DWORD_PTR)icsetstatusProc; 
lParam = sizeof(ICSETSTATUSPROC); 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="icsetstatusProc"></span><span id="icsetstatusproc"></span><span id="ICSETSTATUSPROC"></span>*icsetstatusProc*
</dt> <dd>

[**ICSETSTATUSPROC**](/windows/desktop/api/Vfw/ns-vfw-icsetstatusproc)結構的指標。

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

**ICSETSTATUSPROC** 的大小（以位元組為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則會傳回 ICERR \_ OK，否則會傳回錯誤。

## <a name="remarks"></a>備註

此訊息的支援是選擇性的，但強烈建議在壓縮或解壓縮所花的時間超過大約一秒的1秒。

應用程式可以在冗長的作業期間，定期將此訊息傳送至狀態回呼函式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                       |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Vfw。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[影片壓縮管理員](video-compression-manager.md)
</dt> <dt>

[影片壓縮訊息](video-compression-messages.md)
</dt> </dl>

 

 






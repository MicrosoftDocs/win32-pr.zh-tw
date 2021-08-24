---
title: WM_POINTERROUTEDRELEASED 訊息
description: 傳送至所有進程 (透過 AddContentWithCrossProcessChaining 設定跨進程的連結，而且目前在目前的進程上收到 WM_POINTERUP 訊息時，目前未處理指標輸入) 與特定指標識別碼相關聯。
ms.assetid: B031ED80-6F1B-42A7-B4E2-55934E2C456C
keywords:
- WM_POINTERROUTEDRELEASED 訊息輸入訊息和通知
topic_type:
- apiref
api_name:
- WM_POINTERROUTEDRELEASED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 318134779d94824daef0b05903f45121665892fbcafbeb48589ef150f324d2b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119611288"
---
# <a name="wm_pointerroutedreleased-message"></a>WM_POINTERROUTEDRELEASED 訊息

傳送至所有進程 (透過 [**AddContentWithCrossProcessChaining**](/windows/win32/api/directmanipulation/nf-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining) 設定跨進程的連結，而且目前在目前的進程上收到 [**WM_POINTERUP**](wm-pointerup.md) 訊息時，目前未處理指標輸入) 與特定指標識別碼相關聯。


```C++
#define WM_POINTERROUTEDRELEASED       0x0253
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

未使用的。

</dd> <dt>

*lParam* 
</dt> <dd>

未使用的。

</dd> </dl>

## <a name="return-value"></a>傳回值

NULL

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10 \[僅限桌面應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | Windows Server 2016 \[僅限桌面應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[訊息](messages.md)
</dt> </dl>

 


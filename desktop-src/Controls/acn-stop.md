---
title: 'ACN_STOP (Commctrl 的通知碼) '
description: 通知動畫控制項的父視窗，相關聯的 AVI 剪輯已停止播放。 此通知碼會以 WM 命令訊息的形式傳送 \_ 。
ms.assetid: 2f21a2ec-975f-4592-8b21-956bd5311ef4
keywords:
- ACN_STOP 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- ACN_STOP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cbdb27677439b7f08b489cba9024d44f3ebee6d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024803"
---
# <a name="acn_stop-notification-code"></a>ACN \_ 停止通知碼

通知動畫控制項的父視窗，相關聯的 AVI 剪輯已停止播放。 此通知碼會以 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息的形式傳送。


```C++
ACN_STOP     

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))包含動畫控制項的識別碼。 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))會指定通知碼。

</dd> <dt>

*lParam* 
</dt> <dd>

指定動畫控制項之控制碼的 **HWND** 。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 


---
title: 'ACN_START (Commctrl 的通知碼) '
description: 通知動畫控制項的父視窗，相關聯的 AVI 剪輯已開始播放。 此通知碼會以 WM 命令訊息的形式傳送 \_ 。
ms.assetid: b4d12225-36f7-4f87-b58a-dac091d14e4c
keywords:
- ACN_START 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- ACN_START
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ccfb5a1fc1f6b258cfe8363e99f38894ed7e601401d4f725431992a31f86376
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119922158"
---
# <a name="acn_start-notification-code"></a>ACN \_ 啟動通知碼

通知動畫控制項的父視窗，相關聯的 AVI 剪輯已開始播放。 此通知碼會以 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息的形式傳送。


```C++
ACN_START 

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
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 


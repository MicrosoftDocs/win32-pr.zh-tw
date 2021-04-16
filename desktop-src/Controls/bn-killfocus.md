---
title: 'BN_KILLFOCUS (Winuser 的通知碼) '
description: 當按鈕失去鍵盤焦點時傳送。 此按鈕必須有 BS \_ 通知樣式才能傳送此通知碼。 按鈕的父視窗會透過 WM 命令訊息接收此通知碼 \_ 。
ms.assetid: 740154ba-47fd-4084-8b86-6166f1e1b39f
keywords:
- BN_KILLFOCUS 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- BN_KILLFOCUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3fb6737d88ccddedbba6db58ffd0f713da7a8a2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464665"
---
# <a name="bn_killfocus-notification-code"></a>BN \_ KILLFOCUS 通知碼

當按鈕失去鍵盤焦點時傳送。 此按鈕必須有 [**BS \_ 通知**](button-styles.md) 樣式才能傳送此通知碼。

按鈕的父視窗會透過 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息接收此通知碼。


```C++
BN_KILLFOCUS

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))包含按鈕的控制項識別碼。 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))會指定通知碼。

</dd> <dt>

*lParam* 
</dt> <dd>

按鈕的控制碼。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[BN \_ SETFOCUS](bn-setfocus.md)
</dt> </dl>

 


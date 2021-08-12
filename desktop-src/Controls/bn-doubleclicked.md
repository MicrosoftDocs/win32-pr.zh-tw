---
title: 'BN_DOUBLECLICKED (Winuser 的通知碼) '
description: BN_DOUBLECLICKED 通知碼-當使用者按兩下按鈕時傳送。
ms.assetid: 2fd7363a-5a02-453c-bfab-df5cbf8e42a5
keywords:
- BN_DOUBLECLICKED 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- BN_DOUBLECLICKED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ce43cebee93516f929f9a763c14dd51d9d486470eeb93818b9605c3f23a1914
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118674122"
---
# <a name="bn_doubleclicked-notification-code"></a>BN \_ DOUBLECLICKED 通知碼

當使用者按兩下按鈕時傳送。 系統會自動為 [**BS \_ USERBUTTON**](button-styles.md)、 [**BS \_ 單選**](button-styles.md)按鈕和 [**BS \_ OWNERDRAW**](button-styles.md) 按鈕傳送此通知碼。 其他按鈕類型只有在 \_ 有 [**BS \_ 通知**](button-styles.md) 樣式時，才會傳送 BN DOUBLECLICKED。

按鈕的父視窗會透過 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息接收此通知碼。


```C++
BN_DOUBLECLICKED

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

## <a name="remarks"></a>備註

BN \_ DOUBLECLICKED 與 [BN \_ DBLCLK](bn-dblclk.md) 通知碼相同。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



 


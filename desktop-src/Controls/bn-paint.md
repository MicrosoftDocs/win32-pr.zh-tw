---
title: 'BN_PAINT (Winuser 的通知碼) '
description: 在應繪製按鈕時傳送。
ms.assetid: 1c742272-60bb-42f1-a9b3-974e9a8540cd
keywords:
- BN_PAINT 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- BN_PAINT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b4c3a412dac84fb5e65c7feb652588d6f16af0f49a8f61723ba48447dbbb2b7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119827598"
---
# <a name="bn_paint-notification-code"></a>BN \_ 油漆通知碼

在應繪製按鈕時傳送。

> [!Note]  
> 此通知碼僅提供給3.0 版之前 Windows 的16位版本相容性。 應用程式應該使用這項工作的 [**BS \_ OWNERDRAW**](button-styles.md) 按鈕樣式和 [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) 結構。

 

按鈕的父視窗會透過 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息接收此通知碼。


```C++
BN_PAINT

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
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



 


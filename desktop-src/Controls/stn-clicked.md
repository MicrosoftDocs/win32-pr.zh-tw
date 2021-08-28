---
title: 'STN_CLICKED (Winuser 的通知碼) '
description: '\_當使用者按一下具有 SS 通知樣式的靜態控制項時，會傳送 STN 點擊通知碼 \_ 。 控制項的父視窗會透過 WM 命令訊息接收此通知碼 \_ 。'
ms.assetid: deeac9e9-c23e-4ffb-a1d7-18782efb7a5c
keywords:
- STN_CLICKED 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- STN_CLICKED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 984bbe63444593707de7e410ebd9cb47fb60bac4766ea6ee57660f034e45924d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119797868"
---
# <a name="stn_clicked-notification-code"></a>STN \_ 按一下通知碼

\_當使用者按一下具有 [**SS \_ 通知**](static-control-styles.md)樣式的靜態控制項時，會傳送 STN 點擊通知碼。 控制項的父視窗會透過 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息接收此通知碼。


```C++
STN_CLICKED

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))包含靜態控制項的識別碼。 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))會指定通知碼。

</dd> <dt>

*lParam* 
</dt> <dd>

靜態控制項的控制碼。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[STN \_ DBLCLK](stn-dblclk.md)
</dt> <dt>

**概念**
</dt> <dt>

[靜態控制項](static-controls.md)
</dt> <dt>

**其他資源**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**WM \_ 命令**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 


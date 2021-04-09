---
title: 'STN_DBLCLK (Winuser 的通知碼) '
description: '\_當使用者按兩下具有 SS 通知樣式的靜態控制項時，會傳送 STN DBLCLK 通知碼 \_ 。 控制項的父視窗會透過 WM 命令訊息接收此通知碼 \_ 。'
ms.assetid: e3203309-87ea-46f4-9269-7e68c6fa0e4a
keywords:
- STN_DBLCLK 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- STN_DBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 853ed5142de99dc85b729b4c4ea208273d4ace1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024797"
---
# <a name="stn_dblclk-notification-code"></a>STN \_ DBLCLK 通知碼

\_當使用者按兩下具有 [**SS \_ 通知**](static-control-styles.md)樣式的靜態控制項時，會傳送 STN DBLCLK 通知碼。 控制項的父視窗會透過 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息接收此通知碼。


```C++
STN_DBLCLK

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
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[STN \_ 按一下](stn-clicked.md)
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

 


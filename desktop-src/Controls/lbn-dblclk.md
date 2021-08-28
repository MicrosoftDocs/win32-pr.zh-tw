---
title: 'LBN_DBLCLK (Winuser 的通知碼) '
description: 通知應用程式，使用者在清單方塊中按兩下某個專案。 清單方塊的父視窗會透過 WM 命令訊息接收此通知碼 \_ 。
ms.assetid: 487282cb-833a-4123-987e-6a417fbd09d4
keywords:
- LBN_DBLCLK 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- LBN_DBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 132e1b68527aca9227702caeea40ffd8deb46e375ffdd87bcf1288dfb01584e1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085308"
---
# <a name="lbn_dblclk-notification-code"></a>LBN \_ DBLCLK 通知碼

通知應用程式，使用者在清單方塊中按兩下某個專案。 清單方塊的父視窗會透過 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息接收此通知碼。


```C++
LBN_DBLCLK

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))包含清單方塊的識別碼。 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))會指定通知碼。

</dd> <dt>

*lParam* 
</dt> <dd>

清單方塊的控制碼。

</dd> </dl>

## <a name="remarks"></a>備註

此通知碼只會由具有 L [**BS \_ 通知**](button-styles.md) 樣式的清單方塊來傳送。

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

[LBN \_ SELCHANGE](lbn-selchange.md)
</dt> <dt>

**其他資源**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**WM \_ 命令**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 


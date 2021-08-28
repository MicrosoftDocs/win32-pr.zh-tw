---
title: 'LBN_SELCHANGE (Winuser 的通知碼) '
description: 通知應用程式，清單方塊中的選取專案已因使用者輸入而變更。 清單方塊的父視窗會透過 WM 命令訊息接收此通知碼 \_ 。
ms.assetid: 126d2c47-816e-4179-a870-f5c5a34c5513
keywords:
- LBN_SELCHANGE 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- LBN_SELCHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ef87aebcf2ce804a10b4682bfaf2cba900bd227a06671959d11babce5f46774
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085178"
---
# <a name="lbn_selchange-notification-code"></a>LBN \_ SELCHANGE 通知碼

通知應用程式，清單方塊中的選取專案已因使用者輸入而變更。 清單方塊的父視窗會透過 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息接收此通知碼。


```C++
LBN_SELCHANGE

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

此通知碼只會由具有 [**磅 \_ 通知**](list-box-styles.md) 樣式的清單方塊來傳送。

如果 [**LB \_ SETSEL**](lb-setsel.md)、 [**LB \_ SETCURSEL**](lb-setcursel.md)、 [**lb \_ SELECTSTRING**](lb-selectstring.md)、 [**lb \_ SELITEMRANGE**](lb-selitemrange.md) 或 [**LB \_ SELITEMRANGEEX**](lb-selitemrangeex.md) message 變更選取專案，則不會傳送此通知碼。

若為多重選取清單方塊， \_ 當使用者按下方向鍵時，即使選取範圍未變更，也會傳送 LBN SELCHANGE 通知碼。

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

[**LB \_ SETCURSEL**](lb-setcursel.md)
</dt> <dt>

[LBN \_ DBLCLK](lbn-dblclk.md)
</dt> <dt>

[LBN \_ SELCANCEL](lbn-selcancel.md)
</dt> <dt>

**其他資源**
</dt> <dt>

[**WM \_ 命令**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 


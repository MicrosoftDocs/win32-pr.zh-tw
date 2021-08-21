---
title: 'WM_SETFOCUS 訊息 (Winuser .h) '
description: 在取得鍵盤焦點之後傳送至視窗。
ms.assetid: 77180e4c-95a6-41a4-93d9-033381ae7543
keywords:
- WM_SETFOCUS 訊息鍵盤和滑鼠輸入
topic_type:
- apiref
api_name:
- WM_SETFOCUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7ba202a4f0205a28d294d2d4f54372921205ebb72516f6f26c4042e08d9cfe2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118757371"
---
# <a name="wm_setfocus-message"></a>WM \_ SETFOCUS 訊息

在取得鍵盤焦點之後傳送至視窗。


```C++
#define WM_SETFOCUS                     0x0007
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

已失去鍵盤焦點的視窗控制碼。 此參數可以是 **Null**。

</dd> <dt>

*lParam* 
</dt> <dd>

不使用這個參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果應用程式處理此訊息，則應該傳回零。

## <a name="remarks"></a>備註

若要顯示插入號，應用程式應該在收到 **WM \_ SETFOCUS** 訊息時呼叫適當的插入號函式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**SetFocus**](/windows/win32/api/winuser/nf-winuser-setfocus)
</dt> <dt>

[**WM \_ KILLFOCUS**](wm-killfocus.md)
</dt> <dt>

**概念**
</dt> <dt>

[鍵盤輸入](keyboard-input.md)
</dt> </dl>

 


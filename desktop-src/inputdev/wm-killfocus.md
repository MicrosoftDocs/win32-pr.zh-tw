---
title: 'WM_KILLFOCUS 訊息 (Winuser .h) '
description: 在失去鍵盤焦點之前，立即傳送至視窗。
ms.assetid: 6d32a09b-a856-4f94-9544-3345b3a700f4
keywords:
- WM_KILLFOCUS 訊息鍵盤和滑鼠輸入
topic_type:
- apiref
api_name:
- WM_KILLFOCUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0e3bba54f2cdb500ba2ba691ffd30419d5beff1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024959"
---
# <a name="wm_killfocus-message"></a>WM \_ KILLFOCUS 訊息

在失去鍵盤焦點之前，立即傳送至視窗。


```C++
#define WM_KILLFOCUS                    0x0008
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

接收鍵盤焦點的視窗控制碼。 此參數可以是 **Null**。

</dd> <dt>

*lParam* 
</dt> <dd>

不使用這個參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果應用程式處理此訊息，則應該傳回零。

## <a name="remarks"></a>備註

如果應用程式顯示插入號，則應該在此時終結插入點。

處理此訊息時，請勿進行任何會顯示或啟動視窗的函式呼叫。 這會導致執行緒產生控制權，而且可能會導致應用程式停止回應訊息。 如需詳細資訊，請參閱 [訊息鎖死](/windows/desktop/winmsg/about-messages-and-message-queues)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**SetFocus**](/windows/win32/api/winuser/nf-winuser-setfocus)
</dt> <dt>

[**WM \_ SETFOCUS**](wm-setfocus.md)
</dt> <dt>

**概念**
</dt> <dt>

[鍵盤輸入](keyboard-input.md)
</dt> </dl>

 


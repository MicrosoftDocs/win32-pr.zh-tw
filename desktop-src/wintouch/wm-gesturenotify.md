---
title: 'WM_GESTURENOTIFY 訊息 (Winuser .h) '
description: 讓您有機會設定手勢設定。
ms.assetid: 83c23928-86ce-421d-bb84-5c41a770bf60
keywords:
- WM_GESTURENOTIFY 訊息 Windows Touch
topic_type:
- apiref
api_name:
- WM_GESTURENOTIFY
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d474f356310a0d7949cecf36e7af9cb586a76029171dfe27c1679970e481ed1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118435234"
---
# <a name="wm_gesturenotify-message"></a>WM \_ GESTURENOTIFY 訊息

讓您有機會設定手勢設定。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

未使用的。

</dd> <dt>

*lParam* 
</dt> <dd>

指向 [**GESTURENOTIFYSTRUCT**](/windows/win32/api/winuser/ns-winuser-gesturenotifystruct)的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

應從 [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca)傳回值。

## <a name="remarks"></a>備註

當收到 **WM \_ GESTURENOTIFY** 訊息時，應用程式可以使用 [**SetGestureConfig**](/windows/desktop/api/winuser/nf-winuser-setgestureconfig) 來指定要接收的手勢。 這則訊息應該一律使用 [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) 函數進行反升。

> [!Note]  
> 處理 **WM \_ GESTURENOTIFY** 訊息將會變更視窗存留期的手勢設定，而不只是下一個手勢。

 

## <a name="examples"></a>範例

下列範例顯示如何啟用所有手勢。 如需更多範例，請參閱 [**SetGestureConfig**](/windows/desktop/api/winuser/nf-winuser-setgestureconfig)。


```C++
    switch (message)
    {
    case WM_GESTURENOTIFY:
        GESTURECONFIG gc = {0,GC_ALLGESTURES,0};
        BOOL bResult = SetGestureConfig(hWnd,0,1,&gc,sizeof(GESTURECONFIG));
            
        if(!bResult)
        {
            // an error
        }
        return DefWindowProc(hWnd, WM_GESTURENOTIFY, wParam, lParam);
    }
      
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                                               |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/>                                                  |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[通知](notifications.md)
</dt> <dt>

[Windows觸控手勢程式設計指南](guide-multi-touch-gestures.md)
</dt> <dt>

[**GESTURENOTIFYSTRUCT**](/windows/win32/api/winuser/ns-winuser-gesturenotifystruct)
</dt> <dt>

[**SetGestureConfig**](/windows/desktop/api/winuser/nf-winuser-setgestureconfig)
</dt> </dl>

 


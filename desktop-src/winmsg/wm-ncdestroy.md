---
description: 通知視窗，其非工作區已被終結。 DestroyWindow 函式會將 WM \_ NCDESTROY 訊息傳送至位於 wm 損毀訊息之後的視窗 \_ 。
ms.assetid: 64ab268d-0e90-4401-81d3-a4da64196001
title: 'WM_NCDESTROY 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a2e74db0abf22fc2fb3d2a16b5cc63187514d1bee26079490c8d19eae13787e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118200044"
---
# <a name="wm_ncdestroy-message"></a>WM \_ NCDESTROY 訊息

通知視窗，其非工作區已被終結。 [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow)函式會將 **wm \_ NCDESTROY** 訊息傳送至位於 wm 損 [**\_ 毀**](wm-destroy.md)訊息之後的視窗。[**使用 \_ WM**](wm-destroy.md)終結來釋放與視窗相關聯的配置記憶體物件。

當子視窗終結之後，會傳送 **WM \_ NCDESTROY** 訊息。 相反地，在子視窗終結之前，會先傳送 [**WM \_ 摧毀**](wm-destroy.md) 。

視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。


```C++
#define WM_NCDESTROY                    0x0082
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

不使用這個參數。

</dd> <dt>

*lParam* 
</dt> <dd>

不使用這個參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **LRESULT**

如果應用程式處理此訊息，它應該會傳回零。

## <a name="remarks"></a>備註

此訊息會釋出任何內部配置給視窗的記憶體。

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

[**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow)
</dt> <dt>

[**WM 損 \_ 毀**](wm-destroy.md)
</dt> <dt>

[**WM \_ NCCREATE**](wm-nccreate.md)
</dt> <dt>

**概念**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 

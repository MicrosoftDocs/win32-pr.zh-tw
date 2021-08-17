---
description: 應用程式會將 WM \_ MDIACTI加值稅E 訊息傳送至多重文件介面 (MDI) 用戶端視窗，以指示用戶端視窗啟用不同的 MDI 子視窗。
ms.assetid: c5de18b5-fac3-4e55-9eca-3b6672df0e7b
title: 'WM_MDIACTI加值稅E 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e8b71e0f3755d76ecb44d60eecbd3b92c124aa59339a6fbf59a098b1eeb274f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119931268"
---
# <a name="wm_mdiactivate-message"></a>WM \_ MDIACTI加值稅E 訊息

應用程式會將 **WM \_ MDIACTI加值稅E** 訊息傳送至多重文件介面 (MDI) 用戶端視窗，以指示用戶端視窗啟用不同的 MDI 子視窗。


```C++
#define WM_MDIACTIVATE                  0x0222
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

要啟用之 MDI 子視窗的控制碼。

</dd> <dt>

*lParam* 
</dt> <dd>

不使用這個參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **LRESULT**

如果應用程式將此訊息傳送至 MDI 用戶端視窗，則傳回值為零。

如果 MDI 子視窗處理此訊息，則應該傳回零。

## <a name="remarks"></a>備註

當用戶端視窗處理此訊息時，它會將 **WM \_ MDIACTI加值稅E** 傳送至已停用的子視窗，以及要啟用的子視窗。 MDI 子視窗所收到的訊息參數如下所示：

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

要停用之 MDI 子視窗的控制碼。

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

要啟用之 MDI 子視窗的控制碼。

</dd> </dl>

Mdi 子視窗會獨立于 MDI 框架視窗之外啟用。 當框架視窗變成作用中時，上次使用 **wm \_ MDIACTI加值稅E** 訊息啟動的子視窗會收到 [**WM \_ NCACTI加值稅E**](wm-ncactivate.md) 訊息，以繪製活動視窗框架和標題列，而子視窗則不會接收另一個 **WM \_ MDIACTI加值稅E** 訊息。

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

[**WM \_ MDIGETACTIVE**](wm-mdigetactive.md)
</dt> <dt>

[**WM \_ MDINEXT**](wm-mdinext.md)
</dt> <dt>

[**WM \_ NCACTI加值稅E**](wm-ncactivate.md)
</dt> <dt>

**概念**
</dt> <dt>

[多個檔介面](multiple-document-interface.md)
</dt> </dl>

 

 





---
title: 'DM_SETDEFID 訊息 (Winuser .h) '
description: 變更對話方塊的預設按鈕的識別碼。
ms.assetid: 30720fa1-48cb-42d4-8370-87bdbaa34600
keywords:
- DM_SETDEFID 訊息對話方塊
topic_type:
- apiref
api_name:
- DM_SETDEFID
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92749cc7eca569b57d239a36bb6559e59a6a7ebc31c63787a93d0720b334d1ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119741748"
---
# <a name="dm_setdefid-message"></a>DM \_ SETDEFID 訊息

變更對話方塊的預設按鈕的識別碼。


```C++
#define WM_USER              0x0400
#define DM_SETDEFID         (WM_USER+1)
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

將成為預設值的按鈕控制項識別碼。

</dd> <dt>

*lParam* 
</dt> <dd>

不使用這個參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值一律為 **TRUE**。

## <a name="remarks"></a>備註

此訊息是由 [**DefDlgProc**](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw) 函數處理。 若要設定預設的推播按鈕，函式可以將 [**WM \_ GETDLGCODE**](wm-getdlgcode.md) 和 [**BM \_ >setstyle**](../controls/bm-setstyle.md) 訊息傳送至指定的控制項和目前的預設推送按鈕。

使用 **DM \_ SETDEFID** 訊息可能會導致出現一個以上的按鈕，使其具有預設的推播按鈕狀態。 當系統顯示對話方塊時，它會在對話方塊範本中繪製具有預設狀態框線的第一個 push 按鈕。 傳送 **DM \_ SETDEFID** 訊息來變更預設按鈕，並不一定會從第一個 push 按鈕移除預設狀態框線。 在這些情況下，應用程式應該傳送 [**BM \_ >setstyle**](../controls/bm-setstyle.md) 訊息來變更第一個 push 按鈕框線樣式。

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

[**DefDlgProc**](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw)
</dt> <dt>

[**DM \_ GETDEFID**](dm-getdefid.md)
</dt> <dt>

[**WM \_ GETDLGCODE**](wm-getdlgcode.md)
</dt> <dt>

**概念**
</dt> <dt>

[對話方塊](dialog-boxes.md)
</dt> <dt>

**其他資源**
</dt> <dt>

[**BM \_ >SETSTYLE**](../controls/bm-setstyle.md)
</dt> <dt>

[**EM \_ SETLIMITTEXT**](../controls/em-setlimittext.md)
</dt> </dl>

 


---
title: 'WM_SETHOTKEY 訊息 (Winuser .h) '
description: 傳送至視窗，以將熱鍵與視窗相關聯。 當使用者按下快速鍵時，系統會啟動視窗。
ms.assetid: b2c7e6ca-da71-440b-a05e-17f2da419d18
keywords:
- WM_SETHOTKEY 訊息鍵盤和滑鼠輸入
topic_type:
- apiref
api_name:
- WM_SETHOTKEY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7ed27a91ddf9506cd12b988db4bd141a988c13e
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "103696296"
---
# <a name="wm_sethotkey-message"></a>WM \_ SETHOTKEY 訊息

傳送至視窗，以將熱鍵與視窗相關聯。 當使用者按下快速鍵時，系統會啟動視窗。


```C++
#define WM_SETHOTKEY                    0x0032
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

低序位字組可指定要與視窗相關聯的虛擬按鍵碼。

高序位單字可以是 CommCtrl 中的一或多個下列值。

將 *wParam* 設定為 **Null** ，就會移除與視窗相關聯的快速鍵。



| 值                                                                                                                                                                                                                         | 意義                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span id="HOTKEYF_ALT"></span><span id="hotkeyf_alt"></span><dl> <dt>**HOTKEYF \_ALT**</dt> <dt>0x04</dt> </dl>             | ALT 鍵<br/>      |
| <span id="HOTKEYF_CONTROL"></span><span id="hotkeyf_control"></span><dl> <dt>**HOTKEYF \_控制**</dt> <dt>0x02</dt> </dl> | CTRL 鍵<br/>     |
| <span id="HOTKEYF_EXT"></span><span id="hotkeyf_ext"></span><dl> <dt>**HOTKEYF \_EXT**</dt> <dt>0x08</dt> </dl>             | 擴充金鑰<br/> |
| <span id="HOTKEYF_SHIFT"></span><span id="hotkeyf_shift"></span><dl> <dt>**HOTKEYF \_SHIFT**</dt> <dt>0x01</dt> </dl>       | SHIFT 鍵<br/>    |



 

</dd> <dt>

*lParam* 
</dt> <dd>

不使用這個參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值是下列其中一項。



| 傳回值                                                                  | 描述                                                                             |
|-------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <dl> <dt>-1</dt> </dl> | 函數不成功;快速鍵無效。<br/>                        |
| <dl> <dt>0</dt> </dl>  | 函數不成功;視窗無效。<br/>                         |
| <dl> <dt>1</dt> </dl>  | 函式成功，而且沒有其他視窗具有相同的快速鍵。<br/>        |
| <dl> <dt>2</dt> </dl>  | 函式成功，但另一個視窗已經有相同的快速鍵。<br/> |



 

## <a name="remarks"></a>備註

快速鍵無法與子視窗相關聯。

**VK \_[ESCAPE**]、[ **VK \_ SPACE**] 和 [ **VK \_ ]** 索引標籤都是不正確快速鍵。

當使用者按下快速鍵時，系統會產生一個 *wParam* 等於 **SC \_ 熱鍵** 的 [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand)訊息，而 *lParam* 等於視窗的控制碼。 如果將此訊息傳遞至 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)，系統會將視窗的最後一個作用中快顯 (（如果有的話）) 或視窗本身 (如果前景沒有快顯視窗) 。

一個視窗只能有一個快速鍵。 如果視窗已經有與其相關聯的熱鍵，則新的熱鍵會取代舊的金鑰。 如果有一個以上的視窗具有相同的熱鍵，則由熱鍵啟動的視窗是隨機的。

這些快速鍵與 [**RegisterHotKey**](/windows/win32/api/winuser/nf-winuser-registerhotkey)所設定的快速鍵無關。

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

[**RegisterHotKey**](/windows/win32/api/winuser/nf-winuser-registerhotkey)
</dt> <dt>

[**WM \_ GETHOTKEY**](wm-gethotkey.md)
</dt> <dt>

[**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

**概念**
</dt> <dt>

[鍵盤輸入](keyboard-input.md)
</dt> </dl>

 


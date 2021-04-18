---
title: 'WM_GETDLGCODE 訊息 (Winuser .h) '
description: 傳送至與控制項相關聯的視窗程式。
ms.assetid: 96d2caee-be6e-46e9-98b3-bffc3af1c003
keywords:
- WM_GETDLGCODE 訊息對話方塊
topic_type:
- apiref
api_name:
- WM_GETDLGCODE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89d6e1ddb3be21e227c4dad404a06113f5c50a49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966130"
---
# <a name="wm_getdlgcode-message"></a>WM \_ GETDLGCODE 訊息

傳送至與控制項相關聯的視窗程式。 根據預設，系統會處理所有鍵盤輸入至控制項;系統會將特定類型的鍵盤輸入視為對話方塊流覽鍵。 若要覆寫此預設行為，控制項可以回應 **WM \_ GETDLGCODE** 訊息，以指出它所要處理的輸入類型。


```C++
#define WM_GETDLGCODE                   0x0087
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

使用者按下的虛擬機器碼，會提示 Windows 發出此通知。 處理常式必須選擇性地處理這些金鑰。 例如，處理常式可能會接受並處理 **VK \_** 傳回，但是會將 [ **VK \_ ]** 索引標籤委派給擁有者視窗。 如需值清單，請參閱 [**虛擬機器碼程式碼**](/windows/desktop/inputdev/virtual-key-codes)。

</dd> <dt>

*lParam* 
</dt> <dd>

訊息 [**結構的**](/windows/win32/api/winuser/ns-winuser-msg) 指標 (如果系統正在執行查詢) ，則為 **Null** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值是下列其中一個或多個值，指出應用程式處理的輸入類型。



| 傳回碼/值                                                                                                                                                | Description                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**DLGC \_按鈕**</dt> <dt>0x2000</dt> </dl>          | 按鈕。<br/>                                                                                                         |
| <dl> <dt>**DLGC \_DEFPUSHBUTTON**</dt> <dt>0x0010</dt> </dl>   | 預設的 [推送] 按鈕。<br/>                                                                                            |
| <dl> <dt>**DLGC \_HASSETSEL**</dt> <dt>0x0008</dt> </dl>       | [**EM \_SETSEL**](/windows/desktop/Controls/em-setsel) 訊息。<br/>                                                           |
| <dl> <dt>**DLGC \_選項按鈕**</dt> <dt>0x0040</dt> </dl>     | 選項按鈕。<br/>                                                                                                   |
| <dl> <dt>**DLGC \_靜態**</dt> <dt>0x0100</dt> </dl>          | 靜態控制項。<br/>                                                                                                 |
| <dl> <dt>**DLGC \_UNDEFPUSHBUTTON**</dt> <dt>0x0020</dt> </dl> | 非預設的推送按鈕。<br/>                                                                                        |
| <dl> <dt>**DLGC \_WANTALLKEYS**</dt> <dt>0x0004</dt> </dl>     | 所有鍵盤輸入。<br/>                                                                                             |
| <dl> <dt>**DLGC \_WANTARROWS**</dt> <dt>0x0001</dt> </dl>      | 方向按鍵。<br/>                                                                                                 |
| <dl> <dt>**DLGC \_WANTCHARS**</dt> <dt>0x0080</dt> </dl>       | [**WM \_CHAR**](/windows/desktop/inputdev/wm-char) 訊息。<br/>                                                                      |
| <dl> <dt>**DLGC \_WANTMESSAGE**</dt> <dt>0x0004</dt> </dl>     | 所有鍵盤輸入 (應用程式 [**都會將訊息結構中**](/windows/win32/api/winuser/ns-winuser-msg) 的這個訊息傳遞給控制項) 。<br/> |
| <dl> <dt>**DLGC \_WANTTAB**</dt> <dt>0x0002</dt> </dl>         | TAB 鍵。<br/>                                                                                                        |



 

## <a name="remarks"></a>備註

雖然 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式一律會傳回零以回應 **WM \_ GETDLGCODE** 訊息，但預先定義之控制項類別的視窗程式會傳回適用于每個類別的程式碼。

只有使用者定義的對話方塊控制項或子類別修改的標準控制項，才能使用 **WM \_ GETDLGCODE** 訊息和傳回的值。

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

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**EM \_ SETSEL**](/windows/desktop/Controls/em-setsel)
</dt> <dt>

[**味精**](/windows/win32/api/winuser/ns-winuser-msg)
</dt> <dt>

[**WM \_ 字元**](/windows/desktop/inputdev/wm-char)
</dt> <dt>

**概念**
</dt> <dt>

[對話方塊](dialog-boxes.md)
</dt> </dl>

 


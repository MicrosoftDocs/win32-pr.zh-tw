---
description: 將對應至視窗的文字複製到呼叫端所提供的緩衝區。
ms.assetid: 117c3d6d-24cd-462f-bdb0-b65d8914273a
title: 'WM_GETTEXT 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3e1bc6a8a77c51b3ab5b84f5cce700e65b180b357c932b4044a2b65cb49fc8e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089888"
---
# <a name="wm_gettext-message"></a>WM \_ GETTEXT 訊息

將對應至視窗的文字複製到呼叫端所提供的緩衝區。


```C++
#define WM_GETTEXT                      0x000D
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

要複製的字元數上限，包括結束的 null 字元。

ANSI 應用程式可能會將緩衝區中的字串縮減 (為 *wParam* 值的最小值一半，) 因為從 ANSI 轉換成 Unicode。

</dd> <dt>

*lParam* 
</dt> <dd>

要接收文字之緩衝區的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **LRESULT**

傳回值是複製的字元數，不包括終止的 null 字元。

## <a name="remarks"></a>備註

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)函式會將與視窗相關聯的文字複製到指定的緩衝區，並傳回復制的字元數。 請注意，對於非文字靜態控制項，這會提供您原先建立控制項的文字，也就是 ID 編號。 不過，它會提供您原本建立之非文字靜態控制項的識別碼。 也就是說，如果您之後使用了 **STM \_ SETIMAGE** 來變更它，仍會傳回原始識別碼。

若為編輯控制項，要複製的文字是編輯控制項的內容。 在下拉式方塊中，文字是編輯控制項的內容 (或下拉式方塊的靜態文字) 部分。 若為按鈕，文字就是按鈕名稱。 若為其他視窗，則文字為視窗標題。 若要在清單方塊中複製專案的文字，應用程式可以使用 [**LB \_ GETTEXT**](../controls/lb-gettext.md) 訊息。

將 **WM \_ GETTEXT** 訊息傳送至具有 **SS \_ 圖示** 樣式的靜態控制項時，會在 *lParam* 所指向之緩衝區的前四個位元組中傳回圖示的控制碼。 只有在使用 [**WM \_ SETTEXT**](wm-settext.md) 訊息來設定圖示時，才會發生此情況。

**Rich Edit：** 如果要複製的文字超過64K，請使用 [**em \_ STREAMOUT**](../controls/em-streamout.md) 或 [**em \_ GETSELTEXT**](../controls/em-getseltext.md) 訊息。

將 **WM \_ GETTEXT** 訊息傳送至非文字靜態控制項（例如靜態點陣圖或靜態圖示控制項）時，不會傳回字串值。 相反地，它會傳回零。 此外，在舊版的 Windows 中，應用程式可以將 **WM \_ GETTEXT** 訊息傳送至非文字靜態控制項，以取得控制項的識別碼。 若要抓取控制項的識別碼，應用程式可以使用 [**GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga)傳遞 **GWL \_ 識別碼** 作為索引值，或使用 **GWLP \_ 識別碼** 來 [**GetWindowLongPtr**](/windows/win32/api/winuser/nf-winuser-getwindowlongptra) 。

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

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga)
</dt> <dt>

[**GetWindowLongPtr**](/windows/win32/api/winuser/nf-winuser-getwindowlongptra)
</dt> <dt>

[**GetWindowText**](/windows/win32/api/winuser/nf-winuser-getwindowtexta)
</dt> <dt>

[**GetWindowTextLength**](/windows/win32/api/winuser/nf-winuser-getwindowtextlengtha)
</dt> <dt>

[**WM \_ GETTEXTLENGTH**](wm-gettextlength.md)
</dt> <dt>

[**WM \_ SETTEXT**](wm-settext.md)
</dt> <dt>

**概念**
</dt> <dt>

[Windows](windows.md)
</dt> <dt>

**其他資源**
</dt> <dt>

[**EM \_ GETSELTEXT**](../controls/em-getseltext.md)
</dt> <dt>

[**EM \_ STREAMOUT**](../controls/em-streamout.md)
</dt> <dt>

[**LB \_ GETTEXT**](../controls/lb-gettext.md)
</dt> </dl>

 

 

---
title: 'WM_KEYDOWN 訊息 (Winuser .h) '
description: 當按下非系統鍵時，將鍵盤焦點張貼至視窗。 非系統機碼是未按下 ALT 鍵時所按下的按鍵。
ms.assetid: 0e37149f-445c-4b20-ad68-fdf39428ac91
keywords:
- WM_KEYDOWN 訊息鍵盤和滑鼠輸入
topic_type:
- apiref
api_name:
- WM_KEYDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: ee6dc21b4fb90f0d02e80fce8ce6cc17099a0547
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996065"
---
# <a name="wm_keydown-message"></a>WM \_ KEYDOWN 訊息

當按下非系統鍵時，將鍵盤焦點張貼至視窗。 非系統機碼是未按下 ALT 鍵時所按下的按鍵。


```C++
#define WM_KEYDOWN                      0x0100
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

非系統索引鍵的虛擬機器碼程式碼。 請參閱 [虛擬金鑰代碼](virtual-key-codes.md)。

</dd> <dt>

*lParam* 
</dt> <dd>

重複計數、掃描程式碼、擴充按鍵旗標、內容程式碼、先前的索引鍵狀態旗標和轉換狀態旗標，如下所示。



| Bits  | 意義                                                                                                                                                                                                                                                               |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0-15  | 目前訊息的重複計數。 值是當使用者按住按鍵時，按鍵 autorepeated 的次數。 如果按鍵夠長，則會傳送多則訊息。 不過，重複計數不是累計的。 |
| 16-23 | 掃描程式碼。 此值取決於 OEM。                                                                                                                                                                                                                          |
| 24    | 指出機碼是否為擴充的索引鍵，例如出現在增強型101或102按鍵鍵盤上的右手 ALT 和 CTRL 鍵。 如果它是擴充索引鍵，則此值為 1;否則，它是0。                                                              |
| 25-28 | 保護請勿使用。                                                                                                                                                                                                                                                 |
| 29    | 內容程式碼。 若為 **WM 的 \_ KEYDOWN** 訊息，此值一律為0。                                                                                                                                                                                                |
| 30    | 先前的金鑰狀態。 如果在傳送訊息之前，金鑰已關閉，則值為1，如果索引鍵已啟動，則為零。                                                                                                                                                 |
| 31    | 轉換狀態。 若為 **WM 的 \_ KEYDOWN** 訊息，此值一律為0。                                                                                                                                                                                            |

如需詳細資訊，請參閱 [按鍵訊息旗標](about-keyboard-input.md#keystroke-message-flags)。
 

</dd> </dl>

## <a name="return-value"></a>傳回值

如果應用程式處理此訊息，則應該傳回零。

## <a name="example"></a>範例

```cpp
LRESULT CALLBACK HostWndProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    switch (message) 
    {
    case WM_KEYDOWN:
        if (wParam == VK_ESCAPE)
        {
            if (isFullScreen) 
            {
                GoPartialScreen();
            }
        }
        break;

    // ...
    default:
        return DefWindowProc(hWnd, message, wParam, lParam);
    }
    return 0;  
}

```

從 GitHub 上的 [Windows 傳統範例](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Magnification/cpp/Windowed/MagnifierSample.cpp) 取得的範例。


## <a name="remarks"></a>備註

如果按下 F10 鍵， [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式會設定內部旗標。 當 **DefWindowProc** 收到 [**WM \_ KEYUP**](wm-keyup.md) 訊息時，此函式會檢查是否已設定內部旗標，如果是，則會將 [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) 訊息傳送至最上層視窗。 訊息的 **WM \_ SYSCOMMAND** 參數設定為 SC \_ KEYMENU。

由於 autorepeat 功能的不同，在發送 [**wm \_ KEYUP**](wm-keyup.md)訊息之前，可能會公佈一個以上的 **wm \_ KEYDOWN** 訊息。 先前的金鑰狀態 (位 30) 可用來判斷 **WM \_ KEYDOWN** 訊息是否表示第一個向下轉換或重複的轉換。

針對增強的101和102鍵鍵盤，擴充的按鍵是鍵盤主要區段上的右 ALT 和 CTRL 鍵;位於數位鍵台左邊的叢集中的 INS、DEL、HOME、END、PAGE UP、PAGE DOWN 和方向鍵;並將 (/) ，然後在數位鍵台中輸入按鍵。 其他鍵盤可能會在 *lParam* 參數中支援擴充金鑰位。

應用程式必須將 *wParam* 傳遞至 [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) ，而不需要加以變更。

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

[**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage)
</dt> <dt>

[**WM \_ 字元**](wm-char.md)
</dt> <dt>

[**WM \_ KEYUP**](wm-keyup.md)
</dt> <dt>

[**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

**概念**
</dt> <dt>

[鍵盤輸入](keyboard-input.md)
</dt> </dl>

 


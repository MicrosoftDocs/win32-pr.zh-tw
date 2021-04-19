---
title: 'WM_CHAR 訊息 (Winuser .h) '
description: 在 TranslateMessage 函式轉譯了 WM KEYDOWN 訊息時，以鍵盤焦點張貼至視窗 \_ 。 WM \_ 字元訊息包含已按下之按鍵的字元碼。
ms.assetid: 7e45dc6f-ff68-4534-9e52-46e5f4110532
keywords:
- WM_CHAR 訊息鍵盤和滑鼠輸入
topic_type:
- apiref
api_name:
- WM_CHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/28/2020
ms.openlocfilehash: 8d174f64fa776b506814540d4f2c97635fba38a1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977724"
---
# <a name="wm_char-message"></a>WM \_ 字元訊息

在 [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage)函式轉譯了 [**WM \_ KEYDOWN**](wm-keydown.md)訊息時，以鍵盤焦點張貼至視窗。 **WM \_ 字元** 訊息包含已按下之按鍵的字元碼。


```C++
#define WM_CHAR                         0x0102
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

按鍵的字元碼。

</dd> <dt>

*lParam* 
</dt> <dd>

[重複計數]、[掃描程式碼]、[擴充按鍵旗標]、[內容程式碼]、先前的索引鍵狀態旗標和轉換狀態旗標，如下表所示。



| Bits  | 意義                                                                                                                                                                                                                                                               |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0-15  | 目前訊息的重複計數。 值是當使用者按住按鍵時，按鍵 autorepeated 的次數。 如果按鍵夠長，則會傳送多則訊息。 不過，重複計數不是累計的。 |
| 16-23 | 掃描程式碼。 此值取決於 OEM。                                                                                                                                                                                                                          |
| 24    | 指出機碼是否為擴充的索引鍵，例如出現在增強型101或102按鍵鍵盤上的右手 ALT 和 CTRL 鍵。 如果它是擴充索引鍵，則此值為 1;否則，它是0。                                                              |
| 25-28 | 保護請勿使用。                                                                                                                                                                                                                                                 |
| 29    | 內容程式碼。 如果按下按鍵時按住 ALT 鍵，則此值為 1;否則，此值為0。                                                                                                                                                     |
| 30    | 先前的金鑰狀態。 如果在傳送訊息之前，金鑰已關閉，則此值為 1; 如果金鑰已啟動，則為0。                                                                                                                                                    |
| 31    | 轉換狀態。 如果正在釋放金鑰，則值為1，如果正在按下索引鍵，則為0。                                                                                                                                                            |

如需詳細資訊，請參閱 [按鍵訊息旗標](about-keyboard-input.md#keystroke-message-flags)。
 

</dd> </dl>

## <a name="return-value"></a>傳回值

如果應用程式處理此訊息，則應該傳回零。

## <a name="example"></a>範例

```cpp
LRESULT CALLBACK WndProc(HWND hwnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    switch (message)
    {
   
    // ...

    case WM_CHAR:
        OnKeyPress(wParam);
        break;

    default:
        return DefWindowProc(hwnd, message, wParam, lParam);
    }
    return 0;
}
```
從 GitHub 上的 [Windows 傳統範例](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/multimedia/mediafoundation/protectedplayback/winmain.cpp) 取得的範例。

## <a name="remarks"></a>備註

**WM \_ 字元** 訊息使用 Unicode 轉換格式 (utf-16) -16。

在按下的按鍵和產生的字元訊息之間不一定會有一對一的對應，因此 *lParam* 參數的高序位字中的資訊通常對應用程式而言並不有用。 高序位字組中的資訊僅適用于在 **wm \_ 字元** 訊息張貼之前的最新 [**wm \_ KEYDOWN**](wm-keydown.md)訊息。

針對增強的101和102鍵鍵盤，擴充的按鍵是鍵盤主要區段上的右 ALT 和右 CTRL 鍵;位於數位鍵台左邊的叢集中的 INS、DEL、HOME、END、PAGE UP、PAGE DOWN 和方向鍵;並將 (/) ，然後在數位鍵台中輸入按鍵。 有些其他鍵盤可能會支援 *lParam* 參數中的擴充金鑰位。

[**Wm \_ 則 unichar 會**](wm-unichar.md)訊息與 **wm \_ CHAR** 相同，但它使用 32 utf-16。 其設計目的是要將 Unicode 字元傳送或張貼至 ANSI 視窗，並且可以處理 Unicode 補充平面字元。

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

[**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage)
</dt> <dt>

[**WM \_ KEYDOWN**](wm-keydown.md)
</dt> <dt>

[**WM \_ 則 UNICHAR 會**](wm-unichar.md)
</dt> <dt>

**概念**
</dt> <dt>

[鍵盤輸入](keyboard-input.md)
</dt> </dl>

 


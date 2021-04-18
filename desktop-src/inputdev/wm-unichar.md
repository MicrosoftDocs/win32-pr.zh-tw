---
title: 'WM_UNICHAR 訊息 (Winuser .h) '
description: '\_應用程式可以使用 WM 則 unichar 會訊息，將輸入張貼到其他視窗。'
ms.assetid: edbfcf14-0371-43ce-9676-eb10d964d0b7
keywords:
- WM_UNICHAR 訊息鍵盤和滑鼠輸入
topic_type:
- apiref
api_name:
- WM_UNICHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 833b5cb59095f5aecc8c0172857c8761fd92449a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965302"
---
# <a name="wm_unichar-message"></a>WM \_ 則 unichar 會訊息

應用程式可以使用 **WM \_ 則 unichar 會** 訊息，將輸入張貼到其他視窗。 此訊息包含已按下之按鍵的字元碼。  (測試目標應用程式是否能藉由傳送 *wParam* 設定為 **UNICODE \_ NOCHAR** 的訊息，來處理 **WM \_ 則 unichar 會** 訊息。 ) 


```C++
#define WM_UNICHAR                      0x0109
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

按鍵的字元碼。

如果 *wParam* 是 **UNICODE \_ NOCHAR** ，而且應用程式會處理此訊息，則傳回 **TRUE**。 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)函式會傳回 **FALSE** (預設) 。

如果 *wParam* 不是 **UNICODE \_ NOCHAR**，則傳回 **FALSE**。 Unicode  [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 會使用相同的參數張貼 [**WM \_ 字元**](wm-char.md) 訊息，而 ANSI **DefWindowProc** 函式會使用對應的 ANSI 字元 (s) 來張貼一或兩個 **wm \_ 字元** 訊息。

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

## <a name="remarks"></a>備註

**Wm \_ 則 unichar 會** 訊息類似于 [**wm \_ 字元**](wm-char.md)，但它使用 Unicode 轉換格式 (Utf-16) -32，而 **WM \_ 字元** 使用 utf-16。

此訊息的設計目的是要將 Unicode 字元傳送或張貼至 ANSI 視窗，並且可以處理 Unicode 補充平面字元。

因為所按下的按鍵和產生的字元訊息之間不一定要有一對一的對應，所以 *lParam* 參數的高序位字中的資訊通常對應用程式而言並不有用。 高序位字組中的資訊只適用于在 **\_ 則 unichar 會** 訊息張貼之前的最新 wm 的一則的 [**wm \_**](wm-keydown.md)訊息。

針對增強的101和102鍵鍵盤，擴充的按鍵是鍵盤主要區段上的右 ALT 和右 CTRL 鍵;位於數位鍵台左邊的叢集中的 INS、DEL、HOME、END、PAGE UP、PAGE DOWN 和方向鍵;並將 (/) ，然後在數位鍵台中輸入按鍵。 有些其他鍵盤可能會支援 *lParam* 參數中的擴充金鑰位。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage)
</dt> <dt>

[**WM \_ 字元**](wm-char.md)
</dt> <dt>

[**WM \_ KEYDOWN**](wm-keydown.md)
</dt> <dt>

**概念**
</dt> <dt>

[鍵盤輸入](keyboard-input.md)
</dt> </dl>

 


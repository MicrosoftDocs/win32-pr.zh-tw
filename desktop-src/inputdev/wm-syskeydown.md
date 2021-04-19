---
title: 'WM_SYSKEYDOWN 訊息 (Winuser .h) '
description: 當使用者按下 F10 (鍵時，以鍵盤焦點張貼至視窗) 或按住 ALT 鍵，然後按下另一個按鍵。
ms.assetid: a3c03dbf-1be7-49ff-b931-1981786b74ce
keywords:
- WM_SYSKEYDOWN 訊息鍵盤和滑鼠輸入
topic_type:
- apiref
api_name:
- WM_SYSKEYDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3053c5933a0388e3c8522b0d7201b491aaa4fa2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967538"
---
# <a name="wm_syskeydown-message"></a>WM \_ SYSKEYDOWN 訊息

當使用者按下 F10 (鍵時，以鍵盤焦點張貼至視窗) 或按住 ALT 鍵，然後按下另一個按鍵。 當目前沒有任何視窗具有鍵盤焦點時，也會發生此問題。在此情況下，會將 **WM \_ SYSKEYDOWN** 訊息傳送至使用中視窗。 接收訊息的視窗可以藉由檢查 *lParam* 參數中的內容程式碼來區分這兩個內容。


```C++
#define WM_SYSKEYDOWN                   0x0104
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

所按下之按鍵的虛擬按鍵碼。 請參閱 [**虛擬金鑰代碼**](virtual-key-codes.md)。

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
| 29    | 內容程式碼。 如果在按下按鍵時，ALT 鍵已關閉，則此值為 1;如果將 **WM \_ SYSKEYDOWN** 訊息張貼至使用中視窗，因為沒有視窗具有鍵盤焦點，則為0。                                                                  |
| 30    | 先前的金鑰狀態。 如果在傳送訊息之前，金鑰已關閉，則此值為 1; 如果金鑰已啟動，則為0。                                                                                                                                                    |
| 31    | 轉換狀態。 **WM \_ SYSKEYDOWN** 訊息的值一律為0。                                                                                                                                                                                         |

如需詳細資訊，請參閱 [按鍵訊息旗標](about-keyboard-input.md#keystroke-message-flags)。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果應用程式處理此訊息，則應該傳回零。

## <a name="remarks"></a>備註

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)函式會檢查指定的索引鍵，並在索引鍵為 TAB 或 ENTER 時產生 [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand)訊息。

當內容程式碼為零時，訊息可以傳遞至 [**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) 函式，它會處理它，就像是一般的索引鍵訊息，而非字元索引鍵訊息一樣。 這可讓快速鍵與使用中視窗搭配使用，即使使用中視窗沒有鍵盤焦點也一樣。

因為會自動重複，所以在傳送 [**wm \_ SYSKEYUP**](wm-syskeyup.md)訊息之前可能會發生一個以上的 **WM \_ SYSKEYDOWN** 訊息。 先前的金鑰狀態 (位 30) 可用來判斷 **WM \_ SYSKEYDOWN** 訊息是否表示第一個向下轉換或重複的轉換。

針對增強的101和102鍵鍵盤，增強型按鍵是鍵盤主要區段上的右 ALT 和 CTRL 鍵;位於數位鍵台左邊的叢集中的 INS、DEL、HOME、END、PAGE UP、PAGE DOWN 和方向鍵;並將 (/) ，然後在數位鍵台中輸入按鍵。 其他鍵盤可能會在 *lParam* 參數中支援擴充金鑰位。

當使用者按下 F10 鍵而沒有 ALT 鍵時，也會傳送此訊息。

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

[**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora)
</dt> <dt>

[**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

[**WM \_ SYSKEYUP**](wm-syskeyup.md)
</dt> <dt>

**概念**
</dt> <dt>

[鍵盤輸入](keyboard-input.md)
</dt> </dl>

 


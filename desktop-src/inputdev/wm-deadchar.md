---
title: 'WM_DEADCHAR 訊息 (Winuser .h) '
description: 在 TranslateMessage 函式轉譯了 WM KEYUP 訊息時，以鍵盤焦點張貼至視窗 \_ 。
ms.assetid: ada9a61c-dabf-447b-ae13-91803c097f0d
keywords:
- WM_DEADCHAR 訊息鍵盤和滑鼠輸入
topic_type:
- apiref
api_name:
- WM_DEADCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6053095b912360e9875fa062c2daba7cafcfd43b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464940"
---
# <a name="wm_deadchar-message"></a>WM \_ DEADCHAR 訊息

在 [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage)函式轉譯了 [**WM \_ KEYUP**](wm-keyup.md)訊息時，以鍵盤焦點張貼至視窗。 **WM \_DEADCHAR** 指定由死索引鍵產生的字元碼。 無作用索引鍵是產生字元的索引鍵，例如，與另一個字元結合以形成複合字元的母音 (雙點) 。 例如，藉由為母音字元輸入死索引鍵，然後輸入 O 鍵來產生 ( ) 的母音字元。


```C++
#define WM_DEADCHAR                     0x0103
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

由死索引鍵產生的字元碼。

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

應用程式通常會使用 **WM \_ DEADCHAR** 訊息，為使用者提供每個按鍵的相關意見反應。 例如，應用程式可以在目前的字元位置顯示輔色，而不移動插入號。

因為所按下的按鍵和產生的字元訊息之間不一定要有一對一的對應，所以 *lParam* 參數的高序位字中的資訊通常對應用程式而言並不有用。 高序位字組中的資訊只適用于在 **\_ DEADCHAR** 訊息張貼之前的最新 wm 的一則的 [**wm \_**](wm-keydown.md)訊息。

針對增強的101和102鍵鍵盤，擴充的按鍵是鍵盤主要區段上的右 ALT 和右 CTRL 鍵;位於數位鍵台左邊的叢集中的 INS、DEL、HOME、END、PAGE UP、PAGE DOWN 和方向鍵;並將 (/) ，然後在數位鍵台中輸入按鍵。 有些其他鍵盤可能會支援 *lParam* 參數中的擴充金鑰位。

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

[**WM \_ KEYUP**](wm-keyup.md)
</dt> <dt>

[**WM \_ SYSDEADCHAR**](wm-sysdeadchar.md)
</dt> <dt>

**概念**
</dt> <dt>

[鍵盤輸入](keyboard-input.md)
</dt> </dl>

 


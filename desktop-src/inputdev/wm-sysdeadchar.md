---
title: 'WM_SYSDEADCHAR 訊息 (Winuser .h) '
description: 當 TranslateMessage 函數轉譯了 WM SYSKEYDOWN 訊息時，會使用鍵盤焦點將其傳送至視窗 \_ 。
ms.assetid: cf9a1171-a47c-4d7b-b351-31f41a893b20
keywords:
- WM_SYSDEADCHAR 訊息鍵盤和滑鼠輸入
topic_type:
- apiref
api_name:
- WM_SYSDEADCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2052f8ced24ac998a56a4365552fee4bc5e0b21e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969815"
---
# <a name="wm_sysdeadchar-message"></a>WM \_ SYSDEADCHAR 訊息

當 [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage)函數轉譯了 [**WM \_ SYSKEYDOWN**](wm-syskeydown.md)訊息時，會使用鍵盤焦點將其傳送至視窗。 **WM \_SYSDEADCHAR** 指定系統失效金鑰的字元碼，也就是按住 ALT 鍵時按下的無作用索引鍵。


```C++
#define WM_SYSDEADCHAR                  0x0107
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

系統死碼產生的字元碼，也就是按住 ALT 鍵時按下的無作用索引鍵。

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
| 31    | 轉換狀態。 如果正在釋放金鑰，則值為1，如果正在按下索引鍵，則為0。                                                                                                                                                                |

如需詳細資訊，請參閱 [按鍵訊息旗標](about-keyboard-input.md#keystroke-message-flags)。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果應用程式處理此訊息，則應該傳回零。

## <a name="remarks"></a>備註

針對增強的101和102鍵鍵盤，擴充的按鍵是鍵盤主要區段上的右 ALT 和 CTRL 鍵;位於數位鍵台左邊的叢集中的 INS、DEL、HOME、END、PAGE UP、PAGE DOWN 和方向鍵;並將 (/) ，然後在數位鍵台中輸入按鍵。 其他鍵盤可能會在 *lParam* 參數中支援擴充金鑰位。

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

[**WM \_ DEADCHAR**](wm-deadchar.md)
</dt> <dt>

[**WM \_ SYSKEYDOWN**](wm-syskeydown.md)
</dt> <dt>

**概念**
</dt> <dt>

[鍵盤輸入](keyboard-input.md)
</dt> </dl>

 


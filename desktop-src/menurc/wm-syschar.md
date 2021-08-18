---
title: 'WM_SYSCHAR 訊息 (Winuser .h) '
description: 當 TranslateMessage 函數轉譯了 WM SYSKEYDOWN 訊息時，以鍵盤焦點張貼至視窗 \_ 。
ms.assetid: 55987105-3c53-42e5-8fab-a3c9f2ca7273
keywords:
- WM_SYSCHAR 訊息功能表和其他資源
topic_type:
- apiref
api_name:
- WM_SYSCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b42d88d5ae1346032da2c663dd8c9189c030d5bb7d538ab7ef84403d42fba76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118472086"
---
# <a name="wm_syschar-message"></a>WM \_ SYSCHAR 訊息

當 [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage)函數轉譯了 [**WM \_ SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown)訊息時，以鍵盤焦點張貼至視窗。 它會指定系統字元索引鍵的字元碼，也就是在 ALT 鍵關閉時按下的字元按鍵。


```C++
#define WM_SYSCHAR                      0x0106
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

視窗功能表鍵的字元碼。

</dd> <dt>

*lParam* 
</dt> <dd>

[重複計數]、[掃描程式碼]、[擴充按鍵旗標]、[內容程式碼]、先前的索引鍵狀態旗標和轉換狀態旗標，如下表所示。



| Bits                                                                             | 意義                                                                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0 15</dt> </dl>  | 目前訊息的重複計數。 值是當使用者按住索引鍵時，自動重複擊鍵的次數。 如果按鍵夠長，則會傳送多則訊息。 不過，重複計數不是累計的。<br/> |
| <dl> <dt>16 23</dt> </dl> | 掃描程式碼。 此值取決於原始設備製造商 (OEM) 。<br/>                                                                                                                                                                                          |
| <dl> <dt>24</dt> </dl>    | 指出機碼是否為擴充的索引鍵，例如出現在增強型101或102按鍵鍵盤上的右手 ALT 和 CTRL 鍵。 如果它是擴充索引鍵，則此值為 1;否則，它是0。<br/>                                                                |
| <dl> <dt>25 28</dt> </dl> | 保護請勿使用。<br/>                                                                                                                                                                                                                                                   |
| <dl> <dt>29</dt> </dl>    | 內容程式碼。 如果按下按鍵時按住 ALT 鍵，則此值為 1;否則，此值為0。<br/>                                                                                                                                                       |
| <dl> <dt>30</dt> </dl>    | 先前的金鑰狀態。 如果在傳送訊息之前，金鑰已關閉，則此值為 1; 如果金鑰已啟動，則為0。<br/>                                                                                                                                                      |
| <dl> <dt>31</dt> </dl>    | 轉換狀態。 如果正在釋放金鑰，則值為1，如果正在按下索引鍵，則為0。<br/>                                                                                                                                                              |

如需詳細資訊，請參閱 [按鍵訊息旗標](../inputdev/about-keyboard-input.md#keystroke-message-flags)。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果應用程式處理此訊息，則應該傳回零。

## <a name="remarks"></a>備註

當內容程式碼為零時，訊息可以傳遞至 [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) 函式，此函式會處理它，就好像它是標準的索引鍵訊息，而不是系統字元金鑰訊息一樣。 這可讓快速鍵與使用中視窗搭配使用，即使使用中視窗沒有鍵盤焦點也一樣。

針對增強的101和102鍵鍵盤，擴充的按鍵是鍵盤主要區段上的右 ALT 和 CTRL 鍵;位於數位鍵台左邊的叢集中的 INS、DEL、HOME、END、PAGE UP、PAGE DOWN 和方向鍵;PRINT SCRN 鍵;BREAK 鍵;數位鍵;並將 (/) ，然後在數位鍵台中輸入按鍵。 其他鍵盤可能會支援參數中的擴充金鑰位。

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

[**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora)
</dt> <dt>

[**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage)
</dt> <dt>

[**WM \_ SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown)
</dt> <dt>

**概念**
</dt> <dt>

[鍵盤加速器](keyboard-accelerators.md)
</dt> </dl>


---
title: 'TF_LBI_STYLE_ 常數 (Ctfutb) '
description: Tf \_ LBI \_ STYLE \_ \ 常數用於 tf LANGBARITEMINFO 結構的 dwStyle 成員 \_ ，以指定語言列專案的樣式。
ms.assetid: 9180a666-774f-401b-bea3-68d5396fab30
topic_type:
- apiref
api_name:
- TF_LBI_STYLE_HIDDENSTATUSCONTROL
- TF_LBI_STYLE_SHOWNINTRAY
- TF_LBI_STYLE_HIDEONNOOTHERITEMS
- TF_LBI_STYLE_SHOWNINTRAYONLY
- TF_LBI_STYLE_HIDDENBYDEFAULT
- TF_LBI_STYLE_TEXTCOLORICON
- TF_LBI_STYLE_BTN_BUTTON
- TF_LBI_STYLE_BTN_MENU
- TF_LBI_STYLE_BTN_TOGGLE
api_location:
- Ctfutb.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b43ef805161afce6cb73bfaa26060308bc0aa5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465209"
---
# <a name="tf_lbi_style_-constants"></a>TF \_ LBI \_ 樣式 \_ \* 常數

Tf **\_ LBI \_ STYLE \_ \* *_ 常數用於*** [tf \_ LANGBARITEMINFO](/windows/desktop/api/Ctfutb/ns-ctfutb-tf_langbariteminfo)結構的 _ dwStyle 成員，以指定語言列專案的樣式。

如果此樣式與 TF \_ LBI \_ style \_ BTN 按鈕結合 \_ ，除了文字之外，還會顯示專案的下拉式箭號。 下拉箭號會以功能表按鈕的形式執行，並按一下它會導致呼叫 **ITfLangBarItemButton：： InitMenu** 。 按一下按鈕的文字部分，就會呼叫 **ITfLangBarItemButton：： OnClick** 。



| 常數/值                                                                                                                                                                                                                                                                           | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_LBI_STYLE_HIDDENSTATUSCONTROL"></span><span id="tf_lbi_style_hiddenstatuscontrol"></span><dl> <dt>**TF \_LBI \_ STYLE \_ HIDDENSTATUSCONTROL**</dt> <dt>0x00000001</dt> </dl> | 您可以使用 \_ \_ \_ [ITfLangBarItem：： GETSTATUS](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-getstatus) 方法中的 TF LBI STATUS hidden 值，以動態方式隱藏或顯示專案。 如果此值不存在，就無法以這種方式隱藏專案。<br/>                                                                                                                                                                                                                                                                         |
| <span id="TF_LBI_STYLE_SHOWNINTRAY"></span><span id="tf_lbi_style_shownintray"></span><dl> <dt>**TF \_LBI \_ 樣式 \_ SHOWNINTRAY**</dt> <dt>0x00000002</dt> </dl>                         | 除了語言列之外，此專案也會顯示在通知圖示紙匣中。 目前不支援此旗標。<br/>                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="TF_LBI_STYLE_HIDEONNOOTHERITEMS"></span><span id="tf_lbi_style_hideonnootheritems"></span><dl> <dt>**TF \_LBI \_ STYLE \_ HIDEONNOOTHERITEMS**</dt> <dt>0x00000004</dt> </dl>    | 如果語言行中的所有專案都包含此樣式，則會隱藏語言列。 如果語言列中的任何專案不包含此樣式，則會顯示語言列。<br/>                                                                                                                                                                                                                                                                                                                                  |
| <span id="TF_LBI_STYLE_SHOWNINTRAYONLY"></span><span id="tf_lbi_style_shownintrayonly"></span><dl> <dt>**TF \_LBI \_ STYLE \_ SHOWNINTRAYONLY**</dt> <dt>0x00000008</dt> </dl>             | 專案只會顯示在通知圖示紙匣中，而不會顯示在語言列中。 目前不支援此旗標。<br/>                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="TF_LBI_STYLE_HIDDENBYDEFAULT"></span><span id="tf_lbi_style_hiddenbydefault"></span><dl> <dt>**TF \_LBI \_ STYLE \_ HIDDENBYDEFAULT**</dt> <dt>0x00000010</dt> </dl>             | 專案在從 [語言列選項] 功能表中選取之前，將不會顯示在工具列中。 如果已 \_ 設定 TF LBI \_ STYLE \_ HIDDENSTATUSCONTROL，或使用者已使用 [語言列選項] 功能表變更隱藏/顯示的狀態，則會忽略此旗標。<br/>                                                                                                                                                                                                                                         |
| <span id="TF_LBI_STYLE_TEXTCOLORICON"></span><span id="tf_lbi_style_textcoloricon"></span><dl> <dt>**TF \_LBI \_ STYLE \_ TEXTCOLORICON**</dt> <dt>0x00000020</dt> </dl>                   | 圖示內的任何黑色圖元都會轉換成所選主題的文字色彩。 圖示必須是單色。<br/>                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="TF_LBI_STYLE_BTN_BUTTON"></span><span id="tf_lbi_style_btn_button"></span><dl> <dt>**TF \_LBI \_ 樣式 \_ BTN \_ 按鈕**</dt> <dt>0x00010000</dt> </dl>                           | 此專案為 push 按鈕。 按下專案時，會呼叫[ITfLangBarItemButton：： OnClick](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-onclick) 。<br/>                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="TF_LBI_STYLE_BTN_MENU"></span><span id="tf_lbi_style_btn_menu"></span><dl> <dt>**TF \_LBI \_ 樣式 \_ BTN \_ 功能表**</dt> <dt>0x00020000</dt> </dl>                                 | 專案是功能表。 [ITfLangBarItemButton：： InitMenu](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-initmenu) 會在按下專案時呼叫。<br/> 如果此樣式與 TF \_ LBI \_ style \_ BTN 按鈕結合 \_ ，除了文字之外，還會顯示專案的下拉式箭號。 下拉箭號會以功能表按鈕的形式執行，並按一下它會導致呼叫 **ITfLangBarItemButton：： InitMenu** 。 按一下按鈕的文字部分，就會呼叫 **ITfLangBarItemButton：： OnClick** 。<br/> |
| <span id="TF_LBI_STYLE_BTN_TOGGLE"></span><span id="tf_lbi_style_btn_toggle"></span><dl> <dt>**TF \_LBI \_ 樣式 \_ BTN \_ 切換**</dt> <dt>0x00040000</dt> </dl>                           | 專案是切換按鈕，其運作方式類似于核取方塊。 按下專案時，會呼叫 **ITfLangBarItemButton：： OnClick** 。<br/>                                                                                                                                                                                                                                                                                                                                                                       |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                            |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                  |
| 可轉散發套件<br/>          | Windows 2000 Professional 上的 TSF 1。0<br/>                                       |
| 標頭<br/>                   | <dl> <dt>Ctfutb。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Ctfutb .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[TF \_ LANGBARITEMINFO](/windows/desktop/api/Ctfutb/ns-ctfutb-tf_langbariteminfo)
</dt> <dt>

[ITfLangBarItem::GetInfo](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-getinfo)
</dt> <dt>

[ITfLangBarItem：： GetStatus](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-getstatus)
</dt> </dl>

 

 






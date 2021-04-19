---
title: 'TF_LBI_ 常數 (Ctfutb) '
description: TF \_ LBI \_ \ 常數會與 ITfLangBarItemSink OnUpdate 方法搭配使用，以指出已變更的語言列專案。
ms.assetid: ed84012f-19ba-43b3-bbb5-7373ed174c33
topic_type:
- apiref
api_name:
- TF_LBI_ICON
- TF_LBI_TEXT
- TF_LBI_TOOLTIP
- TF_LBI_BITMAP
- TF_LBI_BALLOON
- TF_LBI_STATUS
- TF_LBI_BMPALL
- TF_LBI_BMPBTNALL
- TF_LBI_BTNALL
api_location:
- Ctfutb.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d72b69f1cb5a5b4a24e78a2bdc1ca0e7a9d79cbf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966302"
---
# <a name="tf_lbi_-constants"></a>TF \_ LBI \_ \* 常數

**TF \_ LBI \_ \** _ 常數可與 [ITfLangBarItemSink：： OnUpdate](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritemsink-onupdate)方法搭配使用，以指出已變更的語言列專案。



| 常數/值                                                                                                                                                                                                                                                                  | Description                                                                                                                                                                                                                                                                                                         |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_LBI_ICON"></span><span id="tf_lbi_icon"></span><dl> <dt>_ * TF \_LBI \_ 圖示 * *</dt> <dt>0x00000001</dt> </dl>                                                        | 專案的圖示已變更。 Language bar 會呼叫 [ITfLangBarItemButton：： GetIcon](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-geticon) 來回應此通知。<br/>                                                                                                                                             |
| <span id="TF_LBI_TEXT"></span><span id="tf_lbi_text"></span><dl> <dt>**TF \_LBI \_ 文本**</dt> <dt>0x00000002</dt> </dl>                                                        | 按鈕或點陣圖按鈕專案的文字已變更。 語言列會呼叫 [ITfLangBarItemButton：： GetText](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-gettext) 或 [ITfLangBarItemBitmapButton：： GetText](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembitmapbutton-gettext)（視何者而定），以回應這項通知。<br/>           |
| <span id="TF_LBI_TOOLTIP"></span><span id="tf_lbi_tooltip"></span><dl> <dt>**TF \_LBI \_ 工具提示**</dt> <dt>0x00000004</dt> </dl>                                               | 專案的工具提示文字已變更。 Language bar 會呼叫 [ITfLangBarItem：： GetTooltipString](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-gettooltipstring) 來回應此通知。<br/>                                                                                                                                   |
| <span id="TF_LBI_BITMAP"></span><span id="tf_lbi_bitmap"></span><dl> <dt>**TF \_LBI \_ 點陣圖**</dt> <dt>0x00000008</dt> </dl>                                                  | 點陣圖或點陣圖按鈕專案的點陣圖已變更。 語言列會呼叫 [ITfLangBarItemBitmap：:D rawbitmap](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembitmap-drawbitmap) 或 [ITfLangBarItemBitmapButton：:D rawbitmap](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembitmapbutton-drawbitmap)（視何者而定），以回應這項通知。<br/> |
| <span id="TF_LBI_BALLOON"></span><span id="tf_lbi_balloon"></span><dl> <dt>**TF \_LBI \_ 氣球**</dt> <dt>0x00000010</dt> </dl>                                               | 氣球專案的資訊已變更。 Language bar 會呼叫 [ITfLangBarItemBalloon：： GetBalloonInfo](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritemballoon-getballooninfo) 來回應此通知。<br/>                                                                                                                   |
| <span id="TF_LBI_STATUS"></span><span id="tf_lbi_status"></span><dl> <dt>**TF \_LBI \_ 狀態**</dt> <dt>0x00010000</dt> </dl>                                                  | 專案狀態已變更。 Language bar 會呼叫 [ITfLangBarItem：： GetStatus](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-getstatus) 來回應此通知。<br/>                                                                                                                                                              |
| <span id="TF_LBI_BMPALL"></span><span id="tf_lbi_bmpall"></span><dl> <dt>**TF \_LBI \_ BMPALL**</dt> <dt>TF \_ LBI \_ 點陣圖 \| TF \_ LBI \_ 工具提示</dt> </dl>                          | 結合 TF \_ LBI \_ BITMAP 和 tf \_ LBI \_ 工具提示。<br/>                                                                                                                                                                                                                                                           |
| <span id="TF_LBI_BMPBTNALL"></span><span id="tf_lbi_bmpbtnall"></span><dl> <dt>**TF \_LBI \_ BMPBTNALL**</dt> <dt>TF \_ LBI \_ BITMAP \| TF \_ LBI \_ TEXT \| TF \_ LBI \_ TOOLTIP</dt> </dl> | 結合 TF \_ LBI \_ BITMAP、tf \_ LBI \_ TEXT 和 tf \_ LBI \_ 工具提示。<br/>                                                                                                                                                                                                                                            |
| <span id="TF_LBI_BTNALL"></span><span id="tf_lbi_btnall"></span><dl> <dt>**TF \_LBI \_ BTNALL**</dt> <dt>TF \_ LBI \_ 圖示 \| TF \_ LBI \_ TEXT \| TF \_ LBI \_ TOOLTIP</dt> </dl>            | 結合 TF \_ LBI \_ 圖示、tf \_ LBI \_ TEXT 和 tf \_ LBI \_ 工具提示。<br/>                                                                                                                                                                                                                                              |



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

[ITfLangBarItemSink：： OnUpdate](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritemsink-onupdate)
</dt> </dl>

 

 






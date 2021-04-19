---
title: 'TF_SFT_ 常數 (Ctfutb) '
description: TF \_ SFT \_ \ 常數指定浮動語言列的顯示設定。
ms.assetid: 628e1d85-9614-4327-b89b-723f6eeb0718
topic_type:
- apiref
api_name:
- TF_SFT_SHOWNORMAL
- TF_SFT_DOCK
- TF_SFT_MINIMIZED
- TF_SFT_HIDDEN
- TF_SFT_NOTRANSPARENCY
- TF_SFT_LOWTRANSPARENCY
- TF_SFT_HIGHTRANSPARENCY
- TF_SFT_LABELS
- TF_SFT_NOLABELS
- TF_SFT_EXTRAICONSONMINIMIZED
- TF_SFT_NOEXTRAICONSONMINIMIZED
- TF_SFT_DESKBAND
api_location:
- Ctfutb.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93a947960bfbe67585dc02a37de2da3dc6737540
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965910"
---
# <a name="tf_sft_-constants"></a>TF \_ SFT \_ \* 常數

**TF \_ SFT \_ \** _ 常數指定浮動語言列的顯示設定。



| 常數/值                                                                                                                                                                                                                                                                    | Description                                                                                                                                                                                                                                                                             |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_SFT_SHOWNORMAL"></span><span id="tf_sft_shownormal"></span><dl> <dt>_ * TF \_SFT \_ SHOWNORMAL * *</dt> <dt>0x00000001</dt> </dl>                                        | 將語言列顯示為浮動視窗。 這個常數無法與 TF \_ sft \_ DOCK、tf \_ sft \_ 最小化、TF \_ sft \_ HIDDEN 或 tf \_ sft \_ DESKBAND 常數合併使用。<br/>                                                                                                 |
| <span id="TF_SFT_DOCK"></span><span id="tf_sft_dock"></span><dl> <dt>**TF \_SFT \_ DOCK**</dt> <dt>0x00000002</dt> </dl>                                                          | 將語言列停駐在自己的工作窗格中。 這個常數無法與 TF \_ sft \_ SHOWNORMAL、tf \_ sft \_ 最小化、TF \_ sft \_ HIDDEN 或 tf \_ sft \_ DESKBAND 常數結合。 僅適用于 Windows XP。<br/>                                                                |
| <span id="TF_SFT_MINIMIZED"></span><span id="tf_sft_minimized"></span><dl> <dt>**TF \_SFT \_ 最小化**</dt>的 <dt>0x00000004</dt> </dl>                                           | 將語言列顯示為系統匣中的單一圖示。 這個常數無法與 TF \_ sft \_ SHOWNORMAL、tf \_ SFT \_ DOCK、TF \_ sft \_ HIDDEN 或 tf \_ sft \_ DESKBAND 常數結合。 在 Windows XP 中，請改用 TF \_ SFT \_ DESKBAND。<br/>                                   |
| <span id="TF_SFT_HIDDEN"></span><span id="tf_sft_hidden"></span><dl> <dt>**TF \_SFT \_ 隱藏**</dt> <dt>0x00000008</dt> </dl>                                                    | 隱藏語言列。 這個常數無法與 TF \_ sft \_ SHOWNORMAL、tf \_ SFT \_ DOCK、tf \_ sft 的 \_ 最小化或 tf \_ sft \_ DESKBAND 常數結合。<br/>                                                                                                                     |
| <span id="TF_SFT_NOTRANSPARENCY"></span><span id="tf_sft_notransparency"></span><dl> <dt>**TF \_SFT \_ NOTRANSPARENCY**</dt> <dt>0x00000010</dt> </dl>                            | 讓語言行不透明。<br/>                                                                                                                                                                                                                                                |
| <span id="TF_SFT_LOWTRANSPARENCY"></span><span id="tf_sft_lowtransparency"></span><dl> <dt>**TF \_SFT \_ LOWTRANSPARENCY**</dt> <dt>0x00000020</dt> </dl>                         | 將語言列設為部分透明。 僅適用于 Windows 2000 或更新版本。<br/>                                                                                                                                                                                        |
| <span id="TF_SFT_HIGHTRANSPARENCY"></span><span id="tf_sft_hightransparency"></span><dl> <dt>**TF \_SFT \_ HIGHTRANSPARENCY**</dt> <dt>0x00000040</dt> </dl>                      | 將語言列設為高度透明。 僅適用于 Windows 2000 或更新版本。<br/>                                                                                                                                                                                           |
| <span id="TF_SFT_LABELS"></span><span id="tf_sft_labels"></span><dl> <dt>**TF \_SFT \_ 標籤**</dt> <dt>0x00000080</dt> </dl>                                                    | 顯示語言列圖示旁邊的文字標籤。<br/>                                                                                                                                                                                                                              |
| <span id="TF_SFT_NOLABELS"></span><span id="tf_sft_nolabels"></span><dl> <dt>**TF \_SFT \_ NOLABELS**</dt> <dt>0x00000100</dt> </dl>                                              | 隱藏語言橫條圖示文字標籤。<br/>                                                                                                                                                                                                                                          |
| <span id="TF_SFT_EXTRAICONSONMINIMIZED"></span><span id="tf_sft_extraiconsonminimized"></span><dl> <dt>**TF \_SFT \_ EXTRAICONSONMINIMIZED**</dt> <dt>0x00000200</dt> </dl>       | 當語言列最小化時，在工作列上顯示文字服務圖示。<br/>                                                                                                                                                                                                |
| <span id="TF_SFT_NOEXTRAICONSONMINIMIZED"></span><span id="tf_sft_noextraiconsonminimized"></span><dl> <dt>**TF \_SFT \_ NOEXTRAICONSONMINIMIZED**</dt> <dt>0x00000400</dt> </dl> | 當語言列最小化時，隱藏工作列上的文字服務圖示。<br/>                                                                                                                                                                                                   |
| <span id="TF_SFT_DESKBAND"></span><span id="tf_sft_deskband"></span><dl> <dt>**TF \_SFT \_ DESKBAND**</dt> <dt>0x00000800</dt> </dl>                                              | 將語言列停駐于系統工作列的 righthand 結尾 (系統匣/時鐘) 的正下方。 這個常數無法與 TF \_ sft \_ SHOWNORMAL、tf \_ SFT \_ DOCK、tf \_ sft 的 \_ 最小化，或 tf \_ sft \_ 隱藏的常數合併。 僅適用于 Windows XP。<br/> |



## <a name="remarks"></a>備註

[ITfLangBarMgr：： ShowFloating](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbarmgr-showfloating)方法會設定一或多個常數的邏輯 **OR** 運算結果，以指定語言列專案的屬性。

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

[ITfLangBarMgr::ShowFloating](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbarmgr-showfloating)
</dt> </dl>

 

 






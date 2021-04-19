---
title: 'Rich Edit 控制項事件遮罩旗標 (RichEdit .h) '
description: 事件遮罩會指定 rich edit 控制項傳送至其父視窗的通知碼。 事件遮罩可以是 none 或這些值的組合。
ms.assetid: ae0d2cbe-5cbc-42bb-aeb1-7e6be846a4ba
topic_type:
- apiref
api_name:
- ENM_CHANGE
- ENM_CLIPFORMAT
- ENM_CORRECTTEXT
- ENM_DRAGDROPDONE
- ENM_DROPFILES
- ENM_IMECHANGE
- ENM_KEYEVENTS
- ENM_LINK
- ENM_LOWFIRTF
- ENM_MOUSEEVENTS
- ENM_OBJECTPOSITIONS
- ENM_PARAGRAPHEXPANDED
- ENM_PROTECTED
- ENM_REQUESTRESIZE
- ENM_SCROLL
- ENM_SCROLLEVENTS
- ENM_SELCHANGE
- ENM_UPDATE
api_location:
- RichEdit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 006a6d82e7aa4958b03360d05d29a78564f99db7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993332"
---
# <a name="rich-edit-control-event-mask-flags"></a>Rich Edit 控制項事件遮罩旗標

事件遮罩會指定 rich edit 控制項傳送至其父視窗的通知碼。 事件遮罩可以是 none 或這些值的組合。



| 常數                                                                                                                                                                              | 描述                                                                                                                                                                                                                                                                                                       |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ENM_CHANGE"></span><span id="enm_change"></span><dl> <dt>**ENM \_ 變更**</dt> </dl>                                  | 傳送 [EN \_ 變更](en-change--rich-edit-control-.md) 通知。<br/>                                                                                                                                                                                                                                   |
| <span id="ENM_CLIPFORMAT"></span><span id="enm_clipformat"></span><dl> <dt>**ENM \_ CLIPFORMAT**</dt> </dl>                      | 傳送 [EN \_ CLIPFORMAT](/windows/desktop/Controls/en-clipformat) 通知。<br/>                                                                                                                                                                                                                                          |
| <span id="ENM_CORRECTTEXT"></span><span id="enm_correcttext"></span><dl> <dt>**ENM \_ CORRECTTEXT**</dt> </dl>                   | 傳送 [EN \_ CORRECTTEXT](en-correcttext.md) 通知。<br/>                                                                                                                                                                                                                                             |
| <span id="ENM_DRAGDROPDONE"></span><span id="enm_dragdropdone"></span><dl> <dt>**ENM \_ DRAGDROPDONE**</dt> </dl>                | 傳送 [EN \_ DRAGDROPDONE](en-dragdropdone.md) 通知。<br/>                                                                                                                                                                                                                                           |
| <span id="ENM_DROPFILES"></span><span id="enm_dropfiles"></span><dl> <dt>**ENM \_ DROPFILES**</dt> </dl>                         | 傳送 [EN \_ DROPFILES](en-dropfiles.md) 通知。<br/>                                                                                                                                                                                                                                                 |
| <span id="ENM_IMECHANGE"></span><span id="enm_imechange"></span><dl> <dt>**ENM \_ IMECHANGE**</dt> </dl>                         | 僅限 Microsoft Rich Edit 1.0：當 IME 轉換狀態變更時傳送 [EN \_ IMECHANGE](en-imechange.md) 通知。 僅適用于亞洲語言版本的作業系統。<br/>                                                                                                              |
| <span id="ENM_KEYEVENTS"></span><span id="enm_keyevents"></span><dl> <dt>**ENM \_ KEYEVENTS**</dt> </dl>                         | 傳送鍵盤事件的 [EN \_ MSGFILTER](en-msgfilter.md) 通知。<br/>                                                                                                                                                                                                                             |
| <span id="ENM_LINK"></span><span id="enm_link"></span><dl> <dt>**ENM \_ 連結**</dt> </dl>                                        | **Rich Edit 2.0 和更新版本：** 當 [滑鼠 \_](en-link.md) 指標停留在具有 CFE 連結的文字上 \_ ，以及執行數個滑鼠動作的其中一個時，傳送 EN 連結通知。<br/>                                                                                                                     |
| <span id="ENM_LOWFIRTF"></span><span id="enm_lowfirtf"></span><dl> <dt>**ENM \_ LOWFIRTF**</dt> </dl>                            | 傳送 [EN \_ LOWFIRTF](en-lowfirtf.md) 通知。<br/>                                                                                                                                                                                                                                                   |
| <span id="ENM_MOUSEEVENTS"></span><span id="enm_mouseevents"></span><dl> <dt>**ENM \_ MOUSEEVENTS**</dt> </dl>                   | 傳送滑鼠事件的 [EN \_ MSGFILTER](en-msgfilter.md) 通知。<br/>                                                                                                                                                                                                                                |
| <span id="ENM_OBJECTPOSITIONS"></span><span id="enm_objectpositions"></span><dl> <dt>**ENM \_ OBJECTPOSITIONS**</dt> </dl>       | 傳送 [EN \_ OBJECTPOSITIONS](en-objectpositions.md) 通知。<br/>                                                                                                                                                                                                                                     |
| <span id="ENM_PARAGRAPHEXPANDED"></span><span id="enm_paragraphexpanded"></span><dl> <dt>**ENM \_ PARAGRAPHEXPANDED**</dt> </dl> | 傳送 [EN \_ PARAGRAPHEXPANDED](/windows/desktop/Controls/en-paragraphexpanded) 通知。<br/>                                                                                                                                                                                                                            |
| <span id="ENM_PROTECTED"></span><span id="enm_protected"></span><dl> <dt>**ENM \_ 保護**</dt> </dl>                         | 傳送 [ \_ 受保護](en-protected.md) 的通知。<br/>                                                                                                                                                                                                                                                 |
| <span id="ENM_REQUESTRESIZE"></span><span id="enm_requestresize"></span><dl> <dt>**ENM \_ REQUESTRESIZE**</dt> </dl>             | 傳送 [EN \_ REQUESTRESIZE](en-requestresize.md) 通知。<br/>                                                                                                                                                                                                                                         |
| <span id="ENM_SCROLL"></span><span id="enm_scroll"></span><dl> <dt>**ENM \_ 捲軸**</dt> </dl>                                  | 傳送 [en \_ HSCROLL](en-hscroll.md) 和 [en \_ VSCROLL](en-vscroll.md) 通知。<br/>                                                                                                                                                                                                                   |
| <span id="ENM_SCROLLEVENTS"></span><span id="enm_scrollevents"></span><dl> <dt>**ENM \_ SCROLLEVENTS**</dt> </dl>                | 傳送滑鼠滾輪事件的 [EN \_ MSGFILTER](en-msgfilter.md) 通知。<br/>                                                                                                                                                                                                                          |
| <span id="ENM_SELCHANGE"></span><span id="enm_selchange"></span><dl> <dt>**ENM \_ SELCHANGE**</dt> </dl>                         | 傳送 [EN \_ SELCHANGE](en-selchange.md) 通知。<br/>                                                                                                                                                                                                                                                 |
| <span id="ENM_UPDATE"></span><span id="enm_update"></span><dl> <dt>**ENM \_ 更新**</dt> </dl>                                  | 傳送 [EN \_ 更新](en-update.md) 通知。 <br/> **Rich Edit 2.0 和更新版本：** 此旗標會被忽略，而且一律會傳送 [EN \_ 更新](en-update.md) 通知。 但是，如果 Rich Edit 3.0 模擬 Microsoft Rich Edit 1.0，您就必須使用此旗標來傳送 \_ UPDATE 通知。<br/> |



## <a name="remarks"></a>備註

預設的事件遮罩是 ENM \_ NONE，在這種情況下，不會有任何通知傳送至父視窗。 您可以使用 [**em \_ GETEVENTMASK**](em-geteventmask.md) 和 [**em \_ SETEVENTMASK**](em-seteventmask.md) 訊息來取得和設定 rich edit 控制項的事件遮罩。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>RichEdit。h</dt> </dl> |



 


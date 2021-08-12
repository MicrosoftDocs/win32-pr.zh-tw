---
title: 'EM_SETOPTIONS 訊息 (Richedit .h) '
description: 設定 rich edit 控制項的選項。
ms.assetid: 98ef2de9-4c34-45ba-8e8a-eaf505f97f56
keywords:
- EM_SETOPTIONS 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5d5c4b7fd9e92261cedaf0681523ad0a3e25a37aa2814f6c00d0d9460e94bb1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118672607"
---
# <a name="em_setoptions-message"></a>EM \_ >setoptions 訊息

設定 rich edit 控制項的選項。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

指定作業，這可以是下列其中一個值。



| 值                                                                                                                                             | 意義                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span id="ECOOP_SET"></span><span id="ecoop_set"></span><dl> <dt>**ECOOP \_ 集**</dt> </dl> | 將選項設定為 *lParam* 所指定的選項。<br/>                             |
| <span id="ECOOP_OR"></span><span id="ecoop_or"></span><dl> <dt>**ECOOP \_ 或**</dt> </dl>    | 結合指定的選項與目前的選項。<br/>                     |
| <span id="ECOOP_AND"></span><span id="ecoop_and"></span><dl> <dt>**ECOOP \_ 和**</dt> </dl> | 只保留 *lParam* 中也會指定的目前選項。<br/>      |
| <span id="ECOOP_XOR"></span><span id="ecoop_xor"></span><dl> <dt>**ECOOP \_ XOR**</dt> </dl> | 以邏輯方式獨佔或目前的選項與 *lParam* 指定的選項。<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

指定下列一或多個值。



| 值                                                                                                                                                                                 | 意義                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span id="ECO_AUTOWORDSELECTION"></span><span id="eco_autowordselection"></span><dl> <dt>**ECO \_ AUTOWORDSELECTION**</dt> </dl> | 按兩下時自動選取單字。<br/>                                                                           |
| <span id="ECO_AUTOVSCROLL"></span><span id="eco_autovscroll"></span><dl> <dt>**ECO \_ AUTOVSCROLL**</dt> </dl>                   | 與 [**ES \_ AUTOVSCROLL**](rich-edit-control-styles.md) 樣式相同。<br/>                                      |
| <span id="ECO_AUTOHSCROLL"></span><span id="eco_autohscroll"></span><dl> <dt>**ECO \_ AUTOHSCROLL**</dt> </dl>                   | 與 [**ES \_ AUTOHSCROLL**](rich-edit-control-styles.md) 樣式相同。<br/>                                      |
| <span id="ECO_NOHIDESEL"></span><span id="eco_nohidesel"></span><dl> <dt>**ECO \_ NOHIDESEL**</dt> </dl>                         | 與 [**ES \_ NOHIDESEL**](rich-edit-control-styles.md) 樣式相同。<br/>                                          |
| <span id="ECO_READONLY"></span><span id="eco_readonly"></span><dl> <dt>**ECO \_ READONLY**</dt> </dl>                            | 與 [**ES \_ READONLY**](rich-edit-control-styles.md) 樣式相同。<br/>                                            |
| <span id="ECO_WANTRETURN"></span><span id="eco_wantreturn"></span><dl> <dt>**ECO \_ WANTRETURN**</dt> </dl>                      | 與 [**ES \_ WANTRETURN**](rich-edit-control-styles.md) 樣式相同。<br/>                                        |
| <span id="ECO_SELECTIONBAR"></span><span id="eco_selectionbar"></span><dl> <dt>**ECO \_ SELECTIONBAR**</dt> </dl>                | 與 [**ES \_ SELECTIONBAR**](rich-edit-control-styles.md) 樣式相同。<br/>                                    |
| <span id="ECO_VERTICAL"></span><span id="eco_vertical"></span><dl> <dt>**經濟 \_ 垂直**</dt> </dl>                            | 與 [**ES \_ 垂直**](rich-edit-control-styles.md) 樣式相同。 僅適用于亞洲語言版本。<br/> |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

此訊息會傳回編輯控制項的目前選項。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Rich Edit 控制項樣式**](rich-edit-control-styles.md)
</dt> </dl>

 

 






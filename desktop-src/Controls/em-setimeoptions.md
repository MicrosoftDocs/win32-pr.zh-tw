---
title: 'EM_SETIMEOPTIONS 訊息 (Richedit .h) '
description: 將輸入方法編輯器 (IME) 選項。
ms.assetid: 8a72ee1c-f6b8-44eb-b8df-57cd834db326
keywords:
- EM_SETIMEOPTIONS message Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETIMEOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59be3148bd00abd998af200368f2ed77ad3ff911
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843811"
---
# <a name="em_setimeoptions-message"></a>EM \_ SETIMEOPTIONS 訊息

將輸入方法編輯器 (IME) 選項。

> [!Note]  
> 只有 Microsoft Rich Edit 1.0 的亞洲語言版本才支援此訊息。 任何較新版本都不支援此功能。

 

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

指定下列其中一個值。



| 值                                                                                                                                             | 意義                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span id="ECOOP_SET"></span><span id="ecoop_set"></span><dl> <dt>**ECOOP \_ 集**</dt> </dl> | 將選項設定為 *lParam* 所指定的選項。<br/>                             |
| <span id="ECOOP_OR"></span><span id="ecoop_or"></span><dl> <dt>**ECOOP \_ 或**</dt> </dl>    | 結合指定的選項與目前的選項。<br/>                     |
| <span id="ECOOP_AND"></span><span id="ecoop_and"></span><dl> <dt>**ECOOP \_ 和**</dt> </dl> | 只保留 *lParam* 中也會指定的目前選項。<br/>      |
| <span id="ECOOP_XOR"></span><span id="ecoop_xor"></span><dl> <dt>**ECOOP \_ XOR**</dt> </dl> | 以邏輯方式獨佔或目前的選項與 LParam 指定的選項 *。*<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

指定下列其中一個值。



| 值                                                                                                                                                                                 | 意義                                                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="IMF_CLOSESTATUSWINDOW"></span><span id="imf_closestatuswindow"></span><dl> <dt>**IMF \_ CLOSESTATUSWINDOW**</dt> </dl> | 當控制項收到輸入焦點時，關閉輸入法狀態視窗。<br/>                                                                                                               |
| <span id="IMF_FORCEACTIVE"></span><span id="imf_forceactive"></span><dl> <dt>**IMF \_ FORCEACTIVE**</dt> </dl>                   | 當控制項收到輸入焦點時啟用 IME。<br/>                                                                                                                          |
| <span id="IMF_FORCEDISABLE"></span><span id="imf_forcedisable"></span><dl> <dt>**IMF \_ FORCEDISABLE**</dt> </dl>                | 當控制項收到輸入焦點時，停用 IME。<br/>                                                                                                                           |
| <span id="IMF_FORCEENABLE"></span><span id="imf_forceenable"></span><dl> <dt>**IMF \_ FORCEENABLE**</dt> </dl>                   | 當控制項收到輸入焦點時啟用 IME。<br/>                                                                                                                            |
| <span id="IMF_FORCEINACTIVE"></span><span id="imf_forceinactive"></span><dl> <dt>**IMF \_ FORCEINACTIVE**</dt> </dl>             | 當控制項收到輸入焦點時，會 IME。<br/>                                                                                                                        |
| <span id="IMF_FORCENONE"></span><span id="imf_forcenone"></span><dl> <dt>**IMF \_ FORCENONE**</dt> </dl>                         | 停用 IME 處理。<br/>                                                                                                                                                                |
| <span id="IMF_FORCEREMEMBER"></span><span id="imf_forceremember"></span><dl> <dt>**IMF \_ FORCEREMEMBER**</dt> </dl>             | 當控制項收到輸入焦點時，還原先前的輸入法狀態。<br/>                                                                                                           |
| <span id="IMF_MULTIPLEEDIT"></span><span id="imf_multipleedit"></span><dl> <dt>**IMF \_ MULTIPLEEDIT**</dt> </dl>                | 指定將不會取消或決定焦點變更的組合字元串。 這可讓應用程式在每個 rich edit 控制項上都有個別的組合字元串。<br/> |
| <span id="IMF_VERTICAL"></span><span id="imf_vertical"></span><dl> <dt>**IMF \_ 垂直**</dt> </dl>                            | 請注意，在豐富的編輯2.0 和更新版本中使用。 <br/>                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

如果作業成功，則傳回值為非零值。

如果作業失敗，則傳回值為零。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**EM \_ GETIMEOPTIONS**](em-getimeoptions.md)
</dt> </dl>

 

 






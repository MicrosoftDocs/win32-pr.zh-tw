---
title: 'EM_SETCTFMODEBIAS 訊息 (Richedit .h) '
description: 設定 rich edit 控制項的文字服務架構 (TSF) 模式偏差。
ms.assetid: 17e3aac8-2ba8-4c06-bfd6-e118cfb82529
keywords:
- EM_SETCTFMODEBIAS message Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETCTFMODEBIAS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b872fa5489c898ec4482ecdc094de7df6e3180be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509172"
---
# <a name="em_setctfmodebias-message"></a>EM \_ SETCTFMODEBIAS 訊息

設定 rich edit 控制項的文字服務架構 (TSF) 模式偏差。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

模式偏差值。 這可以是下列其中一個值。



| 值                                                                                                                                                                                                                     | 意義                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="CTFMODEBIAS_DEFAULT"></span><span id="ctfmodebias_default"></span><dl> <dt>**CTFMODEBIAS \_ 預設值**</dt> </dl>                                           | 沒有模式偏差。<br/>                             |
| <span id="CTFMODEBIAS_FILENAME"></span><span id="ctfmodebias_filename"></span><dl> <dt>**CTFMODEBIAS \_ 檔案名**</dt> </dl>                                        | 偏差是檔案名。<br/>                         |
| <span id="CTFMODEBIAS_NAME"></span><span id="ctfmodebias_name"></span><dl> <dt>**CTFMODEBIAS \_ 名稱**</dt> </dl>                                                    | 偏差是指名稱。<br/>                             |
| <span id="CTFMODEBIAS_READING"></span><span id="ctfmodebias_reading"></span><dl> <dt>**CTFMODEBIAS \_ 閱讀**</dt> </dl>                                           | 偏差是讀取的。<br/>                        |
| <span id="CTFMODEBIAS_DATETIME"></span><span id="ctfmodebias_datetime"></span><dl> <dt>**CTFMODEBIAS \_ DATETIME**</dt> </dl>                                        | 偏差是指日期或時間。<br/>                     |
| <span id="CTFMODEBIAS_CONVERSATION"></span><span id="ctfmodebias_conversation"></span><dl> <dt>**CTFMODEBIAS \_ 對話**</dt> </dl>                            | 偏差是指交談。<br/>                     |
| <span id="CTFMODEBIAS_NUMERIC"></span><span id="ctfmodebias_numeric"></span><dl> <dt>**CTFMODEBIAS \_ 數值**</dt> </dl>                                           | 偏差是數位。<br/>                           |
| <span id="CTFMODEBIAS_HIRAGANA"></span><span id="ctfmodebias_hiragana"></span><dl> <dt>**CTFMODEBIAS \_ 平假名**</dt> </dl>                                        | 偏差是指平假名字串。<br/>                   |
| <span id="CTFMODEBIAS_KATAKANA"></span><span id="ctfmodebias_katakana"></span><dl> <dt>**CTFMODEBIAS \_ 片假名**</dt> </dl>                                        | 偏差是片假名字串。<br/>                   |
| <span id="CTFMODEBIAS_HANGUL"></span><span id="ctfmodebias_hangul"></span><dl> <dt>**CTFMODEBIAS \_ 韓文**</dt> </dl>                                              | 偏差是以韓文字元為單位。<br/>                  |
| <span id="CTFMODEBIAS_HALFWIDTHKATAKANA"></span><span id="ctfmodebias_halfwidthkatakana"></span><dl> <dt>**CTFMODEBIAS \_ HALFWIDTHKATAKANA**</dt> </dl>             | 偏差是半形片假名字串。<br/>        |
| <span id="CTFMODEBIAS_FULLWIDTHALPHANUMERIC"></span><span id="ctfmodebias_fullwidthalphanumeric"></span><dl> <dt>**CTFMODEBIAS \_ FULLWIDTHALPHANUMERIC**</dt> </dl> | 偏差是全形的英數位元。<br/> |
| <span id="CTFMODEBIAS_HALFWIDTHALPHANUMERIC"></span><span id="ctfmodebias_halfwidthalphanumeric"></span><dl> <dt>**CTFMODEBIAS \_ HALFWIDTHALPHANUMERIC**</dt> </dl> | 偏差是半形的英數位元。<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

未使用;必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，傳回值就是新的 TSF 模式偏差值。 如果不成功，則傳回值為舊的 TSF 模式偏差值。

## <a name="remarks"></a>備註

當 Microsoft Rich Edit 應用程式使用 TSF 時，可以選取 TSF 模式偏差。 這則訊息會設定在清單頂端顯示替代選項的準則，以供選取。

若要為輸入方法編輯器設定模式偏差 (IME) ，請使用 [**EM \_ SETIMEMODEBIAS**](em-setimemodebias.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP （含 SP1） \[ 桌面應用程式\]<br/>                                  |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**EM \_ GETCTFMODEBIAS**](em-getctfmodebias.md)
</dt> <dt>

[**EM \_ SETIMEMODEBIAS**](em-setimemodebias.md)
</dt> </dl>

 

 






---
title: 'EM_SETIMEMODEBIAS 訊息 (Richedit .h) '
description: 針對 rich edit 控制項設定輸入法的 (IME) 模式偏差。
ms.assetid: 4a3f97eb-fe80-4e84-a73e-3ed6d73644de
keywords:
- EM_SETIMEMODEBIAS message Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETIMEMODEBIAS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48fbd93971a57cffa3441c2a3db0816572f761d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465709"
---
# <a name="em_setimemodebias-message"></a>EM \_ SETIMEMODEBIAS 訊息

針對 rich edit 控制項設定輸入法的 (IME) 模式偏差。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

輸入法模式偏差值。 它可以是下列其中一項。



| 值                                                                                                                                                                                        | 意義                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <span id="IMF_SMODE_PLAURALCLAUSE"></span><span id="imf_smode_plauralclause"></span><dl> <dt>**IMF \_ SMODE \_ PLAURALCLAUSE**</dt> </dl> | 將輸入法模式偏差設定為 Name。<br/> |
| <span id="IMF_SMODE_NONE"></span><span id="imf_smode_none"></span><dl> <dt>**IMF \_ SMODE \_ NONE**</dt> </dl>                            | 無偏差。<br/>                        |



 

</dd> <dt>

*lParam* 
</dt> <dd>

這必須與 *wParam* 的值相同。

</dd> </dl>

## <a name="return-value"></a>傳回值

此訊息會傳回新的 IME 模式偏差設定。

## <a name="remarks"></a>備註

當 IME 產生一組字元的替代挑選清單時，此訊息會設定一些選項會出現在清單頂端的準則。

若要將文字服務架構 (TSF) 模式偏差，請使用 [**EM \_ SETCTFMODEBIAS**](em-setctfmodebias.md)。

在呼叫此函式之前，應用程式應該呼叫 [**EM \_ ISIME**](em-isime.md) 。

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

[**EM \_ ISIME**](em-isime.md)
</dt> <dt>

[**EM \_ SETCTFMODEBIAS**](em-setctfmodebias.md)
</dt> </dl>

 

 






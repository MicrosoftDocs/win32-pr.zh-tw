---
title: 'EM_FINDWORDBREAK 訊息 (Richedit .h) '
description: 尋找指定字元位置之前或之後的下一個字組，或抓取位於該位置之字元的相關資訊。
ms.assetid: b5df1365-4672-4c82-8ae4-ebf8b60bf871
keywords:
- EM_FINDWORDBREAK 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- EM_FINDWORDBREAK
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8eaa2a58c8af1181ca22ddd767392749b2c838238e933c52a96268542be0240
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119541138"
---
# <a name="em_findwordbreak-message"></a>EM \_ FINDWORDBREAK 訊息

尋找指定字元位置之前或之後的下一個字組，或抓取位於該位置之字元的相關資訊。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

指定尋找作業。 此參數可以是下列其中一個值。



| 值                                                                                                                                                                  | 意義                                                                                                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WB_CLASSIFY"></span><span id="wb_classify"></span><dl> <dt>**WB \_ 分類**</dt> </dl>                | 傳回字元類別和字元在指定位置的斷詞旗標。<br/>                                                                                                                          |
| <span id="WB_ISDELIMITER"></span><span id="wb_isdelimiter"></span><dl> <dt>**WB \_ ISDELIMITER**</dt> </dl>       | 如果指定位置的字元是分隔符號，則傳回 **TRUE** ，否則傳回 **FALSE** 。<br/>                                                                                                                   |
| <span id="WB_LEFT"></span><span id="wb_left"></span><dl> <dt>**\_左 WB**</dt> </dl>                            | 尋找開頭為單字的指定位置之前的最接近字元。<br/>                                                                                                                                         |
| <span id="WB_LEFTBREAK"></span><span id="wb_leftbreak"></span><dl> <dt>**WB \_ LEFTBREAK**</dt> </dl>             | 尋找指定位置之前的下一個單字結尾。 此值與 WB \_ PREVBREAK 相同。<br/>                                                                                                                       |
| <span id="WB_MOVEWORDLEFT"></span><span id="wb_movewordleft"></span><dl> <dt>**WB \_ MOVEWORDLEFT**</dt> </dl>    | 尋找在指定位置之前的單字開頭的下一個字元。 CTRL + 向左鍵處理期間會使用這個值。 此值類似于 WB \_ MOVEWORDPREV。 如需詳細資訊，請參閱「備註」。<br/> |
| <span id="WB_MOVEWORDRIGHT"></span><span id="wb_movewordright"></span><dl> <dt>**WB \_ MOVEWORDRIGHT**</dt> </dl> | 尋找在指定位置之後開始單字的下一個字元。 此值會在 CTRL + 右按鍵處理期間使用。 此值類似于 WB \_ MOVEWORDNEXT。 如需詳細資訊，請參閱「備註」。<br/>           |
| <span id="WB_RIGHT"></span><span id="wb_right"></span><dl> <dt>**WB \_ RIGHT**</dt> </dl>                         | 尋找在指定位置之後開始單字的下一個字元。<br/>                                                                                                                                             |
| <span id="WB_RIGHTBREAK"></span><span id="wb_rightbreak"></span><dl> <dt>**WB \_ RIGHTBREAK**</dt> </dl>          | 尋找指定位置之後的下一個字組結尾分隔符號。 此值與 WB \_ NEXTBREAK 相同。<br/>                                                                                                           |



 

</dd> <dt>

*lParam* 
</dt> <dd>

以零起始的字元開始位置。

</dd> </dl>

## <a name="return-value"></a>傳回值

訊息會根據 *wParam* 參數傳回值。



| 傳回碼                                                                                    | 描述                                                                                                            |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**wParam**</dt> </dl>          | 傳回值<br/>                                                                                                |
| <dl> <dt>**WB \_ 分類**</dt> </dl>    | 傳回字元類別和字元在指定位置的斷詞旗標。<br/>                |
| <dl> <dt>**WB \_ ISDELIMITER**</dt> </dl> | 如果指定位置的字元是分隔符號，則傳回 **TRUE** ;否則會傳回 **FALSE**。<br/> |
| <dl> <dt>**別人**</dt> </dl>          | 傳回斷字的字元索引。<br/>                                                              |



 

## <a name="remarks"></a>備註

如果 *wParam* 是 WB \_ LEFT 和 WB \_ RIGHT，則斷詞程式只會在分隔符號之後尋找斷詞。 這符合編輯控制項的功能。 如果 *wParam* 是 WB \_ MOVEWORDLEFT 或 WB \_ MOVEWORDRIGHT，則斷詞程式也會比較字元類別和斷詞旗標。

如需有關字元類別和斷詞字元旗標的詳細資訊，請參閱 [單字和分行符號](using-rich-edit-controls.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



 

 






---
title: 'EM_SETTABLEPARMS 訊息 (Richedit .h) '
description: 變更資料表中資料列的參數。
ms.assetid: 6CE9B8D1-68C9-4692-8454-24BC81E9038F
keywords:
- EM_SETTABLEPARMS message Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETTABLEPARMS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86fa77774bd7fcf461fc74b479a57304a5f8ee3c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934207"
---
# <a name="em_settableparms-message"></a>EM \_ SETTABLEPARMS 訊息

變更資料表中資料列的參數。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

[**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms)結構的指標。

</dd> <dt>

*lParam* 
</dt> <dd>

[**TABLECELLPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms)結構的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

\_如果成功，則傳回 S OK，或下列其中一個錯誤碼。



| 傳回碼                                                                                    | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**E \_失敗**</dt> </dl>        | 無法進行變更。 如果控制項是純文字或單行控制項，或插入點位於數學物件內，就會發生這種情況。 如果停用資料表，或者 [**EM \_ SETEDITSTYLEEX**](em-seteditstyleex.md) 訊息設定了 **SES 的 \_ \_ 值得注意** 的值，也會發生這種情況。 <br/>                                                                                                                                                                                                                                                                              |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>   | *WParam* 或 *lParam* 為 Null 或指向不正確結構。 [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms)結構的 **cCell** 成員必須至少為1，且不能超過63。 **CbRow** 成員必須等於 `sizeof(TABLEROWPARMS)` 或 `sizeof(TABLEROWPARMS)   2*sizeof(long)` 。 第二個值是 RichEdit 4.1 **TABLEROWPARMS** 結構的大小。 **TABLEROWPARMS** 的 **cbCell** 成員必須相等 `sizeof(TABLECELLPARMS)` 。 插入點必須在資料表的開頭或在資料表資料列內，而且資料格的數目只能變更一次。 |
| <dl> <dt>**E \_OUTOFMEMORY**</dt> </dl> | 可用的記憶體不足。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



 

## <a name="remarks"></a>備註

如果資料表有多個連續的資料列，此訊息就會變更 [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms)結構之 **魚尾紋** 成員所指定的資料列數目參數。 如果 **魚尾紋** 小於0，訊息會逐一查看到資料表的結尾。 如果新的資料格計數與目前的資料格計數不同于 + 1 或1，它會插入或刪除 **TABLEROWPARMS** 的 **iCell** 成員所指定索引處的資料格。 起始資料表資料列是由字元位置所識別。 這個位置是由值大於或等於零的 **cpStartRow** 成員所指定。 除非您想要變更該資料表的參數，否則位置應該在資料表資料列中，但不能在嵌套的資料表內。 如果 **cpStartRow** 成員是1，則會由目前的選取範圍來指定字元位置。 若要這樣做，請將選取範圍放在資料表資料列內的任何位置，或選取在資料表資料列結尾有選取範圍的有效資料列。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**EM \_ GETTABLEPARMS**](em-gettableparms.md)
</dt> </dl>

 

 






---
title: 'EM_GETTABLEPARMS 訊息 (Richedit .h) '
description: 抓取資料表資料列的資料表參數，以及指定之資料格數目的資料格參數。
ms.assetid: 36ADA41B-735B-4D6E-92B1-33260C71DF73
keywords:
- EM_GETTABLEPARMS message Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETTABLEPARMS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7eb244b64258b1cf83559e21affea51b1d0c5d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843483"
---
# <a name="em_gettableparms-message"></a>EM \_ GETTABLEPARMS 訊息

抓取資料表資料列的資料表參數，以及指定之資料格數目的資料格參數。


```C++
#define EM_GETTABLEPARMS       (WM_USER + 265)
```



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



| 傳回碼                                                                                    | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**E \_失敗**</dt> </dl>        | 無法進行變更。 如果控制項是純文字或單行控制項，或插入點位於數學物件內，就會發生這種情況。 如果 [**EM \_ SETEDITSTYLEEX**](em-seteditstyleex.md) 訊息設定了「SES」（ **\_ \_ 值得注意** 的值），則也會在停用資料表時進行。 <br/>                                                                                                                                                                     |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>   | *WParam* 或 *lParam* 為 Null 或指向不正確結構。 [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms)結構的 **cbRow** 成員必須等於 `sizeof(TABLEROWPARMS)` 或 sizeof (TABLEROWPARMS) 2 \* sizeof (long) 。 第二個值是 RichEdit 4.1 **TABLEROWPARMS** 結構的大小。 **TABLEROWPARMS** 結構的 **cbCell** 成員必須相等 `sizeof(TABLECELLPARMS)` 。 查詢字元位置必須是資料表資料列分隔符號。 |
| <dl> <dt>**E \_OUTOFMEMORY**</dt> </dl> | 可用的記憶體不足。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

## <a name="remarks"></a>備註

這則訊息會取得 [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms)結構的 **cpStartRow** 成員所指定的字元位置之資料列的資料表參數，以及 [**TABLECELLPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms)結構的 **cCells** 成員所指定的資料格數目。

[**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms)結構的 **cpStartRow** 成員所指定的字元位置應該在資料表資料列的開頭，或資料表資料列的結尾分隔符號。 如果 **cpStartRow** 設定為1，則字元位置會由目前的選取範圍指定。 在這種情況下，請將選取範圍放在資料列的結尾 (在資料表資料列的資料格標記與結束分隔符號之間) ，或選取資料列。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**EM \_ SETTABLEPARMS**](em-settableparms.md)
</dt> </dl>

 

 






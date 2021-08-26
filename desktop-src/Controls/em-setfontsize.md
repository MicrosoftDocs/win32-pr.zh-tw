---
title: 'EM_SETFONTSIZE 訊息 (Richedit .h) '
description: 設定 rich edit 控制項中所選取文字的字型大小。
ms.assetid: 18d91370-12c0-4e5f-a0e9-ffde02abc966
keywords:
- EM_SETFONTSIZE 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETFONTSIZE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e646d58626a034f4764d6b9636e5b4b3eedba5befd7986eade9979c1f4a4fd5a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048458"
---
# <a name="em_setfontsize-message"></a>EM \_ SETFONTSIZE 訊息

設定 rich edit 控制項中所選取文字的字型大小。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

變更所選文字的點大小。 結果會根據下表所示的值進行四捨五入。 此參數的範圍應介於-1637 到1638之間。 產生的字型大小會在1到1638的範圍內。

</dd> <dt>

*lParam* 
</dt> <dd>

未使用此參數;它必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果未發生任何錯誤，則傳回值為 **TRUE**。

如果發生錯誤，傳回值為 **FALSE**。

## <a name="remarks"></a>備註

您可以藉由傳送 [**EM \_ GETCHARFORMAT**](em-getcharformat.md) 訊息來輕鬆取得字型大小。

Rich Edit 會先將 *wParam* 新增至目前的字型大小，然後使用產生的大小和下表來判斷舍入值。



| 樂隊    | 舍入值 |
|---------|----------------|
| <= 12 | 1              |
| 28      | 2              |
| 36      | 0              |
| 48      | 0              |
| 72      | 0              |
| 80      | 0              |
| > 80 | 10             |



 

如果產生的字型大小未以舍入值來平均整除，則會將字型大小舍入成可平均除以舍入值的數位。 因此，如果字型大小小於或等於12，則舍入值會是1。 同樣地，如果字型大小小於或等於28，則舍入值為2。 針對大於28的值，字型大小會四捨五入至下一個頻外。 因此，字型大小會跳到36、48、72、80。 80之後，會以十個點遞增的方式來完成所有四捨五入。

字型大小會根據 *wParam* 的正負號進位或下移。 如果 *wParam* 是正數，則四捨五入一律為向上。 否則，舍入一律會關閉。 因此，如果目前的字型大小為10，而 *wParam* 為3，則產生的字型大小會是 14 (10 + 3 = 13，其不能被2整除，因此大小會四捨五入為 14) 。 相反地，如果目前的字型大小為14，而 *wParam* 為-3，則產生的字型大小會是 10 (14-3 = 11，而不是由2整除，因此大小會四捨五入為 10) 。

這項變更會套用至選取專案的每個部分。 因此，如果部分文字是10pt 和某些20pt，在 *wParam* 設定為1的呼叫之後，字型大小會分別變成11pt 和22pt。

下表顯示其他範例。



| 原始字型大小 | *wParam* | 產生的字型大小 |
|--------------------|----------|---------------------|
| 7                  | 1        | 8                   |
| 7                  | 3        | 10                  |
| 10                 | 3        | 14                  |
| 14                 | -3       | 10                  |
| 28                 | 1        | 36                  |
| 28                 | 3        | 36                  |
| 80                 | 1        | 90                  |
| 80                 | -1       | 72                  |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 可轉散發套件<br/>          | Rich Edit 3。0<br/>                                                              |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**EM \_ GETCHARFORMAT**](em-getcharformat.md)
</dt> <dt>

[**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a)
</dt> <dt>

**概念**
</dt> <dt>

[關於 Rich Edit 控制項](about-rich-edit-controls.md)
</dt> </dl>

 

 






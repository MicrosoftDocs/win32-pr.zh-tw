---
description: 抓取 ICoNtextNode 物件的集合，這些物件與指定之內容節點的指定文字範圍有關。
ms.assetid: 39a5dd52-7007-4395-8668-261eca78a090
title: 'IInkAnalyzer：： GetNodesFromTextRange 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetNodesFromTextRange
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: df9eb6e1e748088abaa4780aedfded4e26977018d70dd79f518159185594a90b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057818"
---
# <a name="iinkanalyzergetnodesfromtextrange-method"></a>IInkAnalyzer：： GetNodesFromTextRange 方法

抓取 [**ICoNtextNode**](icontextnode.md) 物件的集合，這些物件與指定之內容節點的指定文字範圍有關。

## <a name="syntax"></a>語法


```C++
HRESULT GetNodesFromTextRange(
  [in, out] LONG          *plStart,
  [in, out] LONG          *plLength,
  [out]     IContextNodes **ppContextNodes,
  [in]      IContextNodes *pNodesToSearch = defaultvalue
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*plStart* \[in、out\]
</dt> <dd>

在可辨識字串的 *pNodesToSearch* 部分中，文字範圍開頭的參考。

</dd> <dt>

*plLength* \[in、out\]
</dt> <dd>

在可辨識字串的 *pNodesToSearch* 部分中，文字範圍長度的參考。

</dd> <dt>

*ppCoNtextNodes* \[擴展\]
</dt> <dd>

與指定之內容節點的指定文字範圍相關之 [**ICoNtextNode**](icontextnode.md) 物件的指標。

</dd> <dt>

*pNodesToSearch* \[在\]
</dt> <dd>

要限制搜尋的 [**ICoNtextNode**](icontextnode.md) 物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

指定的文字範圍應該相對於 [**IInkAnalyzer**](iinkanalyzer.md)字串的 *pNodesToSearch* 部分，而不是整個 **IInkAnalyzer** 的可辨識字串。

這個方法會將文字範圍展開至最接近的單字界限，藉以修改 *plStart* 和 *plLength* 參數的值。

例如，如果可辨識的字串為 "I am"，而且您使用 *plStart* 的參數值來呼叫這個方法，並使用 *plLength* 的參數值（對應至「晚期」中的字母 "a"），這個方法會傳回包含單一 [**ICoNtextNode**](icontextnode.md)的集合，也就是對應至 "晚期" 這個字的 InkWord 或 TextWord。 在此範例中，這個方法也會將 *plStart* 的值修改為5，並將 *plLength* 的值修改為對應至 "晚期" 這個字的4。

> [!Note]  
> *PlStart* 參數相對於 *pNodesToSearch* 參數的可辨識字串。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows僅限 XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                     |
| 標頭<br/>                   | <dl> <dt>IACom (也需要 IACom \_ c) </dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> </dl>

 

 





---
description: 在可辨識的字串中尋找對應于 ICoNtextNode 物件集合的文字範圍。
ms.assetid: 2c5bc4a1-08de-4872-b552-6d22924ce2a8
title: 'IInkAnalyzer：： GetTextRangeFromNodes 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetTextRangeFromNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 147877ef8871f7b07e2aa501a107c1e40bd75e80009e5bee97dca03346bb853a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092128"
---
# <a name="iinkanalyzergettextrangefromnodes-method"></a>IInkAnalyzer：： GetTextRangeFromNodes 方法

在可辨識的字串中尋找對應于 [**ICoNtextNode**](icontextnode.md) 物件集合的文字範圍。

## <a name="syntax"></a>語法


```C++
HRESULT GetTextRangeFromNodes(
  [out] LONG          *plStart,
  [out] LONG          *plLength,
  [in]  IContextNodes *pNodesToSearch
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*plStart* \[擴展\]
</dt> <dd>

表示文字範圍開頭的32位帶正負號的整數。 這個參數會以未初始化的狀態傳遞。

</dd> <dt>

*plLength* \[擴展\]
</dt> <dd>

表示文字範圍長度的32位帶正負號的整數。 這個參數會以未初始化的狀態傳遞。

</dd> <dt>

*pNodesToSearch* \[在\]
</dt> <dd>

要尋找其文字範圍之 [**ICoNtextNode**](icontextnode.md) 物件的集合。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

如果 *pNodesToSearch* 包含不連續的 [**ICoNtextNode**](icontextnode.md) 物件，這個方法會傳回最小的文字範圍，其中涵蓋所有的 **ICoNtextNode** 物件。

\_當 *pNodesToSearch* 包含未與 [**IInkAnalyzer**](iinkanalyzer.md)相關聯的 [**ICoNtextNode**](icontextnode.md)時，這個方法會擲回 E INVALIDARG 例外狀況。

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

 

 





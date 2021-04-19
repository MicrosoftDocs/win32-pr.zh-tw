---
description: 修改確認類型，以控制 IInkAnalyzer 物件可變更的 ICoNtextNode 內容。
ms.assetid: a506f27e-3909-453e-a2f3-10d4c04d78a4
title: 'ICoNtextNode：： Confirm 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.Confirm
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 3703bb735c0707c412b7c1e41c43819904d83ce8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973480"
---
# <a name="icontextnodeconfirm-method"></a>ICoNtextNode：： Confirm 方法

修改確認類型，以控制 [**IInkAnalyzer**](iinkanalyzer.md) 物件可變更的 [**ICoNtextNode**](icontextnode.md)內容。

## <a name="syntax"></a>語法


```C++
HRESULT Confirm(
  [in] ConfirmationType confirmedType
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*confirmedType* \[在\]
</dt> <dd>

套用至節點的 [**ConfirmationType**](confirmationtype.md) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

使用這個方法可讓使用者確認 [**IInkAnalyzer**](iinkanalyzer.md) 已正確分析筆劃。 在呼叫 **ICoNtextNode：： Confirm** 之後， **IInkAnalyzer** 將不會在後續分析期間變更這些筆觸的 [**ICoNtextNode**](icontextnode.md) 物件。

當使用者已確認分析結果，而不希望 [**IInkAnalyzer**](iinkanalyzer.md)在稍後的分析期間變更 [**ICoNtextNode**](icontextnode.md)時，請使用 **ICoNtextNode：： Confirm** 。 例如，如果使用者將 "to" 單字寫入，然後應用程式呼叫 [**IInkAnalyzer：：分析方法**](iinkanalyzer-analyze.md)，則筆墨分析器會產生值為 "to" 的 InkWord 節點。 如果使用者接著將 "me" 之後新增為一個單字，而應用程式再次呼叫 **IInkAnalyzer：：分析方法** ，則筆墨分析器可以移除先前的 InkWord 節點，並建立值為 "書籍" 的新 InkWord 節點。 但是，如果在第一次呼叫 **IInkAnalyzer：： Confirm 方法** 之後，應用程式會在 InkWord 節點上呼叫 **ICoNtextNode：： Confirm** （ [**ConfirmationType**](confirmationtype.md) 值 **NodeTypeAndProperties**），然後使用者加入 "Me"，然後當應用程式呼叫 **IInkAnalyzer：：分析方法** 時，筆墨分析器不會移除或變更 "to" 節點。 相反地，「筆跡分析器」可能會辨識「到」和「我」兩個 InkWord 節點。

[**ICoNtextNode**](icontextnode.md) 只能確認 InkWord 和 InkDrawing 類型的物件 (請參閱) 的 [內容節點類型](context-node-types.md) 。 當節點不是分葉節點時， **ICoNtextNode：： Confirm** 會傳回 **E \_ INVALIDARG** 。

[**IInkAnalyzer：： RemoveStroke 方法**](iinkanalyzer-removestroke.md) 和 [**IInkAnalyzer：： RemoveStrokes 方法**](iinkanalyzer-removestrokes.md) 會 unconfirm 從中移除筆劃資料的任何節點。

[**ICoNtextNode：： SetStrokes**](icontextnode-setstrokes.md)、 [**IInkAnalyzer：： SetStrokesType**](iinkanalyzer-setstrokestype.md)和 [**IInkAnalyzer：： SetStrokeType**](iinkanalyzer-setstroketype.md)如果已確認 [**INVALIDOPERATION**](icontextnode.md)物件，則傳回 **CORE \_ E \_ ICoNtextNode** 。

如果已確認來源或目的節點， [**ICoNtextNode：： ReparentStrokeByIdToNode**](icontextnode-reparentstrokebyidtonode.md)會傳回錯誤。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                     |
| 標頭<br/>                   | <dl> <dt>IACom (也需要 IACom \_ c) </dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ICoNtextNode**](icontextnode.md)
</dt> <dt>

[**ICoNtextNode::IsConfirmed**](icontextnode-isconfirmed.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

 





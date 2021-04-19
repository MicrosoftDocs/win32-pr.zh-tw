---
description: 發生于 IInkAnalyzer 將 ICoNtextNode 物件移至其父節點的子節點集合內的新位置之前。
ms.assetid: c7a5956e-ffc4-4205-9de3-e8b7d672156d
title: '_IAnalysisProxyEvents：： CoNtextNodeMovingToPosition 事件 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.ContextNodeMovingToPosition
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 462e7428fb43fd998d769dd152e19f8109b04158
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106991398"
---
# <a name="_ianalysisproxyeventscontextnodemovingtoposition-event"></a>\_IAnalysisProxyEvents：： CoNtextNodeMovingToPosition 事件

發生于 [**IInkAnalyzer**](iinkanalyzer.md) 將 [**ICoNtextNode**](icontextnode.md) 物件移至其父節點的子節點集合內的新位置之前。

## <a name="syntax"></a>語法


```C++
HRESULT ContextNodeMovingToPosition(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextNode *pISubNodeToMove,
  [in] IContextNode *pParentContextNode,
  [in] ULONG        ulNewIndex
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pInkAnalyzer* \[在\]
</dt> <dd>

移動 [**ICoNtextNode**](icontextnode.md)物件的 [**IInkAnalyzer**](iinkanalyzer.md)物件。

</dd> <dt>

*pISubNodeToMove* \[在\]
</dt> <dd>

要移動的 [**ICoNtextNode**](icontextnode.md) 物件。

</dd> <dt>

*pParentCoNtextNode* \[在\]
</dt> <dd>

*PISubNodeToMove* 的父 [**ICoNtextNode**](icontextnode.md)物件。

</dd> <dt>

*ulNewIndex* \[在\]
</dt> <dd>

*PISubNodeToMove* 在其父節點的子節點集合中的新位置。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

當您的應用程式維護自己的資料結構（與 [**IInkAnalyzer**](iinkanalyzer.md)同步處理）時，請使用此事件。 此事件發生于筆墨分析的協調階段，或為了回應在其父節點的子節點集合中移動 [**ICoNtextNode**](icontextnode.md) 的筆墨分析器方法 (參閱 [**ICoNtextNode：： GetParentNode**](icontextnode-getparentnode.md) 和 [**ICoNtextNode：： GetSubNodes**](icontextnode-getsubnodes.md)) 。

如需有關同步處理應用程式資料與 [**IInkAnalyzer**](iinkanalyzer.md)的詳細資訊，請參閱 [使用筆墨分析的資料 Proxy](data-proxy-with-ink-analysis.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                     |
| 標頭<br/>                   | <dl> <dt>IACom (也需要 IACom \_ c) </dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**\_IAnalysisProxyEvents**](-ianalysisproxyevents.md)
</dt> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**ICoNtextNode**](icontextnode.md)
</dt> <dt>

[**IInkAnalyzer：：分析方法**](iinkanalyzer-analyze.md)
</dt> <dt>

[**IInkAnalyzer：： BackgroundAnalyze 方法**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[**ICoNtextNode::GetParentNode**](icontextnode-getparentnode.md)
</dt> <dt>

[**ICoNtextNode::GetSubNodes**](icontextnode-getsubnodes.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

 





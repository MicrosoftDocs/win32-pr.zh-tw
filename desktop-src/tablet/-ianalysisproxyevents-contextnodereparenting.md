---
description: 在 IInkAnalyzer 藉由變更其父節點來移動 ICoNtextNode 物件之前發生。
ms.assetid: 91261270-aa7c-4f0a-a790-1b2bf322a3ad
title: '_IAnalysisProxyEvents：： CoNtextNodeReparenting 事件 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.ContextNodeReparenting
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: eafb37fd4083f0ecf7c68eaf45fc3339a730e818864f4be15eca4b94d4bd5b7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117857107"
---
# <a name="_ianalysisproxyeventscontextnodereparenting-event"></a>\_IAnalysisProxyEvents：： CoNtextNodeReparenting 事件

在 [**IInkAnalyzer**](iinkanalyzer.md) 藉由變更其父節點來移動 [**ICoNtextNode**](icontextnode.md) 物件之前發生。

## <a name="syntax"></a>語法


```C++
HRESULT ContextNodeReparenting(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextNode *pNewParentContextNode,
  [in] IContextNode *pContextNodeToBeReparented
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pInkAnalyzer* \[在\]
</dt> <dd>

移動 [**ICoNtextNode**](icontextnode.md)物件的 [**IInkAnalyzer**](iinkanalyzer.md)物件。

</dd> <dt>

*pNewParentCoNtextNode* \[在\]
</dt> <dd>

新的父 [**ICoNtextNode**](icontextnode.md) 物件。

</dd> <dt>

*pCoNtextNodeToBeReparented* \[在\]
</dt> <dd>

要移動的 [**ICoNtextNode**](icontextnode.md) 物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

當您的應用程式維護自己的資料結構（與 [**IInkAnalyzer**](iinkanalyzer.md)同步處理）時，請使用此事件。 此事件發生于筆墨分析的協調階段，或為了回應將 [**ICoNtextNode**](icontextnode.md) 從一個子節點集合移至 (另一個子節點的方法，請參閱 [**ICoNtextNode：： GetParentNode**](icontextnode-getparentnode.md) 和 [**ICoNtextNode：： GetSubNodes**](icontextnode-getsubnodes.md)) 。

如需有關同步處理應用程式資料與 [**IInkAnalyzer**](iinkanalyzer.md)的詳細資訊，請參閱 [使用筆墨分析的資料 Proxy](data-proxy-with-ink-analysis.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows僅限 XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                 |
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

[**ICoNtextNode::GetParentNode**](icontextnode-getparentnode.md)
</dt> <dt>

[**ICoNtextNode::GetSubNodes**](icontextnode-getsubnodes.md)
</dt> <dt>

[**IInkAnalyzer：：分析方法**](iinkanalyzer-analyze.md)
</dt> <dt>

[**IInkAnalyzer：： BackgroundAnalyze 方法**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

 





---
description: 在 IInkAnalyzer 建立 ICoNtextNode 物件之後發生。
ms.assetid: b4ba0d3b-da91-4cc7-b071-240155687b83
title: '_IAnalysisProxyEvents：： CoNtextNodeCreated 事件 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.ContextNodeCreated
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ac06a7fc45604e93408b1bb144ee7e884efd351e
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "103945737"
---
# <a name="_ianalysisproxyeventscontextnodecreated-event"></a>\_IAnalysisProxyEvents：： CoNtextNodeCreated 事件

在 [**IInkAnalyzer**](iinkanalyzer.md) 建立 [**ICoNtextNode**](icontextnode.md) 物件之後發生。

## <a name="syntax"></a>語法


```C++
HRESULT ContextNodeCreated(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextNode *pContextNodeCreated
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pInkAnalyzer* \[在\]
</dt> <dd>

建立 [**ICoNtextNode**](icontextnode.md)物件的 [**IInkAnalyzer**](iinkanalyzer.md) 。

</dd> <dt>

*pCoNtextNodeCreated* \[在\]
</dt> <dd>

新的 [**ICoNtextNode**](icontextnode.md) 物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

當您的應用程式維護自己的資料結構（與 [**IInkAnalyzer**](iinkanalyzer.md)同步處理）時，請使用此事件。 此事件發生于筆墨分析的協調階段，或為了回應建立 [**ICoNtextNode**](icontextnode.md)的筆墨分析器方法。

當 [**IInkAnalyzer**](iinkanalyzer.md) 建立 [**ICoNtextNode**](icontextnode.md)時，新的 **ICoNtextNode** 不會包含任何筆觸、不包含其他 **ICoNtextNode** 物件的連結，而且可能不會設定其所有屬性。 此外，新的 **ICoNtextNode** 會加入至其父節點的子節點集合結尾 (請參閱 [**ICoNtextNode：： GetParentNode**](icontextnode-getparentnode.md) 和 [**ICoNtextNode：： GetSubNodes**](icontextnode-getsubnodes.md)) 。 在這個事件之後， **IInkAnalyzer** 可能會引發下列事件。

-   [**\_ IAnalysisProxyEvents：： StrokeReparented**](-ianalysisproxyevents-strokereparented.md)事件將筆劃從某個內容節點移至另一個內容節點時。
-   [**\_ IAnalysisProxyEvents：： CoNtextNodeLinkAdding**](-ianalysisproxyevents-contextnodelinkadding.md)事件將 [**ICoNtextLink**](icontextlink.md)加入 [**ICoNtextNode**](icontextnode.md)時的事件。
-   [**\_ IAnalysisProxyEvents：： CoNtextNodeMovingToPosition**](-ianalysisproxyevents-contextnodemovingtoposition.md)事件，它會在其父節點的子節點集合中變更 [**ICoNtextNode**](icontextnode.md)的順序。
-   [**IInkAnalyzer**](iinkanalyzer.md)在解析此分析階段的 [**ICoNtextNode**](icontextnode.md)狀態之後，會引發 [**\_ IAnalysisProxyEvents：： CoNtextNodePropertiesUpdated**](-ianalysisproxyevents-contextnodepropertiesupdated.md)事件。

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

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

 





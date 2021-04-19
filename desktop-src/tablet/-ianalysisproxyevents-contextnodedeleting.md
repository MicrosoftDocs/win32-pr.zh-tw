---
description: 在 IInkAnalyzer 刪除 ICoNtextNode 物件之前發生。
ms.assetid: 9c89198e-cc64-4041-b7a3-457f94c4aeaf
title: '_IAnalysisProxyEvents：： CoNtextNodeDeleting 事件 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.ContextNodeDeleting
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 26488c5657b6d2765534f82b6eacae774adcf561
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106985825"
---
# <a name="_ianalysisproxyeventscontextnodedeleting-event"></a>\_IAnalysisProxyEvents：： CoNtextNodeDeleting 事件

在 [**IInkAnalyzer**](iinkanalyzer.md) 刪除 [**ICoNtextNode**](icontextnode.md) 物件之前發生。

## <a name="syntax"></a>語法


```C++
HRESULT ContextNodeDeleting(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextNode *pContextNodeToBeDeleted
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pInkAnalyzer* \[在\]
</dt> <dd>

刪除 [**ICoNtextNode**](icontextnode.md)物件的 [**IInkAnalyzer**](iinkanalyzer.md)物件。

</dd> <dt>

*pCoNtextNodeToBeDeleted* \[在\]
</dt> <dd>

要刪除的 [**ICoNtextNode**](icontextnode.md) 物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

當您的應用程式維護自己的資料結構（與 [**IInkAnalyzer**](iinkanalyzer.md)同步處理）時，請使用此事件。 此事件發生于筆墨分析的協調階段，或為了回應刪除 [**ICoNtextNode**](icontextnode.md)的筆墨分析器方法。

在 [**IInkAnalyzer**](iinkanalyzer.md) 刪除 [**ICoNtextNode**](icontextnode.md)之前， **IInkAnalyzer** 會移除內容節點的所有筆劃，並移除其他內容節點的所有連結。 在移除內容節點之前， **IInkAnalyzer** 可能會引發下列事件。

-   [**\_ IAnalysisProxyEvents：： StrokeReparented**](-ianalysisproxyevents-strokereparented.md)事件從 [**ICoNtextNode**](icontextnode.md)移動筆劃時。
-   [**\_ IAnalysisProxyEvents：： CoNtextNodeLinkDeleting**](-ianalysisproxyevents-contextnodelinkdeleting.md)事件會先從 [**ICoNtextNode**](icontextnode.md)移除 [**ICoNtextLink**](icontextlink.md) 。
-   **\_ IAnalysisProxyEvents：： CoNtextNodeDeleting** 事件在移除不再具有子節點的父內容節點之前。

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

 

 





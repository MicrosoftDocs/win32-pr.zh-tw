---
description: 發生于 IInkAnalyzer 協調分析結果之前，讓應用程式可以與 IInkAnalyzer 同步處理資料。
ms.assetid: 9daa8723-5234-40d9-ac41-6dcca988a8b4
title: '_IAnalysisProxyEvents：： InkAnalyzerStateChanging 事件 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.InkAnalyzerStateChanging
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 92535c34b5d107fb1e435e9abe229df46204f236
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106992651"
---
# <a name="_ianalysisproxyeventsinkanalyzerstatechanging-event"></a>\_IAnalysisProxyEvents：： InkAnalyzerStateChanging 事件

發生于 [**IInkAnalyzer**](iinkanalyzer.md) 協調分析結果之前，讓應用程式可以與 **IInkAnalyzer** 同步處理資料。

## <a name="syntax"></a>語法


```C++
HRESULT InkAnalyzerStateChanging(
  [in] IInkAnalyzer *pInkAnalyzer
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pInkAnalyzer* \[在\]
</dt> <dd>

即將協調其分析結果的 [**IInkAnalyzer**](iinkanalyzer.md) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

當您的應用程式維護自己的資料結構（與 [**IInkAnalyzer**](iinkanalyzer.md)同步處理）時，請使用此事件。 當 **IInkAnalyzer** 引發這個事件時，您的應用程式應該填入筆墨分析器根節點的子節點 (請參閱 [**ICoNtextNode：： GetSubNodes**](icontextnode-getsubnodes.md) 和 [**IInkAnalyzer：： GetRootNode 方法**](iinkanalyzer-getrootnode.md)) 。

[**IInkAnalyzer**](iinkanalyzer.md)引發 [**\_ IAnalysisEvents：： ReadyToReconcile**](-ianalysisevents-readytoreconcile.md)事件之後，就會引發此事件。 只有在執行背景分析時，才會引發此事件。

當 [**IInkAnalyzer**](iinkanalyzer.md)引發 **\_ IAnalysisProxyEvents：： InkAnalyzerStateChanging** 事件時，請鎖定您的資料結構。 在此分析階段中，資料結構的變更可能會導致筆跡分析和同步處理發生錯誤。 當 **IInkAnalyzer** 引發 [**\_ IAnalysisEvents：： IntermediateResults**](-ianalysisevents-intermediateresults.md)或 [**\_ IAnalysisEvents：： Results**](-ianalysisevents-results.md)事件時，請解除鎖定您的資料結構。

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

 

 





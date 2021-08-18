---
description: 將背景筆墨分析作業的結果套用至應用程式在呼叫 IInkAnalyzer：： BackgroundAnalyze 方法之後，尚未修改之樹狀結構部分的內容節點樹狀結構。
ms.assetid: 60e15d4f-6e81-48b9-b7f3-97d2de5c0c1c
title: 'IInkAnalyzer：：調解方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.Reconcile
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 3b16497a7f7822bf1557e3e686a81497a4e3723e71f115a1a7d6aa59d8381db2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092028"
---
# <a name="iinkanalyzerreconcile-method"></a>IInkAnalyzer：：調解方法

將背景筆墨分析作業的結果套用至應用程式在呼叫 [**IInkAnalyzer：： BackgroundAnalyze 方法**](iinkanalyzer-backgroundanalyze.md)之後，尚未修改之樹狀結構部分的內容節點樹狀結構。

## <a name="syntax"></a>語法


```C++
HRESULT Reconcile();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

根據預設， [**IInkAnalyzer**](iinkanalyzer.md)會在引發 [**\_ IAnalysisEvents：： IntermediateResults**](-ianalysisevents-intermediateresults.md)和 [**\_ IAnalysisEvents：： Results**](-ianalysisevents-results.md)事件之前立即執行自動調整階段。

若要停用自動調整，請清除筆墨分析器分析模式中的 **AnalysisModes \_ AutomaticReconciliation** 旗標 (查看 [**IInkAnalyzer：： SetAnalysisModes 方法**](iinkanalyzer-setanalysismodes.md) 和 [**AnalysisModes**](analysismodes.md)) 。 [**IInkAnalyzer：： BackgroundAnalyze 方法**](iinkanalyzer-backgroundanalyze.md)方法會在停用自動調整時傳回錯誤，而您的應用程式不會處理 [**\_ IAnalysisEvents：： ReadyToReconcile**](-ianalysisevents-readytoreconcile.md)事件。 您的應用程式必須先呼叫 **IInkAnalyzer：：調解方法** 方法， [**IInkAnalyzer**](iinkanalyzer.md) 才能繼續處理結果，或繼續分析對應的分析階段。

在背景分析期間，您的應用程式可以在 [**IInkAnalyzer**](iinkanalyzer.md) 物件的內容節點樹狀結構中進行變更，例如新增或移除筆劃及變更筆觸資料。 這類變更可能會使部分背景分析結果失效。 這個方法只會針對您的應用程式未變更的樹狀結構部分，將分析結果套用至分析器的內容節點樹狀結構。 這個方法也會將包含無效分析結果的區域新增至 **IInkAnalyzer** 物件的中途區域 (請參閱 [**IInkAnalyzer：： GetDirtyRegion 方法**](iinkanalyzer-getdirtyregion.md)) 。

如需使用來分析筆墨的詳細資訊，請參閱 [筆墨分析總覽](ink-analysis-overview.md)。[**AnalysisModes**](analysismodes.md)

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
</dt> <dt>

[**IInkAnalyzer：： BackgroundAnalyze 方法**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[**\_IAnalysisEvents::ReadyToReconcile**](-ianalysisevents-readytoreconcile.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

 





---
description: 當目前的中繼分析階段完成時發生。
ms.assetid: 9ade61f4-bcfe-4c49-bda1-b60aaf780935
title: '_IAnalysisEvents：： IntermediateResults 事件 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisEvents.IntermediateResults
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 33430225746ddd1a4099f89112f14f99f2b6da84
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106986681"
---
# <a name="_ianalysiseventsintermediateresults-event"></a>\_IAnalysisEvents：： IntermediateResults 事件

當目前的中繼分析階段完成時發生。

## <a name="syntax"></a>語法


```C++
HRESULT IntermediateResults(
  [in] IInkAnalyzer    *pInkAnalyzer,
  [in] IAnalysisStatus *pAnalysisStatus
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pInkAnalyzer* \[在\]
</dt> <dd>

正在執行分析的 [**IInkAnalyzer**](iinkanalyzer.md) 。

</dd> <dt>

*pAnalysisStatus* \[在\]
</dt> <dd>

代表中繼結果狀態的 [**IAnalysisStatus**](ianalysisstatus.md) 物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

[**IInkAnalyzer**](iinkanalyzer.md)會在對目前分析階段的中繼結果進行協調之後引發此事件。

如果您的應用程式維護自己的資料結構（與 [**IInkAnalyzer**](iinkanalyzer.md)同步處理），此事件表示 **IInkAnalyzer** 已完成此分析階段的內部資料變更。

當 [**IInkAnalyzer**](iinkanalyzer.md)引發 [**\_ IAnalysisProxyEvents：： InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md)事件時，請鎖定您的資料結構。 在此分析階段中，資料結構的變更可能會導致筆跡分析和同步處理發生錯誤。 當 **IInkAnalyzer** 引發 **\_ IAnalysisEvents：： IntermediateResults** 或 [**\_ IAnalysisEvents：： Results**](-ianalysisevents-results.md)事件時，您可以解除鎖定您的資料結構。

如需有關同步處理應用程式資料與 [**IInkAnalyzer**](iinkanalyzer.md)的詳細資訊，請參閱 [使用筆墨分析的資料 Proxy](data-proxy-with-ink-analysis.md)。

[**IInkAnalyzer**](iinkanalyzer.md)只會在其分析模式已設定 **AnalysisModes \_ IntermediateResults** 旗標時產生中繼結果 (請參閱 [**IInkAnalyzer：： GetAnalysisModes 方法**](iinkanalyzer-getanalysismodes.md)) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                     |
| 標頭<br/>                   | <dl> <dt>IACom (也需要 IACom \_ c) </dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**\_IAnalysisEvents**](-ianalysisevents.md)
</dt> <dt>

[**AnalysisModes**](analysismodes.md)
</dt> <dt>

[**\_IAnalysisEvents：： Results**](-ianalysisevents-results.md)
</dt> <dt>

[**\_IAnalysisProxyEvents**](-ianalysisproxyevents.md)
</dt> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IInkAnalyzer：：分析方法**](iinkanalyzer-analyze.md)
</dt> <dt>

[**IInkAnalyzer：： BackgroundAnalyze 方法**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

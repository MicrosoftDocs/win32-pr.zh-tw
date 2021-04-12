---
description: 當 IInkAnalyzer 已準備好要將其背景分析結果與目前狀態協調時，就會發生此問題。
ms.assetid: 63cf48eb-9d1e-4017-a4eb-55d811f7e6cf
title: '_IAnalysisEvents：： ReadyToReconcile 事件 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisEvents.ReadyToReconcile
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4f3144f34dc680f9bc31f51b9e6b4284a70fb9bc
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "104195793"
---
# <a name="_ianalysiseventsreadytoreconcile-event"></a>\_IAnalysisEvents：： ReadyToReconcile 事件

當 [**IInkAnalyzer**](iinkanalyzer.md) 已準備好要將其背景分析結果與目前狀態協調時，就會發生此問題。

## <a name="syntax"></a>語法


```C++
HRESULT ReadyToReconcile();
```



## <a name="parameters"></a>參數

此事件沒有任何參數。

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

設定筆墨分析器的 **AnalysisModes \_ AutomaticReconciliation** 旗標時， [**IInkAnalyzer**](iinkanalyzer.md)會執行自動調整 (請參閱 [**IInkAnalyzer：： SetAnalysisModes 方法**](iinkanalyzer-setanalysismodes.md)) 。 未設定 **AnalysisModes \_ AutomaticReconciliation** 旗標時，您的應用程式需要手動協調背景分析結果。

若要執行手動對帳，請遵循下列步驟。

1.  清除筆墨分析器的 **AnalysisModes \_ AutomaticReconciliation** 旗標。
2.  處理 **\_ IAnalysisEvents：： ReadyToReconcile** 事件。
3.  若要調解分析結果，請從 **\_ IAnalysisEvents：： ReadyToReconcile** 事件的事件處理常式呼叫 [**IInkAnalyzer：：調解方法**](iinkanalyzer-reconcile.md)方法。 若要取消目前的背景分析作業，請從 **\_ IAnalysisEvents：： ReadyToReconcile** 事件的事件處理常式呼叫 [**IInkAnalyzer：： Abort 方法**](iinkanalyzer-abort.md)方法。

[**IInkAnalyzer**](iinkanalyzer.md)會在引發 [**\_ IAnalysisProxyEvents：： InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md)事件之前引發此事件。

如需有關同步處理應用程式資料與 [**IInkAnalyzer**](iinkanalyzer.md)的詳細資訊，請參閱 [使用筆墨分析的資料 Proxy](data-proxy-with-ink-analysis.md)。

[**IInkAnalyzer**](iinkanalyzer.md)會在背景分析期間引發此事件。

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

[**\_IAnalysisProxyEvents**](-ianalysisproxyevents.md)
</dt> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IInkAnalyzer：：分析方法**](iinkanalyzer-analyze.md)
</dt> <dt>

[**IInkAnalyzer：： BackgroundAnalyze 方法**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[**IInkAnalyzer：：調解方法**](iinkanalyzer-reconcile.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

 





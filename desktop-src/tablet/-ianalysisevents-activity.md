---
description: 在呼叫 IInkAnalyzer：：分析方法或 IInkAnalyzer：： BackgroundAnalyze 方法時發生。
ms.assetid: 339b41c6-f388-4b81-b2bc-3705b39d9cc9
title: '_IAnalysisEvents：： Activity 事件 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisEvents.Activity
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: f235d3414b0d514f32b4ebd197c04a8721968a2a
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "104321703"
---
# <a name="_ianalysiseventsactivity-event"></a>\_IAnalysisEvents：： Activity 事件

在呼叫 [**IInkAnalyzer：：分析**](iinkanalyzer-analyze.md) 方法或 [**IInkAnalyzer：： BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) 方法時發生。

## <a name="syntax"></a>語法


```C++
HRESULT Activity();
```



## <a name="parameters"></a>參數

此事件沒有任何參數。

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

此事件表示 [**IInkAnalyzer**](iinkanalyzer.md) 正在執行筆墨分析。 此事件不會指出筆墨分析作業的進度。

若要執行下列任何一項，請執行 **\_ IAnalysisEvents：： Activity** 事件處理常式：

-   向使用者指出筆墨分析器正在執行筆墨分析。
-   在同步分析期間處理使用者輸入。
-   在筆跡分析期間，接收系統要求的通知，例如重新繪製應用程式的視窗。

[**IInkAnalyzer**](iinkanalyzer.md)會在版面配置分析階段以及筆跡分析的書寫和繪圖分類階段，經常引發此事件。 **IInkAnalyzer** 會在存取筆跡辨識器之前和之後的手寫辨識階段期間引發此事件。

[**IInkAnalyzer**](iinkanalyzer.md)產生的活動事件數目受下列影響：

-   [**IInkAnalyzer**](iinkanalyzer.md)適用于筆墨辨識的筆墨辨識器。
-   [**IInkAnalyzer**](iinkanalyzer.md)正在分析之筆劃的數目和長度。
-   分類為書寫的筆劃數目。

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

[**\_IAnalysisEvents**](-ianalysisevents.md)
</dt> <dt>

[**\_IAnalysisProxyEvents**](-ianalysisproxyevents.md)
</dt> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)
</dt> <dt>

[**IInkAnalyzer：：分析方法**](iinkanalyzer-analyze.md)
</dt> <dt>

[**IInkAnalyzer：： BackgroundAnalyze 方法**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

 





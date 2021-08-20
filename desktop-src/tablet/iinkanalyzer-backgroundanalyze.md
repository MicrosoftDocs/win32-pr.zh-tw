---
description: 執行非同步筆跡分析。
ms.assetid: 36427b80-5e3b-4c9a-bb49-e6b7f9301cbd
title: 'IInkAnalyzer：： BackgroundAnalyze 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.BackgroundAnalyze
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 5f52488109eaf751926fca50c0d1f3fc8702752526bbf1fc9ce12b3b1ee02a98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118044110"
---
# <a name="iinkanalyzerbackgroundanalyze-method"></a>IInkAnalyzer：： BackgroundAnalyze 方法

執行非同步筆跡分析。

## <a name="syntax"></a>語法


```C++
HRESULT BackgroundAnalyze();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

當呼叫這個方法時， [**IInkAnalyzer**](iinkanalyzer.md) 會在背景執行緒上執行筆墨分析。

這個方法會 **傳回 \_ FALSE** ，而且在下列情況下並不會啟動新的背景分析作業。

-   [**IInkAnalyzer**](iinkanalyzer.md)目前正在執行背景分析。
-   中途區域 (參閱 [**IInkAnalyzer：： GetDirtyRegion 方法**](iinkanalyzer-getdirtyregion.md)) 代表空白區域。

[**IInkAnalyzer**](iinkanalyzer.md)會在呼叫 [**IInkAnalyzer：：分析方法**](iinkanalyzer-analyze.md)或 **IInkAnalyzer：： BackgroundAnalyze 方法** 期間，分析其中途區域內的筆墨。 不過， **IInkAnalyzer** 可能會擴充分析作業，以包含鄰近區域。

這個方法會將中途區域設定為空白區域。

如果在呼叫 **IInkAnalyzer：： BackgroundAnalyze 方法** 之後將筆劃資料加入至 [**IInkAnalyzer**](iinkanalyzer.md) ， **IInkAnalyzer** 可能會在筆跡分析的協調階段期間更新中途區域。

分析模式設定 (請參閱 [**IInkAnalyzer：： GetAnalysisModes 方法**](iinkanalyzer-getanalysismodes.md)) 指定 [**IInkAnalyzer**](iinkanalyzer.md) 執行背景分析的方式。 如需筆跡分析的詳細資訊，請參閱 [筆墨分析總覽](ink-analysis-overview.md)。

在下列情況下，這個方法會傳回錯誤碼。

-   您的應用程式已在 [**IInkAnalyzer**](iinkanalyzer.md) (中設定 [**AnalysisModes**](analysismodes.md)值 **AnalysisModes \_ IntermediateResults** ，請參閱 [**IInkAnalyzer：： SetAnalysisModes 方法**](iinkanalyzer-setanalysismodes.md)) ，而且不會處理 [**\_ IAnalysisEvents：： IntermediateResults**](-ianalysisevents-intermediateresults.md)事件。
-   您的應用程式已清除 [**IInkAnalyzer**](iinkanalyzer.md)中的 [**AnalysisModes**](analysismodes.md)值 **AnalysisModes \_ AutomaticReconciliation** (請參閱 [**IInkAnalyzer：： SetAnalysisModes 方法**](iinkanalyzer-setanalysismodes.md)) ，而且不會處理 [**\_ IAnalysisEvents：： ReadyToReconcile**](-ianalysisevents-readytoreconcile.md)事件。
-   您的應用程式不會處理 [**\_ IAnalysisEvents：： Results**](-ianalysisevents-results.md)事件。
-   您的應用程式不會處理 [**\_ IAnalysisEvents：： UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md)事件。

## <a name="examples"></a>範例

下列範例會檢查筆墨分析器的中途區域，然後在中途區域不是空的情況下起始背景筆墨分析。


```C++
// Check that the ink analyzer's dirty region is not empty.
IAnalysisRegion *pDirtyRegion;
hr = this->m_spIInkAnalyzer->GetDirtyRegion(&pDirtyRegion);

if (SUCCEEDED(hr))
{
    VARIANT_BOOL bIsEmpty;
    hr = pDirtyRegion->IsEmpty(&bIsEmpty);

    if (SUCCEEDED(hr))
    {
        if (!bIsEmpty)
        {
            // Insert code that prepares the application for background
            // ink analysis here.

            // Start background ink analysis. The _IAnalysisEvents::Results
            // event signals when background ink analysis is complete.
            hr = this->m_spIInkAnalyzer->BackgroundAnalyze();
        }
    }
}

// Free the memory for the dirty region.
if (pDirtyRegion != NULL)
{
    pDirtyRegion->Release();
}
```



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

[**AnalysisModes**](analysismodes.md)
</dt> <dt>

[**IInkAnalyzer：：分析方法**](iinkanalyzer-analyze.md)
</dt> <dt>

[**IInkAnalyzer：： GetAnalysisModes 方法**](iinkanalyzer-getanalysismodes.md)
</dt> <dt>

[**IInkAnalyzer：： SetAnalysisModes 方法**](iinkanalyzer-setanalysismodes.md)
</dt> <dt>

[**IInkAnalyzer：： GetDirtyRegion 方法**](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[**IInkAnalyzer：： SetDirtyRegion 方法**](iinkanalyzer-setdirtyregion.md)
</dt> <dt>

[**IInkAnalyzer：： GetRootNode 方法**](iinkanalyzer-getrootnode.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

 





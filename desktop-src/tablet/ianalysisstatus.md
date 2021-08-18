---
description: 藉由描述分析是否成功完成，以及是否發生任何警告，來表示筆墨分析作業的狀態。
ms.assetid: 57910a1d-3472-4689-ba0d-a220145e77c4
title: 'IAnalysisStatus 介面 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisStatus
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 006b042981392ecdd52508181c7a5cde270d2e0195fe9c8b971c142361ab6081
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118719995"
---
# <a name="ianalysisstatus-interface"></a>IAnalysisStatus 介面

藉由描述分析是否成功完成，以及是否發生任何警告，來表示筆墨分析作業的狀態。

## <a name="members"></a>成員

**IAnalysisStatus** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **IAnalysisStatus** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IAnalysisStatus** 介面具有這些方法。



| 方法                                                                     | 描述                                                                                                                                                                                    |
|:---------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetAppliedChangesRegion**](ianalysisstatus-getappliedchangesregion.md) | 抓取檔的區域，該區域對應于 [**IInkAnalyzer**](iinkanalyzer.md) 物件的內容節點樹狀結構中，做為筆跡分析結果的變更。<br/> |
| [**GetWarnings**](ianalysisstatus-getwarnings.md)                         | 抓取 [**IAnalysisWarnings**](ianalysiswarnings.md) 集合，此集合會描述分析作業所產生的任何錯誤和警告。<br/>                                  |
| [**IsSuccessful**](ianalysisstatus-issuccessful.md)                       | 捕獲分析作業結果的布林值摘要。<br/>                                                                                                               |



 

## <a name="examples"></a>範例

下列範例會顯示 [**\_ IAnalysisEvents：： Results**](-ianalysisevents-results.md)事件的事件處理常式的大綱。 處理常式會檢查 [**IAnalysisStatus：： IsSuccessful**](ianalysisstatus-issuccessful.md)。 如果分析作業產生警告，處理常式會逐一查看 [**IAnalysisWarning**](ianalysiswarning.md) 物件的集合。


```C++
// _IAnalysisEvents::Results event handler.
STDMETHODIMP CMyClass::Results(
    IInkAnalyzer *pInkAnalyzer,
    IAnalysisStatus *pAnalysisStatus)
{
    // Check the status of the analysis operation.
    VARIANT_BOOL bResult = VARIANT_FALSE;
    HRESULT hr = pAnalysisStatus->IsSuccessful(&bResult);

    if( SUCCEEDED(hr) )
    {
        if( bResult )
        {
            // Insert code that handles a successful result.
        }
        else
        {
            // Get the analysis warnings.
            IAnalysisWarnings* pAnalysisWarnings = NULL;
            hr = pAnalysisStatus->GetWarnings(&pAnalysisWarnings);
            if (SUCCEEDED(hr))
            {
                // Iterate through the warning collection.
                ULONG warningCount = 0;
                hr = pAnalysisWarnings->GetCount(&warningCount);
                if (SUCCEEDED(hr))
                {
                    IAnalysisWarning *pAnalysisWarning = NULL;
                    AnalysisWarningCode analysisWarningCode;
                    for (ULONG index=0; index<warningCount; index++)
                    {
                        // Get an analysis warning.
                        hr = pAnalysisWarnings->GetAnalysisWarning(
                            index, &pAnalysisWarning);

                        if (SUCCEEDED(hr))
                        {
                            // Get the warning code for the warning.
                            hr = pAnalysisWarning->GetWarningCode(
                                &analysisWarningCode);

                            if (SUCCEEDED(hr))
                            {
                                // Insert code that handles each
                                // analysis warning.
                            }
                        }

                        // Release this reference to the analysis warning.
                        if (pAnalysisWarning != NULL)
                        {
                            pAnalysisWarning->Release();
                            pAnalysisWarning = NULL;
                        }

                        if (FAILED(hr))
                        {
                            break;
                        }
                    }
                }
            }

            // Release this reference to the analysis warnings collection.
            if (pAnalysisWarnings != NULL)
            {
                pAnalysisWarnings->Release();
                pAnalysisWarnings = NULL;
            }
        }
    }
    return hr;
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

[**IInkAnalyzer：：分析方法**](iinkanalyzer-analyze.md)
</dt> <dt>

[**IInkAnalyzer：： BackgroundAnalyze 方法**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 


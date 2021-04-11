---
description: 表示筆墨分析作業期間發生的警告或錯誤。
ms.assetid: a9b0564b-8a49-44bc-9dbc-60a2fd5b60f2
title: 'IAnalysisWarning 介面 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisWarning
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 79e865ac909d6f9ee1862926ffab06f538661d6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113400"
---
# <a name="ianalysiswarning-interface"></a>IAnalysisWarning 介面

表示筆墨分析作業期間發生的警告或錯誤。

## <a name="members"></a>成員

**IAnalysisWarning** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **IAnalysisWarning** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IAnalysisWarning** 介面具有這些方法。



| 方法                                                            | 描述                                                                                                                            |
|:------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| [**GetBackgroundError**](ianalysiswarning-getbackgrounderror.md) | 如果發生錯誤，則捕獲背景筆墨分析作業的錯誤碼。<br/>                                    |
| [**GetHint**](ianalysiswarning-gethint.md)                       | 抓取造成此警告的分析提示<br/>                                                                        |
| [**GetNodeIds**](ianalysiswarning-getnodeids.md)                 | 抓取與此警告相關聯之任何相關內容節點的識別碼。<br/>                              |
| [**GetWarningCode**](ianalysiswarning-getwarningcode.md)         | 使用 [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) 列舉來抓取發生的警告類型。<br/> |



 

## <a name="remarks"></a>備註

[**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode)列舉會描述可能發生的警告類型。 當您嘗試使用 [**IInkAnalyzer**](iinkanalyzer.md)所使用的 [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)不支援的功能時，通常會發生警告。

有些警告表示 [**IInkAnalyzer**](iinkanalyzer.md) 未完成分析作業。 如需詳細資訊，請參閱 [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode)。

## <a name="examples"></a>範例

下列範例會顯示 [**\_ IAnalysisEvents：： Results**](-ianalysisevents-results.md)事件的事件處理常式的大綱。 處理常式會檢查 [**IAnalysisStatus：： IsSuccessful**](ianalysisstatus-issuccessful.md)。 如果分析作業產生警告，處理常式會逐一查看 **IAnalysisWarning** 物件的集合。


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
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                     |
| 標頭<br/>                   | <dl> <dt>IACom (也需要 IACom \_ c) </dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IAnalysisWarnings**](ianalysiswarnings.md)
</dt> <dt>

[**AnalysisWarningCode**](analysiswarningcode.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 


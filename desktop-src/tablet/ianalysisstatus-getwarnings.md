---
description: 抓取 IAnalysisWarnings 集合，此集合會描述分析作業所產生的任何錯誤和警告。
ms.assetid: fe1258a1-c9a9-4090-a458-f5f09371057a
title: 'IAnalysisStatus：： GetWarnings 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisStatus.GetWarnings
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: f3a5ba2c7c6e0ab586861d209ebb7cae3761af4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191422"
---
# <a name="ianalysisstatusgetwarnings-method"></a>IAnalysisStatus：： GetWarnings 方法

抓取 [**IAnalysisWarnings**](ianalysiswarnings.md) 集合，此集合會描述分析作業所產生的任何錯誤和警告。

## <a name="syntax"></a>語法


```C++
HRESULT GetWarnings(
  [out] IAnalysisWarnings **ppAnalysisWarnings
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppAnalysisWarnings* \[擴展\]
</dt> <dd>

[**IAnalysisWarnings**](ianalysiswarnings.md)集合的指標，此集合會描述分析作業所產生的任何錯誤和警告。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

> [!Caution]  
> [](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) \* 當您不再需要警告時，請在 *ppAnalysisWarnings* 上呼叫 IUnknown：： Release。

 

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
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                     |
| 標頭<br/>                   | <dl> <dt>IACom (也需要 IACom \_ c) </dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IAnalysisStatus**](ianalysisstatus.md)
</dt> <dt>

[**IAnalysisWarnings**](ianalysiswarnings.md)
</dt> <dt>

[**IAnalysisWarning**](ianalysiswarning.md)
</dt> <dt>

[**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 


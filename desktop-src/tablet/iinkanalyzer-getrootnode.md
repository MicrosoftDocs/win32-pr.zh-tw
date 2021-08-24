---
description: 取得 IInkAnalyzer 物件的內容樹狀結構的根 ICoNtextNode。
ms.assetid: 6c073952-7962-4f38-89ae-f543e64e904f
title: 'IInkAnalyzer：： GetRootNode 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetRootNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 5ff2181eacd3df1d2815448a0c2d7cafce4d521fa0abbc7b26492d9c078982dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119713418"
---
# <a name="iinkanalyzergetrootnode-method"></a>IInkAnalyzer：： GetRootNode 方法

取得 [**IInkAnalyzer**](iinkanalyzer.md)物件的內容樹狀結構的根 [**ICoNtextNode**](icontextnode.md) 。

## <a name="syntax"></a>語法


```C++
HRESULT GetRootNode(
  [out] IContextNode **ppRootNode
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppRootNode* \[擴展\]
</dt> <dd>

[**IInkAnalyzer**](iinkanalyzer.md)物件的內容樹狀結構的根 [**ICoNtextNode**](icontextnode.md) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

> [!Caution]  
> 若要避免記憶體流失，當您不再需要使用根節點時，請在 *ppRootNode* 上呼叫 [**IUnknown：： Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) 。

 

[**IInkAnalyzer**](iinkanalyzer.md)會維護 [**ICoNtextNode**](icontextnode.md)物件的樹狀結構。 這些物件包含用於分析的輸入，以及分析的結果。 當首次將筆劃加入至 **IInkAnalyzer** 時， **IInkAnalyzer** 會將它們指派給類型 UnclassifiedInk 的 **ICoNtextNode** (請參閱 [**ICoNtextNode：： GetType**](icontextnode-gettype.md) 和 [內容節點類型](context-node-types.md)) 。 在分析筆劃之後， **IInkAnalyzer** 會將它們指派給樹狀結構中適當的 **ICoNtextNode** 物件。 如需使用 **IInkAnalyzer** 來分析筆墨的詳細資訊，請參閱 [筆墨分析總覽](ink-analysis-overview.md)。

## <a name="examples"></a>範例

下列範例顯示的方法會逐步解說筆墨分析器的 [**ICoNtextNode**](icontextnode.md) 結果樹狀結構。 如果 IInkAnlyzer 目前未執行筆墨分析，則方法會執行下列動作。

-   取得最前面的辨識字串。
-   取得筆墨分析器的根節點。
-   呼叫 helper 方法， `ExploreContextNode` 以檢查根節點和其子節點。


```C++
// Helper method that explores the current analysis results of an ink analyzer.
HRESULT CMyClass::ExploreAnalysisResults(
    IInkAnalyzer *pInkAnalyzer)
{
    // Check that the ink analyzer is not currently analyzing ink.
    VARIANT_BOOL bIsAnalyzing;
    HRESULT hr = pInkAnalyzer->IsAnalyzing(&bIsAnalyzing);

    if (SUCCEEDED(hr))
    {
        if (bIsAnalyzing)
        {
            return E_PENDING;
        }

        // Get the ink analyzer's best-result string.
        BSTR recognizedString = NULL;
        hr = pInkAnalyzer->GetRecognizedString(&recognizedString);

        if (SUCCEEDED(hr))
        {
            // Insert code that records the ink analyzer's best-result string here.

            // Get the ink analyzer's root node.
            IContextNode *pRootNode = NULL;
            hr = pInkAnalyzer->GetRootNode(&pRootNode);

            if (SUCCEEDED(hr))
            {
                // Call a helper method that recursively explores context
                // nodes and their subnodes.
                hr = this->ExploreContextNode(pRootNode);
            }

            // Release this reference to the root node.
            if (pRootNode != NULL)
            {
                pRootNode->Release();
                pRootNode = NULL;
            }
        }

        // Free the system resources for the recognized string.
        SysFreeString(recognizedString);
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

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**ICoNtextNode**](icontextnode.md)
</dt> <dt>

[內容節點類型](context-node-types.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 


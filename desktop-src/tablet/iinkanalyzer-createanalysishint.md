---
description: 將具有無限區域的新分析提示節點加入至 IInkAnalyzer。
ms.assetid: 4cc592c4-456f-4aa5-9a87-d9427de487f3
title: 'IInkAnalyzer：： CreateAnalysisHint 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.CreateAnalysisHint
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 041dc1a60c1eeb18d6896a6a23537ac9ebccd321
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318459"
---
# <a name="iinkanalyzercreateanalysishint-method"></a>IInkAnalyzer：： CreateAnalysisHint 方法

將具有無限區域的新分析提示節點加入至 [**IInkAnalyzer**](iinkanalyzer.md)。

## <a name="syntax"></a>語法


```C++
HRESULT CreateAnalysisHint(
  [out] IContextNode **ppAnalysisHint
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppAnalysisHint* \[擴展\]
</dt> <dd>

新的分析提示節點。

</dd> </dl>

## <a name="return-value"></a>傳回值

請參閱 [類別和介面-筆墨分析](classes-and-interfaces---ink-analysis.md) 以取得傳回值的描述。

## <a name="remarks"></a>備註

> [!Caution]  
> 若要避免記憶體流失，請在 *ppAnalysisHint* 上呼叫 [**IUnknown：： Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) （當您不再需要使用物件時）。

 

若要為 [**IInkAnalyzer**](iinkanalyzer.md)提供額外的內容資訊，您可以將分析提示加入至筆墨分析器。 分析提示可以改善辨識的精確度。 例如，您可以在表單應用程式中加入欄位的「模擬」和「指南」資訊。

這個方法會使用 AnalysisHint 的內容節點類型來建立新的 [**ICoNtextNode**](icontextnode.md) (請參閱 [**ICoNtextNode：： GetType**](icontextnode-gettype.md)) 並加入新的提示做為 [**IInkAnalyzer**](iinkanalyzer.md) 物件根節點的子節點 (請參閱 [**ICoNtextNode：： GetSubNodes**](icontextnode-getsubnodes.md) 和 [**IInkAnalyzer：： GetRootNode 方法**](iinkanalyzer-getrootnode.md)) 。

若要將內容資訊加入至提示，請使用 [**ICoNtextNode：： AddPropertyData**](icontextnode-addpropertydata.md) ，並將 *pPropertyDataId* 參數設定為其中一個 [分析提示屬性](analysis-hint-properties.md) 常數。

如果提示指派了一個無限區域（稱為全域提示），則 [**IInkAnalyzer**](iinkanalyzer.md) 會將提示的內容套用至不在另一個提示區域內的所有筆墨。 多個提示可能會附加至單一 **IInkAnalyzer**。 不過，只有一個全域提示可以附加至單一筆墨分析器，而且沒有任何非全域提示可以重迭。 如需有關提示可提供之內容資訊類型的詳細資訊，請參閱 [分析提示屬性](analysis-hint-properties.md)。

新增分析提示並不會標示提示的區域以進行 reanalysis。 若要標記 reanalysis 提示內的區域，請使用 [**IInkAnalyzer：： SetDirtyRegion 方法**](iinkanalyzer-setdirtyregion.md) ，將中途區域設定為目前中途區域和分析提示區域的聯集。

使用表單應用程式的提示時，應用程式應該避免在表單中混合文字內容與筆跡。 這表示，不應該在分析樹狀結構中建立文字欄位名稱。 提示的目的是要將筆墨與頁面上的區域產生關聯;任何文字內容會干擾這個筆墨與提示關聯。 分析作業可能會在相同的書寫區域中合併筆跡和文字內容，這會使筆墨無法與提示區域相關聯。

如需筆跡分析的詳細資訊，請參閱 [筆墨分析總覽](ink-analysis-overview.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                     |
| 標頭<br/>                   | <dl> <dt>IACom (也需要 IACom \_ c) </dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**ICoNtextNode::AddPropertyData**](icontextnode-addpropertydata.md)
</dt> <dt>

[**IInkAnalyzer：:D eleteAnalysisHint 方法**](iinkanalyzer-deleteanalysishint.md)
</dt> <dt>

[**IInkAnalyzer：： GetAnalysisHints 方法**](iinkanalyzer-getanalysishints.md)
</dt> <dt>

[**IInkAnalyzer：： GetAnalysisHintsByName 方法**](iinkanalyzer-getanalysishintsbyname.md)
</dt> <dt>

[分析提示屬性](analysis-hint-properties.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 


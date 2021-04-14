---
description: 將儲存的分析結果載入 IInkAnalyzer 中。
ms.assetid: 7634dbe2-1857-497c-81b5-76b92fed862d
title: 'IInkAnalyzer：： LoadResults 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.LoadResults
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 76c7fed63b38f1b4fc058fbe7676a727c2d47f19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104469124"
---
# <a name="iinkanalyzerloadresults-method"></a>IInkAnalyzer：： LoadResults 方法

將儲存的分析結果載入 [**IInkAnalyzer**](iinkanalyzer.md)中。

## <a name="syntax"></a>語法


```C++
HRESULT LoadResults(
  [in]          ULONG        ulDataSize,
  [in]          BYTE         *pbSerializedResults,
  [in]          ULONG        ulStrokeIdsCount,
  [in]          LONG         *plOriginalStrokeIds,
  [in]          LONG         *plNewStrokeIds,
  [out, retval] VARIANT_BOOL *pfSuccessful
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ulDataSize* \[在\]
</dt> <dd>

*PbSerializedResults* 中的位元組數目。

</dd> <dt>

*pbSerializedResults* \[在\]
</dt> <dd>

序列化分析結果。

</dd> <dt>

*ulStrokeIdsCount* \[在\]
</dt> <dd>

筆觸識別碼的數目。

</dd> <dt>

*plOriginalStrokeIds* \[在\]
</dt> <dd>

原始筆觸識別碼的陣列。

</dd> <dt>

*plNewStrokeIds* \[在\]
</dt> <dd>

新筆劃識別碼的陣列。

</dd> <dt>

*pfSuccessful* \[退出，retval\]
</dt> <dd>

**變異 \_** 如果載入成功則為 TRUE;否則， **VARIANT \_ FALSE**。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

當 [**IInkAnalyzer**](iinkanalyzer.md) 從儲存的結果加入 [**ICoNtextNode**](icontextnode.md) 時，它會將新的全域唯一識別碼 (GUID) 指派給 **ICoNtextNode** (請參閱 [**ICoNtextNode：： GetPropertyData**](icontextnode-getpropertydata.md) 和 [內容節點屬性](context-node-properties.md)) 。

這個方法會將已儲存的分析結果新增至現有的 [**ICoNtextNode**](icontextnode.md) 樹狀結構。 為了確保合併的結果順序正確，請將包含已載入內容節點的區域加入至 [**IInkAnalyzer**](iinkanalyzer.md) 物件的中途區域 (請參閱 [**IInkAnalyzer：： GetDirtyRegion 方法**](iinkanalyzer-getdirtyregion.md)) 和重新分析筆墨。

[**IInkAnalyzer：： SaveResults 方法**](iinkanalyzer-saveresults.md)、 [**IInkAnalyzer：： SaveResultsForNodes 方法**](iinkanalyzer-saveresultsfornodes.md)和 [**IInkAnalyzer：： SaveResultsForStrokes 方法**](iinkanalyzer-saveresultsforstrokes.md)方法不會儲存封包資料和分析結果。

*PlOriginalStrokeIds* 中的每個識別碼都是儲存分析結果中筆劃的筆觸識別碼。 *PlNewStrokeIds* 中的每個識別碼都是新的識別碼，用來取代載入的分析結果中的原始識別碼。

如果已儲存的分析提示與現有的分析提示發生衝突，則 [**IInkAnalyzer**](iinkanalyzer.md) 不會載入儲存的提示，但會載入其餘的儲存結果。 但是，如果 **IInkAnalyzer** 在 **IInkAnalyzer** 未載入的已儲存分析提示區域內載入筆觸的結果，則 **IInkAnalyzer** 會將筆劃的周框方塊加入 **IInkAnalyzer** 物件的已變更區域。 此外，如果 **IInkAnalyzer** 為現有分析提示區域內的筆劃載入結果， **IInkAnalyzer** 也會將筆劃的周框方塊新增至 **IInkAnalyzer** 物件的已變更區域。 如需有關分析提示的詳細資訊，請參閱 [分析提示屬性](analysis-hint-properties.md)。

當載入儲存的結果時，這個方法可能會引發 [**\_ IAnalysisProxyEvents：： CoNtextNodeCreated**](-ianalysisproxyevents-contextnodecreated.md)、 [**\_ IAnalysisProxyEvents：： CoNtextNodeLinkAdding**](-ianalysisproxyevents-contextnodelinkadding.md)和 [**\_ IAnalysisProxyEvents：： CoNtextNodePropertiesUpdated**](-ianalysisproxyevents-contextnodepropertiesupdated.md)事件。

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

[**ICoNtextNode**](icontextnode.md)
</dt> <dt>

[**IInkAnalyzer：： GetDirtyRegion 方法**](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[**IInkAnalyzer：： SetDirtyRegion 方法**](iinkanalyzer-setdirtyregion.md)
</dt> <dt>

[**IInkAnalyzer：： SaveResults 方法**](iinkanalyzer-saveresults.md)
</dt> <dt>

[**IInkAnalyzer：： SaveResultsForNodes 方法**](iinkanalyzer-saveresultsfornodes.md)
</dt> <dt>

[**IInkAnalyzer：： SaveResultsForStrokes 方法**](iinkanalyzer-saveresultsforstrokes.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

 





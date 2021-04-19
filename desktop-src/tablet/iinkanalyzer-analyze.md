---
description: 執行同步筆墨分析。
ms.assetid: 957845f3-96b4-4184-aaec-e266cbe47e46
title: 'IInkAnalyzer：：分析方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.Analyze
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 2867064067b902105508a7742c6fec88fdcd58be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971412"
---
# <a name="iinkanalyzeranalyze-method"></a>IInkAnalyzer：：分析方法

執行同步筆墨分析。

## <a name="syntax"></a>語法


```C++
HRESULT Analyze(
  [out] IAnalysisStatus **ppStatus
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppStatus* \[擴展\]
</dt> <dd>

描述分析作業狀態之 [**IAnalysisStatus**](ianalysisstatus.md) 的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

> [!Caution]  
> 若要避免記憶體流失，當您不再需要流量分析狀態時，請在 *ppStatus* 上呼叫 [**IUnknown：： Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) 。

 

這個方法會啟動同步的筆墨分析作業。 筆墨分析包括版面配置分析、書寫和繪圖分類，以及手寫辨識。 完成分析作業之後，這個方法會傳回。

如果 *ppStatus* 為 **Null**，則這個方法會傳回 **E \_ 指標**。

在呼叫 **IInkAnalyzer：：分析方法** 或 [**IInkAnalyzer：： BackgroundAnalyze 方法**](iinkanalyzer-backgroundanalyze.md)期間， [**IInkAnalyzer**](iinkanalyzer.md) 會分析其中途區域內的筆墨 (請參閱 [**IInkAnalyzer：： GetDirtyRegion 方法**](iinkanalyzer-getdirtyregion.md)) 。 不過， **IInkAnalyzer** 可能會擴充分析作業，以包含鄰近區域。

這個方法會將 [**IInkAnalyzer**](iinkanalyzer.md) 物件的中途區域設定為空白區域。 如果另一個執行緒已新增尚未分析的筆劃資料， **IInkAnalyzer** 會在分析的協調階段期間，將 unanalyzed 筆觸的周框方塊加入其中途區域中。

如果您的應用程式不會處理 [**\_ IAnalysisEvents：： UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md)事件，這個方法會傳回錯誤。

[**IInkAnalyzer**](iinkanalyzer.md)不會引發 [**\_ IAnalysisEvents：： Results**](-ianalysisevents-results.md)和 [**\_ IAnalysisEvents：： IntermediateResults**](-ianalysisevents-intermediateresults.md)事件以回應這個方法。

若要修改筆跡分析的執行方式，請使用 [**IInkAnalyzer：： SetAnalysisModes 方法**](iinkanalyzer-setanalysismodes.md)。

如需筆跡分析的詳細資訊，請參閱 [筆墨分析總覽](ink-analysis-overview.md)。

## <a name="examples"></a>範例

下列範例會執行前景筆墨分析。


```C++
// Perform synchronous ink analysis.
IAnalysisStatus *pAnalysisStatus = NULL;
hr = this->m_spIInkAnalyzer->Analyze(&pAnalysisStatus);

if (SUCCEEDED(hr))
{
    // Insert code that processes the analysis results.
}

// Release this reference to the analysis status.
if (pAnalysisStatus != NULL)
{
    pAnalysisStatus->Release();
    pAnalysisStatus = NULL;
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

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**AnalysisModes**](analysismodes.md)
</dt> <dt>

[**IInkAnalyzer：： GetDirtyRegion 方法**](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[**IInkAnalyzer：： SetDirtyRegion 方法**](iinkanalyzer-setdirtyregion.md)
</dt> <dt>

[**IInkAnalyzer：： GetRootNode 方法**](iinkanalyzer-getrootnode.md)
</dt> <dt>

[**IInkAnalyzer：： BackgroundAnalyze 方法**](iinkanalyzer-backgroundanalyze.md)
</dt> </dl>

 


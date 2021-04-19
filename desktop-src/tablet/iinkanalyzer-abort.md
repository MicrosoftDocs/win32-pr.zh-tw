---
description: 取消目前的分析作業。
ms.assetid: 909bfa66-b6df-4730-95b7-809fc2170e85
title: 'IInkAnalyzer：： Abort 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.Abort
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: eac96809bfbe41e7d6a070782da3ffd0f6407c60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106998071"
---
# <a name="iinkanalyzerabort-method"></a>IInkAnalyzer：： Abort 方法

取消目前的分析作業。

## <a name="syntax"></a>語法


```C++
HRESULT Abort(
  [out] IAnalysisRegion **ppAbortedRegion
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppAbortedRegion* \[擴展\]
</dt> <dd>

[**IAnalysisRegion**](ianalysisregion.md)的指標，代表中途區域 (參閱 [**IInkAnalyzer：： GetDirtyRegion 方法**](iinkanalyzer-getdirtyregion.md)) 目前的分析作業。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

當您不再需要使用物件時，請在 *ppAbortedRegion* 上呼叫 [**IUnknown：： Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) 。

這個方法會取消目前的分析作業。

當 *ppAbortedRegion* 為 **Null** 時，這個方法會正常執行中止，因為這表示呼叫端對傳回值沒有任何意義。

**IInkAnalyzer：： Abort 方法** 會讓閉嘴目前分析作業的 [**\_ IAnalysisEvents：： Results**](-ianalysisevents-results.md)和 [**\_ IAnalysisEvents：： Activity**](-ianalysisevents-activity.md)事件。

**IInkAnalyzer：： Abort 方法** 會以非同步方式執行，直到目前的背景分析作業取消為止。 由於取消程式是非同步，因此應用程式可以在目前的分析操作就取消時執行其他工作。

如果沒有進行中的分析作業，這個方法會傳回空白的分析區域。

如果有一個分析作業正在進行中，這個方法就會取消作業。

如果同步和非同步分析作業正在進行中，此方法會取消同步作業。

如果針對相同的分析作業呼叫這個方法一次以上，第一個呼叫會傳回作業的中途區域，而後續的呼叫會傳回空白區域。

如果您的應用程式維護本身與 [**IInkAnalyzer**](iinkanalyzer.md)同步處理的資料結構，則呼叫 **IInkAnalyzer：： Abort 方法** 可能會讓您的檔具有部分結果。 若要避免這種情況，請不要在 **IInkAnalyzer** 收到 [**\_ IAnalysisProxyEvents：： InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md)事件和 **IInkAnalyzer** 收到 [**\_ IAnalysisEvents：： IntermediateResults**](-ianalysisevents-intermediateresults.md)或 [**\_ IAnalysisEvents：： Results**](-ianalysisevents-results.md)事件的時間之間呼叫 **IInkAnalyzer：： Abort 方法**。

如需有關同步處理您的應用程式資料與筆墨分析器的詳細資訊，請參閱 [使用筆墨分析的資料 Proxy](data-proxy-with-ink-analysis.md)。

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

[**IInkAnalyzer：：分析方法**](iinkanalyzer-analyze.md)
</dt> <dt>

[**IInkAnalyzer：： BackgroundAnalyze 方法**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[**IInkAnalyzer：： GetDirtyRegion 方法**](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[**IInkAnalyzer：： SetDirtyRegion 方法**](iinkanalyzer-setdirtyregion.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 


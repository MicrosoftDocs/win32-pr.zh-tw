---
description: 指定與 IInkAnalyzer 物件的分析步驟相關聯的事件。
ms.assetid: 8cb75f99-aa39-44d1-a055-dc1fb3f6b292
title: _IAnalysisEvents 介面
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisEvents
api_type:
- COM
api_location: ''
ms.openlocfilehash: 90e32669d8b542202f6166052c072f224bb2954a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988881"
---
# <a name="_ianalysisevents-interface"></a>\_IAnalysisEvents 介面

指定與 [**IInkAnalyzer**](iinkanalyzer.md) 物件的分析步驟相關聯的事件。

-   [事件](/windows)

### <a name="events"></a>事件

**\_ IAnalysisEvents** 介面具有這些事件。



| 事件                                                               | 描述                                                                                                                                                                                    |
|:--------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**活動**](-ianalysisevents-activity.md)                       | 在呼叫 [**IInkAnalyzer：：分析方法**](iinkanalyzer-analyze.md) 或 [**IInkAnalyzer：： BackgroundAnalyze 方法**](iinkanalyzer-backgroundanalyze.md) 方法期間發生。<br/> |
| [**IntermediateResults**](-ianalysisevents-intermediateresults.md) | 當目前的中繼分析階段完成時發生。<br/>                                                                                                                    |
| [**ReadyToReconcile**](-ianalysisevents-readytoreconcile.md)       | 當 [**IInkAnalyzer**](iinkanalyzer.md) 已準備好要將其背景分析結果與目前狀態協調時，就會發生此問題。<br/>                                                  |
| [**結果**](-ianalysisevents-results.md)                         | 在最後一個分析階段完成時發生。<br/>                                                                                                                                   |
| [**UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md)   | 在 [**IInkAnalyzer**](iinkanalyzer.md) 存取筆劃資料之前發生。<br/>                                                                                                        |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/> |
| 最低支援的伺服器<br/> | 都不支援<br/>                                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**\_IAnalysisProxyEvents**](-ianalysisproxyevents.md)
</dt> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IInkAnalyzer：：分析方法**](iinkanalyzer-analyze.md)
</dt> <dt>

[**IInkAnalyzer：： BackgroundAnalyze 方法**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 


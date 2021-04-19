---
description: 指定與 IInkAnalyzer 物件的資料 proxy 步驟相關聯的事件。
ms.assetid: 57fee525-02e2-4721-b6e5-28112d53db2a
title: '_IAnalysisProxyEvents 介面 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4b83019cafb6053b9f803c815289d9f9f64d32a5
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106992654"
---
# <a name="_ianalysisproxyevents-interface"></a>\_IAnalysisProxyEvents 介面

指定與 [**IInkAnalyzer**](iinkanalyzer.md) 物件的資料 proxy 步驟相關聯的事件。

-   [事件](/windows)

### <a name="events"></a>事件

**\_ IAnalysisProxyEvents** 介面具有這些事件。



| 事件                                                                                      | 描述                                                                                                                                                                               |
|:-------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CoNtextNodeCreated**](-ianalysisproxyevents-contextnodecreated.md)                     | 在 [**IInkAnalyzer**](iinkanalyzer.md) 建立 [**ICoNtextNode**](icontextnode.md) 物件之後發生。<br/>                                                                  |
| [**CoNtextNodeDeleting**](-ianalysisproxyevents-contextnodedeleting.md)                   | 在 [**IInkAnalyzer**](iinkanalyzer.md) 刪除 [**ICoNtextNode**](icontextnode.md) 物件之前發生。<br/>                                                                 |
| [**CoNtextNodeLinkAdding**](-ianalysisproxyevents-contextnodelinkadding.md)               | 在 [**IInkAnalyzer**](iinkanalyzer.md)于兩個 [**ICoNtextNode**](icontextnode.md)物件之間加入 [**ICoNtextLink**](icontextlink.md)物件之前發生。<br/>           |
| [**CoNtextNodeLinkDeleting**](-ianalysisproxyevents-contextnodelinkdeleting.md)           | 在 [**IInkAnalyzer**](iinkanalyzer.md)刪除兩個 [**ICoNtextNode**](icontextnode.md)物件之間的 [**ICoNtextLink**](icontextlink.md)物件之前發生。<br/>         |
| [**CoNtextNodeMovingToPosition**](-ianalysisproxyevents-contextnodemovingtoposition.md)   | 發生于 [**IInkAnalyzer**](iinkanalyzer.md) 將 [**ICoNtextNode**](icontextnode.md) 物件移至其父節點的子節點集合內的新位置之前。<br/> |
| [**CoNtextNodePropertiesUpdated**](-ianalysisproxyevents-contextnodepropertiesupdated.md) | 在 [**IInkAnalyzer**](iinkanalyzer.md) 更新 [**ICoNtextNode**](icontextnode.md) 物件的一或多個屬性之後發生。<br/>                                        |
| [**CoNtextNodeReparenting**](-ianalysisproxyevents-contextnodereparenting.md)             | 在 [**IInkAnalyzer**](iinkanalyzer.md) 藉由變更其父節點來移動 [**ICoNtextNode**](icontextnode.md) 物件之前發生。<br/>                                       |
| [**InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md)         | 發生于 [**IInkAnalyzer**](iinkanalyzer.md) 協調分析結果之前，讓應用程式可以與 **IInkAnalyzer** 同步處理資料。<br/>                      |
| [**PopulateCoNtextNode**](-ianalysisproxyevents-populatecontextnode.md)                   | 發生于 [**IInkAnalyzer**](iinkanalyzer.md) 在部分填入的 [**ICoNtextNode**](icontextnode.md) 物件區域內執行分析之前。<br/>               |
| [**StrokeReparented**](-ianalysisproxyevents-strokereparented.md)                         | 當 [**IInkAnalyzer**](iinkanalyzer.md) 將筆劃從一個 [**ICoNtextNode**](icontextnode.md) 物件移動到另一個時，就會發生。<br/>                                           |



 

## <a name="remarks"></a>備註

當您的應用程式維護自己的資料結構（與 [**IInkAnalyzer**](iinkanalyzer.md)同步處理）時，請使用這些事件。 如需有關同步處理應用程式資料與 **IInkAnalyzer** 的詳細資訊，請參閱 [使用筆墨分析的資料 Proxy](data-proxy-with-ink-analysis.md)。

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

[**IInkAnalyzer：：分析方法**](iinkanalyzer-analyze.md)
</dt> <dt>

[**IInkAnalyzer：： BackgroundAnalyze 方法**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[\_IAnalysisEvents](-ianalysisevents.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 


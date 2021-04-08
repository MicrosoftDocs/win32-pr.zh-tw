---
description: 控制篩選圖形的介面
ms.assetid: f7de0165-e356-45d5-baed-d127caeebaf6
title: 控制篩選圖形的介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61e88dc4ba2143bbbf33a58763a5ff9005254236
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103688231"
---
# <a name="interfaces-for-controlling-a-filter-graph"></a>控制篩選圖形的介面

這些介面提供控制篩選圖形的方法。



| 介面                                  | 描述                                                                                               |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [**IAMClockAdjust**](/windows/desktop/api/Strmif/nn-strmif-iamclockadjust)   | 調整圖形時鐘。                                                                                   |
| [**IAMGraphStreams**](/windows/desktop/api/Strmif/nn-strmif-iamgraphstreams) | 同步處理篩選圖形中的即時資料流。                                                               |
| [**IFilterChain**](/windows/desktop/api/Strmif/nn-strmif-ifilterchain)       | 控制篩選準則的鏈。                                                                                |
| [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol)     | 執行、暫停和停止篩選圖形。  (也提供自動化相容的方法來建立圖形。 )  |
| [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex)     | 回應圖形中的事件。                                                                           |
| [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)     | 在檔案中搜尋。                                                                                       |
| [**IQueueCommand**](/windows/desktop/api/Control/nn-control-iqueuecommand)     | 稍後要執行的佇列命令。                                                                    |
| [**IVideoFrameStep**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep) | 畫面-逐步執行影片串流。                                                                        |



 

 

 




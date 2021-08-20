---
description: 用來控制篩選 Graph 的介面
ms.assetid: f7de0165-e356-45d5-baed-d127caeebaf6
title: 用來控制篩選 Graph 的介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec8170b8d2da80272a5620abe163f938e53105cc5b471593a3799d4c36069fe1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118154089"
---
# <a name="interfaces-for-controlling-a-filter-graph"></a>用來控制篩選 Graph 的介面

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



 

 

 




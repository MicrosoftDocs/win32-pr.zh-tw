---
description: 建立篩選圖形的介面
ms.assetid: 18d5217a-7f4e-49e9-ac14-2f4ba229e065
title: 建立篩選圖形的介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 862d581f44a711cc6f2aa094210571995b15005b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103687683"
---
# <a name="interfaces-for-building-filter-graphs"></a>建立篩選圖形的介面

應用程式會使用這些介面來建立各種類型的篩選圖形。



| 介面                                                  | 描述                                                 |
|------------------------------------------------------------|-------------------------------------------------------------|
| [**IAMFilterGraphCallback**](/windows/desktop/api/Strmif/nn-strmif-iamfiltergraphcallback)   | 如果無法轉譯 pin，則接收回呼通知。 |
| [**IAMGraphBuilderCallback**](/windows/desktop/api/Strmif/nn-strmif-iamgraphbuildercallback) | 在圖形建立期間提供回呼機制。        |
| [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2)     | 影片捕獲的組建篩選圖形。                      |
| [**ICreateDevEnum**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum)                   | 列舉系統裝置，例如「捕獲裝置」。          |
| [**IDvdGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-idvdgraphbuilder)               | 建立 DVD 流覽和播放的篩選圖形。        |
| [**IEnumFilters**](/windows/desktop/api/Strmif/nn-strmif-ienumfilters)                       | 列舉圖形中的篩選準則。                         |
| [**IFilterGraph2**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph2)                     | 加入、移除或連接篩選。                            |
| [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2)                   | 列舉在使用者的系統上註冊的篩選準則。      |
| [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder)                     | 建立檔案播放或自訂用途的篩選圖形。   |
| [**IGraphConfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig)                       | 以動態方式重新設定篩選圖形。                     |
| [**IGraphVersion**](/windows/desktop/api/Strmif/nn-strmif-igraphversion)                     | 判斷圖形何時變更。                           |



 

 

 




---
description: 篩選圖形管理員
ms.assetid: b1a53193-27c6-4e86-a5b9-f3c1e4401690
title: 篩選圖形管理員
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7161f15ea04e1404425d4671ca7991420e0aa993
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103845791"
---
# <a name="filter-graph-manager"></a>篩選圖形管理員

篩選圖形管理員會建立和控制篩選圖形。 此物件是 DirectShow 中的主要元件。 應用程式會使用它來建立和控制篩選圖形。 篩選圖形管理員也會處理同步處理、事件通知，以及控制篩選圖形的其他層面。 藉由呼叫 **CoCreateInstance** 來建立此物件。

### <a name="clsid"></a>CLSID

有兩個 Clsid 可用於建立篩選圖形管理員：



| CLSID                      | Description                                                 |
|----------------------------|-------------------------------------------------------------|
| CLSID \_ FilterGraph         | 在共用背景工作執行緒上建立篩選圖形管理員。 |
| CLSID \_ FilterGraphNoThread | 在應用程式執行緒上建立篩選圖形管理員。 |



 

一般而言，應用程式應該使用 CLSID \_ FilterGraph。 這兩個 Clsid 都會建立相同的物件，但會使用不同的執行緒模型：

-   CLSID \_ FilterGraph 會在背景工作執行緒上建立篩選圖形管理員，該執行緒會由 \_ 相同進程內的所有 CLSID FilterGraph 實例共用。 執行緒會分派篩選所傳送的訊息，並控制篩選器所建立之任何視窗的存留期。
-   CLSID \_ FilterGraphNoThread 會在應用程式的執行緒上建立篩選圖形管理員。 如果您使用此 CLSID，呼叫 **CoCreateInstance** 的執行緒必須有可分派訊息的訊息迴圈;否則，可能會發生鎖死。 此外，在應用程式執行緒結束之前，它必須釋放篩選圖形管理員和所有繪圖物件 (例如篩選、釘選、參考時鐘等等) 。

### <a name="interfaces"></a>介面

篩選圖形管理員會公開下列介面：

-   [**IAMGraphStreams**](/windows/desktop/api/Strmif/nn-strmif-iamgraphstreams)
-   [**IAMStats**](/windows/desktop/api/Control/nn-control-iamstats)
-   [**IBasicAudio**](/windows/desktop/api/Control/nn-control-ibasicaudio)
-   [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo)
-   [**IBasicVideo2**](/windows/desktop/api/Control/nn-control-ibasicvideo2)
-   [**IFilterChain**](/windows/desktop/api/Strmif/nn-strmif-ifilterchain)
-   [**IFilterGraph**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph)
-   [**IFilterGraph2**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph2)
-   [**IFilterGraph3**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph3)
-   [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2)
-   [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder)
-   [**IGraphConfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig)
-   [**IGraphVersion**](/windows/desktop/api/Strmif/nn-strmif-igraphversion)
-   [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol)
-   [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent)
-   [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex)
-   [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink)
-   [**IMediaFilter**](/windows/desktop/api/Strmif/nn-strmif-imediafilter)
-   [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition)
-   [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)
-   [**IQueueCommand**](/windows/desktop/api/Control/nn-control-iqueuecommand)
-   [**IRegisterServiceProvider**](/windows/desktop/api/Strmif/nn-strmif-iregisterserviceprovider)
-   [**IResourceManager**](/windows/desktop/api/Strmif/nn-strmif-iresourcemanager)
-   **IServiceProvider**
-   [**IVideoFrameStep**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep)
-   [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow 物件](directshow-objects.md)
</dt> </dl>

 

 




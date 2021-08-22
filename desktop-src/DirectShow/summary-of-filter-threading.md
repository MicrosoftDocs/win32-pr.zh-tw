---
description: 篩選準則執行緒的摘要
ms.assetid: b7e42101-75c9-428d-9dc7-e625242dbc1e
title: 篩選準則執行緒的摘要
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 048c151ed5fe69eea4cb0c81d01f43e97790b7223970791d3717adb9e15bea41
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951737"
---
# <a name="summary-of-filter-threading"></a>篩選準則執行緒的摘要

在串流執行緒上呼叫下列方法：

-   [**IMemInputPin：： Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive)
-   [**IMemInputPin::ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple)
-   [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)
-   [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment)
-   [**IMemAllocator：： GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer)

應用程式執行緒會呼叫下列方法：

-   狀態變更： [**IBaseFilter：： JoinFilterGraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph)、 [**IMediaFilter：:P ause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause)、 [**IMediaFilter：： Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run)、 [**IMediaFilter：： Stop**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop)、 [**IQualityControl：： SetSink**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink)。
-   參考時鐘： [**IMediaFilter：： GetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getsyncsource)， [**IMediaFilter：： SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource)。
-   Pin 作業： [**IBaseFilter：： FindPin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin)、 [**IPin：：連線**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect)、 [**IPin：： ConnectedTo**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto)、 [**IPin：： ConnectionMediaType**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectionmediatype)、 [**IPin：:D isconnect**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect)、 [**IPin：： ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection)。
-   配置器函數： [**IMemInputPin：： GetAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator)， [**IMemInputPin：： NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator)。
-   排清： [**IPin：： BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush)， [**IPin：： EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush)。

此清單未涵蓋全部種類。 當您執行篩選時，您必須考慮哪些方法會變更篩選狀態，以及哪些方法會執行串流作業。

 

 




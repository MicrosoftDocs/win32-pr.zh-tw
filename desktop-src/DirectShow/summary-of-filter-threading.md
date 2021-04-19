---
description: 篩選準則執行緒的摘要
ms.assetid: b7e42101-75c9-428d-9dc7-e625242dbc1e
title: 篩選準則執行緒的摘要
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa0a7c4ce19c46a0f7b05db3cb4d82e8f2aa0beb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106999942"
---
# <a name="summary-of-filter-threading"></a><span data-ttu-id="2c688-103">篩選準則執行緒的摘要</span><span class="sxs-lookup"><span data-stu-id="2c688-103">Summary of Filter Threading</span></span>

<span data-ttu-id="2c688-104">在串流執行緒上呼叫下列方法：</span><span class="sxs-lookup"><span data-stu-id="2c688-104">The following methods are called on the streaming thread:</span></span>

-   [<span data-ttu-id="2c688-105">**IMemInputPin：： Receive**</span><span class="sxs-lookup"><span data-stu-id="2c688-105">**IMemInputPin::Receive**</span></span>](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive)
-   [<span data-ttu-id="2c688-106">**IMemInputPin::ReceiveMultiple**</span><span class="sxs-lookup"><span data-stu-id="2c688-106">**IMemInputPin::ReceiveMultiple**</span></span>](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple)
-   [<span data-ttu-id="2c688-107">**IPin::EndOfStream**</span><span class="sxs-lookup"><span data-stu-id="2c688-107">**IPin::EndOfStream**</span></span>](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)
-   [<span data-ttu-id="2c688-108">**IPin::NewSegment**</span><span class="sxs-lookup"><span data-stu-id="2c688-108">**IPin::NewSegment**</span></span>](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment)
-   [<span data-ttu-id="2c688-109">**IMemAllocator：： GetBuffer**</span><span class="sxs-lookup"><span data-stu-id="2c688-109">**IMemAllocator::GetBuffer**</span></span>](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer)

<span data-ttu-id="2c688-110">應用程式執行緒會呼叫下列方法：</span><span class="sxs-lookup"><span data-stu-id="2c688-110">The following methods are called on the application thread:</span></span>

-   <span data-ttu-id="2c688-111">狀態變更： [**IBaseFilter：： JoinFilterGraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph)、 [**IMediaFilter：:P ause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause)、 [**IMediaFilter：： Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run)、 [**IMediaFilter：： Stop**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop)、 [**IQualityControl：： SetSink**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink)。</span><span class="sxs-lookup"><span data-stu-id="2c688-111">State changes: [**IBaseFilter::JoinFilterGraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph), [**IMediaFilter::Pause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause), [**IMediaFilter::Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run), [**IMediaFilter::Stop**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop), [**IQualityControl::SetSink**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink).</span></span>
-   <span data-ttu-id="2c688-112">參考時鐘： [**IMediaFilter：： GetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getsyncsource)， [**IMediaFilter：： SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource)。</span><span class="sxs-lookup"><span data-stu-id="2c688-112">Reference clock: [**IMediaFilter::GetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getsyncsource), [**IMediaFilter::SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource).</span></span>
-   <span data-ttu-id="2c688-113">Pin 作業： [**IBaseFilter：： FindPin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin)、 [**IPin：： Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect)、 [**IPin：： ConnectedTo**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto)、 [**IPin：： ConnectionMediaType**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectionmediatype)、 [**IPin：:D isconnect**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect)、 [**IPin：： ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection)。</span><span class="sxs-lookup"><span data-stu-id="2c688-113">Pin operations: [**IBaseFilter::FindPin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin), [**IPin::Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect), [**IPin::ConnectedTo**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto), [**IPin::ConnectionMediaType**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectionmediatype), [**IPin::Disconnect**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect), [**IPin::ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection).</span></span>
-   <span data-ttu-id="2c688-114">配置器函數： [**IMemInputPin：： GetAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator)， [**IMemInputPin：： NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator)。</span><span class="sxs-lookup"><span data-stu-id="2c688-114">Allocator functions: [**IMemInputPin::GetAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator), [**IMemInputPin::NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator).</span></span>
-   <span data-ttu-id="2c688-115">排清： [**IPin：： BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush)， [**IPin：： EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush)。</span><span class="sxs-lookup"><span data-stu-id="2c688-115">Flushing: [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush), [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush).</span></span>

<span data-ttu-id="2c688-116">此清單未涵蓋全部種類。</span><span class="sxs-lookup"><span data-stu-id="2c688-116">This list is not exhaustive.</span></span> <span data-ttu-id="2c688-117">當您執行篩選時，您必須考慮哪些方法會變更篩選狀態，以及哪些方法會執行串流作業。</span><span class="sxs-lookup"><span data-stu-id="2c688-117">When you implement a filter, you must consider which methods change the filter state, and which methods perform streaming operations.</span></span>

 

 




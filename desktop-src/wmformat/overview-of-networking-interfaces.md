---
title: 網路介面的概觀
description: 網路介面的概觀
ms.assetid: 7aa7ff1b-9c81-4fee-afa9-2a9eed457360
keywords:
- Windows Media Format SDK，網路介面
- Windows Media Format SDK，介面
- Advanced Systems Format (ASF) ，網路介面
- ASF (Advanced Systems Format) ，網路介面
- Advanced Systems Format (ASF) ，網路功能的介面清單
- ASF (Advanced Systems Format) ，網路功能的介面清單
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebd1c235e7e8b36964993bb24ce30977446d9af8
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2020
ms.locfileid: "103681565"
---
# <a name="overview-of-networking-interfaces"></a><span data-ttu-id="bf619-109">網路介面的概觀</span><span class="sxs-lookup"><span data-stu-id="bf619-109">Overview of Networking Interfaces</span></span>

<span data-ttu-id="bf619-110">透過下列介面的方法，可支援此 SDK 的網路功能。</span><span class="sxs-lookup"><span data-stu-id="bf619-110">The networking features of this SDK are supported through methods of the following interfaces.</span></span>



| <span data-ttu-id="bf619-111">介面</span><span class="sxs-lookup"><span data-stu-id="bf619-111">Interface</span></span>                                                  | <span data-ttu-id="bf619-112">描述</span><span class="sxs-lookup"><span data-stu-id="bf619-112">Description</span></span>                                                                                                                                           |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bf619-113">**IWMClientConnections**</span><span class="sxs-lookup"><span data-stu-id="bf619-113">**IWMClientConnections**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmclientconnections)       | <span data-ttu-id="bf619-114">取得連接到網路接收器之用戶端的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="bf619-114">Gets information about the clients connected to a network sink.</span></span>                                                                                       |
| [<span data-ttu-id="bf619-115">**IWMClientConnections2**</span><span class="sxs-lookup"><span data-stu-id="bf619-115">**IWMClientConnections2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmclientconnections2)     | <span data-ttu-id="bf619-116">提供方法，以取得附加至寫入器網路接收之用戶端的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="bf619-116">Provides a method to get information about a client attached to a writer network sink.</span></span> <span data-ttu-id="bf619-117">這個介面會擴充 **IWMClientConnections** 介面。</span><span class="sxs-lookup"><span data-stu-id="bf619-117">This interface extends the **IWMClientConnections** interface.</span></span> |
| [<span data-ttu-id="bf619-118">**IWMCredentialCallback**</span><span class="sxs-lookup"><span data-stu-id="bf619-118">**IWMCredentialCallback**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcredentialcallback)     | <span data-ttu-id="bf619-119">提供回呼方法，以在存取遠端網站時取得使用者認證。</span><span class="sxs-lookup"><span data-stu-id="bf619-119">Provides a callback method to acquire user credentials when accessing a remote site.</span></span>                                                                  |
| [<span data-ttu-id="bf619-120">**IWMReaderAdvanced2**</span><span class="sxs-lookup"><span data-stu-id="bf619-120">**IWMReaderAdvanced2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)           | <span data-ttu-id="bf619-121">提供 reader 物件的 advanced 方法。</span><span class="sxs-lookup"><span data-stu-id="bf619-121">Provides advanced methods on the reader object.</span></span>                                                                                                       |
| [<span data-ttu-id="bf619-122">**IWMReaderAdvanced3**</span><span class="sxs-lookup"><span data-stu-id="bf619-122">**IWMReaderAdvanced3**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced3)           | <span data-ttu-id="bf619-123">擴充 **IWMReaderAdvanced2** 介面。</span><span class="sxs-lookup"><span data-stu-id="bf619-123">Extends the **IWMReaderAdvanced2** interface.</span></span>                                                                                                         |
| [<span data-ttu-id="bf619-124">**IWMReaderAdvanced4**</span><span class="sxs-lookup"><span data-stu-id="bf619-124">**IWMReaderAdvanced4**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4)           | <span data-ttu-id="bf619-125">擴充 **IWMReaderAdvanced3** 介面。</span><span class="sxs-lookup"><span data-stu-id="bf619-125">Extends the **IWMReaderAdvanced3** interface.</span></span>                                                                                                         |
| [<span data-ttu-id="bf619-126">**IWMReaderNetworkConfig**</span><span class="sxs-lookup"><span data-stu-id="bf619-126">**IWMReaderNetworkConfig**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig)   | <span data-ttu-id="bf619-127">在 reader 物件上設定網路設定。</span><span class="sxs-lookup"><span data-stu-id="bf619-127">Configures the network settings on the reader object.</span></span>                                                                                                 |
| [<span data-ttu-id="bf619-128">**IWMReaderNetworkConfig2**</span><span class="sxs-lookup"><span data-stu-id="bf619-128">**IWMReaderNetworkConfig2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig2) | <span data-ttu-id="bf619-129">在 reader 物件上設定額外的網路設定。</span><span class="sxs-lookup"><span data-stu-id="bf619-129">Configures additional network settings on the reader object.</span></span> <span data-ttu-id="bf619-130">這個介面會擴充 **IWMReaderNetworkConfig** 介面。</span><span class="sxs-lookup"><span data-stu-id="bf619-130">This interface extends the **IWMReaderNetworkConfig** interface.</span></span>                         |
| [<span data-ttu-id="bf619-131">**IWMWriterNetworkSink**</span><span class="sxs-lookup"><span data-stu-id="bf619-131">**IWMWriterNetworkSink**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriternetworksink)       | <span data-ttu-id="bf619-132">設定用來將數位媒體寫入網路的網路接收物件。</span><span class="sxs-lookup"><span data-stu-id="bf619-132">Configures the network sink object, which is used to write digital media to a network.</span></span>                                                                |
| [<span data-ttu-id="bf619-133">**IWMWriterPushSink**</span><span class="sxs-lookup"><span data-stu-id="bf619-133">**IWMWriterPushSink**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpushsink)             | <span data-ttu-id="bf619-134">設定用來將數位媒體散發至發行端點的推播接收物件。</span><span class="sxs-lookup"><span data-stu-id="bf619-134">Configures the push sink object, which is used to distribute digital media to publishing points.</span></span>                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="bf619-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="bf619-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf619-136">**執行網路功能**</span><span class="sxs-lookup"><span data-stu-id="bf619-136">**Implementing Network Functionality**</span></span>](implementing-network-functionality.md)
</dt> </dl>

 

 





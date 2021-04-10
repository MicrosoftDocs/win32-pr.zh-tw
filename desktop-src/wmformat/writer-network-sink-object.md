---
title: 寫入器網路接收物件
description: 寫入器網路接收物件
ms.assetid: f7765b42-693a-4f48-b750-17579e860b6d
keywords:
- Windows Media Format SDK，寫入器網路接收物件
- Advanced Systems Format (ASF) 、writer 網路接收物件
- ASF (Advanced 系統格式) 、寫入器網路接收物件
- 物件，寫入器網路接收物件
- 寫入器網路接收物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c85af356c1d326ddaaf3703ca87c3b7bdd1628b9
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2020
ms.locfileid: "104092587"
---
# <a name="writer-network-sink-object"></a><span data-ttu-id="ac90f-108">寫入器網路接收物件</span><span class="sxs-lookup"><span data-stu-id="ac90f-108">Writer Network Sink Object</span></span>

<span data-ttu-id="ac90f-109">寫入器網路接收物件是用來將數位媒體寫入至網路。</span><span class="sxs-lookup"><span data-stu-id="ac90f-109">The writer network sink object is used to write digital media to a network.</span></span>

<span data-ttu-id="ac90f-110">寫入器網路接收物件是由函式 [**WMCreateWriterNetworkSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriternetworksink)所建立，它會將指標設定為 **IWMWriterNetworkSink** 介面。</span><span class="sxs-lookup"><span data-stu-id="ac90f-110">The writer network sink object is created by the function [**WMCreateWriterNetworkSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriternetworksink), which sets a pointer to an **IWMWriterNetworkSink** interface.</span></span> <span data-ttu-id="ac90f-111">您可以藉由呼叫 **QueryInterface** 方法來取得寫入器網路接收物件的其他介面。</span><span class="sxs-lookup"><span data-stu-id="ac90f-111">The other interfaces of the writer network sink object can be obtained by calling the **QueryInterface** method.</span></span>



| <span data-ttu-id="ac90f-112">介面</span><span class="sxs-lookup"><span data-stu-id="ac90f-112">Interface</span></span>                                              | <span data-ttu-id="ac90f-113">描述</span><span class="sxs-lookup"><span data-stu-id="ac90f-113">Description</span></span>                                                                                                                                                                                                     |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ac90f-114">**IWMClientConnections**</span><span class="sxs-lookup"><span data-stu-id="ac90f-114">**IWMClientConnections**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmclientconnections)   | <span data-ttu-id="ac90f-115">收集連線用戶端的資訊。</span><span class="sxs-lookup"><span data-stu-id="ac90f-115">Collects information on connected clients.</span></span>                                                                                                                                                                      |
| [<span data-ttu-id="ac90f-116">**IWMClientConnections2**</span><span class="sxs-lookup"><span data-stu-id="ac90f-116">**IWMClientConnections2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmclientconnections2) | <span data-ttu-id="ac90f-117">抓取 advanced 用戶端資訊。</span><span class="sxs-lookup"><span data-stu-id="ac90f-117">Retrieves advanced client information.</span></span>                                                                                                                                                                          |
| [<span data-ttu-id="ac90f-118">**IWMRegisterCallback**</span><span class="sxs-lookup"><span data-stu-id="ac90f-118">**IWMRegisterCallback**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback)     | <span data-ttu-id="ac90f-119">讓應用程式從物件取得狀態訊息。</span><span class="sxs-lookup"><span data-stu-id="ac90f-119">Enables the application to get status messages from the object.</span></span>                                                                                                                                                 |
| [<span data-ttu-id="ac90f-120">**IWMWriterNetworkSink**</span><span class="sxs-lookup"><span data-stu-id="ac90f-120">**IWMWriterNetworkSink**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriternetworksink)   | <span data-ttu-id="ac90f-121">開啟和關閉埠、設定和抓取可連接至接收器物件的用戶端數目上限、設定寫入器物件所要使用的網路通訊協定，以及執行其他的 advanced 函數。</span><span class="sxs-lookup"><span data-stu-id="ac90f-121">Opens and closes ports, sets and retrieves the maximum number of clients that can connect to the sink object, sets the network protocol to be used by the writer object, and performs other advanced functions.</span></span> |
| [<span data-ttu-id="ac90f-122">**IWMWriterSink**</span><span class="sxs-lookup"><span data-stu-id="ac90f-122">**IWMWriterSink**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink)                 | <span data-ttu-id="ac90f-123">配置記憶體、判斷接收是否即時運作，以及處理數個回呼函數。</span><span class="sxs-lookup"><span data-stu-id="ac90f-123">Allocates memory, determines whether the sink is operating in real time, and handles several callback functions.</span></span>                                                                                                |



 

<span data-ttu-id="ac90f-124">下列回呼介面可以由應用程式執行，以追蹤寫入器網路接收物件的進度。</span><span class="sxs-lookup"><span data-stu-id="ac90f-124">The following callback interface can be implemented by the application to track the progress of a writer network sink object.</span></span>



| <span data-ttu-id="ac90f-125">介面</span><span class="sxs-lookup"><span data-stu-id="ac90f-125">Interface</span></span>                                      | <span data-ttu-id="ac90f-126">描述</span><span class="sxs-lookup"><span data-stu-id="ac90f-126">Description</span></span>                                                                    |
|------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="ac90f-127">**IWMStatusCallback**</span><span class="sxs-lookup"><span data-stu-id="ac90f-127">**IWMStatusCallback**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | <span data-ttu-id="ac90f-128">必須將狀態資訊傳達給主應用程式時，才需要此資訊。</span><span class="sxs-lookup"><span data-stu-id="ac90f-128">Required when status information must be communicated to the host application.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="ac90f-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="ac90f-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ac90f-130">**廣播 ASF 資料**</span><span class="sxs-lookup"><span data-stu-id="ac90f-130">**Broadcasting ASF Data**</span></span>](broadcasting-asf-data.md)
</dt> <dt>

[<span data-ttu-id="ac90f-131">**物件**</span><span class="sxs-lookup"><span data-stu-id="ac90f-131">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="ac90f-132">**使用寫入器接收器**</span><span class="sxs-lookup"><span data-stu-id="ac90f-132">**Working with Writer Sinks**</span></span>](working-with-writer-sinks.md)
</dt> </dl>

 

 





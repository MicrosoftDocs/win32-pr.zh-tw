---
title: 寫入器推送接收物件
description: 寫入器推送接收物件
ms.assetid: 34e48f35-13d7-4649-a8b2-ed6510b16f88
keywords:
- Windows Media Format SDK，寫入器推播接收物件
- Advanced Systems Format (ASF) 、writer push sink 物件
- ASF (Advanced 系統格式) 、寫入器推送接收物件
- 物件、寫入器推送接收物件
- 寫入器推送接收物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a19ea9855219dcb4572ef187ad93e03696b88492
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "103932923"
---
# <a name="writer-push-sink-object"></a><span data-ttu-id="91a1e-108">寫入器推送接收物件</span><span class="sxs-lookup"><span data-stu-id="91a1e-108">Writer Push Sink Object</span></span>

<span data-ttu-id="91a1e-109">寫入器發送接收物件會將數位媒體分配至發行端點。</span><span class="sxs-lookup"><span data-stu-id="91a1e-109">The writer push sink object distributes digital media to publishing points.</span></span> <span data-ttu-id="91a1e-110">例如，即時音樂會可以由單一伺服器進行編碼，然後傳遞或 *推送* 至數部其他伺服器，這些伺服器實際上會將內容串流至使用者。</span><span class="sxs-lookup"><span data-stu-id="91a1e-110">For example, a live concert can be encoded by a single server and then delivered, or *pushed*, to several other servers that will actually stream the content to users.</span></span>

<span data-ttu-id="91a1e-111">寫入器發送接收物件是由函式 [**WMCreateWriterPushSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriterpushsink)所建立，它會設定 **IWMWriterPushSink** 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="91a1e-111">A writer push sink object is created by the function [**WMCreateWriterPushSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriterpushsink), which sets a pointer to an **IWMWriterPushSink** interface.</span></span> <span data-ttu-id="91a1e-112">下表所列的物件所支援的其他介面，可以藉由呼叫 **QueryInterface** 方法來取得。</span><span class="sxs-lookup"><span data-stu-id="91a1e-112">The other interfaces supported by the object, listed in the following table, can be obtained by calling the **QueryInterface** method.</span></span>



| <span data-ttu-id="91a1e-113">介面</span><span class="sxs-lookup"><span data-stu-id="91a1e-113">Interface</span></span>                                          | <span data-ttu-id="91a1e-114">描述</span><span class="sxs-lookup"><span data-stu-id="91a1e-114">Description</span></span>                                                                                                      |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="91a1e-115">**IWMRegisterCallback**</span><span class="sxs-lookup"><span data-stu-id="91a1e-115">**IWMRegisterCallback**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback) | <span data-ttu-id="91a1e-116">讓應用程式從物件取得狀態訊息。</span><span class="sxs-lookup"><span data-stu-id="91a1e-116">Enables the application to get status messages from the object.</span></span>                                                  |
| [<span data-ttu-id="91a1e-117">**IWMWriterPushSink**</span><span class="sxs-lookup"><span data-stu-id="91a1e-117">**IWMWriterPushSink**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpushsink)     | <span data-ttu-id="91a1e-118">管理推播散發會話。</span><span class="sxs-lookup"><span data-stu-id="91a1e-118">Manages a push distribution session.</span></span>                                                                             |
| [<span data-ttu-id="91a1e-119">**IWMWriterSink**</span><span class="sxs-lookup"><span data-stu-id="91a1e-119">**IWMWriterSink**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink)             | <span data-ttu-id="91a1e-120">配置記憶體、判斷接收是否即時運作，以及公開數個回呼函數。</span><span class="sxs-lookup"><span data-stu-id="91a1e-120">Allocates memory, determines whether the sink is operating in real time, and exposes several callback functions.</span></span> |



 

<span data-ttu-id="91a1e-121">下列回呼介面可以由應用程式執行，以追蹤寫入器推送接收物件的進度。</span><span class="sxs-lookup"><span data-stu-id="91a1e-121">The following callback interface can be implemented by the application to track the progress of a writer push sink object.</span></span>



| <span data-ttu-id="91a1e-122">介面</span><span class="sxs-lookup"><span data-stu-id="91a1e-122">Interface</span></span>                                      | <span data-ttu-id="91a1e-123">描述</span><span class="sxs-lookup"><span data-stu-id="91a1e-123">Description</span></span>                                                                    |
|------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="91a1e-124">**IWMStatusCallback**</span><span class="sxs-lookup"><span data-stu-id="91a1e-124">**IWMStatusCallback**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | <span data-ttu-id="91a1e-125">必須將狀態資訊傳達給主應用程式時，才需要此資訊。</span><span class="sxs-lookup"><span data-stu-id="91a1e-125">Required when status information must be communicated to the host application.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="91a1e-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="91a1e-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="91a1e-127">**物件**</span><span class="sxs-lookup"><span data-stu-id="91a1e-127">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="91a1e-128">**將 ASF 資料傳送至發行端點**</span><span class="sxs-lookup"><span data-stu-id="91a1e-128">**Sending ASF Data to a Publishing Point**</span></span>](sending-asf-data-to-a-publishing-point.md)
</dt> <dt>

[<span data-ttu-id="91a1e-129">**使用寫入器接收器**</span><span class="sxs-lookup"><span data-stu-id="91a1e-129">**Working with Writer Sinks**</span></span>](working-with-writer-sinks.md)
</dt> </dl>

 

 





---
title: 寫入器檔案接收物件
description: 寫入器檔案接收物件
ms.assetid: 93f44579-fb2d-498e-a271-5bc91d6f0321
keywords:
- Windows Media Format SDK，寫入器檔案接收物件
- Advanced Systems Format (ASF) 、writer file sink 物件
- ASF (Advanced Systems Format) 、writer file sink 物件
- 物件，寫入器檔案接收物件
- 寫入器檔案接收物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82009e5be74cfc23e687001a2a81cd4546812af9
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2020
ms.locfileid: "104023174"
---
# <a name="writer-file-sink-object"></a><span data-ttu-id="bb32f-108">寫入器檔案接收物件</span><span class="sxs-lookup"><span data-stu-id="bb32f-108">Writer File Sink Object</span></span>

<span data-ttu-id="bb32f-109">寫入 Windows Media 輸出至檔案時，會使用寫入器檔案接收物件。</span><span class="sxs-lookup"><span data-stu-id="bb32f-109">The writer file sink object is used when writing Windows Media output to a file.</span></span>

<span data-ttu-id="bb32f-110">寫入器檔案接收物件是由函式 [**WMCreateWriterFileSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriterfilesink)所建立，它會將指標設定為 **IWMWriterFileSink** 介面。</span><span class="sxs-lookup"><span data-stu-id="bb32f-110">The writer file sink object is created by the function [**WMCreateWriterFileSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriterfilesink), which sets a pointer to an **IWMWriterFileSink** interface.</span></span> <span data-ttu-id="bb32f-111">您可以藉由呼叫 **QueryInterface** 方法來取得寫入器檔案接收物件的其他介面。</span><span class="sxs-lookup"><span data-stu-id="bb32f-111">The other interfaces of the writer file sink object can be obtained by calling the **QueryInterface** method.</span></span>

<span data-ttu-id="bb32f-112">寫入器檔案接收物件支援下列介面。</span><span class="sxs-lookup"><span data-stu-id="bb32f-112">The following interfaces are supported by the writer file sink object.</span></span>



| <span data-ttu-id="bb32f-113">介面</span><span class="sxs-lookup"><span data-stu-id="bb32f-113">Interface</span></span>                                          | <span data-ttu-id="bb32f-114">描述</span><span class="sxs-lookup"><span data-stu-id="bb32f-114">Description</span></span>                                                                                                                     |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bb32f-115">**IWMRegisterCallback**</span><span class="sxs-lookup"><span data-stu-id="bb32f-115">**IWMRegisterCallback**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback) | <span data-ttu-id="bb32f-116">讓應用程式從物件取得狀態訊息。</span><span class="sxs-lookup"><span data-stu-id="bb32f-116">Enables the application to get status messages from the object.</span></span>                                                                 |
| [<span data-ttu-id="bb32f-117">**IWMWriterFileSink**</span><span class="sxs-lookup"><span data-stu-id="bb32f-117">**IWMWriterFileSink**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink)     | <span data-ttu-id="bb32f-118">開啟寫入器物件可以寫入資料的檔案。</span><span class="sxs-lookup"><span data-stu-id="bb32f-118">Opens a file to which the writer object can write data.</span></span>                                                                         |
| [<span data-ttu-id="bb32f-119">**IWMWriterFileSink2**</span><span class="sxs-lookup"><span data-stu-id="bb32f-119">**IWMWriterFileSink2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink2)   | <span data-ttu-id="bb32f-120">提供檔案接收物件的擴充管理。</span><span class="sxs-lookup"><span data-stu-id="bb32f-120">Provides extended management of a file sink object.</span></span> <span data-ttu-id="bb32f-121">繼承 **IWMWriterFileSink** 的所有方法。</span><span class="sxs-lookup"><span data-stu-id="bb32f-121">Inherits all of the methods of **IWMWriterFileSink**.</span></span>                       |
| [<span data-ttu-id="bb32f-122">**IWMWriterFileSink3**</span><span class="sxs-lookup"><span data-stu-id="bb32f-122">**IWMWriterFileSink3**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink3)   | <span data-ttu-id="bb32f-123">提供用來寫入檔案的其他選項。</span><span class="sxs-lookup"><span data-stu-id="bb32f-123">Provides additional options for writing files.</span></span> <span data-ttu-id="bb32f-124">繼承 **IWMWriterFileSink** 和 **IWMWriterFileSink2** 的所有方法。</span><span class="sxs-lookup"><span data-stu-id="bb32f-124">Inherits all of the methods of **IWMWriterFileSink** and **IWMWriterFileSink2**.</span></span> |
| [<span data-ttu-id="bb32f-125">**IWMWriterSink**</span><span class="sxs-lookup"><span data-stu-id="bb32f-125">**IWMWriterSink**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink)             | <span data-ttu-id="bb32f-126">配置記憶體、判斷接收是否即時運作，以及處理數個回呼函數。</span><span class="sxs-lookup"><span data-stu-id="bb32f-126">Allocates memory, determines whether the sink is operating in real time, and handles several callback functions.</span></span>                |



 

<span data-ttu-id="bb32f-127">應用程式應該執行下列回呼介面，以追蹤寫入器檔案接收物件的進度。</span><span class="sxs-lookup"><span data-stu-id="bb32f-127">The following callback interface should be implemented by the application to track the progress of a writer file sink object.</span></span>



| <span data-ttu-id="bb32f-128">介面</span><span class="sxs-lookup"><span data-stu-id="bb32f-128">Interface</span></span>                                      | <span data-ttu-id="bb32f-129">描述</span><span class="sxs-lookup"><span data-stu-id="bb32f-129">Description</span></span>                                                                    |
|------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="bb32f-130">**IWMStatusCallback**</span><span class="sxs-lookup"><span data-stu-id="bb32f-130">**IWMStatusCallback**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | <span data-ttu-id="bb32f-131">必須將狀態資訊傳達給主應用程式時，才需要此資訊。</span><span class="sxs-lookup"><span data-stu-id="bb32f-131">Required when status information must be communicated to the host application.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="bb32f-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="bb32f-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bb32f-133">**物件**</span><span class="sxs-lookup"><span data-stu-id="bb32f-133">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="bb32f-134">**使用寫入器接收器**</span><span class="sxs-lookup"><span data-stu-id="bb32f-134">**Working with Writer Sinks**</span></span>](working-with-writer-sinks.md)
</dt> </dl>

 

 





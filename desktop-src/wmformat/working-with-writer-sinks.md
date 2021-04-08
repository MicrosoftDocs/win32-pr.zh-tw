---
title: 使用寫入器接收器
description: 使用寫入器接收器
ms.assetid: 1ad28684-47d2-4ddb-bf18-22310f0392a0
keywords:
- Advanced Systems Format (ASF) 、寫入器接收
- ASF (Advanced 系統格式) 、寫入器接收
- Advanced Systems Format (ASF) 、接收
- ASF (Advanced 系統格式) 、接收
- 接收，寫入器接收
- 寫入器接收器，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d5b690d9e1ab25d15f7c1e8612bf20e32f87c81
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "103681376"
---
# <a name="working-with-writer-sinks"></a><span data-ttu-id="656c6-109">使用寫入器接收器</span><span class="sxs-lookup"><span data-stu-id="656c6-109">Working with Writer Sinks</span></span>

<span data-ttu-id="656c6-110">Windows Media 格式 SDK 的寫入器物件會將輸入媒體資料處理成位資料流程。</span><span class="sxs-lookup"><span data-stu-id="656c6-110">The writer object of the Windows Media Format SDK processes input media data into a bit stream.</span></span> <span data-ttu-id="656c6-111">但是，寫入器物件不會將位資料流程傳遞至其最終目的地 () 的檔案或網路位置。</span><span class="sxs-lookup"><span data-stu-id="656c6-111">However, the writer object does not deliver the bit stream to its final destination (either to a file or a network location).</span></span> <span data-ttu-id="656c6-112">若要將 ASF 內容寫入可使用的格式，您必須使用寫入器接收器。</span><span class="sxs-lookup"><span data-stu-id="656c6-112">To write the ASF content to a usable format, you must use writer sinks.</span></span>

<span data-ttu-id="656c6-113">寫入器物件支援三種接收類型：檔接收、網路接收和推播接收。</span><span class="sxs-lookup"><span data-stu-id="656c6-113">The writer object supports three types of sinks: file sinks, network sinks, and push sinks.</span></span> <span data-ttu-id="656c6-114">File 接收會將 ASF 內容寫入磁片上的 ASF 檔案。</span><span class="sxs-lookup"><span data-stu-id="656c6-114">A file sink writes ASF content to an ASF file on disk.</span></span> <span data-ttu-id="656c6-115">網路接收會從網路位址廣播 ASF 內容。</span><span class="sxs-lookup"><span data-stu-id="656c6-115">A network sink broadcasts ASF content from a network address.</span></span> <span data-ttu-id="656c6-116">推播接收會將資料傳遞至執行 Windows Media Services 的伺服器，讓伺服器可以將內容提供給其預定的物件。</span><span class="sxs-lookup"><span data-stu-id="656c6-116">A push sink delivers data to a server running Windows Media Services so that the server can make the content available to its intended audience.</span></span> <span data-ttu-id="656c6-117">您也可以建立自己的接收器，以應用程式所需的任何方式來傳遞 ASF 資料。</span><span class="sxs-lookup"><span data-stu-id="656c6-117">You can also create your own sinks to deliver ASF data in whatever way is required by your application.</span></span> <span data-ttu-id="656c6-118">如需網路接收和推播接收的詳細資訊，請參閱透過 [網路傳送 ASF 資料](sending-asf-data-over-a-network.md)。</span><span class="sxs-lookup"><span data-stu-id="656c6-118">For information about network sinks and push sinks, see [Sending ASF Data Over a Network](sending-asf-data-over-a-network.md).</span></span> <span data-ttu-id="656c6-119">本節的其餘部分將討論寫入器接收器。</span><span class="sxs-lookup"><span data-stu-id="656c6-119">The remainder of this section discusses writer sinks.</span></span>

<span data-ttu-id="656c6-120">您可以為所使用的每個寫入器實例設定一或多個接收。</span><span class="sxs-lookup"><span data-stu-id="656c6-120">You can configure one or more sinks for each instance of the writer you use.</span></span> <span data-ttu-id="656c6-121">每個接收只會處理單一目的地。</span><span class="sxs-lookup"><span data-stu-id="656c6-121">Each sink handles only a single destination.</span></span> <span data-ttu-id="656c6-122">例如，如果您想要一次寫入三個檔案，您必須為每個檔案建立和設定個別的檔案接收。</span><span class="sxs-lookup"><span data-stu-id="656c6-122">For example, if you want to write three files at once, you must create and configure a separate file sink for each.</span></span>

<span data-ttu-id="656c6-123">下列各節說明寫入器接收器的使用。</span><span class="sxs-lookup"><span data-stu-id="656c6-123">The following sections describe the use of writer sinks.</span></span>



| <span data-ttu-id="656c6-124">區段</span><span class="sxs-lookup"><span data-stu-id="656c6-124">Section</span></span>                                                                      | <span data-ttu-id="656c6-125">描述</span><span class="sxs-lookup"><span data-stu-id="656c6-125">Description</span></span>                                                                      |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [<span data-ttu-id="656c6-126">將接收器新增至寫入器</span><span class="sxs-lookup"><span data-stu-id="656c6-126">Adding Sinks to the Writer</span></span>](adding-sinks-to-the-writer.md)                 | <span data-ttu-id="656c6-127">描述如何將接收器新增至寫入器。</span><span class="sxs-lookup"><span data-stu-id="656c6-127">Describes how to add sinks to the writer.</span></span>                                        |
| [<span data-ttu-id="656c6-128">列舉接收</span><span class="sxs-lookup"><span data-stu-id="656c6-128">Enumerating Sinks</span></span>](enumerating-sinks.md)                                   | <span data-ttu-id="656c6-129">描述如何列舉已新增至寫入器的接收。</span><span class="sxs-lookup"><span data-stu-id="656c6-129">Describes how to enumerate the sinks that have been added to the writer.</span></span>         |
| [<span data-ttu-id="656c6-130">從接收取得錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="656c6-130">Getting Error Messages from a Sink</span></span>](getting-error-messages-from-a-sink.md) | <span data-ttu-id="656c6-131">說明如何設定接收以將狀態訊息傳遞給您的應用程式。</span><span class="sxs-lookup"><span data-stu-id="656c6-131">Describes how to configure sinks to deliver status messages to your application.</span></span> |
| [<span data-ttu-id="656c6-132">使用檔案接收</span><span class="sxs-lookup"><span data-stu-id="656c6-132">Using File Sinks</span></span>](using-file-sinks.md)                                     | <span data-ttu-id="656c6-133">說明如何使用寫入器檔案接收在磁片上建立 ASF 檔案。</span><span class="sxs-lookup"><span data-stu-id="656c6-133">Describes how to use a writer file sink to create an ASF file on disk.</span></span>           |
| [<span data-ttu-id="656c6-134">使用自訂接收器</span><span class="sxs-lookup"><span data-stu-id="656c6-134">Using Custom Sinks</span></span>](using-custom-sinks.md)                                 | <span data-ttu-id="656c6-135">說明如何建立及使用您自己的自訂接收來傳遞 ASF 資料。</span><span class="sxs-lookup"><span data-stu-id="656c6-135">Describes how to create and use your own custom sinks to deliver ASF data.</span></span>       |



 

## <a name="related-topics"></a><span data-ttu-id="656c6-136">相關主題</span><span class="sxs-lookup"><span data-stu-id="656c6-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="656c6-137">**IWMWriterAdvanced 介面**</span><span class="sxs-lookup"><span data-stu-id="656c6-137">**IWMWriterAdvanced Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)
</dt> <dt>

[<span data-ttu-id="656c6-138">**IWMWriterSink 介面**</span><span class="sxs-lookup"><span data-stu-id="656c6-138">**IWMWriterSink Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink)
</dt> <dt>

[<span data-ttu-id="656c6-139">**寫入 ASF 檔案**</span><span class="sxs-lookup"><span data-stu-id="656c6-139">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 





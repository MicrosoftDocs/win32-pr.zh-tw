---
title: 接收器
description: 接收器
ms.assetid: 6781a326-a30a-4d4d-96db-332d0f681a31
keywords:
- Windows Media 格式 SDK，接收
- Windows Media Format SDK，file 接收
- Advanced Systems Format (ASF) 、接收
- ASF (Advanced 系統格式) 、接收
- Advanced Systems Format (ASF) ，file 接收
- ASF (Advanced Systems Format) ，file 接收
- Windows Media Format SDK，網路接收器
- Windows Media Format SDK、push 接收器
- Advanced Systems Format (ASF) ，網路接收器
- ASF (Advanced Systems Format) ，網路接收器
- Advanced Systems Format (ASF) 、push 接收器
- ASF (Advanced 系統格式) 、推播接收
- 接收、關於
- 檔接收，關於
- 網路接收器
- 推播接收器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a62548f159172f58d4f52b0289c5adbfef02f55
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104023066"
---
# <a name="sinks"></a><span data-ttu-id="b1a55-119">接收器</span><span class="sxs-lookup"><span data-stu-id="b1a55-119">Sinks</span></span>

<span data-ttu-id="b1a55-120">Windows Media 格式 SDK 的寫入器物件會將已處理的內容傳遞給接收。</span><span class="sxs-lookup"><span data-stu-id="b1a55-120">The writer object of the Windows Media Format SDK delivers processed content to sinks.</span></span> <span data-ttu-id="b1a55-121">每個接收都是可傳遞資料的物件。</span><span class="sxs-lookup"><span data-stu-id="b1a55-121">Each sink is an object that delivers data.</span></span> <span data-ttu-id="b1a55-122">傳遞點取決於接收的類型。</span><span class="sxs-lookup"><span data-stu-id="b1a55-122">The point of delivery depends upon the type of sink.</span></span> <span data-ttu-id="b1a55-123">有三種類型的接收：檔案接收、網路接收和推播接收。</span><span class="sxs-lookup"><span data-stu-id="b1a55-123">There are three types of sinks: file sinks, network sinks, and push sinks.</span></span>

## <a name="file-sinks"></a><span data-ttu-id="b1a55-124">檔案接收</span><span class="sxs-lookup"><span data-stu-id="b1a55-124">File Sinks</span></span>

<span data-ttu-id="b1a55-125">File 接收會將 ASF 內容寫入本機或網路磁碟機機上的檔案。</span><span class="sxs-lookup"><span data-stu-id="b1a55-125">File sinks write ASF content to a file on a local or network drive.</span></span> <span data-ttu-id="b1a55-126">當您使用 writer 物件來寫入檔案，但未明確地新增檔案接收時，寫入器會使用您傳遞給 [**IWMWriter：： SetOutputFilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename)的名稱來為您建立一個檔案。</span><span class="sxs-lookup"><span data-stu-id="b1a55-126">When you use the writer object to write a file without explicitly adding a file sink, the writer will create one for you using the name you pass to [**IWMWriter::SetOutputFilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename).</span></span> <span data-ttu-id="b1a55-127">您可以將多個檔案接收指派給寫入器物件，以便一次寫入數個檔案中的內容。</span><span class="sxs-lookup"><span data-stu-id="b1a55-127">You can assign multiple file sinks to a writer object to write the content in several files at once.</span></span>

<span data-ttu-id="b1a55-128">藉由使用檔案接收，您可以控制檔案的許多層面。</span><span class="sxs-lookup"><span data-stu-id="b1a55-128">By using a file sink, you can control many aspects of the file.</span></span> <span data-ttu-id="b1a55-129">下列功能可透過 file 接收取得。</span><span class="sxs-lookup"><span data-stu-id="b1a55-129">The following features are available through a file sink.</span></span>

-   <span data-ttu-id="b1a55-130">檔案統計資料監視。</span><span class="sxs-lookup"><span data-stu-id="b1a55-130">File statistics monitoring.</span></span> <span data-ttu-id="b1a55-131">您可以在建立檔案時，監視檔案的大小和持續時間。</span><span class="sxs-lookup"><span data-stu-id="b1a55-131">You can monitor the file size and duration as it is being created.</span></span>
-   <span data-ttu-id="b1a55-132">部分內容檔案建立。</span><span class="sxs-lookup"><span data-stu-id="b1a55-132">Partial content file creation.</span></span> <span data-ttu-id="b1a55-133">檔案接收可以設定為在特定時間開始寫入內容，並在特定時間結束寫入。</span><span class="sxs-lookup"><span data-stu-id="b1a55-133">File sinks can be configured to begin writing content at a specific time and to end writing at a specific time.</span></span> <span data-ttu-id="b1a55-134">這可讓您在相同的寫入行程中，建立多個檔案，其中包含相同內容的不同區段。</span><span class="sxs-lookup"><span data-stu-id="b1a55-134">This enables you to create multiple files containing different sections of the same content in the same writing pass.</span></span>

## <a name="network-sinks"></a><span data-ttu-id="b1a55-135">網路接收器</span><span class="sxs-lookup"><span data-stu-id="b1a55-135">Network Sinks</span></span>

<span data-ttu-id="b1a55-136">網路接收會將內容廣播到網路位址。</span><span class="sxs-lookup"><span data-stu-id="b1a55-136">Network sinks broadcast content to a network address.</span></span> <span data-ttu-id="b1a55-137">讀取用戶端可以連接到位址以接收廣播。</span><span class="sxs-lookup"><span data-stu-id="b1a55-137">Reading clients can connect to the address to receive the broadcast.</span></span>

## <a name="push-sinks"></a><span data-ttu-id="b1a55-138">推播接收器</span><span class="sxs-lookup"><span data-stu-id="b1a55-138">Push Sinks</span></span>

<span data-ttu-id="b1a55-139">推播接收會將內容從寫入器傳遞至執行 Windows Media Services 的伺服器。</span><span class="sxs-lookup"><span data-stu-id="b1a55-139">Push sinks deliver content from the writer to a server running Windows Media Services.</span></span> <span data-ttu-id="b1a55-140">推播接收器通常用於一部電腦編碼即時內容，並將它傳遞給一或多部伺服器進行廣泛散發的案例。</span><span class="sxs-lookup"><span data-stu-id="b1a55-140">Push sinks are typically used in scenarios where one computer encodes live content and delivers it to one or more servers for wide distribution.</span></span> <span data-ttu-id="b1a55-141">使用推播接收可讓您將電腦專用於特定工作，以節省每部伺服器的頻寬和處理能力。</span><span class="sxs-lookup"><span data-stu-id="b1a55-141">Using a push sink enables you to dedicate computers to specific tasks, saving bandwidth and processing power on each server.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b1a55-142">相關主題</span><span class="sxs-lookup"><span data-stu-id="b1a55-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b1a55-143">**檔案寫入功能**</span><span class="sxs-lookup"><span data-stu-id="b1a55-143">**File Writing Features**</span></span>](file-writing-features.md)
</dt> <dt>

[<span data-ttu-id="b1a55-144">**使用寫入器接收器**</span><span class="sxs-lookup"><span data-stu-id="b1a55-144">**Working with Writer Sinks**</span></span>](working-with-writer-sinks.md)
</dt> </dl>

 

 





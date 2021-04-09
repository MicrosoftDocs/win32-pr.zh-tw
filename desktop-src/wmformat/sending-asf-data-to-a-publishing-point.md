---
title: 將 ASF 資料傳送至發行端點
description: 將 ASF 資料傳送至發行端點
ms.assetid: 8f01beae-4270-4cf5-afff-3f7014cae90f
keywords:
- Windows Media Format SDK，傳送 ASF 資料
- Windows Media Format SDK，發行端點
- Advanced Systems Format (ASF) ，傳送資料
- ASF (Advanced Systems Format) ，傳送資料
- Advanced Systems Format (ASF) 、發行端點
- ASF (Advanced Systems Format) ，發行端點
- 發行端點
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a0f38f4d24a458681c4b0dc4ee6d1a73563bdd2
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2020
ms.locfileid: "103681564"
---
# <a name="sending-asf-data-to-a-publishing-point"></a><span data-ttu-id="be466-110">將 ASF 資料傳送至發行端點</span><span class="sxs-lookup"><span data-stu-id="be466-110">Sending ASF Data to a Publishing Point</span></span>

<span data-ttu-id="be466-111">您可以使用 Windows Media Format SDK 將 ASF 資料推送至 Windows Media 伺服器上的發行端點。</span><span class="sxs-lookup"><span data-stu-id="be466-111">You can use the Windows Media Format SDK to push ASF data to a publishing point on a Windows Media server.</span></span> <span data-ttu-id="be466-112">然後伺服器會從該發行端點廣播資料。</span><span class="sxs-lookup"><span data-stu-id="be466-112">The server then broadcasts the data from that publishing point.</span></span> <span data-ttu-id="be466-113">如果您要在一部電腦上捕獲或重新編碼內容，而且想要從另一部電腦 (或數部電腦) 發佈內容，此案例就很有用。</span><span class="sxs-lookup"><span data-stu-id="be466-113">This scenario is useful if you are capturing or re-encoding content on one computer, and wish to distribute the content from another computer (or several computers).</span></span> <span data-ttu-id="be466-114">如果您需要將內容從防火牆內的電腦移至防火牆外部的 Windows Media 伺服器，這也很有用，因為推送散發會使用 HTTP 通訊協定。</span><span class="sxs-lookup"><span data-stu-id="be466-114">It is also useful if you need to move content from a computer inside a firewall to a Windows Media server outside the firewall, because push distribution uses the HTTP protocol.</span></span>

> [!Note]  
> <span data-ttu-id="be466-115">*發行端點* 的運作方式基本上就像是重新導向器。</span><span class="sxs-lookup"><span data-stu-id="be466-115">A *publishing point* acts essentially like a redirector.</span></span> <span data-ttu-id="be466-116">用戶端會在 URL 中指定發行端點 (例如 mms://MyServer/MyPublishingPoint) ，而伺服器會將此內容轉譯成內容的要求。</span><span class="sxs-lookup"><span data-stu-id="be466-116">The client specifies the publishing point in the URL (for example, mms://MyServer/MyPublishingPoint) and the server translates this into a request for content.</span></span>

 

<span data-ttu-id="be466-117">若要將資料推送至發行端點，請將推送接收物件附加至寫入器物件。</span><span class="sxs-lookup"><span data-stu-id="be466-117">To push data to the publishing point, attach the push sink object to the writer object.</span></span> <span data-ttu-id="be466-118">推播接收可用來開啟與伺服器的連線，以及管理推播會話。</span><span class="sxs-lookup"><span data-stu-id="be466-118">The push sink is used to open the connection to the server and manage the push session.</span></span> <span data-ttu-id="be466-119">寫入器物件會處理建立檔案的所有其他層面。</span><span class="sxs-lookup"><span data-stu-id="be466-119">The writer object handles all the other aspects of creating the file.</span></span>

<span data-ttu-id="be466-120">執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="be466-120">Perform the following steps:</span></span>

1.  <span data-ttu-id="be466-121">藉由呼叫 [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) 函式來建立寫入器物件，該函式會傳回 [**IWMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter) 指標。</span><span class="sxs-lookup"><span data-stu-id="be466-121">Create the writer object by calling the [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) function, which returns an [**IWMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter) pointer.</span></span>
2.  <span data-ttu-id="be466-122">藉由呼叫 [**WMCreateWriterPushSink**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriterpushsink) 函式來建立推送接收物件，該函式會傳回 [**IWMWriterPushSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpushsink) 指標。</span><span class="sxs-lookup"><span data-stu-id="be466-122">Create the push sink object by calling the [**WMCreateWriterPushSink**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriterpushsink) function, which returns an [**IWMWriterPushSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpushsink) pointer.</span></span>
3.  <span data-ttu-id="be466-123">在寫入器上呼叫 [**IWMWriterAdvanced：： AddSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink) ，並使用網路接收器的 **IWMWriterPushSink** 介面指標，以將網路接收器附加至寫入器。</span><span class="sxs-lookup"><span data-stu-id="be466-123">Attach the network sink to the writer by calling [**IWMWriterAdvanced::AddSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink) on the writer, with a pointer to the network sink's **IWMWriterPushSink** interface.</span></span>
4.  <span data-ttu-id="be466-124">藉由呼叫 [**IWMWriterPushSink：： connect**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpushsink-connect)來連接到伺服器。</span><span class="sxs-lookup"><span data-stu-id="be466-124">Connect to the server by calling [**IWMWriterPushSink::Connect**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpushsink-connect).</span></span>
5.  <span data-ttu-id="be466-125">寫入資料流。</span><span class="sxs-lookup"><span data-stu-id="be466-125">Write the stream.</span></span> <span data-ttu-id="be466-126">此步驟包含在寫入器物件上設定設定檔、將範例傳送至寫入器，以及可能的其他工作。</span><span class="sxs-lookup"><span data-stu-id="be466-126">This step involves setting the profile on the writer object, sending samples to the writer, and possibly other tasks.</span></span> <span data-ttu-id="be466-127">如需詳細資訊，請參閱 [寫入 ASF](writing-asf-files.md)檔。</span><span class="sxs-lookup"><span data-stu-id="be466-127">For more information, see [Writing ASF Files](writing-asf-files.md).</span></span> <span data-ttu-id="be466-128">其他工作可能包括設定中繼資料屬性 (如 [使用中繼資料](working-with-metadata.md)) 中所述，或在資料流程上設定即時 DRM (如 [啟用 DRM 支援](enabling-drm-support.md)) 所述。</span><span class="sxs-lookup"><span data-stu-id="be466-128">Additional tasks might include setting metadata attributes (as described in [Working with Metadata](working-with-metadata.md)) or setting live-DRM on the stream (as described in [Enabling DRM Support](enabling-drm-support.md)).</span></span> <span data-ttu-id="be466-129">這些工作的執行方式與寫入 ASF 檔案的方式完全相同。</span><span class="sxs-lookup"><span data-stu-id="be466-129">These tasks are performed exactly as they are for ASF file writing.</span></span>
6.  <span data-ttu-id="be466-130">撰寫完成之後，請在寫入器上呼叫 [**IWMWriterAdvanced：： RemoveSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-removesink) ，以卸離推送接收物件。</span><span class="sxs-lookup"><span data-stu-id="be466-130">After you are done writing, call [**IWMWriterAdvanced::RemoveSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-removesink) on the writer to detach the push sink object.</span></span>
7.  <span data-ttu-id="be466-131">在推播接收上呼叫 [**IWMWriterPushSink：： EndSession**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpushsink-endsession) ，以結束與伺服器的會話。</span><span class="sxs-lookup"><span data-stu-id="be466-131">Call [**IWMWriterPushSink::EndSession**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpushsink-endsession) on the push sink to end the session with the server.</span></span>

<span data-ttu-id="be466-132">這些步驟說明于 WMVNetWrite 範例應用程式中。</span><span class="sxs-lookup"><span data-stu-id="be466-132">These steps are illustrated in the WMVNetWrite sample application.</span></span>

> [!Note]  
> <span data-ttu-id="be466-133">如果您要傳送非常低位的僅限影片檔案，它可能不會在發行端點上開始播放幾秒鐘的時間。</span><span class="sxs-lookup"><span data-stu-id="be466-133">If you are sending a very-low-bit-rate video-only file, it might not start playing on the publishing point for several seconds.</span></span> <span data-ttu-id="be466-134">這種情況可能會在各種情況下發生，例如，當單一封包包含許多小型影片框架且沒有音訊，或第一個封包與低位視頻檔案中的第二個封包之間有很長的時間間距時。</span><span class="sxs-lookup"><span data-stu-id="be466-134">This can happen in various cases, for example when a single packet contains many small video frames and no audio, or when there is a long time gap between the first packet and the second packet in a low-bit-rate video-only file.</span></span> <span data-ttu-id="be466-135">若要避免這個問題，請在檔案中插入無訊息音訊串流。</span><span class="sxs-lookup"><span data-stu-id="be466-135">To avoid this problem, insert a silent audio stream into the file.</span></span>

 

## <a name="authentication"></a><span data-ttu-id="be466-136">驗證</span><span class="sxs-lookup"><span data-stu-id="be466-136">Authentication</span></span>

<span data-ttu-id="be466-137">推播接收物件會自動處理伺服器的驗證。</span><span class="sxs-lookup"><span data-stu-id="be466-137">Authentication to the server is automatically handled by the push sink object.</span></span> <span data-ttu-id="be466-138">不過，應用程式可能需要提供認證。</span><span class="sxs-lookup"><span data-stu-id="be466-138">However, the application may need to supply credentials.</span></span> <span data-ttu-id="be466-139">這是透過 **IWMCredentialCallback** 回呼介面完成的，如下所示：</span><span class="sxs-lookup"><span data-stu-id="be466-139">This is done through the **IWMCredentialCallback** callback interface, as follows:</span></span>

1.  <span data-ttu-id="be466-140">在您的應用程式中執行 [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) 和 [**IWMCredentialCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcredentialcallback) 介面。</span><span class="sxs-lookup"><span data-stu-id="be466-140">Implement the [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) and [**IWMCredentialCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcredentialcallback) interface in your application.</span></span>
2.  <span data-ttu-id="be466-141">查詢 [**IWMRegisterCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback) 介面的推送接收物件。</span><span class="sxs-lookup"><span data-stu-id="be466-141">Query the push sink object for the [**IWMRegisterCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback) interface.</span></span>
3.  <span data-ttu-id="be466-142">使用應用程式的 **IWMStatusCallback** 介面指標呼叫 [**IWMRegisterCallback：： Advise**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistercallback-advise) 。</span><span class="sxs-lookup"><span data-stu-id="be466-142">Call [**IWMRegisterCallback::Advise**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistercallback-advise) with a pointer to your application's **IWMStatusCallback** interface.</span></span>
4.  <span data-ttu-id="be466-143">如果推送接收需要從應用程式取得認證，它會查詢 **IWMCredentialCallback** 介面的 **IWMStatusCallback** 指標，並呼叫 [**IWMCredentialCallback：： AcquireCredentials**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcredentialcallback-acquirecredentials)。</span><span class="sxs-lookup"><span data-stu-id="be466-143">If the push sink needs to get credentials from the application, it queries the **IWMStatusCallback** pointer for the **IWMCredentialCallback** interface and calls [**IWMCredentialCallback::AcquireCredentials**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcredentialcallback-acquirecredentials).</span></span> <span data-ttu-id="be466-144">如需此方法的詳細資訊，請參閱 [驗證](authentication.md)。</span><span class="sxs-lookup"><span data-stu-id="be466-144">For information about this method, see [Authentication](authentication.md).</span></span>
5.  <span data-ttu-id="be466-145">當您完成時，請呼叫 [**IWMRegisterCallback：： Unadvise**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistercallback-unadvise) ，以停止從推播接收取得事件通知。</span><span class="sxs-lookup"><span data-stu-id="be466-145">When you are done, call [**IWMRegisterCallback::Unadvise**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistercallback-unadvise) to stop getting event notifications from the push sink.</span></span>

## <a name="related-topics"></a><span data-ttu-id="be466-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="be466-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="be466-147">**透過網路傳送 ASF 資料**</span><span class="sxs-lookup"><span data-stu-id="be466-147">**Sending ASF Data Over a Network**</span></span>](sending-asf-data-over-a-network.md)
</dt> <dt>

[<span data-ttu-id="be466-148">**使用寫入器接收器**</span><span class="sxs-lookup"><span data-stu-id="be466-148">**Working with Writer Sinks**</span></span>](working-with-writer-sinks.md)
</dt> <dt>

[<span data-ttu-id="be466-149">**寫入器推送接收物件**</span><span class="sxs-lookup"><span data-stu-id="be466-149">**Writer Push Sink Object**</span></span>](writer-push-sink-object.md)
</dt> </dl>

 

 





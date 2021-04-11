---
title: 廣播 ASF 資料
description: 廣播 ASF 資料
ms.assetid: 1b04f361-8147-4f6a-8c9d-d8eeed28550a
keywords:
- Windows Media Format SDK，廣播 ASF 資料
- Advanced Systems Format (ASF) ，廣播資料
- ASF (Advanced Systems Format) ，廣播資料
- Windows Media Format SDK，傳送 ASF 資料
- Advanced Systems Format (ASF) ，傳送資料
- ASF (Advanced Systems Format) ，傳送資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42339b4a3e60666c1ea0cb69a07dfdc836b19409
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/21/2020
ms.locfileid: "104023151"
---
# <a name="broadcasting-asf-data"></a><span data-ttu-id="e37b1-109">廣播 ASF 資料</span><span class="sxs-lookup"><span data-stu-id="e37b1-109">Broadcasting ASF Data</span></span>

<span data-ttu-id="e37b1-110">本主題說明如何使用 HTTP 通訊協定，在網路上傳送 ASF 資料。</span><span class="sxs-lookup"><span data-stu-id="e37b1-110">This topic describes how to send ASF data across a network using the HTTP protocol.</span></span> <span data-ttu-id="e37b1-111">透過網路傳送檔案需要使用寫入器物件，因此在閱讀本主題之前，您應該先對此物件有大致的瞭解。</span><span class="sxs-lookup"><span data-stu-id="e37b1-111">Sending files over a network requires the use of the writer object, so you should have a general understanding of this object before reading this topic.</span></span> <span data-ttu-id="e37b1-112">如需詳細資訊，請參閱 [寫入 ASF](writing-asf-files.md)檔。</span><span class="sxs-lookup"><span data-stu-id="e37b1-112">For more information, see [Writing ASF Files](writing-asf-files.md).</span></span>

<span data-ttu-id="e37b1-113">如果您要開始使用未壓縮的資料，請執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="e37b1-113">If you are starting with uncompressed data, do the following:</span></span>

1.  <span data-ttu-id="e37b1-114">藉由呼叫 [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) 函數來建立寫入器物件。</span><span class="sxs-lookup"><span data-stu-id="e37b1-114">Create the writer object by calling the [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) function.</span></span> <span data-ttu-id="e37b1-115">此函數會傳回 **IWMWriter** 指標。</span><span class="sxs-lookup"><span data-stu-id="e37b1-115">This function returns an **IWMWriter** pointer.</span></span>
    ```C++
    IWMWriter *pWriter;
    hr = WMCreateWriter(NULL, &pWriter);
    ```

    

2.  <span data-ttu-id="e37b1-116">藉由呼叫 [**WMCreateWriterNetworkSink**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriternetworksink) 函式來建立網路接收器物件，該函式會傳回 **IWMWriterNetworkSink** 指標。</span><span class="sxs-lookup"><span data-stu-id="e37b1-116">Create the network sink object by calling the [**WMCreateWriterNetworkSink**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriternetworksink) function, which returns an **IWMWriterNetworkSink** pointer.</span></span>
    ```C++
    IWMWriterNetworkSink *pNetSink;
    hr = WMCreateWriterNetworkSink(&pNetSink);
    ```

    

3.  <span data-ttu-id="e37b1-117">在網路接收上呼叫 [**IWMWriterNetworkSink：： Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-open) ，並指定要開啟的埠號碼。例如，8080。</span><span class="sxs-lookup"><span data-stu-id="e37b1-117">Call [**IWMWriterNetworkSink::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-open) on the network sink and specify the port number to open; for example, 8080.</span></span> <span data-ttu-id="e37b1-118">（選擇性）呼叫 [**IWMWriterNetworkSink：： GetHostURL**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-gethosturl) 以取得主機的 URL。</span><span class="sxs-lookup"><span data-stu-id="e37b1-118">Optionally, call [**IWMWriterNetworkSink::GetHostURL**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-gethosturl) to get the URL of the host.</span></span> <span data-ttu-id="e37b1-119">用戶端會存取此 URL 的內容。</span><span class="sxs-lookup"><span data-stu-id="e37b1-119">Clients will access the content from this URL.</span></span> <span data-ttu-id="e37b1-120">您也可以呼叫 [**IWMWriterNetworkSink：： SetMaximumClients**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-setmaximumclients) 來限制用戶端數目。</span><span class="sxs-lookup"><span data-stu-id="e37b1-120">You can also call [**IWMWriterNetworkSink::SetMaximumClients**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-setmaximumclients) to restrict the number of clients.</span></span>
    ```C++
    DWORD dwPortNum = 8080;
    hr = pNetSink->Open( &dwPortNum)
    ```

    

4.  <span data-ttu-id="e37b1-121">在寫入器上呼叫 [**IWMWriterAdvanced：： AddSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink) ，並使用網路接收器的 **IWMWriterNetworkSink** 介面指標，以將網路接收器附加至寫入器。</span><span class="sxs-lookup"><span data-stu-id="e37b1-121">Attach the network sink to the writer by calling [**IWMWriterAdvanced::AddSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink) on the writer, with a pointer to the network sink's **IWMWriterNetworkSink** interface.</span></span>
    ```C++
    IWMWriterAdvanced *pWriterAdvanced;
    hr = pWriter->QueryInterface(IID_IWMWriterAdvanced, ( void** ) pWriterAdvanced );
    if (SUCCEEDED(hr))
    {
        pWriterAdvanced->AddSink(pNetSink);
    }
    ```

    

5.  <span data-ttu-id="e37b1-122">在寫入器物件上呼叫 [**IWMWriter：： SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) 方法，並使用 [**IWMProfile**](iwmprofile.md) 指標來設定 ASF 設定檔。</span><span class="sxs-lookup"><span data-stu-id="e37b1-122">Set the ASF profile by calling the [**IWMWriter::SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) method on the writer object, with an [**IWMProfile**](iwmprofile.md) pointer.</span></span> <span data-ttu-id="e37b1-123">如需建立設定檔的詳細資訊，請參閱 [使用設定檔](working-with-profiles.md)。</span><span class="sxs-lookup"><span data-stu-id="e37b1-123">For information about creating a profile, see [Working with Profiles](working-with-profiles.md).</span></span>
6.  <span data-ttu-id="e37b1-124">（選擇性）使用寫入器上的 [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) 介面來指定中繼資料。</span><span class="sxs-lookup"><span data-stu-id="e37b1-124">Optionally, specify metadata using the [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) interface on the writer.</span></span>
7.  <span data-ttu-id="e37b1-125">在寫入器上呼叫 [**IWMWriter：： BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting) 。</span><span class="sxs-lookup"><span data-stu-id="e37b1-125">Call [**IWMWriter::BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting) on the writer.</span></span>
    ```C++
    hr = pWriter->BeginWriting();
    ```

    

8.  <span data-ttu-id="e37b1-126">針對每個範例，呼叫 [**IWMWriter：： WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) 方法。</span><span class="sxs-lookup"><span data-stu-id="e37b1-126">For each sample, call the [**IWMWriter::WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) method.</span></span> <span data-ttu-id="e37b1-127">指定串流號碼、展示時間、樣本的持續時間，以及範例緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="e37b1-127">Specify the stream number, the presentation time, the duration of the sample, and a pointer to the sample buffer.</span></span> <span data-ttu-id="e37b1-128">**WriteSample** 方法會壓縮範例。</span><span class="sxs-lookup"><span data-stu-id="e37b1-128">The **WriteSample** method compresses the samples.</span></span>
9.  <span data-ttu-id="e37b1-129">當您完成時，請在寫入器上呼叫 [**IWMWriter：： EndWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-endwriting) 。</span><span class="sxs-lookup"><span data-stu-id="e37b1-129">When you are done, call [**IWMWriter::EndWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-endwriting) on the writer.</span></span>
    ```C++
    hr = pWriter->EndWriting();
    ```

    

10. <span data-ttu-id="e37b1-130">在寫入器上呼叫 [**IWMWriterAdvanced：： RemoveSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-removesink) ，以卸離網路接收器物件。</span><span class="sxs-lookup"><span data-stu-id="e37b1-130">Call [**IWMWriterAdvanced::RemoveSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-removesink) on the writer to detach the network sink object.</span></span>
    ```C++
    hr = pWriterAdvanced->RemoveSink(pNetSink);
    ```

    

11. <span data-ttu-id="e37b1-131">在網路接收上呼叫 [**IWMWriterNetworkSink：： Close**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-close) 以釋放埠。</span><span class="sxs-lookup"><span data-stu-id="e37b1-131">Call [**IWMWriterNetworkSink::Close**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-close) on the network sink to release the port.</span></span>
    ```C++
    hr = pNetSink->Close();
    ```

    

<span data-ttu-id="e37b1-132">透過網路串流 ASF 內容的另一種方式，是從現有的 ASF 檔案讀取該內容。</span><span class="sxs-lookup"><span data-stu-id="e37b1-132">Another way to stream ASF content over a network is to read it from an existing ASF file.</span></span> <span data-ttu-id="e37b1-133">SDK 中提供的 WMVNetWrite 範例會示範這種方法。</span><span class="sxs-lookup"><span data-stu-id="e37b1-133">The WMVNetWrite sample provided in the SDK demonstrates this approach.</span></span> <span data-ttu-id="e37b1-134">除了先前所列的步驟之外，請執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="e37b1-134">In addition to the steps listed previously, do the following:</span></span>

1.  <span data-ttu-id="e37b1-135">建立讀取器物件，並使用檔案的名稱來呼叫 **Open** 方法。</span><span class="sxs-lookup"><span data-stu-id="e37b1-135">Create a reader object and call the **Open** method with the name of the file.</span></span>
2.  <span data-ttu-id="e37b1-136">針對 reader 物件呼叫 [**IWMReaderAdvanced：： SetManualStreamSelection**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setmanualstreamselection) ，並將值 **設為 TRUE**。</span><span class="sxs-lookup"><span data-stu-id="e37b1-136">Call [**IWMReaderAdvanced::SetManualStreamSelection**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setmanualstreamselection) on the reader object, with the value **TRUE**.</span></span> <span data-ttu-id="e37b1-137">這可讓應用程式讀取檔案中的每個資料流程，包括具有相互排除的資料流程。</span><span class="sxs-lookup"><span data-stu-id="e37b1-137">This enables the application to read every stream in the file, including streams with mutual exclusion.</span></span>
3.  <span data-ttu-id="e37b1-138">查詢 [**IWMProfile**](iwmprofile.md) 介面的讀取器。</span><span class="sxs-lookup"><span data-stu-id="e37b1-138">Query the reader for the [**IWMProfile**](iwmprofile.md) interface.</span></span> <span data-ttu-id="e37b1-139">當您在寫入器物件上呼叫 [**IWMWriter：： SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) 時，請使用這個指標， (上一個程式中的步驟 5) 。</span><span class="sxs-lookup"><span data-stu-id="e37b1-139">Use this pointer when you call [**IWMWriter::SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) on the writer object (step 5 in the previous procedure).</span></span>
4.  <span data-ttu-id="e37b1-140">針對設定檔中定義的每個資料流程，呼叫 [**IWMProfile：： GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) 來取得資料流程號碼。</span><span class="sxs-lookup"><span data-stu-id="e37b1-140">For every stream defined in the profile, call [**IWMProfile::GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) to get the stream number.</span></span> <span data-ttu-id="e37b1-141">將此串流號碼傳遞給讀取器的 [**IWMReaderAdvanced：： SetReceiveStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setreceivestreamsamples) 方法。</span><span class="sxs-lookup"><span data-stu-id="e37b1-141">Pass this stream number to the reader's [**IWMReaderAdvanced::SetReceiveStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setreceivestreamsamples) method.</span></span> <span data-ttu-id="e37b1-142">這個方法會通知讀者傳遞壓縮的範例，而不是解碼它們。</span><span class="sxs-lookup"><span data-stu-id="e37b1-142">This method informs the reader to deliver compressed samples, rather than decoding them.</span></span> <span data-ttu-id="e37b1-143">這些範例會透過應用程式的 [**IWMReaderCallbackAdvanced：： OnStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamsample) 回呼方法傳遞至應用程式。</span><span class="sxs-lookup"><span data-stu-id="e37b1-143">The samples will be delivered to the application through the application's [**IWMReaderCallbackAdvanced::OnStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamsample) callback method.</span></span>

    <span data-ttu-id="e37b1-144">您必須為每個已解壓縮的資料流程取得編解碼器資訊，並在廣播之前將它新增至標頭。</span><span class="sxs-lookup"><span data-stu-id="e37b1-144">You must obtain codec information for every stream that you read uncompressed and add it to the header before broadcast.</span></span> <span data-ttu-id="e37b1-145">若要取得編解碼器資訊，請呼叫 [**IWMHeaderInfo2：： GetCodecInfoCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfocount) 和 [**IWMHeaderInfo2：： GetCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfo) ，以列舉讀取器中與檔案相關聯的編解碼器。</span><span class="sxs-lookup"><span data-stu-id="e37b1-145">To obtain the codec information, call [**IWMHeaderInfo2::GetCodecInfoCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfocount) and [**IWMHeaderInfo2::GetCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfo) to enumerate the codecs associated with the file in the reader.</span></span> <span data-ttu-id="e37b1-146">選取符合資料流程設定的編解碼器資訊。</span><span class="sxs-lookup"><span data-stu-id="e37b1-146">Select the codec information that matches the stream configuration.</span></span> <span data-ttu-id="e37b1-147">然後藉由呼叫 [**IWMHeaderInfo3：： AddCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addcodecinfo)來設定寫入器中的編解碼器資訊，傳遞從讀取器取得的資訊。</span><span class="sxs-lookup"><span data-stu-id="e37b1-147">Then set the codec information in the writer by calling [**IWMHeaderInfo3::AddCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addcodecinfo), passing the information obtained from the reader.</span></span>

5.  <span data-ttu-id="e37b1-148">在寫入器上設定設定檔之後，請在寫入器上呼叫 [**IWMWriter：： GetInputCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputcount) 來取得輸入的數目。</span><span class="sxs-lookup"><span data-stu-id="e37b1-148">After you set the profile on the writer, call [**IWMWriter::GetInputCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputcount) on the writer to get the number of inputs.</span></span> <span data-ttu-id="e37b1-149">針對每個輸入，呼叫 [**IWMWriter：： SetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops) ，其值 **為 Null**。</span><span class="sxs-lookup"><span data-stu-id="e37b1-149">For each input, call [**IWMWriter::SetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops) with the value **NULL**.</span></span> <span data-ttu-id="e37b1-150">這會向寫入器物件表示應用程式會提供壓縮的範例，因此寫入器不需要使用任何編解碼器來壓縮資料。</span><span class="sxs-lookup"><span data-stu-id="e37b1-150">This indicates to the writer object that the application will deliver compressed samples, so the writer does not have to use any codecs to compress the data.</span></span> <span data-ttu-id="e37b1-151">呼叫 **BeginWriting** 之前，請務必先呼叫 **SetInputProps** 。</span><span class="sxs-lookup"><span data-stu-id="e37b1-151">Make sure to call **SetInputProps** before calling **BeginWriting**.</span></span>
6.  <span data-ttu-id="e37b1-152">（選擇性）將中繼資料屬性從讀取器複製到寫入器。</span><span class="sxs-lookup"><span data-stu-id="e37b1-152">Optionally, copy the metadata attributes from the reader to the writer</span></span>
7.  <span data-ttu-id="e37b1-153">由於讀取器的範例已經壓縮，因此請使用 [**IWMWriterAdvanced：： WriteStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-writestreamsample) 方法來撰寫範例，而不是 **WriteSample** 方法。</span><span class="sxs-lookup"><span data-stu-id="e37b1-153">Because the samples from the reader are already compressed, use the [**IWMWriterAdvanced::WriteStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-writestreamsample) method to write the samples, instead of the **WriteSample** method.</span></span> <span data-ttu-id="e37b1-154">**WriteStreamSample** 方法會略過寫入器物件的一般壓縮程式。</span><span class="sxs-lookup"><span data-stu-id="e37b1-154">The **WriteStreamSample** method bypasses the writer object's usual compression procedures.</span></span>
8.  <span data-ttu-id="e37b1-155">當讀取器到達檔案結尾時，會將 WMT \_ EOF 通知傳送至應用程式。</span><span class="sxs-lookup"><span data-stu-id="e37b1-155">When the reader reaches the end of the file, it sends a WMT\_EOF notification to the application.</span></span>

<span data-ttu-id="e37b1-156">此外，應用程式應該會驅動讀取器物件上的時鐘，讓讀取器儘快從檔案提取資料。</span><span class="sxs-lookup"><span data-stu-id="e37b1-156">In addition, the application should drive the clock on the reader object, so that the reader pulls data from the file as quickly as possible.</span></span> <span data-ttu-id="e37b1-157">若要這樣做，請在讀取器上呼叫 [**IWMReaderAdvanced：： SetUserProvidedClock**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setuserprovidedclock) 方法，並將值 **設為 TRUE**。</span><span class="sxs-lookup"><span data-stu-id="e37b1-157">To do this, call the [**IWMReaderAdvanced::SetUserProvidedClock**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setuserprovidedclock) method on the reader, with the value **TRUE**.</span></span> <span data-ttu-id="e37b1-158">當讀取器 \_ 傳送 WMT 啟動通知之後，請呼叫 [**IWMReaderAdvanced：:D elivertime**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-delivertime) ，並指定讀取器應提供的時間間隔。</span><span class="sxs-lookup"><span data-stu-id="e37b1-158">After the reader sends the WMT\_STARTED notification, call [**IWMReaderAdvanced::DeliverTime**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-delivertime) and specify the time interval that the reader should deliver.</span></span> <span data-ttu-id="e37b1-159">讀取器完成此時間間隔之後，它會呼叫應用程式的 [**IWMReaderCallbackAdvanced：： OnTime**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-ontime) 回呼方法。</span><span class="sxs-lookup"><span data-stu-id="e37b1-159">After the reader is done reading this time interval, it calls the application's [**IWMReaderCallbackAdvanced::OnTime**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-ontime) callback method.</span></span> <span data-ttu-id="e37b1-160">應用程式應該再次呼叫 **DeliverTime** ，以讀取下一個時間間隔。</span><span class="sxs-lookup"><span data-stu-id="e37b1-160">The application should call **DeliverTime** again to read the next time interval.</span></span> <span data-ttu-id="e37b1-161">例如，若要以一秒的間隔讀取檔案：</span><span class="sxs-lookup"><span data-stu-id="e37b1-161">For example, to read from the file in one-second intervals:</span></span>


```C++
// Initial call to DeliverTime.
QWORD m_qwTime = 10000000; // 1 second.
hr = m_pReaderAdvanced->DeliverTime(m_qwTime);

// In the callback:
HRESULT CNetWrite::OnTime(QWORD cnsCurrentTime, void *pvContext)
{
    HRESULT hr = S_OK;
    // Continue calling DeliverTime until the end of the file.
    if(!m_bEOF)
    {
        m_qwTime += 10000000; // 1 second.
        hr = m_pReaderAdvanced->DeliverTime(m_qwTime);
    }
    return S_OK;
}
```



## <a name="related-topics"></a><span data-ttu-id="e37b1-162">相關主題</span><span class="sxs-lookup"><span data-stu-id="e37b1-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e37b1-163">**透過網路傳送 ASF 資料**</span><span class="sxs-lookup"><span data-stu-id="e37b1-163">**Sending ASF Data Over a Network**</span></span>](sending-asf-data-over-a-network.md)
</dt> <dt>

[<span data-ttu-id="e37b1-164">**使用寫入器接收器**</span><span class="sxs-lookup"><span data-stu-id="e37b1-164">**Working with Writer Sinks**</span></span>](working-with-writer-sinks.md)
</dt> </dl>

 

 





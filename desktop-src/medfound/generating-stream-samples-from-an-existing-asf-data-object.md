---
description: 從現有的 ASF 資料物件產生資料流程範例
ms.assetid: eb27f122-d958-495d-98ea-8befd105a9a8
title: 從現有的 ASF 資料物件產生資料流程範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee612c9352e3295d6b4957922e385de40a9a1fa3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111768"
---
# <a name="generating-stream-samples-from-an-existing-asf-data-object"></a><span data-ttu-id="048e6-103">從現有的 ASF 資料物件產生資料流程範例</span><span class="sxs-lookup"><span data-stu-id="048e6-103">Generating Stream Samples from an Existing ASF Data Object</span></span>

<span data-ttu-id="048e6-104">ASF *分隔器* 物件是 WMContainer 層元件，可剖析 Advanced Systems 格式的 Asf 資料物件 (asf) 檔。</span><span class="sxs-lookup"><span data-stu-id="048e6-104">The ASF *splitter* object is a WMContainer layer component that parses the ASF Data Object of an Advanced Systems Format (ASF) file.</span></span>

<span data-ttu-id="048e6-105">將資料封包傳遞給分隔器之前，應用程式必須在分隔器上初始化、設定和選取資料流程，才能為剖析程式做好準備。</span><span class="sxs-lookup"><span data-stu-id="048e6-105">Before passing data packets to the splitter, the application must initialize, configure, and select streams on the splitter in order to prepare it for the parsing process.</span></span> <span data-ttu-id="048e6-106">如需詳細資訊，請參閱 [建立 Asf 分隔器物件](creating-the-asf-splitter-object.md) 和設定 [Asf 分隔器物件](configuring-the-asf-splitter-object.md)。</span><span class="sxs-lookup"><span data-stu-id="048e6-106">For information, see [Creating the ASF Splitter Object](creating-the-asf-splitter-object.md) and [Configuring the ASF Splitter Object](configuring-the-asf-splitter-object.md).</span></span>

<span data-ttu-id="048e6-107">剖析 ASF 資料物件所需的方法如下：</span><span class="sxs-lookup"><span data-stu-id="048e6-107">The methods required for parsing the ASF Data Object are:</span></span>

-   <span data-ttu-id="048e6-108">[**IMFASFSplitter：**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata) 將包含資料封包的緩衝區推送至分隔器，以啟動剖析程式的:P arsedata。</span><span class="sxs-lookup"><span data-stu-id="048e6-108">[**IMFASFSplitter::ParseData**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata) that starts the parsing process by pushing the buffer containing data packets to the splitter.</span></span>
-   <span data-ttu-id="048e6-109">[**IMFASFSplitter：： GetNextSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getnextsample) ，可收集從傳遞給分隔器的緩衝區產生的資料流程範例。</span><span class="sxs-lookup"><span data-stu-id="048e6-109">[**IMFASFSplitter::GetNextSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getnextsample) that collects stream samples that were generated from the buffer passed to splitter.</span></span>

## <a name="finding-the-data-offset"></a><span data-ttu-id="048e6-110">尋找資料位移</span><span class="sxs-lookup"><span data-stu-id="048e6-110">Finding the Data Offset</span></span>

<span data-ttu-id="048e6-111">開始剖析程式之前，應用程式必須在 ASF 檔案內找出資料物件。</span><span class="sxs-lookup"><span data-stu-id="048e6-111">Before starting the parsing process, the application must locate the Data Object within the ASF file.</span></span> <span data-ttu-id="048e6-112">有兩種方式可從檔案的開頭取得資料物件的位移：</span><span class="sxs-lookup"><span data-stu-id="048e6-112">There are two ways to get the offset of the Data Object from the start of the file:</span></span>

-   <span data-ttu-id="048e6-113">在初始化 ContentInfo 物件之前，您可以呼叫 [**IMFASFContentInfo：： GetHeaderSize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getheadersize) 方法。</span><span class="sxs-lookup"><span data-stu-id="048e6-113">Before you have initialized the ContentInfo object, you can call the [**IMFASFContentInfo::GetHeaderSize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getheadersize) method.</span></span> <span data-ttu-id="048e6-114">此方法需要包含 ASF 標頭前30個位元組的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="048e6-114">This method requires a buffer that contains the first 30 bytes of the ASF header.</span></span> <span data-ttu-id="048e6-115">它會傳回整個標頭的大小，表示第一個資料封包的位移。</span><span class="sxs-lookup"><span data-stu-id="048e6-115">It returns the size of the entire header that indicates the offset to the first data packet.</span></span> <span data-ttu-id="048e6-116">此值也包含資料物件標頭大小50個位元組。</span><span class="sxs-lookup"><span data-stu-id="048e6-116">This value also includes the Data Object header size of 50 bytes.</span></span>
-   <span data-ttu-id="048e6-117">初始化 ContentInfo 物件之後，您可以藉由呼叫 [**IMFASFContentInfo：： GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor)來取得簡報描述項，然後查詢適用于 [**MF \_ PD \_ ASF \_ 資料 \_ 起始 \_ 位移**](mf-pd-asf-data-start-offset-attribute.md) 屬性的簡報描述項。</span><span class="sxs-lookup"><span data-stu-id="048e6-117">After you have initialized the ContentInfo object, you can get the presentation descriptor by calling [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor), and then querying the presentation descriptor for the [**MF\_PD\_ASF\_DATA\_START\_OFFSET**](mf-pd-asf-data-start-offset-attribute.md) attribute.</span></span> <span data-ttu-id="048e6-118">這個屬性的值是標頭大小。</span><span class="sxs-lookup"><span data-stu-id="048e6-118">The value of this attribute is the header size.</span></span>
    > [!Note]  
    > <span data-ttu-id="048e6-119">展示描述項上的 [ [**MF \_ PD \_ ASF \_ 資料 \_ 長度**](mf-pd-asf-data-length-attribute.md) ] 屬性會指定 ASF 資料物件的長度。</span><span class="sxs-lookup"><span data-stu-id="048e6-119">The [**MF\_PD\_ASF\_DATA\_LENGTH**](mf-pd-asf-data-length-attribute.md) attribute on the presentation descriptor specifies the length of the ASF Data Object.</span></span>

     

<span data-ttu-id="048e6-120">在這兩種情況下，傳回的值是標頭物件的大小加上資料物件的標頭區段大小。</span><span class="sxs-lookup"><span data-stu-id="048e6-120">In both cases, the returned value is the size of the Header Object plus the size of the header section of the Data Object.</span></span> <span data-ttu-id="048e6-121">因此，產生的值是 ASF 資料物件中資料封包開頭的位移。</span><span class="sxs-lookup"><span data-stu-id="048e6-121">Therefore, the resulting value is the offset to the start of the data packets in the ASF Data Object.</span></span> <span data-ttu-id="048e6-122">當您開始將資料傳送到分隔器時，資料必須從 ASF 檔案開頭的這個位移開始。</span><span class="sxs-lookup"><span data-stu-id="048e6-122">When you begin sending data to the splitter, the data must start at this offset from the beginning of the ASF file.</span></span>

<span data-ttu-id="048e6-123">位移值會以參數的形式傳遞至 **ParseData** ，以啟動剖析程式。</span><span class="sxs-lookup"><span data-stu-id="048e6-123">The offset value is passed as a parameter to **ParseData** that starts the parsing process.</span></span>

<span data-ttu-id="048e6-124">資料物件會分割成資料封包。</span><span class="sxs-lookup"><span data-stu-id="048e6-124">The Data Object is divided into data packets.</span></span> <span data-ttu-id="048e6-125">每個資料封包都包含一個資料封包標頭，以提供封包剖析資訊和承載資料—實際的數位媒體資料。</span><span class="sxs-lookup"><span data-stu-id="048e6-125">Each data packet contains a data packet header that provides packet parsing information and the payload data—the actual digital media data.</span></span> <span data-ttu-id="048e6-126">在搜尋案例中，應用程式可能會想要讓分隔器開始在特定的資料封包上進行剖析。</span><span class="sxs-lookup"><span data-stu-id="048e6-126">In a seeking scenario, the application might want the splitter to start parsing at a particular data packet.</span></span> <span data-ttu-id="048e6-127">若要這樣做，您可以使用 ASF 索引子來取得位移。</span><span class="sxs-lookup"><span data-stu-id="048e6-127">To do this, you can use the ASF Indexer is used to retrieve the offset.</span></span> <span data-ttu-id="048e6-128">索引子會傳回從封包界限開始的位移值。</span><span class="sxs-lookup"><span data-stu-id="048e6-128">The indexer returns an offset value that starts at the packet boundary.</span></span> <span data-ttu-id="048e6-129">如果您不是使用索引子，請確定位移是從資料封包標頭的開頭開始。</span><span class="sxs-lookup"><span data-stu-id="048e6-129">If you are not using the indexer, make sure that the offset starts at the start of the data packet header.</span></span> <span data-ttu-id="048e6-130">如果將不正確位移傳遞給分隔器，例如值沒有指向封包界限， **ParseHeader** 和 **GetNextSample** 呼叫會成功，但 **GetNextSample** 不會取出任何範例，且 *pSample* 參數中會收到 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="048e6-130">If an invalid offset is passed to the splitter, such as the value does not point at the packet boundary, **ParseHeader** and **GetNextSample** calls succeed but **GetNextSample** does not retrieve any samples and **NULL** is received in the *pSample* parameter.</span></span>

<span data-ttu-id="048e6-131">如果分隔器已設定為以反向方向進行剖析，則分隔器一律會在傳遞至 **ParseData** 之媒體緩衝區的結尾處開始剖析。</span><span class="sxs-lookup"><span data-stu-id="048e6-131">If the splitter is configured to parse in the reverse direction, then the splitter always starts parsing at the end of the media buffer that is passed to **ParseData**.</span></span> <span data-ttu-id="048e6-132">因此，若要在呼叫 **ParseData** 時進行反向剖析，請在 *cbLength* 參數中傳遞位移，這會指定資料的長度，並將 *cbBufferOffset* 設定為零。</span><span class="sxs-lookup"><span data-stu-id="048e6-132">Therefore, for reverse parsing in the call to **ParseData**, pass the offset in the *cbLength* parameter, which specifies the length of the data and set *cbBufferOffset* to zero.</span></span>

## <a name="generating-samples-for-asf-data-packets"></a><span data-ttu-id="048e6-133">產生 ASF 資料封包的範例</span><span class="sxs-lookup"><span data-stu-id="048e6-133">Generating Samples for ASF Data Packets</span></span>

<span data-ttu-id="048e6-134">應用程式會將資料封包傳遞給分隔器，以啟動剖析程式。</span><span class="sxs-lookup"><span data-stu-id="048e6-134">An application starts the parsing process by passing the data packets to the splitter.</span></span> <span data-ttu-id="048e6-135">分隔器的輸入是一系列的媒體緩衝區，其中包含資料物件的整個或片段。</span><span class="sxs-lookup"><span data-stu-id="048e6-135">The input to the splitter is a series of media buffers that contain the entire or fragments of the Data Object.</span></span> <span data-ttu-id="048e6-136">分隔器的輸出是一系列包含封包資料的媒體範例。</span><span class="sxs-lookup"><span data-stu-id="048e6-136">The output from the splitter is a series of media samples that contain the packet data.</span></span>

<span data-ttu-id="048e6-137">若要將輸入資料傳遞給分隔器，請建立媒體緩衝區，並使用 ASF 檔案的資料物件區段中的資料填入該緩衝區。</span><span class="sxs-lookup"><span data-stu-id="048e6-137">To pass input data to the splitter, create a media buffer and fill it with data from the Data Object section of the ASF file.</span></span> <span data-ttu-id="048e6-138"> (如需媒體緩衝區的詳細資訊，請參閱 [媒體緩衝區](media-buffers.md)。 ) 然後將媒體緩衝區傳遞給 [**IMFASFSplitter：:P arsedata**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata) 方法。</span><span class="sxs-lookup"><span data-stu-id="048e6-138">(For more information about media buffers, see [Media Buffers](media-buffers.md).) Then, pass the media buffer to the [**IMFASFSplitter::ParseData**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata) method.</span></span> <span data-ttu-id="048e6-139">您也可以指定：</span><span class="sxs-lookup"><span data-stu-id="048e6-139">You can also specify:</span></span>

-   <span data-ttu-id="048e6-140">緩衝區中分隔器應開始剖析的位移。</span><span class="sxs-lookup"><span data-stu-id="048e6-140">The offset into the buffer where the splitter should start parsing.</span></span> <span data-ttu-id="048e6-141">如果位移為零，則會從緩衝區開頭開始剖析。</span><span class="sxs-lookup"><span data-stu-id="048e6-141">If the offset is zero, parsing begins at the start of the buffer.</span></span> <span data-ttu-id="048e6-142">如需設定資料位移的詳細資訊，請參閱本主題中的「尋找資料位移」一節。</span><span class="sxs-lookup"><span data-stu-id="048e6-142">For information about setting the data offset, see the "Finding the Data Offset" section in this topic.</span></span>
-   <span data-ttu-id="048e6-143">要剖析的資料量。</span><span class="sxs-lookup"><span data-stu-id="048e6-143">The amount of data to parse.</span></span> <span data-ttu-id="048e6-144">如果這個值為零，則分隔器會剖析，直到到達緩衝區的結尾，如 [**IMFMediaBuffer：： GetCurrentLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-getcurrentlength) 方法所指定。</span><span class="sxs-lookup"><span data-stu-id="048e6-144">If this value is zero, the splitter parses until it reaches the end of the buffer, as specified by the [**IMFMediaBuffer::GetCurrentLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-getcurrentlength) method.</span></span>

<span data-ttu-id="048e6-145">分隔器會藉由參考媒體緩衝區中的資料來產生媒體範例。</span><span class="sxs-lookup"><span data-stu-id="048e6-145">The splitter generates media samples by referencing the data in the media buffers.</span></span> <span data-ttu-id="048e6-146">用戶端可以藉由在迴圈中呼叫 [**IMFASFSplitter：： GetNextSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getnextsample) 來取出輸出範例，直到沒有其他資料可剖析為止。</span><span class="sxs-lookup"><span data-stu-id="048e6-146">The client can retrieve the output samples by calling [**IMFASFSplitter::GetNextSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getnextsample) in a loop until there is no more data to parse.</span></span> <span data-ttu-id="048e6-147">如果 **GetNextSample** \_ \_ 在 *pdwStatusFlags* 參數中傳回 ASF STATUSFLAGS 不完整旗標，則表示有更多要抓取的範例，而且應用程式可以再次呼叫 **GetNextSample** 。</span><span class="sxs-lookup"><span data-stu-id="048e6-147">If **GetNextSample** returns the ASF\_STATUSFLAGS\_INCOMPLETE flag in the *pdwStatusFlags* parameter, it means there are more samples to retrieve, and the application can call **GetNextSample** again.</span></span> <span data-ttu-id="048e6-148">否則，呼叫 **ParseData** 以將更多資料傳遞給分隔器。</span><span class="sxs-lookup"><span data-stu-id="048e6-148">Otherwise, call **ParseData** to pass more data to the splitter.</span></span> <span data-ttu-id="048e6-149">針對產生的範例，分隔器會設定下列資訊：</span><span class="sxs-lookup"><span data-stu-id="048e6-149">For the generated samples, the splitter sets the following information:</span></span>

-   <span data-ttu-id="048e6-150">分割器會針對它所產生的所有樣本設定時間戳記。</span><span class="sxs-lookup"><span data-stu-id="048e6-150">The splitter sets a time stamp on all the samples that it generates.</span></span> <span data-ttu-id="048e6-151">取樣時間代表表示時間，不包括預先執行的時間。</span><span class="sxs-lookup"><span data-stu-id="048e6-151">The sample time represents the presentation time and does not include the preroll time.</span></span> <span data-ttu-id="048e6-152">應用程式可以呼叫 [**IMFSample：： GetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampletime) 來取得呈現時間，以 100-毫微秒單位表示。</span><span class="sxs-lookup"><span data-stu-id="048e6-152">The application can call [**IMFSample::GetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampletime) to get the presentation time, in 100-nanosecond units.</span></span>
-   <span data-ttu-id="048e6-153">如果在產生範例期間發生中斷，則分隔器會在不連續的第一個範例上設定 [**MFSampleExtension \_**](mfsampleextension-discontinuity-attribute.md) 中斷屬性。</span><span class="sxs-lookup"><span data-stu-id="048e6-153">If a break occurs during sample generation, the splitter sets the [**MFSampleExtension\_Discontinuity**](mfsampleextension-discontinuity-attribute.md) attribute on the first sample after the discontinuity.</span></span> <span data-ttu-id="048e6-154">不連續通常是因為網路連線上的封包、損毀的檔案資料或分隔器切換到另一個來來源資料流所造成。</span><span class="sxs-lookup"><span data-stu-id="048e6-154">Discontinuities are usually caused by dropped packets on a network connection, corrupt file data, or the splitter switching from one source stream to another.</span></span>
-   <span data-ttu-id="048e6-155">針對影片，分隔器會檢查範例是否包含主要畫面格。</span><span class="sxs-lookup"><span data-stu-id="048e6-155">For video, the splitter checks whether the sample contains a key frame.</span></span> <span data-ttu-id="048e6-156">如果有的話，分隔器會在範例上設定 [**MFSampleExtension \_ CleanPoint**](mfsampleextension-cleanpoint-attribute.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="048e6-156">If it does, the splitter sets the [**MFSampleExtension\_CleanPoint**](mfsampleextension-cleanpoint-attribute.md) attribute on the sample.</span></span>

<span data-ttu-id="048e6-157">如果分隔器正在剖析從媒體伺服器接收的資料封包，封包長度可能是可變的。</span><span class="sxs-lookup"><span data-stu-id="048e6-157">If the splitter is parsing data packets that are received from a media server, it is possible that the packet length is variable.</span></span> <span data-ttu-id="048e6-158">在此情況下，用戶端必須針對每個封包呼叫 **ParseData** ，並在傳送到分隔器的每個緩衝區上設定 MFASFSPLITTER 的封 [**\_ 包 \_ 界限**](mfasfsplitter-packet-boundary-attribute.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="048e6-158">In this case, the client must call **ParseData** for each packet and set the [**MFASFSPLITTER\_PACKET\_BOUNDARY**](mfasfsplitter-packet-boundary-attribute.md) attribute on each buffer that is sent to the splitter.</span></span> <span data-ttu-id="048e6-159">這個屬性會向分隔器指出媒體緩衝區是否包含 ASF 封包的開頭。</span><span class="sxs-lookup"><span data-stu-id="048e6-159">This attribute indicates to the splitter whether the media buffer contains the start of an ASF packet.</span></span> <span data-ttu-id="048e6-160">如果緩衝區包含新封包的開頭，請將屬性設定為 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="048e6-160">Set the attribute to **TRUE** if the buffer contains the start of a new packet.</span></span> <span data-ttu-id="048e6-161">如果緩衝區包含前一個封包的接續，請將屬性設定為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="048e6-161">If the buffer contains a continuation of the previous packet, set the attribute to **FALSE**.</span></span> <span data-ttu-id="048e6-162">緩衝區無法跨越多個封包。</span><span class="sxs-lookup"><span data-stu-id="048e6-162">The buffers cannot span multiple packets.</span></span>

<span data-ttu-id="048e6-163">將新的媒體緩衝區傳遞給分隔器之前，應用程式必須呼叫 [**IMFASFSplitter：： Flush**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-flush)。</span><span class="sxs-lookup"><span data-stu-id="048e6-163">Before passing new media buffers to the splitter, the application must call [**IMFASFSplitter::Flush**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-flush).</span></span> <span data-ttu-id="048e6-164">這個方法會重設分割器，並清除等候完成的任何部分框架。</span><span class="sxs-lookup"><span data-stu-id="048e6-164">This method resets the splitter and clears any partial frame that is waiting to be completed.</span></span> <span data-ttu-id="048e6-165">這在搜尋案例中很有用，因為該案例的位移位於不同的位置。</span><span class="sxs-lookup"><span data-stu-id="048e6-165">This is useful in a seeking scenario where the offset is at a different location.</span></span>

### <a name="example"></a><span data-ttu-id="048e6-166">範例</span><span class="sxs-lookup"><span data-stu-id="048e6-166">Example</span></span>

<span data-ttu-id="048e6-167">下列程式碼範例顯示如何剖析資料封包。</span><span class="sxs-lookup"><span data-stu-id="048e6-167">The following code example shows how to parse data packets.</span></span> <span data-ttu-id="048e6-168">此範例會從資料物件的開頭到資料流程的結尾進行剖析，並顯示包含主要畫面格之範例的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="048e6-168">This example parses from the beginning of the Data Object to the end of the stream and displays information about the samples that contain key frames.</span></span> <span data-ttu-id="048e6-169">如需使用此程式碼的完整範例，請參閱 [教學課程：讀取 ASF](tutorial--reading-an-asf-file.md)檔。</span><span class="sxs-lookup"><span data-stu-id="048e6-169">For a complete example that uses this code, see [Tutorial: Reading an ASF File](tutorial--reading-an-asf-file.md).</span></span>


```C++
// Parse the video stream and display information about the video samples.
//
// The current read position of the byte stream must be at the start of the ASF
// Data Object.

HRESULT DisplayKeyFrames(IMFByteStream *pStream, IMFASFSplitter *pSplitter)
{
    const DWORD cbReadSize = 2048;  // Read size (arbitrary value)

    IMFMediaBuffer *pBuffer = NULL;
    IMFSample *pSample = NULL;

    HRESULT hr = S_OK;
    while (SUCCEEDED(hr))
    {
        // The parser must get a newly allocated buffer each time.
        hr = MFCreateMemoryBuffer(cbReadSize, &pBuffer);
        if (FAILED(hr))
        {
            break;
        }

        // Read data into the buffer.
        hr = ReadFromByteStream(pStream, pBuffer, cbReadSize);
        if (FAILED(hr)) 
        {
            break; 
        }

        // Get the amound of data that was read.
        DWORD cbData;
        hr = pBuffer->GetCurrentLength(&cbData);
        if (FAILED(hr)) 
        { 
            break; 
        }

        if (cbData == 0)
        {
            break; // End of file.
        }

        // Send the data to the ASF splitter.
        hr = pSplitter->ParseData(pBuffer, 0, 0);
        SafeRelease(&pBuffer);
        if (FAILED(hr)) 
        { 
            break; 
        }

        // Pull samples from the splitter.
        DWORD parsingStatus = 0;
        do
        {
            WORD streamID;
            hr = pSplitter->GetNextSample(&parsingStatus, &streamID, &pSample);
            if (FAILED(hr)) 
            { 
                break; 
            }
            if (pSample == NULL)
            {
                // No samples yet. Parse more data.
                break;
            }
            if (IsRandomAccessPoint(pSample))
            {
                DisplayKeyFrame(pSample);
            }
            SafeRelease(&pSample);
            
        } while (parsingStatus & ASF_STATUSFLAGS_INCOMPLETE);
    }
    SafeRelease(&pSample);
    SafeRelease(&pBuffer);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="048e6-170">相關主題</span><span class="sxs-lookup"><span data-stu-id="048e6-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="048e6-171">ASF 分隔器</span><span class="sxs-lookup"><span data-stu-id="048e6-171">ASF Splitter</span></span>](asf-splitter.md)
</dt> </dl>

 

 




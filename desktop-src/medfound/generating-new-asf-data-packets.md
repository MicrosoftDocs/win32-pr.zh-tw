---
description: 產生新的 ASF 資料封包
ms.assetid: 7afa9694-c965-40e2-8549-e32ff48def2a
title: 產生新的 ASF 資料封包
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78f3432ecf34c58247a1533adb202b75f59d770c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468621"
---
# <a name="generating-new-asf-data-packets"></a><span data-ttu-id="027a1-103">產生新的 ASF 資料封包</span><span class="sxs-lookup"><span data-stu-id="027a1-103">Generating New ASF Data Packets</span></span>

<span data-ttu-id="027a1-104">ASF 多工器是 *一種 WMContainer* 層元件，可與 [ASF 資料物件](asf-file-structure.md) 搭配使用，並讓應用程式能夠針對符合 ContentInfo 物件中所定義之需求的資料流程產生 ASF 資料封包。</span><span class="sxs-lookup"><span data-stu-id="027a1-104">The ASF *multiplexer* is a WMContainer layer component that works with the [ASF Data Object](asf-file-structure.md) and gives an application the ability to generate ASF data packets for a stream that match the requirements defined in the ContentInfo object.</span></span>

<span data-ttu-id="027a1-105">多工器有一個輸入和一個輸出。</span><span class="sxs-lookup"><span data-stu-id="027a1-105">The multiplexer has one input and one output.</span></span> <span data-ttu-id="027a1-106">它會接收包含數位媒體資料的串流範例，並產生一或多個可寫入至 ASF 容器的資料封包。</span><span class="sxs-lookup"><span data-stu-id="027a1-106">It receives a stream sample that contains digital media data and produces one or more data packet that can be written to an ASF container.</span></span>

<span data-ttu-id="027a1-107">下列清單摘要說明產生 ASF 資料封包的流程：</span><span class="sxs-lookup"><span data-stu-id="027a1-107">The following list summarizes the process of generating ASF data packets:</span></span>

1.  <span data-ttu-id="027a1-108">將輸入資料傳遞給 IMFASFMultiplexer 中的多 [**任務器：:P rocesssample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample)。</span><span class="sxs-lookup"><span data-stu-id="027a1-108">Pass input data to the multiplexer in [**IMFASFMultiplexer::ProcessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample).</span></span>
2.  <span data-ttu-id="027a1-109">藉由在迴圈中呼叫 [**IMFASFMultiplexer：： GetNextPacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket) 來收集資料封包，直到所有完成的封包都已取出為止。</span><span class="sxs-lookup"><span data-stu-id="027a1-109">Collect the data packets by calling [**IMFASFMultiplexer::GetNextPacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket) in a loop until all the complete packets have been retrieved.</span></span>
3.  <span data-ttu-id="027a1-110">將輸入資料轉換成完整的封包之後，多工器中可能會有一些暫止的資料，但 [**GetNextPacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket)並不會加以取出。</span><span class="sxs-lookup"><span data-stu-id="027a1-110">After the input data has been converted into complete packets there might be some pending data in the multiplexer, which was not retrieved by [**GetNextPacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket).</span></span> <span data-ttu-id="027a1-111">呼叫 [**IMFASFMultiplexer：： Flush**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-flush) 以 packetize 暫止的範例，並再次呼叫 **GetNextPacket** ，以從多工器收集這些樣本。</span><span class="sxs-lookup"><span data-stu-id="027a1-111">Call [**IMFASFMultiplexer::Flush**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-flush) to packetize the pending samples and collect them from the multiplexer by calling **GetNextPacket** again.</span></span>
4.  <span data-ttu-id="027a1-112">藉由呼叫 [**IMFASFMultiplexer：： End**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-end) 以反映多工器在產生資料封包期間所做的變更，來更新相關聯的 ASF 標頭物件。</span><span class="sxs-lookup"><span data-stu-id="027a1-112">Update the associated ASF Header Objects by calling [**IMFASFMultiplexer::End**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-end) to reflect changes made by the multiplexer during data packet generation.</span></span>

<span data-ttu-id="027a1-113">下圖說明透過多工器對 ASF 檔案產生的資料封包。</span><span class="sxs-lookup"><span data-stu-id="027a1-113">The following diagram illustrates data packet generation for an ASF file through the multiplexer.</span></span>

![顯示 asf 檔案之資料封包產生的圖表](images/packet.gif)

## <a name="asf-data-packet-creation"></a><span data-ttu-id="027a1-115">建立 ASF 資料封包</span><span class="sxs-lookup"><span data-stu-id="027a1-115">ASF Data Packet Creation</span></span>

<span data-ttu-id="027a1-116">建立並初始化多工器（如建立多工器 [物件](creating-the-multiplexer-object.md)中所述）之後，請呼叫 [**IMFASFMultiplexer：:P rocesssample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample) ，將輸入資料傳遞給多工器，以處理資料封包。</span><span class="sxs-lookup"><span data-stu-id="027a1-116">After creating and initializing the multiplexer as described in [Creating the Multiplexer Object](creating-the-multiplexer-object.md), call [**IMFASFMultiplexer::ProcessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample) to pass input data to the multiplexer for processing into data packets.</span></span> <span data-ttu-id="027a1-117">指定的輸入必須位於媒體範例 ([**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) 介面) 可以有一或多個媒體緩衝區 ([**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) 介面) 包含資料流程的資料。</span><span class="sxs-lookup"><span data-stu-id="027a1-117">The specified input must be in a media sample ([**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface) that can have one or more media buffers ([**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) interface) containing the data for a stream.</span></span> <span data-ttu-id="027a1-118">在 ASF 到 ASF 轉碼的情況下，可以從建立 packetized 資料流程範例的分隔器產生輸入媒體範例。</span><span class="sxs-lookup"><span data-stu-id="027a1-118">In case of ASF-to-ASF transcoding, the input media sample can be generated from the splitter that creates packetized stream samples.</span></span> <span data-ttu-id="027a1-119">如需詳細資訊，請參閱 [ASF 分隔器](asf-splitter.md)。</span><span class="sxs-lookup"><span data-stu-id="027a1-119">For more information, see [ASF Splitter](asf-splitter.md).</span></span>

<span data-ttu-id="027a1-120">在呼叫 [**ProcessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample)之前，請確定輸入媒體範例的時間戳記是有效的呈現時間;否則 **ProcessSample** 會失敗，並傳回 MF \_ E \_ NO \_ 範例 \_ 時間戳記程式碼。</span><span class="sxs-lookup"><span data-stu-id="027a1-120">Before calling [**ProcessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample), make sure that the time stamp of the input media sample is a valid presentation time; otherwise **ProcessSample** fails and returns the MF\_E\_NO\_SAMPLE\_TIMESTAMP code.</span></span>

<span data-ttu-id="027a1-121">多工器可以透過 [**ProcessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample)，以壓縮或未壓縮的媒體範例形式接受輸入。</span><span class="sxs-lookup"><span data-stu-id="027a1-121">The multiplexer can accept input as compressed or uncompressed media samples through [**ProcessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample).</span></span> <span data-ttu-id="027a1-122">多工器會根據資料流程的頻寬使用量，將傳送時間指派給這些範例。</span><span class="sxs-lookup"><span data-stu-id="027a1-122">The multiplexer assigns send times to these samples depending on the bandwidth usage of the stream.</span></span> <span data-ttu-id="027a1-123">在這個過程中，多工器會檢查有漏洞值區參數 (的位元速率和緩衝區視窗使用率) ，而且可以拒絕不遵守這些值的範例。</span><span class="sxs-lookup"><span data-stu-id="027a1-123">During this process, the multiplexer checks the leaky bucket parameters (bit rate and buffer window utilization) and can reject samples that do not adhere to those values.</span></span> <span data-ttu-id="027a1-124">輸入媒體範例可能會因為下列其中一個原因而導致頻寬檢查失敗：</span><span class="sxs-lookup"><span data-stu-id="027a1-124">The input media sample can fail the bandwidth check for either of the following reasons:</span></span>

-   <span data-ttu-id="027a1-125">如果輸入媒體範例晚抵達，因為最後指派的傳送時間大於此媒體範例的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="027a1-125">If the input media sample arrived late because the last-assigned send time is greater than the time stamp on this media sample.</span></span> <span data-ttu-id="027a1-126">[**ProcessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample) 失敗並傳回 **MF \_ E \_ 晚期 \_ 範例** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="027a1-126">[**ProcessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample) fails and returns the **MF\_E\_LATE\_SAMPLE** error code.</span></span>
-   <span data-ttu-id="027a1-127">如果輸入媒體範例上的時間戳記早于指派的傳送時間 (這表示) 緩衝區溢位。</span><span class="sxs-lookup"><span data-stu-id="027a1-127">If the time stamp on the input media sample is earlier than the assigned send time (this indicates buffer overflow).</span></span> <span data-ttu-id="027a1-128">如果多工器已設定為在多工器初始化期間設定 MFASF 多工器 **\_ \_ AUTOADJUST \_ 位元速率** 旗標來調整位元速率，則可以忽略這種情況。</span><span class="sxs-lookup"><span data-stu-id="027a1-128">The multiplexer can ignore this situation if it is configured to adjust the bit rate by setting the **MFASF\_MULTIPLEXER\_AUTOADJUST\_BITRATE** flag during multiplexer initialization.</span></span> <span data-ttu-id="027a1-129">如需詳細資訊，請參閱建立多工器 [物件](creating-the-multiplexer-object.md)中的「多工器初始化和有漏洞 Bucket 設定」。</span><span class="sxs-lookup"><span data-stu-id="027a1-129">For more information, see "Multiplexer Initialization and Leaky Bucket Settings" in [Creating the Multiplexer Object](creating-the-multiplexer-object.md).</span></span> <span data-ttu-id="027a1-130">如果未設定此旗標，而多工器遇到頻寬溢出， [**ProcessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample) 就會失敗，並傳回 **MF \_ E \_ 頻寬 \_ 溢出** 的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="027a1-130">If this flag is not set and the multiplexer encounters bandwidth overrun, [**ProcessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample) fails and returns the **MF\_E\_BANDWIDTH\_OVERRUN** error code.</span></span>

<span data-ttu-id="027a1-131">在多工器指派傳送時間之後，輸入媒體範例會新增至 [ *傳送] 視窗*，也就是輸入媒體範例的清單，依傳送時間和準備處理到資料封包。</span><span class="sxs-lookup"><span data-stu-id="027a1-131">After the multiplexer assigns the send time, the input media sample is added to the *send window*—a list of input media samples ordered by send times and ready to be processed into data packets.</span></span> <span data-ttu-id="027a1-132">在資料封包結構期間，會剖析輸入媒體範例，並將相關的資料寫入資料封包作為承載。</span><span class="sxs-lookup"><span data-stu-id="027a1-132">During data packet construction, the input media sample is parsed and relevant data is written to a data packet as payload.</span></span> <span data-ttu-id="027a1-133">完整的資料封包可包含一或多個輸入媒體範例中的資料。</span><span class="sxs-lookup"><span data-stu-id="027a1-133">A complete data packet can contain data from one or more input media samples.</span></span>

<span data-ttu-id="027a1-134">當新的輸入媒體範例抵達傳送視窗時，會將它們新增至佇列，直到有足夠的媒體樣本可形成一個完整的封包。</span><span class="sxs-lookup"><span data-stu-id="027a1-134">When new input media samples arrive in the send window, they are added to a queue until there are enough media samples to form one complete packet.</span></span> <span data-ttu-id="027a1-135">輸入媒體範例所包含媒體緩衝區中的資料不會複製到產生的資料封包。</span><span class="sxs-lookup"><span data-stu-id="027a1-135">The data in media buffers contained by the input media sample are not copied to the generated data packet.</span></span> <span data-ttu-id="027a1-136">資料封包會保存輸入媒體緩衝區的參考，直到已完全 packetized 輸入媒體範例，並從多工器收集完整的封包為止。</span><span class="sxs-lookup"><span data-stu-id="027a1-136">The data packet hold references to the input media buffers until the input media sample has been fully packetized and the complete packet have been collected from the multiplexer.</span></span>

<span data-ttu-id="027a1-137">當有完整的資料封包可用時，可以藉由呼叫 [**IMFASFMultiplexer：： GetNextPacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket)來加以取出。</span><span class="sxs-lookup"><span data-stu-id="027a1-137">When a complete data packet is available, it can be retrieved by calling [**IMFASFMultiplexer::GetNextPacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket).</span></span> <span data-ttu-id="027a1-138">如果您在完成封包準備進行抓取時呼叫 [**ProcessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample) ，它會失敗並傳回 **MF \_ E \_ NOTACCEPTING** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="027a1-138">If you call [**ProcessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample) while there are complete packets ready for retrieval, it fails and returns the **MF\_E\_NOTACCEPTING** error code.</span></span> <span data-ttu-id="027a1-139">這表示多工器無法接受更多輸入，您必須呼叫 **GetNextPacket** 來取出等候中的封包。</span><span class="sxs-lookup"><span data-stu-id="027a1-139">This indicates that the multiplexer cannot accept more input and you must call **GetNextPacket** to retrieve the waiting packets.</span></span> <span data-ttu-id="027a1-140">在理想的情況下，每個 **ProcessSample** 呼叫後面應該接著一或多個 **GetNextPacket** 呼叫，以取得完整的資料封包。</span><span class="sxs-lookup"><span data-stu-id="027a1-140">Ideally, every **ProcessSample** call should be followed by one or more **GetNextPacket** calls to get the complete data packets.</span></span> <span data-ttu-id="027a1-141">它可能需要一個以上的輸入媒體範例來建立完整的資料封包。</span><span class="sxs-lookup"><span data-stu-id="027a1-141">It may take more than one input media sample to create a complete data packet.</span></span> <span data-ttu-id="027a1-142">相反地，一個輸入媒體範例中的資料可能會跨越多個封包。</span><span class="sxs-lookup"><span data-stu-id="027a1-142">Conversely, data in one input media sample might span multiple packets.</span></span> <span data-ttu-id="027a1-143">因此，並非所有對 **ProcessSample** 的呼叫都會產生輸出媒體範例。</span><span class="sxs-lookup"><span data-stu-id="027a1-143">Therefore, not all calls to **ProcessSample** will yield output media samples.</span></span>

<span data-ttu-id="027a1-144">如果輸入媒體範例包含由 [**MFSampleExtension \_ CleanPoint**](mfsampleextension-cleanpoint-attribute.md) 屬性工作表示的主要畫面格，則多工器會將屬性複製到封包。</span><span class="sxs-lookup"><span data-stu-id="027a1-144">If the input media sample contains a key frame indicated by the [**MFSampleExtension\_CleanPoint**](mfsampleextension-cleanpoint-attribute.md) attribute, the multiplexer copies the attribute to the packet.</span></span>

## <a name="getting-asf-data-packets"></a><span data-ttu-id="027a1-145">取得 ASF 資料封包</span><span class="sxs-lookup"><span data-stu-id="027a1-145">Getting ASF Data Packets</span></span>

<span data-ttu-id="027a1-146">若要收集多工器所產生之完整資料封包的輸出媒體範例，請在迴圈中呼叫 [**IMFASFMultiplexer：： GetNextPacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket) ，直到沒有其他輸出媒體樣本剩下的封包。</span><span class="sxs-lookup"><span data-stu-id="027a1-146">To collect the output media samples for a complete data packet generated by the multiplexer, call [**IMFASFMultiplexer::GetNextPacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket) in a loop until there are no more output media samples left for the packet.</span></span> <span data-ttu-id="027a1-147">以下列出成功案例：</span><span class="sxs-lookup"><span data-stu-id="027a1-147">The following lists the success cases:</span></span>

-   <span data-ttu-id="027a1-148">如果有完整的資料封包可用， [**GetNextPacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket)會在 *pdwStatusFlags* 參數中收到「 **ASF \_ 狀態 \_ 旗標 \_ 不完整**」旗標; *ppIPacket* 參數會接收第一個資料封包的指標。</span><span class="sxs-lookup"><span data-stu-id="027a1-148">If there is a complete data packet available, [**GetNextPacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket) receives the **ASF\_STATUS\_FLAGS\_INCOMPLETE** flag in the *pdwStatusFlags* parameter; the *ppIPacket* parameter receives a pointer to the first data packet.</span></span> <span data-ttu-id="027a1-149">只要收到此旗標，您就必須呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="027a1-149">You must call this method as long it receives this flag.</span></span> <span data-ttu-id="027a1-150">在每個反復專案中， *ppIPacket* 會指向佇列中的下一個封包。</span><span class="sxs-lookup"><span data-stu-id="027a1-150">With every iteration, *ppIPacket* points to the next packet in the queue.</span></span>
-   <span data-ttu-id="027a1-151">如果只有一個資料封包， *ppIPacket* 會指向它，而 *pdwStatusFlags* 中不會收到 [ **ASF \_ 狀態 \_ 旗標未 \_ 完成**] 旗標。</span><span class="sxs-lookup"><span data-stu-id="027a1-151">If there is only one data packet, *ppIPacket* points to it and the **ASF\_STATUS\_FLAGS\_INCOMPLETE** flag is not received in *pdwStatusFlags*.</span></span>
-   <span data-ttu-id="027a1-152">如果多工器仍在 packetizing 和新增資料封包的過程中， [**GetNextPacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket)可能會成功，而不會產生任何資料封包。</span><span class="sxs-lookup"><span data-stu-id="027a1-152">[**GetNextPacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket) can succeed without yielding any data packets if the multiplexer is still in the process of packetizing and adding data packets.</span></span> <span data-ttu-id="027a1-153">在此情況下， *ppIPacket* 會指向 **Null**。</span><span class="sxs-lookup"><span data-stu-id="027a1-153">In this case, *ppIPacket* points to **NULL**.</span></span> <span data-ttu-id="027a1-154">若要繼續，您必須藉由呼叫 [**ProcessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample)，提供多工器的輸入媒體範例。</span><span class="sxs-lookup"><span data-stu-id="027a1-154">To proceed, you must provide the multiplexer with more input media samples by calling [**ProcessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample).</span></span>

<span data-ttu-id="027a1-155">下列範例程式碼顯示使用多工器產生資料封包的函式。</span><span class="sxs-lookup"><span data-stu-id="027a1-155">The following example code shows a function that generates data packets by using the multiplexer.</span></span> <span data-ttu-id="027a1-156">產生的資料封包內容將會寫入至呼叫端所配置的資料位元組資料流程中。</span><span class="sxs-lookup"><span data-stu-id="027a1-156">The generated data packet contents will be written to the data byte stream allocated by the caller.</span></span>


```C++
//-------------------------------------------------------------------
// GenerateASFDataPackets
// 
// Gets data packets from the mux. This function is called after 
// calling IMFASFMultiplexer::ProcessSample. 
//-------------------------------------------------------------------

HRESULT GenerateASFDataPackets( 
    IMFASFMultiplexer *pMux, 
    IMFByteStream *pDataStream
    )
{
    HRESULT hr = S_OK;

    IMFSample *pOutputSample = NULL;
    IMFMediaBuffer *pDataPacketBuffer = NULL;

    DWORD dwMuxStatus = ASF_STATUSFLAGS_INCOMPLETE;

    while (dwMuxStatus & ASF_STATUSFLAGS_INCOMPLETE)
    {
        hr = pMux->GetNextPacket(&dwMuxStatus, &pOutputSample);

        if (FAILED(hr))
        {
            break;
        }

        if (pOutputSample)
        {
            //Convert to contiguous buffer
            hr = pOutputSample->ConvertToContiguousBuffer(&pDataPacketBuffer);
            
            if (FAILED(hr))
            {
                break;
            }

            //Write buffer to byte stream
            hr = WriteBufferToByteStream(pDataStream, pDataPacketBuffer, NULL);

            if (FAILED(hr))
            {
                break;
            }
        }

        SafeRelease(&pDataPacketBuffer);
        SafeRelease(&pOutputSample);
    }

    SafeRelease(&pOutputSample);
    SafeRelease(&pDataPacketBuffer);
    return hr;
}
```



<span data-ttu-id="027a1-157">此函式 `WriteBufferToByteStream` 會顯示在 [**IMFByteStream：： Write**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-write)主題中。</span><span class="sxs-lookup"><span data-stu-id="027a1-157">The `WriteBufferToByteStream` function is shown in the topic [**IMFByteStream::Write**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-write).</span></span>

<span data-ttu-id="027a1-158">若要查看使用此程式碼範例的完整應用程式，請參閱 [教學課程：將 ASF 資料流程從一個檔案複製到另](tutorial--copying-asf-streams-from-one-file-to-another.md)一個檔案。</span><span class="sxs-lookup"><span data-stu-id="027a1-158">To see a complete application that uses this code example, see [Tutorial: Copying ASF Streams from One File to Another](tutorial--copying-asf-streams-from-one-file-to-another.md).</span></span>

## <a name="post-packet-generation-calls"></a><span data-ttu-id="027a1-159">Post Packet-Generation 呼叫</span><span class="sxs-lookup"><span data-stu-id="027a1-159">Post Packet-Generation Calls</span></span>

<span data-ttu-id="027a1-160">若要確定沒有任何完整的資料封包正在等候多工器，請呼叫 [**IMFASFMultiplexer：： Flush**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-flush)。</span><span class="sxs-lookup"><span data-stu-id="027a1-160">To make sure that there are no complete data packets waiting in the multiplexer, call [**IMFASFMultiplexer::Flush**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-flush).</span></span> <span data-ttu-id="027a1-161">這會強制多工器 packetize 正在進行中的所有媒體範例。</span><span class="sxs-lookup"><span data-stu-id="027a1-161">This forces the multiplexer to packetize all the media samples that are in progress.</span></span> <span data-ttu-id="027a1-162">應用程式可以透過 **GetNextPacket** 在迴圈中以媒體範例的形式收集這些封包，直到沒有其他要抓取的封包為止。</span><span class="sxs-lookup"><span data-stu-id="027a1-162">The application can collect these packets in form of media samples through **GetNextPacket** in a loop until there are no more packets left to be retrieved.</span></span>

<span data-ttu-id="027a1-163">產生所有媒體範例之後，請呼叫 [**IMFASFMultiplexer：： End**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-end) 以更新與這些資料封包相關聯的 ASF 標頭物件。</span><span class="sxs-lookup"><span data-stu-id="027a1-163">After all the media samples are generated, call [**IMFASFMultiplexer::End**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-end) to update the ASF Header Object that is associated with these data packets.</span></span> <span data-ttu-id="027a1-164">標頭物件是藉由傳遞用來初始化多工器的 ContentInfo 物件來指定。</span><span class="sxs-lookup"><span data-stu-id="027a1-164">The Header Object is specified by passing the ContentInfo object that was used to initialize the multiplexer.</span></span> <span data-ttu-id="027a1-165">此呼叫會更新不同的標頭物件，以反映在資料封包產生期間由多工器所做的變更。</span><span class="sxs-lookup"><span data-stu-id="027a1-165">This call updates various Header Objects to reflect changes made by the multiplexer during data packet generation.</span></span> <span data-ttu-id="027a1-166">這項資訊包括封包計數、傳送持續時間、播放持續時間，以及所有資料流程的串流號碼。</span><span class="sxs-lookup"><span data-stu-id="027a1-166">This information includes packet count, send duration, play duration, and stream numbers of all the streams.</span></span> <span data-ttu-id="027a1-167">整體的標頭大小也會更新。</span><span class="sxs-lookup"><span data-stu-id="027a1-167">The overall header size is also updated.</span></span>

<span data-ttu-id="027a1-168">您必須確保在抓取所有資料封包之後呼叫 [**End**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-end) 。</span><span class="sxs-lookup"><span data-stu-id="027a1-168">You must ensure that [**End**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-end) is called after all the data packets have been retrieved.</span></span> <span data-ttu-id="027a1-169">如果有任何封包在多工器中等候， **End** 將會失敗，並傳回 **MF \_ E \_ FLUSH \_ 需要** 的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="027a1-169">If there are any packets waiting in the multiplexer, **End** will fail and return the **MF\_E\_FLUSH\_NEEDED** error code.</span></span> <span data-ttu-id="027a1-170">在此情況下，請在迴圈中呼叫 [**Flush**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-flush) 和 [**GetNextPacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket) ，以取得等候封包。</span><span class="sxs-lookup"><span data-stu-id="027a1-170">In this case, get the waiting packet by calling [**Flush**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-flush) and [**GetNextPacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket) in a loop.</span></span>

> [!Note]  
> <span data-ttu-id="027a1-171">針對 VBR 編碼，在呼叫 **End** 之後，您必須在 ContentInfo 物件的編碼屬性中設定編碼統計資料。</span><span class="sxs-lookup"><span data-stu-id="027a1-171">For VBR encoding, after calling **End**, you must set the encoding statistics in the ContentInfo object's encoding properties.</span></span> <span data-ttu-id="027a1-172">如需此程式的詳細資訊，請參閱在 [ContentInfo 物件中設定屬性](setting-properties-in-the-contentinfo-object.md)（property）中的「使用編碼器設定來設定 ContentInfo 物件」。</span><span class="sxs-lookup"><span data-stu-id="027a1-172">For information about this process, see "Configuring the ContentInfo Object with Encoder Settings" in [Setting Properties in the ContentInfo Object](setting-properties-in-the-contentinfo-object.md).</span></span> <span data-ttu-id="027a1-173">下列清單顯示要設定的特定屬性：</span><span class="sxs-lookup"><span data-stu-id="027a1-173">The following list shows the specific properties to set:</span></span>
>
> -   <span data-ttu-id="027a1-174">[**MFPKEY \_RAVG**](mfpkey-ravgproperty.md) 是 VBR 內容的平均位元速率。</span><span class="sxs-lookup"><span data-stu-id="027a1-174">[**MFPKEY\_RAVG**](mfpkey-ravgproperty.md) is the average bit rate of the VBR content.</span></span>
> -   <span data-ttu-id="027a1-175">[**MFPKEY \_BAVG**](mfpkey-bavgproperty.md) 是平均位元速率的緩衝區視窗。</span><span class="sxs-lookup"><span data-stu-id="027a1-175">[**MFPKEY\_BAVG**](mfpkey-bavgproperty.md) is the buffer window for the average bit rate.</span></span>
> -   <span data-ttu-id="027a1-176">[**MFPKEY \_RMAX**](mfpkey-rmaxproperty.md) 是 VBR 內容的尖峰位元速率。</span><span class="sxs-lookup"><span data-stu-id="027a1-176">[**MFPKEY\_RMAX**](mfpkey-rmaxproperty.md) is the peak bit rate of the VBR content.</span></span>
> -   <span data-ttu-id="027a1-177">[**MFPKEY \_BMAX**](mfpkey-bmaxproperty.md) 是尖峰緩衝區視窗。</span><span class="sxs-lookup"><span data-stu-id="027a1-177">[**MFPKEY\_BMAX**](mfpkey-bmaxproperty.md) is the peak buffer window.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="027a1-178">相關主題</span><span class="sxs-lookup"><span data-stu-id="027a1-178">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="027a1-179">ASF 多工器</span><span class="sxs-lookup"><span data-stu-id="027a1-179">ASF Multiplexer</span></span>](asf-multiplexer.md)
</dt> <dt>

[<span data-ttu-id="027a1-180">教學課程：將 ASF 資料流程從一個檔案複製到另一個檔案</span><span class="sxs-lookup"><span data-stu-id="027a1-180">Tutorial: Copying ASF Streams from One File to Another</span></span>](tutorial--copying-asf-streams-from-one-file-to-another.md)
</dt> <dt>

[<span data-ttu-id="027a1-181">教學課程：使用 CBR 編碼方式撰寫 WMA 檔案</span><span class="sxs-lookup"><span data-stu-id="027a1-181">Tutorial: Writing a WMA File by Using CBR Encoding</span></span>](tutorial--writing-a-wma-file-by-using-cbr-encoding.md)
</dt> </dl>

 

 




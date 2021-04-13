---
title: 使用協力廠商編解碼器建立 ASF 檔案
description: 使用協力廠商編解碼器建立 ASF 檔案
ms.assetid: 5cd348ca-1f86-429d-92ee-4eab4ced8571
keywords:
- Windows Media Format SDK，建立 ASF 檔案
- Windows Media Format SDK，協力廠商編解碼器
- Advanced Systems Format (ASF) ，建立檔案
- ASF (Advanced Systems Format) ，建立檔案
- Advanced Systems Format (ASF) ，協力廠商編解碼器
- ASF (Advanced Systems Format) ，協力廠商編解碼器
- 協力廠商編解碼器
- 編解碼器，協力廠商
- 編解碼器，建立 ASF 檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d6c057f1785ed50e328ac6094ff7dbe078e98fc
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2020
ms.locfileid: "104314505"
---
# <a name="to-create-asf-files-using-third-party-codecs"></a><span data-ttu-id="b3924-112">使用協力廠商編解碼器建立 ASF 檔案</span><span class="sxs-lookup"><span data-stu-id="b3924-112">To Create ASF Files Using Third-Party Codecs</span></span>

<span data-ttu-id="b3924-113">您可以使用 Windows Media Format SDK 來建立 ASF 檔案，其中包含以您選擇的任何編解碼器編碼的數位媒體。</span><span class="sxs-lookup"><span data-stu-id="b3924-113">You can use the Windows Media Format SDK to create ASF files that contain digital media encoded with any codec you choose.</span></span> <span data-ttu-id="b3924-114">使用此 SDK 隨附的編解碼器時，您必須執行下列步驟。</span><span class="sxs-lookup"><span data-stu-id="b3924-114">When using a codec other than one included with this SDK, you must perform the following steps.</span></span>

1.  <span data-ttu-id="b3924-115">使用所需的編解碼器將內容編碼。</span><span class="sxs-lookup"><span data-stu-id="b3924-115">Encode the content with the desired codec.</span></span>
2.  <span data-ttu-id="b3924-116">尋找或建立 GUID 值，以識別使用步驟1中所用編解碼器編碼的內容。</span><span class="sxs-lookup"><span data-stu-id="b3924-116">Find or create a GUID value to identify content encoded with the codec used in step 1.</span></span>
3.  <span data-ttu-id="b3924-117">建立新的設定檔，或修改現有的設定檔以搭配編碼的內容使用。</span><span class="sxs-lookup"><span data-stu-id="b3924-117">Create a new profile, or modify an existing profile for use with the encoded content.</span></span>
    -   <span data-ttu-id="b3924-118">使用適當的主要類型建立編碼內容的資料流程。</span><span class="sxs-lookup"><span data-stu-id="b3924-118">Create a stream for the encoded content with the appropriate major type.</span></span> <span data-ttu-id="b3924-119">如需主要媒體類型的詳細資訊，請參閱 [媒體類型](media-types.md)。</span><span class="sxs-lookup"><span data-stu-id="b3924-119">For more information about major media types, see [Media Types](media-types.md).</span></span> <span data-ttu-id="b3924-120">使用步驟2中識別的 GUID 作為媒體子類型。</span><span class="sxs-lookup"><span data-stu-id="b3924-120">Use the GUID identified in step 2 as the media subtype.</span></span>
    -   <span data-ttu-id="b3924-121">將資料流程的位元速率和緩衝區視窗設定為不會產生緩衝區溢位的值。</span><span class="sxs-lookup"><span data-stu-id="b3924-121">Set the bit rate and buffer window for the stream to values that will not result in buffer overflow.</span></span> <span data-ttu-id="b3924-122">編碼時，您應該能夠從編解碼器取得這些值。</span><span class="sxs-lookup"><span data-stu-id="b3924-122">You should be able to obtain these values from the codec at the time of encoding.</span></span> <span data-ttu-id="b3924-123">SDK 執行時間元件會檢查位元速率/緩衝區視窗值，並視需要卸載範例，以使指定的資料符合這些值。</span><span class="sxs-lookup"><span data-stu-id="b3924-123">The SDK runtime components check the bitrate/buffer window values and drop samples if necessary to make the given data fit in with these values.</span></span> <span data-ttu-id="b3924-124">如果您不正確地設定這些值，檔案將無法正確地進行串流，因而導致播放不良。</span><span class="sxs-lookup"><span data-stu-id="b3924-124">If you set the values incorrectly, the file will not stream properly, resulting in poor playback.</span></span>
    -   <span data-ttu-id="b3924-125">針對影片資料流程，您必須將 [**WMVIDEOINFOHEADER**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader)結構中所包含之 **BITMAPINFOHEADER** 結構的 **biCompression** 成員設定為內容的適當 FOURCC 值。</span><span class="sxs-lookup"><span data-stu-id="b3924-125">For video streams, you must set the **biCompression** member of the **BITMAPINFOHEADER** structure contained in the [**WMVIDEOINFOHEADER**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader) structure to the appropriate FOURCC value for the content.</span></span> <span data-ttu-id="b3924-126">此值必須等於子類型 GUID 的前四個位元組。</span><span class="sxs-lookup"><span data-stu-id="b3924-126">This value must be equal to the first four bytes of the subtype GUID.</span></span> <span data-ttu-id="b3924-127">例如，如果 **biCompression** 是 MAKEFOURCC ( t '、' E '、'，t ' ) = 0x54455354，則子類型 GUID 的開頭會像這樣： 54455354-xxxx。</span><span class="sxs-lookup"><span data-stu-id="b3924-127">For example, if **biCompression** is MAKEFOURCC('T','E','S','T')=0x54455354, then the subtype GUID will begin like this: 54455354-XXXX-XXXX-XXXX-XXXXXXXXXXXX.</span></span>
4.  <span data-ttu-id="b3924-128">建立寫入器物件，並載入在上一個步驟中建立的設定檔。</span><span class="sxs-lookup"><span data-stu-id="b3924-128">Create a writer object and load the profile created in the previous step.</span></span> <span data-ttu-id="b3924-129">如需寫入檔案的詳細資訊，請參閱 [寫入 ASF](writing-asf-files.md)檔。</span><span class="sxs-lookup"><span data-stu-id="b3924-129">For more information about writing files, see [Writing ASF Files](writing-asf-files.md).</span></span>
5.  <span data-ttu-id="b3924-130">在檔案的輸入之間執行迴圈，並為每個檔案指派輸入屬性。</span><span class="sxs-lookup"><span data-stu-id="b3924-130">Loop through the inputs of the file and assign input properties for each as you normally would.</span></span> <span data-ttu-id="b3924-131">如需輸入的詳細資訊，請參閱 [使用輸入](working-with-inputs.md)。</span><span class="sxs-lookup"><span data-stu-id="b3924-131">For more information about inputs, see [Working with Inputs](working-with-inputs.md).</span></span> <span data-ttu-id="b3924-132">若為使用協力廠商編解碼器編碼的資料流程，請在呼叫 [**IWMWriter：： BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting)之前，將 [**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops)介面指標設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="b3924-132">For the stream encoded with a third-party codec, set the [**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) interface pointer to **NULL** before calling [**IWMWriter::BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).</span></span>
6.  <span data-ttu-id="b3924-133">使用在上一個步驟中建立的新設定檔來寫入檔案。</span><span class="sxs-lookup"><span data-stu-id="b3924-133">Use the new profile created in the previous step to write the file.</span></span> <span data-ttu-id="b3924-134">使用 [**IWMWriterAdvanced：： WriteStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-writestreamsample) 傳遞壓縮的範例，而不是 [**IWMWriter：： WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample)。</span><span class="sxs-lookup"><span data-stu-id="b3924-134">Pass the compressed samples using [**IWMWriterAdvanced::WriteStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-writestreamsample) instead of [**IWMWriter::WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample).</span></span> <span data-ttu-id="b3924-135">針對影片，您必須將 WM \_ SF \_ CLEANPOINT 傳遞為 *dwFlags* 參數，以指定哪些範例是主要畫面格。</span><span class="sxs-lookup"><span data-stu-id="b3924-135">For video, you must specify which samples are key frames by passing WM\_SF\_CLEANPOINT as the *dwFlags* parameter.</span></span>

<span data-ttu-id="b3924-136">若要處理和解壓縮以協力廠商編解碼器編碼的資料流程，您必須閱讀壓縮的資料流程範例。</span><span class="sxs-lookup"><span data-stu-id="b3924-136">To process and decompress the stream encoded with a third-party codec, you must read compressed stream samples.</span></span> <span data-ttu-id="b3924-137">您的讀取應用程式也必須處理資料流程的解壓縮範例。</span><span class="sxs-lookup"><span data-stu-id="b3924-137">Your reading application must handle sample decompression for the stream as well.</span></span>

## <a name="putting-mpeg-2-streams-into-asf"></a><span data-ttu-id="b3924-138">將 MPEG 2 串流放入 ASF</span><span class="sxs-lookup"><span data-stu-id="b3924-138">Putting MPEG-2 streams into ASF</span></span>

> [!Note]  
> <span data-ttu-id="b3924-139">本主題適用于使用 Windows Media Format SDK 的應用程式，可將使用 B 框架) 的 MPEG-2 (或其他壓縮格式放入 ASF 檔案容器中。</span><span class="sxs-lookup"><span data-stu-id="b3924-139">This topic applies to applications that use the Windows Media Format SDK to put MPEG-2 (or other compression formats that use B frames) into the ASF file container.</span></span>

 

<span data-ttu-id="b3924-140">寫入器物件要求所有輸入範例都必須有時間戳記，並假設每個輸入範例的呈現時間晚于其之前的呈現時間。</span><span class="sxs-lookup"><span data-stu-id="b3924-140">The writer object requires that all input samples have time stamps, and it assumes that each input sample has a presentation time later than the one that preceded it.</span></span> <span data-ttu-id="b3924-141">雖然幾乎所有未壓縮的影片，甚至某些壓縮的影片串流都符合這些條件，但 MPEG-2 資料流程並不會。</span><span class="sxs-lookup"><span data-stu-id="b3924-141">While virtually all uncompressed video and even some compressed video streams meet these conditions, MPEG-2 streams do not.</span></span> <span data-ttu-id="b3924-142">在 MPEG 2 中，並非所有樣本都有時間戳記，而當 B 框架存在時，範例解碼順序與轉譯順序不同。</span><span class="sxs-lookup"><span data-stu-id="b3924-142">In MPEG-2, not all samples are time stamped, and when B frames are present, the sample decoding order is not the same as the rendering order.</span></span> <span data-ttu-id="b3924-143">當寫入器物件遇到無法排序的範例時，它會將它們重新排列成「正確」的順序。</span><span class="sxs-lookup"><span data-stu-id="b3924-143">When the writer object encounters out-of-order samples, it rearranges them into the "correct" order.</span></span> <span data-ttu-id="b3924-144">因此，若要將 MPEG-2 資料流程原生 (未解碼) 在 ASF 容器中，您必須執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="b3924-144">Therefore, to store MPEG-2 streams natively (not decoded) in an ASF container, you must perform the following steps:</span></span>

<span data-ttu-id="b3924-145">寫入檔案時：</span><span class="sxs-lookup"><span data-stu-id="b3924-145">When writing the file:</span></span>

1.  <span data-ttu-id="b3924-146">將固定大小的資料單位延伸 () 至每個輸入範例，此範例會保存包含範例之實際 MPEG 時間戳記開始時間和停止時間值的結構。</span><span class="sxs-lookup"><span data-stu-id="b3924-146">Add a fixed-size data unit extension (DUE) to each input sample that will hold a structure that contains the actual MPEG time-stamp start-time and stop-time values for the sample.</span></span> <span data-ttu-id="b3924-147">如果樣本沒有時間戳記，請針對這些值使用-1。</span><span class="sxs-lookup"><span data-stu-id="b3924-147">Use -1 for these values if the sample has no time stamp.</span></span>
2.  <span data-ttu-id="b3924-148">提供寫入器物件「虛設」輸入時間戳記，一律會不斷增加，以便將範例以完全相同的順序寫入至檔案。</span><span class="sxs-lookup"><span data-stu-id="b3924-148">Give the writer object "dummy" input time stamps that are always increasing so that it will write the samples to the file in exactly the same order as they are received.</span></span> <span data-ttu-id="b3924-149">虛擬時間戳記應該大約對應到實際的呈現時間，如一段時間的平均值。</span><span class="sxs-lookup"><span data-stu-id="b3924-149">The dummy time stamps should correspond approximately to the actual presentation times, as averaged over time.</span></span> <span data-ttu-id="b3924-150">虛擬時間戳記會形成搜尋時間軸，因此，如果它們相對於即時戳記，則搜尋檔案上的作業將會產生非預期的結果。</span><span class="sxs-lookup"><span data-stu-id="b3924-150">The dummy time stamps will form the seeking timeline, so if they diverge relative to the real time stamps, seek operations on the file will produce unexpected results.</span></span> <span data-ttu-id="b3924-151">不過，取樣時間之間的抖動量不會嚴重影響搜尋作業。</span><span class="sxs-lookup"><span data-stu-id="b3924-151">However, a limited amount of jitter between the sample times will not seriously affect seek operations.</span></span>

<span data-ttu-id="b3924-152">讀取檔案時：</span><span class="sxs-lookup"><span data-stu-id="b3924-152">When reading the file:</span></span>

-   <span data-ttu-id="b3924-153">針對從檔案讀取的每個範例，檢查是否已到期。</span><span class="sxs-lookup"><span data-stu-id="b3924-153">For each sample read from the file, examine the DUE.</span></span> <span data-ttu-id="b3924-154">如果它包含大於或等於零的開始時間，請將該值複製到輸出範例的時間戳記，然後再傳遞給解碼器。</span><span class="sxs-lookup"><span data-stu-id="b3924-154">If it contains a start time that is greater than or equal to zero, copy that value to the time stamp for the output sample before it is delivered to the decoder.</span></span> <span data-ttu-id="b3924-155">將輸出範例上的所有其他時間戳記設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="b3924-155">Set all other time stamps on the output samples to **NULL**.</span></span> <span data-ttu-id="b3924-156">在 DirectShow 中，藉由呼叫 **IMediaSample：： SetTime** (**null**，**null**) 來完成這項操作。</span><span class="sxs-lookup"><span data-stu-id="b3924-156">In DirectShow, this is done by calling **IMediaSample::SetTime**(**NULL**,**NULL**).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b3924-157">相關主題</span><span class="sxs-lookup"><span data-stu-id="b3924-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b3924-158">**緩衝處理內容**</span><span class="sxs-lookup"><span data-stu-id="b3924-158">**Buffering Content**</span></span>](buffering-content.md)
</dt> <dt>

[<span data-ttu-id="b3924-159">**IWMWriter 介面**</span><span class="sxs-lookup"><span data-stu-id="b3924-159">**IWMWriter Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[<span data-ttu-id="b3924-160">**IWMWriterAdvanced 介面**</span><span class="sxs-lookup"><span data-stu-id="b3924-160">**IWMWriterAdvanced Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)
</dt> <dt>

[<span data-ttu-id="b3924-161">**使用非同步讀取器傳遞壓縮的範例**</span><span class="sxs-lookup"><span data-stu-id="b3924-161">**To Deliver Compressed Samples with the Asynchronous Reader**</span></span>](to-deliver-compressed-samples-with-the-asynchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="b3924-162">**使用同步讀取器取出資料流程範例**</span><span class="sxs-lookup"><span data-stu-id="b3924-162">**To Retrieve Stream Samples with the Synchronous Reader**</span></span>](to-retrieve-stream-samples-with-the-synchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="b3924-163">**WMVIDEOINFOHEADER**</span><span class="sxs-lookup"><span data-stu-id="b3924-163">**WMVIDEOINFOHEADER**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader)
</dt> <dt>

[<span data-ttu-id="b3924-164">**使用設定檔**</span><span class="sxs-lookup"><span data-stu-id="b3924-164">**Working with Profiles**</span></span>](working-with-profiles.md)
</dt> <dt>

[<span data-ttu-id="b3924-165">**寫入 ASF 檔案**</span><span class="sxs-lookup"><span data-stu-id="b3924-165">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 





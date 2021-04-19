---
title: 範例擴充功能類型
description: 範例擴充功能類型
ms.assetid: 8de2e003-cb21-4be9-bcde-7f5909b6260a
keywords:
- Windows Media 格式 SDK，範例延伸模組
- Advanced Systems Format (ASF) 、範例延伸模組
- ASF (Advanced Systems Format) ，範例延伸模組
- Windows Media Format SDK，資料單位延伸模組
- Advanced Systems Format (ASF) 、資料單位延伸模組
- ASF (Advanced Systems Format) 、資料單位延伸模組
- Windows Media Format SDK，緩衝區屬性
- Advanced Systems Format (ASF) ，buffer 屬性
- ASF (Advanced Systems Format) ，buffer 屬性
- 範例延伸模組，類型
- 資料單位延伸模組，類型
- 緩衝區屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 972e3da1ecaad277158bb270cc358436f53db9e2
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/11/2020
ms.locfileid: "106996161"
---
# <a name="sample-extension-types"></a><span data-ttu-id="f83cd-115">範例擴充功能類型</span><span class="sxs-lookup"><span data-stu-id="f83cd-115">Sample Extension Types</span></span>

<span data-ttu-id="f83cd-116">範例延伸模組（也稱為資料單位延伸 () 或緩衝區屬性）是附加至 ASF 檔案之 data 區段中媒體範例的資料項目目。</span><span class="sxs-lookup"><span data-stu-id="f83cd-116">Sample extensions, also called data unit extensions (DUEs) or buffer properties, are items of data that are attached to the media samples in the data section of the ASF file.</span></span> <span data-ttu-id="f83cd-117">Windows Media 格式 SDK 中定義了數種類型的範例延伸模組。</span><span class="sxs-lookup"><span data-stu-id="f83cd-117">Several types of sample extensions are defined in the Windows Media Format SDK.</span></span> <span data-ttu-id="f83cd-118">您也可以建立自己的延伸模組類型。</span><span class="sxs-lookup"><span data-stu-id="f83cd-118">You can also create your own extension types.</span></span>

<span data-ttu-id="f83cd-119">若要使用範例延伸模組，您必須在設定檔的串流設定資料中識別延伸模組類型。</span><span class="sxs-lookup"><span data-stu-id="f83cd-119">To use sample extensions, you must identify the extension type in the stream configuration data of the profile.</span></span> <span data-ttu-id="f83cd-120">呼叫 [**IWMStreamConfig2：： AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) 方法，將資料流程設定為接受擴充資料的範例。</span><span class="sxs-lookup"><span data-stu-id="f83cd-120">Call the [**IWMStreamConfig2::AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) method to configure a stream to accept samples with extended data.</span></span>

<span data-ttu-id="f83cd-121">您必須藉由呼叫 [**INSSBuffer3：： SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) 方法，將個別範例延伸模組新增至輸入範例。</span><span class="sxs-lookup"><span data-stu-id="f83cd-121">Individual sample extensions must be added to the input samples by calling the [**INSSBuffer3::SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) method.</span></span> <span data-ttu-id="f83cd-122">讀取範例時，您可以呼叫 [**INSSBuffer3：： GetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-getproperty) 方法來取得延伸模組資料。</span><span class="sxs-lookup"><span data-stu-id="f83cd-122">When reading samples, you can call the [**INSSBuffer3::GetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-getproperty) method to retrieve the extension data.</span></span> <span data-ttu-id="f83cd-123">您也可以使用 [**INSSBuffer4**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer4) 介面的方法來列舉附加至範例的資料單位延伸模組。</span><span class="sxs-lookup"><span data-stu-id="f83cd-123">You can also use the methods of the [**INSSBuffer4**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer4) interface to enumerate the data unit extensions attached to a sample.</span></span>

<span data-ttu-id="f83cd-124">下表列出預先定義的資料單位延伸模組識別碼，並說明附加至每個的範例的資料。</span><span class="sxs-lookup"><span data-stu-id="f83cd-124">The following table lists the predefined data unit extension identifiers, and describes the data that is attached to samples for each.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f83cd-125">範例延伸模組 GUID</span><span class="sxs-lookup"><span data-stu-id="f83cd-125">Sample extension GUID</span></span></th>
<th><span data-ttu-id="f83cd-126">Description</span><span class="sxs-lookup"><span data-stu-id="f83cd-126">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f83cd-127">WM_SampleExtensionGUID_OutputCleanPoint</span><span class="sxs-lookup"><span data-stu-id="f83cd-127">WM_SampleExtensionGUID_OutputCleanPoint</span></span></td>
<td><span data-ttu-id="f83cd-128">資料會指出此範例是否為 <a href="wmformat-glossary.md"><em>cleanpoint</em></a>。</span><span class="sxs-lookup"><span data-stu-id="f83cd-128">The data indicates whether the sample is a <a href="wmformat-glossary.md"><em>cleanpoint</em></a>.</span></span> <span data-ttu-id="f83cd-129">值為零表示此範例不是 cleanpoint。</span><span class="sxs-lookup"><span data-stu-id="f83cd-129">A value of zero indicates that the sample is not a cleanpoint.</span></span> <span data-ttu-id="f83cd-130">非零值表示它是 cleanpoint。</span><span class="sxs-lookup"><span data-stu-id="f83cd-130">A non-zero value indicates that it is a cleanpoint.</span></span> <span data-ttu-id="f83cd-131">此範例資料單位延伸 (的) 類型是在撰寫以協力廠商編解碼器編碼的 precompressed 媒體資料流程時，用來追蹤 cleanpoints。</span><span class="sxs-lookup"><span data-stu-id="f83cd-131">This sample data unit extension (DUE) type is used to keep track of cleanpoints when writing precompressed media streams that were encoded with third-party codecs.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f83cd-132">WM_SampleExtensionGUID_Timecode</span><span class="sxs-lookup"><span data-stu-id="f83cd-132">WM_SampleExtensionGUID_Timecode</span></span></td>
<td><span data-ttu-id="f83cd-133">資料是 <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data"><strong>WMT_TIMECODE_EXTENSION_DATA</strong></a> 結構，其中包含與範例相關聯的 SMPTE 時間代碼資料。這項應付的大小一律是 WM_SampleExtension_Timecode_Size，也就是14個位元組。</span><span class="sxs-lookup"><span data-stu-id="f83cd-133">The data is a <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data"><strong>WMT_TIMECODE_EXTENSION_DATA</strong></a> structure containing SMPTE time code data associated with the sample.The size for this DUE is always WM_SampleExtension_Timecode_Size, which is 14 bytes.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f83cd-134">WM_SampleExtensionGUID_FileName</span><span class="sxs-lookup"><span data-stu-id="f83cd-134">WM_SampleExtensionGUID_FileName</span></span></td>
<td><span data-ttu-id="f83cd-135">這種類型的範例延伸模組用於檔案資料流程。</span><span class="sxs-lookup"><span data-stu-id="f83cd-135">This type of sample extension is used for file streams.</span></span> <span data-ttu-id="f83cd-136">檔案資料流程範例中的資料是資料檔案的片段。</span><span class="sxs-lookup"><span data-stu-id="f83cd-136">The data in a file stream sample is a piece of a data file.</span></span> <span data-ttu-id="f83cd-137">範例延伸模組中的資料會指定從中取得範例內容的檔案名。檔案名是寬字元字串，其中包含副檔名格式的檔案名，而不含任何路徑資訊。</span><span class="sxs-lookup"><span data-stu-id="f83cd-137">The data in the sample extension specifies the name of the file from which the content in the sample was taken.The file name is a wide-character string containing the file name in name.extension format without any path information.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f83cd-138">WM_SampleExtensionGUID_ContentType</span><span class="sxs-lookup"><span data-stu-id="f83cd-138">WM_SampleExtensionGUID_ContentType</span></span></td>
<td><span data-ttu-id="f83cd-139">資料會識別此範例所包含的內容類型。</span><span class="sxs-lookup"><span data-stu-id="f83cd-139">The data identifies the type of content that the sample contains.</span></span> <span data-ttu-id="f83cd-140">這種類型的範例延伸模組可搭配交錯式影片串流使用。所有交錯內容都使用 WM_CT_INTERLACED 旗標，並以位 <strong>or</strong> 結合 WM_CT_BOTTOM_FIELD_FIRST、WM_CT_TOP_FIELD_FIRST 或 WM_CT_REPEAT_FIRST_FIELD。</span><span class="sxs-lookup"><span data-stu-id="f83cd-140">This type of sample extension is used with interlaced video streams.All interlaced content uses the WM_CT_INTERLACED flag combined by a bitwise <strong>OR</strong> with either WM_CT_BOTTOM_FIELD_FIRST, WM_CT_TOP_FIELD_FIRST, or WM_CT_REPEAT_FIRST_FIELD.</span></span><br/> <span data-ttu-id="f83cd-141">在編碼過程中不會使用欄位順序，但會使用壓縮的範例進行維護，以便將其傳遞至轉譯硬體。</span><span class="sxs-lookup"><span data-stu-id="f83cd-141">The field order is not used in the encoding process, but is maintained with the compressed samples so that it can be passed to the rendering hardware.</span></span> <span data-ttu-id="f83cd-142">使用不正確的欄位順序來播放交錯式內容，會在影片中引進運動抖動等成品。</span><span class="sxs-lookup"><span data-stu-id="f83cd-142">Playing interlaced content with the incorrect field order introduces artifacts such as motion jitter in the video.</span></span><br/> <span data-ttu-id="f83cd-143">這項應付的大小一律是 WM_SampleExtension_ContentType_Size。</span><span class="sxs-lookup"><span data-stu-id="f83cd-143">The size for this DUE is always WM_SampleExtension_ContentType_Size.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f83cd-144">WM_SampleExtensionGUID_PixelAspectRatio</span><span class="sxs-lookup"><span data-stu-id="f83cd-144">WM_SampleExtensionGUID_PixelAspectRatio</span></span></td>
<td><span data-ttu-id="f83cd-145">資料會指出範例中內容的圖元外觀比例。</span><span class="sxs-lookup"><span data-stu-id="f83cd-145">The data indicates the pixel aspect ratio of the content in the sample.</span></span> <span data-ttu-id="f83cd-146">這只適用于影片。此延伸模組類型是用來識別非正方形圖元的長寬比。</span><span class="sxs-lookup"><span data-stu-id="f83cd-146">This applies only to video.This extension type is used to identify the aspect ratio of non-square pixels.</span></span> <span data-ttu-id="f83cd-147">如需詳細資訊，請參閱 <a href="to-read-and-write-video-streams-with-non-square-pixels.md">以非正方形圖元讀取和寫入影片串流</a>。</span><span class="sxs-lookup"><span data-stu-id="f83cd-147">For more information, see <a href="to-read-and-write-video-streams-with-non-square-pixels.md">To Read and Write Video Streams with Non-Square Pixels</a>.</span></span><br/> <span data-ttu-id="f83cd-148">外觀比例值會儲存為位元組下限的單字，而其最大的位元組是 Y 的外觀。</span><span class="sxs-lookup"><span data-stu-id="f83cd-148">Aspect ratio values are stored as a word whose low byte is the X aspect and whose high byte is the Y aspect.</span></span> <span data-ttu-id="f83cd-149">例如，16:9 會儲存為0x0910。</span><span class="sxs-lookup"><span data-stu-id="f83cd-149">For example, 16:9 is stored as 0x0910.</span></span><br/> <span data-ttu-id="f83cd-150">這項應付的大小一律是 WM_SampleExtension_PixelAspectRatio_Size，也就是2個位元組。</span><span class="sxs-lookup"><span data-stu-id="f83cd-150">The size for this DUE is always WM_SampleExtension_PixelAspectRatio_Size, which is 2 bytes.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f83cd-151">WM_SampleExtensionGUID_SampleDuration</span><span class="sxs-lookup"><span data-stu-id="f83cd-151">WM_SampleExtensionGUID_SampleDuration</span></span></td>
<td><span data-ttu-id="f83cd-152">資料表示緩衝區物件中所含樣本的持續時間（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="f83cd-152">The data indicates the duration, in milliseconds, of the sample contained in the buffer object.</span></span> <span data-ttu-id="f83cd-153">在播放時，如果已設定此項，讀取器物件將會使用它來覆寫現有的範例持續時間值。這是因為影片資料流程上的 SDK 執行時間元件會自動設定此項，其位元速率為 100 kbps 或更高，而到期資訊的額外負荷並不重要。</span><span class="sxs-lookup"><span data-stu-id="f83cd-153">On playback, if this DUE is set the reader object will use it to overwrite the existing sample duration value.This DUE is set automatically by the SDK run-time components on video streams with bit rates of 100 kbps or greater, where the overhead of the DUE information is not significant.</span></span> <span data-ttu-id="f83cd-154">它不會針對速率低於 100 kbps 的資料流程進行設定。</span><span class="sxs-lookup"><span data-stu-id="f83cd-154">It is not set for streams with bit rates under 100 kbps.</span></span> <span data-ttu-id="f83cd-155">應用程式不應手動設定，因為高位速率資料流程上的寫入器 () 將會以自己的資料覆寫該值。</span><span class="sxs-lookup"><span data-stu-id="f83cd-155">Applications should not set this DUE manually because the writer (on high-bit-rate streams) will overwrite the value with its own data.</span></span><br/> <span data-ttu-id="f83cd-156">這項應付的大小一律是 WM_SampleExtension_SampleDuration_Size，也就是2個位元組。</span><span class="sxs-lookup"><span data-stu-id="f83cd-156">The size for this DUE is always WM_SampleExtension_SampleDuration_Size, which is 2 bytes.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f83cd-157">WM_SampleExtensionGUID_ChromaLocation</span><span class="sxs-lookup"><span data-stu-id="f83cd-157">WM_SampleExtensionGUID_ChromaLocation</span></span></td>
<td><span data-ttu-id="f83cd-158">資料表示 I420 影片格式所使用的色度次取樣類型。此延伸模組的值會設定為下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="f83cd-158">The data indicates the type of chroma subsampling used in the I420 video format.The value of this extension is set to one of the follow values:</span></span><br/>
<ul>
<li><span data-ttu-id="f83cd-159">WM_CL_INTERLACED420</span><span class="sxs-lookup"><span data-stu-id="f83cd-159">WM_CL_INTERLACED420</span></span></li>
<li><span data-ttu-id="f83cd-160">WM_CL_PROGRESSIVE420</span><span class="sxs-lookup"><span data-stu-id="f83cd-160">WM_CL_PROGRESSIVE420</span></span></li>
</ul>
<span data-ttu-id="f83cd-161">設定檔中未設定此資料單位延伸模組。</span><span class="sxs-lookup"><span data-stu-id="f83cd-161">This data unit extension is not configured in the profile.</span></span> <span data-ttu-id="f83cd-162">它包含在來自解碼器的範例輸出中。</span><span class="sxs-lookup"><span data-stu-id="f83cd-162">It is included in samples output from the decoder.</span></span><br/> <span data-ttu-id="f83cd-163">這項應付的大小一律是 WM_SampleExtension_ChromaLocation_Size，也就是1個位元組。</span><span class="sxs-lookup"><span data-stu-id="f83cd-163">The size of this DUE is always WM_SampleExtension_ChromaLocation_Size, which is 1 byte.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f83cd-164">WM_SampleExtensionGUID_ColorSpaceInfo</span><span class="sxs-lookup"><span data-stu-id="f83cd-164">WM_SampleExtensionGUID_ColorSpaceInfo</span></span></td>
<td><span data-ttu-id="f83cd-165">資料會提供用於目前影片框架之色彩空間的相關資訊。此延伸模組的值是 <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmt_colorspaceinfo_extension_data"><strong>WMT_COLORSPACEINFO_EXTENSION_DATA</strong></a> 結構。</span><span class="sxs-lookup"><span data-stu-id="f83cd-165">The data provides information about the color space used for the current video frame.The value of this extension is a <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmt_colorspaceinfo_extension_data"><strong>WMT_COLORSPACEINFO_EXTENSION_DATA</strong></a> structure.</span></span><br/> <span data-ttu-id="f83cd-166">設定檔中未設定此資料單位延伸模組。</span><span class="sxs-lookup"><span data-stu-id="f83cd-166">This data unit extension is not configured in the profile.</span></span> <span data-ttu-id="f83cd-167">它包含在來自解碼器的範例輸出中。</span><span class="sxs-lookup"><span data-stu-id="f83cd-167">It is included in samples output from the decoder.</span></span><br/> <span data-ttu-id="f83cd-168">這項應付的大小一律是 WM_SampleExtension_ColorSpaceInfo_Size，也就是3個位元組。</span><span class="sxs-lookup"><span data-stu-id="f83cd-168">The size of this DUE is always WM_SampleExtension_ColorSpaceInfo_Size, which is 3 bytes.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f83cd-169">WM_SampleExtensionGUID_UserDataInfo</span><span class="sxs-lookup"><span data-stu-id="f83cd-169">WM_SampleExtensionGUID_UserDataInfo</span></span></td>
<td><span data-ttu-id="f83cd-170">資料是自訂的使用者資料。資料的前四個位元組包含自訂資料的大小。</span><span class="sxs-lookup"><span data-stu-id="f83cd-170">The data is custom user data.The first four bytes of the data contain the size of the custom data.</span></span><br/> <span data-ttu-id="f83cd-171">下一個位元組包含範例延伸模組中提供的使用者資料類型。</span><span class="sxs-lookup"><span data-stu-id="f83cd-171">The next byte contains the type of user data provided in the sample extension.</span></span> <span data-ttu-id="f83cd-172">支援下列類型：</span><span class="sxs-lookup"><span data-stu-id="f83cd-172">The following types are supported:</span></span><br/>
<ul>
<li><span data-ttu-id="f83cd-173">0x1F-序列層級使用者資料</span><span class="sxs-lookup"><span data-stu-id="f83cd-173">0x1F - Sequence level user data</span></span></li>
<li><span data-ttu-id="f83cd-174">0x1E-進入點層級使用者資料</span><span class="sxs-lookup"><span data-stu-id="f83cd-174">0x1E - Entry-point level user data</span></span></li>
<li><span data-ttu-id="f83cd-175">Bugcheck 0x1d-框架層級使用者資料</span><span class="sxs-lookup"><span data-stu-id="f83cd-175">0x1D - Frame level user data</span></span></li>
<li><span data-ttu-id="f83cd-176">0x1C-欄位層級使用者資料</span><span class="sxs-lookup"><span data-stu-id="f83cd-176">0x1C - Field level user data</span></span></li>
<li><span data-ttu-id="f83cd-177">0x1B 配量層級使用者資料</span><span class="sxs-lookup"><span data-stu-id="f83cd-177">0x1B - Slice level user data</span></span></li>
</ul>
<span data-ttu-id="f83cd-178">第六個和後續的位元組包含使用者資料。</span><span class="sxs-lookup"><span data-stu-id="f83cd-178">The sixth and subsequent bytes contain the user data.</span></span> <span data-ttu-id="f83cd-179">前四個位元組中的數位所指定的使用者資料有許多位元組。</span><span class="sxs-lookup"><span data-stu-id="f83cd-179">There are as many bytes of user data as specified by the number in the first four bytes.</span></span><br/> <span data-ttu-id="f83cd-180">設定檔中未設定此資料單位延伸模組。</span><span class="sxs-lookup"><span data-stu-id="f83cd-180">This data unit extension is not configured in the profile.</span></span> <span data-ttu-id="f83cd-181">它包含在從解碼器輸出的範例中。</span><span class="sxs-lookup"><span data-stu-id="f83cd-181">It is included in samples that are output from the decoder.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f83cd-182">WM_SampleExtensionGUID_SampleProtectionSalt</span><span class="sxs-lookup"><span data-stu-id="f83cd-182">WM_SampleExtensionGUID_SampleProtectionSalt</span></span></td>
<td><span data-ttu-id="f83cd-183">資料會以範例加密。</span><span class="sxs-lookup"><span data-stu-id="f83cd-183">The data is encrypted by sample.</span></span> <span data-ttu-id="f83cd-184">此範例延伸模組類型用於從非 ASF 檔案格式匯入的內容，以及 Windows Media DRM 以外的版權保護設定。匯入受保護的內容時，每個範例都必須包含唯一的 salt。</span><span class="sxs-lookup"><span data-stu-id="f83cd-184">This sample extension type is used for content that is imported from a non-ASF file format and a rights protection scheme other than Windows Media DRM.When importing protected content, each sample must include a unique salt.</span></span> <span data-ttu-id="f83cd-185">此值通常是單純增加的計數器。</span><span class="sxs-lookup"><span data-stu-id="f83cd-185">Typically, this value is a monotonically increasing counter.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="f83cd-186">相關主題</span><span class="sxs-lookup"><span data-stu-id="f83cd-186">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f83cd-187">**程式設計參考**</span><span class="sxs-lookup"><span data-stu-id="f83cd-187">**Programming Reference**</span></span>](programming-reference.md)
</dt> </dl>

 

 






---
title: 關於 IMediaObject
description: 關於 IMediaObject
ms.assetid: c483f74a-efd8-4a9f-a719-686099755e63
keywords:
- Windows Media Player 外掛程式，介面
- 外掛程式，介面
- 數位信號處理外掛程式，介面
- DSP 外掛程式，介面
- 介面、DSP 外掛程式
- Windows Media Player 外掛程式、IMediaObject 介面
- 外掛程式，IMediaObject 介面
- 數位信號處理外掛程式，IMediaObject 介面
- DSP 外掛程式，IMediaObject 介面
- IMediaObject 介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfbbecd749242b67bc5c8f36b3c7a2c0a5fbe461
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671564"
---
# <a name="about-imediaobject"></a><span data-ttu-id="8dc0a-113">關於 IMediaObject</span><span class="sxs-lookup"><span data-stu-id="8dc0a-113">About IMediaObject</span></span>

<span data-ttu-id="8dc0a-114">**IMediaObject** 介面是 DMOs 所需的介面。</span><span class="sxs-lookup"><span data-stu-id="8dc0a-114">The **IMediaObject** interface is the required interface for DMOs.</span></span> <span data-ttu-id="8dc0a-115">**IMediaObject** 包含 WINDOWS MEDIA PLAYER 的 DSP 外掛程式用來從 Windows Media Player 取得資料、處理資料，以及將已處理的資料傳回 Windows Media Player 的方法。</span><span class="sxs-lookup"><span data-stu-id="8dc0a-115">**IMediaObject** contains the methods that a Windows Media Player DSP plug-in uses to get data from Windows Media Player, to process the data, and to return the processed data to Windows Media Player.</span></span> <span data-ttu-id="8dc0a-116">如需 **IMediaObject** 介面的完整檔，請參閱 Windows SDK 的 [DirectShow] 區段。</span><span class="sxs-lookup"><span data-stu-id="8dc0a-116">For complete documentation of the **IMediaObject** interface, see the DirectShow section of the Windows SDK.</span></span>

<span data-ttu-id="8dc0a-117">**IMediaObject** 的方法可分類如下：</span><span class="sxs-lookup"><span data-stu-id="8dc0a-117">The methods of **IMediaObject** can be categorized as follows:</span></span>

## <a name="methods-that-handle-format-negotiation"></a><span data-ttu-id="8dc0a-118">處理格式協調的方法</span><span class="sxs-lookup"><span data-stu-id="8dc0a-118">Methods that Handle Format Negotiation</span></span>

<span data-ttu-id="8dc0a-119">這些是 Windows Media Player 呼叫的方法，以取得外掛程式所支援之資料格式的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="8dc0a-119">These are the methods that Windows Media Player calls to get information about the data formats supported by the plug-in.</span></span> <span data-ttu-id="8dc0a-120">這些方法包括：</span><span class="sxs-lookup"><span data-stu-id="8dc0a-120">These methods include:</span></span>

-   <span data-ttu-id="8dc0a-121">**GetInputMaxLatency**</span><span class="sxs-lookup"><span data-stu-id="8dc0a-121">**GetInputMaxLatency**</span></span>
-   <span data-ttu-id="8dc0a-122">**GetInputSizeInfo**</span><span class="sxs-lookup"><span data-stu-id="8dc0a-122">**GetInputSizeInfo**</span></span>
-   <span data-ttu-id="8dc0a-123">**GetInputStreamInfo**</span><span class="sxs-lookup"><span data-stu-id="8dc0a-123">**GetInputStreamInfo**</span></span>
-   <span data-ttu-id="8dc0a-124">**GetInputType**</span><span class="sxs-lookup"><span data-stu-id="8dc0a-124">**GetInputType**</span></span>
-   <span data-ttu-id="8dc0a-125">**GetOutputSizeInfo**</span><span class="sxs-lookup"><span data-stu-id="8dc0a-125">**GetOutputSizeInfo**</span></span>
-   <span data-ttu-id="8dc0a-126">**GetOutputStreamInfo**</span><span class="sxs-lookup"><span data-stu-id="8dc0a-126">**GetOutputStreamInfo**</span></span>
-   <span data-ttu-id="8dc0a-127">**GetOutputType**</span><span class="sxs-lookup"><span data-stu-id="8dc0a-127">**GetOutputType**</span></span>
-   <span data-ttu-id="8dc0a-128">**GetStreamCount**</span><span class="sxs-lookup"><span data-stu-id="8dc0a-128">**GetStreamCount**</span></span>
-   <span data-ttu-id="8dc0a-129">**SetInputMaxLatency**</span><span class="sxs-lookup"><span data-stu-id="8dc0a-129">**SetInputMaxLatency**</span></span>
-   <span data-ttu-id="8dc0a-130">**SetInputType**</span><span class="sxs-lookup"><span data-stu-id="8dc0a-130">**SetInputType**</span></span>
-   <span data-ttu-id="8dc0a-131">**SetOutputType**</span><span class="sxs-lookup"><span data-stu-id="8dc0a-131">**SetOutputType**</span></span>

<span data-ttu-id="8dc0a-132">其中有幾種方法（例如 **GetInputType** 和 **SetInputType**）會使用 **sql-dmo \_ 媒體 \_ 類型** 結構來描述資料流程所使用的資料格式。</span><span class="sxs-lookup"><span data-stu-id="8dc0a-132">Several of these methods, such as **GetInputType** and **SetInputType**, use the **DMO\_MEDIA\_TYPE** structure to describe the format of the data used by a stream.</span></span> <span data-ttu-id="8dc0a-133">當 Windows Media Player 呼叫這些方法時，它會提供一種對等 **\_ 媒體 \_ 類型** 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="8dc0a-133">When Windows Media Player calls these methods, it provides a pointer to a **DMO\_MEDIA\_TYPE** structure.</span></span> <span data-ttu-id="8dc0a-134">如果方法（例如 **SetInputType** ）指定媒體類型資訊，外掛程式應該將 [] **\_ 媒體 \_ 類型** 結構複製到成員變數，並檢查其資料成員，以判斷 Windows Media Player 將在輸入緩衝區中提供的資料類型。</span><span class="sxs-lookup"><span data-stu-id="8dc0a-134">If a method such as **SetInputType** specifies the media type information, the plug-in should copy the **DMO\_MEDIA\_TYPE** structure to a member variable and inspect its data members to determine the type of data that Windows Media Player will provide in the input buffer.</span></span> <span data-ttu-id="8dc0a-135">如果 **GetInputType** 這類方法會抓取媒體型別資訊，外掛程式應該將包含 **sql-dmo \_ 媒體 \_ 類型** 結構的成員變數位址複製到參數清單中 Windows Media Player 所提供的指標。</span><span class="sxs-lookup"><span data-stu-id="8dc0a-135">If a method such as **GetInputType** retrieves the media type information, the plug-in should copy the address of the member variable containing the **DMO\_MEDIA\_TYPE** structure to the pointer provided by Windows Media Player in the parameter list.</span></span>

<span data-ttu-id="8dc0a-136">Windows Media Player 主要會使用兩種 **類型的 \_ 媒體 \_ 類型** 結構的成員：</span><span class="sxs-lookup"><span data-stu-id="8dc0a-136">Windows Media Player mainly uses two members of the **DMO\_MEDIA\_TYPE** structure:</span></span>

-   <span data-ttu-id="8dc0a-137">**majortype**： (GUID) 的全域唯一識別碼，可指定媒體的整體類別，例如音訊或影片。</span><span class="sxs-lookup"><span data-stu-id="8dc0a-137">**majortype**: A globally unique identifier (GUID) that specifies the overall category of the media, such as audio or video.</span></span>
-   <span data-ttu-id="8dc0a-138">**子類型**：指定更詳細描述媒體的 GUID，例如 PCM 音訊。</span><span class="sxs-lookup"><span data-stu-id="8dc0a-138">**subtype**: A GUID that specifies a more detailed description of the media, such as PCM audio.</span></span>

<span data-ttu-id="8dc0a-139">這些 Guid 可以在名為 uuid 的標頭中找到，該標頭包含在 Windows SDK 中。</span><span class="sxs-lookup"><span data-stu-id="8dc0a-139">These GUIDs can be found in the header named uuids.h, which is included with the Windows SDK.</span></span>

<span data-ttu-id="8dc0a-140">**GetInputSizeInfo** 之類的方法會提供相關資訊，以 Windows Media Player 配置處理緩衝區所需的記憶體數量。</span><span class="sxs-lookup"><span data-stu-id="8dc0a-140">Methods such as **GetInputSizeInfo** provide information to Windows Media Player about how much memory is required to allocate the processing buffers.</span></span> <span data-ttu-id="8dc0a-141">**GetStreamCount** 和 **GetOutputStreamInfo** 這類方法會提供有關 DSP 外掛程式所支援資料流程之數位和字元的資訊 Windows Media Player。</span><span class="sxs-lookup"><span data-stu-id="8dc0a-141">Methods such as **GetStreamCount** and **GetOutputStreamInfo** provide information to Windows Media Player about the number and character of the streams supported by the DSP plug-in.</span></span>

<span data-ttu-id="8dc0a-142">在特殊情況下，DMOs 會執行 **GetInputMaxLatency** 和 **SetInputMaxLatency** 。</span><span class="sxs-lookup"><span data-stu-id="8dc0a-142">**GetInputMaxLatency** and **SetInputMaxLatency** are implemented by DMOs in special cases.</span></span> <span data-ttu-id="8dc0a-143">Windows Media Player 的 DSP 外掛程式應該會傳回 E \_ >notimpl。</span><span class="sxs-lookup"><span data-stu-id="8dc0a-143">Windows Media Player DSP plug-ins should return E\_NOTIMPL.</span></span>

## <a name="methods-that-specify-or-retrieve-state-information"></a><span data-ttu-id="8dc0a-144">指定或取得狀態資訊的方法</span><span class="sxs-lookup"><span data-stu-id="8dc0a-144">Methods that Specify or Retrieve State Information</span></span>

<span data-ttu-id="8dc0a-145">這些方法可 Windows Media Player 呼叫來取得或設定與外掛程式目前狀態相關的值。</span><span class="sxs-lookup"><span data-stu-id="8dc0a-145">These are the methods that Windows Media Player calls to get or set values related to the current state of the plug-in.</span></span> <span data-ttu-id="8dc0a-146">這些方法包括：</span><span class="sxs-lookup"><span data-stu-id="8dc0a-146">These methods include:</span></span>

-   <span data-ttu-id="8dc0a-147">**GetInputCurrentType**</span><span class="sxs-lookup"><span data-stu-id="8dc0a-147">**GetInputCurrentType**</span></span>
-   <span data-ttu-id="8dc0a-148">**GetInputStatus**</span><span class="sxs-lookup"><span data-stu-id="8dc0a-148">**GetInputStatus**</span></span>
-   <span data-ttu-id="8dc0a-149">**GetOutputCurrentType**</span><span class="sxs-lookup"><span data-stu-id="8dc0a-149">**GetOutputCurrentType**</span></span>

<span data-ttu-id="8dc0a-150">**GetInputCurrentType** 和 **GetOutputCurrentType** 會使用 **： \_ 媒體 \_ 類型** 結構來傳回有關先前針對輸入和輸出資料流程設定之媒體類型 Windows Media Player 的資訊。</span><span class="sxs-lookup"><span data-stu-id="8dc0a-150">**GetInputCurrentType** and **GetOutputCurrentType** use the **DMO\_MEDIA\_TYPE** structure to return information to Windows Media Player about the media types previously set for the input and output streams.</span></span> <span data-ttu-id="8dc0a-151">**GetInputStatus** 會傳回旗標，告知 Windows Media Player DSP 外掛程式是否可以接受輸入資料。</span><span class="sxs-lookup"><span data-stu-id="8dc0a-151">**GetInputStatus** returns a flag that tells Windows Media Player whether the DSP plug-in can accept input data.</span></span>

## <a name="methods-that-handle-buffering-and-processing-data"></a><span data-ttu-id="8dc0a-152">處理緩衝處理和處理資料的方法</span><span class="sxs-lookup"><span data-stu-id="8dc0a-152">Methods that Handle Buffering and Processing Data</span></span>

<span data-ttu-id="8dc0a-153">這些是 Windows Media Player 呼叫的方法，以起始外掛程式執行以執行數位信號處理的各種進程。</span><span class="sxs-lookup"><span data-stu-id="8dc0a-153">These are the methods that Windows Media Player calls to initiate the various processes that the plug-in performs to do the digital signal processing.</span></span> <span data-ttu-id="8dc0a-154">這些方法包括：</span><span class="sxs-lookup"><span data-stu-id="8dc0a-154">These methods include:</span></span>

-   <span data-ttu-id="8dc0a-155">**AllocateStreamingResources**</span><span class="sxs-lookup"><span data-stu-id="8dc0a-155">**AllocateStreamingResources**</span></span>
-   <span data-ttu-id="8dc0a-156">**間斷**</span><span class="sxs-lookup"><span data-stu-id="8dc0a-156">**Discontinuity**</span></span>
-   <span data-ttu-id="8dc0a-157">**清除**</span><span class="sxs-lookup"><span data-stu-id="8dc0a-157">**Flush**</span></span>
-   <span data-ttu-id="8dc0a-158">**FreeStreamingResources**</span><span class="sxs-lookup"><span data-stu-id="8dc0a-158">**FreeStreamingResources**</span></span>
-   <span data-ttu-id="8dc0a-159">**鎖定**</span><span class="sxs-lookup"><span data-stu-id="8dc0a-159">**Lock**</span></span>
-   <span data-ttu-id="8dc0a-160">**ProcessInput**</span><span class="sxs-lookup"><span data-stu-id="8dc0a-160">**ProcessInput**</span></span>
-   <span data-ttu-id="8dc0a-161">**ProcessOutput**</span><span class="sxs-lookup"><span data-stu-id="8dc0a-161">**ProcessOutput**</span></span>

<span data-ttu-id="8dc0a-162">Windows Media Player 會呼叫 **AllocateStreamingResources** 和 **FREESTREAMINGRESOURCES** 來提供 DSP 外掛程式，讓您有機會設定或釋放外掛程式可能需要進行內部處理的任何其他緩衝區。</span><span class="sxs-lookup"><span data-stu-id="8dc0a-162">Windows Media Player calls **AllocateStreamingResources** and **FreeStreamingResources** to provide the DSP plug-in with an opportunity to set up or release any additional buffers the plug-in may require for internal processing.</span></span>

<span data-ttu-id="8dc0a-163">Windows Media Player 的 DSP 外掛程式不需要 **使用 sql-dmo 中斷** 方法。</span><span class="sxs-lookup"><span data-stu-id="8dc0a-163">Windows Media Player DSP plug-ins do not need to use the DMO **Discontinuity** method.</span></span>

<span data-ttu-id="8dc0a-164">Windows Media Player 呼叫 **Flush** 來指示 DSP 外掛程式，以排清所有內部緩衝的資料。</span><span class="sxs-lookup"><span data-stu-id="8dc0a-164">Windows Media Player calls **Flush** to direct the DSP plug-in to flush all internally buffered data.</span></span> <span data-ttu-id="8dc0a-165">外掛程式應釋放 **IMediaBuffer** 介面的任何參考、清除任何指定媒體緩衝區之時間戳記或取樣長度的值，然後重新初始化相依于媒體範例內容的任何內部狀態。</span><span class="sxs-lookup"><span data-stu-id="8dc0a-165">The plug-in should release any references to **IMediaBuffer** interfaces, clear any values that specify the time stamp or sample length for the media buffer, and reinitialize any internal states that depend upon the contents of the media sample.</span></span>

<span data-ttu-id="8dc0a-166">Windows Media Player 會呼叫 ProcessInput，將 **IMediaBuffer** 介面的指標傳遞至 DSP 外掛程式。</span><span class="sxs-lookup"><span data-stu-id="8dc0a-166">Windows Media Player calls ProcessInput to pass a pointer to an **IMediaBuffer** interface to the DSP plug-in.</span></span> <span data-ttu-id="8dc0a-167">這個介面可讓您存取 Windows Media Player 所配置的輸入緩衝區，以提供資料給外掛程式。</span><span class="sxs-lookup"><span data-stu-id="8dc0a-167">This interface provides access to the input buffer allocated by Windows Media Player to supply data to the plug-in.</span></span> <span data-ttu-id="8dc0a-168">Windows Media Player 接著會呼叫 **ProcessOutput** ，將指標傳遞至 **IMediaBuffer** 介面，以提供由 Windows Media Player 所配置之輸出緩衝區的存取，以接收來自 DSP 外掛程式的已處理資料。</span><span class="sxs-lookup"><span data-stu-id="8dc0a-168">Windows Media Player subsequently calls **ProcessOutput** to pass a pointer to an **IMediaBuffer** interface that provides access to the output buffer allocated by Windows Media Player to receive the processed data from the DSP plug-in.</span></span>

<span data-ttu-id="8dc0a-169">**IMediaObject** 介面包含名為 **Lock** 的方法。</span><span class="sxs-lookup"><span data-stu-id="8dc0a-169">The **IMediaObject** interface includes a method named **Lock**.</span></span> <span data-ttu-id="8dc0a-170">這個方法是設計用來取得或釋放該的鎖定，以在執行多個作業時保留一次。</span><span class="sxs-lookup"><span data-stu-id="8dc0a-170">This method is designed to acquire or release a lock on the DMO to keep the DMO serialized when performing multiple operations.</span></span> <span data-ttu-id="8dc0a-171">Wizard 程式碼中的 **IMediaObject：： Lock** 版本會覆寫 **鎖定** 的 ATL 執行。</span><span class="sxs-lookup"><span data-stu-id="8dc0a-171">The version of **IMediaObject::Lock** in the wizard code overrides the ATL implementation of **Lock**.</span></span> <span data-ttu-id="8dc0a-172">因為 Windows Media Player 會序列化對 DSP 外掛程式的 SQL-DMO 介面進行的呼叫，所以 **鎖定** 的執行只會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="8dc0a-172">Because Windows Media Player serializes calls made to the DMO interface of a DSP plug-in, the implementation of **Lock** simply returns S\_OK.</span></span> <span data-ttu-id="8dc0a-173">如需有關如何建立多執行緒的詳細資訊，請參閱 Windows SDK 的 [DirectShow] 區段。</span><span class="sxs-lookup"><span data-stu-id="8dc0a-173">For details about how to create a multithreaded DMO, refer to the DirectShow section of the Windows SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8dc0a-174">相關主題</span><span class="sxs-lookup"><span data-stu-id="8dc0a-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8dc0a-175">**必要的介面**</span><span class="sxs-lookup"><span data-stu-id="8dc0a-175">**Required Interfaces**</span></span>](required-interfaces.md)
</dt> </dl>

 

 





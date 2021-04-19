---
description: 本主題說明何時及如何使用 h.264/AVC Remux MFT 和的接收。
ms.assetid: 1DD236D9-775B-4417-BC49-BF52A6B3C8AD
title: 何時及如何使用 h.264/AVC Remux MFT 和數量的接收
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 132c582fa16eae56c4fec8809caa4bd501469e16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106976837"
---
# <a name="when-and-how-to-use-h264avc-remux-mft-and-mp4-sink"></a><span data-ttu-id="51568-103">何時及如何使用 h.264/AVC Remux MFT 和數量的接收</span><span class="sxs-lookup"><span data-stu-id="51568-103">When and How to Use H.264/AVC Remux MFT and MP4 Sink</span></span>

<span data-ttu-id="51568-104">本主題說明何時及如何使用 h.264/AVC Remux MFT 和的接收。</span><span class="sxs-lookup"><span data-stu-id="51568-104">This topic describes when and how to use a H.264/AVC Remux MFT and MP4 Sink.</span></span>

## <a name="when-to-use-h264avc-remux-mft"></a><span data-ttu-id="51568-105">使用 h.264/AVC Remux MFT 的時機</span><span class="sxs-lookup"><span data-stu-id="51568-105">When to use H.264/AVC Remux MFT</span></span>

<span data-ttu-id="51568-106">MPEG-2 檔案格式需要每個壓縮的範例都以正確的順序包含一張具有 NAL 單位的主要圖片。</span><span class="sxs-lookup"><span data-stu-id="51568-106">MPEG-4 file format requires that each compressed sample contains one primary picture with NAL units in the correct order.</span></span> <span data-ttu-id="51568-107"> (請參閱主要圖片的定義和強制 NAL 單位順序，例如7.4.1.2.3 中的區段、 **NAL 單位順序和程式碼圖片以及存取單位的關聯** 性，以及 h.264 AVC 規格。 ) 它也需要每個壓縮的範例都與簡報時間戳記、解碼時間戳記和取樣持續時間相關聯。</span><span class="sxs-lookup"><span data-stu-id="51568-107">(Please refer to the definition of primary picture and mandatory NAL units order in section 7.4.1.2.3, **Order of NAL units and coded pictures and association to access units**, of the H.264 AVC specification.) It also requires each compressed sample is associated with a presentation time stamp, decoding time stamp, and sample duration.</span></span>

<span data-ttu-id="51568-108">在許多情況下，當應用程式需要在 MPEG 4 檔案容器中錄製 h.264/AVC 影片時，壓縮的範例可能無法滿足上述需求。</span><span class="sxs-lookup"><span data-stu-id="51568-108">In many scenarios when applications need to record H.264/AVC video in a MPEG-4 file container, the compressed sample may not satisfy the above requirements.</span></span> <span data-ttu-id="51568-109">例如，一個壓縮的範例可能不會包含完整的主要圖片，也可能不會有正確的呈現時間戳記與其相關聯。</span><span class="sxs-lookup"><span data-stu-id="51568-109">For example, one compressed sample might not contain a complete primary picture or might not have a correct presentation time stamp associated with it.</span></span> <span data-ttu-id="51568-110">以下是一些應用程式範例：</span><span class="sxs-lookup"><span data-stu-id="51568-110">A few application examples are:</span></span>

-   <span data-ttu-id="51568-111">將 AVC 串流的基本影片寫入至 MPEG-2 檔案容器中。</span><span class="sxs-lookup"><span data-stu-id="51568-111">Write H.264/AVC streaming elementary video into MPEG-4 file container.</span></span>
-   <span data-ttu-id="51568-112">錄製攝影機在 MPEG 檔案容器中捕捉到 h.264/AVC 基本影片。</span><span class="sxs-lookup"><span data-stu-id="51568-112">Record camera captured H.264/AVC elementary video in MPEG-4 file container.</span></span>
-   <span data-ttu-id="51568-113">在 MPEG-2 檔案容器中錄製 h.264/AVC video 會議。</span><span class="sxs-lookup"><span data-stu-id="51568-113">Record H.264/AVC video conference in MPEG-4 file container.</span></span>
-   <span data-ttu-id="51568-114">串連 MPEG-2 TS 或 AVC 中的兩個 h.264/影片，並以正確的時間戳記寫入 MPEG-2 檔案容器中。</span><span class="sxs-lookup"><span data-stu-id="51568-114">Concatenate two H.264/AVC video in MPEG-2 TS or MP4 and write into MPEG-4 file container with correct time stamps.</span></span>
-   <span data-ttu-id="51568-115">Remux h.264/AVC video，從 AVCHD、MPEG-2 TS/PS 檔案格式到 MPEG 4 檔案格式。</span><span class="sxs-lookup"><span data-stu-id="51568-115">Remux H.264/AVC video from AVCHD, MPEG-2 TS/PS file format to MPEG-4 file format.</span></span>
-   <span data-ttu-id="51568-116">Trim/AVC video 檔案，但不包含轉碼。</span><span class="sxs-lookup"><span data-stu-id="51568-116">Trim H.264/AVC video file without transcoding.</span></span>

<span data-ttu-id="51568-117">在這種情況下，應用程式必須使用 h.264/AVC remux MFT 來轉換壓縮的範例，這些範例不包含完整的主要圖片，再將它們寫入 MPEG 4 檔案容器中。</span><span class="sxs-lookup"><span data-stu-id="51568-117">In this situation, the application needs to use a H.264/AVC remux MFT to convert the compressed samples not containing a complete primary picture before they are written into the MPEG-4 file container.</span></span>

## <a name="how-to-use-h264avc-remux-mft-and-mp4-sink"></a><span data-ttu-id="51568-118">如何使用 h.264/AVC Remux MFT 和的接收器</span><span class="sxs-lookup"><span data-stu-id="51568-118">How to use H.264/AVC Remux MFT and MP4 sink</span></span>

<span data-ttu-id="51568-119">將來源輸出媒體類型設定為 **MFVideoFormat \_ H264 \_ ES**，這表示每個範例可能不會包含完整的主要圖片。</span><span class="sxs-lookup"><span data-stu-id="51568-119">Set the source output media type to **MFVideoFormat\_H264\_ES**, which indicates each sample might not contain a complete primary picture.</span></span> <span data-ttu-id="51568-120">將配置接收的輸入媒體類型設定為 **MFVideoFormat \_ H264**。</span><span class="sxs-lookup"><span data-stu-id="51568-120">Set the input media type of MP4 sink to **MFVideoFormat\_H264**.</span></span> <span data-ttu-id="51568-121">因此，h.264/AVC remux MFT 的輸入媒體類型是 **MFVideoFormat \_ H264 \_ ES** ，而 H.264/AVC remux mft 的輸出媒體類型是 **MFVideoFormat \_ h264**，會自動插入拓撲解析程式。</span><span class="sxs-lookup"><span data-stu-id="51568-121">So, the input media type of the H.264/AVC remux MFT is **MFVideoFormat\_H264\_ES** and the output media type of the H.264/AVC remux MFT is **MFVideoFormat\_H264**, which will be automatically inserted into the topology resolver.</span></span>

<span data-ttu-id="51568-122">H.264/AVC remux 會忽略範例持續時間，因為範例不包含完整主要圖片的範例持續時間沒有明確意義。</span><span class="sxs-lookup"><span data-stu-id="51568-122">Sample duration is ignored by the H.264/AVC remux, because the sample duration for a sample not containing a complete primary picture does not have clear meaning.</span></span> <span data-ttu-id="51568-123">而是從畫面播放速率計算範例持續時間。</span><span class="sxs-lookup"><span data-stu-id="51568-123">Instead, the sample duration is calculated from the frame rate.</span></span> <span data-ttu-id="51568-124">畫面播放速率是從 sequence 參數計算而來。</span><span class="sxs-lookup"><span data-stu-id="51568-124">The frame rate is calculated from the sequence parameter.</span></span> <span data-ttu-id="51568-125">如果順序參數中沒有此資訊，則會從輸入媒體類型中的參數計算畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="51568-125">If the information does not exist in the sequence parameter, the frame rate is calculated from the parameters in the input media type.</span></span> <span data-ttu-id="51568-126">如果無法使用畫面播放速率資訊，則會使用預設的畫面播放速率 29.97 fps。</span><span class="sxs-lookup"><span data-stu-id="51568-126">If frame rate information is not available, the default frame rate of 29.97 fps is used.</span></span>

<span data-ttu-id="51568-127">H.264/AVC remux MFT 會根據畫面播放速率，以線性方式將解碼時間戳記插入每個壓縮圖片 (DTS) 。</span><span class="sxs-lookup"><span data-stu-id="51568-127">H.264/AVC remux MFT linearly interpolates the decoding time stamps (DTS) for each compressed picture according to the frame rate.</span></span> <span data-ttu-id="51568-128">H.264/AVC remux MFT 接受輸入範例中的輸入呈現時間戳記 (PT) ，並將它們傳遞給輸出（如果存在的話）。</span><span class="sxs-lookup"><span data-stu-id="51568-128">H.264/AVC remux MFT honors the input presentation time stamps (PTS) in input samples and passes them to the output if they exist.</span></span> <span data-ttu-id="51568-129">它會根據畫面播放速率、先前的點和圖片輸出順序來執行 PT 插補， () .DBP AVC 規格的 **4.5.3 上下加減一點流程** 中所指定的已解碼圖片緩衝處理。</span><span class="sxs-lookup"><span data-stu-id="51568-129">It performs PTS interpolation according to frame rate, the previous PTS, and the picture output order through Decoded Picture Buffering (DBP) bumping process as specified in **Annex C.4.5.3 Bumping process** of the H.264 AVC specification.</span></span> <span data-ttu-id="51568-130">H.264/AVC remux MFT 中的每個輸出範例都應該有時間、DTS 和取樣持續時間。</span><span class="sxs-lookup"><span data-stu-id="51568-130">Each output sample from the H.264/AVC remux MFT shall have PTS, DTS, and sample duration.</span></span> <span data-ttu-id="51568-131">H.264/AVC remux MFT 也會識別位流中的 IDR 圖片，並將其設定為具有 [MFSampleExtension \_ CLEANPOINT](mfsampleextension-cleanpoint-attribute.md)之 MF 屬性的清理點。</span><span class="sxs-lookup"><span data-stu-id="51568-131">H.264/AVC remux MFT also identifies the IDR pictures in the bitstream and sets them as clean point with the MF attribute of [MFSampleExtension\_CleanPoint](mfsampleextension-cleanpoint-attribute.md).</span></span>

<span data-ttu-id="51568-132">目前，h.264/AVC remux MFT 最多可處理64個重新排序的框架。</span><span class="sxs-lookup"><span data-stu-id="51568-132">Currently the H.264/AVC remux MFT can handle a maximum of 64 reordered frame.</span></span> <span data-ttu-id="51568-133">如果重新排序的框架數目超過64，而且存在長期參考框架，則 h.264/AVC remux MFT 會為該框架插入錯誤的時間，並在錯誤的時間輸出該框架。</span><span class="sxs-lookup"><span data-stu-id="51568-133">If the number of reordered frame exceeds 64 with a long term reference frame present, the H.264/AVC remux MFT will interpolate a wrong PTS for that frame and output that frame at a wrong time.</span></span>

<span data-ttu-id="51568-134">若要具現化 h.264/AVC remux MFT，請在 h.264/AVC remux MFT 上設定正確的輸入和輸出媒體類型、設定配置之接收的輸入媒體類型，以及解析拓撲。</span><span class="sxs-lookup"><span data-stu-id="51568-134">To instantiate a H.264/AVC remux MFT, set the correct input and output media types on the H.264/AVC remux MFT, set the input media type for the MP4 sink, and resolve the topology.</span></span>

<span data-ttu-id="51568-135">下列範例程式碼示範如何初始化 h.264/AVC remux MFT 和的接收。</span><span class="sxs-lookup"><span data-stu-id="51568-135">The following sample code show how to initialize the H.264/AVC remux MFT and MP4 sink.</span></span>

<span data-ttu-id="51568-136">若為 h.264/AVC remux MFT，</span><span class="sxs-lookup"><span data-stu-id="51568-136">For H.264/AVC remux MFT,</span></span>


```C++
hr = CoCreateInstance(
            CLSID_CMSH264RemuxMFT,
            NULL,
            CLSCTX_INPROC_SERVER,
            IID_IMFTransform,
            (void**) &pIMFTransform
            );
```



<span data-ttu-id="51568-137">不需要進一步設定。</span><span class="sxs-lookup"><span data-stu-id="51568-137">No further configuration is necessary.</span></span>

<span data-ttu-id="51568-138">針對的是，</span><span class="sxs-lookup"><span data-stu-id="51568-138">For MP4 sink,</span></span>


```C++
IMFByteStream*  pMFBSOutputFile = NULL;
hr = MFCreateFile(
    MF_ACCESSMODE_READWRITE,
    MF_OPENMODE_DELETE_IF_EXIST,
    MF_FILEFLAGS_NONE,
    m_pszOutputFile,
    &pMFBSOutputFile);
if(FAILED(hr))
{
    Log(L"ERROR>> Failed to create output file for MP4 Sink (hr=0x%x)", hr);
    break;
}

hr = MFCreateMPEG4MediaSink(
    pMFBSOutputFile,
    (guidMajorType == MFMediaType_Video) ? pMediaType : NULL,  // pMediaType comes from the output type of the remux MFT
    (guidMajorType == MFMediaType_Audio) ? pMediaType : NULL,
    &m_pMediaSink);
if(FAILED(hr))
{
    Log(L"ERROR>> Failed to create MP4 Sink (hr=0x%x)", hr);
    break;
}
hr = m_pMediaSink->GetStreamSinkByIndex(0, &pStream);
```



## <a name="related-topics"></a><span data-ttu-id="51568-139">相關主題</span><span class="sxs-lookup"><span data-stu-id="51568-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="51568-140">媒體基礎中支援的媒體格式</span><span class="sxs-lookup"><span data-stu-id="51568-140">Supported Media Formats in Media Foundation</span></span>](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

 




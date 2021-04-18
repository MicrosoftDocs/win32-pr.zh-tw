---
description: AVI 檔案格式的 DV 資料
ms.assetid: ae1ec184-afc3-4ec1-9b92-f53656293446
title: AVI 檔案格式的 DV 資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65f1393bfe4bbee4d080d90755f33cfa7f4a7fa4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467859"
---
# <a name="dv-data-in-the-avi-file-format"></a><span data-ttu-id="0b812-103">AVI 檔案格式的 DV 資料</span><span class="sxs-lookup"><span data-stu-id="0b812-103">DV Data in the AVI File Format</span></span>

<span data-ttu-id="0b812-104">Microsoft 已指定在 AVI 檔案中儲存數位視訊 (DV) 資料的格式。</span><span class="sxs-lookup"><span data-stu-id="0b812-104">Microsoft has specified the format for storage of digital video (DV) data in AVI files.</span></span> <span data-ttu-id="0b812-105">符合此規格可確保以這種格式撰寫的 AVI 檔案，將與 Windowsplatform 的未來版本的 DirectShow 數位影片架構相容。</span><span class="sxs-lookup"><span data-stu-id="0b812-105">Conforming to this specification will ensure that the AVI files authored in this format will be compatible with future versions of the DirectShow digital video architecture for the Windowsplatform.</span></span>

<span data-ttu-id="0b812-106">本文描述包含 DV 資料的 AVI 檔案格式。</span><span class="sxs-lookup"><span data-stu-id="0b812-106">This article describes the format of AVI files containing DV data.</span></span> <span data-ttu-id="0b812-107">特定 FOURCCs (四個字元的程式碼) ，用於交錯式 DV 資料流程和 DV 壓縮/解壓縮程式串流處理常式。</span><span class="sxs-lookup"><span data-stu-id="0b812-107">Specific FOURCCs (four-character codes) for interleaved DV data streams and DV compressor/decompressor stream handlers are defined.</span></span> <span data-ttu-id="0b812-108">已定義 DV 資料的資料流程格式結構。</span><span class="sxs-lookup"><span data-stu-id="0b812-108">The stream format structure for DV data is defined.</span></span> <span data-ttu-id="0b812-109">指定以 AVI 檔案格式儲存 DV 資料的兩種方法規格。</span><span class="sxs-lookup"><span data-stu-id="0b812-109">Specifications for two methods of storing DV data in the AVI file format are specified.</span></span>

<span data-ttu-id="0b812-110">假設讀者已熟悉 DV 資料格式。</span><span class="sxs-lookup"><span data-stu-id="0b812-110">It is assumed that the reader is familiar with the DV data format.</span></span> <span data-ttu-id="0b812-111"> (此格式定義于取用 *者使用的數位 Vcr 規格* 中，也稱為藍色書籍。 ) </span><span class="sxs-lookup"><span data-stu-id="0b812-111">(This format is defined in the *Specification of Consumer-use Digital VCRs*, also called the Blue Book.)</span></span>

<span data-ttu-id="0b812-112">有兩種類型的 DV AVI 檔案： AVI 檔案，其中包含一個 DV 資料流程，稱為 *type-1* files;以及包含 DV 影片作為「vids」資料流程和 DV 音訊做為「auds」串流（稱為 *類型 2* 檔案）的 AVI 檔。</span><span class="sxs-lookup"><span data-stu-id="0b812-112">There are two types of DV AVI files: AVI files that contain one DV data stream, called *type-1* files; and AVI files that contain DV video as a 'vids' stream and DV audio as 'auds' streams, called *type-2* files.</span></span>

<span data-ttu-id="0b812-113">**包含一個 DV 資料流程的 AVI 檔案 (類型 1)**</span><span class="sxs-lookup"><span data-stu-id="0b812-113">**AVI Files Containing One DV Data Stream (Type-1)**</span></span>

<span data-ttu-id="0b812-114">交錯的 DV 資料可以用原生格式儲存為 AVI RIFF 檔中的單一資料流程。</span><span class="sxs-lookup"><span data-stu-id="0b812-114">Interleaved DV data can be stored in its native format as a single stream within an AVI RIFF file.</span></span> <span data-ttu-id="0b812-115">這有一個優點，就是使用 DV 的資料儲存體的最小數量。</span><span class="sxs-lookup"><span data-stu-id="0b812-115">This has the advantage of using the minimum amount of data storage for DV.</span></span> <span data-ttu-id="0b812-116">主要的缺點是此檔案格式與 Windows 的影片不具回溯相容性，因為它不包含影片 ' vids ' 或音訊 ' auds ' 資料流程。</span><span class="sxs-lookup"><span data-stu-id="0b812-116">The primary disadvantage is that this file format is not backward-compatible with Video for Windows, because it doesn't contain either a video 'vids' or an audio 'auds' stream.</span></span> <span data-ttu-id="0b812-117">支援是透過透過 DirectShow 提供的 [Dv Muxer](dv-muxer-filter.md) 和 [dv 分隔](dv-splitter-filter.md) 器篩選器提供給交錯的 dv 串流。</span><span class="sxs-lookup"><span data-stu-id="0b812-117">Support is provided for the interleaved DV stream through the [DV Muxer](dv-muxer-filter.md) and [DV Splitter](dv-splitter-filter.md) filters provided with DirectShow.</span></span>

<span data-ttu-id="0b812-118">您可以藉由指定 ' iavs ' (交錯音訊和影片資料流程，將 DV 資料儲存在單一資料流程中，) FOURCC (**fccType** 成員中的四字元程式碼) ，以及 ' dvsd ' 資料流程標頭區塊之 **dvhd** 成員中的 ' dvsl '、' FOURCCs ' 或 ' fccHandler ' strh。</span><span class="sxs-lookup"><span data-stu-id="0b812-118">DV data can be stored in a single stream within an AVI RIFF file by specifying the 'iavs' (interleaved audio and video stream) FOURCC (four-character code) in the **fccType** member and either of the 'dvsd', 'dvhd', or 'dvsl' FOURCCs in the **fccHandler** member of the 'strh' stream header chunk.</span></span> <span data-ttu-id="0b812-119">影片串流的每秒畫面格必須指定在 **dwRate** 和 **dwScale** 成員中，以及 **dwLength** 成員中 ' movi ' 區塊內的影片區塊總數。</span><span class="sxs-lookup"><span data-stu-id="0b812-119">The frames per second of the video stream must be specified in the **dwRate** and **dwScale** members and the total number of video blocks in the 'movi' chunk in the **dwLength** member.</span></span>

<span data-ttu-id="0b812-120">' Dvsd ' 資料流程處理常式 FOURCC 指定 DV 資料在取用 *者使用數位 vcr* 的第2部分中定義。</span><span class="sxs-lookup"><span data-stu-id="0b812-120">The 'dvsd' stream handler FOURCC specifies that the DV data is as defined in Part 2 of the *Specification of Consumer-use Digital VCRs*.</span></span> <span data-ttu-id="0b812-121">影片的格式為525行 29.97 Hz (525-60) 或625線，25.00 Hz (625-50) 。</span><span class="sxs-lookup"><span data-stu-id="0b812-121">Video is in the format of 525 lines at 29.97 Hz (525-60) or 625 lines at 25.00 Hz (625-50).</span></span>

<span data-ttu-id="0b812-122">' Dvhd ' 資料流程處理常式 FOURCC 指定 DV 資料在取用 *者-使用數位 Vcr 規格* 的第3部分中定義。</span><span class="sxs-lookup"><span data-stu-id="0b812-122">The 'dvhd' stream handler FOURCC specifies that the DV data is as defined in Part 3 of the *Specification of Consumer-use Digital VCRs*.</span></span> <span data-ttu-id="0b812-123">影片的格式為1125行 30.00 Hz (1125-60) 或1250線，25.00 Hz (1250-50) 。</span><span class="sxs-lookup"><span data-stu-id="0b812-123">Video is in the format of 1125 lines at 30.00 Hz (1125-60) or 1250 lines at 25.00 Hz (1250-50).</span></span>

<span data-ttu-id="0b812-124">' Dvsl ' 資料流程處理常式 FOURCC 指定 DV 資料在取用 *者使用數位 vcr* 的第6部分中定義。</span><span class="sxs-lookup"><span data-stu-id="0b812-124">The 'dvsl' stream handler FOURCC specifies that the DV data is as defined in Part 6 of *Specification of Consumer-use Digital VCRs*.</span></span> <span data-ttu-id="0b812-125">影片的格式為高壓縮 SD (SDL) 。</span><span class="sxs-lookup"><span data-stu-id="0b812-125">Video is in the format of high-compression SD (SDL).</span></span>

> [!Note]  
> <span data-ttu-id="0b812-126">本文的其餘部分會提供 ' dvsd ' 資料流程的定義。</span><span class="sxs-lookup"><span data-stu-id="0b812-126">The remainder of this article provides definitions for 'dvsd' streams.</span></span>

 

<span data-ttu-id="0b812-127">資料流程標頭區塊後面必須接著 [**DVINFO**](/windows/desktop/api/strmif/ns-strmif-dvinfo) 資料流程格式區塊。</span><span class="sxs-lookup"><span data-stu-id="0b812-127">The stream header chunk must be followed by a [**DVINFO**](/windows/desktop/api/strmif/ns-strmif-dvinfo) stream format chunk.</span></span>

<span data-ttu-id="0b812-128">實際的 DV 資料會在 \# \# ' movi ' 區塊中儲存為 ' dc ' 區塊 (\# \# 格式代表資料流程識別碼) 。</span><span class="sxs-lookup"><span data-stu-id="0b812-128">The actual DV data is stored as '\#\#dc' chunks in the 'movi' chunk (the \#\# in the format represents the stream identifier).</span></span> <span data-ttu-id="0b812-129">每個區塊都包含一個資料框架，分別是10或12個適用于525-60 或625-50 系統的 DV DIF 序列。</span><span class="sxs-lookup"><span data-stu-id="0b812-129">Each chunk contains one frame of data, either 10 or 12 DV DIF sequences for 525-60 or 625-50 systems, respectively.</span></span> <span data-ttu-id="0b812-130">DV SD ( ' dvsd ' ) DIF 順序格式，定義于取用 *者使用數位 vcr* 的第2部分。</span><span class="sxs-lookup"><span data-stu-id="0b812-130">The DV SD ('dvsd') DIF sequence format is defined in Part 2 of the *Specification of Consumer-use Digital VCRs*.</span></span>

<span data-ttu-id="0b812-131">下列範例顯示具有一個 DV 資料流程之 AVI 檔案的 .AIFF RIFF 表單，以已完成的標頭區塊擴充。</span><span class="sxs-lookup"><span data-stu-id="0b812-131">The following example shows the AIFF RIFF form for an AVI file with one DV data stream, expanded with completed header chunks.</span></span>


```C++
00000000 RIFF (0FAE35D4) 'AVI '
0000000C     LIST (00000106) 'hdrl'
00000018         avih (00000038)
                     dwMicroSecPerFrame    : 33367
                     dwMaxBytesPerSec      : 3728000
                     dwPaddingGranularity  : 0
                     dwFlags               : 0x810 HASINDEX | TRUSTCKTYPE
                     dwTotalFrames         : 2192
                     dwInitialFrames       : 0
                     dwStreams             : 1
                     dwSuggestedBufferSize : 120000
                     dwWidth               : 720
                     dwHeight              : 480
                     dwReserved            : 0x0
00000058         LIST (0000006C) 'strl'
00000064             strh (00000038)
                         fccType               : 'iavs'
                         fccHandler            : 'dvsd'
                         dwFlags               : 0x0
                         wPriority             : 0
                         wLanguage             : 0x0 undefined
                         dwInitialFrames       : 0
                         dwScale               : 100 (29.970 Frames/Sec)
                         dwRate                : 2997
                         dwStart               : 0
                         dwLength              : 2192
                         dwSuggestedBufferSize : 120000
                         dwQuality             : 0
                         dwSampleSize          : 0
                         rcFrame               : 0,0,720,480
000000A4             strf (00000020)
                         dwDVAAuxSrc     : 0x........
                         dwDVAAuxCtl     : 0x........
                         dwDVAAuxSrc1    : 0x........
                         dwDVAAuxCtl1    : 0x........
                         dwDVVAuxSrc     : 0x........
                         dwDVVAuxCtl     : 0x........
                         dwDVReserved[2] : 0,0
000000CC     LIST (0FADAC00) 'movi'
0FADACD4     idx1 (00008900)
```



<span data-ttu-id="0b812-132">**包含 DV 影片和 DV 音訊串流的 AVI 檔案 (類型 2)**</span><span class="sxs-lookup"><span data-stu-id="0b812-132">**AVI Files Containing DV Video and DV Audio Streams (Type-2)**</span></span>

<span data-ttu-id="0b812-133">交錯的 DV 資料可以分割成影片串流，以及 AVI RIFF 檔案內的一到四個音訊串流。</span><span class="sxs-lookup"><span data-stu-id="0b812-133">Interleaved DV data can be split into a video stream and one to four audio streams within an AVI RIFF file.</span></span> <span data-ttu-id="0b812-134">這項功能的優點是可回溯相容于 Windows 的影片，因為它包含標準的影片 ' vids ' 資料流程，以及至少一個標準音頻 ' auds ' 資料流程的主要缺點是，此檔案格式需要將音訊資料重複儲存為音訊串流。</span><span class="sxs-lookup"><span data-stu-id="0b812-134">This has the advantage of being backward-compatible with Video for Windows, because it contains a standard video 'vids' stream and at least one standard audio 'auds' stream The primary disadvantage is that this file format requires the audio data to be redundantly stored as audio streams.</span></span> <span data-ttu-id="0b812-135">「影片」資料流程實際上是原生交錯的 DV 資料流程。</span><span class="sxs-lookup"><span data-stu-id="0b812-135">The "video" stream is actually the native interleaved DV data stream.</span></span> <span data-ttu-id="0b812-136">但是，如果是處理類型為 ' dvsd ' 的標準 ' vids ' 資料流程，則會使用 [DV 影片解碼](dv-video-decoder-filter.md) 。</span><span class="sxs-lookup"><span data-stu-id="0b812-136">However, as a standard 'vids' stream with a handler type of 'dvsd', the [DV Video Decoder](dv-video-decoder-filter.md) is used.</span></span> <span data-ttu-id="0b812-137">此格式也需要使用 [DV 分隔](dv-splitter-filter.md) 器篩選器來分割「已捕捉」檔案，然後再將它們寫入為 AVI 檔案。</span><span class="sxs-lookup"><span data-stu-id="0b812-137">This format also requires using the [DV Splitter](dv-splitter-filter.md) filter to split "captured" files before writing them as AVI files.</span></span>

<span data-ttu-id="0b812-138">DV 資料可以儲存為具有 AVI RIFF 檔中不同音訊串流數目的影片串流。</span><span class="sxs-lookup"><span data-stu-id="0b812-138">DV data can be stored as a video stream with a separate number of audio streams in an AVI RIFF file.</span></span> <span data-ttu-id="0b812-139">影片資料流程是使用標準的影片資料流程標頭所指定 (**fccType** 成員值為 ' vids ' ) 。</span><span class="sxs-lookup"><span data-stu-id="0b812-139">The video stream is specified with a standard video stream header (the **fccType** member value is 'vids').</span></span> <span data-ttu-id="0b812-140">**FccHandler** 成員指定為 ' dvsd '、' dvhd ' 或 ' dvsl '。</span><span class="sxs-lookup"><span data-stu-id="0b812-140">The **fccHandler** member is specified as 'dvsd', 'dvhd', or 'dvsl'.</span></span> <span data-ttu-id="0b812-141">影片串流的每秒畫面格必須指定在 **dwRate** 和 **dwScale** 成員中，以及 **dwLength** 成員中 ' movi ' 區塊內的影片區塊總數。</span><span class="sxs-lookup"><span data-stu-id="0b812-141">The frames per second of the video stream must be specified in the **dwRate** and **dwScale** members and the total number of video blocks in the 'movi' chunk in the **dwLength** member.</span></span>

<span data-ttu-id="0b812-142">在這個包含 DV 影片的 AVI 檔案中，以「vids」資料流程和 DV 音訊做為「auds」資料流程形式的 DV，影片串流格式區塊是標準的 [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) 結構。</span><span class="sxs-lookup"><span data-stu-id="0b812-142">In this AVI file containing DV video as a 'vids' stream and DV audio as 'auds' streams form of DV, the video stream format chunk is a standard [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure.</span></span> <span data-ttu-id="0b812-143">您可以選擇性地擴充資料流程格式區塊，以包含 [**DVINFO**](/windows/desktop/api/strmif/ns-strmif-dvinfo) 區塊，方法是將資料流程格式區塊大小從40個位元組增加 (**BITMAPINFOHEADER** 結構的大小) 為72個位元組 (**BITMAPINFOHEADER** 加 **DVINFO**) 結構的大小，然後緊接在 **BITMAPINFOHEADER** 資料結構 **的 DVINFO 資料** 結構後面。</span><span class="sxs-lookup"><span data-stu-id="0b812-143">The stream format chunk can be optionally extended to include the [**DVINFO**](/windows/desktop/api/strmif/ns-strmif-dvinfo) chunk, by increasing the stream format chunk size from 40 bytes (size of the **BITMAPINFOHEADER** structure) to 72 bytes (size of **BITMAPINFOHEADER** plus **DVINFO** structures) and immediately following the **BITMAPINFOHEADER** data structure with a **DVINFO** data structure.</span></span>

<span data-ttu-id="0b812-144">音訊串流 (s) 是使用標準音頻資料流程標頭所指定， (**fccType** 成員值為 ' auds ' ) 。</span><span class="sxs-lookup"><span data-stu-id="0b812-144">The audio stream(s) is specified with a standard audio stream header (the **fccType** member value is 'auds').</span></span> <span data-ttu-id="0b812-145">**FccHandler** 成員不會用於音訊串流。</span><span class="sxs-lookup"><span data-stu-id="0b812-145">The **fccHandler** member is not used for audio streams.</span></span>

<span data-ttu-id="0b812-146">DV 影片資料會以「dc」 \# \# 區塊的形式儲存（如先前的 AVI 檔案描述中所定義，其中包含一個 DV 資料），而音訊資料會 \# \# 在 ' movi ' 區塊中儲存為 ' wb ' 區塊。</span><span class="sxs-lookup"><span data-stu-id="0b812-146">The DV video data is stored as '\#\#dc' chunks, as defined in the preceding description of an AVI file with one DV data, and the audio data is stored as '\#\#wb' chunks in the 'movi' chunk.</span></span>

> [!Note]  
> <span data-ttu-id="0b812-147">某些語言和國家/地區可能不提供取用 *者使用數位 vcr 的規格* 。</span><span class="sxs-lookup"><span data-stu-id="0b812-147">The *Specification of Consumer-use Digital VCRs* may not be available in some languages and countries.</span></span>

 

<span data-ttu-id="0b812-148">下列範例顯示包含 DV 影片作為「vids」資料流程的 AVI 檔案的 .AIFF RIFF 表單，以及以已完成的標頭區塊擴充的 DV 音訊做為 ' auds ' 資料流程的表單 (包括在 ' BITMAPINFO ' 子區塊的 [**strf**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo)中，于 "vids ' 資料流程) 之後的選擇性 [**DVINFO**](/windows/desktop/api/strmif/ns-strmif-dvinfo)資料。</span><span class="sxs-lookup"><span data-stu-id="0b812-148">The following example shows the AIFF RIFF form for an AVI file containing DV video as a 'vids' stream and DV audio as 'auds' streams expanded with completed header chunks (including optional [**DVINFO**](/windows/desktop/api/strmif/ns-strmif-dvinfo) data following the [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) in the 'strf' sub-chunk for the 'vids' stream).</span></span>


```C++
00000000 RIFF (103E2920) 'AVI '
0000000C     LIST (00000146) 'hdrl'
00000018         avih (00000038)
                     dwMicroSecPerFrame    : 33367
                     dwMaxBytesPerSec      : 3728000
                     dwPaddingGranularity  : 0
                     dwFlags               : 0x810 HASINDEX | TRUSTCKTYPE
                     dwTotalFrames         : 2192
                     dwInitialFrames       : 0
                     dwStreams             : 2
                     dwSuggestedBufferSize : 120000
                     dwWidth               : 720
                     dwHeight              : 480
                     dwReserved            : 0x0
00000058         LIST (00000094) 'strl'
00000064             strh (00000038)
                         fccType               : 'vids'
                         fccHandler            : 'dvsd'
                         dwFlags               : 0x0
                         wPriority             : 0
                         wLanguage             : 0x0 undefined
                         dwInitialFrames       : 0
                         dwScale               : 100 (29.970 Frames/Sec)
                         dwRate                : 2997
                         dwStart               : 0
                         dwLength              : 2192
                         dwSuggestedBufferSize : 120000
                         dwQuality             : 0
                         dwSampleSize          : 0
                         rcFrame               : 0,0,720,480
000000A4             strf (00000048)
                         biSize          : 40
                         biWidth         : 720
                         biHeight        : 480
                         biPlanes        : 1
                         biBitCount      : 24
                         biCompression   : 0x64737664 'dvsd'
                         biSizeImage     : 120000
                         biXPelsPerMeter : 0
                         biYPelsPerMeter : 0
                         biClrUsed       : 0
                         biClrImportant  : 0
                         dwDVAAuxSrc     : 0x........
                         dwDVAAuxCtl     : 0x........
                         dwDVAAuxSrc1    : 0x........
                         dwDVAAuxCtl1    : 0x........
                         dwDVVAuxSrc     : 0x........
                         dwDVVAuxCtl     : 0x........
                         dwDVReserved[2] : 0,0
000000F4         LIST (0000005E) 'strl'
00000100             strh (00000038)
                         fccType               : 'auds'
                         fccHandler            : '    '
                         dwFlags               : 0x0
                         wPriority             : 0
                         wLanguage             : 0x0 undefined
                         dwInitialFrames       : 0
                         dwScale               : 1 (32000.000 Samples/Sec)
                         dwRate                : 32000
                         dwStart               : 0
                         dwLength              : 2340474
                         dwSuggestedBufferSize : 4272
                         dwQuality             : 0
                         dwSampleSize          : 4
                         rcFrame               : 0,0,0,0
00000140             strf (00000012)
                         wFormatTag      : 1 PCM
                         nChannels       : 2
                         nSamplesPerSec  : 32000
                         nAvgBytesPerSec : 128000
                         nBlockAlign     : 4
                         wBitsPerSample  : 16
                         cbSize          : 0
00000814     LIST (103D0EF4) 'movi'
103D1710     idx1 (00011210)
```



## <a name="related-topics"></a><span data-ttu-id="0b812-149">相關主題</span><span class="sxs-lookup"><span data-stu-id="0b812-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b812-150">AVI 檔案格式</span><span class="sxs-lookup"><span data-stu-id="0b812-150">AVI File Format</span></span>](avi-file-format.md)
</dt> </dl>

 

 

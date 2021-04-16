---
description: 關於 DirectShow 中的數位視訊
ms.assetid: 0570bf7c-c38d-4ada-9593-27b9be117893
title: 關於 DirectShow 中的數位視訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8f4ae0253754583bb89132289db87f0aad673d6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104562618"
---
# <a name="about-digital-video-in-directshow"></a><span data-ttu-id="084d1-103">關於 DirectShow 中的數位視訊</span><span class="sxs-lookup"><span data-stu-id="084d1-103">About Digital Video in DirectShow</span></span>

<span data-ttu-id="084d1-104">數位視訊 (DV) 可以從 DV 攝影機中捕捉、儲存在使用者電腦上的檔案中，或使用影片磁帶錄製器儲存在磁帶上 (VTR) 。</span><span class="sxs-lookup"><span data-stu-id="084d1-104">Digital video (DV) can be captured from a DV camera, stored in a file on the user's computer, or stored on tape using a video tape recorder (VTR).</span></span> <span data-ttu-id="084d1-105">因此，應用程式可能會在 DV 串流上執行的作業包括：</span><span class="sxs-lookup"><span data-stu-id="084d1-105">Thus, the operations that an application might perform on a DV stream include:</span></span>

-   <span data-ttu-id="084d1-106">從 DV 攝影機捕獲實況影片。</span><span class="sxs-lookup"><span data-stu-id="084d1-106">Capture live video from a DV camera.</span></span>
-   <span data-ttu-id="084d1-107">從 VTR 磁帶傳輸 DV 資料至電腦。</span><span class="sxs-lookup"><span data-stu-id="084d1-107">Transmit DV data from VTR tape to the computer.</span></span>
-   <span data-ttu-id="084d1-108">將 DV 資料從電腦傳輸到 VTR。</span><span class="sxs-lookup"><span data-stu-id="084d1-108">Transmit DV data from the computer to the VTR.</span></span>
-   <span data-ttu-id="084d1-109">從檔案讀取 DV 資料。</span><span class="sxs-lookup"><span data-stu-id="084d1-109">Read DV data from a file.</span></span>
-   <span data-ttu-id="084d1-110">將 DV 資料寫入檔案。</span><span class="sxs-lookup"><span data-stu-id="084d1-110">Write DV data to a file.</span></span>
-   <span data-ttu-id="084d1-111">轉譯 DV 串流中的音訊和影片。</span><span class="sxs-lookup"><span data-stu-id="084d1-111">Render the audio and video in a DV stream.</span></span>

<span data-ttu-id="084d1-112">DirectShow 提供下列 DV 篩選器：</span><span class="sxs-lookup"><span data-stu-id="084d1-112">DirectShow provides the following DV filters:</span></span>

-   <span data-ttu-id="084d1-113">[MSDV 驅動程式](msdv-driver.md)。</span><span class="sxs-lookup"><span data-stu-id="084d1-113">[MSDV Driver](msdv-driver.md).</span></span> <span data-ttu-id="084d1-114">MSDV 驅動程式控制 DV 裝置，例如攝像機。</span><span class="sxs-lookup"><span data-stu-id="084d1-114">The MSDV driver controls a DV device, such as a camcorder.</span></span> <span data-ttu-id="084d1-115">裝置可能具有相機子單位和 VTR 子單位;MSDV 會控制兩個次單元連接。</span><span class="sxs-lookup"><span data-stu-id="084d1-115">The device may have a camera subunit and a VTR subunit; MSDV controls both subunits.</span></span> <span data-ttu-id="084d1-116">MSDV 驅動程式會以 DirectShow 濾波器的形式出現在應用程式中。</span><span class="sxs-lookup"><span data-stu-id="084d1-116">The MSDV driver appears to applications as a DirectShow filter.</span></span>
-   <span data-ttu-id="084d1-117">[DV 分隔](dv-splitter-filter.md) 器篩選器。</span><span class="sxs-lookup"><span data-stu-id="084d1-117">[DV Splitter](dv-splitter-filter.md) filter.</span></span> <span data-ttu-id="084d1-118">DV 框架在相同的框架中包含音訊和影片。</span><span class="sxs-lookup"><span data-stu-id="084d1-118">DV frames contain audio and video in the same frame.</span></span> <span data-ttu-id="084d1-119">DV 分隔器篩選器會將音訊資料解壓縮，並將其輸出為一或兩個音訊串流。</span><span class="sxs-lookup"><span data-stu-id="084d1-119">The DV Splitter filter extracts the audio data and outputs it as one or two audio streams.</span></span> <span data-ttu-id="084d1-120">它會將原始資料輸出為個別的 DV 影片串流。</span><span class="sxs-lookup"><span data-stu-id="084d1-120">It outputs the original data as a separate DV video stream.</span></span>
-   <span data-ttu-id="084d1-121">[DV 影片解碼](dv-video-decoder-filter.md) 篩選器。</span><span class="sxs-lookup"><span data-stu-id="084d1-121">[DV Video Decoder](dv-video-decoder-filter.md) filter.</span></span> <span data-ttu-id="084d1-122">將 DV 影片解碼成未壓縮的影片。</span><span class="sxs-lookup"><span data-stu-id="084d1-122">Decodes DV video into uncompressed video.</span></span>
-   <span data-ttu-id="084d1-123">[DV 影片編碼器](dv-video-encoder-filter.md) 篩選器。</span><span class="sxs-lookup"><span data-stu-id="084d1-123">[DV Video Encoder](dv-video-encoder-filter.md) filter.</span></span> <span data-ttu-id="084d1-124">將未壓縮的影片編碼為 DV 編碼的影片。</span><span class="sxs-lookup"><span data-stu-id="084d1-124">Encodes uncompressed video to DV-encoded video.</span></span>
-   <span data-ttu-id="084d1-125">[DV Muxer](dv-muxer-filter.md)。</span><span class="sxs-lookup"><span data-stu-id="084d1-125">[DV Muxer](dv-muxer-filter.md).</span></span> <span data-ttu-id="084d1-126">結合 DV 影片串流與一或兩個音訊串流，以建立單一交錯 DV 串流。</span><span class="sxs-lookup"><span data-stu-id="084d1-126">Combines a DV video stream with one or two audio streams, to create a single interleaved DV stream.</span></span>

<span data-ttu-id="084d1-127">DV 分隔器和 DV 影片解碼可一起運作。</span><span class="sxs-lookup"><span data-stu-id="084d1-127">The DV Splitter and DV Video Decoder work together.</span></span> <span data-ttu-id="084d1-128">分割器會採用交錯的資料流程，並輸出個別的音訊和 DV 影片串流。</span><span class="sxs-lookup"><span data-stu-id="084d1-128">The splitter takes the interleaved stream and outputs separate audio and DV video streams.</span></span> <span data-ttu-id="084d1-129">此解碼器會將 DV 影片轉換成未壓縮的影片。</span><span class="sxs-lookup"><span data-stu-id="084d1-129">The decoder converts the DV video to uncompressed video.</span></span> <span data-ttu-id="084d1-130">下圖說明此程式。</span><span class="sxs-lookup"><span data-stu-id="084d1-130">The following image illustrates this process.</span></span>

![dv 分隔器和 dv 解碼器](images/dv-filters1.png)

<span data-ttu-id="084d1-132">DV 影片編碼器和 DV Muxer 會反轉進程：編碼器會將未壓縮的影片轉換成 DV 影片，而 mux 則結合了音訊和 DV 影片來建立單一交錯式串流，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="084d1-132">The DV Video Encoder and the DV Muxer reverse the process: The encoder converts uncompressed video to DV video, and the mux combines audio and DV video to create a single interleaved stream, as shown in the following diagram.</span></span>

![dv 編碼器和 dv muxer](images/dv-filters2.png)

## <a name="related-topics"></a><span data-ttu-id="084d1-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="084d1-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="084d1-135">DirectShow 中的數位視訊</span><span class="sxs-lookup"><span data-stu-id="084d1-135">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> </dl>

 

 




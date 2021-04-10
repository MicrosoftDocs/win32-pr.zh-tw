---
title: 使用 Windows Media 視訊9螢幕編解碼器取得良好的結果
description: 使用 Windows Media 視訊9螢幕編解碼器取得良好的結果
ms.assetid: c5b080d3-2934-4af7-8f01-9ab0829db05d
keywords:
- Windows Media 格式 SDK，Windows Media 視訊9螢幕編解碼器
- Advanced Systems Format (ASF) ，Windows Media 視訊9螢幕編解碼器
- ASF (Advanced Systems Format) ，Windows Media 視訊9螢幕編解碼器
- 編解碼器，Windows Media 視訊9螢幕
- Windows Media 視訊9螢幕編解碼器，結果
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a297638c7c50a6380fd4c43ea1d4b9971d44db5
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "103932948"
---
# <a name="getting-good-results-with-the-windows-media-video-9-screen-codec"></a><span data-ttu-id="d10cd-108">使用 Windows Media 視訊9螢幕編解碼器取得良好的結果</span><span class="sxs-lookup"><span data-stu-id="d10cd-108">Getting Good Results with the Windows Media Video 9 Screen Codec</span></span>

<span data-ttu-id="d10cd-109">Windows Media 視訊9畫面編解碼器的設計目的是要為螢幕擷取畫面產生高度壓縮的影片。</span><span class="sxs-lookup"><span data-stu-id="d10cd-109">The Windows Media Video 9 Screen codec is designed to produce highly compressed video for screen capture.</span></span> <span data-ttu-id="d10cd-110">由於螢幕擷取畫面的大部分需求都牽涉到相當簡單和靜態的映射，因此，最高層級的壓縮通常表示影像品質很大的犧牲。</span><span class="sxs-lookup"><span data-stu-id="d10cd-110">Because most of the need for screen capture involves fairly simple and static images, the high levels of compression attained do not usually mean a great sacrifice in image quality.</span></span> <span data-ttu-id="d10cd-111">不過，每個螢幕擷取畫面都是不同的，而產生的影像品質可能會因情況而有很大的差異。</span><span class="sxs-lookup"><span data-stu-id="d10cd-111">However, each screen capture is different, and the resulting image quality can vary considerably depending upon the circumstances.</span></span>

<span data-ttu-id="d10cd-112">判斷螢幕編解碼器會話設定檔設定的最佳方式，就是使用以品質為基礎的變數位元速率資料流程來編碼測試檔案。</span><span class="sxs-lookup"><span data-stu-id="d10cd-112">The best way to determine the profile settings for a screen codec session is to encode a test file using a quality-based variable bit rate stream.</span></span> <span data-ttu-id="d10cd-113">將品質設定為您想要的值，並將螢幕擷取畫面編碼為您錄製最終檔案的方式。</span><span class="sxs-lookup"><span data-stu-id="d10cd-113">Set the quality to the value you desire, and encode a screen capture as if you were recording the final file.</span></span> <span data-ttu-id="d10cd-114">寫入檔案時，請使用非同步讀取器物件來播放，並定期呼叫 [**IWMReaderAdvanced：： GetStatistics**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstatistics)。</span><span class="sxs-lookup"><span data-stu-id="d10cd-114">When the file is written, play it using the asynchronous reader object, making regular calls to [**IWMReaderAdvanced::GetStatistics**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstatistics).</span></span> <span data-ttu-id="d10cd-115">藉由監視每次呼叫之 [**WM \_ 讀取器 \_ 統計資料**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_reader_statistics)結構的 **dwBandwidth** 成員值，您可以判斷達到您想要的品質所需的大約位元速率。</span><span class="sxs-lookup"><span data-stu-id="d10cd-115">By monitoring the value of the **dwBandwidth** member of the [**WM\_READER\_STATISTICS**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_reader_statistics) structure for each call, you can determine the approximate bit rate required to achieve the quality you want.</span></span> <span data-ttu-id="d10cd-116">然後，您可以將該位元速率用於常數位元速率編碼。</span><span class="sxs-lookup"><span data-stu-id="d10cd-116">You can then use that bit rate for constant bit rate encoding.</span></span>

<span data-ttu-id="d10cd-117">如果您發現您想要的品質需要比您用於傳遞案例更高的位元速率，您可以嘗試下列技術，以從編解碼器獲得更高的效率。</span><span class="sxs-lookup"><span data-stu-id="d10cd-117">If you discover that the quality you want requires a higher bit rate than you can use for your delivery scenario, you can try the following techniques to get more efficiency from the codec.</span></span>

-   <span data-ttu-id="d10cd-118">針對螢幕擷取畫面使用較小的解析度。</span><span class="sxs-lookup"><span data-stu-id="d10cd-118">Use a smaller resolution for the screen capture.</span></span> <span data-ttu-id="d10cd-119">若要取得比您所需更大的螢幕解析度，也可以藉由呈現比所需更多的資訊，來為檢視器建立混淆。</span><span class="sxs-lookup"><span data-stu-id="d10cd-119">Capturing a larger screen resolution than you need can also create confusion for the viewer by presenting more information than is needed.</span></span>
-   <span data-ttu-id="d10cd-120">在螢幕擷取畫面中使用較少的圖形。</span><span class="sxs-lookup"><span data-stu-id="d10cd-120">Use fewer graphics in the screen capture.</span></span> <span data-ttu-id="d10cd-121">Windows Media 視訊9畫面編解碼器經過優化，可將 Windows 基本專案和高品質的文字編碼。</span><span class="sxs-lookup"><span data-stu-id="d10cd-121">The Windows Media Video 9 Screen codec is optimized to encode Windows primitives and text with high quality.</span></span> <span data-ttu-id="d10cd-122">通常是因為點陣圖圖形所造成的問題，這些圖形通常包含數以千計的個人色彩。</span><span class="sxs-lookup"><span data-stu-id="d10cd-122">Usually problems occur because of bitmapped graphics, which often contain thousands of individual colors.</span></span> <span data-ttu-id="d10cd-123">當您捕捉時，螢幕上的點陣圖越少，結果就越好。</span><span class="sxs-lookup"><span data-stu-id="d10cd-123">The fewer bitmaps that are on the screen when you capture, the better your results will be.</span></span> <span data-ttu-id="d10cd-124">如果您無法從螢幕擷取畫面中排除圖形，有幾種方式可以將點陣圖對影像品質的影響降至最低：</span><span class="sxs-lookup"><span data-stu-id="d10cd-124">If you cannot eliminate graphics from your screen capture, there are several ways to minimize the impact a bitmap has on image quality:</span></span>
    -   <span data-ttu-id="d10cd-125">縮小圖形的大小。</span><span class="sxs-lookup"><span data-stu-id="d10cd-125">Reduce the size of the graphic.</span></span>
    -   <span data-ttu-id="d10cd-126">減少同時出現在螢幕上的個別圖形數目。</span><span class="sxs-lookup"><span data-stu-id="d10cd-126">Reduce the number of individual graphics that appear on the screen concurrently.</span></span>
    -   <span data-ttu-id="d10cd-127">減少圖形的移動量。</span><span class="sxs-lookup"><span data-stu-id="d10cd-127">Reduce the amount of movement of the graphic.</span></span> <span data-ttu-id="d10cd-128">例如，如果圖形是在視窗中，請盡可能讓視窗保持固定。</span><span class="sxs-lookup"><span data-stu-id="d10cd-128">For example, if the graphic is in a window, keep the window as stationary as possible.</span></span>
    -   <span data-ttu-id="d10cd-129">避免將滑鼠指標移到圖形上，或將視窗或其他元素拖曳到圖形上。</span><span class="sxs-lookup"><span data-stu-id="d10cd-129">Avoid moving the mouse pointer over the graphic, or dragging windows or other elements over the graphic.</span></span>
-   <span data-ttu-id="d10cd-130">使用較慢的 [*畫面播放速率*](wmformat-glossary.md)。</span><span class="sxs-lookup"><span data-stu-id="d10cd-130">Use a slower [*frame rate*](wmformat-glossary.md).</span></span> <span data-ttu-id="d10cd-131">螢幕捕捉通常會以極低的畫面播放速率來有效 (有時每秒4或5個畫面格) 。</span><span class="sxs-lookup"><span data-stu-id="d10cd-131">Screen captures can often be effective at very low frame rates (sometimes as low as 4 or 5 frames per second).</span></span>
-   <span data-ttu-id="d10cd-132">減少伴隨音訊的位元速率。</span><span class="sxs-lookup"><span data-stu-id="d10cd-132">Reduce the bit rate of the accompanying audio.</span></span>

<span data-ttu-id="d10cd-133">此外，編解碼器不支援調整影片矩形的大小。</span><span class="sxs-lookup"><span data-stu-id="d10cd-133">Also, the codec does not support resizing of the video rectangle.</span></span> <span data-ttu-id="d10cd-134">換句話說，如果您嘗試使用編解碼器將 800 x 600 螢幕編碼成 640 x 480 的影片矩形，則產生的影片將會有重要的成品，可讓螢幕上的大部分文字無法辨認。</span><span class="sxs-lookup"><span data-stu-id="d10cd-134">In other words, if you try to use the codec to encode a 800 x 600 screen down into to a 640 x 480 video rectangle, the resulting video will have significant artifacts that may make much of the text on the screen illegible.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d10cd-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="d10cd-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d10cd-136">**設定畫面抓取資料流程**</span><span class="sxs-lookup"><span data-stu-id="d10cd-136">**Configuring Screen Capture Streams**</span></span>](configuring-screen-capture-streams.md)
</dt> <dt>

[<span data-ttu-id="d10cd-137">**設定資料流程**</span><span class="sxs-lookup"><span data-stu-id="d10cd-137">**Configuring Streams**</span></span>](configuring-streams.md)
</dt> </dl>

 

 





---
description: MSYUV 是 YUV 至 RGB 的色彩空間轉換器編解碼器。
ms.assetid: 77b00937-ac63-4b23-b546-c0896b3c57ba
title: MSYUV 色彩空間轉換器編解碼器
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 838e7cd749042b2fb97adaf0b2b4cd0378a81c07
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001935"
---
# <a name="msyuv-color-space-converter-codec"></a><span data-ttu-id="f7daa-103">MSYUV 色彩空間轉換器編解碼器</span><span class="sxs-lookup"><span data-stu-id="f7daa-103">MSYUV Color Space Converter Codec</span></span>

<span data-ttu-id="f7daa-104">MSYUV 是 YUV 至 RGB 的色彩空間轉換器編解碼器。</span><span class="sxs-lookup"><span data-stu-id="f7daa-104">MSYUV is a YUV-to-RGB color space converter codec.</span></span> <span data-ttu-id="f7daa-105">它可在用戶端上以 YUV 格式播放影片來源資料，而這些用戶端的視頻顯示器介面卡無法用於硬體中的 YUV 至 RGB 轉換。</span><span class="sxs-lookup"><span data-stu-id="f7daa-105">It enables playback of video source data in YUV formats on clients whose video display adapter cannot be used for YUV-to-RGB conversions in hardware.</span></span> <span data-ttu-id="f7daa-106">編解碼器會透過 [AVI 解壓縮](avi-decompressor-filter.md) 套裝程式裝函式篩選來參與篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="f7daa-106">The codec participates in filter graphs through the [AVI Decompressor](avi-decompressor-filter.md) wrapper filter.</span></span>

<span data-ttu-id="f7daa-107">具有1394或 USB 介面的數位會議攝影機，可以產生各種形式的影像資料。</span><span class="sxs-lookup"><span data-stu-id="f7daa-107">Digital conferencing cameras with 1394 or USB interfaces can produce image data in various YUV formats.</span></span> <span data-ttu-id="f7daa-108">如果顯示器硬體不支援面板上的 YUV 到 RGB 轉換，或者硬體轉換功能無法用於某些其他原因，則必須先將 YUV 影像資料轉換成 RGB 格式，然後再傳送到影片轉譯器。</span><span class="sxs-lookup"><span data-stu-id="f7daa-108">If the display hardware does not support on-board YUV-to-RGB conversion, or if the hardware conversion capability cannot be used for some other reason, then the YUV image data must be converted to RGB format before it is sent to the Video Renderer.</span></span>

<span data-ttu-id="f7daa-109">由於 [影片](video-renderer-filter.md)轉譯器在連接時需要 RGB 輸入類型，因此在自動建立圖表時，此篩選器可能會從影片轉譯器插入圖形上游。</span><span class="sxs-lookup"><span data-stu-id="f7daa-109">Because of the [Video Renderer](video-renderer-filter.md)'s requirement for an RGB input type at connection time, this filter might be inserted into a graph upstream from the Video Renderer during automatic graph building.</span></span> <span data-ttu-id="f7daa-110">具體而言，如果圖形產生器在上游篩選器輸出釘選的媒體類型中偵測到 YUV 格式，則圖形產生器會插入 AVI 解壓縮程式，然後載入 MSYUV 編解碼器，並一開始就設定它以執行轉換成 RGB。</span><span class="sxs-lookup"><span data-stu-id="f7daa-110">Specifically, if the Graph Builder detects a YUV format in the media type of the upstream filter's output pin, the Graph Builder will insert the AVI Decompressor, which will then load the MSYUV codec and configure it initially to perform the conversion to RGB.</span></span> <span data-ttu-id="f7daa-111">在圖形首次轉換成執行中或已暫停狀態之後，影片轉譯器篩選器可以偵測視頻顯示器介面卡是否可以在硬體中執行轉換。</span><span class="sxs-lookup"><span data-stu-id="f7daa-111">After the graph first transitions to a run or paused state, the Video Renderer filter can detect whether the video display adapter can perform the conversion in hardware.</span></span> <span data-ttu-id="f7daa-112">如果可以，則會通知 AVI 解壓縮程式，並將 MSYUV 重新配置為以「傳遞模式」操作，這會造成編解碼器略過轉換，並將 YUV 影像資料直接複製到視訊記憶體中的 DirectDraw 重迭表面。</span><span class="sxs-lookup"><span data-stu-id="f7daa-112">If it can, then the AVI Decompressor is notified and it reconfigures MSYUV to operate in "pass-through mode," which causes the codec to skip the conversion and copy the YUV image data directly onto a DirectDraw overlay surface in video memory.</span></span>

<span data-ttu-id="f7daa-113">由於影片混合轉譯器 (VMR-7 和 VMR-9) 絕不會使用 GDI，因此在連接時不需要 RGB 類型，而且 MSYUV 色彩空間轉換器永遠不會在圖形中的 VMR 之前插入。</span><span class="sxs-lookup"><span data-stu-id="f7daa-113">Because the Video Mixing Renderers (VMR-7 and VMR-9) never use GDI, they do not require an RGB type at connect time, and the MSYUV Color Space Converter is never inserted before the VMR in a graph.</span></span>

<span data-ttu-id="f7daa-114">MSYUV 會將封裝的 YUV 格式轉換為 RGB，如下列清單所示：</span><span class="sxs-lookup"><span data-stu-id="f7daa-114">MSYUV converts packed YUV formats to RGB, as shown in the following list:</span></span>

-   <span data-ttu-id="f7daa-115">輸入格式： UYVY、YUY2、YVYU</span><span class="sxs-lookup"><span data-stu-id="f7daa-115">Input formats: UYVY, YUY2, YVYU</span></span>
-   <span data-ttu-id="f7daa-116">輸出格式： RGB 8、RGB 16、RGB 24、RGB 32</span><span class="sxs-lookup"><span data-stu-id="f7daa-116">Output formats: RGB 8, RGB 16, RGB 24, RGB 32</span></span>

<span data-ttu-id="f7daa-117">MSYUV 色彩空間轉換器編解碼器是視訊壓縮管理員 (BC-VCM-LVM-HYPERV) 編解碼器。</span><span class="sxs-lookup"><span data-stu-id="f7daa-117">The MSYUV Color Space Converter Codec is a Video Compression Manager (VCM) codec.</span></span> <span data-ttu-id="f7daa-118">它會透過 [AVI 解壓縮](avi-decompressor-filter.md) 程式篩選器用於 DirectShow 中。</span><span class="sxs-lookup"><span data-stu-id="f7daa-118">It is used in DirectShow through the [AVI Decompressor](avi-decompressor-filter.md) filter.</span></span> <span data-ttu-id="f7daa-119">若為更一般用途的色彩轉換器，請使用 [**色彩轉換器 DSP**](../medfound/colorconverter.md)。</span><span class="sxs-lookup"><span data-stu-id="f7daa-119">For a more general-purpose color converter, use the [**Color Converter DSP**](../medfound/colorconverter.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f7daa-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="f7daa-120">Requirements</span></span>



| <span data-ttu-id="f7daa-121">需求</span><span class="sxs-lookup"><span data-stu-id="f7daa-121">Requirement</span></span> | <span data-ttu-id="f7daa-122">值</span><span class="sxs-lookup"><span data-stu-id="f7daa-122">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f7daa-123">DLL</span><span class="sxs-lookup"><span data-stu-id="f7daa-123">DLL</span></span><br/> | <dl> <span data-ttu-id="f7daa-124"><dt>Msyuv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f7daa-124"><dt>Msyuv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7daa-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f7daa-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7daa-126">DirectShow 篩選</span><span class="sxs-lookup"><span data-stu-id="f7daa-126">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 

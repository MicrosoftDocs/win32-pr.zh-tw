---
description: DirectShow 影片捕獲篩選
ms.assetid: e4d1452d-ceac-4b5c-b9ba-ad4722ecff76
title: DirectShow 影片捕獲篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 238f18dd77bc40011fa9fc0dbab3192ea81a223f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467480"
---
# <a name="directshow-video-capture-filters"></a><span data-ttu-id="4ce75-103">DirectShow 影片捕獲篩選</span><span class="sxs-lookup"><span data-stu-id="4ce75-103">DirectShow Video Capture Filters</span></span>

<span data-ttu-id="4ce75-104">DirectShow 中的 Capture 濾波器有一些功能與其他種類的篩選器有所區別。</span><span class="sxs-lookup"><span data-stu-id="4ce75-104">Capture filters in DirectShow have some features that distinguish them from other kinds of filters.</span></span> <span data-ttu-id="4ce75-105">雖然「 [捕獲圖形](capture-graph-builder.md) 產生器」會隱藏許多詳細資料，但建議您閱讀這一節，以對 DirectShow 捕捉圖形有大致的瞭解。</span><span class="sxs-lookup"><span data-stu-id="4ce75-105">Although the [Capture Graph Builder](capture-graph-builder.md) hides many of the details, it is a good idea to read this section, in order to have a general understanding of DirectShow capture graphs.</span></span>

<span data-ttu-id="4ce75-106">**釘選類別**</span><span class="sxs-lookup"><span data-stu-id="4ce75-106">**Pin Categories**</span></span>

<span data-ttu-id="4ce75-107">Capture 濾波器通常有兩個以上的輸出圖釘可提供相同類型的資料，例如預覽 pin 和捕捉 pin。</span><span class="sxs-lookup"><span data-stu-id="4ce75-107">A capture filter often has two or more output pins that deliver the same kind of data—for example, a preview pin and a capture pin.</span></span> <span data-ttu-id="4ce75-108">因此，媒體類型並不適合用來區別 pin。</span><span class="sxs-lookup"><span data-stu-id="4ce75-108">Therefore, media types are not a good way to distinguish the pins.</span></span> <span data-ttu-id="4ce75-109">相反地，pin 會透過其功能來區別，其使用稱為 *pin 類別* 的 GUID 來識別。</span><span class="sxs-lookup"><span data-stu-id="4ce75-109">Instead, the pins are distinguished by their functionality, which is identified using a GUID, called the *pin category*.</span></span>

<span data-ttu-id="4ce75-110">如需如何針對其類別查詢 pin 的討論，請參閱 [使用釘選類別](working-with-pin-categories.md)。</span><span class="sxs-lookup"><span data-stu-id="4ce75-110">For a discussion of how to query pins for their category, see [Working with Pin Categories](working-with-pin-categories.md).</span></span> <span data-ttu-id="4ce75-111">不過，大部分的應用程式都不需要直接查詢 pin。</span><span class="sxs-lookup"><span data-stu-id="4ce75-111">For most applications, however, you will not have to query pins directly.</span></span> <span data-ttu-id="4ce75-112">相反地，不同的 [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) 方法會取得參數，以指定要在其上操作的釘選類別。</span><span class="sxs-lookup"><span data-stu-id="4ce75-112">Instead, various [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) methods take parameters that specify the pin category on which to operate.</span></span> <span data-ttu-id="4ce75-113">「捕獲圖形產生器」會自動尋找正確的 pin。</span><span class="sxs-lookup"><span data-stu-id="4ce75-113">The Capture Graph Builder automatically locates the correct pin.</span></span>

<span data-ttu-id="4ce75-114">**預覽釘選和捕捉釘**</span><span class="sxs-lookup"><span data-stu-id="4ce75-114">**Preview Pins and Capture Pins**</span></span>

<span data-ttu-id="4ce75-115">某些影片捕獲裝置有個別的輸出 pin 可供預覽和捕捉。</span><span class="sxs-lookup"><span data-stu-id="4ce75-115">Some video capture devices have separate output pins for preview and capture.</span></span> <span data-ttu-id="4ce75-116">預覽 pin 是用來在螢幕上呈現影片，而捕捉釘用來將影片寫入檔案。</span><span class="sxs-lookup"><span data-stu-id="4ce75-116">The preview pin is used to render video to the screen, while the capture pin is used to write video to a file.</span></span>

<span data-ttu-id="4ce75-117">預覽 pin 和捕捉 pin 有下列差異：</span><span class="sxs-lookup"><span data-stu-id="4ce75-117">A preview pin and a capture pin have the following differences:</span></span>

-   <span data-ttu-id="4ce75-118">預覽 pin 會視需要卸載框架，以維護捕捉釘選上的輸送量。</span><span class="sxs-lookup"><span data-stu-id="4ce75-118">A preview pin drops frames as needed to maintain throughput on the capture pin.</span></span>
-   <span data-ttu-id="4ce75-119">從捕捉釘選的每個畫面格都會加上時間戳記，並在框架被捕獲時提供串流時間。</span><span class="sxs-lookup"><span data-stu-id="4ce75-119">Each frame from a capture pin is time-stamped with the stream time when the frame was captured.</span></span> <span data-ttu-id="4ce75-120">預覽 pin 不會時間戳記所提供的範例。</span><span class="sxs-lookup"><span data-stu-id="4ce75-120">A preview pin does not time stamp the samples it delivers.</span></span>

<span data-ttu-id="4ce75-121">預覽框架沒有時間戳記的原因是，篩選圖形在串流中引進了少量的延遲。</span><span class="sxs-lookup"><span data-stu-id="4ce75-121">The reason that preview frames do not have time stamps is that the filter graph introduces a small amount of latency into the stream.</span></span> <span data-ttu-id="4ce75-122">如果將捕獲時間當做展示時間使用，則影片轉譯器會將每個樣本視為稍微延遲。</span><span class="sxs-lookup"><span data-stu-id="4ce75-122">If the capture time is used as the presentation time, the video renderer treats every sample as being slightly late.</span></span> <span data-ttu-id="4ce75-123">這可能會導致影片轉譯器在嘗試趕上時，卸載畫面格。</span><span class="sxs-lookup"><span data-stu-id="4ce75-123">This can cause the video renderer to drop frames while it tries to catch up.</span></span> <span data-ttu-id="4ce75-124">移除時間戳記可確保轉譯器會在到達時顯示每個範例，而不會卸載框架。</span><span class="sxs-lookup"><span data-stu-id="4ce75-124">Removing the time stamps ensures that the renderer presents each sample when it arrives, without dropping frames.</span></span>

<span data-ttu-id="4ce75-125">預覽 pin 的釘選類別為釘選 \_ 類別 \_ 預覽版。</span><span class="sxs-lookup"><span data-stu-id="4ce75-125">The pin category for preview pins is PIN\_CATEGORY\_PREVIEW.</span></span> <span data-ttu-id="4ce75-126">捕捉釘選的類別是釘選 \_ 類別 \_ 捕獲。</span><span class="sxs-lookup"><span data-stu-id="4ce75-126">The category for capture pins is PIN\_CATEGORY\_CAPTURE.</span></span>

<span data-ttu-id="4ce75-127">**影片埠釘選**</span><span class="sxs-lookup"><span data-stu-id="4ce75-127">**Video Port Pins**</span></span>

<span data-ttu-id="4ce75-128">影片埠是影片裝置 (（例如類比電視調諧器) 和視訊卡）之間的硬體連接。</span><span class="sxs-lookup"><span data-stu-id="4ce75-128">A video port is a hardware connection between a video device (such as an analog TV tuner) and the video card.</span></span> <span data-ttu-id="4ce75-129">影片埠可讓裝置將影片資料直接傳送至圖形配接器。</span><span class="sxs-lookup"><span data-stu-id="4ce75-129">A video port enables the device to send video data directly to the graphics card.</span></span> <span data-ttu-id="4ce75-130">影片會使用硬體重迭顯示在畫面上。</span><span class="sxs-lookup"><span data-stu-id="4ce75-130">The video is displayed on the screen using a hardware overlay.</span></span> <span data-ttu-id="4ce75-131">影片埠可能是在不同卡片上連接兩個裝置的實際纜線;或者，它可能是相同卡片上的硬式連接。</span><span class="sxs-lookup"><span data-stu-id="4ce75-131">A video port might be an actual cable that connects two devices on separate cards; or it might be a hard-wired connection on the same card.</span></span>

<span data-ttu-id="4ce75-132">影片埠的優點是影片會直接進入視訊記憶體，而不會有 CPU 的任何工作。</span><span class="sxs-lookup"><span data-stu-id="4ce75-132">The advantage of a video port is that the video goes directly into video memory, without any work by the CPU.</span></span> <span data-ttu-id="4ce75-133">不過，影片埠有一些缺點：</span><span class="sxs-lookup"><span data-stu-id="4ce75-133">However, video ports have some drawbacks:</span></span>

-   <span data-ttu-id="4ce75-134">無論您是否想要預覽影片，影片埠一律會在捕捉期間使用重迭表面。</span><span class="sxs-lookup"><span data-stu-id="4ce75-134">A video port always uses the overlay surface during capture, regardless of whether you want to preview the video.</span></span>
-   <span data-ttu-id="4ce75-135">系統會自動在畫面格之間進行切換，因此很難將翻轉與其他影片作業進行同步處理。</span><span class="sxs-lookup"><span data-stu-id="4ce75-135">Flipping between frames occurs automatically, which makes it difficult to synchronize the flip with other video operations.</span></span>

<span data-ttu-id="4ce75-136">如果捕捉裝置使用影片埠，則捕獲篩選器會有影片埠 pin，而不是預覽 pin。</span><span class="sxs-lookup"><span data-stu-id="4ce75-136">If a capture device uses a video port, the capture filter has a video port pin instead of a preview pin.</span></span> <span data-ttu-id="4ce75-137">影片埠 pin 的釘選類別是釘選 \_ 類別 \_ VIDEOPORT。</span><span class="sxs-lookup"><span data-stu-id="4ce75-137">The pin category for video port pins is PIN\_CATEGORY\_VIDEOPORT.</span></span>

<span data-ttu-id="4ce75-138">每個 capture 濾波器都至少有一個 capture pin。</span><span class="sxs-lookup"><span data-stu-id="4ce75-138">Every capture filter has at least one capture pin.</span></span> <span data-ttu-id="4ce75-139">此外，它可能會有預覽 pin 或影片埠 pin，但不能同時有兩者。</span><span class="sxs-lookup"><span data-stu-id="4ce75-139">In addition it might have a preview pin or a video port pin, but never both.</span></span> <span data-ttu-id="4ce75-140">篩選器可以有多個捕捉釘和預覽 pin，每個都提供不同的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="4ce75-140">Filters can have multiple capture pins and preview pins, each delivering a separate media type.</span></span> <span data-ttu-id="4ce75-141">因此，單一篩選器可能會有影片捕獲釘選、影片預覽釘選、音訊捕獲 pin 和音訊預覽 pin。</span><span class="sxs-lookup"><span data-stu-id="4ce75-141">Thus, a single filter could have a video capture pin, a video preview pin, an audio capture pin, and an audio preview pin.</span></span> <span data-ttu-id="4ce75-142">不過， (沒有適用于音訊的影片埠。 ) </span><span class="sxs-lookup"><span data-stu-id="4ce75-142">(There is nothing equivalent to a video port for audio, however.)</span></span>

<span data-ttu-id="4ce75-143">**上游 WDM 篩選**</span><span class="sxs-lookup"><span data-stu-id="4ce75-143">**Upstream WDM Filters**</span></span>

<span data-ttu-id="4ce75-144">Windows Driver Model (WDM) 裝置可能需要從 capture 篩選器上游的一些額外篩選準則。</span><span class="sxs-lookup"><span data-stu-id="4ce75-144">Windows Driver Model (WDM) devices may require some additional filters upstream from the capture filter.</span></span> <span data-ttu-id="4ce75-145">這些篩選器包括下列各項：</span><span class="sxs-lookup"><span data-stu-id="4ce75-145">These filters include the following:</span></span>

-   <span data-ttu-id="4ce75-146">[電視調諧器篩選器](tv-tuner-filter.md)。</span><span class="sxs-lookup"><span data-stu-id="4ce75-146">[TV Tuner Filter](tv-tuner-filter.md).</span></span> <span data-ttu-id="4ce75-147">控制類比 TV 調諧器的微調。</span><span class="sxs-lookup"><span data-stu-id="4ce75-147">Controls tuning for analog TV tuners.</span></span>
-   <span data-ttu-id="4ce75-148">[電視音訊篩選器](tv-audio-filter.md)。</span><span class="sxs-lookup"><span data-stu-id="4ce75-148">[TV Audio Filter](tv-audio-filter.md).</span></span> <span data-ttu-id="4ce75-149">控制類比 TV 調諧器的音訊設定。</span><span class="sxs-lookup"><span data-stu-id="4ce75-149">Controls audio settings for analog TV tuners.</span></span>
-   <span data-ttu-id="4ce75-150">[類比視頻縱橫條濾波器](analog-video-crossbar-filter.md)。</span><span class="sxs-lookup"><span data-stu-id="4ce75-150">[Analog Video Crossbar Filter](analog-video-crossbar-filter.md).</span></span> <span data-ttu-id="4ce75-151">透過硬體裝置路由傳送影片和音訊信號。</span><span class="sxs-lookup"><span data-stu-id="4ce75-151">Routes video and audio signals through the hardware device.</span></span> <span data-ttu-id="4ce75-152">例如，裝置可能會有多個輸入，例如 S-video 和複合影片。</span><span class="sxs-lookup"><span data-stu-id="4ce75-152">For example, a device might have multiple inputs, such as S-Video and composite video.</span></span> <span data-ttu-id="4ce75-153">縱橫比對篩選器可讓應用程式選取輸入。</span><span class="sxs-lookup"><span data-stu-id="4ce75-153">The crossbar filter enables the application to select the input.</span></span>

<span data-ttu-id="4ce75-154">雖然這些是 DirectShow 中的個別篩選器，但它們通常代表相同的硬體裝置。</span><span class="sxs-lookup"><span data-stu-id="4ce75-154">Although these are separate filters in DirectShow, they typically represent the same hardware device.</span></span> <span data-ttu-id="4ce75-155">每個篩選器會控制裝置的不同功能。</span><span class="sxs-lookup"><span data-stu-id="4ce75-155">Each filter controls a different function of the device.</span></span> <span data-ttu-id="4ce75-156">篩選是透過釘選，但不會在 pin 連線之間移動媒體資料。</span><span class="sxs-lookup"><span data-stu-id="4ce75-156">The filters are connected by pins, but no media data moves across the pin connections.</span></span> <span data-ttu-id="4ce75-157">因此，這些篩選器上的釘選不會藉由建立媒體類型來連接。</span><span class="sxs-lookup"><span data-stu-id="4ce75-157">Therefore, the pins on these filters do not connect by establishing a media type.</span></span> <span data-ttu-id="4ce75-158">相反地，它們會使用稱為 *媒體* 的 GUID 值。</span><span class="sxs-lookup"><span data-stu-id="4ce75-158">Instead, they use GUID values called *mediums*.</span></span> <span data-ttu-id="4ce75-159">系統會針對指定的裝置迷你驅動程式，唯一定義中等 Guid。</span><span class="sxs-lookup"><span data-stu-id="4ce75-159">Medium GUIDs are uniquely defined for a given device minidriver.</span></span> <span data-ttu-id="4ce75-160">例如，相同的電視視訊卡的電視調諧器篩選器和影片捕獲篩選器都支援相同的媒體，讓應用程式能夠正確地建立圖形。</span><span class="sxs-lookup"><span data-stu-id="4ce75-160">For example, the TV Tuner filter and the Video Capture filter for the same TV card will both support the same medium, which enables the application to build the graph correctly.</span></span>

<span data-ttu-id="4ce75-161">在實務上，只要您使用 **ICaptureGraphBuilder2** 來建立您的捕獲圖形，這些篩選器就會自動新增至圖形。</span><span class="sxs-lookup"><span data-stu-id="4ce75-161">In practice, as long as you are using **ICaptureGraphBuilder2** to build your capture graphs, these filters are added to the graph automatically.</span></span> <span data-ttu-id="4ce75-162">如需更詳細的討論，請參閱 [WDM 類別驅動程式篩選器](wdm-class-driver-filters.md)。</span><span class="sxs-lookup"><span data-stu-id="4ce75-162">For a more detailed discussion, see [WDM Class Driver Filters](wdm-class-driver-filters.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4ce75-163">相關主題</span><span class="sxs-lookup"><span data-stu-id="4ce75-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4ce75-164">關於 DirectShow 中的影片捕獲</span><span class="sxs-lookup"><span data-stu-id="4ce75-164">About Video Capture in DirectShow</span></span>](about-video-capture-in-directshow.md)
</dt> </dl>

 

 




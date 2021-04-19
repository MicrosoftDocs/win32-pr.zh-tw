---
description: 使用 Windows Media 視訊9螢幕編解碼器
ms.assetid: d88d5f5e-0935-4bbe-8abf-72cc536f9b40
title: '使用 Windows Media 視訊9螢幕編解碼器 (Microsoft 媒體基礎) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b825e053c4c732481c8d1ca5d4dc972f804f262a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106992633"
---
# <a name="using-the-windows-media-video-9-screen-codec-microsoft-media-foundation"></a><span data-ttu-id="31bce-103">使用 Windows Media 視訊9螢幕編解碼器 (Microsoft 媒體基礎) </span><span class="sxs-lookup"><span data-stu-id="31bce-103">Using the Windows Media Video 9 Screen Codec (Microsoft Media Foundation)</span></span>

<span data-ttu-id="31bce-104">Windows Media 視訊9畫面編解碼器已針對壓縮 *應用程式影片* 進行優化，其中包含電腦顯示的連續螢幕擷取畫面。</span><span class="sxs-lookup"><span data-stu-id="31bce-104">The Windows Media Video 9 Screen codec is optimized for compressing *application video*, which consists of consecutive screen shots for a computer display.</span></span> <span data-ttu-id="31bce-105">編解碼器會利用一般的影像簡單性 (相對較少的色彩、大量的直線等等) 和相對缺乏的動作，以達到非常高的壓縮比率。</span><span class="sxs-lookup"><span data-stu-id="31bce-105">The codec takes advantage of the typical image simplicity (relatively few colors, lots of straight lines, and so on) and relative lack of motion to achieve a very high compression ratio.</span></span> <span data-ttu-id="31bce-106">這項優化的缺點是不符合應用程式影片預期特性的影片，可能很難以可接受的品質層級進行壓縮。</span><span class="sxs-lookup"><span data-stu-id="31bce-106">The disadvantage of this optimization is that video that doesn't conform to the expected characteristics of application video can be difficult to compress with an acceptable level of quality.</span></span>

<span data-ttu-id="31bce-107">Windows Media 視訊9螢幕編碼程式是由類別識別碼 CLSID CMSSEncMediaObject2 來識別 \_ ，而此解碼器會識別出類別識別碼 clsid \_ CMSSDecMediaObject。</span><span class="sxs-lookup"><span data-stu-id="31bce-107">The Windows Media Video 9 Screen encoder is identified by the class identifier CLSID\_CMSSEncMediaObject2, and the decoder is identified the class identifier CLSID\_CMSSDecMediaObject.</span></span> <span data-ttu-id="31bce-108">使用此編解碼器之媒體類型的 FOURCC 值為 "MSS2"。</span><span class="sxs-lookup"><span data-stu-id="31bce-108">The FOURCC value for media types using this codec is "MSS2".</span></span>

## <a name="configuring-the-encoder"></a><span data-ttu-id="31bce-109">設定編碼器</span><span class="sxs-lookup"><span data-stu-id="31bce-109">Configuring the Encoder</span></span>

<span data-ttu-id="31bce-110">Windows Media 視訊9畫面編解碼器的編碼器的設定方式與標準視頻編碼器相同。</span><span class="sxs-lookup"><span data-stu-id="31bce-110">The encoder of the Windows Media Video 9 Screen codec is configured in the same way as the standard video decoder.</span></span>

> [!Note]  
> <span data-ttu-id="31bce-111">螢幕編碼器只支援一次傳遞編碼。</span><span class="sxs-lookup"><span data-stu-id="31bce-111">The screen encoder supports only one-pass encoding.</span></span> <span data-ttu-id="31bce-112">您可以將 [MFPKEY \_ PASSESUSED](mfpkey-passesusedproperty.md) 屬性設定為2，並處理輸入兩次，而不會發生錯誤，但是這樣做並沒有任何好處。</span><span class="sxs-lookup"><span data-stu-id="31bce-112">You can set the [MFPKEY\_PASSESUSED](mfpkey-passesusedproperty.md) property to 2 and process the inputs twice without error, but there is no benefit to doing so.</span></span> <span data-ttu-id="31bce-113">這是已知的問題，可能會在未來的版本中修正。</span><span class="sxs-lookup"><span data-stu-id="31bce-113">This is a known issue and may be corrected in future releases.</span></span>

 

## <a name="getting-the-best-results"></a><span data-ttu-id="31bce-114">取得最佳結果</span><span class="sxs-lookup"><span data-stu-id="31bce-114">Getting the Best Results</span></span>

<span data-ttu-id="31bce-115">如果您在螢幕擷取畫面內容中發現您想要的品質，需要比您用於傳遞案例更高的位元速率，您可以嘗試下列技巧以從編解碼器獲得更高的效率：</span><span class="sxs-lookup"><span data-stu-id="31bce-115">If you discover that the quality you want in your screen capture content requires a higher bit rate than you can use for your delivery scenario, you can try the following techniques to get more efficiency from the codec:</span></span>

-   <span data-ttu-id="31bce-116">針對螢幕擷取畫面使用較小的解析度。</span><span class="sxs-lookup"><span data-stu-id="31bce-116">Use a smaller resolution for the screen capture.</span></span> <span data-ttu-id="31bce-117">若要取得比所需更大的螢幕解析度，可以藉由呈現不必要的資訊來混淆檢視器。</span><span class="sxs-lookup"><span data-stu-id="31bce-117">Capturing a larger screen resolution than needed can confuse the viewer by presenting unnecessary information.</span></span>
-   <span data-ttu-id="31bce-118">使用較慢的畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="31bce-118">Use a slower frame rate.</span></span> <span data-ttu-id="31bce-119">螢幕捕捉通常會以極低的畫面播放速率來有效 (有時每秒4或5個畫面格) 。</span><span class="sxs-lookup"><span data-stu-id="31bce-119">Screen captures can often be effective at very low frame rates (sometimes as low as 4 or 5 frames per second).</span></span>
-   <span data-ttu-id="31bce-120">在螢幕擷取畫面中使用較少的圖形。</span><span class="sxs-lookup"><span data-stu-id="31bce-120">Use fewer graphics in the screen capture.</span></span> <span data-ttu-id="31bce-121">Windows Media 視訊9畫面編解碼器經過優化，可將 Windows 基本專案和高品質的文字編碼。</span><span class="sxs-lookup"><span data-stu-id="31bce-121">The Windows Media Video 9 Screen codec is optimized to encode Windows primitives and text with high quality.</span></span> <span data-ttu-id="31bce-122">通常是因為點陣圖圖形所造成的問題，這些圖形通常包含數以千計的個人色彩。</span><span class="sxs-lookup"><span data-stu-id="31bce-122">Usually problems occur because of bitmapped graphics, which often contain thousands of individual colors.</span></span> <span data-ttu-id="31bce-123">當您捕捉時，螢幕上的點陣圖越少，結果就越好。</span><span class="sxs-lookup"><span data-stu-id="31bce-123">The fewer bitmaps that are on the screen when you capture, the better your results will be.</span></span> <span data-ttu-id="31bce-124">如果您無法從螢幕擷取畫面中排除圖形，有數種方式可以將點陣圖對影像品質的影響降至最低：</span><span class="sxs-lookup"><span data-stu-id="31bce-124">If you cannot eliminate graphics from your screen capture, there are several ways to minimize the impact that a bitmap has on image quality:</span></span>
    -   <span data-ttu-id="31bce-125">縮小圖形的大小。</span><span class="sxs-lookup"><span data-stu-id="31bce-125">Reduce the size of the graphic.</span></span>
    -   <span data-ttu-id="31bce-126">減少同時出現在螢幕上的個別圖形數目。</span><span class="sxs-lookup"><span data-stu-id="31bce-126">Reduce the number of individual graphics that appear on the screen at the same time.</span></span>
    -   <span data-ttu-id="31bce-127">減少圖形的移動量。</span><span class="sxs-lookup"><span data-stu-id="31bce-127">Reduce the amount of movement of the graphic.</span></span> <span data-ttu-id="31bce-128">例如，如果圖形是在視窗中，請盡可能讓視窗保持固定。</span><span class="sxs-lookup"><span data-stu-id="31bce-128">For example, if the graphic is in a window, keep the window as stationary as possible.</span></span>
    -   <span data-ttu-id="31bce-129">避免將滑鼠指標移到圖形上，或將視窗或其他元素拖曳到圖形上。</span><span class="sxs-lookup"><span data-stu-id="31bce-129">Avoid moving the mouse pointer over the graphic, or dragging windows or other elements over the graphic.</span></span>

## <a name="decoding"></a><span data-ttu-id="31bce-130">解碼</span><span class="sxs-lookup"><span data-stu-id="31bce-130">Decoding</span></span>

<span data-ttu-id="31bce-131">解碼螢幕擷取畫面影片沒有特殊需求。</span><span class="sxs-lookup"><span data-stu-id="31bce-131">There are no special requirements for decoding screen capture video.</span></span> <span data-ttu-id="31bce-132">不過，如同所有 Windows Media 視訊9編解碼器，螢幕擷取畫面解碼器無法在沒有編解碼器私用資料的情況下正確解壓縮編碼的內容。</span><span class="sxs-lookup"><span data-stu-id="31bce-132">However, as with all Windows Media Video 9 codecs, the screen capture decoder cannot properly decompress the encoded content without the codec private data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="31bce-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="31bce-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="31bce-134">設定影片編碼</span><span class="sxs-lookup"><span data-stu-id="31bce-134">Configuring Video Encoding</span></span>](configuringvideoencoding.md)
</dt> <dt>

[<span data-ttu-id="31bce-135">使用影片編解碼器私用資料</span><span class="sxs-lookup"><span data-stu-id="31bce-135">Using Video Codec Private Data</span></span>](usingvideocodecprivatedata.md)
</dt> <dt>

[<span data-ttu-id="31bce-136">Windows Media 視訊9螢幕編碼器</span><span class="sxs-lookup"><span data-stu-id="31bce-136">Windows Media Video 9 Screen Encoder</span></span>](windowsmediavideo9screenencoder.md)
</dt> <dt>

[<span data-ttu-id="31bce-137">使用影片</span><span class="sxs-lookup"><span data-stu-id="31bce-137">Working with Video</span></span>](workingwithvideo.md)
</dt> </dl>

 

 




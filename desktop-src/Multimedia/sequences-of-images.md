---
title: 影像的順序
description: 影像的順序
ms.assetid: fbfb944c-a927-4c92-b3d6-2f8c278408e6
keywords:
- DrawDib，映射序列
- DrawDib，點陣圖順序
- DrawDibDraw 函式
- DrawDibBegin 函式
- DrawDibEnd 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a7ae2c85d62e93e4149518221aa520eabe13ee2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106968490"
---
# <a name="sequences-of-images"></a><span data-ttu-id="f3cf5-108">影像的順序</span><span class="sxs-lookup"><span data-stu-id="f3cf5-108">Sequences of Images</span></span>

<span data-ttu-id="f3cf5-109">您可以搭配使用 [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) 函式和 [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) 函式，以顯示具有相同維度和格式的一系列點陣圖。</span><span class="sxs-lookup"><span data-stu-id="f3cf5-109">You can display a sequence of bitmaps with the same dimensions and formats by using the [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) function with the [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) function.</span></span> <span data-ttu-id="f3cf5-110">**DrawDibBegin** 藉由準備 DrawDib DC 來進行繪製，以改善 **DrawDibDraw** 的效率。</span><span class="sxs-lookup"><span data-stu-id="f3cf5-110">**DrawDibBegin** improves the efficiency of **DrawDibDraw** by preparing the DrawDib DC for drawing.</span></span>

> [!Note]  
> <span data-ttu-id="f3cf5-111">如果您的應用程式不使用 [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin)， [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) 會在繪製之前隱含地執行。</span><span class="sxs-lookup"><span data-stu-id="f3cf5-111">If your application does not use [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin), [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) implicitly executes it prior to drawing.</span></span> <span data-ttu-id="f3cf5-112">如果您的應用程式在 **DrawDibDraw** 之前使用 **DrawDibBegin** ， **DrawDibDraw** 就不需要處理函式並等候它完成。</span><span class="sxs-lookup"><span data-stu-id="f3cf5-112">If your application uses **DrawDibBegin** prior to **DrawDibDraw**, **DrawDibDraw** does not have to process the function and wait for it to complete.</span></span>

 

<span data-ttu-id="f3cf5-113">[**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin)函式會為 [**DRAWDIBDRAW**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw)提供 DrawDib DC、DC 控制碼、 [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader)結構的位址，以及來源和目的地矩形維度。</span><span class="sxs-lookup"><span data-stu-id="f3cf5-113">The [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) function provides [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) with the DrawDib DC, the DC handle, the address of the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure, and the source and destination rectangle dimensions.</span></span> <span data-ttu-id="f3cf5-114">當您顯示一系列的點陣圖時， **DrawDibDraw** 會針對序列中的每個影像檢查這些專案的值。</span><span class="sxs-lookup"><span data-stu-id="f3cf5-114">When you display a sequence of bitmaps, **DrawDibDraw** checks the values of these items for each image in the sequence.</span></span> <span data-ttu-id="f3cf5-115">如果 **DrawDibDraw** 偵測到任何這些專案的變更，它會隱含地再次呼叫 **DrawDibBegin** 來調整 DrawDib DC 設定。</span><span class="sxs-lookup"><span data-stu-id="f3cf5-115">If **DrawDibDraw** detects changes to any of these items, it implicitly calls **DrawDibBegin** again to adjust the DrawDib DC settings.</span></span>

<span data-ttu-id="f3cf5-116">使用 [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin)之後，您可以使用 [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) 並適當地指定一或多個旗標，以繪製影像順序。</span><span class="sxs-lookup"><span data-stu-id="f3cf5-116">After using [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin), you can draw the image sequence by using [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) and specifying one or more flags as appropriate.</span></span> <span data-ttu-id="f3cf5-117">指定 **DDF \_ 相同的 \_ HDC** 旗標，但 DC 控制碼未變更。</span><span class="sxs-lookup"><span data-stu-id="f3cf5-117">Specify the **DDF\_SAME\_HDC** flag as long as the DC handle has not changed.</span></span> <span data-ttu-id="f3cf5-118">\_ \_ 當下列 **DrawDibDraw** 參數未變更時，請指定 DDF 相同的繪圖旗標： [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader)結構的位址和來源和目的矩形維度。</span><span class="sxs-lookup"><span data-stu-id="f3cf5-118">Specify the DDF\_SAME\_DRAW flag when the following parameters for **DrawDibDraw** have not changed: the address of the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure and the source and destination rectangle dimensions.</span></span>

<span data-ttu-id="f3cf5-119">您可以使用 [**DrawDibEnd**](/windows/desktop/api/Vfw/nf-vfw-drawdibend)函數，然後再呼叫 **DrawDibBegin**，以更新使用 [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin)設定的旗標。</span><span class="sxs-lookup"><span data-stu-id="f3cf5-119">You can update the flags set with [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) by using the [**DrawDibEnd**](/windows/desktop/api/Vfw/nf-vfw-drawdibend) function followed by another call to **DrawDibBegin**.</span></span> <span data-ttu-id="f3cf5-120">然後使用 **DrawDibEnd** 清除其目前旗標和設定的 DrawDib DC。</span><span class="sxs-lookup"><span data-stu-id="f3cf5-120">Then use **DrawDibEnd** to clear the DrawDib DC of its current flags and settings.</span></span> <span data-ttu-id="f3cf5-121">後續的 **DrawDibBegin** 呼叫會重新初始化具有適當旗標和設定的 DrawDib DC。</span><span class="sxs-lookup"><span data-stu-id="f3cf5-121">The subsequent call to **DrawDibBegin** reinitializes the DrawDib DC with the appropriate flags and settings.</span></span> <span data-ttu-id="f3cf5-122">或者，您可以使用 **DrawDibBegin** 而不 **DrawDibEnd** 來更新 DrawDib DC 的旗標。</span><span class="sxs-lookup"><span data-stu-id="f3cf5-122">Alternatively, you can update the flags for a DrawDib DC by using **DrawDibBegin** without **DrawDibEnd**.</span></span> <span data-ttu-id="f3cf5-123">若要這樣做，您必須同時變更下列其中一項設定： [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) 結構的位址，或是來源或目的矩形維度。</span><span class="sxs-lookup"><span data-stu-id="f3cf5-123">To do this, you must change at least one of the following settings concurrently with the flags: the address of the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure, or the source or destination rectangle dimensions.</span></span>

<span data-ttu-id="f3cf5-124">您可以使用 [**DrawDibStart**](/windows/desktop/api/Vfw/nf-vfw-drawdibstart)和 [**DrawDibStop**](/windows/desktop/api/Vfw/nf-vfw-drawdibstop)函式，來提高使用壓縮影像（例如播放影片剪輯）之資料串流作業的 [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw)效率。</span><span class="sxs-lookup"><span data-stu-id="f3cf5-124">You can increase the efficiency of [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) for data-streaming operations that use compressed images, such as playing a video clip, by using the [**DrawDibStart**](/windows/desktop/api/Vfw/nf-vfw-drawdibstart) and [**DrawDibStop**](/windows/desktop/api/Vfw/nf-vfw-drawdibstop) functions.</span></span> <span data-ttu-id="f3cf5-125">**DrawDibStart** 函式會將訊息傳送至視訊壓縮管理員 (bc-vcm-lvm-hyperv) ，以準備 DrawDib DC 以接收影像的資料流程。</span><span class="sxs-lookup"><span data-stu-id="f3cf5-125">The **DrawDibStart** function prepares the DrawDib DC to receive a stream of images by sending a message to the video compression manager (VCM).</span></span> <span data-ttu-id="f3cf5-126">當串流結束時， **DrawDibStop** 會將訊息傳送至 bc-vcm-lvm-hyperv，指出它可以釋放為數據串流作業所配置的資源。</span><span class="sxs-lookup"><span data-stu-id="f3cf5-126">When streaming has ended, **DrawDibStop** sends a message to VCM indicating that it can release resources it allocated for the data-streaming operation.</span></span> <span data-ttu-id="f3cf5-127">如需 BC-VCM-LVM-HYPERV 的詳細資訊，請參閱 [影片壓縮管理員](video-compression-manager.md)。</span><span class="sxs-lookup"><span data-stu-id="f3cf5-127">For more information about VCM, see [Video Compression Manager](video-compression-manager.md).</span></span>

> [!Note]  
> <span data-ttu-id="f3cf5-128">您必須在應用程式中指定來源和目的地矩形的寬度和高度。</span><span class="sxs-lookup"><span data-stu-id="f3cf5-128">You must specify the width and height of the source and destination rectangles in your application.</span></span> <span data-ttu-id="f3cf5-129">不過，您不需要指定矩形的來源。</span><span class="sxs-lookup"><span data-stu-id="f3cf5-129">However, you do not need to specify the origins of the rectangles.</span></span> <span data-ttu-id="f3cf5-130">您的應用程式可以在 [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) 中重新定義來源，以使用影像的不同部分或更新顯示的不同部分。</span><span class="sxs-lookup"><span data-stu-id="f3cf5-130">Your application can redefine the origins in [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) to use different portions of the image or to update different portions of the display.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="f3cf5-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="f3cf5-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f3cf5-132">影像轉譯</span><span class="sxs-lookup"><span data-stu-id="f3cf5-132">Image Rendering</span></span>](image-rendering.md)
</dt> </dl>

 

 
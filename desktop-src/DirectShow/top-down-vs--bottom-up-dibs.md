---
description: Top-Down 與
ms.assetid: c292f145-f385-4f18-8f98-e414d86860e2
title: Top-Down 與 Bottom-Up Dib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e719bea5923aeccc4a0a92b5f73a253e13d2e12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106969403"
---
# <a name="top-down-vs-bottom-up-dibs"></a><span data-ttu-id="2e0c2-103">Top-Down 與 Bottom-Up Dib</span><span class="sxs-lookup"><span data-stu-id="2e0c2-103">Top-Down vs. Bottom-Up DIBs</span></span>

<span data-ttu-id="2e0c2-104">如果您不熟悉圖形程式設計，您可能會預期點陣圖會排列在記憶體中，讓影像的頂端列出現在緩衝區的開頭，後面接著下一個資料列等等。</span><span class="sxs-lookup"><span data-stu-id="2e0c2-104">If you are new to graphics programming, you might expect that a bitmap would be arranged in memory so that the top row of the image appeared at the start of the buffer, followed by the next row, and so forth.</span></span> <span data-ttu-id="2e0c2-105">不過，這不一定是如此。</span><span class="sxs-lookup"><span data-stu-id="2e0c2-105">However, this is not necessarily the case.</span></span> <span data-ttu-id="2e0c2-106">在 Windows 中，與裝置無關的點陣圖 (Dib) 可以放在記憶體中，以兩種不同的方向（上下排列）。</span><span class="sxs-lookup"><span data-stu-id="2e0c2-106">In Windows, device-independent bitmaps (DIBs) can be placed in memory in two different orientations, bottom-up and top-down.</span></span>

<span data-ttu-id="2e0c2-107">在下一個 DIB 中，影像緩衝區是以圖元的底部列開始，後面接著下一個資料列，依此類推。</span><span class="sxs-lookup"><span data-stu-id="2e0c2-107">In a bottom-up DIB, the image buffer starts with the bottom row of pixels, followed by the next row up, and so forth.</span></span> <span data-ttu-id="2e0c2-108">影像的頂端資料列是緩衝區中的最後一個資料列。</span><span class="sxs-lookup"><span data-stu-id="2e0c2-108">The top row of the image is the last row in the buffer.</span></span> <span data-ttu-id="2e0c2-109">因此，記憶體中的第一個位元組是影像的左下角圖元。</span><span class="sxs-lookup"><span data-stu-id="2e0c2-109">Therefore, the first byte in memory is the bottom-left pixel of the image.</span></span> <span data-ttu-id="2e0c2-110">在 GDI 中，所有 Dib 都是自下而上的。</span><span class="sxs-lookup"><span data-stu-id="2e0c2-110">In GDI, all DIBs are bottom-up.</span></span> <span data-ttu-id="2e0c2-111">下圖顯示最下層 DIB 的實體版面配置。</span><span class="sxs-lookup"><span data-stu-id="2e0c2-111">The following diagram shows the physical layout of a bottom-up DIB.</span></span>

![右下角的 dib](images/pixel-layout-bottomup.png)

<span data-ttu-id="2e0c2-113">在由上而下的 DIB 中，資料列的順序會反轉。</span><span class="sxs-lookup"><span data-stu-id="2e0c2-113">In a top-down DIB, the order of the rows is reversed.</span></span> <span data-ttu-id="2e0c2-114">影像的頂端資料列是記憶體中的第一個資料列，後面接著下一個資料列。</span><span class="sxs-lookup"><span data-stu-id="2e0c2-114">The top row of the image is the first row in memory, followed by the next row down.</span></span> <span data-ttu-id="2e0c2-115">影像的底部資料列是緩衝區中的最後一個資料列。</span><span class="sxs-lookup"><span data-stu-id="2e0c2-115">The bottom row of the image is the last row in the buffer.</span></span> <span data-ttu-id="2e0c2-116">使用由上而下的 DIB 時，記憶體中的第一個位元組是影像的左上角圖元。</span><span class="sxs-lookup"><span data-stu-id="2e0c2-116">With a top-down DIB, the first byte in memory is the top-left pixel of the image.</span></span> <span data-ttu-id="2e0c2-117">DirectDraw 使用由上而下的 Dib。</span><span class="sxs-lookup"><span data-stu-id="2e0c2-117">DirectDraw uses top-down DIBs.</span></span> <span data-ttu-id="2e0c2-118">下圖顯示由上而下 DIB 的實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="2e0c2-118">The following diagram shows the physical layout of a top-down DIB:</span></span>

![由上而下的 dib](images/pixel-layout-topdown.png)

<span data-ttu-id="2e0c2-120">若為 RGB Dib，影像方向會以 [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader)結構的 **biHeight** 成員來表示。</span><span class="sxs-lookup"><span data-stu-id="2e0c2-120">For RGB DIBs, the image orientation is indicated by the **biHeight** member of the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure.</span></span> <span data-ttu-id="2e0c2-121">如果 **biHeight** 是正面的，則影像會靠下。</span><span class="sxs-lookup"><span data-stu-id="2e0c2-121">If **biHeight** is positive, the image is bottom-up.</span></span> <span data-ttu-id="2e0c2-122">如果 **biHeight** 為負數，則影像會由上而下。</span><span class="sxs-lookup"><span data-stu-id="2e0c2-122">If **biHeight** is negative, the image is top-down.</span></span>

<span data-ttu-id="2e0c2-123">YUV 格式的 Dib 一律會由上而下，而且會忽略 **biHeight** 成員的正負號。</span><span class="sxs-lookup"><span data-stu-id="2e0c2-123">DIBs in YUV formats are always top-down, and the sign of the **biHeight** member is ignored.</span></span> <span data-ttu-id="2e0c2-124">您應以正面的 **biHeight** 提供 yuv 格式，但它們也應接受具有負面 **biHeight** 的 yuv 格式並忽略符號。</span><span class="sxs-lookup"><span data-stu-id="2e0c2-124">Decoders should offer YUV formats with positive **biHeight**, but they should also accept YUV formats with negative **biHeight** and ignore the sign.</span></span>

<span data-ttu-id="2e0c2-125">此外，任何在 **biCompression** 成員中使用 **FOURCC** 的 DIB 型別，都應該將其 **biHeight** 表達為正數，無論其方向為何，因為 **FOURCC** 本身會識別其影像方向應該由任何相容的篩選器瞭解的壓縮配置。</span><span class="sxs-lookup"><span data-stu-id="2e0c2-125">Also, any DIB type that uses a **FOURCC** in the **biCompression** member, should express its **biHeight** as a positive number no matter what its orientation is, since the **FOURCC** itself identifies a compression scheme whose image orientation should be understood by any compatible filter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2e0c2-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="2e0c2-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2e0c2-127">使用影片畫面</span><span class="sxs-lookup"><span data-stu-id="2e0c2-127">Working with Video Frames</span></span>](working-with-video-frames.md)
</dt> </dl>

 

 




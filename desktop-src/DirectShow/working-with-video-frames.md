---
description: 使用影片畫面
ms.assetid: a5ad74dd-abfd-4810-a512-42e4b98a6c59
title: 使用影片畫面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ead597fac5a28befc9c9868485840d03b46e5185
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987578"
---
# <a name="working-with-video-frames"></a><span data-ttu-id="58619-103">使用影片畫面</span><span class="sxs-lookup"><span data-stu-id="58619-103">Working with Video Frames</span></span>

<span data-ttu-id="58619-104">未壓縮的影片是快速連續播放的一系列點陣圖，通常是每秒大約30個畫面格的速率。</span><span class="sxs-lookup"><span data-stu-id="58619-104">Uncompressed video is a sequence of bitmaps played in rapid succession, typically at a rate of about 30 frames per second.</span></span> <span data-ttu-id="58619-105">因為大部分的影片都會進入壓縮格式的 DirectShow 篩選圖形，所以影片串流通常會通過用於解壓縮的解碼器。</span><span class="sxs-lookup"><span data-stu-id="58619-105">Because most video enters a DirectShow filter graph in a compressed format, the video stream generally goes through a decoder for decompression.</span></span> <span data-ttu-id="58619-106">許多的解碼器都會以 YUV 格式輸出資料，並在轉譯之前，將最後轉換成 RGB 的影片硬體。</span><span class="sxs-lookup"><span data-stu-id="58619-106">Many decoders output data in a YUV format and leave the final conversion to RGB for the video hardware just prior to rendering.</span></span> <span data-ttu-id="58619-107">如果解碼器使用 DirectX Video 加速，則影片硬體會執行額外的工作來將映射解碼。</span><span class="sxs-lookup"><span data-stu-id="58619-107">If a decoder uses DirectX Video Acceleration, the video hardware performs additional work to decode the image.</span></span> <span data-ttu-id="58619-108">因此，在資料到達影片硬體之前，可能不會執行點陣圖的最終解壓縮。</span><span class="sxs-lookup"><span data-stu-id="58619-108">Thus, final decompression of the bitmaps may not be performed until the data reaches the video hardware.</span></span>

<span data-ttu-id="58619-109">但是，若要執行許多類型的影片分析、處理或編輯，通常必須使用某種 RGB 或 YUV 格式的未壓縮點陣圖，才能轉譯或寫入至檔案。</span><span class="sxs-lookup"><span data-stu-id="58619-109">But to perform many types of video analysis, processing, or editing, it is often necessary to work on uncompressed bitmaps in some type of RGB or YUV format before they are rendered or written to file.</span></span> <span data-ttu-id="58619-110">這項工作通常是在以 [**CTransformFilter**](ctransformfilter.md) 基類為基礎的轉換篩選準則中完成，特別是在 **轉換** 方法中。</span><span class="sxs-lookup"><span data-stu-id="58619-110">This work is typically done within a transform filter based on the [**CTransformFilter**](ctransformfilter.md) base class, specifically in the **Transform** method.</span></span> <span data-ttu-id="58619-111">這個方法會接收封裝影片資料之 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="58619-111">This method receives a pointer to an [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) object that encapsulates the video data.</span></span> <span data-ttu-id="58619-112">**IMediaSample：： GetPointer** 方法會傳回原始資料之第一個位元組的指標。</span><span class="sxs-lookup"><span data-stu-id="58619-112">The **IMediaSample::GetPointer** method returns a pointer to the first byte of the raw data.</span></span> <span data-ttu-id="58619-113">針對未壓縮的框架，此資料包含可由篩選準則直接存取或修改的圖元。</span><span class="sxs-lookup"><span data-stu-id="58619-113">For uncompressed frames, this data consists of pixels that can be accessed or modified directly by the filter.</span></span> <span data-ttu-id="58619-114">下列各節提供的背景資訊可協助您以這種方式有效地使用 DIB 資料。</span><span class="sxs-lookup"><span data-stu-id="58619-114">The following sections provide background information that will help you work effectively with DIB data in this manner.</span></span>

> [!Note]  
> <span data-ttu-id="58619-115">您也可以使用 GDI、GDI +、DirectDraw 或 Direct3D 函數來修改位，但這些技術已超出本文的範圍。</span><span class="sxs-lookup"><span data-stu-id="58619-115">You can also modify the bits by using GDI, GDI+, DirectDraw or Direct3D functions, but these techniques are beyond the scope of this article.</span></span>

 

<span data-ttu-id="58619-116">本節包含下列主題：</span><span class="sxs-lookup"><span data-stu-id="58619-116">This section contains the following topics:</span></span>

-   [<span data-ttu-id="58619-117">由上而下與 Bottom-Up Dib</span><span class="sxs-lookup"><span data-stu-id="58619-117">Top-Down vs. Bottom-Up DIBs</span></span>](top-down-vs--bottom-up-dibs.md)
-   [<span data-ttu-id="58619-118">使用16位 RGB</span><span class="sxs-lookup"><span data-stu-id="58619-118">Working with 16-bit RGB</span></span>](working-with-16-bit-rgb.md)

 

 




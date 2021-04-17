---
description: 影像 Stride
ms.assetid: 13cd1106-48b3-4522-ac09-8efbaab5c31d
title: 影像 Stride
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 813c0f3d99297758761bdfb5973fc2b16e3339f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104558381"
---
# <a name="image-stride"></a><span data-ttu-id="fa5b4-103">影像 Stride</span><span class="sxs-lookup"><span data-stu-id="fa5b4-103">Image Stride</span></span>

<span data-ttu-id="fa5b4-104">當影片影像儲存在記憶體中時，記憶體緩衝區可能會在每個圖元資料列之後包含額外的填補位元組。</span><span class="sxs-lookup"><span data-stu-id="fa5b4-104">When a video image is stored in memory, the memory buffer might contain extra padding bytes after each row of pixels.</span></span> <span data-ttu-id="fa5b4-105">填補位元組會影響影像儲存在記憶體中的方式，但不會影響影像的顯示方式。</span><span class="sxs-lookup"><span data-stu-id="fa5b4-105">The padding bytes affect how the image is stored in memory, but do not affect how the image is displayed.</span></span>

<span data-ttu-id="fa5b4-106">*Stride* 是記憶體中一個圖元的位元組數，以及記憶體中的下一個資料列。</span><span class="sxs-lookup"><span data-stu-id="fa5b4-106">The *stride* is the number of bytes from one row of pixels in memory to the next row of pixels in memory.</span></span> <span data-ttu-id="fa5b4-107">Stride 也稱為「 *音調*」。</span><span class="sxs-lookup"><span data-stu-id="fa5b4-107">Stride is also called *pitch*.</span></span> <span data-ttu-id="fa5b4-108">如果有填補位元組存在，stride 的寬度會比影像的寬度更寬，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="fa5b4-108">If padding bytes are present, the stride is wider than the width of the image, as shown in the following illustration.</span></span>

![顯示影像加上填補的圖表。](images/c85c6a40-f0a8-48a3-b465-39ceada66339.gif)

<span data-ttu-id="fa5b4-110">包含有相等維度之影片框架的兩個緩衝區可以有兩個不同的進展。</span><span class="sxs-lookup"><span data-stu-id="fa5b4-110">Two buffers that contain video frames with equal dimensions can have two different strides.</span></span> <span data-ttu-id="fa5b4-111">如果您處理影片影像，您必須將 stride 列入考慮。</span><span class="sxs-lookup"><span data-stu-id="fa5b4-111">If you process a video image, you must take the stride into account.</span></span>

<span data-ttu-id="fa5b4-112">此外，也有兩種方式可將影像排列在記憶體中。</span><span class="sxs-lookup"><span data-stu-id="fa5b4-112">In addition, there are two ways that an image can be arranged in memory.</span></span> <span data-ttu-id="fa5b4-113">在由 *上而下* 的影像中，影像中最上層的圖元會先出現在記憶體中。</span><span class="sxs-lookup"><span data-stu-id="fa5b4-113">In a *top-down* image, the top row of pixels in the image appears first in memory.</span></span> <span data-ttu-id="fa5b4-114">在 *下* 圖中，最後一列的圖元會先出現在記憶體中。</span><span class="sxs-lookup"><span data-stu-id="fa5b4-114">In a *bottom-up* image, the last row of pixels appears first in memory.</span></span> <span data-ttu-id="fa5b4-115">下圖顯示由上而下的影像與底部影像之間的差異。</span><span class="sxs-lookup"><span data-stu-id="fa5b4-115">The following illustration shows the difference between a top-down image and a bottom-up image.</span></span>

![顯示頂端和底部影像的圖表。](images/f03bd9ff-0cf3-4a56-88c5-5b8c44637272.gif)

<span data-ttu-id="fa5b4-117">底部的影像有負面的跨距，因為會將 stride 定義為相對於顯示的影像，需要向下移動圖元資料列的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="fa5b4-117">A bottom-up image has a negative stride, because stride is defined as the number of bytes need to move down a row of pixels, relative to the displayed image.</span></span> <span data-ttu-id="fa5b4-118">YUV 影像應該一律是由上而下，而且 Direct3D 介面中包含的任何影像都必須由上而下。</span><span class="sxs-lookup"><span data-stu-id="fa5b4-118">YUV images should always be top-down, and any image that is contained in a Direct3D surface must be top-down.</span></span> <span data-ttu-id="fa5b4-119">系統記憶體中的 RGB 影像通常是自下而上的。</span><span class="sxs-lookup"><span data-stu-id="fa5b4-119">RGB images in system memory are usually bottom-up.</span></span>

<span data-ttu-id="fa5b4-120">影片轉換特別需要處理不相符的緩衝區，因為輸入緩衝區可能不符合輸出緩衝區。</span><span class="sxs-lookup"><span data-stu-id="fa5b4-120">Video transforms in particular need to handle buffers with mismatched strides, because the input buffer might not match the output buffer.</span></span> <span data-ttu-id="fa5b4-121">例如，假設您想要轉換來源影像，並將結果寫入目的地影像。</span><span class="sxs-lookup"><span data-stu-id="fa5b4-121">For example, suppose that you want to convert a source image and write the result to a destination image.</span></span> <span data-ttu-id="fa5b4-122">假設兩個影像都有相同的寬度和高度，但可能沒有相同的像素格式或相同的影像跨距。</span><span class="sxs-lookup"><span data-stu-id="fa5b4-122">Assume that both images have the same width and height, but might not have the same pixel format or the same image stride.</span></span>

<span data-ttu-id="fa5b4-123">下列範例程式碼顯示撰寫這類函數的一般化方法。</span><span class="sxs-lookup"><span data-stu-id="fa5b4-123">The following example code shows a generalized approach for writing this kind of function.</span></span> <span data-ttu-id="fa5b4-124">這不是完整的運作範例，因為它會抽象化許多特定的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="fa5b4-124">This is not a complete working example, because it abstracts many of the specific details.</span></span>


```C++
void ProcessVideoImage(
    BYTE*       pDestScanLine0,     
    LONG        lDestStride,        
    const BYTE* pSrcScanLine0,      
    LONG        lSrcStride,         
    DWORD       dwWidthInPixels,     
    DWORD       dwHeightInPixels
    )
{
    for (DWORD y = 0; y < dwHeightInPixels; y++)
    {
        SOURCE_PIXEL_TYPE *pSrcPixel = (SOURCE_PIXEL_TYPE*)pDestScanLine0;
        DEST_PIXEL_TYPE *pDestPixel = (DEST_PIXEL_TYPE*)pSrcScanLine0;

        for (DWORD x = 0; x < dwWidthInPixels; x +=2)
        {
            pDestPixel[x] = TransformPixelValue(pSrcPixel[x]);
        }
        pDestScanLine0 += lDestStride;
        pSrcScanLine0 += lSrcStride;
    }
}
```



<span data-ttu-id="fa5b4-125">此函式會使用六個參數：</span><span class="sxs-lookup"><span data-stu-id="fa5b4-125">This function takes six parameters:</span></span>

-   <span data-ttu-id="fa5b4-126">目的地影像中掃描行0開頭的指標。</span><span class="sxs-lookup"><span data-stu-id="fa5b4-126">A pointer to the start of scan line 0 in the destination image.</span></span>
-   <span data-ttu-id="fa5b4-127">目的地影像的 stride。</span><span class="sxs-lookup"><span data-stu-id="fa5b4-127">The stride of the destination image.</span></span>
-   <span data-ttu-id="fa5b4-128">來源影像中掃描行0開頭的指標。</span><span class="sxs-lookup"><span data-stu-id="fa5b4-128">A pointer to the start of scan line 0 in the source image.</span></span>
-   <span data-ttu-id="fa5b4-129">來源影像的 stride。</span><span class="sxs-lookup"><span data-stu-id="fa5b4-129">The stride of the source image.</span></span>
-   <span data-ttu-id="fa5b4-130">影像的寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="fa5b4-130">The width of the image in pixels.</span></span>
-   <span data-ttu-id="fa5b4-131">影像的高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="fa5b4-131">The height of the image in pixels.</span></span>

<span data-ttu-id="fa5b4-132">一般概念是一次處理一個資料列，逐一查看資料列中的每個圖元。</span><span class="sxs-lookup"><span data-stu-id="fa5b4-132">The general idea is to process one row at a time, iterating over each pixel in the row.</span></span> <span data-ttu-id="fa5b4-133">假設來源 \_ 圖元 \_ 型別和目的地 \_ 圖元 \_ 型別分別是代表來源和目的影像之圖元配置的結構。</span><span class="sxs-lookup"><span data-stu-id="fa5b4-133">Assume that SOURCE\_PIXEL\_TYPE and DEST\_PIXEL\_TYPE are structures representing the pixel layout for the source and destination images, respectively.</span></span> <span data-ttu-id="fa5b4-134"> (例如，32位 RGB 會使用 [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) 結構。</span><span class="sxs-lookup"><span data-stu-id="fa5b4-134">(For example, 32-bit RGB uses the [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) structure.</span></span> <span data-ttu-id="fa5b4-135">並非每個像素格式都有預先定義的結構。 ) 將陣列指標轉換成結構類型，可讓您存取每個圖元的 RGB 或 YUV 元件。</span><span class="sxs-lookup"><span data-stu-id="fa5b4-135">Not every pixel format has a predefined structure.) Casting the array pointer to the structure type enables you to access the RGB or YUV components of each pixel.</span></span> <span data-ttu-id="fa5b4-136">在每個資料列的開頭，此函數會儲存資料列的指標。</span><span class="sxs-lookup"><span data-stu-id="fa5b4-136">At the start of each row, the function stores a pointer to the row.</span></span> <span data-ttu-id="fa5b4-137">在資料列的結尾，會將指標遞增影像跨距的寬度，使指標前進至下一個資料列。</span><span class="sxs-lookup"><span data-stu-id="fa5b4-137">At the end of the row, it increments the pointer by the width of the image stride, which advances the pointer to the next row.</span></span>

<span data-ttu-id="fa5b4-138">此範例會針對每個圖元呼叫名為 TransformPixelValue 的假設函數。</span><span class="sxs-lookup"><span data-stu-id="fa5b4-138">This example calls a hypothetical function named TransformPixelValue for each pixel.</span></span> <span data-ttu-id="fa5b4-139">這可能是從來源圖元計算目標圖元的任何函數。</span><span class="sxs-lookup"><span data-stu-id="fa5b4-139">This could be any function that calculates a target pixel from a source pixel.</span></span> <span data-ttu-id="fa5b4-140">當然，確切的詳細資料將取決於特定的工作。</span><span class="sxs-lookup"><span data-stu-id="fa5b4-140">Of course, the exact details will depend on the particular task.</span></span> <span data-ttu-id="fa5b4-141">例如，如果您有平面 YUV 格式，就必須在 luma 平面以外獨立存取色度平面;使用交錯式影片，您可能需要個別處理欄位;等等。</span><span class="sxs-lookup"><span data-stu-id="fa5b4-141">For example, if you have a planar YUV format, you must access the chroma planes independently from the luma plane; with interlaced video, you might need to process the fields separately; and so forth.</span></span>

<span data-ttu-id="fa5b4-142">為了提供更具體的範例，下列程式碼會將32位 RGB 映射轉換成 AYUV 映射。</span><span class="sxs-lookup"><span data-stu-id="fa5b4-142">To give a more concrete example, the following code converts a 32-bit RGB image into an AYUV image.</span></span> <span data-ttu-id="fa5b4-143">您可以使用 [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) 結構來存取 RGB 圖元，並使用 [**DXVA2 \_ AYUVSample8**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_ayuvsample8) 結構結構來存取 AYUV 的圖元。</span><span class="sxs-lookup"><span data-stu-id="fa5b4-143">The RGB pixels are accessed using an [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) structure, and the AYUV pixels are accessed using a [**DXVA2\_AYUVSample8**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_ayuvsample8) structure structure.</span></span>


```C++
//-------------------------------------------------------------------
// Name: RGB32_To_AYUV
// Description: Converts an image from RGB32 to AYUV
//-------------------------------------------------------------------
void RGB32_To_AYUV(
    BYTE*       pDest,
    LONG        lDestStride,
    const BYTE* pSrc,
    LONG        lSrcStride,
    DWORD       dwWidthInPixels,
    DWORD       dwHeightInPixels
    )
{
    for (DWORD y = 0; y < dwHeightInPixels; y++)
    {
        RGBQUAD             *pSrcPixel = (RGBQUAD*)pSrc;
        DXVA2_AYUVSample8   *pDestPixel = (DXVA2_AYUVSample8*)pDest;
        
        for (DWORD x = 0; x < dwWidthInPixels; x++)
        {
            pDestPixel[x].Alpha = 0x80;
            pDestPixel[x].Y = RGBtoY(pSrcPixel[x]);   
            pDestPixel[x].Cb = RGBtoU(pSrcPixel[x]);   
            pDestPixel[x].Cr = RGBtoV(pSrcPixel[x]);   
        }
        pDest += lDestStride;
        pSrc += lSrcStride;
    }
}
```



<span data-ttu-id="fa5b4-144">下一個範例會將32位 RGB 映射轉換成 YV12 映射。</span><span class="sxs-lookup"><span data-stu-id="fa5b4-144">The next example converts a 32-bit RGB image to a YV12 image.</span></span> <span data-ttu-id="fa5b4-145">此範例顯示如何處理平面 YUV 格式。</span><span class="sxs-lookup"><span data-stu-id="fa5b4-145">This example shows how to handle a planar YUV format.</span></span> <span data-ttu-id="fa5b4-146"> (YV12 是平面4:2:0 格式。 ) 在此範例中，此函式會針對目標影像中的三個平面維護三個不同的指標。</span><span class="sxs-lookup"><span data-stu-id="fa5b4-146">(YV12 is a planar 4:2:0 format.) In this example, the function maintains three separate pointers for the three planes in the target image.</span></span> <span data-ttu-id="fa5b4-147">不過，基本的方法與上一個範例相同。</span><span class="sxs-lookup"><span data-stu-id="fa5b4-147">However, the basic approach is the same as the previous example.</span></span>


```C++
void RGB32_To_YV12(
    BYTE*       pDest,
    LONG        lDestStride,
    const BYTE* pSrc,
    LONG        lSrcStride,
    DWORD       dwWidthInPixels,
    DWORD       dwHeightInPixels
    )
{
    assert(dwWidthInPixels % 2 == 0);
    assert(dwHeightInPixels % 2 == 0);

    const BYTE *pSrcRow = pSrc;
    
    BYTE *pDestY = pDest;

    // Calculate the offsets for the V and U planes.

    // In YV12, each chroma plane has half the stride and half the height  
    // as the Y plane.
    BYTE *pDestV = pDest + (lDestStride * dwHeightInPixels);
    BYTE *pDestU = pDest + 
                   (lDestStride * dwHeightInPixels) + 
                   ((lDestStride * dwHeightInPixels) / 4);

    // Convert the Y plane.
    for (DWORD y = 0; y < dwHeightInPixels; y++)
    {
        RGBQUAD *pSrcPixel = (RGBQUAD*)pSrcRow;
        
        for (DWORD x = 0; x < dwWidthInPixels; x++)
        {
            pDestY[x] = RGBtoY(pSrcPixel[x]);    // Y0
        }
        pDestY += lDestStride;
        pSrcRow += lSrcStride;
    }

    // Convert the V and U planes.

    // YV12 is a 4:2:0 format, so each chroma sample is derived from four 
    // RGB pixels.
    pSrcRow = pSrc;
    for (DWORD y = 0; y < dwHeightInPixels; y += 2)
    {
        RGBQUAD *pSrcPixel = (RGBQUAD*)pSrcRow;
        RGBQUAD *pNextSrcRow = (RGBQUAD*)(pSrcRow + lSrcStride);

        BYTE *pbV = pDestV;
        BYTE *pbU = pDestU;

        for (DWORD x = 0; x < dwWidthInPixels; x += 2)
        {
            // Use a simple average to downsample the chroma.

            *pbV++ = ( RGBtoV(pSrcPixel[x]) +
                       RGBtoV(pSrcPixel[x + 1]) +       
                       RGBtoV(pNextSrcRow[x]) +         
                       RGBtoV(pNextSrcRow[x + 1]) ) / 4;        

            *pbU++ = ( RGBtoU(pSrcPixel[x]) +
                       RGBtoU(pSrcPixel[x + 1]) +       
                       RGBtoU(pNextSrcRow[x]) +         
                       RGBtoU(pNextSrcRow[x + 1]) ) / 4;    
        }
        pDestV += lDestStride / 2;
        pDestU += lDestStride / 2;
        
        // Skip two lines on the source image.
        pSrcRow += (lSrcStride * 2);
    }
}
```



<span data-ttu-id="fa5b4-148">在這些範例中，假設應用程式已經決定了影像 stride。</span><span class="sxs-lookup"><span data-stu-id="fa5b4-148">In all of these examples, it is assumed that the application has already determined the image stride.</span></span> <span data-ttu-id="fa5b4-149">您有時可以從媒體緩衝區取得此資訊。</span><span class="sxs-lookup"><span data-stu-id="fa5b4-149">You can sometimes get this information from the media buffer.</span></span> <span data-ttu-id="fa5b4-150">否則，您必須根據影片格式來計算。</span><span class="sxs-lookup"><span data-stu-id="fa5b4-150">Otherwise, you must calculate it based on the video format.</span></span> <span data-ttu-id="fa5b4-151">如需有關計算影像 stride 以及使用影片媒體緩衝區的詳細資訊，請參閱 [未壓縮的影片緩衝區](uncompressed-video-buffers.md)。</span><span class="sxs-lookup"><span data-stu-id="fa5b4-151">For more information about calculating image stride and working with media buffers for video, see [Uncompressed Video Buffers](uncompressed-video-buffers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="fa5b4-152">相關主題</span><span class="sxs-lookup"><span data-stu-id="fa5b4-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa5b4-153">影片媒體類型</span><span class="sxs-lookup"><span data-stu-id="fa5b4-153">Video Media Types</span></span>](video-media-types.md)
</dt> <dt>

[<span data-ttu-id="fa5b4-154">媒體類型</span><span class="sxs-lookup"><span data-stu-id="fa5b4-154">Media Types</span></span>](media-types.md)
</dt> </dl>

 

 

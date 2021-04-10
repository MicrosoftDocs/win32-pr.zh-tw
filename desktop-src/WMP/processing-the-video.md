---
title: 處理影片
description: 處理影片
ms.assetid: 2fa337dd-34c0-4a09-8c20-21f6103627dd
keywords:
- Windows Media Player 外掛程式、影片 DSP
- 外掛程式、視頻 DSP
- 數位信號處理外掛程式、影片處理
- DSP 外掛程式、影片處理
- 影片 DSP 外掛程式，處理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a8d21aaa3999d05ea3628ff341c74379b07a6dd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023658"
---
# <a name="processing-the-video"></a><span data-ttu-id="00ed7-108">處理影片</span><span class="sxs-lookup"><span data-stu-id="00ed7-108">Processing the Video</span></span>

<span data-ttu-id="00ed7-109">處理影片的詳細資料會因每種格式而異;它已超出本檔的範圍，以提供這些詳細資料。</span><span class="sxs-lookup"><span data-stu-id="00ed7-109">The details of processing video vary for each format; it is beyond the scope of this documentation to provide these details.</span></span> <span data-ttu-id="00ed7-110">一般而言，外掛程式的目標是要變更輸入緩衝區中的色彩資料，然後將資料複製到輸出緩衝區。</span><span class="sxs-lookup"><span data-stu-id="00ed7-110">In a general sense, the goal of the plug-in is to change the color data in the input buffer and then copy the data to the output buffer.</span></span>

<span data-ttu-id="00ed7-111">範例外掛程式會處理兩種類型的影片格式： YUV 和 RGB。</span><span class="sxs-lookup"><span data-stu-id="00ed7-111">The sample plug-in processes two types of video formats: YUV and RGB.</span></span>

<span data-ttu-id="00ed7-112">如果是 YUV video，紅色和藍色的資訊會以您的和 V 值進行編碼，而亮度層級則以 Y 值表示。綠色值經過編碼，並且可以使用演算法來復原。</span><span class="sxs-lookup"><span data-stu-id="00ed7-112">For YUV video, the red and blue color information is encoded in the U and V values and the luminance level is represented by the Y value; the green value is encoded and can be recovered by using an algorithm.</span></span> <span data-ttu-id="00ed7-113">範例外掛程式只會變更您的和 V 值，以影響色彩層級。</span><span class="sxs-lookup"><span data-stu-id="00ed7-113">The sample plug-in simply changes the U and V values to affect the color level.</span></span> <span data-ttu-id="00ed7-114">每個 U 或 V 位元組都有0到255之間的值。</span><span class="sxs-lookup"><span data-stu-id="00ed7-114">Each U or V byte has a value between zero and 255.</span></span> <span data-ttu-id="00ed7-115">外掛程式會先調整每個值，以從-128 到127的範圍表示，然後以提供的縮放比例來調整值。</span><span class="sxs-lookup"><span data-stu-id="00ed7-115">The plug-in first adjusts each value to be represented by a range from -128 to 127, and then scales the value by the supplied scale factor.</span></span> <span data-ttu-id="00ed7-116">最後，程式碼會再次調整原始零到255範圍的值，並將資料複製到輸出緩衝區。</span><span class="sxs-lookup"><span data-stu-id="00ed7-116">Finally, the code adjusts the value again for the original zero-to-255 range and copies the data to the output buffer.</span></span> <span data-ttu-id="00ed7-117">下列程式碼範例會處理 UYVY 影片。</span><span class="sxs-lookup"><span data-stu-id="00ed7-117">The following example code processes UYVY video.</span></span> <span data-ttu-id="00ed7-118">在此格式中，每個其他位元組都是 U 或 Y 值。</span><span class="sxs-lookup"><span data-stu-id="00ed7-118">In this format, every other byte is a U or Y value.</span></span>


```C++
while( dwHeight-- )
{
    DWORD x = dwWidth; 

        while( x-- )
        {
        // Scale the U and V bytes to 128.
        // Just copy the Y bytes.
        if( x%2 )
        {
            pbTarget[x] = pbSource[x];
        }
        else
        {
            long temp = (long)((pbSource[x] - 128) * m_fScaleFactor);

            // Truncate if exceeded full scale.
            if (temp > 127)
            temp = 127;
            if (temp < -128)
            temp = -128;

            pbTarget[x] = temp + 128;
        }
    }

    // Move the pointers to the next row.
    pbSource += lStrideIn;
    pbTarget += lStrideOut;
}

```



<span data-ttu-id="00ed7-119">針對 RGB 影片，色彩和亮度資訊會編碼為個別的紅色、綠色和藍色值。</span><span class="sxs-lookup"><span data-stu-id="00ed7-119">For RGB video, the color and luminance information is encoded as separate red, green, and blue values.</span></span> <span data-ttu-id="00ed7-120">範例外掛程式會計算三個值的平均值以判斷灰色的值，然後使用提供的比例因數來調整每個色彩值。</span><span class="sxs-lookup"><span data-stu-id="00ed7-120">The sample plug-in computes the average of the three values to determine the value for gray, and then adjusts each color value by using the supplied scale factor.</span></span> <span data-ttu-id="00ed7-121">同樣地，您必須在調整之前將-128 到127範圍的值正規化。</span><span class="sxs-lookup"><span data-stu-id="00ed7-121">Once again, the values must be normalized for the -128 to 127 range before scaling.</span></span> <span data-ttu-id="00ed7-122">Process32Bit 中的下列程式碼會顯示 RGB32 的進程：</span><span class="sxs-lookup"><span data-stu-id="00ed7-122">The following code from Process32Bit shows the process for RGB32:</span></span>


```C++
while( dwHeight-- )
{
    RGBQUAD* pPixelIn = (RGBQUAD*)pbSource;
    RGBQUAD* pPixelOut = (RGBQUAD*)pbTarget;

    for( DWORD x = 0; x < dwWidth; x++ )
    {
    // Get the color bytes.
    long lBlue = (long) pPixelIn[x].rgbBlue;
    long lGreen = (long) pPixelIn[x].rgbGreen;
    long lRed = (long) pPixelIn[x].rgbRed;

    // Compute the average for gray.
    long lAverage = ( lBlue + lGreen + lRed ) / 3;

    // Scale the colors to the average.
    pPixelOut[x].rgbBlue = (BYTE)( ( lBlue - lAverage ) * m_fScaleFactor  + lAverage );
    pPixelOut[x].rgbGreen = (BYTE)( ( lGreen - lAverage ) * m_fScaleFactor  + lAverage );
    pPixelOut[x].rgbRed = (BYTE)( ( lRed - lAverage ) * m_fScaleFactor  + lAverage );
    pPixelOut[x].rgbReserved = pPixelIn[x].rgbReserved;
    }

    // Move the pointers to the next row.
    pbSource += lStrideIn;
    pbTarget += lStrideOut;
}

```



<span data-ttu-id="00ed7-123">如需影片格式的詳細資訊，請參閱 [FourCC 網站](../directshow/fourcc-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="00ed7-123">For more information about video formats, see the [FourCC website](../directshow/fourcc-codes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="00ed7-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="00ed7-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="00ed7-125">**執行 Video DSP 外掛程式**</span><span class="sxs-lookup"><span data-stu-id="00ed7-125">**Implementing a Video DSP Plug-in**</span></span>](implementing-a-video-dsp-plug-in.md)
</dt> </dl>

 

 
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
# <a name="image-stride"></a>影像 Stride

當影片影像儲存在記憶體中時，記憶體緩衝區可能會在每個圖元資料列之後包含額外的填補位元組。 填補位元組會影響影像儲存在記憶體中的方式，但不會影響影像的顯示方式。

*Stride* 是記憶體中一個圖元的位元組數，以及記憶體中的下一個資料列。 Stride 也稱為「 *音調*」。 如果有填補位元組存在，stride 的寬度會比影像的寬度更寬，如下圖所示。

![顯示影像加上填補的圖表。](images/c85c6a40-f0a8-48a3-b465-39ceada66339.gif)

包含有相等維度之影片框架的兩個緩衝區可以有兩個不同的進展。 如果您處理影片影像，您必須將 stride 列入考慮。

此外，也有兩種方式可將影像排列在記憶體中。 在由 *上而下* 的影像中，影像中最上層的圖元會先出現在記憶體中。 在 *下* 圖中，最後一列的圖元會先出現在記憶體中。 下圖顯示由上而下的影像與底部影像之間的差異。

![顯示頂端和底部影像的圖表。](images/f03bd9ff-0cf3-4a56-88c5-5b8c44637272.gif)

底部的影像有負面的跨距，因為會將 stride 定義為相對於顯示的影像，需要向下移動圖元資料列的位元組數目。 YUV 影像應該一律是由上而下，而且 Direct3D 介面中包含的任何影像都必須由上而下。 系統記憶體中的 RGB 影像通常是自下而上的。

影片轉換特別需要處理不相符的緩衝區，因為輸入緩衝區可能不符合輸出緩衝區。 例如，假設您想要轉換來源影像，並將結果寫入目的地影像。 假設兩個影像都有相同的寬度和高度，但可能沒有相同的像素格式或相同的影像跨距。

下列範例程式碼顯示撰寫這類函數的一般化方法。 這不是完整的運作範例，因為它會抽象化許多特定的詳細資料。


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



此函式會使用六個參數：

-   目的地影像中掃描行0開頭的指標。
-   目的地影像的 stride。
-   來源影像中掃描行0開頭的指標。
-   來源影像的 stride。
-   影像的寬度（以圖元為單位）。
-   影像的高度（以圖元為單位）。

一般概念是一次處理一個資料列，逐一查看資料列中的每個圖元。 假設來源 \_ 圖元 \_ 型別和目的地 \_ 圖元 \_ 型別分別是代表來源和目的影像之圖元配置的結構。  (例如，32位 RGB 會使用 [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) 結構。 並非每個像素格式都有預先定義的結構。 ) 將陣列指標轉換成結構類型，可讓您存取每個圖元的 RGB 或 YUV 元件。 在每個資料列的開頭，此函數會儲存資料列的指標。 在資料列的結尾，會將指標遞增影像跨距的寬度，使指標前進至下一個資料列。

此範例會針對每個圖元呼叫名為 TransformPixelValue 的假設函數。 這可能是從來源圖元計算目標圖元的任何函數。 當然，確切的詳細資料將取決於特定的工作。 例如，如果您有平面 YUV 格式，就必須在 luma 平面以外獨立存取色度平面;使用交錯式影片，您可能需要個別處理欄位;等等。

為了提供更具體的範例，下列程式碼會將32位 RGB 映射轉換成 AYUV 映射。 您可以使用 [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) 結構來存取 RGB 圖元，並使用 [**DXVA2 \_ AYUVSample8**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_ayuvsample8) 結構結構來存取 AYUV 的圖元。


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



下一個範例會將32位 RGB 映射轉換成 YV12 映射。 此範例顯示如何處理平面 YUV 格式。  (YV12 是平面4:2:0 格式。 ) 在此範例中，此函式會針對目標影像中的三個平面維護三個不同的指標。 不過，基本的方法與上一個範例相同。


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



在這些範例中，假設應用程式已經決定了影像 stride。 您有時可以從媒體緩衝區取得此資訊。 否則，您必須根據影片格式來計算。 如需有關計算影像 stride 以及使用影片媒體緩衝區的詳細資訊，請參閱 [未壓縮的影片緩衝區](uncompressed-video-buffers.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[影片媒體類型](video-media-types.md)
</dt> <dt>

[媒體類型](media-types.md)
</dt> </dl>

 

 

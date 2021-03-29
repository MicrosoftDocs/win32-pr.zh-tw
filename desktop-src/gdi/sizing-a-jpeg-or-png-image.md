---
description: StretchDIBits 函式會將 DIB 中圖元矩形的色彩資料複製到指定的目的地矩形。
ms.assetid: d4e3f631-3852-4cee-8e97-2244c39b200e
title: 調整 JPEG 或 PNG 影像的大小
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28cd5bf3cbef8bab80d45536d90bfdd10174c26d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973093"
---
# <a name="sizing-a-jpeg-or-png-image"></a>調整 JPEG 或 PNG 影像的大小

[**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits)函式會將 DIB 中圖元矩形的色彩資料複製到指定的目的地矩形。 如果目的地矩形大於來源矩形，此函式會將色彩資料的資料列和資料行拉伸，以符合目的地矩形。 如果目的地矩形小於來源矩形， **StretchDIBits** 會使用指定的點陣運算來壓縮資料列和資料行。

[**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) 已擴充，可讓 JPEG 或 PNG 影像以來源影像的形式傳遞。

例如：


```C++
// pvJpgImage points to a buffer containing the JPEG image 
// nJpgImageSize is the size of the buffer 
// ulJpgWidth is the width of the JPEG image 
// ulJpgHeight is the height of the JPEG image 
// 

// 
// Check if CHECKJPEGFORMAT is supported (device has JPEG support) 
// and use it to verify that device can handle the JPEG image. 
// 

ul = CHECKJPEGFORMAT;

if (
    // Check if CHECKJPEGFORMAT exists: 

    (ExtEscape(hdc, QUERYESCSUPPORT,
               sizeof(ul), &ul, 0, 0) > 0) &&

    // Check if CHECKJPEGFORMAT executed without error: 

    (ExtEscape(hdc, CHECKJPEGFORMAT,
               nJpgImageSize, pvJpgImage, sizeof(ul), &ul) > 0) &&

    // Check status code returned by CHECKJPEGFORMAT: 

    (ul == 1)
   )
{
    // 
    // Initialize the BITMAPINFO. 
    // 

    memset(&bmi, 0, sizeof(bmi));
    bmi.bmiHeader.biSize        = sizeof(BITMAPINFOHEADER);
    bmi.bmiHeader.biWidth       = ulJpgWidth;
    bmi.bmiHeader.biHeight      = -ulJpgHeight; // top-down image 
    bmi.bmiHeader.biPlanes      = 1;
    bmi.bmiHeader.biBitCount    = 0;
    bmi.bmiHeader.biCompression = BI_JPEG;
    bmi.bmiHeader.biSizeImage   = nJpgImageSize;

    // 
    // Do the StretchDIBits. 
    // 

    iRet = StretchDIBits(hdc,
                         // destination rectangle 
                         ulDstX, ulDstY, ulDstWidth, ulDstHeight,
                         // source rectangle 
                         0, 0, ulJpgWidth, ulJpgHeight,
                         pvJpgImage,
                         &bmi,
                         DIB_RGB_COLORS,
                         SRCCOPY);

    if (iRet == GDI_ERROR)
        return FALSE;
}
else
{
    // 
    // Decompress image into a DIB and call StretchDIBits  
    // with the DIB instead. 
    // 
}
```



 

 




---
description: 本主題說明兩個相關的概念、圖片外觀比例和圖元外觀比例。
ms.assetid: 384bdeaa-5360-42af-9f95-b791af2dcafc
title: 圖片外觀比例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74e81f1b8e26af753a5c8c1bc7ecb09d8a658582
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191764"
---
# <a name="picture-aspect-ratio"></a>圖片外觀比例

本主題說明兩個相關的概念、圖片外觀比例和圖元外觀比例。 接著，它會說明如何使用媒體類型在 Microsoft 媒體基礎中表示這些概念。

-   [圖片外觀比例](#picture-aspect-ratio)
    -   [上下黑邊縮](#letterboxing)
    -   [平移和掃描](#pan-and-scan)
-   [圖元外觀比例](#pixel-aspect-ratio)
-   [使用外觀比例](#working-with-aspect-ratios)
-   [程式碼範例](#code-examples)
    -   [尋找顯示區域](#finding-the-display-area)
    -   [圖元外觀比例之間的轉換](#converting-between-pixel-aspect-ratios)
    -   [計算黑邊區域](#calculating-the-letterbox-area)
-   [相關主題](#related-topics)

## <a name="picture-aspect-ratio"></a>圖片外觀比例

*圖片外觀比例* 會定義所顯示影片影像的形狀。 圖片外觀比例為 X:Y，其中 X:Y 是圖片寬度與圖片高度的比例。 大部分的影片標準都使用4:3 或16:9 圖片外觀比例。 16:9 外觀比例通常稱為 *寬螢幕*。 電影院電影通常會使用1:85:1 或1:66:1 外觀比例。 圖片外觀比例也稱為 *顯示外觀比例* (DAR) 。

![顯示4:3 和16:9 外觀比例的圖表](images/aspect-ratio01.png)

影片影像有時與顯示區域沒有相同的圖形。 例如，4:3 的影片可能會顯示在寬屏 (16 × 9) 電視上。 在「電腦影片」中，影片可能會顯示在具有任意大小的視窗內。 在這種情況下，您可以透過三種方式來使影像符合顯示區域：

-   沿著一個軸伸展影像以符合顯示區域。
-   調整影像以符合顯示區域，同時維持原始圖片的外觀比例。
-   裁剪影像。

將影像延展成適合顯示區域幾乎都是錯誤的，因為它不會保留正確的圖片外觀比例。

### <a name="letterboxing"></a>上下黑邊縮

調整寬螢幕影像以符合4:3 顯示器的程式稱為 *上下黑邊縮*，如下圖所示。 影像頂端和底部的結果 rectanglular 區域通常會填滿黑色，雖然可以使用其他色彩。

![顯示正確黑邊方式的圖表](images/aspect-ratio02.png)

相反地，調整4:3 影像以符合寬螢幕顯示器的情況，有時也稱為 *pillarboxing*。 不過， *黑邊* 一詞也會用來表示調整影片影像以符合任何指定的顯示區域。

![顯示 pillarboxing 的圖表](images/aspect-ratio03.png)

### <a name="pan-and-scan"></a>平移和掃描

移動流覽和掃描是一種技術，可將寬螢幕影像裁剪成4×3矩形區域，以顯示于4:3 顯示裝置上。 產生的影像會填滿整個顯示器，而不需要黑色黑邊的區域，而原始影像的部分則會裁剪掉。 裁剪的區域可以從畫面格移至框架，如同感興趣的區域。 *平移和掃描* 中的「移動流覽」一詞是指移動移動流覽和掃描區域所造成的移動流覽效果。

![顯示平移和掃描的圖表](images/aspect-ratio04.png)

## <a name="pixel-aspect-ratio"></a>圖元外觀比例

*圖元外觀比例* (PAR) 測量圖元的形狀。

當您捕獲數位映射時，會以垂直和水準方式取樣影像，產生量化範例的矩形陣列，稱為 *圖元* 或 *pels*。 取樣方格的形狀決定了數位化影像中圖元的形狀。

以下範例會使用較小的數位來簡化數學運算。 假設原始影像是正方形 (也就是說，圖片的外觀比例為 1:1) ;並假設取樣方格包含12個元素，並以4×3方格排列。 每個產生圖元的形狀將會高於寬度。 具體而言，每個圖元的形狀將會是3×4。 非正方形的圖元稱為 *非正方形圖元*。

![顯示非方形取樣方格的圖表](images/aspect-ratio05.png)

圖元外觀比例也適用于顯示裝置。 顯示裝置和實體圖元解析度 (的實體圖形，) 判斷顯示裝置的範圍。 電腦監視器通常使用正方形圖元。 如果影像相等且顯示的不相符，則必須以垂直或水準方式調整影像的大小，才能正確顯示。 下列公式的關聯等同、顯示外觀比例 (DAR) 和影像大小（以圖元為單位）：

*DAR* = (*影像寬度（以* 圖元為單位）  /  *影像高度（圖元）*) × *PAR*

請注意，此公式中的影像寬度和影像高度會參考記憶體中的影像，而不是所顯示的影像。

以下是真實世界的範例： NTSC-M 類比影片包含使用中影像區域的480掃描行。 ITU-R Rec 指定水準取樣率為每行704個可見的圖元，並產生具有 704 x 480 圖元的數位影像。 預期的圖片外觀比例為4:3，而產生的是10:11。

-   DAR：4:3
-   寬度（以圖元為單位）：704
-   高度（以圖元為單位）：480
-   PAR：10/11

4/3 = (704/420) x (10/11) 

若要在具有正方形圖元的顯示裝置上正確地顯示此影像，您必須將寬度調整為10/11 或依11/10 的高度。

## <a name="working-with-aspect-ratios"></a>使用外觀比例

影片框架的正確圖形是以 *圖元外觀比例* 定義 (PAR) 和 *顯示區域*。

-   等同定義影像中圖元的形狀。 正方形圖元的外觀比例為1:1。 任何其他外觀比例都會描述非正方形圖元。 例如，NTSC 電視使用10:11。 假設您要在電腦監視器上呈現影片，顯示器的 (1:1 PAR) 的正方形圖元。 在媒體類型上的 [ [**MF \_ MT \_ 圖元 \_ 外觀 \_ 比例**](mf-mt-pixel-aspect-ratio-attribute.md) ] 屬性中，會提供來源內容的等同部分。
-   顯示區域是要顯示之影片影像的區域。 媒體類型中可能會指定兩個相關的顯示區域：
    -   平移和掃描光圈。 移動流覽和掃描光圈是一部影片的4×3區域，應以平移/掃描模式顯示。 它是用來在沒有上下黑邊縮的情況下，顯示4×3顯示器上的寬螢幕內容。 [移動流覽] 和 [掃描] 光圈是在 [ [**mf \_ mt \_ 平移 \_ 掃描 \_**](mf-mt-pan-scan-aperture-attribute.md) ] 屬性中提供，只有在 [ [**mf \_ Mt \_ 平移 \_ 掃描 \_ 已啟用**](mf-mt-pan-scan-enabled-attribute.md) ] 屬性為 **TRUE** 時才會使用。
    -   顯示光圈。 這個光圈是以部分影片標準定義。 顯示光圈以外的任何地方都是 overscan 區域，不應該顯示。 例如，NTSC 電視為720×480圖元，顯示口徑為704×480。 您可以在 [**MF \_ MT \_ 最小 \_ 顯示 \_ 光圈**](mf-mt-minimum-display-aperture-attribute.md) 屬性中指定顯示光圈。 如果有的話，則應該在平移和掃描模式為 **FALSE** 時使用。

如果平移和可以模式為 **FALSE** ，且未定義顯示光圈，則應該會顯示整個影片畫面。 事實上，除了電視和 DVD 影片之外，大部分的影片內容都是如此。 整個圖片的外觀比例會計算為 (*顯示區域寬度*  /  *顯示區域高度*) ×等於。 

## <a name="code-examples"></a>程式碼範例

### <a name="finding-the-display-area"></a>尋找顯示區域

下列程式碼顯示如何從媒體類型取得顯示區域。


```C++
MFVideoArea MakeArea(float x, float y, DWORD width, DWORD height);

HRESULT GetVideoDisplayArea(IMFMediaType *pType, MFVideoArea *pArea)
{
    HRESULT hr = S_OK;
    BOOL bPanScan = FALSE;
    UINT32 width = 0, height = 0;

    bPanScan = MFGetAttributeUINT32(pType, MF_MT_PAN_SCAN_ENABLED, FALSE);

    // In pan-and-scan mode, try to get the pan-and-scan region.
    if (bPanScan)
    {
        hr = pType->GetBlob(MF_MT_PAN_SCAN_APERTURE, (UINT8*)pArea, 
            sizeof(MFVideoArea), NULL);
    }

    // If not in pan-and-scan mode, or the pan-and-scan region is not set, 
    // get the minimimum display aperture.

    if (!bPanScan || hr == MF_E_ATTRIBUTENOTFOUND)
    {
        hr = pType->GetBlob(MF_MT_MINIMUM_DISPLAY_APERTURE, (UINT8*)pArea, 
            sizeof(MFVideoArea), NULL);

        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            // Minimum display aperture is not set.

            // For backward compatibility with some components, 
            // check for a geometric aperture. 

            hr = pType->GetBlob(MF_MT_GEOMETRIC_APERTURE, (UINT8*)pArea, 
                sizeof(MFVideoArea), NULL);
        }

        // Default: Use the entire video area.

        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            hr = MFGetAttributeSize(pType, MF_MT_FRAME_SIZE, &width, &height);

            if (SUCCEEDED(hr))
            {
                *pArea = MakeArea(0.0, 0.0, width, height);
            }
        }
    }
    return hr;
}
```




```C++
MFOffset MakeOffset(float v)
{
    MFOffset offset;
    offset.value = short(v);
    offset.fract = WORD(65536 * (v-offset.value));
    return offset;
}
```




```C++
MFVideoArea MakeArea(float x, float y, DWORD width, DWORD height)
{
    MFVideoArea area;
    area.OffsetX = MakeOffset(x);
    area.OffsetY = MakeOffset(y);
    area.Area.cx = width;
    area.Area.cy = height;
    return area;
}
```



### <a name="converting-between-pixel-aspect-ratios"></a>圖元外觀比例之間的轉換

下列程式碼示範如何將矩形從一個圖元的外觀比例轉換成另一個圖元的外觀比例 (相等的) ，同時保留圖片的外觀比例。


```C++
//-----------------------------------------------------------------------------
// Converts a rectangle from one pixel aspect ratio (PAR) to another PAR.
// Returns the corrected rectangle.
//
// For example, a 720 x 486 rect with a PAR of 9:10, when converted to 1x1 PAR,
// must be stretched to 720 x 540.
//-----------------------------------------------------------------------------

RECT CorrectAspectRatio(const RECT& src, const MFRatio& srcPAR, const MFRatio& destPAR)
{
    // Start with a rectangle the same size as src, but offset to (0,0).
    RECT rc = {0, 0, src.right - src.left, src.bottom - src.top};

    // If the source and destination have the same PAR, there is nothing to do.
    // Otherwise, adjust the image size, in two steps:
    //  1. Transform from source PAR to 1:1
    //  2. Transform from 1:1 to destination PAR.

    if ((srcPAR.Numerator != destPAR.Numerator) || 
        (srcPAR.Denominator != destPAR.Denominator))
    {
        // Correct for the source's PAR.

        if (srcPAR.Numerator > srcPAR.Denominator)
        {
            // The source has "wide" pixels, so stretch the width.
            rc.right = MulDiv(rc.right, srcPAR.Numerator, srcPAR.Denominator);
        }
        else if (srcPAR.Numerator < srcPAR.Denominator)
        {
            // The source has "tall" pixels, so stretch the height.
            rc.bottom = MulDiv(rc.bottom, srcPAR.Denominator, srcPAR.Numerator);
        }
        // else: PAR is 1:1, which is a no-op.

        // Next, correct for the target's PAR. This is the inverse operation of 
        // the previous.

        if (destPAR.Numerator > destPAR.Denominator)
        {
            // The destination has "wide" pixels, so stretch the height.
            rc.bottom = MulDiv(rc.bottom, destPAR.Numerator, destPAR.Denominator);
        }
        else if (destPAR.Numerator < destPAR.Denominator)
        {
            // The destination has "tall" pixels, so stretch the width.
            rc.right = MulDiv(rc.right, destPAR.Denominator, destPAR.Numerator);
        }
        // else: PAR is 1:1, which is a no-op.
    }
    return rc;
}
```



### <a name="calculating-the-letterbox-area"></a>計算黑邊區域

下列程式碼會在給定來源和目的地矩形的情況下，計算黑邊區域。 假設兩個矩形都有相同的 PAR。


```C++
RECT LetterBoxRect(const RECT& rcSrc, const RECT& rcDst)
{
    // Compute source/destination ratios.
    int iSrcWidth  = rcSrc.right - rcSrc.left;
    int iSrcHeight = rcSrc.bottom - rcSrc.top;

    int iDstWidth  = rcDst.right - rcDst.left;
    int iDstHeight = rcDst.bottom - rcDst.top;

    int iDstLBWidth;
    int iDstLBHeight;

    if (MulDiv(iSrcWidth, iDstHeight, iSrcHeight) <= iDstWidth) 
    {
        // Column letterboxing ("pillar box")
        iDstLBWidth  = MulDiv(iDstHeight, iSrcWidth, iSrcHeight);
        iDstLBHeight = iDstHeight;
    }
    else 
    {
        // Row letterboxing.
        iDstLBWidth  = iDstWidth;
        iDstLBHeight = MulDiv(iDstWidth, iSrcHeight, iSrcWidth);
    }

    // Create a centered rectangle within the current destination rect

    LONG left = rcDst.left + ((iDstWidth - iDstLBWidth) / 2);
    LONG top = rcDst.top + ((iDstHeight - iDstLBHeight) / 2);

    RECT rc;
    SetRect(&rc, left, top, left + iDstLBWidth, top + iDstLBHeight);
    return rc;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體類型](media-types.md)
</dt> <dt>

[影片媒體類型](video-media-types.md)
</dt> <dt>

[**MF \_ MT \_ 最小 \_ 顯示 \_ 光圈**](mf-mt-minimum-display-aperture-attribute.md)
</dt> <dt>

[**MF \_ MT \_ 平移 \_ 掃描 \_ 光圈**](mf-mt-pan-scan-aperture-attribute.md)
</dt> <dt>

[**\_已啟用 MF MT \_ PAN \_ 掃描 \_**](mf-mt-pan-scan-enabled-attribute.md)
</dt> <dt>

[**MF \_ MT \_ 圖元 \_ 外觀 \_ 比例**](mf-mt-pixel-aspect-ratio-attribute.md)
</dt> </dl>

 

 




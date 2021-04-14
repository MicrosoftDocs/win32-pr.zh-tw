---
description: 本主題介紹點陣圖來源（核心 Windows 影像處理元件 (WIC) 元件，代表影像的點陣圖圖元。
ms.assetid: cff0c088-ca22-4d55-9cf0-9cbe9803923e
title: 點陣圖來源總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 910bfc253798058639b98a1d1beaacec9bd4d1bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468976"
---
# <a name="bitmap-sources-overview"></a>點陣圖來源總覽

本主題介紹點陣圖來源（核心 Windows 影像處理元件 (WIC) 元件，代表影像的點陣圖圖元。

本主題包含下列各節。

-   [點陣圖來源](#bitmap-sources-overview)
-   [點陣圖框架](#bitmap-frames)
-   [點陣圖](#bitmap-sources-overview)
-   [轉換點陣圖來源](#transform-bitmap-sources)
-   [像素格式和色彩內容轉換器](#pixel-format-and-color-context-converters)
-   [繪製點陣圖來源](#drawing-bitmap-sources)
-   [相關主題](#related-topics)

## <a name="bitmap-sources"></a>點陣圖來源

[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)元件是 WIC 的基本組建區塊，代表一組圖元。 點陣圖來源可以是 multiframe 影像的個別框架，也可以是在點陣圖來源上執行轉換的結果。 **IWICBitmapSource** 介面是許多主要 WIC 介面的基底，例如「解碼器框架 [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)和轉換點陣圖來源，例如 [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)。

下表描述 WIC 提供的不同點陣圖來源元件。



| 點陣圖來源                                                    | Description                                                          |
|-------------------------------------------------------------------|----------------------------------------------------------------------|
| [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) | 表示解碼器圖像框架。                                    |
| [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)                       | 提供點陣圖來源的可寫性和記憶體中標記法。 |
| [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper)         | 將點陣圖來源裁剪至所需的矩形。                        |
| [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) | 翻轉和/或將點陣圖來源旋轉為所需的方向。       |
| [**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler)           | 將點陣圖來源調整為所需的大小。                            |
| [**IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform)       | 轉換點陣圖來源的色彩內容。                     |
| [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)     | 轉換點陣圖來源的像素格式。                        |



 

## <a name="bitmap-frames"></a>點陣圖框架

最常見的 [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) 是 [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)。 這個介面是用來存取影像格式的實際點陣圖資料。 許多影像格式只支援單一點陣圖框架，而其他格式（例如 GIF 和 TIFF）支援每個影像有多個畫面格。

如需從影像取得點陣圖框架的範例，請參閱 [如何取出影像](https://www.bing.com/search?q=How+to+Retrieve+the+Frames+of+an+Image) 主題的畫面格。

## <a name="bitmaps"></a>點陣圖

[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)會將可寫性和靜態記憶體內部的概念加入點陣圖來源中。 WIC 點陣圖可讓使用者直接存取點陣圖來源的圖元。 這種直接存取是由 [**鎖定**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-lock) 方法提供，而且支援點陣圖圖元的任何讀取和/或寫入存取組合。 **Lock** 方法會鎖定指定的點陣圖矩形，並提供 [**IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) 物件來存取圖元。

如需使用 [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) 和 [**IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) 物件的範例，請參閱 [如何修改點陣圖來源的圖元](-wic-bitmapsources-howto-modifypixels.md) 主題。

## <a name="transform-bitmap-sources"></a>轉換點陣圖來源

WIC 提供數個可轉換圖元資料的 [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) 介面。 具體而言，WIC 會提供點陣圖來源轉換來調整、裁剪、旋轉和翻轉圖元資料。 這些點陣圖來源轉換有 [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper)、 [**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler)和 [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)。 這些點陣圖來源的每一個都有方法可初始化並建立新的轉換點陣圖來源。 例如， **IWICBitmapClipper** 包括 [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapclipper-initialize) 方法。 這個方法會在指定的 [**WICRect**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect)上，使用輸入點陣圖來源的裁剪圖元資料來初始化 clipper 點陣圖來源。

下列的 how to 主題示範轉換點陣圖來源的不同用途。

-   [如何調整點陣圖來源](-wic-bitmapsources-howto-scale.md)
-   [如何裁剪點陣圖來源](-wic-bitmapsources-howto-clip.md)
-   [如何翻轉和旋轉點陣圖來源](-wic-bitmapsources-howto-flipandrotate.md)

## <a name="pixel-format-and-color-context-converters"></a>像素格式和色彩內容轉換器

WIC 也提供點陣圖來源轉換點陣圖來源的像素格式和色彩內容。 WIC 提供這些作業的 [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter) 和 [**IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform) 。

[**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter) 會將指定的點陣圖來源從一個像素格式轉換成另一個圖元。

如需使用 [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)的範例，請參閱 [如何使用 Direct2D 繪製點陣圖來源](-wic-bitmapsources-howto-drawusingd2d.md) 主題。

## <a name="drawing-bitmap-sources"></a>繪製點陣圖來源

WIC 是靜止的影像編解碼器技術，可用來管理影像資料和中繼資料，而不是原本提供呈現影像的方式。 不過，您可以使用數種 Windows 圖形技術來繪製點陣圖來源，例如 Direct2D、Windows 圖形裝置介面 (GDI) 和 Windows GDI +。 這些技術各有不同的 WIC 互通性層級。 Direct2D 透過 [ID2D1Bitmap](../direct2d/render-targets-overview.md) 介面和 [ID2D1RenderTarget：： CreateBitmapFromWicBitmap](../direct2d/id2d1rendertarget-createbitmapfromwicbitmap.md) 方法提供直接的互通性，而 gdi 和 gdi + 則需要使用者將點陣圖來源圖元複製到 [點陣圖](../gdi/bitmaps.md)。

下列範例示範如何使用 Direct2D 繪製點陣圖來源。

-   [如何使用 Direct2D 繪製點陣圖來源](-wic-bitmapsources-howto-drawusingd2d.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[Windows 影像處理元件總覽](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[編碼總覽](-wic-creating-encoder.md)
</dt> <dt>

**其他資源**
</dt> <dt>

[如何撰寫 WIC-Enabled 編解碼器](-wic-howtowriteacodec.md)
</dt> </dl>

 

 

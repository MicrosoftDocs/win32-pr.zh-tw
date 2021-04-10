---
description: 執行 IWICBitmapSource
ms.assetid: d092e9e5-c041-42f5-84c8-0af52bb5c810
title: 執行 IWICBitmapSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c88e2f7dfd073405f9de8c82b2ce6d9592b241a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103694175"
---
# <a name="implementing-iwicbitmapsource"></a>執行 IWICBitmapSource

## <a name="iwicbitmapsource"></a>IWICBitmapSource

從應用程式的觀點來看映射時， [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)是很重要的。 它代表影像來源的最高層級抽象，以及代表影像的所有 Windows 影像處理元件 (WIC) 介面，包括 [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)、 [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)，以及所有轉換介面 ([**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler)、 [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper)、 [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)和 [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)) 衍生自該映射。 在任何特定時間， **IWICBitmapSource** 物件不一定是由記憶體中的實際點陣圖支援。 這可讓應用程式進行非常有效率的處理，因為影像可以用抽象形式處理。 轉換作業可以在轉換管線中連結，而不需耗用記憶體資源，直到應用程式準備好轉譯或列印影像為止，此時它會在最後的轉換上叫用 [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) 方法，以在已套用選取轉換的情況下，取得影像記憶體中的點陣圖。

``` syntax
interface IWICBitmapSource : IUnknown
{
   // Required methods
   HRESULT GetSize ( UINT *puiWidth, UINT *puiHeight );
   HRESULT GetPixelFormat ( WICPixelFormatGUID *pPixelFormat );
   HRESULT GetResolution ( double *pDpiX, double *pDpiY );
   HRESULT CopyPixels ( const WICRect *prc,
      UINT cbStride,
      UINT cbBufferSize, 
      BYTE *pbBuffer );
   // Optional method
   HRESULT CopyPalette ( IWICPalette *pIPalette );
}
```

從編解碼器的觀點來看， [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) 方法會在框架解碼物件上執行。 這些方法會在實 IWICBitmapSource 中說明，以及 [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)上的其他方法（衍生自 **IWICBitmapSource**）。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**參考**
</dt> <dt>

[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)
</dt> <dt>

[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)
</dt> <dt>

[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)
</dt> <dt>

**概念**
</dt> <dt>

[執行 IWICBitmapCodecProgressNotification (解碼器) ](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md)
</dt> <dt>

[執行 IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md)
</dt> <dt>

[如何撰寫 WIC-Enabled 編解碼器](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows 影像處理元件總覽](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 




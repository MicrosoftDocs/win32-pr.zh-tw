---
description: 執行 IWICBitmapFrameDecode
ms.assetid: 7dc626ad-1158-4b67-8ca7-47b4cf88e278
title: 執行 IWICBitmapFrameDecode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4b49e3636f5d81202b1060d868ecb40bb99d095dd9f26b6afd0d40c5f5fd0d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118205762"
---
# <a name="implementing-iwicbitmapframedecode"></a>執行 IWICBitmapFrameDecode

## <a name="iwicbitmapframedecode"></a>IWICBitmapFrameDecode

[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) 是提供實際影像位存取權的框架層級介面。 您可以在框架層級的解碼類別上執行這個介面。 因為它衍生自 [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)，所以您的 **IWICBitmapFrameDecode** 執行將包含 **IWICBitmapSource** 方法的執行。 **IWICBitmapFrameDecode** 上的其他方法可讓您存取框架層級的縮圖、影像的任何色彩內容，以及框架的中繼資料查詢讀取器。

``` syntax
interface IWICBitmapFrameDecode : IWICBitmapSource
{
// Required methods
HRESULT GetThumbnail ( IWICBitmapSource **ppIThumbnail );
HRESULT GetColorContexts ( UINT cCount, 
IWICColorContext **ppIColorContexts, UINT *pcActualCount );
HRESULT GetMetadataQueryReader ( IWICMetadataQueryReader **ppIMetadataQueryReader );

// Methods inherited from IWICBitmapSource
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

-   [GetThumbnail](#getthumbnail)
-   [GetColorCoNtexts](#getcolorcontexts)
-   [GetMetadataQueryReader](#getmetadataqueryreader)
-   [GetSize、GetPixelFormat 和 GetResolution](#getsize-getpixelformat-and-getresolution)
-   [CopyPixels](#copypixels)
-   [CopyPalette](#copypalette)

### <a name="getthumbnail"></a>GetThumbnail

[**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) 會傳回目前畫面格的縮圖。 基於效能考慮，縮圖最常以 JPEG 格式編碼。 就像在解碼器上的預覽一樣，您不需要或建議您為縮圖提供自己的 JPEG 解碼器。 相反地，您應該委派給 Windows 影像處理元件 (WIC) 所提供的 JPEG 解碼器。

如需縮圖的詳細資訊，請參閱[執行 IWICBitmapFrameEncode](-wic-imp-iwicbitmapframeencode.md)的[SetThumbnail](-wic-imp-iwicbitmapframeencode.md)方法。

### <a name="getcolorcontexts"></a>GetColorCoNtexts

[**GetColorCoNtexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getcolorcontexts) 會傳回有效的色彩內容 (也稱為色彩設定檔) 與此框架中的影像相關聯。 在大部分的情況下，這只是其中一種，但可能會有兩個或更少的情況。 呼叫端會傳入一或多個 [**IWICColorCoNtext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) 物件，並將 *帳戶 c)* 參數設定為指出傳入的數目。 這個方法會在 **IWICColorCoNtext** 物件中填入與影像相關聯之色彩設定檔的實際色彩內容資料。 將 *pcActualCount* 參數設定為與影像相關聯的實際色彩內容數目，即使該值大於您可以傳回的數目。  (如果有更多的色彩內容可供呼叫端傳入的 **IWICColorCoNtext** 物件數目使用，這會告知呼叫者有一或多個其他可用的物件。 ) 

### <a name="getmetadataqueryreader"></a>GetMetadataQueryReader

[**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) 會傳回 [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) ，讓應用程式用來從影像框架取出中繼資料。 這個介面是由元資料處理程式所執行，並可讓應用程式查詢屬於特定元資料格式的特定中繼資料屬性。 如需詳細資訊，請參閱 [執行 IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md)。

若要具現化 [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)，請在 [**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory)上呼叫 [**CreateQueryReaderFromBlockReader**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createqueryreaderfromblockreader) 。


```C++
IWICMetadataQueryReader* pQueryReader = NULL;
HRESULT hr;

hr = m_pComponentFactory->CreateQueryReaderFromBlockReader( 
  static_cast<IWICMetadataBlockWriter*>(this),
  &pQueryReader);
```



### <a name="getsize-getpixelformat-and-getresolution"></a>GetSize、GetPixelFormat 和 GetResolution

[**GetSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getsize)、 [**GetPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getpixelformat)和 [**GetResolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getresolution) 是一目了然的，並會傳回所要求的影像屬性。

### <a name="copypixels"></a>CopyPixels

當應用程式想要在記憶體中建立可轉譯成顯示或印表機的點陣圖時， [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels)是應用程式所呼叫的方法。 這是執行影像位實際解碼的方法。 這些參數是一個矩形，代表要複製到記憶體的來源影像中的相關區域;跨距，指定一個掃描行中的位元組數目;應用程式已配置之記憶體中的緩衝區大小;以及要將要求的影像位複製到其中的緩衝區指標。  (若要防止潛在的緩衝區溢位產生安全性弱點，請務必將最多的影像資料複製到緩衝區中，因為 *cbBufferSize* 參數指定。 ) 

### <a name="copypalette"></a>CopyPalette

只有具有索引像素格式的編解碼器必須執行 [**CopyPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypalette) 方法。 如果影像使用已編制索引的格式，請使用這個方法來傳回影像中所使用之色彩的調色板。 如果您的編解碼器沒有已編制索引的格式，則傳回 WINCODEC \_ ERR \_ PALETTEUNAVAILABLE。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**參考**
</dt> <dt>

[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)
</dt> <dt>

[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)
</dt> <dt>

[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)
</dt> <dt>

**概念**
</dt> <dt>

[執行 IWICBitmapSource](-wic-imp-iwicbitmapsource.md)
</dt> <dt>

[執行 IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md)
</dt> <dt>

[如何撰寫 WIC-Enabled 編解碼器](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows映射處理元件總覽](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 




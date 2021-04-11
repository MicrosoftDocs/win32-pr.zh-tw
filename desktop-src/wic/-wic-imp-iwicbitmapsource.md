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
# <a name="implementing-iwicbitmapsource"></a><span data-ttu-id="25992-103">執行 IWICBitmapSource</span><span class="sxs-lookup"><span data-stu-id="25992-103">Implementing IWICBitmapSource</span></span>

## <a name="iwicbitmapsource"></a><span data-ttu-id="25992-104">IWICBitmapSource</span><span class="sxs-lookup"><span data-stu-id="25992-104">IWICBitmapSource</span></span>

<span data-ttu-id="25992-105">從應用程式的觀點來看映射時， [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)是很重要的。</span><span class="sxs-lookup"><span data-stu-id="25992-105">[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) is important for working with images from an application perspective.</span></span> <span data-ttu-id="25992-106">它代表影像來源的最高層級抽象，以及代表影像的所有 Windows 影像處理元件 (WIC) 介面，包括 [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)、 [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)，以及所有轉換介面 ([**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler)、 [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper)、 [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)和 [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)) 衍生自該映射。</span><span class="sxs-lookup"><span data-stu-id="25992-106">It represents the highest level abstraction for an image source, and all Windows Imaging Component (WIC) interfaces that represent an image, including [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode), [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap), and all the transform interfaces ([**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler), [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper), [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator), and [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)) are derived from it.</span></span> <span data-ttu-id="25992-107">在任何特定時間， **IWICBitmapSource** 物件不一定是由記憶體中的實際點陣圖支援。</span><span class="sxs-lookup"><span data-stu-id="25992-107">At any specific time, an **IWICBitmapSource** object may or may not be backed by an actual bitmap in memory.</span></span> <span data-ttu-id="25992-108">這可讓應用程式進行非常有效率的處理，因為影像可以用抽象形式處理。</span><span class="sxs-lookup"><span data-stu-id="25992-108">This enables very efficient processing by an application, because an image can be dealt with as an abstraction.</span></span> <span data-ttu-id="25992-109">轉換作業可以在轉換管線中連結，而不需耗用記憶體資源，直到應用程式準備好轉譯或列印影像為止，此時它會在最後的轉換上叫用 [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) 方法，以在已套用選取轉換的情況下，取得影像記憶體中的點陣圖。</span><span class="sxs-lookup"><span data-stu-id="25992-109">Transform operations can be chained in a transform pipeline without consuming memory resources until the application is ready to render or print the image, at which time it invokes the [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) method on the final transform to get a bitmap in memory of the image with the selected transforms applied.</span></span>

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

<span data-ttu-id="25992-110">從編解碼器的觀點來看， [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) 方法會在框架解碼物件上執行。</span><span class="sxs-lookup"><span data-stu-id="25992-110">From a codec perspective, the [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) methods are implemented on the frame decoder object.</span></span> <span data-ttu-id="25992-111">這些方法會在實 IWICBitmapSource 中說明，以及 [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)上的其他方法（衍生自 **IWICBitmapSource**）。</span><span class="sxs-lookup"><span data-stu-id="25992-111">These methods are described in Implementing IWICBitmapSource, along with the other methods on [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode), which is derived from **IWICBitmapSource**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="25992-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="25992-112">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="25992-113">**參考**</span><span class="sxs-lookup"><span data-stu-id="25992-113">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="25992-114">**IWICBitmapDecoder**</span><span class="sxs-lookup"><span data-stu-id="25992-114">**IWICBitmapDecoder**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)
</dt> <dt>

[<span data-ttu-id="25992-115">**IWICBitmapSource**</span><span class="sxs-lookup"><span data-stu-id="25992-115">**IWICBitmapSource**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)
</dt> <dt>

[<span data-ttu-id="25992-116">**IWICBitmapFrameDecode**</span><span class="sxs-lookup"><span data-stu-id="25992-116">**IWICBitmapFrameDecode**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)
</dt> <dt>

<span data-ttu-id="25992-117">**概念**</span><span class="sxs-lookup"><span data-stu-id="25992-117">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="25992-118">執行 IWICBitmapCodecProgressNotification (解碼器) </span><span class="sxs-lookup"><span data-stu-id="25992-118">Implementing IWICBitmapCodecProgressNotification (Decoder)</span></span>](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md)
</dt> <dt>

[<span data-ttu-id="25992-119">執行 IWICBitmapFrameDecode</span><span class="sxs-lookup"><span data-stu-id="25992-119">Implementing IWICBitmapFrameDecode</span></span>](-wic-imp-iwicbitmapframedecode.md)
</dt> <dt>

[<span data-ttu-id="25992-120">如何撰寫 WIC-Enabled 編解碼器</span><span class="sxs-lookup"><span data-stu-id="25992-120">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="25992-121">Windows 影像處理元件總覽</span><span class="sxs-lookup"><span data-stu-id="25992-121">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 




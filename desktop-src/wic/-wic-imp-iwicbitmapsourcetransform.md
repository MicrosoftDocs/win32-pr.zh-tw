---
description: 執行 IWICBitmapSourceTransform
ms.assetid: 6a3e682c-55c6-4728-9d14-5eb0290f3dcc
title: 執行 IWICBitmapSourceTransform
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0809e1e56fe3c05c8803bb70106c4a24a466eafe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319851"
---
# <a name="implementing-iwicbitmapsourcetransform"></a>執行 IWICBitmapSourceTransform

## <a name="iwicbitmapsourcetransform"></a>IWICBitmapSourceTransform

雖然是選擇性的，但強烈建議每個解碼器在您的框架層級解碼類別上執行這個介面，因為它可以提供主要的效能優勢。 當應用程式要求感興趣的特定區域、大小、方向或像素格式，而不是只在完整解析度解碼整個影像，然後套用要求的轉換時，Windows 影像處理元件 (WIC) 會針對 [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)物件上的這個介面呼叫 [IUnknown：： QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 。 如果框架解碼支援它，WIC 會呼叫適當的方法或方法，以判斷畫面格解碼器是否可以執行要求的轉換，或決定可提供給所要求之的最接近大小或像素格式。 如果此解碼器可以執行要求的轉換或轉換，WIC 會使用適當的參數來叫用 [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) 。 如果此解碼器可以執行部分（但不是所有要求的轉換），WIC 會要求該解碼器執行其所能執行的轉換，並使用 WIC 轉換物件 ([**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler)、 [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper)、 [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)和 [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)) ，以執行在 **CopyPixels** 呼叫的結果上無法由框架解碼執行的其餘轉換。 如果此解碼器不支援 [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)，則 WIC 必須使用轉換物件來執行所有轉換。 比起將整個映射解碼，然後執行轉換，讓解碼器在解碼程式期間執行轉換，通常會更有效率。 這特別適用于調整規模較小或像素格式轉換等作業。


```C++
interface IWICBitmapSourceTransform : IUnknown
{
   // Required methods
   HRESULT DoesSupportTransform ( WICTransformOptions dstTransform,
              BOOL *pfIsSupported);
   HRESULT CopyPixels ( WICRect *prcSrc, 
      UINT uiWidth, 
      UINT uiHeight,
      WICPixelFormatGUID * pguidDstFormat,
      WICBitmapTransformOptions dstTransform, 
      UINT nStride, 
      UINT cbBufferSize, 
      BYTE *pbBuffer );

   // Optional methods
   HRESULT GetClosestSize ( UINT *puiWidth,
              UINT *puiHeight);
   HRESULT GetClosestPixelFormat ( WICPixelFormatGUID *pguidDstFormat);
}
```



-   [DoesSupportTransform](#doessupporttransform)
-   [CopyPixels](#copypixels)
-   [GetClosestSize](#getclosestsize)
-   [GetClosestPixelFormat](#getclosestpixelformat)

### <a name="doessupporttransform"></a>DoesSupportTransform

[**DoesSupportTransform**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-doessupporttransform) 會詢問此解碼器是否支援要求的旋轉或翻轉操作。 可能要求的 [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) 為：


```C++
enum WICBitmapTransformOptions
{   
   WICBitmapTransformRotate0,
   WICBitmapTransformRotate90,
   WICBitmapTransformRotate180,
   WICBitmapTransformRotate270,
   WICBitmapTransformFlipHorizontal,
   WICBitmapTransformFlipVertical
}
```



### <a name="copypixels"></a>CopyPixels

[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels)會執行解碼影像位的實際工作（例如 [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)介面上的 [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels)方法），但 [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)上的 [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels)方法更強大，而且可以大幅改善影像處理效能。

當要求多個轉換作業時，結果會取決於執行作業的順序。 為了確保編解碼器之間的可預測性和一致性，所有編解碼器都必須以相同的循序執行這些作業。 這是執行這些作業的標準順序。

1.  調整
2.  Crop
3.  Rotate

您可以隨時執行像素格式轉換，因為它不會影響其他轉換。

第一個參數（ *prcSrc*）是用來指定裁剪影像的相關區域。 由於調整是在依慣例裁剪之前執行，因此如果要縮放影像並進行裁剪，則應該在調整影像之後，判斷感興趣的區域。

第二個和第三個參數指出調整影像的大小。

*PguidDstFormat* 參數會指出已解碼影像所要求的像素格式。 因為 WIC 已經呼叫 [**GetClosestPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestpixelformat)，所以這應該是解碼器指出它所支援的像素格式。

*DstTransform* 參數表示要求的旋轉角度，以及是否要垂直、水準或兩者翻轉影像。 同樣地，因為 WIC 已經呼叫 [**DoesSupportTransform**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-doessupporttransform)，所以要求的轉換應該是該解碼器已指出它所支援的轉換。 請記住，在縮放和裁剪之後，應該一律執行旋轉。

### <a name="getclosestsize"></a>GetClosestSize

[**GetClosestSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestsize) 接受兩個 in/out 參數。 呼叫端會使用 *puiWidth* 和 *puiHeight* 參數來指定呼叫者偏好要解碼影像的大小。 不過，解碼器只能將影像解碼為其 DCT 大小的倍數，且不同的影像格式可以有不同的 DCT 大小。 此解碼器應該根據其本身的 DCT 大小來決定，最接近的是它可以進入所要求的大小，然後將 *puiWidth* 和 *puiHeight* 設定為傳回的維度。 如果要求較大的大小，但編解碼器不支援消除倍增，則應該傳回原始。

### <a name="getclosestpixelformat"></a>GetClosestPixelFormat

[**GetClosestPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestpixelformat) 可用來決定最接近所要求像素格式的像素格式，此格式可讓您在不遺失資料的情況下提供要求的像素格式。 最好的方式是轉換成較窄的像素格式，即使它會增加影像的大小，也是如此，因為它可以在必要時 reconverted 成更嚴格的格式。 不過，資料遺失之後，就無法復原。

## <a name="continued-reading"></a>繼續閱讀

若要深入瞭解如何建立已啟用 WIC 的編解碼器，請參閱 [執行 IWICDevelopRaw](-wic-imp-iwicdevelopraw.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**參考**
</dt> <dt>

[**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)
</dt> <dt>

[**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)
</dt> <dt>

**概念**
</dt> <dt>

[執行 IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md)
</dt> <dt>

[執行 IWICDevelopRaw](-wic-imp-iwicdevelopraw.md)
</dt> <dt>

[如何撰寫 WIC-Enabled 編解碼器](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows 影像處理元件總覽](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 

---
description: 對 IWICDevelopRaw 的支援
ms.assetid: 8e8ff65b-0849-42e0-924e-2a7c61d4b1bb
title: 對 IWICDevelopRaw 的支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6436eb9d9422da6f5a29c196df10c97014df6beff178bb584b70e45d207dd50d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118709728"
---
# <a name="support-for-iwicdevelopraw"></a>對 IWICDevelopRaw 的支援

為了讓應用程式能夠支援原始處理，強烈建議您使用編解碼器作者來執行 [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)的所有參數。 針對 Windows 7，Windows 影像處理元件 (WIC) 將需要所有 [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)的支援。 如果您的檔案格式不支援這些參數，則您應該修改影像檔案格式。

若要在應用程式中啟用基本的原始處理，編解碼器必須支援 (ExposureCompensationSupport) 和色彩 (的曝光調整，例如 KelvinWhitePointSupport 和 TintSupport) 。 此外，強烈建議您輸入特定的色彩空間和像素格式。 當然，對於其他調整的支援也是建議的做法，Windows 7 是必要的。

原始編解碼器必須提供映射輪替和快速預覽的基本支援。 您可以透過兩種不同的方式來指定旋轉：

-   [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)：：[**SetRotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) 方法。 這個方法會針對後續呼叫 [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels)的輸出，設定所需的旋轉角度。
-   [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)：：[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) 方法。 呼叫端可以設定 dstTransform 選項，以指出所需的旋轉角度。

這兩種方法的差異如下：

-   只有 [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) 設定可以跨解碼器物件的實例來保存。
-   [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)：：[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) 只適用于該特定呼叫;沒有任何類型的持續性。
-   [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) 可提供更細微的旋轉控制。 [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)：：[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) 受限於90度的增量。

如果在 [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) 和 [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)中同時指定了旋轉，則旋轉效果會是累計的。 例如，如果 [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) 指定25度的旋轉，而 [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) 指定90度的旋轉，則應該會發生下列情況：

-   [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)：：[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels)的呼叫應該套用25度的旋轉 (也就是，只有 [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)) 中指定的數量。
-   若呼叫 [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)：：[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) ，dstTransform 90，則會產生115度的旋轉 (25 + 90) 。
-   同樣地，只有透過 [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)：：[**SetRotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) 指定的25度旋轉才能保存。

在 Windows Vista 中， [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)：：[**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail)和 [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)：：[**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview)方法可讓呼叫者分別取得內嵌縮圖和預覽影像。 這些是為了從影像檔案串流傳回預先計算的預覽和縮圖。 「立即產生預覽或縮圖」會導致 Windows 檔案總管和相片檢視器的效能不佳。 當使用者執行處理設定的互動式控制時，編解碼器也必須提供方法，以快速傳回更新的螢幕解析度映射。

[**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)：：[**SetRenderMode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrendermode)的呼叫將會決定後續呼叫 [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)：：[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels)會傳回 (favoring 的速度或品質) 。 此外，IWICBitmapSourceTransform 介面可以用來判斷是否需要縮減取樣，而且可以在套用時提高效能。 所有影像的色彩精確度應該是可比較的。 對處理設定進行變更時，這些轉譯都應該反映變更。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[Windows映射處理元件總覽](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[相機原始影像格式的 WIC 指導方針](-wic-rawguidelines.md)
</dt> <dt>

[如何撰寫 WIC-Enabled 編解碼器](-wic-howtowriteacodec.md)
</dt> </dl>

 

 




---
description: 深入瞭解：實施 WIC-Enabled 的解碼器
ms.assetid: a26a592d-42ef-4690-95b4-48a5324be75a
title: 執行 WIC-Enabled 的解碼器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ebd6d56258bf18e6cc914a40efa4cd3a57a92fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850647"
---
# <a name="implementing-a-wic-enabled-decoder"></a>執行 WIC-Enabled 的解碼器


執行 Windows 影像處理元件 (WIC) 解碼器需要撰寫兩個類別。 這些類別上的介面直接對應至[Windows 影像處理元件運作方式](-wic-howwicworks.md)的[解碼](-wic-howwicworks.md)章節中所述的解碼器責任。

其中一個類別會提供容器層級的服務，並執行 [IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md) 介面。 如果您的影像格式支援容器層級的中繼資料，您也必須在這個類別上執行 [IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md) 介面。 建議您在解碼器和編碼器上同時支援 [IWICBitmapCodecProgressNotification](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md) 介面，以支援更佳的使用者體驗。

您將會執行的另一個類別會提供框架層級的服務，並對容器中的每個框架執行映射位的實際解碼。 這個類別會實 [IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md) 介面和 [IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md) 介面。 如果您要撰寫原始格式的解碼器，也可以在這個類別上執行 [IWICDevelopRaw](-wic-imp-iwicdevelopraw.md) 介面。 除了所需的介面，強烈建議您在此類別上執行 [IWICBitmapSourceTransform](-wic-imp-iwicmetadatablockreader.md) 介面，以針對您的影像格式啟用最佳的可能效能。

WIC 提供的其中一個物件是 [**ImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)。 您經常使用此物件上的 [**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) 介面來建立各種元件。 因為通常會使用它，所以您應該將它的參考保留為您的解碼器和編碼器類別的成員屬性。


```C++
IWICImagingFactory* m_pImagingFactory = NULL;
IWICComponentFactory* m_pComponentFactory = NULL;
HRESULT hr;
      
hr = CoCreateInstance(CLSID_WICImagingFactory, NULL,
  CLSCTX_INPROC_SERVER, IID_IWICImagingFactory,
  (LPVOID*) m_pImagingFactory);

hr = m_pImagingFactory->QueryInterface(
  IID_IWICComponentFactory, (void**)&m_pComponentFactory);
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[Windows 影像處理元件的運作方式](-wic-howwicworks.md)
</dt> <dt>

[解碼器介面](-wic-decoderinterfaces.md)
</dt> <dt>

[如何撰寫 WIC-Enabled 編解碼器](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows 影像處理元件總覽](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[WIC 中繼資料總覽](-wic-about-metadata.md)
</dt> <dt>

[編碼總覽](-wic-creating-encoder.md)
</dt> </dl>

 

 




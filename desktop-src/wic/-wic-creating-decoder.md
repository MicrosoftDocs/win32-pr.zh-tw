---
description: 本主題介紹點陣圖解碼（核心 Windows 影像處理元件 (WIC) 編解碼器元件，用來從資料流程解碼影像檔案。
ms.assetid: 9dc8d2ec-5cc5-45fa-8a4d-5bdc3072c90c
title: 解碼總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a15e6a9c914cfa220e1aad5bff4badeb8fc8cc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320924"
---
# <a name="decoding-overview"></a>解碼總覽

本主題介紹點陣圖解碼（核心 Windows 影像處理元件 (WIC) 編解碼器元件，用來從資料流程解碼影像檔案。

本主題包含下列各節。

-   [簡介](#introduction)
-   [原生點陣圖解碼器](#native-bitmap-decoders)
-   [建立點陣圖解碼器](#creating-a-bitmap-decoder)
-   [解碼器擴充性](#decoder-extensibility)
-   [相關主題](#related-topics)

## <a name="introduction"></a>簡介

您可以將點陣圖解碼器視為數位影像的外部容器，並提供全域屬性和影像框架的存取權。 某些影像格式支援全域縮圖、預覽、色彩內容或中繼資料，而有些則只在框架層級提供這些屬性。 不過請注意，許多標準影像格式都不支援這些全域屬性。 因此，WIC 提供的許多原生編解碼器，都不支援這些全域屬性的大部分。 如需全域屬性支援的相關資訊，請參閱本主題的「原生點陣圖解碼器」一節中的表格。

在 WIC 中，點陣圖解碼器會以 [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) 介面表示，並可讓您存取點陣圖的這些全域屬性，更重要的是它所包含的框架。 [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)介面代表個別的點陣圖框架，在 [點陣圖來源總覽](-wic-bitmapsources.md)中會詳細討論。

## <a name="native-bitmap-decoders"></a>原生點陣圖解碼器

WIC 針對標準的 web 影像格式和高動態範圍的 HD 相片格式，提供 [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) 介面的數個原生實作為。 下表列出可用的原生解碼器、類別識別碼名稱，以及全域屬性的支援。 雖然功能可能不支援全域層級的縮圖等屬性，但影像格式可能會在個別的框架層級支援這類屬性。



| 映像格式 | CLSID 名稱            | 縮圖 | 預覽 | 色彩內容 | 中繼資料 |
|--------------|-----------------------|------------|----------|----------------|----------|
| BMP          | CLSID \_ WICBmpDecoder  | 否         | 否       | 否             | 否       |
| GIF          | CLSID \_ WICGifDecoder  | 否         | 否       | 否             | 是      |
| ICO          | CLSID \_ WICIcoDecoder  | 否         | 否       | 否             | 否       |
| JPEG         | CLSID \_ WICJpegDecoder | 否         | 否       | 否             | 否       |
| PNG          | CLSID \_ WICPngDecoder  | 否         | 否       | 否             | 否       |
| TIFF         | CLSID \_ WICTiffDecoder | 否         | 否       | 否             | 否       |
| HD 相片     | CLSID \_ WICWmpDecoder  | 否         | 是      | 否             | 否       |



 

## <a name="creating-a-bitmap-decoder"></a>建立點陣圖解碼器

若要使用 WIC 解碼影像，您必須先針對目標影像格式建立 [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) 的實例。 如果支援，則可讓您存取全域屬性和中繼資料，以及影像框架。 WIC 影像處理 factory [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)提供數種建立點陣圖解碼器的方法。 提供下列 factory 方法來建立點陣圖解碼器。

-   [**CreateDecoder**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoder)
-   [**CreateDecoderFromFileHandle**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilehandle)
-   [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename)
-   [**CreateDecoderFromStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream)

下列程式碼示範如何使用映射檔案名建立點陣圖解碼器，以及抓取影像的第一個畫面格。


```C++
   // Create a decoder
   IWICBitmapDecoder *pDecoder = NULL;

   hr = m_pIWICFactory->CreateDecoderFromFilename(
       szFileName,                      // Image to be decoded
       NULL,                            // Do not prefer a particular vendor
       GENERIC_READ,                    // Desired read access to the file
       WICDecodeMetadataCacheOnDemand,  // Cache metadata when needed
       &pDecoder                        // Pointer to the decoder
       );

   // Retrieve the first frame of the image from the decoder
   IWICBitmapFrameDecode *pFrame = NULL;

   if (SUCCEEDED(hr))
   {
       hr = pDecoder->GetFrame(0, &pFrame);
   }
```



## <a name="decoder-extensibility"></a>解碼器擴充性

WIC 的其中一個核心功能是擴充性架構，可讓編解碼器開發人員開發自己的映射編解碼器，並取得與映射編解碼器原生執行相同的平臺支援。 不論影像格式為何，都使用單一、一致的介面集來處理所有圖像。 任何使用 WIC 的應用程式都會在安裝編解碼器時立即取得新映射格式的自動支援。 如需有關編解碼器開發的詳細資訊，請參閱 [元件開發](-wic-component-development.md)中的主題。 如需有關如何開發的詳細資訊，請參閱 [執行 WIC-Enabled 的解碼器](-wic-implementingwicdecoder.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[Windows 影像處理元件總覽](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[編碼總覽](-wic-creating-encoder.md)
</dt> <dt>

[元件開發](-wic-component-development.md)
</dt> </dl>

 

 




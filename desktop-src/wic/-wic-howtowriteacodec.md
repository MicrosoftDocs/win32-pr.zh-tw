---
description: 本主題將為開發人員提供有關如何執行可在 Windows 影像處理元件 (WIC) framework 中運作之圖像檔案格式編解碼器的指引。
ms.assetid: 58f03dc2-cc31-4d76-b75a-f332da1f900f
title: 如何撰寫 WIC-Enabled 編解碼器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee694d9a857781e97a31cb37f5ef18c518dae964
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849507"
---
# <a name="how-to-write-a-wic-enabled-codec"></a>如何撰寫 WIC-Enabled 編解碼器

本主題將為開發人員提供有關如何執行可在 Windows 影像處理元件 (WIC) framework 中運作之圖像檔案格式編解碼器的指引。

<dl>

[簡介](-wic-howtowriteacodec-intro.md)  
[Windows 影像處理元件 (WIC) 的運作方式](-wic-howwicworks.md)  
<dl>

[探索和仲裁](-wic-howwicworks.md)  
[解碼](-wic-howwicworks.md)  
[編碼方式](-wic-howwicworks.md)  
[編解碼器的存留期](-wic-howwicworks.md)  
[如何 WIC-啟用編解碼器](-wic-howwicworks.md)  
[WIC 中的多執行緒單元支援](-wic-howwicworks.md)  
</dl> </dd> <a href="-wic-implementingwicdecoder.md">執行 WIC-Enabled 的解碼器</a><dl>

[解碼器介面](-wic-decoderinterfaces.md)<dl>

[IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md)  
[IWICBitmapCodecProgressNotification](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md)  
[IWICBitmapSource](-wic-imp-iwicbitmapsource.md)  
[IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md)  
[IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md)  
[IWICBitmapSourceTransform](-wic-imp-iwicbitmapsourcetransform.md)  
[IWICDevelopRaw](-wic-imp-iwicdevelopraw.md)  
</dl> </dd> </dl> </dd> <a href="-wic-implementingwicencoder.md">執行 WIC-Enabled 編碼器</a>  
<dl>

[編碼器介面](-wic-encoderinterfaces.md)  
<dl>

[IWICBitmapEncoder](-wic-imp-iwicbitmapencoder.md)  
[IWICBitmapCodecProgressNotification](-wic-imp-iwicbitmapcodecprogressnotification-encoder.md)  
[IWICBitmapFrameEncode](-wic-imp-iwicbitmapframeencode.md)  
[IWICMetadataBlockWriter](-wic-imp-iwicmetadatablockwriter.md)  
</dl> </dd> </dl> </dd> <a href="-wic-codecinstallandreg.md">編解碼器安裝和註冊</a>  
<dl>

[註冊編解碼器](-wic-codecinstallandreg.md)  
<dl>

[一般註冊專案](-wic-generalregentries.md)  
[編碼器特定的登錄專案](-wic-encoderregentries.md)  
<dl>

[使用中繼資料寫入器註冊容器格式](-wic-encoderregentries.md)  
</dl> </dd> <a href="-wic-decoderregentries.md">編碼器特定的登錄專案</a>  
<dl>

[使用中繼資料讀取器註冊新的容器格式](-wic-decoderregentries.md)  
</dl> </dd> <a href="-wic-integrationregentries.md">與 Windows Vista PhotoGallery 和 Explorer 整合</a>  
<dl>

[Windows 屬性儲存區](-wic-integrationregentries.md)  
[Windows Vista 影像中心](-wic-integrationregentries.md)  
[Windows Vista 縮圖快取](-wic-integrationregentries.md)  
</dl> </dd> </dl> </dd> <a href="-wic-codecinstallandreg.md">安裝編解碼器時，更新縮圖</a>快取，[讓使用者可以使用 WIC-Enabled 編解碼器的](-wic-codecinstallandreg.md)</dl> </dd> <a href="-wic-howtowriteacodec-conclusion.md">結論</a>  
</dl>

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[簡介 (如何撰寫 WIC-Enabled 編解碼器) ](-wic-howtowriteacodec-intro.md)
</dt> <dt>

[Windows 影像處理元件總覽](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 




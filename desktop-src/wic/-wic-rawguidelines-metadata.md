---
description: 中繼資料支援
ms.assetid: f3b4a3d9-a353-4af8-9998-cb7da7a062b7
title: 中繼資料支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32499a88bd9cc12186629476f4d9f32a6e811858
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988341"
---
# <a name="metadata-support"></a>中繼資料支援

未經處理的格式也應該支援 Windows 中映射的一般中繼資料讀取和寫入案例。 Microsoft 開發了一組原生中繼資料提供者來交換影像檔案 (的 EXIF) 、國際新聞電訊委員會 (IPTC) ，以及可延伸的中繼資料平臺 (目前僅針對 TIFF 和 JPEG 容器叫用的 XMP) 中繼資料。 如果原始影像儲存為這些容器格式的其中一種，建議使用 Windows 內建的中繼資料提供者。 不過，編解碼器作者必須負責正確設定。 對於不是以 TIFF 容器為基礎的原始檔案，可能需要執行 EXIF、IPTC 或 XMP 寫入器，因為內建的讀取器和寫入器預期資料必須符合 EXIF、IPTC 和 XMP 磁片配置規格。 編解碼器作者也可以針對任何自訂中繼資料來執行自己的提供者。

因為 Windows 影像處理元件 (WIC) 的架構，所以只能透過影像編碼器的實例叫用中繼資料寫入器。 因此，原始格式的擁有者應建立至少一個 "stub" [**WICRawParameterSet. WICAutoAdjustedParameterSet**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawparameterset) 編碼器，即使實際的圖元編碼為未經處理的格式也不會執行。 編解碼器作者必須叫用正確的元資料處理程式：

-   視需要在解碼器和框架解碼器上 [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) 。
-   視需要在編碼器和框架編碼器上 [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) 。

若要在 Windows Vista 中支援映射處理應用程式中的所有預期案例，建議使用編解碼器廠商至少支援下列各項：

-   EXIF 讀取
-   部分 EXIF 寫入 (，以允許更新來捕捉日期和時間) 
-   XMP 讀取和寫入 (包括適用于 XMP 的選擇性 IPTC 核心) 
-   IPTC IIMv4 讀取和寫入

大部分的中繼資料存取 (Windows Vista 中的讀取和寫入) 都會透過 [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) 或 [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) 介面進行。 因此，若要參與 Windows Vista 中繼資料的體驗，原始編解碼器作者必須執行 [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)：：[**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) 和 [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)：：[**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) 方法。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[Windows 影像處理元件總覽](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[相機原始影像格式的 WIC 指導方針](-wic-rawguidelines.md)
</dt> <dt>

[如何撰寫 WIC-Enabled 編解碼器](-wic-howtowriteacodec.md)
</dt> </dl>

 

 




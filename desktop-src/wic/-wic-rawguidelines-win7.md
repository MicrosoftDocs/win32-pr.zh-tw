---
description: Windows 7 的原始編解碼器需求
ms.assetid: 3f8bd336-ba03-4ffb-9aa2-ea55a276e3bc
title: Windows 7 的原始編解碼器需求
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e0c4d04175eab1b6e68ac87ed18a648fa4655b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980376"
---
# <a name="raw-codec-requirements-for-windows-7"></a>Windows 7 的原始編解碼器需求

至少需要下列編解碼器功能：

Windows Vista shell 和影像中心支援所需的所有功能：縮圖、預覽和 (保存) 旋轉。 原始處理應該預設為適當的進行中設定。

支援核心中繼資料 (讀取和寫入) 、非 EXIF 中繼資料以及 EXIF 中繼資料）都必須保存在未經處理的檔案格式中，而不需要使用側車檔。

[**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)介面的支援。 在 Windows 7 中，Windows 影像處理元件 (WIC) WIC 需要實 [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) 所公開的所有參數介面。

方向狀態支援：

-   應使用 [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)：：[**SetRotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) 方法來套用90度階的影像旋轉。 應用程式和 Windows 會使用這個方法，將影像 (和快取的縮圖和預覽) 旋轉。
-   使用此 API 的旋轉應用程式也應該由編解碼器保存 (請參閱本檔中稍早的) 。
-   應用程式可以使用 [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) API 的旋轉功能，但編解碼器不會序列化此 api 上的任何旋轉設定，因此使用 [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) 完成的旋轉將不會保存。

高速縮圖和預覽解壓縮支援。 如果最大的圖元尺寸 (寬度或高度) 小於1024圖元，Windows Vista 將會要求螢幕預覽的呈現：

-   [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)：：[**SetRenderMode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrendermode)方法應該至少支援 [**WICRawRenderQualityDraftMode**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawrendermode)和 [**WICRawRenderQualityBestQuality**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawrendermode)模式，以允許更快速地轉譯縮圖和預覽，而非全品質模式。
-   Windows 會使用要求的螢幕解析度大小來呼叫 [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)：：[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) 。
-   上述 API 必須支援螢幕解析度大小。
-   需要 [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) 縮圖、預覽和全映射位的一致性影像處理。

高動態範圍 (HDR) 像素格式。

XML 檔規格 (XPS) 列印。

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

 

 




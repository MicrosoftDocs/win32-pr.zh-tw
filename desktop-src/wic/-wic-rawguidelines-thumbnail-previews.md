---
description: 縮圖和預覽
ms.assetid: e45f025e-a1ac-47c8-b794-ab1402ab35fb
title: 縮圖和預覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 110b0f4da08eaf2b17582dabec1ff7bd6d4f3ab4389c6bcf7654cdb5ca3198a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119086881"
---
# <a name="thumbnails-and-previews"></a>縮圖和預覽

WindowsVista 和 Windows 影像中心依賴 Windows 影像處理元件 (WIC) ，以轉譯影像的快速縮圖和預覽。 為了支援快速縮圖和預覽轉譯，原始編解碼器必須執行 WIC [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) 和 [**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) 介面。 若要支援回應式使用者體驗，強烈希望這些介面在200毫秒以內將 [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) 傳回給呼叫者。

Microsoft 強烈建議 RAW 檔案格式的擁有者會產生資源清單預覽，並在影像檔案中快取。 針對裝置內的格式，這通常是在捕獲時間完成。 不過，每當 [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) 介面屬性變更時，也可以重新產生預覽版，並將其儲存在影像檔中-如果沒有太多工作。

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

 

 




---
description: 執行原始編解碼器的一般指導方針
ms.assetid: 47b3b226-4642-41d2-b05c-bc12583047aa
title: 執行原始編解碼器的一般指導方針
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f774e5d254330e3274daccb6062f35baa443144
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194118"
---
# <a name="general-guidelines-for-implementing-raw-codecs"></a><span data-ttu-id="b2b5b-103">執行原始編解碼器的一般指導方針</span><span class="sxs-lookup"><span data-stu-id="b2b5b-103">General Guidelines for Implementing RAW Codecs</span></span>

<span data-ttu-id="b2b5b-104">相較于非原始影像類型（例如 JPEG 或 TIFF），原始影像格式在 Windows 中的運作方式有兩個顯著差異：</span><span class="sxs-lookup"><span data-stu-id="b2b5b-104">Compared to non-RAW image types such as JPEG or TIFF, there are two notable differences in how RAW image formats are expected to behave in Windows:</span></span>

-   <span data-ttu-id="b2b5b-105">大部分的原始影像格式會假設為「唯讀」，而且可能不支援將圖元編碼為原始格式。</span><span class="sxs-lookup"><span data-stu-id="b2b5b-105">Most RAW image formats are presumed to be "read only" and probably will not support pixel encoding to RAW format.</span></span> <span data-ttu-id="b2b5b-106">不過，因為 Windows 影像處理元件 (WIC) 需要編碼器支援中繼資料回寫，所以原始編解碼器作者應計畫至少執行一個基本架構編碼器類別。</span><span class="sxs-lookup"><span data-stu-id="b2b5b-106">However, because Windows Imaging Component (WIC) requires an encoder to support metadata write-back, RAW codec authors should plan to implement at least a skeleton encoder class.</span></span>
-   <span data-ttu-id="b2b5b-107">相較于其他格式，解碼完整大小的原始影像可能需要很長的時間。</span><span class="sxs-lookup"><span data-stu-id="b2b5b-107">Decoding a full-size RAW image can take a long time compared to other formats.</span></span> <span data-ttu-id="b2b5b-108">基於這個理由，Microsoft 建議採取某些方法來將解碼延遲降至最低，並確保支援快速轉譯縮圖和預覽等案例。</span><span class="sxs-lookup"><span data-stu-id="b2b5b-108">For this reason, Microsoft recommends that certain approaches be taken to minimize decoding latency and to ensure support for scenarios such as rapid rendering of thumbnails and previews.</span></span>

    <span data-ttu-id="b2b5b-109">例如，所有原始編解碼器作者都必須執行 [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) 介面，這個介面會提供一種機制，在目標點陣圖大小之前通知編碼器，藉此啟用對較小輸出影像大小的優化解碼。</span><span class="sxs-lookup"><span data-stu-id="b2b5b-109">For example, all RAW codec authors must implement the [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) interface, which provides a mechanism to notify the decoder in advance of the target bitmap size, thus enabling optimized decoding to a smaller output image size.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b2b5b-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="b2b5b-110">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="b2b5b-111">**概念**</span><span class="sxs-lookup"><span data-stu-id="b2b5b-111">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b2b5b-112">Windows 影像處理元件總覽</span><span class="sxs-lookup"><span data-stu-id="b2b5b-112">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="b2b5b-113">相機原始影像格式的 WIC 指導方針</span><span class="sxs-lookup"><span data-stu-id="b2b5b-113">WIC Guidelines for Camera RAW Image Formats</span></span>](-wic-rawguidelines.md)
</dt> <dt>

[<span data-ttu-id="b2b5b-114">如何撰寫 WIC-Enabled 編解碼器</span><span class="sxs-lookup"><span data-stu-id="b2b5b-114">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 




---
description: 縮圖和預覽
ms.assetid: e45f025e-a1ac-47c8-b794-ab1402ab35fb
title: 縮圖和預覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e279da9771a43eb75bb94faff23d2e6aa29c4ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106989971"
---
# <a name="thumbnails-and-previews"></a><span data-ttu-id="2a76b-103">縮圖和預覽</span><span class="sxs-lookup"><span data-stu-id="2a76b-103">Thumbnails and Previews</span></span>

<span data-ttu-id="2a76b-104">Windows Vista 和 Windows 影像中心依賴 Windows 影像處理元件 (WIC) ，以轉譯影像的快速縮圖和預覽。</span><span class="sxs-lookup"><span data-stu-id="2a76b-104">Windows Vista and the Windows Photo Gallery rely on Windows Imaging Component (WIC) to render fast thumbnails and previews of images.</span></span> <span data-ttu-id="2a76b-105">為了支援快速縮圖和預覽轉譯，原始編解碼器必須執行 WIC [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) 和 [**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) 介面。</span><span class="sxs-lookup"><span data-stu-id="2a76b-105">To support fast thumbnail and preview rendering, RAW codecs must implement the WIC [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) and [**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) interfaces.</span></span> <span data-ttu-id="2a76b-106">若要支援回應式使用者體驗，強烈希望這些介面在200毫秒以內將 [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) 傳回給呼叫者。</span><span class="sxs-lookup"><span data-stu-id="2a76b-106">To support a responsive user experience, it is highly desirable that these interfaces return an [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) to the caller in 200 milliseconds or less.</span></span>

<span data-ttu-id="2a76b-107">Microsoft 強烈建議 RAW 檔案格式的擁有者會產生資源清單預覽，並在影像檔案中快取。</span><span class="sxs-lookup"><span data-stu-id="2a76b-107">Microsoft strongly recommends that RAW file format owners generate a prerendered preview and cache this in the image file.</span></span> <span data-ttu-id="2a76b-108">針對裝置內的格式，這通常是在捕獲時間完成。</span><span class="sxs-lookup"><span data-stu-id="2a76b-108">For an in-device format, this is usually done at capture time.</span></span> <span data-ttu-id="2a76b-109">不過，每當 [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) 介面屬性變更時，也可以重新產生預覽版，並將其儲存在影像檔中-如果沒有太多工作。</span><span class="sxs-lookup"><span data-stu-id="2a76b-109">However, previews could also be regenerated and stored in the image file whenever [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) interface properties are changed-if it does not take too much work to do so.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2a76b-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="2a76b-110">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="2a76b-111">**概念**</span><span class="sxs-lookup"><span data-stu-id="2a76b-111">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="2a76b-112">Windows 影像處理元件總覽</span><span class="sxs-lookup"><span data-stu-id="2a76b-112">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="2a76b-113">相機原始影像格式的 WIC 指導方針</span><span class="sxs-lookup"><span data-stu-id="2a76b-113">WIC Guidelines for Camera RAW Image Formats</span></span>](-wic-rawguidelines.md)
</dt> <dt>

[<span data-ttu-id="2a76b-114">如何撰寫 WIC-Enabled 編解碼器</span><span class="sxs-lookup"><span data-stu-id="2a76b-114">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 




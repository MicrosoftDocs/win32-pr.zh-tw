---
description: 在 Windows 影像處理元件 (WIC) 平臺上建立編解碼器，可讓所有在 WIC 上建立的應用程式都能針對您的映射格式取得相同的平臺支援，以供平臺隨附的通用映射格式使用。
ms.assetid: 4f25f0f4-246c-4cbd-bd11-d061dbc7de45
title: '結論 (如何撰寫 WIC-Enabled 編解碼器) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de165f20ff81094c3b64d7e9667795f0bf80cef8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978993"
---
# <a name="conclusion-how-to-write-a-wic-enabled-codec"></a><span data-ttu-id="dff4c-103">結論 (如何撰寫 WIC-Enabled 編解碼器) </span><span class="sxs-lookup"><span data-stu-id="dff4c-103">Conclusion (How to Write a WIC-Enabled Codec)</span></span>

<span data-ttu-id="dff4c-104">在 Windows 影像處理元件 (WIC) 平臺上建立編解碼器，可讓所有在 WIC 上建立的應用程式都能針對您的映射格式取得相同的平臺支援，以供平臺隨附的通用映射格式使用。</span><span class="sxs-lookup"><span data-stu-id="dff4c-104">Building your codec on the Windows Imaging Component (WIC) platform makes it possible for all applications built on WIC to get the same platform support for your image format that they get for the common image formats shipped with the platform.</span></span> <span data-ttu-id="dff4c-105">它也可讓 Windows Vista 影像中心、Windows 檔案總管和相片檢視器使用您提供的解碼器，以您的格式顯示影像的縮圖和預覽。</span><span class="sxs-lookup"><span data-stu-id="dff4c-105">It also enables the Windows Vista Photo Gallery, Windows Explorer, and Photo Viewer to display thumbnails and previews of images in your format using the decoder that you provide.</span></span> <span data-ttu-id="dff4c-106">針對原始格式，它可讓更精密的影像處理應用程式充分利用您的解碼器原始處理功能。</span><span class="sxs-lookup"><span data-stu-id="dff4c-106">For raw formats, it enables more sophisticated imaging applications to take advantage of your decoder’s raw processing capabilities.</span></span> <span data-ttu-id="dff4c-107">根據您支援的編碼器選項，您也可以公開編碼器的獨特功能，讓應用程式能夠充分利用影像格式的先進功能。</span><span class="sxs-lookup"><span data-stu-id="dff4c-107">Depending on the encoder options you support, you can also expose unique capabilities of your encoder to enable applications to take full advantage of the advanced features of your image format.</span></span>

<span data-ttu-id="dff4c-108">開發已啟用 WIC 的編解碼器需要您執行一些新的介面。</span><span class="sxs-lookup"><span data-stu-id="dff4c-108">Developing a WIC-enabled codec requires you to implement some new interfaces.</span></span> <span data-ttu-id="dff4c-109">在許多情況下，您可以為現有的編解碼器撰寫可執行這些介面的包裝函式。</span><span class="sxs-lookup"><span data-stu-id="dff4c-109">In many cases, you can write a wrapper for your existing codec that implements these interfaces.</span></span> <span data-ttu-id="dff4c-110">當您安裝編解碼器時，必須建立一些登錄專案，讓 WIC 平臺可以探索編解碼器，並將其與適當的元資料處理程式產生關聯。</span><span class="sxs-lookup"><span data-stu-id="dff4c-110">When you install your codec, you must make some registry entries to make your codec discoverable by the WIC platform and associate it with the appropriate metadata handlers.</span></span> <span data-ttu-id="dff4c-111">您也必須叫用 API，以清除任何預設 (空白) 縮圖的縮圖快取，這些縮圖先前可能已與您格式的影像相關聯。</span><span class="sxs-lookup"><span data-stu-id="dff4c-111">You also need to invoke an API to clear the thumbnail cache of any default (empty) thumbnails that may have previously associated with images in your format.</span></span> <span data-ttu-id="dff4c-112">如果您想要的話，可以啟用 Windows Vista 影像中心，在影像中心遇到具有您副檔名的影像時，為使用者提供下載編解碼器的連結。</span><span class="sxs-lookup"><span data-stu-id="dff4c-112">If you want, you can enable the Windows Vista Photo Gallery to provide users with a link to download your codec when the Photo Gallery encounters an image with your file name extension.</span></span> <span data-ttu-id="dff4c-113">若要這樣做，您必須為 Microsoft 提供您的編解碼器副檔名的相關資訊，以及下載網站的 URL。</span><span class="sxs-lookup"><span data-stu-id="dff4c-113">To do this, you must provide Microsoft with information about your codec’s file name extension and the URL for your download site.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dff4c-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="dff4c-114">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="dff4c-115">**概念**</span><span class="sxs-lookup"><span data-stu-id="dff4c-115">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="dff4c-116">編解碼器安裝和註冊</span><span class="sxs-lookup"><span data-stu-id="dff4c-116">CODEC Installation and Registration</span></span>](-wic-codecinstallandreg.md)
</dt> <dt>

[<span data-ttu-id="dff4c-117">如何撰寫 WIC-Enabled 編解碼器</span><span class="sxs-lookup"><span data-stu-id="dff4c-117">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="dff4c-118">Windows 影像處理元件總覽</span><span class="sxs-lookup"><span data-stu-id="dff4c-118">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 




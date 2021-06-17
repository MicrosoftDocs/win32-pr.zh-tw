---
title: 美工檔案格式
description: 瞭解 Windows Media Player 為面板辨識的藝術檔案格式。 這些包括點陣圖、GIF、JPEG 和 PNG。
ms.assetid: 803479e8-0e00-4724-80b7-9d86709c43db
keywords:
- Windows Media Player 的外觀、美工檔案
- 外觀、美工檔案
- 適用于外觀、藝術的檔案
- 面板的美工檔案，檔案格式
- Windows Media Player 的外觀、圖案的檔案格式
- 圖案的外觀、檔案格式
- 面板封面的檔案格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b525bc316d6a9901e32e51a54b6fb938fa91208
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262210"
---
# <a name="art-file-formats"></a><span data-ttu-id="e1ef4-111">美工檔案格式</span><span class="sxs-lookup"><span data-stu-id="e1ef4-111">Art File Formats</span></span>

<span data-ttu-id="e1ef4-112">適用于面板的 Windows Media Player 可辨識下列藝術檔案格式：</span><span class="sxs-lookup"><span data-stu-id="e1ef4-112">The following art file formats are recognized by Windows Media Player for skins:</span></span>



| <span data-ttu-id="e1ef4-113">格式</span><span class="sxs-lookup"><span data-stu-id="e1ef4-113">Format</span></span>                                  | <span data-ttu-id="e1ef4-114">分機</span><span class="sxs-lookup"><span data-stu-id="e1ef4-114">Extension</span></span>   | <span data-ttu-id="e1ef4-115">描述</span><span class="sxs-lookup"><span data-stu-id="e1ef4-115">Description</span></span>                                                                                        |
|-----------------------------------------|-------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1ef4-116">點陣圖</span><span class="sxs-lookup"><span data-stu-id="e1ef4-116">Bitmap</span></span>                                  | <span data-ttu-id="e1ef4-117">.bmp</span><span class="sxs-lookup"><span data-stu-id="e1ef4-117">.bmp</span></span>        | <span data-ttu-id="e1ef4-118">建議使用點陣圖影像，因為它們提供對確切影像和色彩的最大控制權。</span><span class="sxs-lookup"><span data-stu-id="e1ef4-118">Bitmap images are recommended because they offer the most control over the exact image and colors.</span></span> |
| <span data-ttu-id="e1ef4-119">圖形交換格式 (GIF)</span><span class="sxs-lookup"><span data-stu-id="e1ef4-119">Graphics Interchange Format (GIF)</span></span>       | <span data-ttu-id="e1ef4-120">.gif</span><span class="sxs-lookup"><span data-stu-id="e1ef4-120">.gif</span></span>        | <span data-ttu-id="e1ef4-121">用於網頁的壓縮影像格式。</span><span class="sxs-lookup"><span data-stu-id="e1ef4-121">Compressed image format used for webpages.</span></span> <span data-ttu-id="e1ef4-122">支援動畫 Gif。</span><span class="sxs-lookup"><span data-stu-id="e1ef4-122">Animated GIFs are supported.</span></span>                            |
| <span data-ttu-id="e1ef4-123">JPEG 格式 (JPEG)</span><span class="sxs-lookup"><span data-stu-id="e1ef4-123">Joint Photographic Experts Group (JPEG)</span></span> | <span data-ttu-id="e1ef4-124">.jpeg、.jpg</span><span class="sxs-lookup"><span data-stu-id="e1ef4-124">.jpeg, .jpg</span></span> | <span data-ttu-id="e1ef4-125">用於網頁的壓縮影像格式。</span><span class="sxs-lookup"><span data-stu-id="e1ef4-125">Compressed image format used for webpages.</span></span>                                                         |
| <span data-ttu-id="e1ef4-126">可攜式網路圖形 (PNG)</span><span class="sxs-lookup"><span data-stu-id="e1ef4-126">Portable Network Graphics (PNG)</span></span>         | <span data-ttu-id="e1ef4-127">.png</span><span class="sxs-lookup"><span data-stu-id="e1ef4-127">.png</span></span>        | <span data-ttu-id="e1ef4-128">用於網頁的壓縮影像格式。</span><span class="sxs-lookup"><span data-stu-id="e1ef4-128">Compressed image format used for webpages.</span></span>                                                         |



 

<span data-ttu-id="e1ef4-129">如果您使用其中一種壓縮檔案格式來定義網頁瀏覽器的透明色彩，請勿在影像檔中將色彩定義為透明。</span><span class="sxs-lookup"><span data-stu-id="e1ef4-129">If you use one of the compressed file formats that defines a color as transparent to a Web browser, do not define a color as transparent in the image file.</span></span> <span data-ttu-id="e1ef4-130">使用可見色彩表示影像中的透明區域，然後在外觀定義檔中將該色彩定義為透明。</span><span class="sxs-lookup"><span data-stu-id="e1ef4-130">Use a visible color to represent transparent areas in your image, and then define that color as transparent in the skin definition file.</span></span> <span data-ttu-id="e1ef4-131">例如，如果您建立的 GIF 檔案中有些區域是透明的，則在您的最終影像中將不會是透明的，而且您將無法使用在您的 GIF 檔案中設定為透明的色彩來呈現您的外觀。</span><span class="sxs-lookup"><span data-stu-id="e1ef4-131">For example, if you create a GIF file with some areas transparent, they will not be transparent in your final image and you will not be able to use the color you set as transparent in your gif file for the transparency color in your skin.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e1ef4-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="e1ef4-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1ef4-133">**美工檔案**</span><span class="sxs-lookup"><span data-stu-id="e1ef4-133">**Art Files**</span></span>](art-files.md)
</dt> </dl>

 

 





---
title: Super 檔案
description: Super 檔案
ms.assetid: a5005d1a-4b87-482d-914e-3184a2c93267
keywords:
- Windows Media Player 行動外觀、美工檔案
- 外觀、美工檔案
- 適用于外觀、藝術的檔案
- 適用于面板的美工圖案、超級檔案檔案
- Windows Media Player 行動外觀、超級檔案檔案
- 外觀，超級檔
- 外觀中的超級檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ece533f81f8866eb0f9848d7296cc23bcd37f453
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106990879"
---
# <a name="super-files"></a><span data-ttu-id="49882-110">Super 檔案</span><span class="sxs-lookup"><span data-stu-id="49882-110">Super Files</span></span>

<span data-ttu-id="49882-111">Super 檔案是用來儲存已停用的 trackbars 映射。</span><span class="sxs-lookup"><span data-stu-id="49882-111">Super files are used to store the Disabled images for trackbars.</span></span> <span data-ttu-id="49882-112">由於主要的 [顯示檔] 影像會顯示在背景檔案中，而使用者可點擊 thumb 影像，而不是 [顯示] 影像，因此 trackbars 只需要停用的影像。</span><span class="sxs-lookup"><span data-stu-id="49882-112">Because the main trackbar image is displayed in the Background file, and the user taps on the thumb image, not the trackbar image, only the Disabled image is needed for trackbars.</span></span> <span data-ttu-id="49882-113">它會儲存在面板定義檔的點陣圖區段中，由 Super 所定義的檔案中。</span><span class="sxs-lookup"><span data-stu-id="49882-113">It is stored in the file defined by Super in the Bitmaps section of the skin definition file.</span></span> <span data-ttu-id="49882-114">超級檔案也可以針對其他按鈕（例如靜音）儲存已推送和停用的影像，而不需要是點擊類型按鈕。</span><span class="sxs-lookup"><span data-stu-id="49882-114">A Super file can also store the Pushed and Disabled images for other buttons such as Mute, which is not required to be a hit-type button.</span></span>

> [!Note]  
> <span data-ttu-id="49882-115">在 Windows Media Player 10 行動版或更新版本的外觀中不會使用最新的檔，因為搜尋 trackbars 的已停用影像位於 seekthumb 檔案中。</span><span class="sxs-lookup"><span data-stu-id="49882-115">Super art files are not used in skins for Windows Media Player 10 Mobile or later because the disabled images for seek trackbars are located in the seekthumb file.</span></span>

 

<span data-ttu-id="49882-116">下圖是一般的超級檔案。</span><span class="sxs-lookup"><span data-stu-id="49882-116">The following image is a typical Super file.</span></span>

![super 檔案](images/cesdksup.png)

<span data-ttu-id="49882-118">這會儲存已停用的 trackbars 影像和靜音按鈕。</span><span class="sxs-lookup"><span data-stu-id="49882-118">This stores the disabled images for the trackbars and the mute button.</span></span> <span data-ttu-id="49882-119">這些影像是依點陣圖區段所定義的位移。</span><span class="sxs-lookup"><span data-stu-id="49882-119">These images are offset as defined by the Bitmaps section.</span></span>

<span data-ttu-id="49882-120">已停用的 [已停用的檔] 影像的背景區域，與背景檔案中的對應區域完全相符。</span><span class="sxs-lookup"><span data-stu-id="49882-120">The background area of the disabled trackbar image exactly matches the corresponding area in the Background file.</span></span> <span data-ttu-id="49882-121">這點很重要，因為針對已停用的 [檢視器] 影像定義的整個矩形將會取代背景檔案中的相符區域。</span><span class="sxs-lookup"><span data-stu-id="49882-121">This is important, because the entire rectangle defined for the disabled trackbar image will replace the matching area in the Background file.</span></span> <span data-ttu-id="49882-122">這可確保停用的 [貼幅] 影像可順暢地混合到背景影像。</span><span class="sxs-lookup"><span data-stu-id="49882-122">This ensures that the disabled trackbar image blends seamlessly into the background image.</span></span>

## <a name="related-topics"></a><span data-ttu-id="49882-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="49882-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="49882-124">**美工檔案**</span><span class="sxs-lookup"><span data-stu-id="49882-124">**Art Files**</span></span>](art-files-mobile.md)
</dt> </dl>

 

 





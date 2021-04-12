---
title: 推送的檔案
description: 推送的檔案
ms.assetid: bea803d2-1237-4983-9673-afdcddc32748
keywords:
- Windows Media Player 行動外觀、美工檔案
- 外觀、美工檔案
- 適用于外觀、藝術的檔案
- 面板的美工檔案，推送的檔案
- Windows Media Player 行動面板，推送的檔案
- 外觀，推送的檔案
- 面板中推送的檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 071a6a4fd00eee7040d2fadb8fb80db343dc0ac6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372273"
---
# <a name="pushed-file"></a><span data-ttu-id="fa8cf-110">推送的檔案</span><span class="sxs-lookup"><span data-stu-id="fa8cf-110">Pushed File</span></span>

<span data-ttu-id="fa8cf-111">推送的檔案包含當使用者按下按鈕時將顯示的影像。</span><span class="sxs-lookup"><span data-stu-id="fa8cf-111">The Pushed file contains the images that will be displayed when the user taps on a button.</span></span> <span data-ttu-id="fa8cf-112">您也可以在 [PlayPause] 按鈕的暫停狀態中包含正常和推送的影像。</span><span class="sxs-lookup"><span data-stu-id="fa8cf-112">You can also include the normal and pushed images for the pause state of the PlayPause button.</span></span>

<span data-ttu-id="fa8cf-113">下圖是典型的推送檔案。</span><span class="sxs-lookup"><span data-stu-id="fa8cf-113">The following image is a typical Pushed file.</span></span>

![推送的檔案](images/cesdkpus.png)

<span data-ttu-id="fa8cf-115">這會儲存在點擊點擊類型按鈕時所顯示的影像。</span><span class="sxs-lookup"><span data-stu-id="fa8cf-115">This stores the images that will be displayed when the hit-type buttons are tapped.</span></span> <span data-ttu-id="fa8cf-116">也儲存在此檔案中，是 PlayPause 按鈕暫停影像的一般和推送映射。</span><span class="sxs-lookup"><span data-stu-id="fa8cf-116">Also stored in this file are the normal and pushed images for the paused image of the PlayPause button.</span></span> <span data-ttu-id="fa8cf-117">除了右邊的 PlayPause 次要影像之外，另一個按鈕影像會以背景影像對齊，並使用在面板定義檔的 [點陣圖] 區段中定義的位移。</span><span class="sxs-lookup"><span data-stu-id="fa8cf-117">Except for the PlayPause secondary images on the right, the other button images line up with the Background image, using the offset defined in the Bitmaps section of the skin definition file.</span></span>

<span data-ttu-id="fa8cf-118">請注意，按鈕影像的背景完全符合背景檔案中對應的區域。</span><span class="sxs-lookup"><span data-stu-id="fa8cf-118">Notice that the background of the button image exactly matches the corresponding area in the Background file.</span></span> <span data-ttu-id="fa8cf-119">這點很重要，因為當使用者按下 [點擊類型] 按鈕時，針對推送影像定義的整個矩形將會取代背景檔案中的相符區域。</span><span class="sxs-lookup"><span data-stu-id="fa8cf-119">This is important, because when the user taps a hit-type button, the entire rectangle defined for the pushed image will replace the matching area in the Background file.</span></span> <span data-ttu-id="fa8cf-120">讓圖形保持與背景影像一致，以確保只有您想要顯示的按鈕部分會實際變更。</span><span class="sxs-lookup"><span data-stu-id="fa8cf-120">Keep the graphic consistent with the background image to ensure that only the parts of the button that you want to appear different will actually change.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fa8cf-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="fa8cf-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa8cf-122">**美工檔案**</span><span class="sxs-lookup"><span data-stu-id="fa8cf-122">**Art Files**</span></span>](art-files-mobile.md)
</dt> </dl>

 

 





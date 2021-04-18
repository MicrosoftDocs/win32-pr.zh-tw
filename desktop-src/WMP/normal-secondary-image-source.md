---
title: 一般次要影像來源
description: 一般次要影像來源
ms.assetid: fe5c0da2-0c40-456f-ab56-ac61ed69ff2d
keywords:
- Windows Media Player 行動外觀、按鈕影像來源
- 外觀，按鈕影像來源
- 外觀、按鈕的參考
- 外觀、影像來源中的按鈕
- 外觀、按鈕的影像來源
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06ff828f6d0f0c8348453cb00fef04ab31718693
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968658"
---
# <a name="normal-secondary-image-source"></a><span data-ttu-id="1a56e-108">一般次要影像來源</span><span class="sxs-lookup"><span data-stu-id="1a56e-108">Normal Secondary Image Source</span></span>

<span data-ttu-id="1a56e-109">視按鈕功能而定，您可能需要為按鈕的次要狀態定義正常影像的位置。</span><span class="sxs-lookup"><span data-stu-id="1a56e-109">Depending on the button function, you may need to define the location of the normal image for the secondary state of the button.</span></span> <span data-ttu-id="1a56e-110">這會是使用者第一次推送 PlayPause 函式按鈕時所看到的影像。</span><span class="sxs-lookup"><span data-stu-id="1a56e-110">This will be the image users see when they push a PlayPause function button the first time.</span></span>

<span data-ttu-id="1a56e-111">若要定義此影像，您必須輸入映射類型，後面接著一個空格和 @ 符號以及另一個空格。</span><span class="sxs-lookup"><span data-stu-id="1a56e-111">To define this image, you must enter the image type followed by a space and the @ symbol and another space.</span></span> <span data-ttu-id="1a56e-112">然後，您必須輸入兩個正整數，以定義您想要在繪圖來源的點陣圖類型內使用之影像的左上座標 (（以圖元為單位）) 。</span><span class="sxs-lookup"><span data-stu-id="1a56e-112">You must then enter two positive integers that define the top-left coordinates (in pixels) of the image you want to use inside the bitmap type you are drawing from.</span></span>

<span data-ttu-id="1a56e-113">例如，若要定義次要影像來源的一般影像，如果您的映射位於推播點陣圖內，請輸入：</span><span class="sxs-lookup"><span data-stu-id="1a56e-113">For example, to define the normal image for a secondary image source, if your image is inside the Pushed bitmap, type:</span></span>


```C++
Pushed @ 210,0

```



<span data-ttu-id="1a56e-114">次要狀態不能有已停用的映射。</span><span class="sxs-lookup"><span data-stu-id="1a56e-114">Secondary states cannot have a Disabled image.</span></span> <span data-ttu-id="1a56e-115">次要影像會假設為與主要映射相同的寬度和高度。</span><span class="sxs-lookup"><span data-stu-id="1a56e-115">Secondary images are assumed to be the same width and height as the primary image.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1a56e-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="1a56e-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1a56e-117">**按鈕**</span><span class="sxs-lookup"><span data-stu-id="1a56e-117">**Buttons**</span></span>](buttons.md)
</dt> </dl>

 

 





---
title: 推送的次要影像來源
description: 推送的次要影像來源
ms.assetid: f2a2380d-c876-456b-837b-01b3997d81f2
keywords:
- Windows Media Player 行動外觀、按鈕影像來源
- 外觀，按鈕影像來源
- 外觀、按鈕的參考
- 外觀、影像來源中的按鈕
- 外觀、按鈕的影像來源
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6de50f72c8af34fa4f3e44507e172cae6890dc47
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021523"
---
# <a name="pushed-secondary-image-source"></a><span data-ttu-id="2e2e5-108">推送的次要影像來源</span><span class="sxs-lookup"><span data-stu-id="2e2e5-108">Pushed Secondary Image Source</span></span>

<span data-ttu-id="2e2e5-109">視按鈕功能而定，您可能需要為按鈕的次要狀態定義推送影像的位置。</span><span class="sxs-lookup"><span data-stu-id="2e2e5-109">Depending on the button function, you may need to define the location of the pushed image for the secondary state of the button.</span></span> <span data-ttu-id="2e2e5-110">這會是使用者在第二次推送 PlayPause 函式按鈕時看到的影像。</span><span class="sxs-lookup"><span data-stu-id="2e2e5-110">This will be the image users see when they push a PlayPause function button the second time.</span></span>

<span data-ttu-id="2e2e5-111">若要定義此影像，您必須輸入映射類型，後面接著一個空格和 @ 符號以及另一個空格。</span><span class="sxs-lookup"><span data-stu-id="2e2e5-111">To define this image, you must enter the image type followed by a space and the @ symbol and another space.</span></span> <span data-ttu-id="2e2e5-112">然後，您必須輸入兩個正整數，以定義您想要在繪圖來源的影像類型內使用的影像（以圖元為單位） (（以圖元為單位）) 。</span><span class="sxs-lookup"><span data-stu-id="2e2e5-112">You must then enter two positive integers that define the top-left coordinates (in pixels) of the image you want to use inside the image type you are drawing from.</span></span>

<span data-ttu-id="2e2e5-113">例如，若要定義次要影像來源的已推播映射，如果您的映射在推送的點陣圖內，請輸入：</span><span class="sxs-lookup"><span data-stu-id="2e2e5-113">For example, to define the Pushed image for a secondary image source, if your image is inside the Pushed bitmap, type:</span></span>


```C++
Pushed @ 248,0

```



<span data-ttu-id="2e2e5-114">次要狀態不能有已停用的映射。</span><span class="sxs-lookup"><span data-stu-id="2e2e5-114">Secondary states cannot have a Disabled image.</span></span> <span data-ttu-id="2e2e5-115">次要影像會假設為與主要映射相同的寬度和高度。</span><span class="sxs-lookup"><span data-stu-id="2e2e5-115">Secondary images are assumed to be the same width and height as the primary image.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2e2e5-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="2e2e5-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2e2e5-117">**按鈕**</span><span class="sxs-lookup"><span data-stu-id="2e2e5-117">**Buttons**</span></span>](buttons.md)
</dt> </dl>

 

 





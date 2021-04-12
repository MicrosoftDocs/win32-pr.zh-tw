---
title: 一般的三映射來源
description: 一般的三映射來源
ms.assetid: ce0b009a-b008-4e8b-875b-b2ff3c1c0b81
keywords:
- Windows Media Player 行動外觀、按鈕影像來源
- 外觀，按鈕影像來源
- 外觀、按鈕的參考
- 外觀、影像來源中的按鈕
- 外觀、按鈕的影像來源
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 109509914c498e950f148caf7c260ef814c1074f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372483"
---
# <a name="normal-tertiary-image-source"></a><span data-ttu-id="b0fa8-108">一般的三映射來源</span><span class="sxs-lookup"><span data-stu-id="b0fa8-108">Normal Tertiary Image Source</span></span>

<span data-ttu-id="b0fa8-109">您必須為按鈕的第三個狀態定義一般影像的位置，才能 PlayPauseStop 按鈕函式。</span><span class="sxs-lookup"><span data-stu-id="b0fa8-109">The PlayPauseStop button function requires that you define the location of the normal image for the tertiary state of the button.</span></span> <span data-ttu-id="b0fa8-110">這會是使用者按下 [PlayPauseStop] 按鈕以開始串流處理實況廣播之後看到的影像。</span><span class="sxs-lookup"><span data-stu-id="b0fa8-110">This will be the image users see after they have pushed the PlayPauseStop button to begin streaming a live broadcast.</span></span>

<span data-ttu-id="b0fa8-111">若要定義此影像，您必須輸入映射類型，後面接著一個空格和 @ 符號以及另一個空格。</span><span class="sxs-lookup"><span data-stu-id="b0fa8-111">To define this image, you must enter the image type followed by a space and the @ symbol and another space.</span></span> <span data-ttu-id="b0fa8-112">然後，您必須輸入兩個正整數，以定義您想要在繪圖來源的點陣圖類型內使用之影像的左上座標 (（以圖元為單位）) 。</span><span class="sxs-lookup"><span data-stu-id="b0fa8-112">You must then enter two positive integers that define the top-left coordinates (in pixels) of the image you want to use inside the bitmap type you are drawing from.</span></span>

<span data-ttu-id="b0fa8-113">例如，若要定義第三個影像來源的一般影像，如果您的映射在推送的點陣圖內，請輸入：</span><span class="sxs-lookup"><span data-stu-id="b0fa8-113">For example, to define the normal image for a tertiary image source, if your image is inside the Pushed bitmap, type:</span></span>


```C++
Pushed @ 286,0

```



<span data-ttu-id="b0fa8-114">第三個狀態不能有已停用的映射。</span><span class="sxs-lookup"><span data-stu-id="b0fa8-114">Tertiary states cannot have a Disabled image.</span></span> <span data-ttu-id="b0fa8-115">系統會假設第三個影像的寬度和高度與主要和次要影像相同。</span><span class="sxs-lookup"><span data-stu-id="b0fa8-115">Tertiary images are assumed to be the same width and height as the primary and secondary images.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b0fa8-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="b0fa8-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b0fa8-117">**按鈕**</span><span class="sxs-lookup"><span data-stu-id="b0fa8-117">**Buttons**</span></span>](buttons.md)
</dt> </dl>

 

 





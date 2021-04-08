---
title: 推送的影像來源
description: 推送的影像來源
ms.assetid: 6cc290d8-2c15-4789-970d-9a3663a64d08
keywords:
- Windows Media Player 行動外觀、按鈕影像來源
- 外觀，按鈕影像來源
- 外觀、按鈕的參考
- 外觀、影像來源中的按鈕
- 外觀、按鈕的影像來源
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 021c77a305e0f6981823c8a1e471862554c32e08
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673903"
---
# <a name="pushed-image-source"></a><span data-ttu-id="dc2ff-108">推送的影像來源</span><span class="sxs-lookup"><span data-stu-id="dc2ff-108">Pushed Image Source</span></span>

<span data-ttu-id="dc2ff-109">當使用者推送按鈕時，您必須定義您想要顯示的影像來源。</span><span class="sxs-lookup"><span data-stu-id="dc2ff-109">You must define the source of the image you want to display when the user pushes a button.</span></span> <span data-ttu-id="dc2ff-110">影像來自您在點陣圖區段中所定義的檔案。</span><span class="sxs-lookup"><span data-stu-id="dc2ff-110">The image comes from the file you defined as Pushed in the Bitmaps section.</span></span> <span data-ttu-id="dc2ff-111">您必須輸入映射類型，後面接著一個空格和 @ 符號以及另一個空格。</span><span class="sxs-lookup"><span data-stu-id="dc2ff-111">You must enter the image type followed by a space and the @ symbol and another space.</span></span> <span data-ttu-id="dc2ff-112">然後，您必須輸入兩個正整數，以定義您想要在推送影像檔案中使用之影像的上和左座標 (以圖元為單位的) 。</span><span class="sxs-lookup"><span data-stu-id="dc2ff-112">You must then enter two positive integers that define the top and left coordinates (in pixels) of the image you want to use inside the Pushed image file.</span></span> <span data-ttu-id="dc2ff-113">影像的顯示位置來自于相對於背景影像的按鈕所定義的座標;但其來源位置是由 "推 @" 之後的兩個數字所定義，而且相對於您正在讀取影像的已推送影像。</span><span class="sxs-lookup"><span data-stu-id="dc2ff-113">The location at which the image will be displayed comes from the coordinates defined for the button relative to the Background image; but the location it comes from is defined by the two numbers following "Pushed @" and is relative to the Pushed image you are reading the image from.</span></span>

<span data-ttu-id="dc2ff-114">例如，若要使用推送的影像中的影像，其左上角位置是50，60，您會使用下列程式碼：</span><span class="sxs-lookup"><span data-stu-id="dc2ff-114">For example, to use an image from the Pushed image that is in the Pushed file whose top-left location is 50,60 you would use the following code:</span></span>


```C++
Pushed @ 50,60

```



<span data-ttu-id="dc2ff-115">如果您不想要顯示不同的影像，您可以將背景點陣圖定義為已推送的點陣圖。</span><span class="sxs-lookup"><span data-stu-id="dc2ff-115">If you do not want to display a different image, you can define the Background bitmap as your Pushed bitmap.</span></span> <span data-ttu-id="dc2ff-116">若要這樣做，請將背景檔案指定為您推送的檔案，並指定按鈕左上角的位移：</span><span class="sxs-lookup"><span data-stu-id="dc2ff-116">To do this, specify the Background file as your pushed file and specify the offset to the top-left corner of the button:</span></span>


```C++
Pushed @ 50,60

```



<span data-ttu-id="dc2ff-117">如果您這樣做，則所有按鈕都不會顯示已推送的影像。</span><span class="sxs-lookup"><span data-stu-id="dc2ff-117">If you do this, none of your buttons can display a Pushed image.</span></span> <span data-ttu-id="dc2ff-118">建議您針對所有按鈕顯示已推入的影像，以提供使用者視覺指示，因為它不一定會清楚是否會產生結果，尤其是在播放音樂或關閉點擊音效時。</span><span class="sxs-lookup"><span data-stu-id="dc2ff-118">We recommend that you display a Pushed image for all buttons to give your user a visual indication, because it is not always clear whether a tap produces a result, especially when music is playing or the tapping sound is turned off.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dc2ff-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="dc2ff-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dc2ff-120">**按鈕**</span><span class="sxs-lookup"><span data-stu-id="dc2ff-120">**Buttons**</span></span>](buttons.md)
</dt> </dl>

 

 





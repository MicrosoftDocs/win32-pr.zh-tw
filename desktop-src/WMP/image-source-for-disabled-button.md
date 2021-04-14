---
title: 已停用按鈕的影像來源
description: 已停用按鈕的影像來源
ms.assetid: 6c50e0bd-c174-4335-8d34-ae25feec9ec6
keywords:
- Windows Media Player 行動外觀、按鈕影像來源
- 外觀，按鈕影像來源
- 外觀、按鈕的參考
- 外觀、影像來源中的按鈕
- 外觀、按鈕的影像來源
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d05ccd0362f3dd11acec71eaf0b92574f2c27c77
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372215"
---
# <a name="image-source-for-disabled-button"></a><span data-ttu-id="7c27c-108">已停用按鈕的影像來源</span><span class="sxs-lookup"><span data-stu-id="7c27c-108">Image Source for Disabled Button</span></span>

<span data-ttu-id="7c27c-109">當按鈕已停用或有對應于 off 的狀態時，您必須定義您想要顯示的影像來源。</span><span class="sxs-lookup"><span data-stu-id="7c27c-109">You must define the source of the image you want to display when a button is disabled or has a state that corresponds to off.</span></span> <span data-ttu-id="7c27c-110">影像來自您在 [點陣圖] 區段中定義為已停用的檔案。</span><span class="sxs-lookup"><span data-stu-id="7c27c-110">The image comes from the file you defined as Disabled in the Bitmaps section.</span></span> <span data-ttu-id="7c27c-111">您必須輸入映射類型，後面接著一個空格和 @ 符號以及另一個空格。</span><span class="sxs-lookup"><span data-stu-id="7c27c-111">You must enter the image type followed by a space and the @ symbol and another space.</span></span> <span data-ttu-id="7c27c-112">然後，您必須輸入兩個正整數，以定義您想要在點陣圖檔案內使用之影像的左上座標 (（以圖元為單位）) 。</span><span class="sxs-lookup"><span data-stu-id="7c27c-112">You must then enter two positive integers that define the top-left coordinates (in pixels) of the image you want to use inside the bitmap file.</span></span> <span data-ttu-id="7c27c-113">影像的顯示位置來自針對相對於背景影像的按鈕所定義的座標，但它的位置是由 "Disabled @" 之後的兩個數字所定義，相對於您正在讀取影像的已停用點陣圖。</span><span class="sxs-lookup"><span data-stu-id="7c27c-113">The location at which the image will be displayed comes from the coordinates defined for the button relative to the Background image, but the location it comes from is defined by the two numbers following "Disabled @" and is relative to the Disabled bitmap you are reading the image from.</span></span>

<span data-ttu-id="7c27c-114">例如，若要使用已停用之點陣圖中的影像，而該點陣圖位於位於50、60圖元的左上角，則使用下列程式碼：</span><span class="sxs-lookup"><span data-stu-id="7c27c-114">For example, to use an image from the Disabled bitmap that is in the Disabled file at a top and left location of 50,60 pixels, use the following code:</span></span>


```C++
Disabled @ 50,60

```



<span data-ttu-id="7c27c-115">您必須定義停用的點陣圖。</span><span class="sxs-lookup"><span data-stu-id="7c27c-115">You must define a Disabled bitmap.</span></span> <span data-ttu-id="7c27c-116">如果您不想要顯示不同的影像，您可以將背景點陣圖定義為已停用的點陣圖，位移為0，0：</span><span class="sxs-lookup"><span data-stu-id="7c27c-116">If you do not want to display a different image, you can define the Background bitmap as your Disabled bitmap with an offset of 0,0:</span></span>


```C++
Disabled @ 50,60

```



<span data-ttu-id="7c27c-117">在上述範例中，50，60是您在已停用的檔案中使用之按鈕的位置 (在此案例中，與背景點陣圖上的按鈕相同的位置) 。</span><span class="sxs-lookup"><span data-stu-id="7c27c-117">In the preceding example, 50,60 is the location of the button you are working with in the Disabled file (in this case, the same location as the button on the Background bitmap).</span></span> <span data-ttu-id="7c27c-118">不過，強烈建議您針對所有按鈕顯示已停用的影像，以提供使用者視覺指示，因為在某些情況下，有許多按鈕將無法使用，例如空白播放清單。</span><span class="sxs-lookup"><span data-stu-id="7c27c-118">However, it is highly recommended that you display a Disabled image for all buttons to give your users a visual indication, because many buttons will not be useable under certain conditions, such as an empty playlist.</span></span> <span data-ttu-id="7c27c-119">如果使用者知道按鈕已停用，就不會繼續嘗試按一下它，或認為您的面板未依照設計的方式運作。</span><span class="sxs-lookup"><span data-stu-id="7c27c-119">If users know a button is disabled, they will not keep trying to click on it or think your skin is not functioning as designed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7c27c-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="7c27c-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7c27c-121">**按鈕**</span><span class="sxs-lookup"><span data-stu-id="7c27c-121">**Buttons**</span></span>](buttons.md)
</dt> </dl>

 

 





---
title: 已停用之跟蹤的影像來源
description: 已停用之跟蹤的影像來源
ms.assetid: ecbe1670-2914-4b66-92bd-d854e6c1e897
keywords:
- Windows Media Player 行動外觀 trackbars
- 外觀，trackbars
- 外觀的參考，trackbars
- 外觀中的 trackbars、影像來源
- 外觀的影像來源，trackbars
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbae540f97c7d1f7241035b074f45e6267e51615
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106967201"
---
# <a name="image-source-for-disabled-trackbar"></a><span data-ttu-id="b4105-108">已停用之跟蹤的影像來源</span><span class="sxs-lookup"><span data-stu-id="b4105-108">Image Source for Disabled Trackbar</span></span>

<span data-ttu-id="b4105-109">您必須使用您想要用來繪製影像的點陣圖類型，來定義要在停用程式時顯示的影像來源。</span><span class="sxs-lookup"><span data-stu-id="b4105-109">You must define the source of the image you want to display when a trackbar is disabled, using the bitmap type you want to draw the image from.</span></span> <span data-ttu-id="b4105-110">您所顯示的影像通常會在超級檔案內，或者，如果您要建立 Windows Media Player 10 行動裝置版的面板，則影像會在 SeekThumb 檔案內。</span><span class="sxs-lookup"><span data-stu-id="b4105-110">The image you display will usually be inside the Super file or if you are creating a skin for Windows Media Player 10 Mobile, the image would be inside the SeekThumb file.</span></span> <span data-ttu-id="b4105-111">您必須輸入映射類型，後面接著一個空格和 @ 符號以及另一個空格。</span><span class="sxs-lookup"><span data-stu-id="b4105-111">You must enter the image type followed by a space and the @ symbol and another space.</span></span> <span data-ttu-id="b4105-112">然後，您必須輸入兩個正整數，以定義您想要在繪圖來源的點陣圖類型內使用之影像的左上座標 (（以圖元為單位）) 。</span><span class="sxs-lookup"><span data-stu-id="b4105-112">You must then enter two positive integers that define the top-left coordinates (in pixels) of the image you want to use inside the bitmap type you are drawing from.</span></span>

<span data-ttu-id="b4105-113">例如，若要使用 SeekThumb 點陣圖中的影像，其左上角的位置為50、60圖元，請輸入：</span><span class="sxs-lookup"><span data-stu-id="b4105-113">For example, to use an image from the SeekThumb bitmap that has a top and left position of 50,60 pixels, type:</span></span>


```C++
Disabled @ 50,60

```



<span data-ttu-id="b4105-114">您必須為已停用的 [查看] 影像定義影像位置。</span><span class="sxs-lookup"><span data-stu-id="b4105-114">You must define an image location for a disabled trackbar image.</span></span> <span data-ttu-id="b4105-115">如果您不想要顯示新的影像，您可以將背景影像定義為已停用的影像，其位移為0、0：</span><span class="sxs-lookup"><span data-stu-id="b4105-115">If you do not want to display a new image, you can define the Background image as your Disabled image with an offset of 0,0:</span></span>


```C++
Disabled @ 50,60

```



<span data-ttu-id="b4105-116">在上述範例中，50，60代表您在 SeekThumb 檔中使用的按鈕位置 (在此案例中，與背景點陣圖上的按鈕相同的位置) 。</span><span class="sxs-lookup"><span data-stu-id="b4105-116">In the preceding example, 50,60 represents the location of the button you are working with in the SeekThumb file (in this case, the same location as the button on the Background bitmap).</span></span> <span data-ttu-id="b4105-117">不過，強烈建議您針對所有 trackbars 顯示已停用的影像，以提供使用者視覺指示，因為在某些情況下，trackbars 將無法使用。</span><span class="sxs-lookup"><span data-stu-id="b4105-117">However, it is highly recommended that you display a Disabled image for all trackbars to give your user a visual indication, because trackbars will not be useable under certain conditions.</span></span> <span data-ttu-id="b4105-118">例如，當目前的播放清單空白時，[搜尋 trackbars] 可能會停用。</span><span class="sxs-lookup"><span data-stu-id="b4105-118">For example, Seek trackbars may be disabled when the current playlist is empty.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b4105-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="b4105-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b4105-120">**Trackbars**</span><span class="sxs-lookup"><span data-stu-id="b4105-120">**Trackbars**</span></span>](trackbars.md)
</dt> </dl>

 

 





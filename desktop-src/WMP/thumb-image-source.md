---
title: Thumb 影像來源
description: Thumb 影像來源
ms.assetid: dca1f54d-ee79-4fd4-9c4e-8226f65c9515
keywords:
- Windows Media Player 行動外觀 trackbars
- 外觀，trackbars
- 外觀的參考，trackbars
- 外觀中的 trackbars、影像來源
- 面板中的 trackbars、thumb 影像來源
- 外觀的影像來源，trackbars
- thumb、影像來源
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ac19053b58c7d12543d38c639abe5a43c01ff64
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021110"
---
# <a name="thumb-image-source"></a><span data-ttu-id="044cb-110">Thumb 影像來源</span><span class="sxs-lookup"><span data-stu-id="044cb-110">Thumb Image Source</span></span>

<span data-ttu-id="044cb-111">您必須定義包含 thumb 影像的檔案名。</span><span class="sxs-lookup"><span data-stu-id="044cb-111">You must define the name of the file that contains the thumb image.</span></span> <span data-ttu-id="044cb-112">這個名稱必須是副檔名為 .bmp、.gif、.jpg 或 .png 的有效檔案名。</span><span class="sxs-lookup"><span data-stu-id="044cb-112">This must be a valid file name with the extension .bmp, .gif, .jpg, or .png.</span></span> <span data-ttu-id="044cb-113">檔案必須包含三個相同大小的並存影像。</span><span class="sxs-lookup"><span data-stu-id="044cb-113">The file must contain three side-by-side images of identical size.</span></span> <span data-ttu-id="044cb-114">它們必須彼此相鄰，不含空格。</span><span class="sxs-lookup"><span data-stu-id="044cb-114">They must be adjacent to each other with no space between.</span></span> <span data-ttu-id="044cb-115">左邊影像的左上角必須位在檔案的左上角。</span><span class="sxs-lookup"><span data-stu-id="044cb-115">The top-left position of the left image must be at the top-left corner of the file.</span></span> <span data-ttu-id="044cb-116">左邊的影像是捲動方塊影像的一般影像，而中間的影像會描繪出推入的狀態，右側的影像則會描繪出已停用的狀態。</span><span class="sxs-lookup"><span data-stu-id="044cb-116">The image on the left side is the normal image for the thumb image, and the image in the middle depicts the pushed state and the image on the right depicts the disabled state.</span></span>


```C++
SeekThumb.bmp

```



<span data-ttu-id="044cb-117">您可能會想要讓 thumb 影像的特定區域變成透明的。</span><span class="sxs-lookup"><span data-stu-id="044cb-117">You may want to make certain areas of the thumb image transparent.</span></span> <span data-ttu-id="044cb-118">這可讓您在矩形以外的圖形中建立 thumb 影像。</span><span class="sxs-lookup"><span data-stu-id="044cb-118">This will allow you to create thumb images in shapes other than rectangular.</span></span> <span data-ttu-id="044cb-119">您以 RGB 值255、0、255所指定色彩填滿的 thumb 影像的任何區域，在您的面板中將會顯示為透明。</span><span class="sxs-lookup"><span data-stu-id="044cb-119">Any region of the thumb image that you fill with the color specified by the RGB value 255, 0, 255 will appear transparent in your skin.</span></span>

## <a name="related-topics"></a><span data-ttu-id="044cb-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="044cb-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="044cb-121">**Trackbars**</span><span class="sxs-lookup"><span data-stu-id="044cb-121">**Trackbars**</span></span>](trackbars.md)
</dt> </dl>

 

 





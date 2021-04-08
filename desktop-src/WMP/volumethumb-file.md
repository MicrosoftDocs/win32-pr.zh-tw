---
title: VolumeThumb 檔案
description: VolumeThumb 檔案
ms.assetid: de6abfed-a811-44c4-8db2-f3b55ea38756
keywords:
- Windows Media Player 行動外觀、美工檔案
- 外觀、美工檔案
- 適用于外觀、藝術的檔案
- 適用于外觀、VolumeThumb 檔案的美工檔案
- Windows Media Player 行動外觀 VolumeThumb 檔案
- 外觀，VolumeThumb 檔
- 面板中的 VolumeThumb 檔案
- thumb、VolumeThumb 檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9b7ba87723025c91b3bdfb5af5fd233197dedb8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672572"
---
# <a name="volumethumb-file"></a><span data-ttu-id="28efc-111">VolumeThumb 檔案</span><span class="sxs-lookup"><span data-stu-id="28efc-111">VolumeThumb File</span></span>

<span data-ttu-id="28efc-112">VolumeThumb 檔案會定義映射，以指出磁片區播放程式的播放音量層級。</span><span class="sxs-lookup"><span data-stu-id="28efc-112">The VolumeThumb file defines the image that indicates the playback volume level for a Volume trackbar.</span></span> <span data-ttu-id="28efc-113">您可以使用一個檔案並定義它，以供 SeekThumb 和 VolumeThumb 使用。</span><span class="sxs-lookup"><span data-stu-id="28efc-113">You can use one file and define it for use by both SeekThumb and VolumeThumb.</span></span> <span data-ttu-id="28efc-114">與其他美工檔案不同的是，thumb 檔案是在外觀定義檔的 Trackbars 區段中定義。</span><span class="sxs-lookup"><span data-stu-id="28efc-114">Unlike the other art files, the thumb files are defined in the Trackbars section of the skin definition file.</span></span>

<span data-ttu-id="28efc-115">下圖是一般的 VolumeThumb 檔案。</span><span class="sxs-lookup"><span data-stu-id="28efc-115">The following image is a typical VolumeThumb file.</span></span>

![volumethumb 檔案](images/cesdkvol.png)

<span data-ttu-id="28efc-117">這兩個按鈕檔看起來相同，但大小稍有不同。</span><span class="sxs-lookup"><span data-stu-id="28efc-117">These two button files look the same but are slightly different sizes.</span></span> <span data-ttu-id="28efc-118">左邊的影像是使用者看到的一般觀點，而右邊的影像則是使用者在按下按鈕時所看到的推播影像。</span><span class="sxs-lookup"><span data-stu-id="28efc-118">The left image is the normal view that the user sees, and the right image is the Pushed image the user sees when they tap on the button.</span></span>

<span data-ttu-id="28efc-119">您可能會想要讓 thumb 影像的特定區域變成透明的。</span><span class="sxs-lookup"><span data-stu-id="28efc-119">You may want to make certain areas of the thumb images transparent.</span></span> <span data-ttu-id="28efc-120">這可讓您在矩形以外的圖形中建立 thumb 影像。</span><span class="sxs-lookup"><span data-stu-id="28efc-120">This will allow you to create thumb images in shapes other than rectangular.</span></span> <span data-ttu-id="28efc-121">您以 RGB 值255、0、255所指定的色彩填滿的任何 thumb 影像區域，在您的面板中將會顯示為透明。</span><span class="sxs-lookup"><span data-stu-id="28efc-121">Any region of a thumb image that you fill with the color specified by the RGB value 255, 0, 255 will appear transparent in your skin.</span></span>

## <a name="related-topics"></a><span data-ttu-id="28efc-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="28efc-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28efc-123">**美工檔案**</span><span class="sxs-lookup"><span data-stu-id="28efc-123">**Art Files**</span></span>](art-files-mobile.md)
</dt> </dl>

 

 





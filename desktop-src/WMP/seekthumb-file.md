---
title: SeekThumb 檔案
description: SeekThumb 檔案
ms.assetid: 757aeb93-ebf0-4659-8cb0-686e54485ac4
keywords:
- Windows Media Player 行動外觀、美工檔案
- 外觀、美工檔案
- 適用于外觀、藝術的檔案
- 適用于外觀、SeekThumbd 檔案的美工檔案
- Windows Media Player 行動外觀 SeekThumb 檔案
- 外觀，SeekThumb 檔
- 面板中的 SeekThumb 檔案
- thumb、SeekThumb 檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc9f1e9434a614dbc02e48b63508c7c2c04f553d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932348"
---
# <a name="seekthumb-file"></a><span data-ttu-id="5da7f-111">SeekThumb 檔案</span><span class="sxs-lookup"><span data-stu-id="5da7f-111">SeekThumb File</span></span>

<span data-ttu-id="5da7f-112">SeekThumb 檔案會定義影像，指出搜尋的播放程式在媒體專案內的播放位置。</span><span class="sxs-lookup"><span data-stu-id="5da7f-112">The SeekThumb file defines the image that indicates the playback location within the media item for a Seek trackbar.</span></span> <span data-ttu-id="5da7f-113">您可以使用一個檔案並定義它，以供 SeekThumb 和 VolumeThumb 使用。</span><span class="sxs-lookup"><span data-stu-id="5da7f-113">You can use one file and define it for use by both SeekThumb and VolumeThumb.</span></span> <span data-ttu-id="5da7f-114">與其他美工檔案不同的是，thumb 檔案是在外觀定義檔的 Trackbars 區段中定義。</span><span class="sxs-lookup"><span data-stu-id="5da7f-114">Unlike the other art files, the thumb files are defined in the Trackbars section of the skin definition file.</span></span>

<span data-ttu-id="5da7f-115">下圖是一般的 SeekThumb 檔案。</span><span class="sxs-lookup"><span data-stu-id="5da7f-115">The following image is a typical SeekThumb file.</span></span>

![seekthumb 檔案](images/cesdksee.gif)

<span data-ttu-id="5da7f-117">這兩個按鈕檔看起來相同，但大小稍有不同。</span><span class="sxs-lookup"><span data-stu-id="5da7f-117">These two button files look the same but are slightly different sizes.</span></span> <span data-ttu-id="5da7f-118">左邊的影像是使用者看到的一般觀點，而右邊的影像則是使用者在按下按鈕時所看到的推播影像。</span><span class="sxs-lookup"><span data-stu-id="5da7f-118">The left image is the normal view that the user sees, and the right image is the Pushed image the user sees when they tap on the button.</span></span>

> [!Note]  
> <span data-ttu-id="5da7f-119">針對 Windows Media Player 10 行動裝置版或更新版本中所使用的面板所建立的 SeekThumb 檔案，必須有下列三個映射 (從左至右) ： normal、推送和停用。</span><span class="sxs-lookup"><span data-stu-id="5da7f-119">SeekThumb art files created for skins used in Windows Media Player 10 Mobile or later must have the following three images (from left to right): normal, pushed, and disabled.</span></span>

 

<span data-ttu-id="5da7f-120">您可能會想要讓 thumb 影像的特定區域變成透明的。</span><span class="sxs-lookup"><span data-stu-id="5da7f-120">You may want to make certain areas of the thumb images transparent.</span></span> <span data-ttu-id="5da7f-121">這可讓您在矩形以外的圖形中建立 thumb 影像。</span><span class="sxs-lookup"><span data-stu-id="5da7f-121">This will allow you to create thumb images in shapes other than rectangular.</span></span> <span data-ttu-id="5da7f-122">您以 RGB 值255、0、255所指定的色彩填滿的任何 thumb 影像區域，在您的面板中將會顯示為透明。</span><span class="sxs-lookup"><span data-stu-id="5da7f-122">Any region of a thumb image that you fill with the color specified by the RGB value 255, 0, 255 will appear transparent in your skin.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5da7f-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="5da7f-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5da7f-124">**美工檔案**</span><span class="sxs-lookup"><span data-stu-id="5da7f-124">**Art Files**</span></span>](art-files-mobile.md)
</dt> </dl>

 

 





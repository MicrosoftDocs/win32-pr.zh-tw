---
title: 建立區域檔案
description: 建立區域檔案
ms.assetid: e901dfa1-1e06-4136-b877-64be03107f6f
keywords:
- Windows Media Player 行動外觀、區域檔案
- 外觀，區域檔案
- 建立外觀、區域檔案
- 外觀中的區域檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bf3268b101255191bef4b3e4c4880e2bb846414
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300235"
---
# <a name="creating-the-region-file"></a><span data-ttu-id="4b262-107">建立區域檔案</span><span class="sxs-lookup"><span data-stu-id="4b262-107">Creating the Region File</span></span>

<span data-ttu-id="4b262-108">您會想要建立一個區域檔案，以顯示哪些區域會回應點擊。</span><span class="sxs-lookup"><span data-stu-id="4b262-108">You will want to create a Region file that shows what areas respond to taps.</span></span> <span data-ttu-id="4b262-109">您可以直接將每個元素的基底圖層複製到新圖層，並將其色彩對應到您將在面板定義檔中使用的色彩數位。</span><span class="sxs-lookup"><span data-stu-id="4b262-109">You can simply copy the base layers of each element to a new layer, and color them to correspond to the color numbers you will use in the skin definition file.</span></span> <span data-ttu-id="4b262-110">確定您在此圖層中建立的影像是穩固的，且不會套用任何效果。</span><span class="sxs-lookup"><span data-stu-id="4b262-110">Be sure that the images you create in this layer are solid and that no effects are applied.</span></span> <span data-ttu-id="4b262-111">您可能會想要寫下每個影像的色彩數位。</span><span class="sxs-lookup"><span data-stu-id="4b262-111">You will probably want to write down the color numbers for each image.</span></span> <span data-ttu-id="4b262-112">您可以從 Photoshop 色彩選擇器取得色彩數位。</span><span class="sxs-lookup"><span data-stu-id="4b262-112">You can get the color numbers from the Photoshop Color Picker.</span></span> <span data-ttu-id="4b262-113">您想要 RGB 數位，也就是三個小數位數。</span><span class="sxs-lookup"><span data-stu-id="4b262-113">You want the RGB numbers, which are three decimal numbers.</span></span> <span data-ttu-id="4b262-114">每個數位的範圍是從0到255。</span><span class="sxs-lookup"><span data-stu-id="4b262-114">Each number ranges from 0 to 255.</span></span> <span data-ttu-id="4b262-115">例如，純紅色會是255、0、0。</span><span class="sxs-lookup"><span data-stu-id="4b262-115">For example, a solid red would be 255, 0, 0.</span></span>

> [!Note]  
> <span data-ttu-id="4b262-116">因為 Windows Media Player 10 行動裝置版或更新版本不支援按鈕類型，所以不會在 Windows Media Player 10 行動面板中使用區域檔案。</span><span class="sxs-lookup"><span data-stu-id="4b262-116">Region files are not used in Windows Media Player 10 Mobile skins because button types are not supported in Windows Media Player 10 Mobile or later.</span></span>

 

<span data-ttu-id="4b262-117">下圖是區域檔案。</span><span class="sxs-lookup"><span data-stu-id="4b262-117">The following image is the Region file.</span></span>

![區域檔案](images/ceswmreg.png)

<span data-ttu-id="4b262-119">此檔案中只有四個影像，因為只有 [PlayPause]、[停止]、[下一步] 和 [上一個] 按鈕是按類型按鈕。</span><span class="sxs-lookup"><span data-stu-id="4b262-119">There are only four images in this file because only the PlayPause, Stop, Next, and Prev buttons are hit-type buttons.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4b262-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="4b262-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b262-121">**建立藝術**</span><span class="sxs-lookup"><span data-stu-id="4b262-121">**Creating the Art**</span></span>](creating-the-art.md)
</dt> </dl>

 

 





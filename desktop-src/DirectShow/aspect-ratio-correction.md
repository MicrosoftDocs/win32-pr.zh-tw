---
description: 外觀比例修正
ms.assetid: 0ed6010b-9168-44b1-be49-0c9d5d77ce3f
title: 外觀比例修正
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2460f7ecce1513394d941eafe8bdf8a7a80e9727
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106970086"
---
# <a name="aspect-ratio-correction"></a><span data-ttu-id="0cdbb-103">外觀比例修正</span><span class="sxs-lookup"><span data-stu-id="0cdbb-103">Aspect Ratio Correction</span></span>

<span data-ttu-id="0cdbb-104">本主題適用于 Windows XP Service Pack 2 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="0cdbb-104">This topic applies to Windows XP Service Pack 2 or later.</span></span>

<span data-ttu-id="0cdbb-105">在混合模式中，VMR 會將影片的大小調整為正確的外觀比例。</span><span class="sxs-lookup"><span data-stu-id="0cdbb-105">In mixing mode, the VMR sizes the video to the correct aspect ratio.</span></span> <span data-ttu-id="0cdbb-106"> (例外狀況：請參閱 [非平方混合](non-square-mixing.md)。 ) 如果慣用的外觀比例與影像的實體外觀比例不同，則可能需要延展影片。</span><span class="sxs-lookup"><span data-stu-id="0cdbb-106">(Exception: See [Non-Square Mixing](non-square-mixing.md).) This may require stretching the video if the preferred aspect ratio is not the same as the image's physical aspect ratio.</span></span> <span data-ttu-id="0cdbb-107">例如，數位視訊 (DV) 格式為 720 x 480 圖元 (3:2) 但應以4:3 的外觀比例顯示。</span><span class="sxs-lookup"><span data-stu-id="0cdbb-107">For example, digital video (DV) format is 720 x 480 pixels (3:2) but should be displayed at a 4:3 aspect ratio.</span></span>

<span data-ttu-id="0cdbb-108">VMR 支援兩種不同的外觀比例修正行為：</span><span class="sxs-lookup"><span data-stu-id="0cdbb-108">The VMR supports two different behaviors for aspect ratio correction:</span></span>

-   <span data-ttu-id="0cdbb-109">調整水準或垂直大小，使影像永遠伸展，永遠不壓縮。</span><span class="sxs-lookup"><span data-stu-id="0cdbb-109">Adjust either the horizontal or vertical size, so that the image is always stretched, never shrunk.</span></span> <span data-ttu-id="0cdbb-110">這現在是預設行為。</span><span class="sxs-lookup"><span data-stu-id="0cdbb-110">This is now the default behavior.</span></span>
-   <span data-ttu-id="0cdbb-111">調整水準大小，也就是縮放或壓縮影片。</span><span class="sxs-lookup"><span data-stu-id="0cdbb-111">Adjust the horizontal size, either stretching or shrinking the video.</span></span>

<span data-ttu-id="0cdbb-112">由於第二個行為 (水準調整，因此) 可能需要壓縮影片，輸出影像的解析度可能較少。</span><span class="sxs-lookup"><span data-stu-id="0cdbb-112">Because the second behavior (horizontal adjustment only) may entail shrinking the video, the output image may have less resolution.</span></span> <span data-ttu-id="0cdbb-113">基於這個原因，第一個行為是慣用的。</span><span class="sxs-lookup"><span data-stu-id="0cdbb-113">For this reason, the first behavior is preferred.</span></span> <span data-ttu-id="0cdbb-114">例如，在 720 x 480 video （4:3 外觀比例）的情況下，預設行為會產生 720 x 550 影像，而水準調整會產生較小的 640 x 480 影像。</span><span class="sxs-lookup"><span data-stu-id="0cdbb-114">For example, in the case of 720 x 480 video at 4:3 aspect ratio, the default behavior produces a 720 x 550 image, while horizontal adjustment produces a smaller 640 x 480 image.</span></span>

<span data-ttu-id="0cdbb-115">**VMR-7**：若要設定外觀比例修正喜好設定，請呼叫 [**IVMRMixerControl：： SetMixingPrefs**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setoutputrect)。</span><span class="sxs-lookup"><span data-stu-id="0cdbb-115">**VMR-7**: To set the aspect ratio correction preference, call [**IVMRMixerControl::SetMixingPrefs**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setoutputrect).</span></span> <span data-ttu-id="0cdbb-116">\_針對預設行為設定 MixerPref ARAdjustXorY 旗標，或清除此旗標僅限水準調整。</span><span class="sxs-lookup"><span data-stu-id="0cdbb-116">Set the MixerPref\_ARAdjustXorY flag for the default behavior, or clear this flag for horizontal adjustment only.</span></span>

<span data-ttu-id="0cdbb-117">**VMR-9**：若要設定外觀比例修正喜好設定，請呼叫 [**IVMRMixerControl9：： SetMixingPrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs)。</span><span class="sxs-lookup"><span data-stu-id="0cdbb-117">**VMR-9**: To set the aspect ratio correction preference, call [**IVMRMixerControl9::SetMixingPrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs).</span></span> <span data-ttu-id="0cdbb-118">\_針對預設行為設定 MixerPref9 ARAdjustXorY 旗標，或清除此旗標僅限水準調整。</span><span class="sxs-lookup"><span data-stu-id="0cdbb-118">Set the MixerPref9\_ARAdjustXorY flag for the default behavior, or clear this flag for horizontal adjustment only.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0cdbb-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="0cdbb-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0cdbb-120">使用 VMR 混合模式</span><span class="sxs-lookup"><span data-stu-id="0cdbb-120">Using VMR Mixing Mode</span></span>](using-vmr-mixing-mode.md)
</dt> </dl>

 

 




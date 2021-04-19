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
# <a name="aspect-ratio-correction"></a>外觀比例修正

本主題適用于 Windows XP Service Pack 2 或更新版本。

在混合模式中，VMR 會將影片的大小調整為正確的外觀比例。  (例外狀況：請參閱 [非平方混合](non-square-mixing.md)。 ) 如果慣用的外觀比例與影像的實體外觀比例不同，則可能需要延展影片。 例如，數位視訊 (DV) 格式為 720 x 480 圖元 (3:2) 但應以4:3 的外觀比例顯示。

VMR 支援兩種不同的外觀比例修正行為：

-   調整水準或垂直大小，使影像永遠伸展，永遠不壓縮。 這現在是預設行為。
-   調整水準大小，也就是縮放或壓縮影片。

由於第二個行為 (水準調整，因此) 可能需要壓縮影片，輸出影像的解析度可能較少。 基於這個原因，第一個行為是慣用的。 例如，在 720 x 480 video （4:3 外觀比例）的情況下，預設行為會產生 720 x 550 影像，而水準調整會產生較小的 640 x 480 影像。

**VMR-7**：若要設定外觀比例修正喜好設定，請呼叫 [**IVMRMixerControl：： SetMixingPrefs**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setoutputrect)。 \_針對預設行為設定 MixerPref ARAdjustXorY 旗標，或清除此旗標僅限水準調整。

**VMR-9**：若要設定外觀比例修正喜好設定，請呼叫 [**IVMRMixerControl9：： SetMixingPrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs)。 \_針對預設行為設定 MixerPref9 ARAdjustXorY 旗標，或清除此旗標僅限水準調整。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 VMR 混合模式](using-vmr-mixing-mode.md)
</dt> </dl>

 

 




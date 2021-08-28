---
title: 在組合空間中定位和移動影片矩形
description: 在組合空間中定位和移動影片矩形
ms.assetid: 97e7bb24-79f6-4638-a9c4-ac09dbd29be9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 563509e062335f496f001d8d61dae8eecfe2cff998da6e63320a7c95c347438c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119583601"
---
# <a name="position-and-move-video-rectangles-in-composition-space"></a>在組合空間中定位和移動影片矩形

當 VMR 混合多個輸入資料流程時，會將每個串流放置於一個正規化的矩形內，稱為「組合空間」。 在組合空間內，座標 (0.0，0.0) 至 (1.0，1.0) 形成可見的影片矩形。 落在這個矩形之外的任何座標都會裁剪。

應用程式可以藉由變更資料流程的組合空間中的目的地矩形，來執行從輸入串流移動、延展和壓縮影片的特殊效果。 如果指定的矩形與原生影片矩形的大小不同，則原生影片將會縮小或伸展以容納。 藉由呼叫 [**IVMRMixerControl：： SetOutputRect**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setmixingprefs) 方法來指定目的地矩形。

例如，假設「資料流程0」 (對應至「pin 0」) 包含主要的影片資料流程，而「串流1」 (對應至 pin 1) 包含次要影片。 您可以藉由指定 {-1.0 f、0.0 f、0.0 f、1.0 f} 的正規化矩形，將 Stream 1 完全放置於外。 然後，您可以在連續呼叫 **SetOutputRect** 時，藉由修改矩形的左右側邊，將 Stream 1 移至可見區域：



| 標籤 | 值 |
|--------|-----------------------------|
| 時間   | 矩形                   |
| t + 0  | {-1.0 f、0.0 f、0.0 f、1.0 f} |
| t + 1  | {-0.9 f、0.0 f、0.1 f、1.0 f} |
| t + 2  | {-0.8 f、0.0 f、0.2 f、1.0 f} |
| ...    | ...                         |
| t + 10 | {0.0 f、0.0 f、1.0 f、1.0 f}  |



 

![在組合空間中移動影片資料流程](images/composition-space.png)

在時間 t + 10，資料流程1的影片完全可見。 在此範例中，資料流程1的原生大小是在移動時進行維護。 您也可以延展或縮小矩形，以產生有趣的效果。 您也可以垂直翻轉影片、指定頂端的較大值，或是水準鏡像影片，方法是指定右邊左邊的較大值。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 VMR 混合模式](using-vmr-mixing-mode.md)
</dt> </dl>

 

 




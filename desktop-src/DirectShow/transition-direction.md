---
description: 轉換方向
ms.assetid: d18525de-bb75-4c5e-b387-cfec7ba03df7
title: 轉換方向
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01d43ec4258d2f23c8b8961e3e1b8fd3d554b057
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104562436"
---
# <a name="transition-direction"></a>轉換方向

\[此 API 不受支援，而且可能會在未來變更或無法使用。\]

轉換會從輸入 A 移至輸入 B，並從時間 t ₀至 t ₁。 因此，轉換的 *方向* 可能表示下列其中一種情況：

-   時間軸圖層與輸入的對應。
-   經過一段時間的進展。

第一個是 *輸入方向*，而第二個則是 *進度方向*。 您可以控制兩個方向。

-   輸入方向：根據預設，轉換會從較低優先順序層級的複合層移至包含轉換的圖層。 若要反轉此方向，請呼叫 [**IAMTimelineTrans：： SetSwapInputs**](iamtimelinetrans-setswapinputs.md) 方法。
-   進度方向：大部分的轉換都支援標準 **進度** 屬性，以指定在指定的時間內，輸出中會反映的轉換百分比。 根據預設，在轉換期間， **進度** 屬性的值會從0.0 到1.0。 若要反轉進度，請將 **進度** 屬性設定為從1.0 移至0.0。

下圖說明輸入方向和進度方向之間的差異。 它會顯示標準 [SMPTE](smpte-wipe-transition.md) 抹除轉換的四個變化。

![抹除方向](images/wipedirections.png)

轉換位於曲目1上。 依預設，抹除會從左至右，以及從「曲目0」到「追蹤1」。 交換輸入會導致抹除從曲目1移至追蹤0，但仍由左至右。 反轉進度可讓轉換從右至左。 您可以結合這兩個，如最左邊的顯示。

如需 DES 如何轉譯轉換的詳細資訊，請參閱 [時間軸模型](the-timeline-model.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用效果和轉換](working-with-effects-and-transitions.md)
</dt> </dl>

 

 




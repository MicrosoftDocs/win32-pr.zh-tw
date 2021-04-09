---
description: C + + 應用程式可以藉由變更 Microsoft Direct3D 如何計算與距離之間的霧化效果，來控制霧化如何影響場景中的物件色彩。
ms.assetid: b7148ae8-45c7-4dbe-8295-0335c7fdeff0
title: " (Direct3D 9) 的霧化公式"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75150a00d491f1e3fc1ea1444209449c1c2a825d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846175"
---
# <a name="fog-formulas-direct3d-9"></a> (Direct3D 9) 的霧化公式

C + + 應用程式可以藉由變更 Microsoft Direct3D 如何計算與距離之間的霧化效果，來控制霧化如何影響場景中的物件色彩。 [**D3DFOGMODE**](./d3dfogmode.md)列舉型別包含可識別三個霧化公式的成員。 所有公式都會將一個霧化因數計算為距離的函式，並指定您的應用程式所設定的參數。

## <a name="linear-fog"></a>線性霧化

這會以下列 D3DFOG 線性方程序來設定 \_ 。

![direct3d 線性模糊的方程式](images/fogliner.png)

其中

-   start 是霧化效果開始的距離。
-   end 是不會再增加霧化效果的距離。
-   d 表示深度，或從觀點來看距離。 針對以範圍為基礎的霧化，d 的值是相機位置與頂點之間的距離。 針對非範圍的霧化，d 的值是相機空間中 Z 座標的絕對值。

## <a name="exponential-fog"></a>指數霧化

線性和指數公式都支援圖元霧化和頂點霧化。

這會使用下列 D3DFOG EXP 方程式來設定 \_ 。

![direct3d 指數霧化的方程式](images/fogexp.png)

其中

-   e 是自然對數的基底， (大約 2.71828) 。
-   密度是任意的霧化密度，範圍從0.0 到1.0。
-   d 表示深度，或與視點之間的距離（如先前所述）。

這會使用下列 D3DFOG EXP2 方程式來設定 \_ 。

![direct3d 指數2霧化的方程式](images/fogexp2.png)

其中

-   e 是自然對數的基底，如上所述。
-   密度是任意的霧化密度，其範圍從0.0 到1.0，如上所述。
-   d 表示深度，或與觀點的距離，如上所述。

> [!Note]  
> 系統會在頂點的反射色彩 Alpha 元件中儲存霧化因數。 如果您的應用程式執行自己的轉換和光源，您可以手動插入霧化因數值，以在轉譯期間由系統套用。

 

下圖顯示這些公式，並使用公式參數中的一般值。

![在距離和色彩量之間的霧化公式圖表](images/foggraph.png)

D3DFOG \_ 線性在開始和0.0 結束時為1.0。 它不會相對於接近或遠的平面來測量。

當 Direct3D 計算霧化效果時，它會使用下列混合方程式中上述其中一個方程式的霧化係數。

![direct3d 的霧化效果方程式](images/fogcalc.png)

此公式會有效地以霧因數 f 來調整目前多邊形 C 的色彩，並將產品加入至霧色 C，並以霧化因數的位反向進行縮放。 產生的色彩值是霧化色彩和原始色彩的 blend，作為距離的係數。 此公式適用于 Microsoft DirectX 7.0 和更新版本中支援的所有裝置。 針對舊版的遞增裝置，霧化因數會調整擴散和反射色彩元件，壓制至0.0 和1.0 （含）的範圍。 下平面的霧化因數通常會從1.0 開始，並在最遠的平面減少為0.0。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[霧化類型](fog-types.md)
</dt> </dl>

 

 

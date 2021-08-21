---
description: 在 Windows GDI+ 中，色彩是32位值，每個都有8個位，分別適用于 Alpha、紅色、綠色和藍色。
ms.assetid: f8c22d1a-b96b-4d16-928e-20adbae4c4a7
title: Alpha 混色線條和填色
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64096bbabc632ad7c2b159191ad21b3b09f3801a486f27679118008e4927e88f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118977798"
---
# <a name="alpha-blending-lines-and-fills"></a>Alpha 混色線條和填色

在 Windows GDI+ 中，色彩是32位值，每個都有8個位，分別適用于 Alpha、紅色、綠色和藍色。 Alpha 值表示色彩的透明度—色彩與背景色彩混合的範圍。 Alpha 值的範圍是從0到255，其中0代表完全透明的色彩，而255代表完全不透明的色彩。

Alpha 混色是來源和背景色彩資料的圖元 x 圖元混合。 這三個元件 (紅色、綠色、藍色) 指定來源色彩會根據下列公式，與背景色彩的對應元件混合：

displayColor = sourceColor × Alpha/255 + backgroundColor × (255 – Alpha) /255

例如，假設來源色彩的紅色元件是150，背景色彩的紅色元件是100。 如果 Alpha 值為200，則會計算結果色彩的紅色元件，如下所示：

150 × 200 / 255 + 100 × (255 – 200) / 255 = 139

下列主題涵蓋 Alpha 混合的詳細資訊：

-   [繪製不透明和半透明線條](-gdiplus-drawing-opaque-and-semitransparent-lines-use.md)
-   [使用不透明和半透明筆刷繪製](-gdiplus-drawing-with-opaque-and-semitransparent-brushes-use.md)
-   [使用複合模式控制 Alpha 混色](-gdiplus-using-compositing-mode-to-control-alpha-blending-use.md)
-   [使用色彩矩陣設定影像中的 Alpha 值](-gdiplus-using-a-color-matrix-to-set-alpha-values-in-images-use.md)
-   [設定個別圖元的 Alpha 值](-gdiplus-setting-the-alpha-values-of-individual-pixels-use.md)

 

 




---
description: 在 Windows GDI + 中，色彩是32位值，每個都有8個位，分別適用于 Alpha、紅色、綠色和藍色。
ms.assetid: f8c22d1a-b96b-4d16-928e-20adbae4c4a7
title: Alpha 混色線條和填色
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd13fe306dbf31c2a60a0bd38bf71b9e96edb201
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848874"
---
# <a name="alpha-blending-lines-and-fills"></a><span data-ttu-id="e2215-103">Alpha 混色線條和填色</span><span class="sxs-lookup"><span data-stu-id="e2215-103">Alpha Blending Lines and Fills</span></span>

<span data-ttu-id="e2215-104">在 Windows GDI + 中，色彩是32位值，每個都有8個位，分別適用于 Alpha、紅色、綠色和藍色。</span><span class="sxs-lookup"><span data-stu-id="e2215-104">In Windows GDI+, a color is a 32-bit value with 8 bits each for alpha, red, green, and blue.</span></span> <span data-ttu-id="e2215-105">Alpha 值表示色彩的透明度—色彩與背景色彩混合的範圍。</span><span class="sxs-lookup"><span data-stu-id="e2215-105">The alpha value indicates the transparency of the color — the extent to which the color is blended with the background color.</span></span> <span data-ttu-id="e2215-106">Alpha 值的範圍是從0到255，其中0代表完全透明的色彩，而255代表完全不透明的色彩。</span><span class="sxs-lookup"><span data-stu-id="e2215-106">Alpha values range from 0 through 255, where 0 represents a fully transparent color, and 255 represents a fully opaque color.</span></span>

<span data-ttu-id="e2215-107">Alpha 混色是來源和背景色彩資料的圖元 x 圖元混合。</span><span class="sxs-lookup"><span data-stu-id="e2215-107">Alpha blending is a pixel-by-pixel blending of source and background color data.</span></span> <span data-ttu-id="e2215-108">這三個元件 (紅色、綠色、藍色) 指定來源色彩會根據下列公式，與背景色彩的對應元件混合：</span><span class="sxs-lookup"><span data-stu-id="e2215-108">Each of the three components (red, green, blue) of a given source color is blended with the corresponding component of the background color according to the following formula:</span></span>

<span data-ttu-id="e2215-109">displayColor = sourceColor × Alpha/255 + backgroundColor × (255 – Alpha) /255</span><span class="sxs-lookup"><span data-stu-id="e2215-109">displayColor = sourceColor × alpha / 255 + backgroundColor × (255 – alpha) / 255</span></span>

<span data-ttu-id="e2215-110">例如，假設來源色彩的紅色元件是150，背景色彩的紅色元件是100。</span><span class="sxs-lookup"><span data-stu-id="e2215-110">For example, suppose the red component of the source color is 150 and the red component of the background color is 100.</span></span> <span data-ttu-id="e2215-111">如果 Alpha 值為200，則會計算結果色彩的紅色元件，如下所示：</span><span class="sxs-lookup"><span data-stu-id="e2215-111">If the alpha value is 200, the red component of the resultant color is calculated as follows:</span></span>

<span data-ttu-id="e2215-112">150 × 200 / 255 + 100 × (255 – 200) / 255 = 139</span><span class="sxs-lookup"><span data-stu-id="e2215-112">150 × 200 / 255 + 100 × (255 – 200) / 255 = 139</span></span>

<span data-ttu-id="e2215-113">下列主題涵蓋 Alpha 混合的詳細資訊：</span><span class="sxs-lookup"><span data-stu-id="e2215-113">The following topics cover alpha blending in more detail:</span></span>

-   [<span data-ttu-id="e2215-114">繪製不透明和半透明線條</span><span class="sxs-lookup"><span data-stu-id="e2215-114">Drawing Opaque and Semitransparent Lines</span></span>](-gdiplus-drawing-opaque-and-semitransparent-lines-use.md)
-   [<span data-ttu-id="e2215-115">使用不透明和半透明筆刷繪製</span><span class="sxs-lookup"><span data-stu-id="e2215-115">Drawing with Opaque and Semitransparent Brushes</span></span>](-gdiplus-drawing-with-opaque-and-semitransparent-brushes-use.md)
-   [<span data-ttu-id="e2215-116">使用複合模式控制 Alpha 混色</span><span class="sxs-lookup"><span data-stu-id="e2215-116">Using Compositing Mode to Control Alpha Blending</span></span>](-gdiplus-using-compositing-mode-to-control-alpha-blending-use.md)
-   [<span data-ttu-id="e2215-117">使用色彩矩陣設定影像中的 Alpha 值</span><span class="sxs-lookup"><span data-stu-id="e2215-117">Using a Color Matrix to Set Alpha Values in Images</span></span>](-gdiplus-using-a-color-matrix-to-set-alpha-values-in-images-use.md)
-   [<span data-ttu-id="e2215-118">設定個別圖元的 Alpha 值</span><span class="sxs-lookup"><span data-stu-id="e2215-118">Setting the Alpha Values of Individual Pixels</span></span>](-gdiplus-setting-the-alpha-values-of-individual-pixels-use.md)

 

 




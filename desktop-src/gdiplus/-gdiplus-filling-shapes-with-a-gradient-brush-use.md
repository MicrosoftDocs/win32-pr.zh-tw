---
description: 您可以使用漸層筆刷，以逐漸變更的色彩填滿形狀。
ms.assetid: e37b4c3a-b753-483a-990f-da3bcc70acf5
title: 使用漸層筆刷填滿圖案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6784d0bfd59fd37f217e8d7a1cdd230348807d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991350"
---
# <a name="filling-shapes-with-a-gradient-brush"></a><span data-ttu-id="470ea-103">使用漸層筆刷填滿圖案</span><span class="sxs-lookup"><span data-stu-id="470ea-103">Filling Shapes with a Gradient Brush</span></span>

<span data-ttu-id="470ea-104">您可以使用漸層筆刷，以逐漸變更的色彩填滿形狀。</span><span class="sxs-lookup"><span data-stu-id="470ea-104">You can use a gradient brush to fill a shape with a gradually changing color.</span></span> <span data-ttu-id="470ea-105">例如，您可以使用水準漸層來填滿圖形，其色彩會隨著您從圖形的左邊緣移至右邊緣而逐漸變更。</span><span class="sxs-lookup"><span data-stu-id="470ea-105">For example, you can use a horizontal gradient to fill a shape with color that changes gradually as you move from the left edge of the shape to the right edge.</span></span> <span data-ttu-id="470ea-106">假設矩形的左邊緣為黑色 (以紅色、綠色和藍色元件0、0、0) 和以紅色 (表示的右邊緣（以255、0、0) 表示）。</span><span class="sxs-lookup"><span data-stu-id="470ea-106">Imagine a rectangle with a left edge that is black (represented by red, green, and blue components 0, 0, 0) and a right edge that is red (represented by 255, 0, 0).</span></span> <span data-ttu-id="470ea-107">如果矩形的寬度為256圖元，則指定圖元的紅色元件將會大於其左邊圖元的紅色元件。</span><span class="sxs-lookup"><span data-stu-id="470ea-107">If the rectangle is 256 pixels wide, the red component of a given pixel will be one greater than the red component of the pixel to its left.</span></span> <span data-ttu-id="470ea-108">資料列中最左邊的圖元具有色彩元件 (0、0、0) 、第二個圖元 (1、0、0) 、第三個圖元有 (2、0、0) 等，直到您到達最右邊的圖元，其中有色彩元件 (255、0、0) 。</span><span class="sxs-lookup"><span data-stu-id="470ea-108">The leftmost pixel in a row has color components (0, 0, 0), the second pixel has (1, 0, 0), the third pixel has (2, 0, 0), and so on, until you get to the rightmost pixel, which has color components (255, 0, 0).</span></span> <span data-ttu-id="470ea-109">這些插補色彩值會構成色彩漸層。</span><span class="sxs-lookup"><span data-stu-id="470ea-109">These interpolated color values make up the color gradient.</span></span>

<span data-ttu-id="470ea-110">當您以水準、垂直或平行方式移動至指定的斜線時，線性漸層會變更色彩。</span><span class="sxs-lookup"><span data-stu-id="470ea-110">A linear gradient changes color as you move horizontally, vertically, or parallel to a specified slanted line.</span></span> <span data-ttu-id="470ea-111">當您移動路徑的內部和界限時，路徑漸層會變更色彩。</span><span class="sxs-lookup"><span data-stu-id="470ea-111">A path gradient changes color as you move about the interior and boundary of a path.</span></span> <span data-ttu-id="470ea-112">您可以自訂路徑漸層以達成各種效果。</span><span class="sxs-lookup"><span data-stu-id="470ea-112">You can customize path gradients to achieve a wide variety of effects.</span></span>

<span data-ttu-id="470ea-113">GDI + 提供 [**LinearGradientBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) 和 [**PathGradientBrush**](/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush) 類別，這兩個類別都是繼承自 [**筆刷**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) 類別。</span><span class="sxs-lookup"><span data-stu-id="470ea-113">GDI+ provides the [**LinearGradientBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) and [**PathGradientBrush**](/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush) classes, both of which inherit from the [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) class.</span></span>

<span data-ttu-id="470ea-114">下列主題會更詳細地討論線性和路徑漸層：</span><span class="sxs-lookup"><span data-stu-id="470ea-114">The following topics cover linear and path gradients in more detail:</span></span>

-   [<span data-ttu-id="470ea-115">建立線性漸層</span><span class="sxs-lookup"><span data-stu-id="470ea-115">Creating a Linear Gradient</span></span>](-gdiplus-creating-a-linear-gradient-use.md)
-   [<span data-ttu-id="470ea-116">建立路徑漸層</span><span class="sxs-lookup"><span data-stu-id="470ea-116">Creating a Path Gradient</span></span>](-gdiplus-creating-a-path-gradient-use.md)
-   [<span data-ttu-id="470ea-117">將 Gamma 修正套用至漸層</span><span class="sxs-lookup"><span data-stu-id="470ea-117">Applying Gamma Correction to a Gradient</span></span>](-gdiplus-applying-gamma-correction-to-a-gradient-use.md)

 

 




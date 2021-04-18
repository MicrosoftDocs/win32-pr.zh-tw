---
description: 路徑是圖形基本專案的序列， (線條、矩形、曲線、文字和類似的) ，可操作並繪製為單一單位。 路徑可以分割成已開啟或已關閉的圖形。 圖可包含數個基本類型。
ms.assetid: dbfe8cea-bd9e-43ad-85c8-37cce3ef97a4
title: 建構和繪製路徑
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fe5f1528e58e3df19afbc83bb6acfdc2a6fca19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991375"
---
# <a name="constructing-and-drawing-paths"></a><span data-ttu-id="7e8b0-105">建構和繪製路徑</span><span class="sxs-lookup"><span data-stu-id="7e8b0-105">Constructing and Drawing Paths</span></span>

<span data-ttu-id="7e8b0-106">路徑是圖形基本專案的序列， (線條、矩形、曲線、文字和類似的) ，可操作並繪製為單一單位。</span><span class="sxs-lookup"><span data-stu-id="7e8b0-106">A path is a sequence of graphics primitives (lines, rectangles, curves, text, and the like) that can be manipulated and drawn as a single unit.</span></span> <span data-ttu-id="7e8b0-107">路徑可以分割成已開啟或已關閉的 *圖形* 。</span><span class="sxs-lookup"><span data-stu-id="7e8b0-107">A path can be divided into *figures* that are either open or closed.</span></span> <span data-ttu-id="7e8b0-108">圖可包含數個基本類型。</span><span class="sxs-lookup"><span data-stu-id="7e8b0-108">A figure can contain several primitives.</span></span>

<span data-ttu-id="7e8b0-109">您可以藉由呼叫 graphics 類別的 [**graphics：:D rawpath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath)方法來繪製路徑，而且可以藉由呼叫 **Graphics** [**類別的**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) [**graphics：： FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath)方法來填滿路徑。</span><span class="sxs-lookup"><span data-stu-id="7e8b0-109">You can draw a path by calling the [**Graphics::DrawPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) method of the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class, and you can fill a path by calling the [**Graphics::FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) method of the **Graphics** class.</span></span>

<span data-ttu-id="7e8b0-110">下列主題會更詳細地討論路徑：</span><span class="sxs-lookup"><span data-stu-id="7e8b0-110">The following topics cover paths in more detail:</span></span>

-   [<span data-ttu-id="7e8b0-111">從線條、曲線和形狀建立圖形</span><span class="sxs-lookup"><span data-stu-id="7e8b0-111">Creating Figures from Lines, Curves, and Shapes</span></span>](-gdiplus-creating-figures-from-lines-curves-and-shapes-use.md)
-   [<span data-ttu-id="7e8b0-112">填滿開放圖形</span><span class="sxs-lookup"><span data-stu-id="7e8b0-112">Filling Open Figures</span></span>](-gdiplus-filling-open-figures-use.md)

 

 




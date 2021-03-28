---
description: Graphics 類別提供各種繪圖方法，包括下列清單所示的方法：
ms.assetid: d3c8d16c-858a-42a9-a512-3fcfa144f5fc
title: 使用畫筆繪製線條和形狀
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 904f53149038d6109365adddc11d3c37881a8def
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112937"
---
# <a name="using-a-pen-to-draw-lines-and-shapes"></a><span data-ttu-id="c840a-103">使用畫筆繪製線條和形狀</span><span class="sxs-lookup"><span data-stu-id="c840a-103">Using a Pen to Draw Lines and Shapes</span></span>

<span data-ttu-id="c840a-104">[**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)類別提供各種繪圖方法，包括下列清單所示的方法：</span><span class="sxs-lookup"><span data-stu-id="c840a-104">The [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class provides a variety of drawing methods including those shown in the following list:</span></span>

-   <span data-ttu-id="c840a-105">[DrawLine 方法](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint))</span><span class="sxs-lookup"><span data-stu-id="c840a-105">[DrawLine Methods](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint))</span></span>
-   <span data-ttu-id="c840a-106">[Graphicswindow.drawrectangle 方法](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inconstrectf_))</span><span class="sxs-lookup"><span data-stu-id="c840a-106">[DrawRectangle Methods](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inconstrectf_))</span></span>
-   <span data-ttu-id="c840a-107">[DrawEllipse 方法](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrectf_))</span><span class="sxs-lookup"><span data-stu-id="c840a-107">[DrawEllipse Methods](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrectf_))</span></span>
-   <span data-ttu-id="c840a-108">[DrawArc 方法](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawarc(inconstpen_inconstrectf__inreal_inreal))</span><span class="sxs-lookup"><span data-stu-id="c840a-108">[DrawArc Methods](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawarc(inconstpen_inconstrectf__inreal_inreal))</span></span>
-   [<span data-ttu-id="c840a-109">**圖形：:D rawPath**</span><span class="sxs-lookup"><span data-stu-id="c840a-109">**Graphics::DrawPath**</span></span>](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath)
-   <span data-ttu-id="c840a-110">[DrawCurve 方法](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawcurve(inconstpen_inconstpoint_inint))</span><span class="sxs-lookup"><span data-stu-id="c840a-110">[DrawCurve Methods](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawcurve(inconstpen_inconstpoint_inint))</span></span>
-   <span data-ttu-id="c840a-111">[DrawBezier 方法](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawbezier(inconstpen_inconstpointf__inconstpointf__inconstpointf__inconstpointf_))</span><span class="sxs-lookup"><span data-stu-id="c840a-111">[DrawBezier Methods](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawbezier(inconstpen_inconstpointf__inconstpointf__inconstpointf__inconstpointf_))</span></span>

<span data-ttu-id="c840a-112">您傳遞給這類繪圖方法的其中一個引數是 [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) 物件的位址。</span><span class="sxs-lookup"><span data-stu-id="c840a-112">One of the arguments that you pass to such a drawing method is the address of a [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object.</span></span>

<span data-ttu-id="c840a-113">下列主題將詳細說明如何使用畫筆：</span><span class="sxs-lookup"><span data-stu-id="c840a-113">The following topics cover the use of pens in more detail:</span></span>

-   [<span data-ttu-id="c840a-114">使用畫筆繪製線條和矩形</span><span class="sxs-lookup"><span data-stu-id="c840a-114">Using a Pen to Draw Lines and Rectangles</span></span>](-gdiplus-using-a-pen-to-draw-lines-and-rectangles-use.md)
-   [<span data-ttu-id="c840a-115">設定畫筆寬度和對齊方式</span><span class="sxs-lookup"><span data-stu-id="c840a-115">Setting Pen Width and Alignment</span></span>](-gdiplus-setting-pen-width-and-alignment-use.md)
-   [<span data-ttu-id="c840a-116">使用行帽繪製線條</span><span class="sxs-lookup"><span data-stu-id="c840a-116">Drawing a Line with Line Caps</span></span>](-gdiplus-drawing-a-line-with-line-caps-use.md)
-   [<span data-ttu-id="c840a-117">聯結線</span><span class="sxs-lookup"><span data-stu-id="c840a-117">Joining Lines</span></span>](-gdiplus-joining-lines-use.md)
-   [<span data-ttu-id="c840a-118">繪製自訂虛線</span><span class="sxs-lookup"><span data-stu-id="c840a-118">Drawing a Custom Dashed Line</span></span>](-gdiplus-drawing-a-custom-dashed-line-use.md)
-   [<span data-ttu-id="c840a-119">繪製填滿材質的線條</span><span class="sxs-lookup"><span data-stu-id="c840a-119">Drawing a Line Filled with a Texture</span></span>](-gdiplus-drawing-a-line-filled-with-a-texture-use.md)

 

 




---
description: GDI + 支援數種曲線類型：橢圓形、弧形、基線曲線和 B&\# 233; zier 曲線。
ms.assetid: 97a1342c-4edb-4671-b36d-b6992efad498
title: 建構和繪製曲線
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f61c1aa12e3152ed65cca2da6911d2d53def81b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991378"
---
# <a name="constructing-and-drawing-curves"></a><span data-ttu-id="2c023-103">建構和繪製曲線</span><span class="sxs-lookup"><span data-stu-id="2c023-103">Constructing and Drawing Curves</span></span>

<span data-ttu-id="2c023-104">GDI + 支援數種曲線類型：橢圓形、弧形、基線曲線和貝茲曲線。</span><span class="sxs-lookup"><span data-stu-id="2c023-104">GDI+ supports several types of curves: ellipses, arcs, cardinal splines, and Bézier splines.</span></span> <span data-ttu-id="2c023-105">橢圓形是由其周框所定義;弧形是由起始角度和清除角度所定義之橢圓形的一部分。</span><span class="sxs-lookup"><span data-stu-id="2c023-105">An ellipse is defined by its bounding rectangle; an arc is a portion of an ellipse defined by a starting angle and a sweep angle.</span></span> <span data-ttu-id="2c023-106">基本曲線是由點陣列和張力參數所定義—曲線會順暢地流經陣列中的每個點，而張力參數則會影響曲線的彎曲方式。</span><span class="sxs-lookup"><span data-stu-id="2c023-106">A cardinal spline is defined by an array of points and a tension parameter — the curve passes smoothly through each point in the array, and the tension parameter influences the way the curve bends.</span></span> <span data-ttu-id="2c023-107">貝茲曲線是由兩個端點和兩個控制點所定義—曲線不會通過控制點，但是控制點會影響方向和折彎，因為曲線會從某個端點移至另一個端點。</span><span class="sxs-lookup"><span data-stu-id="2c023-107">A Bézier spline is defined by two end points and two control points — the curve does not pass through the control points, but the control points influence the direction and bend as the curve goes from one end point to the other.</span></span>

<span data-ttu-id="2c023-108">下列主題會更詳細地討論基本曲線和貝茲曲線：</span><span class="sxs-lookup"><span data-stu-id="2c023-108">The following topics cover cardinal splines and Bézier splines in more detail:</span></span>

-   [<span data-ttu-id="2c023-109">繪製基本曲線</span><span class="sxs-lookup"><span data-stu-id="2c023-109">Drawing Cardinal Splines</span></span>](-gdiplus-drawing-cardinal-splines-use.md)
-   [<span data-ttu-id="2c023-110">繪圖貝茲曲線</span><span class="sxs-lookup"><span data-stu-id="2c023-110">Drawing Bézier Splines</span></span>](-gdiplus-drawing-bezier-splines-use.md)

 

 




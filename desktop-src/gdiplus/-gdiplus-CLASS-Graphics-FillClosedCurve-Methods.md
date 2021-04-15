---
description: 本主題列出 Graphics 類別的 FillClosedCurve 方法。 如需圖形類別之方法的完整清單，請參閱圖形。
ms.assetid: 378f0d34-7328-45e5-9f55-826bdaed3aab
title: 'FillClosedCurve 方法 (Gdiplusgraphics .h) '
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: c48ad7ffb772b6ff362fdb49995c969374eccc76
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "104992527"
---
# <a name="graphicsfillclosedcurve-methods"></a><span data-ttu-id="7be23-104">FillClosedCurve 方法</span><span class="sxs-lookup"><span data-stu-id="7be23-104">Graphics.FillClosedCurve methods</span></span>

<span data-ttu-id="7be23-105">本主題列出 [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 類別的 FillClosedCurve 方法。</span><span class="sxs-lookup"><span data-stu-id="7be23-105">This topic lists the FillClosedCurve methods of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class.</span></span> <span data-ttu-id="7be23-106">如需 **圖形** 類別之方法的完整清單，請參閱 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)。</span><span class="sxs-lookup"><span data-stu-id="7be23-106">For a complete list of methods for the **Graphics** class, see [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics).</span></span>

### <a name="overload-list"></a><span data-ttu-id="7be23-107">多載清單</span><span class="sxs-lookup"><span data-stu-id="7be23-107">Overload list</span></span>



| <span data-ttu-id="7be23-108">方法</span><span class="sxs-lookup"><span data-stu-id="7be23-108">Method</span></span>                                                                                                                                                              | <span data-ttu-id="7be23-109">描述</span><span class="sxs-lookup"><span data-stu-id="7be23-109">Description</span></span>                                                                                                                                                                                                                                                                                                   |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7be23-110">[**FillClosedCurve (筆刷 \* 、點 \* 、INT)**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillclosedcurve(inconstbrush_inconstpoint_inint))</span><span class="sxs-lookup"><span data-stu-id="7be23-110">[**FillClosedCurve(Brush\*,Point\*,INT)**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillclosedcurve(inconstbrush_inconstpoint_inint))</span></span>                                         | <span data-ttu-id="7be23-111">[**Graphics：： FillClosedCurve**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillclosedcurve(inconstbrush_inconstpoint_inint))方法會從點陣列建立封閉的基線曲線，並使用筆刷來填滿曲線的內部。</span><span class="sxs-lookup"><span data-stu-id="7be23-111">The [**Graphics::FillClosedCurve**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillclosedcurve(inconstbrush_inconstpoint_inint)) method creates a closed cardinal spline from an array of points and uses a brush to fill the interior of the spline.</span></span> <br/>                                                         |
| <span data-ttu-id="7be23-112">[**FillClosedCurve (筆刷 \* ，PointF \* ，INT)**](/previous-versions//ms535972(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7be23-112">[**FillClosedCurve(Brush\*,PointF\*,INT)**](/previous-versions//ms535972(v=vs.85))</span></span>                                       | <span data-ttu-id="7be23-113">[**Graphics：： FillClosedCurve**](/previous-versions//ms535972(v=vs.85))方法會從點陣列建立封閉的基線曲線，並使用筆刷來填滿曲線的內部。</span><span class="sxs-lookup"><span data-stu-id="7be23-113">The [**Graphics::FillClosedCurve**](/previous-versions//ms535972(v=vs.85)) method creates a closed cardinal spline from an array of points and uses a brush to fill the interior of the spline.</span></span><br/>                                                         |
| <span data-ttu-id="7be23-114">[**FillClosedCurve (筆刷 \* 、Point \* 、INT、FILLMODE、REAL)**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillclosedcurve(inconstbrush_inconstpoint_inint_infillmode_inreal))</span><span class="sxs-lookup"><span data-stu-id="7be23-114">[**FillClosedCurve(Brush\*,Point\*,INT,FillMode,REAL)**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillclosedcurve(inconstbrush_inconstpoint_inint_infillmode_inreal))</span></span>  | <span data-ttu-id="7be23-115">[**Graphics：： FillClosedCurve**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillclosedcurve(inconstbrush_inconstpoint_inint_infillmode_inreal))方法會從點陣列建立封閉的基線曲線，並根據指定的模式（曲線的內部），使用筆刷來填滿。</span><span class="sxs-lookup"><span data-stu-id="7be23-115">The [**Graphics::FillClosedCurve**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillclosedcurve(inconstbrush_inconstpoint_inint_infillmode_inreal)) method creates a closed cardinal spline from an array of points and uses a brush to fill, according to a specified mode, the interior of the spline.</span></span><br/> |
| <span data-ttu-id="7be23-116">[**FillClosedCurve (筆刷 \* 、PointF \* 、INT、FILLMODE、REAL)**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillclosedcurve(inconstbrush_inconstpointf_inint_infillmode_inreal))</span><span class="sxs-lookup"><span data-stu-id="7be23-116">[**FillClosedCurve(Brush\*,PointF\*,INT,FillMode,REAL)**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillclosedcurve(inconstbrush_inconstpointf_inint_infillmode_inreal))</span></span> | <span data-ttu-id="7be23-117">[**Graphics：： FillClosedCurve**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillclosedcurve(inconstbrush_inconstpointf_inint_infillmode_inreal))方法會從點陣列建立封閉的基線曲線，並根據指定的模式（曲線的內部），使用筆刷來填滿。</span><span class="sxs-lookup"><span data-stu-id="7be23-117">The [**Graphics::FillClosedCurve**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillclosedcurve(inconstbrush_inconstpointf_inint_infillmode_inreal)) method creates a closed cardinal spline from an array of points and uses a brush to fill, according to a specified mode, the interior of the spline.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="7be23-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="7be23-118">Requirements</span></span>



| <span data-ttu-id="7be23-119">需求</span><span class="sxs-lookup"><span data-stu-id="7be23-119">Requirement</span></span> | <span data-ttu-id="7be23-120">值</span><span class="sxs-lookup"><span data-stu-id="7be23-120">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7be23-121">標頭</span><span class="sxs-lookup"><span data-stu-id="7be23-121">Header</span></span><br/> | <dl> <span data-ttu-id="7be23-122"><dt>Gdiplusgraphics。h</dt></span><span class="sxs-lookup"><span data-stu-id="7be23-122"><dt>Gdiplusgraphics.h</dt></span></span> </dl> |



 

 

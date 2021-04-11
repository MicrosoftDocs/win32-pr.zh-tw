---
title: 'R (OpenGL) '
description: 以字母 R 為開頭之 OpenGL 詞彙的定義。
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: ab0286f5-cad2-4537-aa98-be0fce55ff53
keywords:
- 點陣化
- 矩形
- 轉譯
- RGBA
- RGBA 模式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b82a2db1bade12a0ff844006a1572cdc3b977dd
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "103842971"
---
# <a name="r-opengl"></a><span data-ttu-id="6ef0b-108">R (OpenGL) </span><span class="sxs-lookup"><span data-stu-id="6ef0b-108">R (OpenGL)</span></span>

<span data-ttu-id="6ef0b-109">[](a.md) [B](b.md) [C](c.md) [D](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) R [S](s.md) [T](t.md) [](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span><span class="sxs-lookup"><span data-stu-id="6ef0b-109">[A](a.md) [B](b.md) [C](c.md) [D](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) R [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span></span>

<dl> <dt>

<span data-ttu-id="6ef0b-110"><span id="opengl_rasterize"></span><span id="OPENGL_RASTERIZE"></span>**光柵**</span><span class="sxs-lookup"><span data-stu-id="6ef0b-110"><span id="opengl_rasterize"></span><span id="OPENGL_RASTERIZE"></span>**rasterize**</span></span>
</dt> <dd>

<span data-ttu-id="6ef0b-111">將投影點、線條或多邊形，或點陣圖或影像的圖元轉換成片段，每個片段都對應到畫面格緩衝區中的圖元。</span><span class="sxs-lookup"><span data-stu-id="6ef0b-111">To convert a projected point, line, or polygon, or the pixels of a bitmap or image, to fragments, each corresponding to a pixel in the framebuffer.</span></span> <span data-ttu-id="6ef0b-112">請注意，所有基本專案都是柵格化的，而不只是點、線條和多邊形</span><span class="sxs-lookup"><span data-stu-id="6ef0b-112">Note that all primitives are rasterized, not just points, lines, and polygons</span></span>

</dd> <dt>

<span data-ttu-id="6ef0b-113"><span id="opengl_rectangle"></span><span id="OPENGL_RECTANGLE"></span>**矩形**</span><span class="sxs-lookup"><span data-stu-id="6ef0b-113"><span id="opengl_rectangle"></span><span id="OPENGL_RECTANGLE"></span>**rectangle**</span></span>
</dt> <dd>

<span data-ttu-id="6ef0b-114">四邊形，其替代邊緣會以物件座標平行處理。</span><span class="sxs-lookup"><span data-stu-id="6ef0b-114">A quadrilateral whose alternate edges are parallel to each other in object coordinates.</span></span> <span data-ttu-id="6ef0b-115">以 glRect ( ) 指定的多邊形 \* 一律為矩形; 其他 quadrilaterals 可能是矩形。</span><span class="sxs-lookup"><span data-stu-id="6ef0b-115">Polygons specified with glRect\*( ) are always rectangles; other quadrilaterals might be rectangles.</span></span>

</dd> <dt>

<span data-ttu-id="6ef0b-116"><span id="opengl_rendering"></span><span id="OPENGL_RENDERING"></span>**渲染**</span><span class="sxs-lookup"><span data-stu-id="6ef0b-116"><span id="opengl_rendering"></span><span id="OPENGL_RENDERING"></span>**rendering**</span></span>
</dt> <dd>

<span data-ttu-id="6ef0b-117">將物件座標中指定的基本類型轉換成畫面格緩衝區中的影像。</span><span class="sxs-lookup"><span data-stu-id="6ef0b-117">Conversion of primitives specified in object coordinates to an image in the framebuffer.</span></span> <span data-ttu-id="6ef0b-118">轉譯是 OpenGL 的主要作業。</span><span class="sxs-lookup"><span data-stu-id="6ef0b-118">Rendering is the primary operation of OpenGL.</span></span>

</dd> <dt>

<span data-ttu-id="6ef0b-119"><span id="opengl_rgba"></span><span id="OPENGL_RGBA"></span>**RGBA**</span><span class="sxs-lookup"><span data-stu-id="6ef0b-119"><span id="opengl_rgba"></span><span id="OPENGL_RGBA"></span>**RGBA**</span></span>
</dt> <dd>

<span data-ttu-id="6ef0b-120">RGBA 模式的紅色、綠色、藍色和 Alpha 色彩元件。</span><span class="sxs-lookup"><span data-stu-id="6ef0b-120">The red, green, blue, and alpha color components of the RGBA mode.</span></span>

</dd> <dt>

<span data-ttu-id="6ef0b-121"><span id="opengl_rgba_mode"></span><span id="OPENGL_RGBA_MODE"></span>**RGBA 模式**</span><span class="sxs-lookup"><span data-stu-id="6ef0b-121"><span id="opengl_rgba_mode"></span><span id="OPENGL_RGBA_MODE"></span>**RGBA mode**</span></span>
</dt> <dd>

<span data-ttu-id="6ef0b-122">OpenGL 內容，其中的色彩緩衝區會儲存紅色、綠色、藍色和 Alpha 色彩元件，而不是色彩索引。</span><span class="sxs-lookup"><span data-stu-id="6ef0b-122">An OpenGL context in which its color buffers store red, green, blue, and alpha color components, rather than color indexes.</span></span>

</dd> </dl>

 

 





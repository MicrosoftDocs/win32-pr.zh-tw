---
title: 'W (OpenGL) '
description: 以字母 W 開頭的 OpenGL 詞彙定義。
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 7f8235a3-ea48-40eb-8957-e7a55a5778af
keywords:
- windows
- 對齊視窗
- 視窗座標
- 著色
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1f6f1897af46c85ed48171d251ebe1b2de8c5e1
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "103685351"
---
# <a name="w-opengl"></a><span data-ttu-id="dd68a-107">W (OpenGL) </span><span class="sxs-lookup"><span data-stu-id="dd68a-107">W (OpenGL)</span></span>

<span data-ttu-id="dd68a-108">[](a.md) [B](b.md) [C](c.md) [D](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [W](u-v.md) [X Y Z](x-y-z.md)</span><span class="sxs-lookup"><span data-stu-id="dd68a-108">[A](a.md) [B](b.md) [C](c.md) [D](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) W [X Y Z](x-y-z.md)</span></span>

<dl> <dt>

<span data-ttu-id="dd68a-109"><span id="opengl_window"></span><span id="OPENGL_WINDOW"></span>**視窗**</span><span class="sxs-lookup"><span data-stu-id="dd68a-109"><span id="opengl_window"></span><span id="OPENGL_WINDOW"></span>**window**</span></span>
</dt> <dd>

<span data-ttu-id="dd68a-110">畫面格緩衝區的子領域，通常是矩形，其圖元全都具有相同的緩衝區設定。</span><span class="sxs-lookup"><span data-stu-id="dd68a-110">A subregion of the framebuffer, usually rectangular, whose pixels all have the same buffer configuration.</span></span> <span data-ttu-id="dd68a-111">OpenGL 內容會一次轉譯成一個視窗。</span><span class="sxs-lookup"><span data-stu-id="dd68a-111">An OpenGL context renders to one window at a time.</span></span>

</dd> <dt>

<span data-ttu-id="dd68a-112"><span id="opengl_window_aligned"></span><span id="OPENGL_WINDOW_ALIGNED"></span>**對齊視窗**</span><span class="sxs-lookup"><span data-stu-id="dd68a-112"><span id="opengl_window_aligned"></span><span id="OPENGL_WINDOW_ALIGNED"></span>**window-aligned**</span></span>
</dt> <dd>

<span data-ttu-id="dd68a-113">輔助線段或多邊形邊緣時，表示這些會與視窗界限平行。</span><span class="sxs-lookup"><span data-stu-id="dd68a-113">When referring to line segments or polygon edges, implies that these are parallel to the window boundaries.</span></span> <span data-ttu-id="dd68a-114"> (在 OpenGL 中，視窗是矩形，水準和垂直邊緣) 。</span><span class="sxs-lookup"><span data-stu-id="dd68a-114">(In OpenGL, the window is rectangular, with horizontal and vertical edges).</span></span> <span data-ttu-id="dd68a-115">參考多邊形模式時，表示模式是相對於視窗原點固定的。</span><span class="sxs-lookup"><span data-stu-id="dd68a-115">When referring to a polygon pattern, implies that the pattern is fixed relative to the window origin.</span></span>

</dd> <dt>

<span data-ttu-id="dd68a-116"><span id="opengl_window_coordinates"></span><span id="OPENGL_WINDOW_COORDINATES"></span>**視窗座標**</span><span class="sxs-lookup"><span data-stu-id="dd68a-116"><span id="opengl_window_coordinates"></span><span id="OPENGL_WINDOW_COORDINATES"></span>**window coordinates**</span></span>
</dt> <dd>

<span data-ttu-id="dd68a-117">視窗的座標系統。</span><span class="sxs-lookup"><span data-stu-id="dd68a-117">The coordinate system of a window.</span></span> <span data-ttu-id="dd68a-118">請務必區分圖元的名稱，這些名稱是離散的，而視窗座標系統則是連續的。</span><span class="sxs-lookup"><span data-stu-id="dd68a-118">It's important to distinguish between the names of pixels, which are discrete, and the window-coordinate system, which is continuous.</span></span> <span data-ttu-id="dd68a-119">例如，視窗左下角的圖元是圖元 (0、0) ;這個圖元中央的視窗座標是 (0.5、0.5、z) 。</span><span class="sxs-lookup"><span data-stu-id="dd68a-119">For example, the pixel at the lower-left corner of a window is pixel (0, 0); the window coordinates of the center of this pixel are (0.5, 0.5, z).</span></span> <span data-ttu-id="dd68a-120">請注意，視窗座標包含深度或 z、元件，而且此元件也是連續的。</span><span class="sxs-lookup"><span data-stu-id="dd68a-120">Note that window coordinates include a depth, or z, component, and that this component is continuous as well.</span></span>

</dd> <dt>

<span data-ttu-id="dd68a-121"><span id="opengl_wireframe"></span><span id="OPENGL_WIREFRAME"></span>**著色**</span><span class="sxs-lookup"><span data-stu-id="dd68a-121"><span id="opengl_wireframe"></span><span id="OPENGL_WIREFRAME"></span>**wireframe**</span></span>
</dt> <dd>

<span data-ttu-id="dd68a-122">物件的表示，其中只包含行區段。</span><span class="sxs-lookup"><span data-stu-id="dd68a-122">A representation of an object that contains line segments only.</span></span> <span data-ttu-id="dd68a-123">通常，線段表示多邊形邊緣。</span><span class="sxs-lookup"><span data-stu-id="dd68a-123">Typically, the line segments indicate polygon edges.</span></span>

</dd> </dl>

 

 





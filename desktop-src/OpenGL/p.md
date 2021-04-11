---
title: 'P (OpenGL) '
description: 以字母 P 開頭之 OpenGL 詞彙的定義。
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: bc7b0c93-af06-44a4-8bb8-adc0c6fedb6e
keywords:
- 參數
- 透視圖部門
- 像素
- 點
- 多邊形
- 原
- 投射矩陣
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9970b3eb84920184e693ace93b14120828573e30
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "103933833"
---
# <a name="p-opengl"></a><span data-ttu-id="d1f78-110">P (OpenGL) </span><span class="sxs-lookup"><span data-stu-id="d1f78-110">P (OpenGL)</span></span>

<span data-ttu-id="d1f78-111">[](a.md) [B](b.md) [C](c.md) [D](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) P [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span><span class="sxs-lookup"><span data-stu-id="d1f78-111">[A](a.md) [B](b.md) [C](c.md) [D](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) P [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span></span>

<dl> <dt>

<span data-ttu-id="d1f78-112"><span id="opengl_parameter"></span><span id="OPENGL_PARAMETER"></span>**參數**</span><span class="sxs-lookup"><span data-stu-id="d1f78-112"><span id="opengl_parameter"></span><span id="OPENGL_PARAMETER"></span>**parameter**</span></span>
</dt> <dd>

<span data-ttu-id="d1f78-113">以引數形式傳遞至 OpenGL 命令的值。</span><span class="sxs-lookup"><span data-stu-id="d1f78-113">A value passed as an argument to an OpenGL command.</span></span> <span data-ttu-id="d1f78-114">有時會以傳址方式傳遞至 OpenGL 命令的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="d1f78-114">Sometimes one of the values passed by reference to an OpenGL command.</span></span>

</dd> <dt>

<span data-ttu-id="d1f78-115"><span id="opengl_perspective_division"></span><span id="OPENGL_PERSPECTIVE_DIVISION"></span>**透視圖部門**</span><span class="sxs-lookup"><span data-stu-id="d1f78-115"><span id="opengl_perspective_division"></span><span id="OPENGL_PERSPECTIVE_DIVISION"></span>**perspective division**</span></span>
</dt> <dd>

<span data-ttu-id="d1f78-116">X、y 和 z 的除以 w，會在剪切座標中執行。</span><span class="sxs-lookup"><span data-stu-id="d1f78-116">The division of x, y, and z by w, carried out in clip coordinates.</span></span> <span data-ttu-id="d1f78-117">另請參閱 [裁剪座標](c.md)。</span><span class="sxs-lookup"><span data-stu-id="d1f78-117">See also [clip coordinates](c.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1f78-118"><span id="opengl_pixel"></span><span id="OPENGL_PIXEL"></span>**圖元**</span><span class="sxs-lookup"><span data-stu-id="d1f78-118"><span id="opengl_pixel"></span><span id="OPENGL_PIXEL"></span>**pixel**</span></span>
</dt> <dd>

<span data-ttu-id="d1f78-119">圖片元素。</span><span class="sxs-lookup"><span data-stu-id="d1f78-119">Picture element.</span></span> <span data-ttu-id="d1f78-120">在畫面格緩衝區中所有 bitplanes 的位置 (x，y) 的位會構成單一圖元 (x，y) 。</span><span class="sxs-lookup"><span data-stu-id="d1f78-120">The bits at location (x, y) of all the bitplanes in the framebuffer constitute the single pixel (x, y).</span></span> <span data-ttu-id="d1f78-121">在用戶端記憶體的影像中，圖元是一個元素群組。</span><span class="sxs-lookup"><span data-stu-id="d1f78-121">In an image in client memory, a pixel is one group of elements.</span></span> <span data-ttu-id="d1f78-122">在 OpenGL 視窗座標中，每個圖元都會對應到 1.0 x 1.0 的螢幕區域。</span><span class="sxs-lookup"><span data-stu-id="d1f78-122">In OpenGL window coordinates, each pixel corresponds to a 1.0x1.0 screen area.</span></span> <span data-ttu-id="d1f78-123">圖元名稱 x、y 的左下角座標為 (x、y) ，而右上角 (x + 1、y + 1) 。</span><span class="sxs-lookup"><span data-stu-id="d1f78-123">The coordinates of the lower-left corner of the pixel names x, y are (x, y), and the upper-right corner are (x+1, y+1).</span></span>

</dd> <dt>

<span data-ttu-id="d1f78-124"><span id="opengl_point"></span><span id="OPENGL_POINT"></span>**點**</span><span class="sxs-lookup"><span data-stu-id="d1f78-124"><span id="opengl_point"></span><span id="OPENGL_POINT"></span>**point**</span></span>
</dt> <dd>

<span data-ttu-id="d1f78-125">空間中的確切位置，會轉譯為有限的直徑點。</span><span class="sxs-lookup"><span data-stu-id="d1f78-125">An exact location in space, which is rendered as a finite-diameter dot.</span></span>

</dd> <dt>

<span data-ttu-id="d1f78-126"><span id="opengl_polygon"></span><span id="OPENGL_POLYGON"></span>**多邊形**</span><span class="sxs-lookup"><span data-stu-id="d1f78-126"><span id="opengl_polygon"></span><span id="OPENGL_POLYGON"></span>**polygon**</span></span>
</dt> <dd>

<span data-ttu-id="d1f78-127">由頂點指定的邊緣周圍的平面介面。</span><span class="sxs-lookup"><span data-stu-id="d1f78-127">A near-planar surface bounded by edges specified by vertices.</span></span> <span data-ttu-id="d1f78-128">三角形網格的每個三角形都是多邊形，如同四邊形網格的每個四邊形。</span><span class="sxs-lookup"><span data-stu-id="d1f78-128">Each triangle of a triangle mesh is a polygon, as is each quadrilateral of a quadrilateral mesh.</span></span> <span data-ttu-id="d1f78-129">GlRect 所指定的矩形也是多邊形。</span><span class="sxs-lookup"><span data-stu-id="d1f78-129">The rectangle specified by glRect is also a polygon.</span></span>

</dd> <dt>

<span data-ttu-id="d1f78-130"><span id="opengl_primitive"></span><span id="OPENGL_PRIMITIVE"></span>**原始**</span><span class="sxs-lookup"><span data-stu-id="d1f78-130"><span id="opengl_primitive"></span><span id="OPENGL_PRIMITIVE"></span>**primitive**</span></span>
</dt> <dd>

<span data-ttu-id="d1f78-131">圖形 (例如點、線條、多邊形、點陣圖或影像) ，可繪製、儲存和操作為離散實體;建立大型圖形設計的元素。</span><span class="sxs-lookup"><span data-stu-id="d1f78-131">A shape (such as a point, line, polygon, bitmap, or image) that can be drawn, stored, and manipulated as a discrete entity; elements from which large graphic designs are created.</span></span>

</dd> <dt>

<span data-ttu-id="d1f78-132"><span id="opengl_projection_matrix"></span><span id="OPENGL_PROJECTION_MATRIX"></span>**投射矩陣**</span><span class="sxs-lookup"><span data-stu-id="d1f78-132"><span id="opengl_projection_matrix"></span><span id="OPENGL_PROJECTION_MATRIX"></span>**projection matrix**</span></span>
</dt> <dd>

<span data-ttu-id="d1f78-133">4x4 矩陣，會將點、線條、多邊形和點陣位置從眼睛座標轉換成剪切座標。</span><span class="sxs-lookup"><span data-stu-id="d1f78-133">The 4x4 matrix that transforms points, lines, polygons, and raster positions from eye coordinates to clip coordinates.</span></span>

</dd> </dl>

 

 





---
title: 'T (OpenGL) '
description: 以字母 T 開頭之 OpenGL 詞彙的定義。
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: effb170b-fea3-4954-9f9c-3bc1aa829bc0
keywords:
- 鑲嵌
- 材質
- 紋理
- 材質對應
- 材質矩陣
- 轉換
- 三角形
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1cb324179137dbf9f9046c0c19acfffdf7394e1
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104093607"
---
# <a name="t-opengl"></a><span data-ttu-id="be86a-110">T (OpenGL) </span><span class="sxs-lookup"><span data-stu-id="be86a-110">T (OpenGL)</span></span>

<span data-ttu-id="be86a-111">[](a.md) [B](b.md) [C](c.md) [D](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span><span class="sxs-lookup"><span data-stu-id="be86a-111">[A](a.md) [B](b.md) [C](c.md) [D](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) T [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span></span>

<dl> <dt>

<span data-ttu-id="be86a-112"><span id="opengl_tessellation"></span><span id="OPENGL_TESSELLATION"></span>**鑲嵌**</span><span class="sxs-lookup"><span data-stu-id="be86a-112"><span id="opengl_tessellation"></span><span id="OPENGL_TESSELLATION"></span>**tessellation**</span></span>
</dt> <dd>

<span data-ttu-id="be86a-113">將分析表面的一部分縮減為多邊形的格線，或將分析曲線的一部分縮減為一連串的線條。</span><span class="sxs-lookup"><span data-stu-id="be86a-113">Reduction of a portion of an analytic surface to a mesh of polygons, or of a portion of an analytic curve to a sequence of lines.</span></span>

</dd> <dt>

<span data-ttu-id="be86a-114"><span id="opengl_texel"></span><span id="OPENGL_TEXEL"></span>**材質**</span><span class="sxs-lookup"><span data-stu-id="be86a-114"><span id="opengl_texel"></span><span id="OPENGL_TEXEL"></span>**texel**</span></span>
</dt> <dd>

<span data-ttu-id="be86a-115">材質元素。</span><span class="sxs-lookup"><span data-stu-id="be86a-115">A texture element.</span></span> <span data-ttu-id="be86a-116">材質是從紋理記憶體取得，代表要套用至對應片段的材質色彩。</span><span class="sxs-lookup"><span data-stu-id="be86a-116">A texel is obtained from texture memory and represents the color of the texture to be applied to a corresponding fragment.</span></span> <span data-ttu-id="be86a-117">另請參閱 [片段](f.md)。</span><span class="sxs-lookup"><span data-stu-id="be86a-117">See also [fragment](f.md).</span></span>

</dd> <dt>

<span data-ttu-id="be86a-118"><span id="opengl_texture"></span><span id="OPENGL_TEXTURE"></span>**紋理**</span><span class="sxs-lookup"><span data-stu-id="be86a-118"><span id="opengl_texture"></span><span id="OPENGL_TEXTURE"></span>**texture**</span></span>
</dt> <dd>

<span data-ttu-id="be86a-119">用來修改點陣化所產生片段色彩的一或兩個維度影像。</span><span class="sxs-lookup"><span data-stu-id="be86a-119">A one- or two-dimensional image used to modify the color of fragments produced by rasterization.</span></span> <span data-ttu-id="be86a-120">另請參閱「 [光柵](r.md)化」。</span><span class="sxs-lookup"><span data-stu-id="be86a-120">See also [rasterize](r.md).</span></span>

</dd> <dt>

<span data-ttu-id="be86a-121"><span id="opengl_texture_mapping"></span><span id="OPENGL_TEXTURE_MAPPING"></span>**材質對應**</span><span class="sxs-lookup"><span data-stu-id="be86a-121"><span id="opengl_texture_mapping"></span><span id="OPENGL_TEXTURE_MAPPING"></span>**texture mapping**</span></span>
</dt> <dd>

<span data-ttu-id="be86a-122">將影像 (材質) 套用至基本的流程。</span><span class="sxs-lookup"><span data-stu-id="be86a-122">The process of applying an image (the texture) to a primitive.</span></span> <span data-ttu-id="be86a-123">材質對應通常用來為場景增加逼真。</span><span class="sxs-lookup"><span data-stu-id="be86a-123">Texture mapping is often used to add realism to a scene.</span></span> <span data-ttu-id="be86a-124">例如，您可以將大樓外觀的圖片套用至代表牆的多邊形。</span><span class="sxs-lookup"><span data-stu-id="be86a-124">For example, you could apply a picture of a building facade to a polygon representing a wall.</span></span> <span data-ttu-id="be86a-125">另請參閱材質。</span><span class="sxs-lookup"><span data-stu-id="be86a-125">See also texture.</span></span>

</dd> <dt>

<span data-ttu-id="be86a-126"><span id="opengl_texture_matrix"></span><span id="OPENGL_TEXTURE_MATRIX"></span>**材質矩陣**</span><span class="sxs-lookup"><span data-stu-id="be86a-126"><span id="opengl_texture_matrix"></span><span id="OPENGL_TEXTURE_MATRIX"></span>**texture matrix**</span></span>
</dt> <dd>

<span data-ttu-id="be86a-127">4x4 矩陣，可將材質座標從其所指定的座標轉換為用於插補和材質查閱的座標。</span><span class="sxs-lookup"><span data-stu-id="be86a-127">The 4x4 matrix that transforms texture coordinates from the coordinates that they're specified in to the coordinates that are used for interpolation and texture lookup.</span></span>

</dd> <dt>

<span data-ttu-id="be86a-128"><span id="opengl_transformation"></span><span id="OPENGL_TRANSFORMATION"></span>**轉型**</span><span class="sxs-lookup"><span data-stu-id="be86a-128"><span id="opengl_transformation"></span><span id="OPENGL_TRANSFORMATION"></span>**transformation**</span></span>
</dt> <dd>

<span data-ttu-id="be86a-129">扭曲的空間。</span><span class="sxs-lookup"><span data-stu-id="be86a-129">A warping of space.</span></span> <span data-ttu-id="be86a-130">在 OpenGL 中，轉換僅限於 projective 轉換，這些轉換包含可由4x4 矩陣表示的任何事物。</span><span class="sxs-lookup"><span data-stu-id="be86a-130">In OpenGL, transformations are limited to projective transformations that include anything that can be represented by a 4x4 matrix.</span></span> <span data-ttu-id="be86a-131">這類轉換包括旋轉、翻譯、 (非統一) scalings 沿著座標軸、觀點轉換以及這些的組合。</span><span class="sxs-lookup"><span data-stu-id="be86a-131">Such transformations include rotations, translations, (nonuniform) scalings along the coordinate axes, perspective transformations, and combinations of these.</span></span>

</dd> <dt>

<span data-ttu-id="be86a-132"><span id="opengl_triangle"></span><span id="OPENGL_TRIANGLE"></span>**三角形**</span><span class="sxs-lookup"><span data-stu-id="be86a-132"><span id="opengl_triangle"></span><span id="OPENGL_TRIANGLE"></span>**triangle**</span></span>
</dt> <dd>

<span data-ttu-id="be86a-133">具有三個邊緣的多邊形。</span><span class="sxs-lookup"><span data-stu-id="be86a-133">A polygon with three edges.</span></span> <span data-ttu-id="be86a-134">三角形一律為凸凸。</span><span class="sxs-lookup"><span data-stu-id="be86a-134">Triangles are always convex.</span></span>

</dd> </dl>

 

 





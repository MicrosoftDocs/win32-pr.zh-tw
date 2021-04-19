---
title: 'F (OpenGL) '
description: 以字母 F 開頭之 OpenGL 詞彙的定義。
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: ba960409-84e0-4ece-967b-97f0e1183956
keywords:
- 臉部
- 平面網底
- 霧
- 字型
- fragments
- framebuffers
- 正面臉部
- 截
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7085765a5585268acb2f20a77c72bdd7cf1b4b81
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "106969746"
---
# <a name="f-opengl"></a><span data-ttu-id="3e836-111">F (OpenGL) </span><span class="sxs-lookup"><span data-stu-id="3e836-111">F (OpenGL)</span></span>

<span data-ttu-id="3e836-112">[](a.md) [B](b.md) [C](c.md) [D](d.md) [E](e.md) F [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span><span class="sxs-lookup"><span data-stu-id="3e836-112">[A](a.md) [B](b.md) [C](c.md) [D](d.md) [E](e.md) F [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span></span>

<dl> <dt>

<span data-ttu-id="3e836-113"><span id="opengl_face"></span><span id="OPENGL_FACE"></span>**臉**</span><span class="sxs-lookup"><span data-stu-id="3e836-113"><span id="opengl_face"></span><span id="OPENGL_FACE"></span>**face**</span></span>
</dt> <dd>

<span data-ttu-id="3e836-114">多邊形的一端。</span><span class="sxs-lookup"><span data-stu-id="3e836-114">One side of a polygon.</span></span> <span data-ttu-id="3e836-115">每個多邊形都有兩個臉部：正面臉部和背面表面。</span><span class="sxs-lookup"><span data-stu-id="3e836-115">Each polygon has two faces: a front face and a back face.</span></span> <span data-ttu-id="3e836-116">視窗中只會顯示一張臉部。</span><span class="sxs-lookup"><span data-stu-id="3e836-116">Only one face is ever visible in the window.</span></span> <span data-ttu-id="3e836-117">當多邊形投射到視窗之後，是否可以看到背面或正面臉部。</span><span class="sxs-lookup"><span data-stu-id="3e836-117">Whether the back or front face is visible is effectively determined after the polygon is projected onto the window.</span></span> <span data-ttu-id="3e836-118">在此投射之後，如果多邊形的邊緣有順向方向，則會顯示其中一個臉部;如果有逆時針方向，則會顯示另一個臉部。</span><span class="sxs-lookup"><span data-stu-id="3e836-118">After this projection, if the polygon's edges are directed clockwise, one of the faces is visible; if directed counterclockwise, the other face is visible.</span></span> <span data-ttu-id="3e836-119">無論是否以順向的方式對應至 front 或 back (，以及逆時針對應至 back 或 front) 是由 OpenGL 程式設計師所決定。</span><span class="sxs-lookup"><span data-stu-id="3e836-119">Whether clockwise corresponds to front or back (and counterclockwise corresponds to back or front) is determined by the OpenGL programmer.</span></span>

</dd> <dt>

<span data-ttu-id="3e836-120"><span id="opengl_flat_shading"></span><span id="OPENGL_FLAT_SHADING"></span>**平面網底**</span><span class="sxs-lookup"><span data-stu-id="3e836-120"><span id="opengl_flat_shading"></span><span id="OPENGL_FLAT_SHADING"></span>**flat shading**</span></span>
</dt> <dd>

<span data-ttu-id="3e836-121">是指將具有單一、常數色彩的基本色彩著色，而不是在基本的範圍內順暢地插上色彩。</span><span class="sxs-lookup"><span data-stu-id="3e836-121">Refers to coloring a primitive with a single, constant color across its extent, rather than smoothly interpolating colors across the primitive.</span></span> <span data-ttu-id="3e836-122">請參閱 [Gouraud 網底](g.md)。</span><span class="sxs-lookup"><span data-stu-id="3e836-122">See [Gouraud shading](g.md).</span></span>

</dd> <dt>

<span data-ttu-id="3e836-123"><span id="opengl_fog"></span><span id="OPENGL_FOG"></span>**霧**</span><span class="sxs-lookup"><span data-stu-id="3e836-123"><span id="opengl_fog"></span><span id="OPENGL_FOG"></span>**fog**</span></span>
</dt> <dd>

<span data-ttu-id="3e836-124">一種轉譯技術，可用來模擬迷霧、霧化和廢氣檢測等大氣效果，方法是根據檢視器的距離，將物件色彩淡化為背景色彩。</span><span class="sxs-lookup"><span data-stu-id="3e836-124">A rendering technique that can be used to simulate atmospheric effects such as haze, fog, and smog by fading object colors to a background color based on distance from the viewer.</span></span> <span data-ttu-id="3e836-125">霧化也有助於查看檢視器距離，並提供深度提示。</span><span class="sxs-lookup"><span data-stu-id="3e836-125">Fog also aids in the perception of distance from the viewer, giving a depth cue.</span></span> <span data-ttu-id="3e836-126">另請參閱 [深度-提示](d.md)。</span><span class="sxs-lookup"><span data-stu-id="3e836-126">See also [depth-cueing](d.md).</span></span>

</dd> <dt>

<span data-ttu-id="3e836-127"><span id="opengl_font"></span><span id="OPENGL_FONT"></span>**字體**</span><span class="sxs-lookup"><span data-stu-id="3e836-127"><span id="opengl_font"></span><span id="OPENGL_FONT"></span>**font**</span></span>
</dt> <dd>

<span data-ttu-id="3e836-128">一組圖形字元表示通常用來顯示文字字串。</span><span class="sxs-lookup"><span data-stu-id="3e836-128">A group of graphical character representations usually used to display strings of text.</span></span> <span data-ttu-id="3e836-129">這些字元可以是羅馬字母、數學符號、亞洲表意文字、埃及 hieroglyphs 等等。</span><span class="sxs-lookup"><span data-stu-id="3e836-129">The characters may be roman letters, mathematical symbols, Asian ideograms, Egyptian hieroglyphs, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="3e836-130"><span id="opengl_fragment"></span><span id="OPENGL_FRAGMENT"></span>**片段**</span><span class="sxs-lookup"><span data-stu-id="3e836-130"><span id="opengl_fragment"></span><span id="OPENGL_FRAGMENT"></span>**fragment**</span></span>
</dt> <dd>

<span data-ttu-id="3e836-131">由基本圖形所產生的圖形資料。</span><span class="sxs-lookup"><span data-stu-id="3e836-131">Graphic data generated by the rasterization of primitives.</span></span> <span data-ttu-id="3e836-132">每個片段都對應至單一圖元，並且包含色彩、深度，以及有時材質座標值。</span><span class="sxs-lookup"><span data-stu-id="3e836-132">Each fragment corresponds to a single pixel and includes color, depth, and sometimes texture-coordinate values.</span></span>

</dd> <dt>

<span data-ttu-id="3e836-133"><span id="opengl_framebuffer"></span><span id="OPENGL_FRAMEBUFFER"></span>**畫面格緩衝區**</span><span class="sxs-lookup"><span data-stu-id="3e836-133"><span id="opengl_framebuffer"></span><span id="OPENGL_FRAMEBUFFER"></span>**framebuffer**</span></span>
</dt> <dd>

<span data-ttu-id="3e836-134">Bitplanes 的堆疊。</span><span class="sxs-lookup"><span data-stu-id="3e836-134">A stack of bitplanes.</span></span> <span data-ttu-id="3e836-135">給定視窗或內容的所有緩衝區。</span><span class="sxs-lookup"><span data-stu-id="3e836-135">All the buffers of a given window or context.</span></span> <span data-ttu-id="3e836-136">有時會包含圖形硬體加速器的所有圖元記憶體。</span><span class="sxs-lookup"><span data-stu-id="3e836-136">Sometimes includes all the pixel memory of the graphics hardware accelerator.</span></span> <span data-ttu-id="3e836-137">另請參閱 [bitplane](b.md)。</span><span class="sxs-lookup"><span data-stu-id="3e836-137">See also [bitplane](b.md).</span></span>

</dd> <dt>

<span data-ttu-id="3e836-138"><span id="opengl_front_face"></span><span id="OPENGL_FRONT_FACE"></span>**正面臉部**</span><span class="sxs-lookup"><span data-stu-id="3e836-138"><span id="opengl_front_face"></span><span id="OPENGL_FRONT_FACE"></span>**front face**</span></span>
</dt> <dd>

<span data-ttu-id="3e836-139">請參閱臉部。</span><span class="sxs-lookup"><span data-stu-id="3e836-139">See face.</span></span>

</dd> <dt>

<span data-ttu-id="3e836-140"><span id="opengl_frustum"></span><span id="OPENGL_FRUSTUM"></span>**截**</span><span class="sxs-lookup"><span data-stu-id="3e836-140"><span id="opengl_frustum"></span><span id="OPENGL_FRUSTUM"></span>**frustum**</span></span>
</dt> <dd>

<span data-ttu-id="3e836-141">依透視圖劃分扭曲的視圖量。</span><span class="sxs-lookup"><span data-stu-id="3e836-141">The view volume warped by perspective division.</span></span>

</dd> </dl>

 

 





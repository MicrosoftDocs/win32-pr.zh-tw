---
title: 'G (OpenGL) '
description: 以字母 G 開頭之 OpenGL 詞彙的定義。
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 588df117-d03c-4a1f-9666-84004cb3d97b
keywords:
- Gamma 修正
- 幾何模型
- 幾何物件
- 幾何基本類型
- Gouraud 網底
- groups
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c369c5c2af949bed221d1afd5fb0c05aebf14849
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "106999809"
---
# <a name="g-opengl"></a><span data-ttu-id="4d3ef-109">G (OpenGL) </span><span class="sxs-lookup"><span data-stu-id="4d3ef-109">G (OpenGL)</span></span>

<span data-ttu-id="4d3ef-110">[](a.md) [B](b.md) [C](c.md) [D](d.md) [E](e.md) [F](f.md) G [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span><span class="sxs-lookup"><span data-stu-id="4d3ef-110">[A](a.md) [B](b.md) [C](c.md) [D](d.md) [E](e.md) [F](f.md) G [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span></span>

<dl> <dt>

<span data-ttu-id="4d3ef-111"><span id="opengl_gamma_correction"></span><span id="OPENGL_GAMMA_CORRECTION"></span>**gamma 修正**</span><span class="sxs-lookup"><span data-stu-id="4d3ef-111"><span id="opengl_gamma_correction"></span><span id="OPENGL_GAMMA_CORRECTION"></span>**gamma correction**</span></span>
</dt> <dd>

<span data-ttu-id="4d3ef-112">一種函式，適用于儲存在框架緩衝區中的色彩，以更正眼睛 (的非線性回應，有時監視器) 色彩濃度值的線性變更。</span><span class="sxs-lookup"><span data-stu-id="4d3ef-112">A function applied to colors stored in the frame buffer to correct for the nonlinear response of the eye (and sometimes of the monitor) to linear changes in color-intensity values.</span></span>

</dd> <dt>

<span data-ttu-id="4d3ef-113"><span id="opengl_geometric_model"></span><span id="OPENGL_GEOMETRIC_MODEL"></span>**幾何模型**</span><span class="sxs-lookup"><span data-stu-id="4d3ef-113"><span id="opengl_geometric_model"></span><span id="OPENGL_GEOMETRIC_MODEL"></span>**geometric model**</span></span>
</dt> <dd>

<span data-ttu-id="4d3ef-114">描述物件的物件座標頂點和參數。</span><span class="sxs-lookup"><span data-stu-id="4d3ef-114">The object-coordinate vertices and parameters that describe an object.</span></span> <span data-ttu-id="4d3ef-115">請注意，OpenGL 不會定義幾何模型的語法，而是用來呈現幾何模型的語法和語義。</span><span class="sxs-lookup"><span data-stu-id="4d3ef-115">Note that OpenGL doesn't define a syntax for geometric models, but rather a syntax and semantics for the rendering of geometric models.</span></span>

</dd> <dt>

<span data-ttu-id="4d3ef-116"><span id="opengl_geometric_object"></span><span id="OPENGL_GEOMETRIC_OBJECT"></span>**幾何物件**</span><span class="sxs-lookup"><span data-stu-id="4d3ef-116"><span id="opengl_geometric_object"></span><span id="OPENGL_GEOMETRIC_OBJECT"></span>**geometric object**</span></span>
</dt> <dd>

<span data-ttu-id="4d3ef-117">幾何模型。</span><span class="sxs-lookup"><span data-stu-id="4d3ef-117">A geometric model.</span></span>

</dd> <dt>

<span data-ttu-id="4d3ef-118"><span id="opengl_geometric_primitive"></span><span id="OPENGL_GEOMETRIC_PRIMITIVE"></span>**幾何基本**</span><span class="sxs-lookup"><span data-stu-id="4d3ef-118"><span id="opengl_geometric_primitive"></span><span id="OPENGL_GEOMETRIC_PRIMITIVE"></span>**geometric primitive**</span></span>
</dt> <dd>

<span data-ttu-id="4d3ef-119">點、線條或多邊形。</span><span class="sxs-lookup"><span data-stu-id="4d3ef-119">A point, line, or polygon.</span></span>

</dd> <dt>

<span data-ttu-id="4d3ef-120"><span id="opengl_gouraud_shading"></span><span id="OPENGL_GOURAUD_SHADING"></span>**Gouraud 網底**</span><span class="sxs-lookup"><span data-stu-id="4d3ef-120"><span id="opengl_gouraud_shading"></span><span id="OPENGL_GOURAUD_SHADING"></span>**Gouraud shading**</span></span>
</dt> <dd>

<span data-ttu-id="4d3ef-121">在多邊形或線段線段之間平滑色彩的插補。</span><span class="sxs-lookup"><span data-stu-id="4d3ef-121">Smooth interpolation of colors across a polygon or line segment.</span></span> <span data-ttu-id="4d3ef-122">色彩會指派于頂點，並以線性方式插入至基本型別，以產生相對較平滑的色彩變化。</span><span class="sxs-lookup"><span data-stu-id="4d3ef-122">Colors are assigned at vertices and linearly interpolated across the primitive to produce a relatively smooth variation in color.</span></span> <span data-ttu-id="4d3ef-123">也稱為平滑陰影。</span><span class="sxs-lookup"><span data-stu-id="4d3ef-123">Also called smooth shading.</span></span>

</dd> <dt>

<span data-ttu-id="4d3ef-124"><span id="opengl_group"></span><span id="OPENGL_GROUP"></span>**組**</span><span class="sxs-lookup"><span data-stu-id="4d3ef-124"><span id="opengl_group"></span><span id="OPENGL_GROUP"></span>**group**</span></span>
</dt> <dd>

<span data-ttu-id="4d3ef-125">一組、二、三或四個元素，代表用戶端記憶體中影像的每個圖元。</span><span class="sxs-lookup"><span data-stu-id="4d3ef-125">A group of one, two, three, or four elements that represents each pixel of an image in client memory.</span></span> <span data-ttu-id="4d3ef-126">因此，在用戶端記憶體映射的內容中，群組和圖元就是相同的東西。</span><span class="sxs-lookup"><span data-stu-id="4d3ef-126">Thus, in the context of a client memory image, a group and a pixel are the same thing.</span></span>

</dd> </dl>

 

 





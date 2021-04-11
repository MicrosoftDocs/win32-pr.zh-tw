---
title: " (OpenGL) "
description: 以字母 A 開頭之 OpenGL 詞彙的定義。
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: e583610f-37da-47bb-bbd6-41d353b88244
keywords:
- 混 疊
- alpha
- 動畫
- 消除鋸齒 (antialiasing)
- 應用程式特定的剪輯
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d161832eb6d81738038e10564233f26920f0d60
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104383702"
---
# <a name="a-opengl"></a><span data-ttu-id="261a9-108"> (OpenGL) </span><span class="sxs-lookup"><span data-stu-id="261a9-108">A (OpenGL)</span></span>

<span data-ttu-id="261a9-109">[B](b.md) [C](c.md) [D](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span><span class="sxs-lookup"><span data-stu-id="261a9-109">A [B](b.md) [C](c.md) [D](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span></span>

<dl> <dt>

<span data-ttu-id="261a9-110"><span id="opengl_aliasing"></span><span id="OPENGL_ALIASING"></span>**混 疊**</span><span class="sxs-lookup"><span data-stu-id="261a9-110"><span id="opengl_aliasing"></span><span id="OPENGL_ALIASING"></span>**aliasing**</span></span>
</dt> <dd>

<span data-ttu-id="261a9-111">轉譯技術，其會將所轉譯之基本型別的色彩指派給圖元，不論該基本型別涵蓋了所有或部分的圖元區域。</span><span class="sxs-lookup"><span data-stu-id="261a9-111">A rendering technique that assigns to pixels the color of the primitive being rendered, whether that primitive covers all or part of the pixel's area.</span></span> <span data-ttu-id="261a9-112">以鋸齒狀邊緣或 jaggies 來產生鋸齒結果。</span><span class="sxs-lookup"><span data-stu-id="261a9-112">Aliasing results in jagged edges, or jaggies.</span></span> <span data-ttu-id="261a9-113">另請參閱 [jaggies](jk.md)。</span><span class="sxs-lookup"><span data-stu-id="261a9-113">See also [jaggies](jk.md).</span></span>

</dd> <dt>

<span data-ttu-id="261a9-114"><span id="opengl_alpha"></span><span id="OPENGL_ALPHA"></span>**阿 爾 法**</span><span class="sxs-lookup"><span data-stu-id="261a9-114"><span id="opengl_alpha"></span><span id="OPENGL_ALPHA"></span>**alpha**</span></span>
</dt> <dd>

<span data-ttu-id="261a9-115">第四個色彩元件通常用來控制色彩混合。</span><span class="sxs-lookup"><span data-stu-id="261a9-115">A fourth color component typically used to control color blending.</span></span> <span data-ttu-id="261a9-116">Alpha 元件永遠不會直接顯示。</span><span class="sxs-lookup"><span data-stu-id="261a9-116">The alpha component is never displayed directly.</span></span> <span data-ttu-id="261a9-117">根據慣例，OpenGL Alpha 表示在0.0 到1.0 的尺規上不透明度和透明度。</span><span class="sxs-lookup"><span data-stu-id="261a9-117">By convention, OpenGL alpha indicates opacity and transparency on a scale of 0.0 to 1.0.</span></span> <span data-ttu-id="261a9-118">1.0 的 Alpha 值表示完全不透明，Alpha 值0.0 表示完整透明度。</span><span class="sxs-lookup"><span data-stu-id="261a9-118">An alpha value of 1.0 implies complete opacity, an alpha value of 0.0 implies complete transparency.</span></span>

</dd> <dt>

<span data-ttu-id="261a9-119"><span id="opengl_animation"></span><span id="OPENGL_ANIMATION"></span>**動畫**</span><span class="sxs-lookup"><span data-stu-id="261a9-119"><span id="opengl_animation"></span><span id="OPENGL_ANIMATION"></span>**animation**</span></span>
</dt> <dd>

<span data-ttu-id="261a9-120">產生重複的場景轉譯，具有順暢變化的觀點或物件位置，可達成運動的假像。</span><span class="sxs-lookup"><span data-stu-id="261a9-120">The generation of repeated renderings of a scene quickly enough, with smoothly changing viewpoint or object positions, that the illusion of motion is achieved.</span></span> <span data-ttu-id="261a9-121">OpenGL 動畫幾乎一律使用雙重緩衝。</span><span class="sxs-lookup"><span data-stu-id="261a9-121">OpenGL animation almost always uses double-buffering.</span></span>

</dd> <dt>

<span data-ttu-id="261a9-122"><span id="opengl_antialiasing"></span><span id="OPENGL_ANTIALIASING"></span>**消除鋸齒**</span><span class="sxs-lookup"><span data-stu-id="261a9-122"><span id="opengl_antialiasing"></span><span id="OPENGL_ANTIALIASING"></span>**antialiasing**</span></span>
</dt> <dd>

<span data-ttu-id="261a9-123">一種轉譯技術，會根據所轉譯之基本區域所涵蓋的圖元區域比例，將色彩指派給圖元。</span><span class="sxs-lookup"><span data-stu-id="261a9-123">A rendering technique that assigns colors to pixels based on the fraction of the pixel area that is covered by the primitive being rendered.</span></span> <span data-ttu-id="261a9-124">反鋸齒轉譯會減少或消除由別名呈現所產生的 jaggies。</span><span class="sxs-lookup"><span data-stu-id="261a9-124">Antialiased rendering reduces or eliminates the jaggies that result from aliased rendering.</span></span> <span data-ttu-id="261a9-125">另請參閱 [jaggies](jk.md)、 [呈現](r.md)。</span><span class="sxs-lookup"><span data-stu-id="261a9-125">See also [jaggies](jk.md), [rendering](r.md).</span></span>

</dd> <dt>

<span data-ttu-id="261a9-126"><span id="opengl_application_specific_clipping"></span><span id="OPENGL_APPLICATION_SPECIFIC_CLIPPING"></span>**應用程式特定的剪輯**</span><span class="sxs-lookup"><span data-stu-id="261a9-126"><span id="opengl_application_specific_clipping"></span><span id="OPENGL_APPLICATION_SPECIFIC_CLIPPING"></span>**application-specific clipping**</span></span> 
</dt> <dd>

<span data-ttu-id="261a9-127">針對眼睛座標中的平面裁剪基本類型。</span><span class="sxs-lookup"><span data-stu-id="261a9-127">Clipping of primitives against planes in eye coordinates.</span></span> <span data-ttu-id="261a9-128">平面是由使用 [**glClipPlane**](glclipplane.md)的應用程式所指定。</span><span class="sxs-lookup"><span data-stu-id="261a9-128">The planes are specified by the application using [**glClipPlane**](glclipplane.md).</span></span> <span data-ttu-id="261a9-129">另請參閱 [眼睛座標](e.md)。</span><span class="sxs-lookup"><span data-stu-id="261a9-129">See also [eye coordinates](e.md).</span></span>

</dd> </dl>

 

 





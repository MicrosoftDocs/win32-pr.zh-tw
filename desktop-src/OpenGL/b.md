---
title: 'B (OpenGL) '
description: 以字母 B 開頭之 OpenGL 詞彙的定義。
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 053fa15a-fbda-43a7-a740-b4477ad9c946
keywords:
- 背景臉部
- 位元
- 點陣圖
- bitplanes
- 混色
- 緩衝區
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5081fa4d1742f2c8dad0a6ef7ef3368135bf0d23
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "103933850"
---
# <a name="b-opengl"></a><span data-ttu-id="266fc-109">B (OpenGL) </span><span class="sxs-lookup"><span data-stu-id="266fc-109">B (OpenGL)</span></span>

<span data-ttu-id="266fc-110">[B](a.md) [C](c.md) [D](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span><span class="sxs-lookup"><span data-stu-id="266fc-110">[A](a.md) B [C](c.md) [D](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span></span>

<dl> <dt>

<span data-ttu-id="266fc-111"><span id="opengl_back_face"></span><span id="OPENGL_BACK_FACE"></span>**背景臉部**</span><span class="sxs-lookup"><span data-stu-id="266fc-111"><span id="opengl_back_face"></span><span id="OPENGL_BACK_FACE"></span>**back face**</span></span>
</dt> <dd>

<span data-ttu-id="266fc-112">請參閱 [臉部](f.md)。</span><span class="sxs-lookup"><span data-stu-id="266fc-112">See [face](f.md).</span></span>

</dd> <dt>

<span data-ttu-id="266fc-113"><span id="opengl_bit"></span><span id="OPENGL_BIT"></span>**位**</span><span class="sxs-lookup"><span data-stu-id="266fc-113"><span id="opengl_bit"></span><span id="OPENGL_BIT"></span>**bit**</span></span>
</dt> <dd>

<span data-ttu-id="266fc-114">二進位位數。</span><span class="sxs-lookup"><span data-stu-id="266fc-114">Binary digit.</span></span> <span data-ttu-id="266fc-115">只有兩個可能值的狀態變數：0或1。</span><span class="sxs-lookup"><span data-stu-id="266fc-115">A state variable that has only two possible values: 0 or 1.</span></span> <span data-ttu-id="266fc-116">二進位數是一或多個位的結構。</span><span class="sxs-lookup"><span data-stu-id="266fc-116">Binary numbers are constructions of one or more bits.</span></span>

</dd> <dt>

<span data-ttu-id="266fc-117"><span id="opengl_bitmap"></span><span id="OPENGL_BITMAP"></span>**點陣圖**</span><span class="sxs-lookup"><span data-stu-id="266fc-117"><span id="opengl_bitmap"></span><span id="OPENGL_BITMAP"></span>**bitmap**</span></span>
</dt> <dd>

<span data-ttu-id="266fc-118">位的矩形陣列。</span><span class="sxs-lookup"><span data-stu-id="266fc-118">A rectangular array of bits.</span></span> <span data-ttu-id="266fc-119">此外， [**glBitmap**](glbitmap.md) 命令所呈現的基本類型，會使用其 bitmap 參數做為遮罩。</span><span class="sxs-lookup"><span data-stu-id="266fc-119">Also, the primitive rendered by the [**glBitmap**](glbitmap.md) command, which uses its bitmap parameter as a mask.</span></span>

</dd> <dt>

<span data-ttu-id="266fc-120"><span id="opengl_bitplane"></span><span id="OPENGL_BITPLANE"></span>**bitplane**</span><span class="sxs-lookup"><span data-stu-id="266fc-120"><span id="opengl_bitplane"></span><span id="OPENGL_BITPLANE"></span>**bitplane**</span></span>
</dt> <dd>

<span data-ttu-id="266fc-121">以圖元為單位對應的位矩形陣列。</span><span class="sxs-lookup"><span data-stu-id="266fc-121">A rectangular array of bits mapped one-to-one with pixels.</span></span>

</dd> <dt>

<span data-ttu-id="266fc-122"><span id="opengl_blending"></span><span id="OPENGL_BLENDING"></span>**混合**</span><span class="sxs-lookup"><span data-stu-id="266fc-122"><span id="opengl_blending"></span><span id="OPENGL_BLENDING"></span>**blending**</span></span>
</dt> <dd>

<span data-ttu-id="266fc-123">將兩個色彩元件減少為一個元件，通常是兩個元件之間的線性插補。</span><span class="sxs-lookup"><span data-stu-id="266fc-123">Reducing two color components to one component, usually as a linear interpolation between the two components.</span></span>

</dd> <dt>

<span data-ttu-id="266fc-124"><span id="opengl_buffer"></span><span id="OPENGL_BUFFER"></span>**緩衝區**</span><span class="sxs-lookup"><span data-stu-id="266fc-124"><span id="opengl_buffer"></span><span id="OPENGL_BUFFER"></span>**buffer**</span></span>
</dt> <dd>

<span data-ttu-id="266fc-125">一組 bitplanes，用來儲存單一元件 (例如深度或綠色) 或單一索引 (例如色彩索引或樣板索引) 。</span><span class="sxs-lookup"><span data-stu-id="266fc-125">A group of bitplanes that stores a single component (such as depth or green) or a single index (such as the color index or the stencil index).</span></span> <span data-ttu-id="266fc-126">有時會將紅色、綠色、藍色和 Alpha 緩衝區統稱為色彩緩衝區 (而不是色彩緩衝區) 。</span><span class="sxs-lookup"><span data-stu-id="266fc-126">Sometimes the red, green, blue, and alpha buffers are referred to collectively as the color buffer (rather than as the color buffers).</span></span>

</dd> </dl>

 

 





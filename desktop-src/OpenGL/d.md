---
title: 'D (OpenGL) '
description: 以字母 D 開頭之 OpenGL 詞彙的定義。
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: f97470e7-a500-47d7-84f0-b3045d04b8fc
keywords:
- depth
- 深度提示
- 顯示清單
- 抖動
- 雙重緩衝
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97cb068f06135c6ba29e8a61f472d98907090a78
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "103685407"
---
# <a name="d-opengl"></a><span data-ttu-id="1703f-108">D (OpenGL) </span><span class="sxs-lookup"><span data-stu-id="1703f-108">D (OpenGL)</span></span>

<span data-ttu-id="1703f-109">[](a.md) [B](b.md) [C](c.md) D [E](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span><span class="sxs-lookup"><span data-stu-id="1703f-109">[A](a.md) [B](b.md) [C](c.md) D [E](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span></span>

<dl> <dt>

<span data-ttu-id="1703f-110"><span id="opengl_depth"></span><span id="OPENGL_DEPTH"></span>**深度**</span><span class="sxs-lookup"><span data-stu-id="1703f-110"><span id="opengl_depth"></span><span id="OPENGL_DEPTH"></span>**depth**</span></span>
</dt> <dd>

<span data-ttu-id="1703f-111">通常是指 z 視窗座標。</span><span class="sxs-lookup"><span data-stu-id="1703f-111">Generally refers to the z window coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="1703f-112"><span id="opengl_depth_cueing"></span><span id="OPENGL_DEPTH_CUEING"></span>**深度提示**</span><span class="sxs-lookup"><span data-stu-id="1703f-112"><span id="opengl_depth_cueing"></span><span id="OPENGL_DEPTH_CUEING"></span>**depth cueing**</span></span>
</dt> <dd>

<span data-ttu-id="1703f-113">一種轉譯技術，可根據視點的距離指派色彩。</span><span class="sxs-lookup"><span data-stu-id="1703f-113">A rendering technique that assigns color based on distance from the viewpoint.</span></span>

</dd> <dt>

<span data-ttu-id="1703f-114"><span id="opengl_display_list"></span><span id="OPENGL_DISPLAY_LIST"></span>**顯示清單**</span><span class="sxs-lookup"><span data-stu-id="1703f-114"><span id="opengl_display_list"></span><span id="OPENGL_DISPLAY_LIST"></span>**display list**</span></span>
</dt> <dd>

<span data-ttu-id="1703f-115">OpenGL 命令的名稱清單。</span><span class="sxs-lookup"><span data-stu-id="1703f-115">A named list of OpenGL commands.</span></span> <span data-ttu-id="1703f-116">顯示清單一律儲存在伺服器上，因此可以使用顯示清單來減少用戶端/伺服器環境中的網路流量。</span><span class="sxs-lookup"><span data-stu-id="1703f-116">Display lists are always stored on the server, so display lists can be used to reduce the network traffic in client/server environments.</span></span> <span data-ttu-id="1703f-117">顯示清單的內容可以預先處理，因此可能會比在立即模式中執行的一組相同的 OpenGL 命令更有效率地執行。</span><span class="sxs-lookup"><span data-stu-id="1703f-117">The contents of a display list may be preprocessed, and might therefore execute more efficiently than the same set of OpenGL commands executed in immediate mode.</span></span> <span data-ttu-id="1703f-118">這類前置處理對於計算密集的命令（例如 [**glTexImage**](glteximage1d.md)）特別重要。</span><span class="sxs-lookup"><span data-stu-id="1703f-118">Such preprocessing is especially important for computing intensive commands such as [**glTexImage**](glteximage1d.md).</span></span>

</dd> <dt>

<span data-ttu-id="1703f-119"><span id="opengl_dithering"></span><span id="OPENGL_DITHERING"></span>**抖動**</span><span class="sxs-lookup"><span data-stu-id="1703f-119"><span id="opengl_dithering"></span><span id="OPENGL_DITHERING"></span>**dithering**</span></span>
</dt> <dd>

<span data-ttu-id="1703f-120">以空間解析度的成本來增加影像中可見色彩範圍的技巧。</span><span class="sxs-lookup"><span data-stu-id="1703f-120">A technique for increasing the perceived range of colors in an image at the cost of spatial resolution.</span></span> <span data-ttu-id="1703f-121">連續的圖元會被指派不同的色彩值。</span><span class="sxs-lookup"><span data-stu-id="1703f-121">Adjacent pixels are assigned differing color values.</span></span> <span data-ttu-id="1703f-122">從距離觀看時，這些色彩看似 blend 成單一的中繼色彩。</span><span class="sxs-lookup"><span data-stu-id="1703f-122">When viewed from a distance, these colors seem to blend into a single intermediate color.</span></span> <span data-ttu-id="1703f-123">這項技術類似于黑色和白色出版物中使用的半色調，以達成灰色陰影。</span><span class="sxs-lookup"><span data-stu-id="1703f-123">The technique is similar to the half-toning used in black-and-white publications to achieve shades of gray.</span></span>

</dd> <dt>

<span data-ttu-id="1703f-124"><span id="opengl_double_buffering"></span><span id="OPENGL_DOUBLE_BUFFERING"></span>**雙重緩衝**</span><span class="sxs-lookup"><span data-stu-id="1703f-124"><span id="opengl_double_buffering"></span><span id="OPENGL_DOUBLE_BUFFERING"></span>**double buffering**</span></span>
</dt> <dd>

<span data-ttu-id="1703f-125">使用 OpenGL 內容，在這兩種情況中，前端和後端色彩緩衝區都會進行雙重緩衝處理。</span><span class="sxs-lookup"><span data-stu-id="1703f-125">Using OpenGL contexts in which both front and back color buffers are double-buffered.</span></span> <span data-ttu-id="1703f-126">平滑動畫的完成方式是只轉譯回背景緩衝區 (不會顯示) ，然後使前端和後端緩衝區交換。</span><span class="sxs-lookup"><span data-stu-id="1703f-126">Smooth animation is accomplished by rendering into only the back buffer (which isn't displayed), then causing the front and back buffers to be swapped.</span></span>

</dd> </dl>

 

 





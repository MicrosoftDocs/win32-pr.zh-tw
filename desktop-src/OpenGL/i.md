---
title: '我 (OpenGL) '
description: 以字母 I 開頭的 OpenGL 詞彙定義。
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 2c78efce-9aed-4bcd-a254-7bff053b0acd
keywords:
- images
- 影像基本專案
- 立即模式
- 索引
- 鳶尾花 GL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fe340cfbd7dbef3d93cc68ba310d863717225c0
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104508232"
---
# <a name="i-opengl"></a><span data-ttu-id="7719e-108">我 (OpenGL) </span><span class="sxs-lookup"><span data-stu-id="7719e-108">I (OpenGL)</span></span>

<span data-ttu-id="7719e-109">[](a.md) [B](b.md) [C](c.md) [D](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) I [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span><span class="sxs-lookup"><span data-stu-id="7719e-109">[A](a.md) [B](b.md) [C](c.md) [D](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) I [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span></span>

<dl> <dt>

<span data-ttu-id="7719e-110"><span id="opengl_image"></span><span id="OPENGL_IMAGE"></span>**圖像**</span><span class="sxs-lookup"><span data-stu-id="7719e-110"><span id="opengl_image"></span><span id="OPENGL_IMAGE"></span>**image**</span></span>
</dt> <dd>

<span data-ttu-id="7719e-111">在用戶端記憶體或畫面格緩衝區中的矩形陣列（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="7719e-111">A rectangular array of pixels, either in client memory or in the framebuffer.</span></span>

</dd> <dt>

<span data-ttu-id="7719e-112"><span id="opengl_image_primitive"></span><span id="OPENGL_IMAGE_PRIMITIVE"></span>**影像基本**</span><span class="sxs-lookup"><span data-stu-id="7719e-112"><span id="opengl_image_primitive"></span><span id="OPENGL_IMAGE_PRIMITIVE"></span>**image primitive**</span></span> 
</dt> <dd>

<span data-ttu-id="7719e-113">點陣圖或影像。</span><span class="sxs-lookup"><span data-stu-id="7719e-113">A bitmap or an image.</span></span>

</dd> <dt>

<span data-ttu-id="7719e-114"><span id="opengl_immediate_mode"></span><span id="OPENGL_IMMEDIATE_MODE"></span>**立即模式**</span><span class="sxs-lookup"><span data-stu-id="7719e-114"><span id="opengl_immediate_mode"></span><span id="OPENGL_IMMEDIATE_MODE"></span>**immediate mode**</span></span>
</dt> <dd>

<span data-ttu-id="7719e-115">直接呼叫 OpenGL 命令的模式，而不是從顯示清單。</span><span class="sxs-lookup"><span data-stu-id="7719e-115">Mode in which an OpenGL command is called directly, rather than from a display list.</span></span> <span data-ttu-id="7719e-116">沒有立即模式位存在;立即模式中的模式指的是 OpenGL 的使用方式，而不是特定的 OpenGL 狀態位。</span><span class="sxs-lookup"><span data-stu-id="7719e-116">No immediate-mode bit exists; the mode in immediate mode refers to usage of OpenGL, rather than to a specific bit of OpenGL state.</span></span>

</dd> <dt>

<span data-ttu-id="7719e-117"><span id="opengl_index"></span><span id="OPENGL_INDEX"></span>**指數**</span><span class="sxs-lookup"><span data-stu-id="7719e-117"><span id="opengl_index"></span><span id="OPENGL_INDEX"></span>**index**</span></span>
</dt> <dd>

<span data-ttu-id="7719e-118">轉譯為絕對值的單一值，而不是指定範圍內的正規化值 (為元件) 。</span><span class="sxs-lookup"><span data-stu-id="7719e-118">A single value that is interpreted as an absolute value, rather than as a normalized value in a specified range (as is a component).</span></span> <span data-ttu-id="7719e-119">色彩索引是色彩的名稱，可使用色彩對應以顯示硬體進行取值。</span><span class="sxs-lookup"><span data-stu-id="7719e-119">Color indexes are the names of colors, which are dereferenced by the display hardware using the color map.</span></span> <span data-ttu-id="7719e-120">索引通常會在超出範圍時進行遮罩，而不是壓制。</span><span class="sxs-lookup"><span data-stu-id="7719e-120">Indexes are typically masked, rather than clamped, when out of range.</span></span> <span data-ttu-id="7719e-121">例如，將索引0xf7 寫入至4位緩衝區時，會將索引遮罩至0x7， (色彩或樣板) 。</span><span class="sxs-lookup"><span data-stu-id="7719e-121">For example, the index 0xf7 is masked to 0x7 when written to a 4-bit buffer (color or stencil).</span></span> <span data-ttu-id="7719e-122">色彩索引和樣板索引一律會被視為索引，而不是元件。</span><span class="sxs-lookup"><span data-stu-id="7719e-122">Color indexes and stencil indexes are always treated as indexes, never as components.</span></span>

</dd> <dt>

<span data-ttu-id="7719e-123"><span id="opengl_iris_gl"></span><span id="OPENGL_IRIS_GL"></span>**鳶尾花 GL**</span><span class="sxs-lookup"><span data-stu-id="7719e-123"><span id="opengl_iris_gl"></span><span id="OPENGL_IRIS_GL"></span>**IRIS GL**</span></span>
</dt> <dd>

<span data-ttu-id="7719e-124">晶片圖形專屬圖形程式庫，從1982到1992開發。</span><span class="sxs-lookup"><span data-stu-id="7719e-124">Silicon Graphics' proprietary graphics library, developed from 1982 through 1992.</span></span> <span data-ttu-id="7719e-125">OpenGL 的設計是以鳶尾花 GL 作為起點。</span><span class="sxs-lookup"><span data-stu-id="7719e-125">OpenGL was designed with IRIS GL as a starting point.</span></span>

</dd> </dl>

 

 





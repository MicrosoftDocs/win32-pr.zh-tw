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
# <a name="f-opengl"></a>F (OpenGL) 

[](a.md) [B](b.md) [C](c.md) [D](d.md) [E](e.md) F [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [](u-v.md) [W](w.md) [X Y Z](x-y-z.md)

<dl> <dt>

<span id="opengl_face"></span><span id="OPENGL_FACE"></span>**臉**
</dt> <dd>

多邊形的一端。 每個多邊形都有兩個臉部：正面臉部和背面表面。 視窗中只會顯示一張臉部。 當多邊形投射到視窗之後，是否可以看到背面或正面臉部。 在此投射之後，如果多邊形的邊緣有順向方向，則會顯示其中一個臉部;如果有逆時針方向，則會顯示另一個臉部。 無論是否以順向的方式對應至 front 或 back (，以及逆時針對應至 back 或 front) 是由 OpenGL 程式設計師所決定。

</dd> <dt>

<span id="opengl_flat_shading"></span><span id="OPENGL_FLAT_SHADING"></span>**平面網底**
</dt> <dd>

是指將具有單一、常數色彩的基本色彩著色，而不是在基本的範圍內順暢地插上色彩。 請參閱 [Gouraud 網底](g.md)。

</dd> <dt>

<span id="opengl_fog"></span><span id="OPENGL_FOG"></span>**霧**
</dt> <dd>

一種轉譯技術，可用來模擬迷霧、霧化和廢氣檢測等大氣效果，方法是根據檢視器的距離，將物件色彩淡化為背景色彩。 霧化也有助於查看檢視器距離，並提供深度提示。 另請參閱 [深度-提示](d.md)。

</dd> <dt>

<span id="opengl_font"></span><span id="OPENGL_FONT"></span>**字體**
</dt> <dd>

一組圖形字元表示通常用來顯示文字字串。 這些字元可以是羅馬字母、數學符號、亞洲表意文字、埃及 hieroglyphs 等等。

</dd> <dt>

<span id="opengl_fragment"></span><span id="OPENGL_FRAGMENT"></span>**片段**
</dt> <dd>

由基本圖形所產生的圖形資料。 每個片段都對應至單一圖元，並且包含色彩、深度，以及有時材質座標值。

</dd> <dt>

<span id="opengl_framebuffer"></span><span id="OPENGL_FRAMEBUFFER"></span>**畫面格緩衝區**
</dt> <dd>

Bitplanes 的堆疊。 給定視窗或內容的所有緩衝區。 有時會包含圖形硬體加速器的所有圖元記憶體。 另請參閱 [bitplane](b.md)。

</dd> <dt>

<span id="opengl_front_face"></span><span id="OPENGL_FRONT_FACE"></span>**正面臉部**
</dt> <dd>

請參閱臉部。

</dd> <dt>

<span id="opengl_frustum"></span><span id="OPENGL_FRUSTUM"></span>**截**
</dt> <dd>

依透視圖劃分扭曲的視圖量。

</dd> </dl>

 

 





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
ms.openlocfilehash: 213fd30866deeaacec6408752424444190801164a3f15de2417fbd308f3beb6b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118936389"
---
# <a name="p-opengl"></a>P (OpenGL) 

[](a.md) [B](b.md) [C](c.md) [D](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) P [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [](u-v.md) [W](w.md) [X Y Z](x-y-z.md)

<dl> <dt>

<span id="opengl_parameter"></span><span id="OPENGL_PARAMETER"></span>**參數**
</dt> <dd>

以引數形式傳遞至 OpenGL 命令的值。 有時會以傳址方式傳遞至 OpenGL 命令的其中一個值。

</dd> <dt>

<span id="opengl_perspective_division"></span><span id="OPENGL_PERSPECTIVE_DIVISION"></span>**透視圖部門**
</dt> <dd>

X、y 和 z 的除以 w，會在剪切座標中執行。 另請參閱 [裁剪座標](c.md)。

</dd> <dt>

<span id="opengl_pixel"></span><span id="OPENGL_PIXEL"></span>**圖元**
</dt> <dd>

圖片元素。 在畫面格緩衝區中所有 bitplanes 的位置 (x，y) 的位會構成單一圖元 (x，y) 。 在用戶端記憶體的影像中，圖元是一個元素群組。 在 OpenGL 視窗座標中，每個圖元都會對應到 1.0 x 1.0 的螢幕區域。 圖元名稱 x、y 的左下角座標為 (x、y) ，而右上角 (x + 1、y + 1) 。

</dd> <dt>

<span id="opengl_point"></span><span id="OPENGL_POINT"></span>**點**
</dt> <dd>

空間中的確切位置，會轉譯為有限的直徑點。

</dd> <dt>

<span id="opengl_polygon"></span><span id="OPENGL_POLYGON"></span>**多邊形**
</dt> <dd>

由頂點指定的邊緣周圍的平面介面。 三角形網格的每個三角形都是多邊形，如同四邊形網格的每個四邊形。 GlRect 所指定的矩形也是多邊形。

</dd> <dt>

<span id="opengl_primitive"></span><span id="OPENGL_PRIMITIVE"></span>**原始**
</dt> <dd>

圖形 (例如點、線條、多邊形、點陣圖或影像) ，可繪製、儲存和操作為離散實體;建立大型圖形設計的元素。

</dd> <dt>

<span id="opengl_projection_matrix"></span><span id="OPENGL_PROJECTION_MATRIX"></span>**投射矩陣**
</dt> <dd>

4x4 矩陣，會將點、線條、多邊形和點陣位置從眼睛座標轉換成剪切座標。

</dd> </dl>

 

 





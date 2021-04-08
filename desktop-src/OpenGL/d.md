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
# <a name="d-opengl"></a>D (OpenGL) 

[](a.md) [B](b.md) [C](c.md) D [E](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [](u-v.md) [W](w.md) [X Y Z](x-y-z.md)

<dl> <dt>

<span id="opengl_depth"></span><span id="OPENGL_DEPTH"></span>**深度**
</dt> <dd>

通常是指 z 視窗座標。

</dd> <dt>

<span id="opengl_depth_cueing"></span><span id="OPENGL_DEPTH_CUEING"></span>**深度提示**
</dt> <dd>

一種轉譯技術，可根據視點的距離指派色彩。

</dd> <dt>

<span id="opengl_display_list"></span><span id="OPENGL_DISPLAY_LIST"></span>**顯示清單**
</dt> <dd>

OpenGL 命令的名稱清單。 顯示清單一律儲存在伺服器上，因此可以使用顯示清單來減少用戶端/伺服器環境中的網路流量。 顯示清單的內容可以預先處理，因此可能會比在立即模式中執行的一組相同的 OpenGL 命令更有效率地執行。 這類前置處理對於計算密集的命令（例如 [**glTexImage**](glteximage1d.md)）特別重要。

</dd> <dt>

<span id="opengl_dithering"></span><span id="OPENGL_DITHERING"></span>**抖動**
</dt> <dd>

以空間解析度的成本來增加影像中可見色彩範圍的技巧。 連續的圖元會被指派不同的色彩值。 從距離觀看時，這些色彩看似 blend 成單一的中繼色彩。 這項技術類似于黑色和白色出版物中使用的半色調，以達成灰色陰影。

</dd> <dt>

<span id="opengl_double_buffering"></span><span id="OPENGL_DOUBLE_BUFFERING"></span>**雙重緩衝**
</dt> <dd>

使用 OpenGL 內容，在這兩種情況中，前端和後端色彩緩衝區都會進行雙重緩衝處理。 平滑動畫的完成方式是只轉譯回背景緩衝區 (不會顯示) ，然後使前端和後端緩衝區交換。

</dd> </dl>

 

 





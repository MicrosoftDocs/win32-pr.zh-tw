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
ms.openlocfilehash: bb69307f869031bb9fd176ec85dd20eac5d543ef3e7f63086c6ea0801d1b8b8a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128368"
---
# <a name="a-opengl"></a> (OpenGL) 

[B](b.md) [C](c.md) [D](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [](u-v.md) [W](w.md) [X Y Z](x-y-z.md)

<dl> <dt>

<span id="opengl_aliasing"></span><span id="OPENGL_ALIASING"></span>**混 疊**
</dt> <dd>

轉譯技術，其會將所轉譯之基本型別的色彩指派給圖元，不論該基本型別涵蓋了所有或部分的圖元區域。 以鋸齒狀邊緣或 jaggies 來產生鋸齒結果。 另請參閱 [jaggies](jk.md)。

</dd> <dt>

<span id="opengl_alpha"></span><span id="OPENGL_ALPHA"></span>**阿 爾 法**
</dt> <dd>

第四個色彩元件通常用來控制色彩混合。 Alpha 元件永遠不會直接顯示。 根據慣例，OpenGL Alpha 表示在0.0 到1.0 的尺規上不透明度和透明度。 1.0 的 Alpha 值表示完全不透明，Alpha 值0.0 表示完整透明度。

</dd> <dt>

<span id="opengl_animation"></span><span id="OPENGL_ANIMATION"></span>**動畫**
</dt> <dd>

產生重複的場景轉譯，具有順暢變化的觀點或物件位置，可達成運動的假像。 OpenGL 動畫幾乎一律使用雙重緩衝。

</dd> <dt>

<span id="opengl_antialiasing"></span><span id="OPENGL_ANTIALIASING"></span>**消除鋸齒**
</dt> <dd>

一種轉譯技術，會根據所轉譯之基本區域所涵蓋的圖元區域比例，將色彩指派給圖元。 反鋸齒轉譯會減少或消除由別名呈現所產生的 jaggies。 另請參閱 [jaggies](jk.md)、 [呈現](r.md)。

</dd> <dt>

<span id="opengl_application_specific_clipping"></span><span id="OPENGL_APPLICATION_SPECIFIC_CLIPPING"></span>**應用程式特定的剪輯** 
</dt> <dd>

針對眼睛座標中的平面裁剪基本類型。 平面是由使用 [**glClipPlane**](glclipplane.md)的應用程式所指定。 另請參閱 [眼睛座標](e.md)。

</dd> </dl>

 

 





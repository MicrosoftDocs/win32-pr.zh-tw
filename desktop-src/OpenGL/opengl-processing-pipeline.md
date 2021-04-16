---
title: OpenGL 處理管線
description: OpenGL 處理管線
ms.assetid: 98ac89d1-0d7b-45b2-8d6e-c421b9289d60
keywords:
- OpenGL，處理管線
- 處理管線 OpenGL
- 管線 OpenGL
- framebuffers，處理管線
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73d67447066b9d397bbb272932f51c6d3003f11e
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "104563406"
---
# <a name="opengl-processing-pipeline"></a>OpenGL 處理管線

許多 OpenGL 函數專門用來繪製物件，例如點、線條、多邊形和點陣圖。 某些函式控制這種繪圖的發生方式 (例如啟用消除鋸齒或紋理) 的方式。 其他函式特別關心畫面格緩衝區操作。 本節中的主題描述所有 OpenGL 函數如何一起運作，以建立 OpenGL 處理管線。 本節也會進一步探討實際處理資料的階段，並將這些階段系結至 OpenGL 函數。

下圖詳細說明 OpenGL 處理管線。 針對大部分的管線，您可以看到主要階段之間的三個垂直箭號。 這些箭號代表頂點，以及可以與頂點相關聯的兩個主要資料類型：色彩值和材質座標。 另請注意，頂點會組合成基本專案，然後放入片段，最後變成畫面格緩衝區中的圖元。 這項進展會在 [頂點](vertices.md)、 [基本](primitives.md)、 [片段](fragments.md)和 [圖元](pixels.md)中更詳細地討論。

![顯示 OpenGL 處理管線的圖表。](images/proc01.png)

 

 





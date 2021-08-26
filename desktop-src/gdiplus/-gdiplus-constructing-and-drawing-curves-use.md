---
description: GDI+ 支援數種曲線類型：橢圓形、弧形、基本曲線和 B&\# 233; zier 曲線。
ms.assetid: 97a1342c-4edb-4671-b36d-b6992efad498
title: 建構和繪製曲線
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b78ebd7ce81099d5b7f483939c0f4b238d1f124357bf6e1863b25fedb7e22f4c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015218"
---
# <a name="constructing-and-drawing-curves"></a>建構和繪製曲線

GDI+ 支援數種曲線類型：橢圓形、弧形、基本曲線和貝茲曲線。 橢圓形是由其周框所定義;弧形是由起始角度和清除角度所定義之橢圓形的一部分。 基本曲線是由點陣列和張力參數所定義—曲線會順暢地流經陣列中的每個點，而張力參數則會影響曲線的彎曲方式。 貝茲曲線是由兩個端點和兩個控制點所定義—曲線不會通過控制點，但是控制點會影響方向和折彎，因為曲線會從某個端點移至另一個端點。

下列主題會更詳細地討論基本曲線和貝茲曲線：

-   [繪製基本曲線](-gdiplus-drawing-cardinal-splines-use.md)
-   [繪圖貝茲曲線](-gdiplus-drawing-bezier-splines-use.md)

 

 




---
title: OpenGL 狀態變數
description: 下列主題列出可查詢的狀態變數名稱
ms.assetid: f4bc4ec1-a529-4b9e-84af-94caa0ef7131
keywords:
- OpenGL 狀態變數
- 狀態變數，OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36dee51ba7726277832d94eaf336d03d3c579189
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106965370"
---
# <a name="opengl-state-variables"></a>OpenGL 狀態變數

下列主題列出可查詢的狀態變數名稱：

-   [**目前值和相關資料的狀態變數**](state-variables-for-current-values-and-associated-data.md)
-   [**轉換狀態變數**](transformation-state-variables.md)
-   [**著色狀態變數**](coloring-state-variables.md)
-   [**光源狀態變數**](lighting-state-variables.md)
-   [**柵格化狀態變數**](rasterization-state-variables.md)
-   [**紋理狀態變數**](texturing-state-variables.md)
-   [**圖元作業**](pixel-operations.md)
-   [**畫面格緩衝區控制項狀態變數**](framebuffer-control-state-variables.md)
-   [**圖元狀態變數**](pixel-state-variables.md)
-   [**評估工具狀態變數**](evaluator-state-variables.md)
-   [**提示狀態變數**](hint-state-variables.md)
-   [**實作為相依狀態變數**](implementation-dependent-state-variables.md)
-   [**與執行相依的 Pixel-Depth 狀態變數**](implementation-dependent-pixel-depth-state-variables.md)
-   [**其他狀態變數**](miscellaneous-state-variables.md)

針對每個變數，此主題會列出描述、屬性群組、初始或最小值，以及建議用來取得它的 [**glGet \***](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)函數。

您可以使用 [**glGetBooleanv**](glgetbooleanv.md)、 [**glGetIntegerv**](glgetintegerv.md)、 [**glGetFloatv**](glgetfloatv.md)或 [**glGetDoublev**](glgetdoublev.md) 取得的狀態變數，只會列出其中一個 functionsthe，最適合傳回的資料類型。 您無法使用 [**glIsEnabled**](glisenabled.md)取得這些狀態變數。 不過，您可以使用 **glGetBooleanv**、 **glGetIntegerv**、 **glGetFloatv** 和 **glGetDoublev** 取得 **glIsEnabled** 列為查詢函數的狀態變數。 您可以使用該函式，取得任何其他函式僅列為查詢函數的狀態變數。 如果未列出任何屬性群組，則變數不屬於任何群組。 您可以查詢的所有狀態變數（除了執行相依的狀態變數）都有初始值。 若要判斷未列出任何初始值之變數的初始值，請參閱該變數的參考或

*OpenGL 參考手冊*。

 

 





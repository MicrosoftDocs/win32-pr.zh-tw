---
title: 使用 NURBS 曲線和表面
description: 非統一的有理 B 曲線 (NURBS) 函數提供兩個和三個維度中曲線和表面的一般和強大描述，並將曲線和曲面轉換為 OpenGL 評估工具。
ms.assetid: 0b55659d-9fa2-47fc-ae15-0c296bd94dcb
keywords:
- 'OpenGL 公用程式 (X.GLU 隊) 、非統一的有理 B 曲線 (NURBS) '
- 'X.GLU 隊 (OpenGL 公用程式) 、非統一的有理 B 曲線 (NURBS) '
- 非統一的有理 B 曲線 (NURBS) OpenGL
- NURBS (非統一有理數 B 曲線) OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c1b366571be7a9210576e78540c77970667aca2f37ec8a092de07edb97493d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118932768"
---
# <a name="using-nurbs-curves-and-surfaces"></a>使用 NURBS 曲線和表面

非統一的有理 B 曲線 (NURBS) 函數提供兩個和三個維度中曲線和表面的一般和強大描述，並將曲線和曲面轉換為 OpenGL 評估工具。 NURBS 函數可以表示許多電腦輔助機械設計系統中的幾何。 它們可以在各種不同的樣式中轉譯曲線和表面，並可自動處理將 tessellates 至較高曲率區域中較小三角形和接近側面裝訂邊的自我調整細分。 NURBS 函數分為下列類別。

若要管理 NURBS 物件，請使用：

-   [**gluNewNurbsRenderer**](glunewnurbsrenderer.md) (建立 NURBS 物件) 
-   [**gluDeleteNurbsRenderer**](gludeletenurbsrenderer.md) (會刪除 NURBS 物件) 
-   [*gluNurbsCallback*](glunurbs.md) (會建立錯誤處理函式) 

若要指定所需的曲線，請使用：

-   [**gluBeginCurve**](glubegincurve.md)
-   [**gluNurbsCurve**](glunurbscurve.md)
-   [**gluEndCurve**](gluendcurve.md)

若要指定所需的表面，請使用：

-   [**gluBeginSurface**](glubeginsurface.md)
-   [**gluNurbsSurface**](glunurbssurface.md)
-   [**gluEndSurface**](gluendsurface.md)

您也可以指定修剪區域，此區域會定義要評估之 NURBS 介面網域的子集，如此您就可以建立具有平滑界限或包含孔洞的表面。

若要指定修剪區域，請使用：

-   [**gluBeginTrim**](glubegintrim.md)
-   [**gluPwlCurve**](glupwlcurve.md)
-   [**gluNurbsCurve**](glunurbscurve.md)
-   [**gluEndTrim**](gluendtrim.md)

如同 quadric 物件，您可以控制如何轉譯的 NURBS 曲線和表面。 您可以判斷：

-   是否要捨棄其控制項多面體位於目前視窗之外的曲線或表面。
-   用來呈現曲線和表面的多邊形邊緣的最大長度 (以圖元為單位) 。
-   您是否將採用 OpenGL 伺服器的投射矩陣、模型矩陣和視口，或提供它們明確與 [**gluLoadSamplingMatrices**](gluloadsamplingmatrices.md)。

使用 [**gluNurbsProperty**](glunurbsproperty.md) 來設定這些屬性，或使用預設值。 您可以使用 [**gluGetNurbsProperty**](glugetnurbsproperty.md)查詢其轉譯樣式的 NURBS 物件。

 

 





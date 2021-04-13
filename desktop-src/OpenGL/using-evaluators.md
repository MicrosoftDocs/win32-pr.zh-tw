---
title: 使用評估工具
description: 使用評估工具
ms.assetid: a5a99d0a-526e-4492-90c4-a6b9fdbdff16
keywords:
- OpenGL，評估工具
- 評估 OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1aef70a7a854e16cf4992d9dd44c4931ad4d044
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300480"
---
# <a name="using-evaluators"></a>使用評估工具

OpenGL 評估工具函數可讓您使用多項式對應來產生頂點、法線、材質座標和色彩。 這些匯出值接著會傳遞至處理管線，就如同直接指定它們一樣。 評估工具函式也是 NURBS (非統一的有理 B 曲線) 函式的基礎，可讓您定義曲線和表面，如 [OpenGL 公用程式程式庫](opengl-utility-library.md)中所述。

使用評估工具的第一個步驟是使用 [**glMap \***](glmap1.md)定義適當的一或兩個維度多項式對應。 然後，您可以透過下列兩種方式之一來指定和評估此對應的定義域值：

-   定義要使用 [**glMapGrid**](glmapgrid-functions.md) 對應的一系列平均間距定義域值，然後使用 [**glEvalMesh**](glevalmesh-functions.md)來評估該方格的矩形子集。 您可以使用 [**glEvalPoint**](glevalpoint.md)來評估方格的單一點。
-   明確指定所需的定義域值做為引數，以在該值上評估對應。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[評估工具參考](evaluators-reference.md)
</dt> </dl>

 

 





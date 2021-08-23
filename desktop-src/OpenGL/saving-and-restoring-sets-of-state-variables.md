---
title: 儲存和還原狀態變數集
description: 您可以使用 glPushAttrib 和 glPopAttrib 函數來儲存和還原屬性堆疊上的狀態變數集合值。
ms.assetid: 339de633-4158-4907-b985-2d75b465fb2a
keywords:
- OpenGL 狀態變數
- 儲存狀態變數 OpenGL
- 還原狀態變數 OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 197a05d80e72479aecdade3323899464bf0b1f4afa2d9f2a8a1a1add6e56db78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119553808"
---
# <a name="saving-and-restoring-sets-of-state-variables"></a>儲存和還原狀態變數集

您可以使用 [**glPushAttrib**](glpushattrib.md) 和 [**glPopAttrib**](glpopattrib.md) 函數來儲存和還原屬性堆疊上的狀態變數集合值。 屬性堆疊的深度至少為16。 若要取得實際的深度，請使用 GL \_ MAX \_ ATTRIB \_ STACK \_ depth with [**glGetIntegerv**](glgetintegerv.md)。 推送完整堆疊或快顯空的堆疊會產生錯誤。

使用 **glPushAttrib** 和 **glPopAttrib** 的速度通常會比自行取得和還原值更快。 某些值可能會在硬體中推送和快顯，並儲存和還原這些值可能需要大量資源。 此外，如果您是在遠端用戶端上操作，則所有屬性資料都必須透過網路連線傳輸，並在儲存和還原時回復。 不過，您的 OpenGL 執行會將屬性堆疊保留在伺服器上，以避免不必要的網路延遲。

**GlPushAttrib** 的原型是：

**void** **glPushAttrib** (**GLbitfield** *mask* ) ;

使用 [**glPushAttrib**](glpushattrib.md) 會將位指定的所有屬性（attribute）推送至屬性堆疊，以儲存 *遮罩* 中的所有屬性。 如需您可以邏輯或一起儲存任何屬性組合的可能遮罩位清單，請參閱 [屬性群組](attribute-groups.md)。 每個位都對應到個別狀態變數的集合。 例如，GL \_ 照明 \_ 位指的是與光源相關的所有狀態變數，包括目前的材質色彩、環境、擴散、反射和發出的燈光、已啟用的燈清單，以及聚光燈的方向。 當您呼叫 [**glPopAttrib**](glpopattrib.md)時，所有這些變數都會還原。 若要找出針對特定遮罩值所儲存的屬性，請參閱 [OpenGL 狀態變數](opengl-state-variables.md)。

 

 





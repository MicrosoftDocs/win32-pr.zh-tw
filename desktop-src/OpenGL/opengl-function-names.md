---
title: OpenGL 函數名稱
description: 許多 OpenGL 函式都是彼此的變化，大多不同于其引數的資料類型。
ms.assetid: 2d30e2e4-9671-4e57-962d-0328b13159f3
keywords:
- OpenGL、函數名稱
- 函數名稱 OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7729ca1f8a092c261a2ae87a835b51ea253ff2d09de710a830458c0825642bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118936878"
---
# <a name="opengl-function-names"></a>OpenGL 函數名稱

許多 OpenGL 函式都是彼此的變化，大多不同于其引數的資料類型。 某些函式的相關引數數目，以及這些引數是否可指定為向量或必須在清單中分開指定。 例如，如果您使用 **glVertex2f** 函式，您必須提供 x 和 y 座標作為32位浮點數;使用 **glVertex3sv** 時，您必須為 x、y 和 z 提供三個簡短 (16 位) 整數值的陣列。 接下來的主題只會使用函式的基底名稱。 星號表示實際的函式名稱可能會比顯示的還多。 例如， [glVertex \*](glvertex-functions.md)代表您用來指定頂點的函式的所有變化： **glVertex2d**、 **glVertex2f**、 **glVertex2i** 等等。

OpenGL 函式的效果會根據是否啟用特定模式而有所不同。 例如，如果光源相關的函式要產生適當的發亮物件，您就必須啟用光源。 若要啟用特定模式，請使用 [**glEnable**](glenable.md) 函式，並提供適當的常數來識別 (例如 GL \_ 照明) 的模式。 若要停用模式，請使用 [**glDisable**](gldisable.md)。 如需可啟用之模式的完整清單，請參閱 **glEnable** 。

 

 





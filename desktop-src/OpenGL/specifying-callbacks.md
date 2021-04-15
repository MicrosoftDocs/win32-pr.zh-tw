---
title: 指定回呼
description: 您最多可以為鑲嵌式指定五個回呼函數。
ms.assetid: b49a8400-8111-450d-a2d7-c313a898a213
keywords:
- " (X.GLU 隊) 的 OpenGL 公用程式，指定回呼函式"
- X.GLU 隊 (OpenGL 公用程式) ，指定回呼函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6086448cf6f4a71ea6a49359d5656f12f613d760
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507409"
---
# <a name="specifying-callbacks"></a>指定回呼

您最多可以為鑲嵌式指定五個回呼函數。 您未指定的任何函式都不會在鑲嵌期間呼叫，且您不會取得任何可能傳回的資訊。 您可以使用 [*gluTessCallback*](glutess.md)來指定回呼函數。

**GluTessCallback** 函式 *會讓回呼* 函式與鑲嵌式物件 *tessobj* 產生關聯。 回呼的類型取決於參數 *類型*，可以是 **X.glu 隊 \_ BEGIN**、 **X.glu 隊 \_ EDGE \_ 旗** 標、 **x.glu 隊 \_ 頂點**、 **x.glu 隊 \_ END** 或 **x.glu 隊 \_ 錯誤**。 五個可能的回呼函數具有下列原型。



| 回呼函數   | 原型                                    |
|---------------------|----------------------------------------------|
| **X.GLU 隊 \_ 開始**      | **void** **Begin** ( **GLenum * * * 類型* ) ;       |
| **X.GLU 隊 \_ EDGE \_ 旗標** | **void** **EdgeFlag** ( **GLboolean * * * 旗* 標 ) ; |
| **X.GLU 隊 \_ 頂點**     | **void** **頂點** ( **void \* * * * 資料* ) ;     |
| **X.GLU 隊 \_ 結束**        | **void** **end** ( *void* ) ;                  |
| **X.GLU 隊 \_ 錯誤**      | **void** **Error** ( **GLenum * * * errno* ) ;      |



 

若要變更回呼函數，請使用新的函式來呼叫 [*gluTessCallback*](glutess.md) 。 若要消除回呼函式，而不將它取代為新的函式，請針對適當的函式傳遞 **gluTessCallback** 為 null 指標。

當鑲嵌式進行時，回呼函式的呼叫方式類似于使用 OpenGL 函數 [**glBegin**](glbegin.md)、 [glEdgeFlag](gledgeflag-functions.md)、 [glVertex](glvertex-functions.md)和 [**glEnd**](glend.md)。

使用三個可能參數中的其中一個來叫用 **X.glu 隊 \_ BEGIN** 回呼函數：

-   GL \_ 三角形 \_ 風扇
-   GL \_ 三角形 \_ 條紋
-   GL \_ 三角形

呼叫 **X.glu 隊 \_ BEGIN** 回呼函式，並在呼叫與 **x.glu 隊 \_ END** 相關聯的回呼函式之前，會叫用一些 **x.glu 隊 \_ 邊緣 \_ 旗** 標和 **x.glu 隊 \_ 頂點** 回呼的組合。 相關聯的頂點和邊緣旗標在 **glBegin** (GL \_ 三角形 \_ 風扇) 、 **glBegin** (gl \_ 三角形區域 \_) 或 **glBegin** (gl 三角形 \_ **)** 和相符 **glEnd** 之間，會完全以 OpenGL 來解讀。

因為邊緣旗標在三角形風扇或三角形區域中沒有任何意義，所以如果有與 **X.glu 隊 \_ edge \_ 旗** 標相關聯的回呼函式，則只會使用 **GL \_ 三角形** 來呼叫 **x.glu 隊 \_ 開始** 回呼。 **X.glu 隊 \_ EDGE \_ 旗** 標回呼函式可以類似至 OpenGL [glEdgeFlag](gledgeflag-functions.md)函式。

如果鑲嵌期間發生錯誤，則會叫用錯誤回呼函數。 錯誤回呼函式會傳遞 X.GLU 隊錯誤號碼。 您可以使用 [**gluErrorString**](gluerrorstring.md) 函數取得描述錯誤的字元字串。

 

 





---
title: 使用鑲嵌式物件
description: 在描述和鑲嵌複雜的多邊形時，需要相關聯的資料，例如頂點、邊緣和回呼函數。
ms.assetid: b6102e25-280c-4d0d-9350-d0038d1a0306
keywords:
- OpenGL 公用程式 (X.GLU 隊) 、鑲嵌式物件
- X.GLU 隊 (OpenGL 公用程式) 、鑲嵌式物件
- 鑲嵌式物件 OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efc2ca11fd037f79a88fed1568c97a24692060d723327cde0c8e8842ed21d084
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011896"
---
# <a name="using-tessellation-objects"></a>使用鑲嵌式物件

在描述和鑲嵌複雜的多邊形時，需要相關聯的資料，例如頂點、邊緣和回呼函數。 所有這些資料都會系結至單一鑲嵌物件。 若要 tessellate 多邊形，您必須先使用 [**gluNewTess**](glunewtess.md) 函式來建立新的鑲嵌式物件，並傳回其指標。 如果函式失敗，則會傳回 null 指標。

如果您不再需要鑲嵌式物件，您可以將其刪除，並使用 [**gluDeleteTess**](gludeletetess.md)釋放所有相關聯的記憶體。

您可以針對所有鑲嵌重複使用單一鑲嵌式物件。 此物件是必要的，因為程式庫函式可能需要執行自己的鑲嵌，而且應該能夠這麼做，而不會干擾程式所執行的任何鑲嵌。 如果您想要針對不同的鑲嵌使用不同的回呼集合，則多個鑲嵌物件也很有用。 不過，通常您會配置單一鑲嵌物件，並將它用於所有鑲嵌。 因為它使用少量的記憶體，所以沒有真正的需要釋放它。 另一方面，如果您要撰寫使用 X.GLU 隊鑲嵌的程式庫函數，請小心釋放您所建立的任何鑲嵌式物件。

 

 





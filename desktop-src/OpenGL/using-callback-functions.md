---
title: 使用回呼函式
description: X.GLU 隊回呼函式（gluBeginPolygon、gluTessVertex、gluNextContour 和 gluEndPolygon）類似于 OpenGL 多邊形函數。
ms.assetid: e8277ba9-e270-4d7d-a29f-143f2f0d0324
keywords:
- OpenGL 公用程式 (X.GLU 隊) ，回呼函數
- X.GLU 隊 (OpenGL 公用程式) ，回呼函數
- OpenGL 公用程式 (X.GLU 隊) ，鑲嵌
- X.GLU 隊 (OpenGL 公用程式) ，鑲嵌
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75556b8c366c83df5a5976c867e6fc5f68d520da65ed8f34609f312cbfebaa7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118932893"
---
# <a name="using-callback-functions"></a>使用回呼函式

X.GLU 隊回呼函式（ [**gluBeginPolygon**](glubeginpolygon.md)、 [**gluTessVertex**](glutessvertex.md)、 [**gluNextContour**](glunextcontour.md)和 [**gluEndPolygon**](gluendpolygon.md)）類似于 OpenGL 多邊形函數。

它們通常會在使用者定義的資料結構或 OpenGL 顯示清單中儲存三角形、三角形網格和三角形風扇的資料。 若要轉譯多邊形，其他程式碼會進行資料結構或呼叫顯示清單。 雖然回呼函式可以呼叫 OpenGL 函式來直接顯示多邊形，但這通常不會這麼做，因為鑲嵌可能會耗用大量資源的計算。 如果您有可能想要再次顯示資料，最好先儲存資料。 X.GLU 隊鑲嵌函式保證永遠不會傳回任何新頂點，因此，不需要頂點、材質座標或色彩的插補。

 

 





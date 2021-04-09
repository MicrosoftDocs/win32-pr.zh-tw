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
ms.openlocfilehash: a826d9416f94304762be2e840a3b6fea9ba458ec
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839703"
---
# <a name="using-callback-functions"></a><span data-ttu-id="3dc3e-107">使用回呼函式</span><span class="sxs-lookup"><span data-stu-id="3dc3e-107">Using Callback Functions</span></span>

<span data-ttu-id="3dc3e-108">X.GLU 隊回呼函式（ [**gluBeginPolygon**](glubeginpolygon.md)、 [**gluTessVertex**](glutessvertex.md)、 [**gluNextContour**](glunextcontour.md)和 [**gluEndPolygon**](gluendpolygon.md)）類似于 OpenGL 多邊形函數。</span><span class="sxs-lookup"><span data-stu-id="3dc3e-108">The GLU callback functions, [**gluBeginPolygon**](glubeginpolygon.md), [**gluTessVertex**](glutessvertex.md), [**gluNextContour**](glunextcontour.md), and [**gluEndPolygon**](gluendpolygon.md), are similar to the OpenGL polygon functions.</span></span>

<span data-ttu-id="3dc3e-109">它們通常會在使用者定義的資料結構或 OpenGL 顯示清單中儲存三角形、三角形網格和三角形風扇的資料。</span><span class="sxs-lookup"><span data-stu-id="3dc3e-109">They typically save the data for the triangles, triangle meshes, and triangle fans in user-defined data structures or in OpenGL display lists.</span></span> <span data-ttu-id="3dc3e-110">若要轉譯多邊形，其他程式碼會進行資料結構或呼叫顯示清單。</span><span class="sxs-lookup"><span data-stu-id="3dc3e-110">To render the polygons, other code traverses the data structures or calls the display lists.</span></span> <span data-ttu-id="3dc3e-111">雖然回呼函式可以呼叫 OpenGL 函式來直接顯示多邊形，但這通常不會這麼做，因為鑲嵌可能會耗用大量資源的計算。</span><span class="sxs-lookup"><span data-stu-id="3dc3e-111">Although the callback functions could call OpenGL functions to display polygons directly, this is usually not done, as tessellation can be computationally resource-intensive.</span></span> <span data-ttu-id="3dc3e-112">如果您有可能想要再次顯示資料，最好先儲存資料。</span><span class="sxs-lookup"><span data-stu-id="3dc3e-112">It's a good idea to save the data if there is any chance that you want to display it again.</span></span> <span data-ttu-id="3dc3e-113">X.GLU 隊鑲嵌函式保證永遠不會傳回任何新頂點，因此，不需要頂點、材質座標或色彩的插補。</span><span class="sxs-lookup"><span data-stu-id="3dc3e-113">The GLU tessellation functions are guaranteed never to return any new vertices, so interpolation of vertices, texture coordinates, or colors is never required.</span></span>

 

 





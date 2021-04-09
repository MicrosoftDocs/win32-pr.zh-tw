---
title: OpenGL 公用程式庫
description: OpenGL 公用程式庫
ms.assetid: 54a7cdce-b38d-416a-a59d-827b6fb76b47
keywords:
- 'OpenGL、OpenGL 公用程式 (X.GLU 隊) '
- 'OpenGL 公用程式 (X.GLU 隊) '
- X.GLU 隊程式庫 OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d40d4a6fa51354204ee37bfc43e9217b742b882
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840031"
---
# <a name="opengl-utility-library"></a><span data-ttu-id="3219b-106">OpenGL 公用程式庫</span><span class="sxs-lookup"><span data-stu-id="3219b-106">OpenGL Utility Library</span></span>

<span data-ttu-id="3219b-107">OpenGL 公用程式 (X.GLU 隊) 程式庫包含數個函數群組，藉由提供協助工具的支援來補充核心 OpenGL 介面。</span><span class="sxs-lookup"><span data-stu-id="3219b-107">The OpenGL Utility (GLU) library contains several groups of functions that complement the core OpenGL interface by providing support for auxiliary features.</span></span> <span data-ttu-id="3219b-108">這些公用程式函式會使用核心 OpenGL 函式，因此可保證任何 OpenGL 實作為支援公用程式函式。</span><span class="sxs-lookup"><span data-stu-id="3219b-108">These utility functions make use of core OpenGL functions, so any OpenGL implementation is guaranteed to support the utility functions.</span></span>

> [!Note]  
> <span data-ttu-id="3219b-109">公用程式程式庫函數的前置詞為 "x.glu 隊"，而不是 "gl"。</span><span class="sxs-lookup"><span data-stu-id="3219b-109">The prefix for Utility library functions is "glu" rather than "gl."</span></span>

 

<span data-ttu-id="3219b-110">這些函式有許多會在檔的前面幾節中描述。</span><span class="sxs-lookup"><span data-stu-id="3219b-110">Many of these functions are described in preceding sections of the documenation as their topics arise.</span></span> <span data-ttu-id="3219b-111">以下列出這些函式的完整性。</span><span class="sxs-lookup"><span data-stu-id="3219b-111">These functions are listed here for completeness.</span></span> <span data-ttu-id="3219b-112">先前章節中未討論的 X.GLU 隊函式如下所述。</span><span class="sxs-lookup"><span data-stu-id="3219b-112">GLU functions that aren't discussed in preceding sections are described here.</span></span> <span data-ttu-id="3219b-113">如需這些函式的詳細說明，請參閱 *OpenGL 參考手冊*。</span><span class="sxs-lookup"><span data-stu-id="3219b-113">For more detailed descriptions of these functions, see the *OpenGL Reference Manual*.</span></span> <span data-ttu-id="3219b-114">本節將相關的 X.GLU 隊函數分組，如下所示：</span><span class="sxs-lookup"><span data-stu-id="3219b-114">This section groups related GLU functions, as follows:</span></span>

-   [<span data-ttu-id="3219b-115">初始 化</span><span class="sxs-lookup"><span data-stu-id="3219b-115">Initializing</span></span>](initializing.md)
-   [<span data-ttu-id="3219b-116">操作影像以用於紋理</span><span class="sxs-lookup"><span data-stu-id="3219b-116">Manipulating Images for Use in Texturing</span></span>](manipulating-images-for-use-in-texturing.md)
-   [<span data-ttu-id="3219b-117">轉換座標</span><span class="sxs-lookup"><span data-stu-id="3219b-117">Transforming Coordinates</span></span>](transforming-coordinates.md)
-   [<span data-ttu-id="3219b-118">鑲嵌多邊形</span><span class="sxs-lookup"><span data-stu-id="3219b-118">Tessellating Polygons</span></span>](tessellating-polygons.md)
-   [<span data-ttu-id="3219b-119">使用回呼函式</span><span class="sxs-lookup"><span data-stu-id="3219b-119">Using Callback Functions</span></span>](using-callback-functions.md)
-   [<span data-ttu-id="3219b-120">使用鑲嵌式物件</span><span class="sxs-lookup"><span data-stu-id="3219b-120">Using Tessellation Objects</span></span>](using-tessellation-objects.md)
-   [<span data-ttu-id="3219b-121">指定回呼</span><span class="sxs-lookup"><span data-stu-id="3219b-121">Specifying Callbacks</span></span>](specifying-callbacks.md)
-   [<span data-ttu-id="3219b-122">指定要鑲嵌的多邊形</span><span class="sxs-lookup"><span data-stu-id="3219b-122">Specifying the Polygon to Be Tessellated</span></span>](specifying-the-polygon-to-be-tessellated.md)
-   [<span data-ttu-id="3219b-123">轉譯簡單的表面</span><span class="sxs-lookup"><span data-stu-id="3219b-123">Rendering Simple Surfaces</span></span>](rendering-simple-surfaces.md)
-   [<span data-ttu-id="3219b-124">使用 NURBS 曲線和表面</span><span class="sxs-lookup"><span data-stu-id="3219b-124">Using NURBS Curves and Surfaces</span></span>](using-nurbs-curves-and-surfaces.md)
-   [<span data-ttu-id="3219b-125">處理錯誤</span><span class="sxs-lookup"><span data-stu-id="3219b-125">Handling Errors</span></span>](handling-errors.md)

 

 





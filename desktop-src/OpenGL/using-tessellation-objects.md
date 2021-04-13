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
ms.openlocfilehash: 590ab571e656fcd346da265bfa921cb965fdf540
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300476"
---
# <a name="using-tessellation-objects"></a><span data-ttu-id="4a0db-106">使用鑲嵌式物件</span><span class="sxs-lookup"><span data-stu-id="4a0db-106">Using Tessellation Objects</span></span>

<span data-ttu-id="4a0db-107">在描述和鑲嵌複雜的多邊形時，需要相關聯的資料，例如頂點、邊緣和回呼函數。</span><span class="sxs-lookup"><span data-stu-id="4a0db-107">As a complex polygon is being described and tessellated, it requires associated data, such as the vertices, edges, and callback functions.</span></span> <span data-ttu-id="4a0db-108">所有這些資料都會系結至單一鑲嵌物件。</span><span class="sxs-lookup"><span data-stu-id="4a0db-108">All this data is tied to a single tessellation object.</span></span> <span data-ttu-id="4a0db-109">若要 tessellate 多邊形，您必須先使用 [**gluNewTess**](glunewtess.md) 函式來建立新的鑲嵌式物件，並傳回其指標。</span><span class="sxs-lookup"><span data-stu-id="4a0db-109">To tessellate a polygon, you first use the [**gluNewTess**](glunewtess.md) function which creates a new tessellation object and returns a pointer to it.</span></span> <span data-ttu-id="4a0db-110">如果函式失敗，則會傳回 null 指標。</span><span class="sxs-lookup"><span data-stu-id="4a0db-110">A null pointer is returned if the function fails.</span></span>

<span data-ttu-id="4a0db-111">如果您不再需要鑲嵌式物件，您可以將其刪除，並使用 [**gluDeleteTess**](gludeletetess.md)釋放所有相關聯的記憶體。</span><span class="sxs-lookup"><span data-stu-id="4a0db-111">If you no longer need a tessellation object, you can delete it and free all associated memory with [**gluDeleteTess**](gludeletetess.md).</span></span>

<span data-ttu-id="4a0db-112">您可以針對所有鑲嵌重複使用單一鑲嵌式物件。</span><span class="sxs-lookup"><span data-stu-id="4a0db-112">You can reuse a single tessellation object for all your tessellations.</span></span> <span data-ttu-id="4a0db-113">此物件是必要的，因為程式庫函式可能需要執行自己的鑲嵌，而且應該能夠這麼做，而不會干擾程式所執行的任何鑲嵌。</span><span class="sxs-lookup"><span data-stu-id="4a0db-113">This object is required only because library functions may need to do their own tessellations, and they should be able to do so without interfering with any tessellation that your program is performing.</span></span> <span data-ttu-id="4a0db-114">如果您想要針對不同的鑲嵌使用不同的回呼集合，則多個鑲嵌物件也很有用。</span><span class="sxs-lookup"><span data-stu-id="4a0db-114">Multiple tessellation objects are also useful if you want to use different sets of callbacks for different tessellations.</span></span> <span data-ttu-id="4a0db-115">不過，通常您會配置單一鑲嵌物件，並將它用於所有鑲嵌。</span><span class="sxs-lookup"><span data-stu-id="4a0db-115">Typically, however, you allocate a single tessellation object and use it for all the tessellations.</span></span> <span data-ttu-id="4a0db-116">因為它使用少量的記憶體，所以沒有真正的需要釋放它。</span><span class="sxs-lookup"><span data-stu-id="4a0db-116">There's no real need to free it, because it uses a small amount of memory.</span></span> <span data-ttu-id="4a0db-117">另一方面，如果您要撰寫使用 X.GLU 隊鑲嵌的程式庫函數，請小心釋放您所建立的任何鑲嵌式物件。</span><span class="sxs-lookup"><span data-stu-id="4a0db-117">On the other hand, if you're writing a library function that uses GLU tessellation, be careful to free any tessellation objects you create.</span></span>

 

 





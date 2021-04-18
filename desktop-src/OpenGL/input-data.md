---
title: 輸入資料
description: OpenGL 管線需要您輸入數種類型的資料
ms.assetid: e820d093-3e39-4feb-ab2a-0c28e298bde4
keywords:
- OpenGL 處理管線，輸入資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 121cf032e0e718b95fd42f3001d2ff8efee1f6b5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968835"
---
# <a name="input-data"></a><span data-ttu-id="d2e02-104">輸入資料</span><span class="sxs-lookup"><span data-stu-id="d2e02-104">Input Data</span></span>

<span data-ttu-id="d2e02-105">OpenGL 管線會要求您輸入數種類型的資料：</span><span class="sxs-lookup"><span data-stu-id="d2e02-105">The OpenGL pipeline requires you to input several types of data:</span></span>

-   <span data-ttu-id="d2e02-106">**頂點**。</span><span class="sxs-lookup"><span data-stu-id="d2e02-106">**Vertices**.</span></span> <span data-ttu-id="d2e02-107">頂點描述所需幾何物件的形狀。</span><span class="sxs-lookup"><span data-stu-id="d2e02-107">Vertices describe the shape of the desired geometric object.</span></span> <span data-ttu-id="d2e02-108">若要指定頂點，請使用 [**\* glVertex**](glvertex-functions.md)函數搭配 [**glBegin**](glbegin.md)和 [**glEnd**](glend.md)來建立點、線條或多邊形。</span><span class="sxs-lookup"><span data-stu-id="d2e02-108">To specify vertices, use [**glVertex\***](glvertex-functions.md) functions in conjunction with [**glBegin**](glbegin.md) and [**glEnd**](glend.md) to create a point, line, or polygon.</span></span> <span data-ttu-id="d2e02-109">您也可以使用 [**glRect**](glrect-functions.md) 來一次描述整個矩形。</span><span class="sxs-lookup"><span data-stu-id="d2e02-109">You can also use [**glRect**](glrect-functions.md) to describe an entire rectangle at one time.</span></span>
-   <span data-ttu-id="d2e02-110">**邊緣旗** 標。</span><span class="sxs-lookup"><span data-stu-id="d2e02-110">**Edge flag**.</span></span> <span data-ttu-id="d2e02-111">依預設，多邊形的所有邊緣都是邊界邊緣。</span><span class="sxs-lookup"><span data-stu-id="d2e02-111">By default, all edges of polygons are boundary edges.</span></span> <span data-ttu-id="d2e02-112">使用 [**glEdgeFlag \***](gledgeflag-functions.md)明確設定 edge 旗標。</span><span class="sxs-lookup"><span data-stu-id="d2e02-112">Use [**glEdgeFlag\***](gledgeflag-functions.md) to explicitly set the edge flag.</span></span>
-   <span data-ttu-id="d2e02-113">**目前的點陣定位**。</span><span class="sxs-lookup"><span data-stu-id="d2e02-113">**Current raster position**.</span></span> <span data-ttu-id="d2e02-114">使用 [**glRasterPos \***](glrasterpos-functions.md)指定時，目前的點陣位置會用來決定圖元和點陣圖繪圖作業的點陣座標。</span><span class="sxs-lookup"><span data-stu-id="d2e02-114">Specified with [**glRasterPos\***](glrasterpos-functions.md), the current raster position is used to determine raster coordinates for pixel- and bitmap-drawing operations.</span></span>
-   <span data-ttu-id="d2e02-115">**目前的一般**。</span><span class="sxs-lookup"><span data-stu-id="d2e02-115">**Current normal**.</span></span> <span data-ttu-id="d2e02-116">與特定頂點相關聯的一般向量會決定該頂點上的介面如何在三維空間中導向;接著，這會影響特定頂點接收的光線量。</span><span class="sxs-lookup"><span data-stu-id="d2e02-116">A normal vector associated with a particular vertex determines how a surface at that vertex is oriented in three-dimensional space; this in turn affects how much light that particular vertex receives.</span></span> <span data-ttu-id="d2e02-117">使用 [**glNormal \***](glnormal-functions.md)來指定一般向量。</span><span class="sxs-lookup"><span data-stu-id="d2e02-117">Use [**glNormal\***](glnormal-functions.md) to specify a normal vector.</span></span>
-   <span data-ttu-id="d2e02-118">**目前的色彩**。</span><span class="sxs-lookup"><span data-stu-id="d2e02-118">**Current color**.</span></span> <span data-ttu-id="d2e02-119">頂點的色彩與光源條件，會決定最終的亮色。</span><span class="sxs-lookup"><span data-stu-id="d2e02-119">The color of a vertex, together with the lighting conditions, determine the final, lit color.</span></span> <span data-ttu-id="d2e02-120">如果在 RGBA 模式中，則以 [**glColor \***](glcolor-functions.md)指定色彩，或是在色彩索引模式下使用 [**glIndex \***](glindex-functions.md) 。</span><span class="sxs-lookup"><span data-stu-id="d2e02-120">Color is specified with [**glColor\***](glcolor-functions.md) if in RGBA mode, or with [**glIndex\***](glindex-functions.md) if in color-index mode.</span></span>
-   <span data-ttu-id="d2e02-121">**目前的材質座標**。</span><span class="sxs-lookup"><span data-stu-id="d2e02-121">**Current texture coordinates**.</span></span> <span data-ttu-id="d2e02-122">以 [**glTexCoord \***](gltexcoord-functions.md)指定的材質座標可決定材質地圖中與物件頂點關聯的位置。</span><span class="sxs-lookup"><span data-stu-id="d2e02-122">Specified with [**glTexCoord\***](gltexcoord-functions.md), texture coordinates determine the location in a texture map to associate with a vertex of an object.</span></span>

> [!Note]  
> <span data-ttu-id="d2e02-123">當 **呼叫 \* glVertex** 時，產生的頂點會繼承目前的邊緣旗標、正常、色彩和材質座標。</span><span class="sxs-lookup"><span data-stu-id="d2e02-123">When **glVertex\*** is called, the resulting vertex inherits the current edge flag, normal, color, and texture coordinates.</span></span> <span data-ttu-id="d2e02-124">因此，必須在 **glVertex \*** 之前呼叫 **glEdgeFlag \***、 **glNormal \***、 **\* glColor** 和 **glTexCoord \*** ，以影響產生的頂點。</span><span class="sxs-lookup"><span data-stu-id="d2e02-124">Therefore, **glEdgeFlag\***, **glNormal\***, **glColor\***, and **glTexCoord\*** must be called before **glVertex\***, if they are to affect the resulting vertex.</span></span>

 

 

 





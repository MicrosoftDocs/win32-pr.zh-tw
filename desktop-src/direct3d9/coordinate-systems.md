---
description: 3D 圖形應用程式通常會使用兩種類型的笛卡兒座標系統：左手和右手。
ms.assetid: 268c3024-85a5-4fd5-b575-e126dd4be97c
title: " (Direct3D 9) 協調系統"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcb9fa389b2bf11bec9ee4f8053bbeb4c822f422
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971306"
---
# <a name="coordinate-systems-direct3d-9"></a><span data-ttu-id="30b72-103"> (Direct3D 9) 協調系統</span><span class="sxs-lookup"><span data-stu-id="30b72-103">Coordinate Systems (Direct3D 9)</span></span>

<span data-ttu-id="30b72-104">3D 圖形應用程式通常會使用兩種類型的笛卡兒座標系統：左手和右手。</span><span class="sxs-lookup"><span data-stu-id="30b72-104">Typically 3D graphics applications use two types of Cartesian coordinate systems: left-handed and right-handed.</span></span> <span data-ttu-id="30b72-105">在這兩個座標系統中，正 x 軸指向右側，而正 y 軸指向上方。</span><span class="sxs-lookup"><span data-stu-id="30b72-105">In both coordinate systems, the positive x-axis points to the right, and the positive y-axis points up.</span></span> <span data-ttu-id="30b72-106">您可以藉由將左手或右手指指向正 x 軸方向，並將它們彎曲至正 y 軸的方向，以記得正 z 軸指向的方向。</span><span class="sxs-lookup"><span data-stu-id="30b72-106">You can remember which direction the positive z-axis points by pointing the fingers of either your left or right hand in the positive x-direction and curling them into the positive y-direction.</span></span> <span data-ttu-id="30b72-107">您拇指所指的方向，不論是指向您或指向您的反方向，即是該座標系統正 z 軸所指的方向。</span><span class="sxs-lookup"><span data-stu-id="30b72-107">The direction your thumb points, either toward or away from you, is the direction that the positive z-axis points for that coordinate system.</span></span> <span data-ttu-id="30b72-108">下圖顯示這兩個座標系統。</span><span class="sxs-lookup"><span data-stu-id="30b72-108">The following illustration shows these two coordinate systems.</span></span>

![左手系和右手系笛卡兒座標的圖例](images/leftrght.png)

<span data-ttu-id="30b72-110">Direct3D 使用左手系座標系統。</span><span class="sxs-lookup"><span data-stu-id="30b72-110">Direct3D uses a left-handed coordinate system.</span></span> <span data-ttu-id="30b72-111">如果您要移植以右手座標系統為基礎的應用程式，則必須對傳遞給 Direct3D 的資料進行兩項變更。</span><span class="sxs-lookup"><span data-stu-id="30b72-111">If you are porting an application that is based on a right-handed coordinate system, you must make two changes to the data passed to Direct3D.</span></span>

-   <span data-ttu-id="30b72-112">翻轉三角形頂點的順序，讓系統從前面順時針轉動這些頂點。</span><span class="sxs-lookup"><span data-stu-id="30b72-112">Flip the order of triangle vertices so that the system traverses them clockwise from the front.</span></span> <span data-ttu-id="30b72-113">意即如果頂點為 v0、v1、v2，請依 v0、v2、v1 的順序傳遞給 Direct3D。</span><span class="sxs-lookup"><span data-stu-id="30b72-113">In other words, if the vertices are v0, v1, v2, pass them to Direct3D as v0, v2, v1.</span></span>
-   <span data-ttu-id="30b72-114">使用檢視矩陣將世界空間在 z 方向縮放 -1。</span><span class="sxs-lookup"><span data-stu-id="30b72-114">Use the view matrix to scale world space by -1 in the z-direction.</span></span> <span data-ttu-id="30b72-115">若要這樣做，請將您用於 \_ \_ 視圖矩陣之 D3DMATRIX 結構的31、32、 \_ 33 和 \_ 34 成員[](d3dmatrix.md)的正負號翻轉。</span><span class="sxs-lookup"><span data-stu-id="30b72-115">To do this, flip the sign of the \_31, \_32, \_33, and \_34 member of the [**D3DMATRIX**](d3dmatrix.md) structure that you use for your view matrix.</span></span>

<span data-ttu-id="30b72-116">若要取得右手 world 的數量，請使用 [**D3DXMatrixPerspectiveRH**](d3dxmatrixperspectiverh.md) 和 [**D3DXMatrixOrthoRH**](d3dxmatrixorthorh.md) 函數來定義投射轉換。</span><span class="sxs-lookup"><span data-stu-id="30b72-116">To obtain what amounts to a right-handed world, use the [**D3DXMatrixPerspectiveRH**](d3dxmatrixperspectiverh.md) and [**D3DXMatrixOrthoRH**](d3dxmatrixorthorh.md) functions to define the projection transform.</span></span> <span data-ttu-id="30b72-117">不過，請小心使用對應的 [**D3DXMatrixLookAtRH**](d3dxmatrixlookatrh.md) 函式、反轉背面剔除順序，並據此配置 cube 對應。</span><span class="sxs-lookup"><span data-stu-id="30b72-117">However, be careful to use the corresponding [**D3DXMatrixLookAtRH**](d3dxmatrixlookatrh.md) function, reverse the backface-culling order, and lay out the cube maps accordingly.</span></span>

<span data-ttu-id="30b72-118">雖然左手系和右手系座標是最常見的系統，但 3D 軟體中還使用各種不同的其他座標系統。</span><span class="sxs-lookup"><span data-stu-id="30b72-118">Although left-handed and right-handed coordinates are the most common systems, there is a variety of other coordinate systems used in 3D software.</span></span> <span data-ttu-id="30b72-119">舉例來說，3D 模型應用程式也常使用一種座標系統，其中 y 軸指向檢視器或指向其反方向，而且 z 軸朝上。</span><span class="sxs-lookup"><span data-stu-id="30b72-119">For example, it is not unusual for 3D modeling applications to use a coordinate system in which the y-axis points toward or away from the viewer, and the z-axis points up.</span></span>

<span data-ttu-id="30b72-120">正式來說，一組基礎向量的方向 (也就是座標系統) 可以藉由計算一組特定基礎向量所定義之矩陣的行列式來尋找。</span><span class="sxs-lookup"><span data-stu-id="30b72-120">Formally, the orientation of a set of basis vectors (i.e. a coordinate system) can be found by the computing the determinant of the matrix defined by the particular set of basis vectors.</span></span> <span data-ttu-id="30b72-121">如果行列式是正面的，則基準會被視為「積極」導向 (或右手) 。</span><span class="sxs-lookup"><span data-stu-id="30b72-121">If the determinant is positive, the basis is said to be "positively" oriented (or right-handed).</span></span> <span data-ttu-id="30b72-122">如果行列式是負數，則會將其視為「負面」導向 (或左手) 。</span><span class="sxs-lookup"><span data-stu-id="30b72-122">If the determinant is negative, the basis is said to be "negatively" oriented (or left-handed).</span></span> <span data-ttu-id="30b72-123">如需行列式的說明，請參閱任何線性代數資源。</span><span class="sxs-lookup"><span data-stu-id="30b72-123">For an explanation of what a determinant is, see any linear algebra resource.</span></span>

<span data-ttu-id="30b72-124">非正式地說，您可以使用「右/左邊規則」來判斷指定的一組基礎向量是否形成右手或左的座標系統。</span><span class="sxs-lookup"><span data-stu-id="30b72-124">Informally, you can use the "right/left hand rule" to determine if a given set of basis vectors form either a right or left handed coordinate system.</span></span>

<span data-ttu-id="30b72-125">在3D 座標系統中定義的物件上所執行的基本作業為轉譯、旋轉和縮放。</span><span class="sxs-lookup"><span data-stu-id="30b72-125">The essential operations performed on objects defined in a 3D coordinate system are translation, rotation, and scaling.</span></span> <span data-ttu-id="30b72-126">您可以結合這些基本轉換來建立轉換矩陣。</span><span class="sxs-lookup"><span data-stu-id="30b72-126">You can combine these basic transformations to create a transform matrix.</span></span> <span data-ttu-id="30b72-127">如需詳細資訊，請參閱 [ (Direct3D 9 的轉換) ](transforms.md)。</span><span class="sxs-lookup"><span data-stu-id="30b72-127">For details, see [Transforms (Direct3D 9)](transforms.md).</span></span>

<span data-ttu-id="30b72-128">當您結合這些作業時，結果不可相互交換。您以倍數增加矩陣的順序至關重要。</span><span class="sxs-lookup"><span data-stu-id="30b72-128">When you combine these operations, the results are not commutative; the order in which you multiply matrices is important.</span></span>

## <a name="related-topics"></a><span data-ttu-id="30b72-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="30b72-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="30b72-130">座標系統和幾何</span><span class="sxs-lookup"><span data-stu-id="30b72-130">Coordinate Systems and Geometry</span></span>](coordinate-systems-and-geometry.md)
</dt> </dl>

 

 




---
description: 在3D 空間中，音效來源和接聽程式的位置、速度和方向會以笛卡兒座標表示，也就是三個軸上的值： X 軸、y 軸和 Z 軸。
ms.assetid: b6315e21-0758-e4c8-195f-4b83c7b61784
title: 3D 空間的座標
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3081c1a3a6c497d53d093c98732a9d381996c96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193537"
---
# <a name="coordinates-of-3d-space"></a><span data-ttu-id="e9185-103">3D 空間的座標</span><span class="sxs-lookup"><span data-stu-id="e9185-103">Coordinates of 3D Space</span></span>

<span data-ttu-id="e9185-104">在3D 空間中，音效來源和接聽程式的位置、速度和方向會以笛卡兒座標表示，也就是三個軸上的值： X 軸、y 軸和 Z 軸。</span><span class="sxs-lookup"><span data-stu-id="e9185-104">The position, velocity, and orientation of sound sources and listeners in 3D space are represented by Cartesian coordinates, which are values on three axes: the x-axis, the y-axis, and the z-axis.</span></span>

<span data-ttu-id="e9185-105">軸是相對於應用程式所建立的觀點。</span><span class="sxs-lookup"><span data-stu-id="e9185-105">The axes are relative to a viewpoint established by the application.</span></span> <span data-ttu-id="e9185-106">X 軸上的值從左至右、從上到右、從上到上、從最接近到 Z 軸向上增加。</span><span class="sxs-lookup"><span data-stu-id="e9185-106">Values on the x-axis increase from left to right, on the y-axis from down to up, and on the z-axis from near to far.</span></span>

<span data-ttu-id="e9185-107">**X3DAUDIO \_ 向量** 結構包含的值會描述三個軸上的位置、速度或方向。</span><span class="sxs-lookup"><span data-stu-id="e9185-107">The **X3DAUDIO\_VECTOR** structure contains values describing position, velocity, or orientation on the three axes.</span></span>

<span data-ttu-id="e9185-108">傳統上，向量會以括弧括住的三個值來表示，並以逗號分隔，順序 (x，y，z) 。</span><span class="sxs-lookup"><span data-stu-id="e9185-108">Conventionally, vectors are expressed as three values enclosed in parentheses and separated by commas, in the order (x, y, z).</span></span>

<span data-ttu-id="e9185-109">針對 [位置]，這些值會在使用者定義的世界單位中。</span><span class="sxs-lookup"><span data-stu-id="e9185-109">For position, the values are in user-defined world units.</span></span>

<span data-ttu-id="e9185-110">針對速度，向量會描述每個軸在每秒的世界單位中移動的速率。</span><span class="sxs-lookup"><span data-stu-id="e9185-110">For velocity, the vector describes the rate of movement along each axis in world units per second.</span></span>

<span data-ttu-id="e9185-111">針對方向，這些值會以任意單位來表示，而它們彼此相對。</span><span class="sxs-lookup"><span data-stu-id="e9185-111">For orientation, the values are in arbitrary units, and they are relative to one another.</span></span> <span data-ttu-id="e9185-112">例如，如果3D 世界的基底視圖朝水準方向，而且接聽程式的方向是 (-1、0、1) ，則接聽程式會面向西北部。</span><span class="sxs-lookup"><span data-stu-id="e9185-112">For example, if the base view of the 3D world is facing north toward the horizon, and the orientation of the listener is (-1, 0, 1), then the listener is facing northwest.</span></span> <span data-ttu-id="e9185-113">因為向量中的值不是絕對單位，所以向量同樣可以表示為 (-5、0、5) 或 (-0.25、0、0.25) 。</span><span class="sxs-lookup"><span data-stu-id="e9185-113">Because the values within a vector are not in absolute units, the vector equally could be expressed as (-5, 0, 5) or (-0.25, 0, 0.25).</span></span>

<span data-ttu-id="e9185-114">3D 向量的運作方式很類似2D 向量，但在上下方向有額外的軸。</span><span class="sxs-lookup"><span data-stu-id="e9185-114">3D vectors work much like 2D vectors, but with an additional axis in the up-down direction.</span></span> <span data-ttu-id="e9185-115">您可以藉由在圖形紙上繪製向量，查看2D 空間中向量的運作方式。</span><span class="sxs-lookup"><span data-stu-id="e9185-115">You can see how vectors work in 2D space by drawing them on a sheet of graph paper.</span></span> <span data-ttu-id="e9185-116">讓值從底部增加到紙張頂端，並從左至右。</span><span class="sxs-lookup"><span data-stu-id="e9185-116">Let the values increase from the bottom to the top of the paper, and from left to right.</span></span> <span data-ttu-id="e9185-117">從 (0、0) 到 (1、1) 從 (0、0) 到 (5，5) 所繪製的方向相同。</span><span class="sxs-lookup"><span data-stu-id="e9185-117">A line drawn from (0, 0) to (1, 1) has the same orientation, or direction, as one drawn from (0, 0) to (5, 5).</span></span> <span data-ttu-id="e9185-118">但是，第二行表示較遠的距離或速度。</span><span class="sxs-lookup"><span data-stu-id="e9185-118">However, the second line indicates a greater distance, or velocity.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e9185-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="e9185-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e9185-120">常見的音訊概念</span><span class="sxs-lookup"><span data-stu-id="e9185-120">Common Audio Concepts</span></span>](common-audio-concepts.md)
</dt> <dt>

[<span data-ttu-id="e9185-121">X3DAudio 總覽</span><span class="sxs-lookup"><span data-stu-id="e9185-121">X3DAudio Overview</span></span>](x3daudio-overview.md)
</dt> </dl>

 

 




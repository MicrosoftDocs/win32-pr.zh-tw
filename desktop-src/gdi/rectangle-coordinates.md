---
description: 應用程式必須使用 RECT 結構來定義矩形。
ms.assetid: 93c63dcb-6c8e-4c8b-aa19-6f8952d75e2e
title: 矩形座標
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb8a3fbc3f42c6d69a3d0eac6555b85fbfc1eecb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991174"
---
# <a name="rectangle-coordinates"></a><span data-ttu-id="7de79-103">矩形座標</span><span class="sxs-lookup"><span data-stu-id="7de79-103">Rectangle Coordinates</span></span>

<span data-ttu-id="7de79-104">應用程式必須使用 [**RECT**](/previous-versions//dd162897(v=vs.85)) 結構來定義矩形。</span><span class="sxs-lookup"><span data-stu-id="7de79-104">An application must use a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure to define a rectangle.</span></span> <span data-ttu-id="7de79-105">結構會指定兩個點的座標：矩形的左上角和右下角。</span><span class="sxs-lookup"><span data-stu-id="7de79-105">The structure specifies the coordinates of two points: the upper left and lower right corners of the rectangle.</span></span> <span data-ttu-id="7de79-106">矩形的側邊會從這兩個點延伸，並且平行至 X 軸和 y 軸。</span><span class="sxs-lookup"><span data-stu-id="7de79-106">The sides of the rectangle extend from these two points and are parallel to the x-axis and y-axis.</span></span>

<span data-ttu-id="7de79-107">矩形的座標值會以帶正負號的整數表示。</span><span class="sxs-lookup"><span data-stu-id="7de79-107">The coordinate values for a rectangle are expressed as signed integers.</span></span> <span data-ttu-id="7de79-108">矩形右邊的座標值必須大於其左邊的座標值。</span><span class="sxs-lookup"><span data-stu-id="7de79-108">The coordinate value of a rectangle's right side must be greater than that of its left side.</span></span> <span data-ttu-id="7de79-109">同樣地，底部的座標值必須大於頂端的座標值。</span><span class="sxs-lookup"><span data-stu-id="7de79-109">Likewise, the coordinate value of the bottom must be greater than that of the top.</span></span>

<span data-ttu-id="7de79-110">由於應用程式可以將矩形用於許多不同的用途，因此矩形函式不會使用明確的測量單位。</span><span class="sxs-lookup"><span data-stu-id="7de79-110">Because applications can use rectangles for many different purposes, the rectangle functions do not use an explicit unit of measure.</span></span> <span data-ttu-id="7de79-111">相反地，所有的矩形座標和維度都會以帶正負號的邏輯值提供。</span><span class="sxs-lookup"><span data-stu-id="7de79-111">Instead, all rectangle coordinates and dimensions are given in signed, logical values.</span></span> <span data-ttu-id="7de79-112">對應模式和使用該矩形的函式會決定測量單位。</span><span class="sxs-lookup"><span data-stu-id="7de79-112">The mapping mode and the function in which the rectangle is used determine the units of measure.</span></span> <span data-ttu-id="7de79-113">如需座標和對應模式的詳細資訊，請參閱 [座標空間和轉換](coordinate-spaces-and-transformations.md)。</span><span class="sxs-lookup"><span data-stu-id="7de79-113">For more information about coordinates and mapping modes, see [Coordinate Spaces and Transformations](coordinate-spaces-and-transformations.md).</span></span>

 

 

---
description: 本節介紹 view 轉換的基本概念，並提供如何在 Direct3D 應用程式中設定視圖轉換矩陣的詳細資料。
ms.assetid: a9885a77-f04e-4ca5-9202-67c4779d03de
title: " (Direct3D 9) 視圖轉換"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60cf933db7424b2c3aeb5aa7c06a37b03782eaa6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510138"
---
# <a name="view-transform-direct3d-9"></a><span data-ttu-id="8ab92-103"> (Direct3D 9) 視圖轉換</span><span class="sxs-lookup"><span data-stu-id="8ab92-103">View Transform (Direct3D 9)</span></span>

<span data-ttu-id="8ab92-104">本節介紹 view 轉換的基本概念，並提供如何在 Direct3D 應用程式中設定視圖轉換矩陣的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="8ab92-104">This section introduces the basic concepts of the view transform and provides details on how to set up a view transform matrix in a Direct3D application.</span></span>

<span data-ttu-id="8ab92-105">檢視轉換將檢視器放置在世界空間中，並將頂點轉換成相機空間。</span><span class="sxs-lookup"><span data-stu-id="8ab92-105">The view transform locates the viewer in world space, transforming vertices into camera space.</span></span> <span data-ttu-id="8ab92-106">在相機空間，相機或檢視器位於原點，朝著正 z 方向看。</span><span class="sxs-lookup"><span data-stu-id="8ab92-106">In camera space, the camera, or viewer, is at the origin, looking in the positive z-direction.</span></span> <span data-ttu-id="8ab92-107">回想一下，Direct3D 會使用左手型座標系統，因此 z 在場景中是正面的。</span><span class="sxs-lookup"><span data-stu-id="8ab92-107">Recall that Direct3D uses a left-handed coordinate system, so z is positive into a scene.</span></span> <span data-ttu-id="8ab92-108">檢視矩陣圍繞相機位置 (相機空間的起點) 將物件重新放置在世界空間中。</span><span class="sxs-lookup"><span data-stu-id="8ab92-108">The view matrix relocates the objects in the world around a camera's position - the origin of camera space - and orientation.</span></span>

<span data-ttu-id="8ab92-109">有許多的方式可建立檢視矩陣。</span><span class="sxs-lookup"><span data-stu-id="8ab92-109">There are many ways to create a view matrix.</span></span> <span data-ttu-id="8ab92-110">在所有情況下，相機在世界空間有特定邏輯位置和方向，做為起點用來建立檢視矩陣，套用到場景中的模型。</span><span class="sxs-lookup"><span data-stu-id="8ab92-110">In all cases, the camera has some logical position and orientation in world space that is used as a starting point to create a view matrix that will be applied to the models in a scene.</span></span> <span data-ttu-id="8ab92-111">檢視矩陣平移並旋轉物件，將它們置於相機空間中 (相機位於原點)。</span><span class="sxs-lookup"><span data-stu-id="8ab92-111">The view matrix translates and rotates objects to place them in camera space, where the camera is at the origin.</span></span> <span data-ttu-id="8ab92-112">建立檢視矩陣的一個方式是為每個軸結合旋轉矩陣和轉移矩陣。</span><span class="sxs-lookup"><span data-stu-id="8ab92-112">One way to create a view matrix is to combine a translation matrix with rotation matrices for each axis.</span></span> <span data-ttu-id="8ab92-113">下列一般矩陣方程式適用於這種方式。</span><span class="sxs-lookup"><span data-stu-id="8ab92-113">In this approach, the following general matrix equation applies.</span></span>

![檢視轉換的方程式](images/viewtran.png)

<span data-ttu-id="8ab92-115">在這個公式中，V 是所建立的檢視矩陣，T 是將物件重新置放在世界空間中的轉移矩陣，而 Rₓ 到 R<sub>z</sub> 則是沿著 x、y 與 z 軸旋轉物件的旋轉矩陣。</span><span class="sxs-lookup"><span data-stu-id="8ab92-115">In this formula, V is the view matrix being created, T is a translation matrix that repositions objects in the world, and Rₓ through R<sub>z</sub> are rotation matrices that rotate objects along the x-, y-, and z-axis.</span></span> <span data-ttu-id="8ab92-116">轉移矩陣與旋轉矩陣以世界空間中的相機邏輯位置和方向為基礎。</span><span class="sxs-lookup"><span data-stu-id="8ab92-116">The translation and rotation matrices are based on the camera's logical position and orientation in world space.</span></span> <span data-ttu-id="8ab92-117">因此，如果世界中的相機邏輯位置是 <10，20100>，則轉譯矩陣的目標是在 X 軸移動物件-10 個單位，沿著 y 軸移動20個單位，並沿著 Z 軸移動-100 個單位。</span><span class="sxs-lookup"><span data-stu-id="8ab92-117">So, if the camera's logical position in the world is <10,20,100>, the aim of the translation matrix is to move objects -10 units along the x-axis, -20 units along the y-axis, and -100 units along the z-axis.</span></span> <span data-ttu-id="8ab92-118">在公式中旋轉矩陣以相機方向為基礎，亦即相機空間的軸旋轉多少，不對齊世界空間。</span><span class="sxs-lookup"><span data-stu-id="8ab92-118">The rotation matrices in the formula are based on the camera's orientation, in terms of how much the axes of camera space are rotated out of alignment with world space.</span></span> <span data-ttu-id="8ab92-119">例如，如果前面所提到的相機往下指，其 z 軸是 90 度（pi/2 弧度），不對齊世界空間的 z 軸，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="8ab92-119">For example, if the camera mentioned earlier is pointing straight down, its z-axis is 90 degrees (pi/2 radians) out of alignment with the z-axis of world space, as shown in the following illustration.</span></span>

![相機檢視空間相對於世界空間的圖例](images/camtop.png)

<span data-ttu-id="8ab92-121">旋轉矩陣對場景中模型套用相等但相反的旋轉大小。</span><span class="sxs-lookup"><span data-stu-id="8ab92-121">The rotation matrices apply rotations of equal, but opposite, magnitude to the models in the scene.</span></span> <span data-ttu-id="8ab92-122">這個相機的檢視矩陣包含圍繞 x 軸 -90 度的旋轉。</span><span class="sxs-lookup"><span data-stu-id="8ab92-122">The view matrix for this camera includes a rotation of -90 degrees around the x-axis.</span></span> <span data-ttu-id="8ab92-123">旋轉矩陣與轉移矩陣結合，建立調整場景中物件之位置和方向的檢視矩陣，使其頂端面向相機，提供相機在模型上方的表面現象。</span><span class="sxs-lookup"><span data-stu-id="8ab92-123">The rotation matrix is combined with the translation matrix to create a view matrix that adjusts the position and orientation of the objects in the scene so that their top is facing the camera, giving the appearance that the camera is above the model.</span></span>

## <a name="setting-up-a-view-matrix"></a><span data-ttu-id="8ab92-124">設定檢視矩陣</span><span class="sxs-lookup"><span data-stu-id="8ab92-124">Setting Up a View Matrix</span></span>

<span data-ttu-id="8ab92-125">[**D3DXMatrixLookAtLH**](d3dxmatrixlookatlh.md)和 [**D3DXMatrixLookAtRH**](d3dxmatrixlookatrh.md)協助程式函式會根據相機位置和查看點建立視圖矩陣。</span><span class="sxs-lookup"><span data-stu-id="8ab92-125">The [**D3DXMatrixLookAtLH**](d3dxmatrixlookatlh.md) and [**D3DXMatrixLookAtRH**](d3dxmatrixlookatrh.md) helper functions create a view matrix based on the camera location and a look-at point.</span></span>

<span data-ttu-id="8ab92-126">下列範例會建立左手座標的視圖矩陣。</span><span class="sxs-lookup"><span data-stu-id="8ab92-126">The following example creates a view matrix for left-handed coordinates.</span></span>


```
D3DXMATRIX out;
D3DXVECTOR3 eye(2,3,3);
D3DXVECTOR3 at(0,0,0);
D3DXVECTOR3 up(0,1,0);
D3DXMatrixLookAtLH(&out, &eye, &at, &up);
```



<span data-ttu-id="8ab92-127">Direct3D 使用世界和檢視矩陣來設定數個內部資料結構。</span><span class="sxs-lookup"><span data-stu-id="8ab92-127">Direct3D uses the world and view matrices to configure several internal data structures.</span></span> <span data-ttu-id="8ab92-128">每當您設定世界或檢視矩陣，系統會重新計算相關內部結構。</span><span class="sxs-lookup"><span data-stu-id="8ab92-128">Each time you set a new world or view matrix, the system recalculates the associated internal structures.</span></span> <span data-ttu-id="8ab92-129">頻繁設定這些矩陣通常在計算上耗費時間。</span><span class="sxs-lookup"><span data-stu-id="8ab92-129">Setting these matrices frequently is computationally time-consuming.</span></span> <span data-ttu-id="8ab92-130">您可以串連世界和檢視矩陣成為世界檢視矩陣 (您將其設為世界矩陣)，然後將檢視矩陣設為單位矩陣，將所需的計算次數最小化。</span><span class="sxs-lookup"><span data-stu-id="8ab92-130">You can minimize the number of required calculations by concatenating your world and view matrices into a world-view matrix that you set as the world matrix, and then setting the view matrix to the identity.</span></span> <span data-ttu-id="8ab92-131">保留個別世界和檢視矩陣的快取複本，您可以視需要修改、串連並重設世界矩陣。</span><span class="sxs-lookup"><span data-stu-id="8ab92-131">Keep cached copies of individual world and view matrices that you can modify, concatenate, and reset the world matrix as needed.</span></span> <span data-ttu-id="8ab92-132">為了清楚起見，範例很少採用這種優化。</span><span class="sxs-lookup"><span data-stu-id="8ab92-132">For clarity, the samples rarely employ this optimization.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8ab92-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="8ab92-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8ab92-134">轉換</span><span class="sxs-lookup"><span data-stu-id="8ab92-134">Transforms</span></span>](transforms.md)
</dt> </dl>

 

 




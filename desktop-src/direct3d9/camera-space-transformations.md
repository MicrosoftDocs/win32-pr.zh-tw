---
description: 相機空間端點的計算方式為使用全球檢視矩陣轉換物件端點。
ms.assetid: 889dd0d8-1933-4901-9bbc-06c3caa26d3e
title: " (Direct3D 9) 的相機空間轉換"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e621fa8318fa45023cee13ffc6fcfc65abcf8f5b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110768"
---
# <a name="camera-space-transformations-direct3d-9"></a><span data-ttu-id="41782-103"> (Direct3D 9) 的相機空間轉換</span><span class="sxs-lookup"><span data-stu-id="41782-103">Camera Space Transformations (Direct3D 9)</span></span>

<span data-ttu-id="41782-104">相機空間端點的計算方式為使用全球檢視矩陣轉換物件端點。</span><span class="sxs-lookup"><span data-stu-id="41782-104">Vertices in the camera space are computed by transforming the object vertices with the world view matrix.</span></span>

<span data-ttu-id="41782-105">V = V \* wvMatrix</span><span class="sxs-lookup"><span data-stu-id="41782-105">V = V \* wvMatrix</span></span>

<span data-ttu-id="41782-106">相機空間頂點標準的計算方式為，使用全球檢視矩陣的反向調換來轉換物件標準。</span><span class="sxs-lookup"><span data-stu-id="41782-106">Vertex normals, in camera space, are computed by transforming the object normals with the inverse transpose of the world view matrix.</span></span> <span data-ttu-id="41782-107">全球檢視矩陣不一定是正交。</span><span class="sxs-lookup"><span data-stu-id="41782-107">The world view matrix may or may not be orthogonal.</span></span>

<span data-ttu-id="41782-108">N = N \* (wvMatrix ⁻¹) <sup>T</sup></span><span class="sxs-lookup"><span data-stu-id="41782-108">N = N \* (wvMatrix⁻¹)<sup>T</sup></span></span>

<span data-ttu-id="41782-109">矩陣反向和矩陣調換於4 x 4 矩陣運作。</span><span class="sxs-lookup"><span data-stu-id="41782-109">The matrix inversion and matrix transpose operate on a 4x4 matrix.</span></span> <span data-ttu-id="41782-110">乘積結合標準與產出之 4 x 4 矩陣的 3 x 3 部分。</span><span class="sxs-lookup"><span data-stu-id="41782-110">The multiply combines the normal with the 3x3 portion of the resulting 4x4 matrix.</span></span>

<span data-ttu-id="41782-111">如果轉譯狀態 D3DRENDERSTATE \_ NORMALIZENORMALS 設定為 **TRUE**，則會在轉換成相機空間之後，將頂點標準向量正規化，如下所示：</span><span class="sxs-lookup"><span data-stu-id="41782-111">If the render state, D3DRENDERSTATE\_NORMALIZENORMALS is set to **TRUE**, vertex normal vectors are normalized after transformation to camera space as follows:</span></span>

<span data-ttu-id="41782-112">N = norm(N)</span><span class="sxs-lookup"><span data-stu-id="41782-112">N = norm(N)</span></span>

<span data-ttu-id="41782-113">相機空間光線位置的計算方式為，使用檢視矩陣轉換光線來源位置。</span><span class="sxs-lookup"><span data-stu-id="41782-113">Light position in camera space is computed by transforming the light source position with the view matrix.</span></span>

<span data-ttu-id="41782-114">Lp = Lp \* vMatrix</span><span class="sxs-lookup"><span data-stu-id="41782-114">Lₚ = Lₚ \* vMatrix</span></span>

<span data-ttu-id="41782-115">相機空間光線方向的計算方式為，將光線來源方向乘以檢視矩陣、正規化以及取補數結果。</span><span class="sxs-lookup"><span data-stu-id="41782-115">The direction to the light in camera space for a directional light is computed by multiplying the light source direction by the view matrix, normalizing, and negating the result.</span></span>

<span data-ttu-id="41782-116">L<sub>dir</sub> =-標準 (L<sub>dir</sub> \* wvMatrix) </span><span class="sxs-lookup"><span data-stu-id="41782-116">L<sub>dir</sub> = -norm(L<sub>dir</sub> \* wvMatrix)</span></span>

<span data-ttu-id="41782-117">若為 D3DLIGHT \_ 點和 D3DLIGHT 點，則會以下列 \_ 方式計算燈的方向：</span><span class="sxs-lookup"><span data-stu-id="41782-117">For the D3DLIGHT\_POINT and D3DLIGHT\_SPOT the direction to light is computed as follows:</span></span>

<span data-ttu-id="41782-118">L<sub>dir</sub> = 標準 (的 \*) ，其中參數定義于下表中。</span><span class="sxs-lookup"><span data-stu-id="41782-118">L<sub>dir</sub> = norm(V \* Lₚ), where the parameters are defined in the following table.</span></span>



| <span data-ttu-id="41782-119">參數</span><span class="sxs-lookup"><span data-stu-id="41782-119">Parameter</span></span>       | <span data-ttu-id="41782-120">預設值</span><span class="sxs-lookup"><span data-stu-id="41782-120">Default value</span></span> | <span data-ttu-id="41782-121">類型</span><span class="sxs-lookup"><span data-stu-id="41782-121">Type</span></span>      | <span data-ttu-id="41782-122">Description</span><span class="sxs-lookup"><span data-stu-id="41782-122">Description</span></span>                                               |
|-----------------|---------------|-----------|-----------------------------------------------------------|
| <span data-ttu-id="41782-123">L<sub>dir</sub></span><span class="sxs-lookup"><span data-stu-id="41782-123">L<sub>dir</sub></span></span> | <span data-ttu-id="41782-124">N/A</span><span class="sxs-lookup"><span data-stu-id="41782-124">N/A</span></span>           | <span data-ttu-id="41782-125">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="41782-125">D3DVECTOR</span></span> | <span data-ttu-id="41782-126">從物件頂點到光線的方向向量</span><span class="sxs-lookup"><span data-stu-id="41782-126">Direction vector from object vertex to the light</span></span>          |
| <span data-ttu-id="41782-127">V</span><span class="sxs-lookup"><span data-stu-id="41782-127">V</span></span>               | <span data-ttu-id="41782-128">N/A</span><span class="sxs-lookup"><span data-stu-id="41782-128">N/A</span></span>           | <span data-ttu-id="41782-129">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="41782-129">D3DVECTOR</span></span> | <span data-ttu-id="41782-130">相機空間的頂點位置</span><span class="sxs-lookup"><span data-stu-id="41782-130">Vertex position in camera space</span></span>                           |
| <span data-ttu-id="41782-131">wvMatrix</span><span class="sxs-lookup"><span data-stu-id="41782-131">wvMatrix</span></span>        | <span data-ttu-id="41782-132">身分識別</span><span class="sxs-lookup"><span data-stu-id="41782-132">Identity</span></span>      | <span data-ttu-id="41782-133">D3DMATRIX</span><span class="sxs-lookup"><span data-stu-id="41782-133">D3DMATRIX</span></span> | <span data-ttu-id="41782-134">複合矩陣包含全球及檢視轉換</span><span class="sxs-lookup"><span data-stu-id="41782-134">Composite matrix containing the world and view transforms</span></span> |
| <span data-ttu-id="41782-135">N</span><span class="sxs-lookup"><span data-stu-id="41782-135">N</span></span>               | <span data-ttu-id="41782-136">N/A</span><span class="sxs-lookup"><span data-stu-id="41782-136">N/A</span></span>           | <span data-ttu-id="41782-137">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="41782-137">D3DVECTOR</span></span> | <span data-ttu-id="41782-138">頂點垂直</span><span class="sxs-lookup"><span data-stu-id="41782-138">Vertex normal</span></span>                                             |
| <span data-ttu-id="41782-139">Lₚ</span><span class="sxs-lookup"><span data-stu-id="41782-139">Lₚ</span></span>              | <span data-ttu-id="41782-140">N/A</span><span class="sxs-lookup"><span data-stu-id="41782-140">N/A</span></span>           | <span data-ttu-id="41782-141">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="41782-141">D3DVECTOR</span></span> | <span data-ttu-id="41782-142">相機空間的光線位置</span><span class="sxs-lookup"><span data-stu-id="41782-142">Light position in camera space</span></span>                            |
| <span data-ttu-id="41782-143">vMatrix</span><span class="sxs-lookup"><span data-stu-id="41782-143">vMatrix</span></span>         | <span data-ttu-id="41782-144">身分識別</span><span class="sxs-lookup"><span data-stu-id="41782-144">Identity</span></span>      | <span data-ttu-id="41782-145">D3DMATRIX</span><span class="sxs-lookup"><span data-stu-id="41782-145">D3DMATRIX</span></span> | <span data-ttu-id="41782-146">矩陣包含檢視轉換</span><span class="sxs-lookup"><span data-stu-id="41782-146">Matrix containing the view transform</span></span>                      |



 

## <a name="related-topics"></a><span data-ttu-id="41782-147">相關主題</span><span class="sxs-lookup"><span data-stu-id="41782-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="41782-148">燈光數學</span><span class="sxs-lookup"><span data-stu-id="41782-148">Mathematics of Lighting</span></span>](mathematics-of-lighting.md)
</dt> </dl>

 

 




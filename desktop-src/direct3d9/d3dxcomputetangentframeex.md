---
description: 在網格上執行正切框架計算。 會產生正切函數、binormal 和選擇性的一般向量。 藉由群組邊緣和分割頂點，Singularities 會視需要進行處理。
ms.assetid: 15cc46bc-6db6-4e1d-a95e-cd60d2666600
title: 'D3DXComputeTangentFrameEx 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeTangentFrameEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 58c7e8a1f1f7247d6a3ecc92d5771d68c9c3e5a9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106976465"
---
# <a name="d3dxcomputetangentframeex-function"></a><span data-ttu-id="6dfc4-105">D3DXComputeTangentFrameEx 函式</span><span class="sxs-lookup"><span data-stu-id="6dfc4-105">D3DXComputeTangentFrameEx function</span></span>

<span data-ttu-id="6dfc4-106">在網格上執行正切框架計算。</span><span class="sxs-lookup"><span data-stu-id="6dfc4-106">Performs tangent frame computations on a mesh.</span></span> <span data-ttu-id="6dfc4-107">會產生正切函數、binormal 和選擇性的一般向量。</span><span class="sxs-lookup"><span data-stu-id="6dfc4-107">Tangent, binormal, and optionally normal vectors are generated.</span></span> <span data-ttu-id="6dfc4-108">藉由群組邊緣和分割頂點，Singularities 會視需要進行處理。</span><span class="sxs-lookup"><span data-stu-id="6dfc4-108">Singularities are handled as required by grouping edges and splitting vertices.</span></span>

## <a name="syntax"></a><span data-ttu-id="6dfc4-109">語法</span><span class="sxs-lookup"><span data-stu-id="6dfc4-109">Syntax</span></span>


```C++
HRESULT D3DXComputeTangentFrameEx(
  _In_        ID3DXMesh   *pMesh,
  _In_        DWORD       dwTextureInSemantic,
  _In_        DWORD       dwTextureInIndex,
  _In_        DWORD       dwUPartialOutSemantic,
  _In_        DWORD       dwUPartialOutIndex,
  _In_        DWORD       dwVPartialOutSemantic,
  _In_        DWORD       dwVPartialOutIndex,
  _In_        DWORD       dwNormalOutSemantic,
  _In_        DWORD       dwNormalOutIndex,
  _In_        DWORD       dwOptions,
  _In_  const DWORD       *pdwAdjacency,
  _In_        FLOAT       fPartialEdgeThreshold,
  _In_        FLOAT       fSingularPointThreshold,
  _In_        FLOAT       fNormalEdgeThreshold,
  _Out_       ID3DXMesh   **ppMeshOut,
  _Out_       ID3DXBuffer **ppVertexMapping
);
```



## <a name="parameters"></a><span data-ttu-id="6dfc4-110">參數</span><span class="sxs-lookup"><span data-stu-id="6dfc4-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6dfc4-111">*pMesh* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6dfc4-111">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6dfc4-112">類型： **[ **ID3DXMesh**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="6dfc4-112">Type: **[**ID3DXMesh**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="6dfc4-113">輸入 [**ID3DXMesh**](id3dxmesh.md) 網格物件的指標。</span><span class="sxs-lookup"><span data-stu-id="6dfc4-113">Pointer to an input [**ID3DXMesh**](id3dxmesh.md) mesh object.</span></span>

</dd> <dt>

<span data-ttu-id="6dfc4-114">*dwTextureInSemantic* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6dfc4-114">*dwTextureInSemantic* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6dfc4-115">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6dfc4-115">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6dfc4-116">指定紋理座標輸入語義。</span><span class="sxs-lookup"><span data-stu-id="6dfc4-116">Specifies the texture coordinate input semantic.</span></span> <span data-ttu-id="6dfc4-117">如果 D3DX \_ 預設值，此函式會假設沒有紋理座標，而且除非指定了一般向量計算，否則函數會失敗。</span><span class="sxs-lookup"><span data-stu-id="6dfc4-117">If D3DX\_DEFAULT, the function assumes that there are no texture coordinates, and the function will fail unless normal vector calculation is specified.</span></span>

</dd> <dt>

<span data-ttu-id="6dfc4-118">*dwTextureInIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6dfc4-118">*dwTextureInIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6dfc4-119">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6dfc4-119">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6dfc4-120">如果網格具有多個材質座標，請指定要用於正切框架計算的材質座標。</span><span class="sxs-lookup"><span data-stu-id="6dfc4-120">If a mesh has multiple texture coordinates, specifies the texture coordinate to use for the tangent frame computations.</span></span> <span data-ttu-id="6dfc4-121">如果為零，則表示網格只有單一材質座標。</span><span class="sxs-lookup"><span data-stu-id="6dfc4-121">If zero, the mesh has only a single texture coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="6dfc4-122">*dwUPartialOutSemantic* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6dfc4-122">*dwUPartialOutSemantic* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6dfc4-123">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6dfc4-123">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6dfc4-124">指定類型的輸出語義，通常是 D3DDECLUSAGE 的正切函數，其 \_ 描述將儲存 U 紋理座標的部分衍生。</span><span class="sxs-lookup"><span data-stu-id="6dfc4-124">Specifies the output semantic for the type, typically D3DDECLUSAGE\_TANGENT, that describes where the partial derivative with respect to the U texture coordinate will be stored.</span></span> <span data-ttu-id="6dfc4-125">如果 D3DX \_ 預設值，則不會儲存此部分衍生。</span><span class="sxs-lookup"><span data-stu-id="6dfc4-125">If D3DX\_DEFAULT, then this partial derivative will not be stored.</span></span>

</dd> <dt>

<span data-ttu-id="6dfc4-126">*dwUPartialOutIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6dfc4-126">*dwUPartialOutIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6dfc4-127">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6dfc4-127">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6dfc4-128">指定要在其上儲存部分導數（與 U 材質座標相關）的語義索引。</span><span class="sxs-lookup"><span data-stu-id="6dfc4-128">Specifies the semantic index at which to store the partial derivative with respect to the U texture coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="6dfc4-129">*dwVPartialOutSemantic* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6dfc4-129">*dwVPartialOutSemantic* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6dfc4-130">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6dfc4-130">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6dfc4-131">指定 [**D3DDECLUSAGE**](./d3ddeclusage.md) 類型（通常是 D3DDECLUSAGE \_ BINORMAL），以描述與 V 材質座標相關的部分衍生會儲存在哪裡。</span><span class="sxs-lookup"><span data-stu-id="6dfc4-131">Specifies the [**D3DDECLUSAGE**](./d3ddeclusage.md) type, typically D3DDECLUSAGE\_BINORMAL, that describes where the partial derivative with respect to the V texture coordinate will be stored.</span></span> <span data-ttu-id="6dfc4-132">如果 D3DX \_ 預設值，則不會儲存此部分衍生。</span><span class="sxs-lookup"><span data-stu-id="6dfc4-132">If D3DX\_DEFAULT, then this partial derivative will not be stored.</span></span>

</dd> <dt>

<span data-ttu-id="6dfc4-133">*dwVPartialOutIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6dfc4-133">*dwVPartialOutIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6dfc4-134">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6dfc4-134">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6dfc4-135">指定要在其上儲存部分導數與 V 材質座標相關的語義索引。</span><span class="sxs-lookup"><span data-stu-id="6dfc4-135">Specifies the semantic index at which to store the partial derivative with respect to the V texture coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="6dfc4-136">*dwNormalOutSemantic* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6dfc4-136">*dwNormalOutSemantic* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6dfc4-137">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6dfc4-137">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6dfc4-138">指定輸出正常語義（通常是 D3DDECLUSAGE \_ normal），描述每個頂點的一般向量將儲存在哪個位置。</span><span class="sxs-lookup"><span data-stu-id="6dfc4-138">Specifies the output normal semantic, typically D3DDECLUSAGE\_NORMAL, that describes where the normal vector at each vertex will be stored.</span></span> <span data-ttu-id="6dfc4-139">如果 D3DX \_ 預設值，則不會儲存這個一般向量。</span><span class="sxs-lookup"><span data-stu-id="6dfc4-139">If D3DX\_DEFAULT, then this normal vector will not be stored.</span></span>

</dd> <dt>

<span data-ttu-id="6dfc4-140">*dwNormalOutIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6dfc4-140">*dwNormalOutIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6dfc4-141">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6dfc4-141">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6dfc4-142">指定要在每個頂點上儲存一般向量的語義索引。</span><span class="sxs-lookup"><span data-stu-id="6dfc4-142">Specifies the semantic index at which to store the normal vector at each vertex.</span></span>

</dd> <dt>

<span data-ttu-id="6dfc4-143">*>dwoptions* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6dfc4-143">*dwOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6dfc4-144">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6dfc4-144">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6dfc4-145">一或多個 [**D3DXTANGENT**](./d3dxtangent.md) 旗標的組合，這些旗標會指定正切框架計算選項。</span><span class="sxs-lookup"><span data-stu-id="6dfc4-145">Combination of one or more [**D3DXTANGENT**](./d3dxtangent.md) flags that specify tangent frame computation options.</span></span> <span data-ttu-id="6dfc4-146">如果是 **Null**，則會指定下列選項：</span><span class="sxs-lookup"><span data-stu-id="6dfc4-146">If **NULL**, the following options will be specified:</span></span>



| <span data-ttu-id="6dfc4-147">Description</span><span class="sxs-lookup"><span data-stu-id="6dfc4-147">Description</span></span>                                                                                              | <span data-ttu-id="6dfc4-148">[**D3DXTANGENT**](./d3dxtangent.md) 旗標值</span><span class="sxs-lookup"><span data-stu-id="6dfc4-148">[**D3DXTANGENT**](./d3dxtangent.md) Flag Value</span></span>                               |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="6dfc4-149">以弧度為單位，以弧度為單位來加權標準向量長度，以弧度為單位，subtended 由兩個邊緣離開頂點。</span><span class="sxs-lookup"><span data-stu-id="6dfc4-149">Weight the normal vector length by the angle, in radians, subtended by the two edges leaving the vertex.</span></span> | <span data-ttu-id="6dfc4-150">&！ ( D3DXTANGENT \_ 權數（ \_ 依 \_ 區域 \| D3DXTANGENT \_ 權數 \_ 等於 ) ）</span><span class="sxs-lookup"><span data-stu-id="6dfc4-150">& !( D3DXTANGENT\_WEIGHT\_BY\_AREA \| D3DXTANGENT\_WEIGHT\_EQUAL )</span></span>                |
| <span data-ttu-id="6dfc4-151">從材質座標計算正笛笛卡兒座標 (u，v) 。</span><span class="sxs-lookup"><span data-stu-id="6dfc4-151">Compute orthogonal Cartesian coordinates from texture coordinates (u, v).</span></span> <span data-ttu-id="6dfc4-152">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="6dfc4-152">See Remarks.</span></span>                   | <span data-ttu-id="6dfc4-153">&！ ( 從 \_ \_ \_ \| \_ \_ \_ V ) D3DXTANGENT 的 U D3DXTANGENT ORTHOGONALIZE</span><span class="sxs-lookup"><span data-stu-id="6dfc4-153">& !( D3DXTANGENT\_ORTHOGONALIZE\_FROM\_U \| D3DXTANGENT\_ORTHOGONALIZE\_FROM\_V )</span></span> |
| <span data-ttu-id="6dfc4-154">紋理不是以 u 或 v 方向包裝</span><span class="sxs-lookup"><span data-stu-id="6dfc4-154">Textures are not wrapped in either u or v directions</span></span>                                                     | <span data-ttu-id="6dfc4-155">&！ ( D3DXTANGENT \_ 包裝 \_ UV ) </span><span class="sxs-lookup"><span data-stu-id="6dfc4-155">& !( D3DXTANGENT\_WRAP\_UV )</span></span>                                                      |
| <span data-ttu-id="6dfc4-156">相對於材質座標的部分衍生會正規化。</span><span class="sxs-lookup"><span data-stu-id="6dfc4-156">Partial derivatives with respect to texture coordinates are normalized.</span></span>                                  | <span data-ttu-id="6dfc4-157">&！ ( D3DXTANGENT 不會將 \_ \_ \_ 部分標準化 ) </span><span class="sxs-lookup"><span data-stu-id="6dfc4-157">& !( D3DXTANGENT\_DONT\_NORMALIZE\_PARTIALS )</span></span>                                     |
| <span data-ttu-id="6dfc4-158">頂點會依每個三角形的逆時針方向排序。</span><span class="sxs-lookup"><span data-stu-id="6dfc4-158">Vertices are ordered in a counterclockwise direction around each triangle.</span></span>                               | <span data-ttu-id="6dfc4-159">&！ ( D3DXTANGENT \_ 風的 \_ CW ) </span><span class="sxs-lookup"><span data-stu-id="6dfc4-159">& !( D3DXTANGENT\_WIND\_CW )</span></span>                                                      |
| <span data-ttu-id="6dfc4-160">使用已存在於輸入網格中的每個頂點一般向量。</span><span class="sxs-lookup"><span data-stu-id="6dfc4-160">Use per-vertex normal vectors already present in the input mesh.</span></span>                                         | <span data-ttu-id="6dfc4-161">&！ ( D3DXTANGENT \_ 計算 \_ 法線 ) </span><span class="sxs-lookup"><span data-stu-id="6dfc4-161">& !( D3DXTANGENT\_CALCULATE\_NORMALS )</span></span>                                            |



 

<span data-ttu-id="6dfc4-162">如果 \_ \_ \_ 未設定 [就地產生 D3DXTANGENT]，則會複製輸入網格。</span><span class="sxs-lookup"><span data-stu-id="6dfc4-162">If D3DXTANGENT\_GENERATE\_IN\_PLACE is not set, the input mesh is cloned.</span></span> <span data-ttu-id="6dfc4-163">因此，原始網格必須有足夠的空間來儲存計算的一般向量和部分衍生的資料。</span><span class="sxs-lookup"><span data-stu-id="6dfc4-163">The original mesh must therefore have sufficient space to store the computed normal vector and partial derivative data.</span></span>

</dd> <dt>

<span data-ttu-id="6dfc4-164">*pdwAdjacency* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6dfc4-164">*pdwAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6dfc4-165">類型： **Const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="6dfc4-165">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="6dfc4-166">指標，指向每個臉部的三個 Dword 陣列，為網格中的每個臉部指定三個相鄰專案。</span><span class="sxs-lookup"><span data-stu-id="6dfc4-166">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="6dfc4-167">此陣列中的位元組數目必須至少有3個 \* [**GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* sizeof (DWORD) 。</span><span class="sxs-lookup"><span data-stu-id="6dfc4-167">The number of bytes in this array must be at least 3 \* [**GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* sizeof(DWORD).</span></span>

</dd> <dt>

<span data-ttu-id="6dfc4-168">*fPartialEdgeThreshold* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6dfc4-168">*fPartialEdgeThreshold* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6dfc4-169">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6dfc4-169">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6dfc4-170">指定角度的最大余弦值，而這兩個部分衍生的會被視為不相容。</span><span class="sxs-lookup"><span data-stu-id="6dfc4-170">Specifies the maximum cosine of the angle at which two partial derivatives are deemed to be incompatible with each other.</span></span> <span data-ttu-id="6dfc4-171">如果相鄰三角形中兩個部分衍生的方向的點乘積小於或等於此臨界值，則會分割這些三角形之間共用的頂點。</span><span class="sxs-lookup"><span data-stu-id="6dfc4-171">If the dot product of the direction of the two partial derivatives in adjacent triangles is less than or equal to this threshold, then the vertices shared between these triangles will be split.</span></span>

</dd> <dt>

<span data-ttu-id="6dfc4-172">*fSingularPointThreshold* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6dfc4-172">*fSingularPointThreshold* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6dfc4-173">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6dfc4-173">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6dfc4-174">指定將頂點視為單數的部分衍生的最大幅度。</span><span class="sxs-lookup"><span data-stu-id="6dfc4-174">Specifies the maximum magnitude of a partial derivative at which a vertex will be deemed singular.</span></span> <span data-ttu-id="6dfc4-175">由於多個三角形在具有附近正切框架的點上是事件，但會將彼此的 (（例如球體) 的頂端）全部取消，而部分衍生的範圍將會降低。</span><span class="sxs-lookup"><span data-stu-id="6dfc4-175">As multiple triangles are incident on a point that have nearby tangent frames, but altogether cancel each other out (such as at the top of a sphere), the magnitude of the partial derivative will decrease.</span></span> <span data-ttu-id="6dfc4-176">如果量級小於或等於此臨界值，則會針對包含它的每個三角形分割頂點。</span><span class="sxs-lookup"><span data-stu-id="6dfc4-176">If the magnitude is less than or equal to this threshold, then the vertex will be split for every triangle that contains it.</span></span>

</dd> <dt>

<span data-ttu-id="6dfc4-177">*fNormalEdgeThreshold* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6dfc4-177">*fNormalEdgeThreshold* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6dfc4-178">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6dfc4-178">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6dfc4-179">類似于 fPartialEdgeThreshold，指定在兩個法線之間的角度的最大余弦值，該臨界值超過三角形之間共用的頂點將會被分割。</span><span class="sxs-lookup"><span data-stu-id="6dfc4-179">Similar to fPartialEdgeThreshold, specifies the maximum cosine of the angle between two normals that is a threshold beyond which vertices shared between triangles will be split.</span></span> <span data-ttu-id="6dfc4-180">如果兩個法線的點乘積小於臨界值，共用頂點將會分割，形成相鄰三角形之間的固定邊緣。</span><span class="sxs-lookup"><span data-stu-id="6dfc4-180">If the dot product of the two normals is less than the threshold, the shared vertices will be split, forming a hard edge between neighboring triangles.</span></span> <span data-ttu-id="6dfc4-181">如果點乘積超過閾值，鄰近三角形將會有其法線插補。</span><span class="sxs-lookup"><span data-stu-id="6dfc4-181">If the dot product is more than the threshold, neighboring triangles will have their normals interpolated.</span></span>

</dd> <dt>

<span data-ttu-id="6dfc4-182">*ppMeshOut* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="6dfc4-182">*ppMeshOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6dfc4-183">類型： **[ **ID3DXMesh**](id3dxmesh.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="6dfc4-183">Type: **[**ID3DXMesh**](id3dxmesh.md)\*\***</span></span>

<span data-ttu-id="6dfc4-184">輸出 [**ID3DXMesh**](id3dxmesh.md) 網格物件的指標位址，此物件會接收計算的正切函數、binormal 和一般向量資料。</span><span class="sxs-lookup"><span data-stu-id="6dfc4-184">Address of a pointer to an output [**ID3DXMesh**](id3dxmesh.md) mesh object that receives the computed tangent, binormal, and normal vector data.</span></span>

</dd> <dt>

<span data-ttu-id="6dfc4-185">*ppVertexMapping* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="6dfc4-185">*ppVertexMapping* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6dfc4-186">類型： **[ **ID3DXBuffer**](id3dxbuffer.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="6dfc4-186">Type: **[**ID3DXBuffer**](id3dxbuffer.md)\*\***</span></span>

<span data-ttu-id="6dfc4-187">輸出 [**ID3DXBuffer**](id3dxbuffer.md) 緩衝區物件的指標位址，此緩衝區物件會接收由此方法計算的新頂點與原始頂點的對應。</span><span class="sxs-lookup"><span data-stu-id="6dfc4-187">Address of a pointer to an output [**ID3DXBuffer**](id3dxbuffer.md) buffer object that receives a mapping of new vertices computed by this method to the original vertices.</span></span> <span data-ttu-id="6dfc4-188">緩衝區是 Dword 陣列，其陣列大小定義為 ppMeshOut 中的頂點數目。</span><span class="sxs-lookup"><span data-stu-id="6dfc4-188">The buffer is an array of DWORDs, with the array size defined as the number of vertices in ppMeshOut.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6dfc4-189">傳回值</span><span class="sxs-lookup"><span data-stu-id="6dfc4-189">Return value</span></span>

<span data-ttu-id="6dfc4-190">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6dfc4-190">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6dfc4-191">如果函式成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="6dfc4-191">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="6dfc4-192">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL、D3DXERR \_ INVALIDDATA、E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="6dfc4-192">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="6dfc4-193">備註</span><span class="sxs-lookup"><span data-stu-id="6dfc4-193">Remarks</span></span>

<span data-ttu-id="6dfc4-194">這個函式的簡化版本會以 [**D3DXComputeTangentFrame**](d3dxcomputetangentframe.md)的形式提供。</span><span class="sxs-lookup"><span data-stu-id="6dfc4-194">A simplified version of this function is available as [**D3DXComputeTangentFrame**](d3dxcomputetangentframe.md).</span></span>

<span data-ttu-id="6dfc4-195">每個頂點上計算的一般向量一律會正規化為具有單位長度。</span><span class="sxs-lookup"><span data-stu-id="6dfc4-195">The computed normal vector at each vertex is always normalized to have unit length.</span></span>

<span data-ttu-id="6dfc4-196">適用于計算正笛笛卡兒座標的最穩固解決方案，是不要設定 D3DXTANGENT ORTHOGONALIZE 的旗標， \_ \_ \_ 並 \_ 從 V D3DXTANGENT ORTHOGONALIZE，如此一來，就能 \_ \_ 從紋理座標和 v 來計算正向座標。</span><span class="sxs-lookup"><span data-stu-id="6dfc4-196">The most robust solution for computing orthogonal Cartesian coordinates is to not set flags D3DXTANGENT\_ORTHOGONALIZE\_FROM\_U and D3DXTANGENT\_ORTHOGONALIZE\_FROM\_V, so that orthogonal coordinates are computed from both texture coordinates u and v.</span></span> <span data-ttu-id="6dfc4-197">不過，在此情況下，如果 u 或 v 為零，則函式會 \_ \_ 分別使用 \_ v 或 D3DXTANGENT \_ ORTHOGONALIZE \_ 中 \_ 的 D3DXTANGENT ORTHOGONALIZE 計算正向座標。</span><span class="sxs-lookup"><span data-stu-id="6dfc4-197">However, in this case, if either u or v is zero, then the function will compute orthogonal coordinates using D3DXTANGENT\_ORTHOGONALIZE\_FROM\_V or D3DXTANGENT\_ORTHOGONALIZE\_FROM\_U, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="6dfc4-198">規格需求</span><span class="sxs-lookup"><span data-stu-id="6dfc4-198">Requirements</span></span>



| <span data-ttu-id="6dfc4-199">需求</span><span class="sxs-lookup"><span data-stu-id="6dfc4-199">Requirement</span></span> | <span data-ttu-id="6dfc4-200">值</span><span class="sxs-lookup"><span data-stu-id="6dfc4-200">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6dfc4-201">標頭</span><span class="sxs-lookup"><span data-stu-id="6dfc4-201">Header</span></span><br/>  | <dl> <span data-ttu-id="6dfc4-202"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="6dfc4-202"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="6dfc4-203">程式庫</span><span class="sxs-lookup"><span data-stu-id="6dfc4-203">Library</span></span><br/> | <dl> <span data-ttu-id="6dfc4-204"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="6dfc4-204"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6dfc4-205">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6dfc4-205">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6dfc4-206">網格函數</span><span class="sxs-lookup"><span data-stu-id="6dfc4-206">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="6dfc4-207">**D3DXComputeTangentFrame**</span><span class="sxs-lookup"><span data-stu-id="6dfc4-207">**D3DXComputeTangentFrame**</span></span>](d3dxcomputetangentframe.md)
</dt> </dl>

 

 

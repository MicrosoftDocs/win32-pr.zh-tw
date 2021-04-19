---
description: 網格的計算正切函數、binormal 和一般向量。
ms.assetid: 54edb9a5-440d-4191-a58f-296e5b804e0c
title: 'D3DXComputeTangentFrame 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeTangentFrame
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4b95d8f046499716a2c7972593093dfb409b11f6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106988616"
---
# <a name="d3dxcomputetangentframe-function"></a><span data-ttu-id="e7d2f-103">D3DXComputeTangentFrame 函式</span><span class="sxs-lookup"><span data-stu-id="e7d2f-103">D3DXComputeTangentFrame function</span></span>

<span data-ttu-id="e7d2f-104">網格的計算正切函數、binormal 和一般向量。</span><span class="sxs-lookup"><span data-stu-id="e7d2f-104">Compute tangent, binormal, and normal vectors for a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7d2f-105">語法</span><span class="sxs-lookup"><span data-stu-id="e7d2f-105">Syntax</span></span>


```C++
HRESULT D3DXComputeTangentFrame(
  _In_ ID3DXMesh *pMesh,
  _In_ DWORD     dwOptions
);
```



## <a name="parameters"></a><span data-ttu-id="e7d2f-106">參數</span><span class="sxs-lookup"><span data-stu-id="e7d2f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7d2f-107">*pMesh* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e7d2f-107">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7d2f-108">類型： **[ **ID3DXMesh**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="e7d2f-108">Type: **[**ID3DXMesh**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="e7d2f-109">輸入 [**ID3DXMesh**](id3dxmesh.md) 網格物件的指標。</span><span class="sxs-lookup"><span data-stu-id="e7d2f-109">Pointer to an input [**ID3DXMesh**](id3dxmesh.md) mesh object.</span></span>

</dd> <dt>

<span data-ttu-id="e7d2f-110">*>dwoptions* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e7d2f-110">*dwOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7d2f-111">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e7d2f-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e7d2f-112">一或多個 [**D3DXTANGENT**](./d3dxtangent.md) 旗標的組合。</span><span class="sxs-lookup"><span data-stu-id="e7d2f-112">Combination of one or more [**D3DXTANGENT**](./d3dxtangent.md) flags.</span></span>

<span data-ttu-id="e7d2f-113">使用 **Null** 來指定下列選項：</span><span class="sxs-lookup"><span data-stu-id="e7d2f-113">Use **NULL** to specify the following options:</span></span>

-   <span data-ttu-id="e7d2f-114">以弧度為單位，以弧度為單位來加權標準向量長度，以弧度為單位，subtended 由兩個邊緣離開頂點。</span><span class="sxs-lookup"><span data-stu-id="e7d2f-114">Weight the normal vector length by the angle, in radians, subtended by the two edges leaving the vertex.</span></span>
-   <span data-ttu-id="e7d2f-115">從 UV 材質座標計算正笛笛卡兒座標。</span><span class="sxs-lookup"><span data-stu-id="e7d2f-115">Compute orthogonal Cartesian coordinates from the UV texture coordinates.</span></span>
-   <span data-ttu-id="e7d2f-116">紋理不是以 U 或 V 方向包裝</span><span class="sxs-lookup"><span data-stu-id="e7d2f-116">Textures are not wrapped in either U or V directions</span></span>
-   <span data-ttu-id="e7d2f-117">相對於材質座標的部分衍生會正規化。</span><span class="sxs-lookup"><span data-stu-id="e7d2f-117">Partial derivatives with respect to texture coordinates are normalized.</span></span>
-   <span data-ttu-id="e7d2f-118">頂點會依每個三角形的逆時針方向排序。</span><span class="sxs-lookup"><span data-stu-id="e7d2f-118">Vertices are ordered in a counterclockwise direction around each triangle.</span></span>
-   <span data-ttu-id="e7d2f-119">使用已存在於輸入網格中的每個頂點一般向量。</span><span class="sxs-lookup"><span data-stu-id="e7d2f-119">Use per-vertex normal vectors already present in the input mesh.</span></span>
-   <span data-ttu-id="e7d2f-120">結果會儲存在原始的輸入網格中。</span><span class="sxs-lookup"><span data-stu-id="e7d2f-120">The results will be stored in the original input mesh.</span></span> <span data-ttu-id="e7d2f-121">如果需要建立新的頂點，函式將會失敗。</span><span class="sxs-lookup"><span data-stu-id="e7d2f-121">The function will fail if new vertices need to be created.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7d2f-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="e7d2f-122">Return value</span></span>

<span data-ttu-id="e7d2f-123">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e7d2f-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e7d2f-124">如果函式成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="e7d2f-124">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="e7d2f-125">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL、D3DXERR \_ INVALIDDATA、E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="e7d2f-125">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7d2f-126">備註</span><span class="sxs-lookup"><span data-stu-id="e7d2f-126">Remarks</span></span>

<span data-ttu-id="e7d2f-127">此函式只會使用下列輸入參數來呼叫 [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) ：</span><span class="sxs-lookup"><span data-stu-id="e7d2f-127">This function simply calls [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) with the following input parameters:</span></span>


```
D3DXComputeTangentFrameEx(pMesh, D3DDECLUSAGE_TEXCOORD, 0,   
      D3DDECLUSAGE_BINORMAL, 0, D3DDECLUSAGE_TANGENT, 0, 
      D3DDECLUSAGE_NORMAL, 0, 
      dwOptions | D3DXTANGENT_GENERATE_IN_PLACE,
      NULL, 0.01f, 0.25f, 0.01f, NULL, NULL);
```



<span data-ttu-id="e7d2f-128">藉由群組邊緣和分割頂點，Singularities 會視需要進行處理。</span><span class="sxs-lookup"><span data-stu-id="e7d2f-128">Singularities are handled as required by grouping edges and splitting vertices.</span></span> <span data-ttu-id="e7d2f-129">如果需要分割任何頂點，函數將會失敗。</span><span class="sxs-lookup"><span data-stu-id="e7d2f-129">If any vertices need to be split, the function will fail.</span></span> <span data-ttu-id="e7d2f-130">每個頂點上計算的一般向量一律會正規化為具有單位長度。</span><span class="sxs-lookup"><span data-stu-id="e7d2f-130">The computed normal vector at each vertex is always normalized to have unit length.</span></span>

<span data-ttu-id="e7d2f-131">適用于計算正笛笛卡兒座標的最穩固解決方案，是不要設定 D3DXTANGENT ORTHOGONALIZE 的旗標， \_ \_ \_ 並 \_ \_ 從 V D3DXTANGENT ORTHOGONALIZE \_ ，以便從 UV 材質座標計算正向座標。</span><span class="sxs-lookup"><span data-stu-id="e7d2f-131">The most robust solution for computing orthogonal Cartesian coordinates is to not set flags D3DXTANGENT\_ORTHOGONALIZE\_FROM\_U and D3DXTANGENT\_ORTHOGONALIZE\_FROM\_V, so that orthogonal coordinates are computed from both UV texture coordinates.</span></span> <span data-ttu-id="e7d2f-132">不過，在此情況下，如果 U 或 V 為零，則函式會使用 D3DXTANGENT \_ ORTHOGONALIZE \_ 從 \_ V 或 \_ \_ 從 \_ U 分別 D3DXTANGENT ORTHOGONALIZE 來計算正向座標。</span><span class="sxs-lookup"><span data-stu-id="e7d2f-132">However, in this case, if either U or V is zero, then the function will compute orthogonal coordinates using D3DXTANGENT\_ORTHOGONALIZE\_FROM\_V or D3DXTANGENT\_ORTHOGONALIZE\_FROM\_U respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7d2f-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="e7d2f-133">Requirements</span></span>



| <span data-ttu-id="e7d2f-134">需求</span><span class="sxs-lookup"><span data-stu-id="e7d2f-134">Requirement</span></span> | <span data-ttu-id="e7d2f-135">值</span><span class="sxs-lookup"><span data-stu-id="e7d2f-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e7d2f-136">標頭</span><span class="sxs-lookup"><span data-stu-id="e7d2f-136">Header</span></span><br/>  | <dl> <span data-ttu-id="e7d2f-137"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="e7d2f-137"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="e7d2f-138">程式庫</span><span class="sxs-lookup"><span data-stu-id="e7d2f-138">Library</span></span><br/> | <dl> <span data-ttu-id="e7d2f-139"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="e7d2f-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e7d2f-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e7d2f-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7d2f-141">網格函數</span><span class="sxs-lookup"><span data-stu-id="e7d2f-141">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="e7d2f-142">**D3DXComputeTangentFrameEx**</span><span class="sxs-lookup"><span data-stu-id="e7d2f-142">**D3DXComputeTangentFrameEx**</span></span>](d3dxcomputetangentframeex.md)
</dt> <dt>

[<span data-ttu-id="e7d2f-143">**D3DXTANGENT**</span><span class="sxs-lookup"><span data-stu-id="e7d2f-143">**D3DXTANGENT**</span></span>](./d3dxtangent.md)
</dt> </dl>

 

 

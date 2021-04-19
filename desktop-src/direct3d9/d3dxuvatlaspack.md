---
description: Pack 網狀將資料分割成塔。
ms.assetid: 4da85626-c36c-44d9-990b-0db80ed04423
title: 'D3DXUVAtlasPack 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXUVAtlasPack
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 31de326160120fe14a71841cb5f2d18e1c8d4e57
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106976479"
---
# <a name="d3dxuvatlaspack-function"></a><span data-ttu-id="dde45-103">D3DXUVAtlasPack 函式</span><span class="sxs-lookup"><span data-stu-id="dde45-103">D3DXUVAtlasPack function</span></span>

<span data-ttu-id="dde45-104">Pack 網狀將資料分割成塔。</span><span class="sxs-lookup"><span data-stu-id="dde45-104">Pack mesh partitioning data into an atlas.</span></span>

## <a name="syntax"></a><span data-ttu-id="dde45-105">語法</span><span class="sxs-lookup"><span data-stu-id="dde45-105">Syntax</span></span>


```C++
HRESULT D3DXUVAtlasPack(
  _In_       LPD3DXMESH      pMesh,
  _In_       UINT            dwWidth,
  _In_       UINT            dwHeight,
  _In_       FLOAT           fGutter,
  _In_       DWORD           dwTextureIndex,
       const DWORD           *pdwPartitionResultAdjacency,
  _In_       LPD3DXUVATLASCB pCallback,
  _In_       FLOAT           fCallbackFrequency,
  _In_       LPVOID          pUserContent,
  _In_       DWORD           dwOptions,
  _In_       LPD3DXBUFFER    pFacePartitioning
);
```



## <a name="parameters"></a><span data-ttu-id="dde45-106">參數</span><span class="sxs-lookup"><span data-stu-id="dde45-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dde45-107">*pMesh* \[在\]</span><span class="sxs-lookup"><span data-stu-id="dde45-107">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dde45-108">類型： **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="dde45-108">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="dde45-109">輸入網格 (的指標，請參閱 [**ID3DXMesh**](id3dxmesh.md)) ，其中包含用來計算塔的物件幾何。</span><span class="sxs-lookup"><span data-stu-id="dde45-109">Pointer to an input mesh (see [**ID3DXMesh**](id3dxmesh.md)) which contains the object geometry for calculating the atlas.</span></span> <span data-ttu-id="dde45-110">網格至少必須包含位置資料和2D 材質座標。</span><span class="sxs-lookup"><span data-stu-id="dde45-110">At a minimum, the mesh must contain position data and 2D texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="dde45-111">*dwWidth* \[在\]</span><span class="sxs-lookup"><span data-stu-id="dde45-111">*dwWidth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dde45-112">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dde45-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dde45-113">材質寬度。</span><span class="sxs-lookup"><span data-stu-id="dde45-113">Texture width.</span></span>

</dd> <dt>

<span data-ttu-id="dde45-114">*dwHeight* \[在\]</span><span class="sxs-lookup"><span data-stu-id="dde45-114">*dwHeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dde45-115">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dde45-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dde45-116">材質高度。</span><span class="sxs-lookup"><span data-stu-id="dde45-116">Texture height.</span></span>

</dd> <dt>

<span data-ttu-id="dde45-117">*fGutter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="dde45-117">*fGutter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dde45-118">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dde45-118">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dde45-119">塔上兩個圖表之間的最小距離（以材質）。</span><span class="sxs-lookup"><span data-stu-id="dde45-119">The minimum distance, in texels, between two charts on the atlas.</span></span> <span data-ttu-id="dde45-120">裝訂邊一律會以寬度調整;因此，如果在512x512 材質上使用2.5 的裝訂邊，則兩個圖表之間的最小距離為 2.5/512.0 材質。</span><span class="sxs-lookup"><span data-stu-id="dde45-120">The gutter is always scaled by the width; so, if a gutter of 2.5 is used on a 512x512 texture, then the minimum distance between two charts is 2.5 / 512.0 texels.</span></span>

</dd> <dt>

<span data-ttu-id="dde45-121">*dwTextureIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="dde45-121">*dwTextureIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dde45-122">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dde45-122">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dde45-123">以零為基礎的材質座標索引，識別要使用的材質座標集。</span><span class="sxs-lookup"><span data-stu-id="dde45-123">Zero-based texture coordinate index that identifies which set of texture coordinates to use.</span></span>

</dd> <dt>

<span data-ttu-id="dde45-124">*pdwPartitionResultAdjacency*</span><span class="sxs-lookup"><span data-stu-id="dde45-124">*pdwPartitionResultAdjacency*</span></span> 
</dt> <dd>

<span data-ttu-id="dde45-125">類型： **Const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="dde45-125">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="dde45-126">指標，指向每個臉部的三個 Dword 陣列，為網格中的每個臉部指定三個相鄰專案。</span><span class="sxs-lookup"><span data-stu-id="dde45-126">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="dde45-127">它應該衍生自 [**D3DXUVAtlasPartition**](d3dxuvatlaspartition.md)所傳回的 ppPartitionResultAdjacency。</span><span class="sxs-lookup"><span data-stu-id="dde45-127">It should be derived from the ppPartitionResultAdjacency returned from [**D3DXUVAtlasPartition**](d3dxuvatlaspartition.md).</span></span> <span data-ttu-id="dde45-128">此值不能是 **Null**，因為 Pack 必須知道資料分割步驟中的圖表剪下的位置，才能找出每個圖表的邊緣。</span><span class="sxs-lookup"><span data-stu-id="dde45-128">This value cannot be **NULL**, because Pack needs to know where charts were cut in the partition step in order to find the edges of each chart.</span></span>

</dd> <dt>

<span data-ttu-id="dde45-129">*pCallback* \[在\]</span><span class="sxs-lookup"><span data-stu-id="dde45-129">*pCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dde45-130">類型： **[LPD3DXU加值稅LASCB](lpd3dxuvatlascb.md)**</span><span class="sxs-lookup"><span data-stu-id="dde45-130">Type: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span></span>

<span data-ttu-id="dde45-131">回呼函式的指標 (查看適用于監視進度的 [LPD3DXU加值稅LASCB](lpd3dxuvatlascb.md)) 。</span><span class="sxs-lookup"><span data-stu-id="dde45-131">A pointer to a callback function (see [LPD3DXUVATLASCB](lpd3dxuvatlascb.md)) that is useful for monitoring progress.</span></span>

</dd> <dt>

<span data-ttu-id="dde45-132">*fCallbackFrequency* \[在\]</span><span class="sxs-lookup"><span data-stu-id="dde45-132">*fCallbackFrequency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dde45-133">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dde45-133">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dde45-134">指定 D3DX 將呼叫回呼的頻率;合理的預設值是 0.0001 f。</span><span class="sxs-lookup"><span data-stu-id="dde45-134">Specify how often D3DX will call the callback; a reasonable default value is 0.0001f.</span></span>

</dd> <dt>

<span data-ttu-id="dde45-135">*pUserContent* \[在\]</span><span class="sxs-lookup"><span data-stu-id="dde45-135">*pUserContent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dde45-136">類型： **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dde45-136">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dde45-137">要傳回給回呼函式的 void 指標。</span><span class="sxs-lookup"><span data-stu-id="dde45-137">A void pointer to be passed back to the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="dde45-138">*>dwoptions* \[在\]</span><span class="sxs-lookup"><span data-stu-id="dde45-138">*dwOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dde45-139">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dde45-139">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dde45-140">此選項參數目前為保留。</span><span class="sxs-lookup"><span data-stu-id="dde45-140">This options parameter is currently reserved.</span></span>

</dd> <dt>

<span data-ttu-id="dde45-141">*pFacePartitioning* \[在\]</span><span class="sxs-lookup"><span data-stu-id="dde45-141">*pFacePartitioning* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dde45-142">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="dde45-142">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)**</span></span>

<span data-ttu-id="dde45-143">[**ID3DXBuffer**](id3dxbuffer.md)的指標，其中包含最終臉部資料分割的陣列。</span><span class="sxs-lookup"><span data-stu-id="dde45-143">A pointer to an [**ID3DXBuffer**](id3dxbuffer.md) containing the array of the final face-partitioning.</span></span> <span data-ttu-id="dde45-144">每個元素都包含每個臉部一個 DWORD。</span><span class="sxs-lookup"><span data-stu-id="dde45-144">Each element contains one DWORD per face.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dde45-145">傳回值</span><span class="sxs-lookup"><span data-stu-id="dde45-145">Return value</span></span>

<span data-ttu-id="dde45-146">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="dde45-146">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="dde45-147">如果函式成功，則傳回值為「D3D 正常」， \_ 否則值為 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="dde45-147">If the function succeeds, the return value is D3D\_OK; otherwise, the value is D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="dde45-148">規格需求</span><span class="sxs-lookup"><span data-stu-id="dde45-148">Requirements</span></span>



| <span data-ttu-id="dde45-149">需求</span><span class="sxs-lookup"><span data-stu-id="dde45-149">Requirement</span></span> | <span data-ttu-id="dde45-150">值</span><span class="sxs-lookup"><span data-stu-id="dde45-150">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dde45-151">標頭</span><span class="sxs-lookup"><span data-stu-id="dde45-151">Header</span></span><br/>  | <dl> <span data-ttu-id="dde45-152"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="dde45-152"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="dde45-153">程式庫</span><span class="sxs-lookup"><span data-stu-id="dde45-153">Library</span></span><br/> | <dl> <span data-ttu-id="dde45-154"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="dde45-154"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="dde45-155">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dde45-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dde45-156">UVAtlas 函式</span><span class="sxs-lookup"><span data-stu-id="dde45-156">UVAtlas Functions</span></span>](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> </dl>

 

 

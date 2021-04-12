---
description: 搭配預先計算 radiance transfer 的頂點版本壓縮結果使用 (PRT) 模擬器。
ms.assetid: 0ec28b8c-5010-48a4-8e45-d7f9aa08185f
title: 'D3DXSHPRTCompSuperCluster 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHPRTCompSuperCluster
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1daf25dddfaf738ecc2fed9605429a19170177ed
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322860"
---
# <a name="d3dxshprtcompsupercluster-function"></a><span data-ttu-id="0cfea-103">D3DXSHPRTCompSuperCluster 函式</span><span class="sxs-lookup"><span data-stu-id="0cfea-103">D3DXSHPRTCompSuperCluster function</span></span>

<span data-ttu-id="0cfea-104">搭配預先計算 radiance transfer 的頂點版本壓縮結果使用 (PRT) 模擬器。</span><span class="sxs-lookup"><span data-stu-id="0cfea-104">Used with compressed results of the vertex version of the precomputed radiance transfer (PRT) simulator.</span></span> <span data-ttu-id="0cfea-105">產生 "superclusters"，這是可在相同繪製呼叫中繪製的群集群組。</span><span class="sxs-lookup"><span data-stu-id="0cfea-105">Generates "superclusters," which are groups of clusters that can be drawn in the same draw call.</span></span> <span data-ttu-id="0cfea-106">將過度繪製降至最低的貪婪演算法會用來將叢集分組。</span><span class="sxs-lookup"><span data-stu-id="0cfea-106">A greedy algorithm that minimizes overdraw is used to group the clusters.</span></span>

## <a name="syntax"></a><span data-ttu-id="0cfea-107">語法</span><span class="sxs-lookup"><span data-stu-id="0cfea-107">Syntax</span></span>


```C++
HRESULT D3DXSHPRTCompSuperCluster(
  _In_    UINT       *pClusterIDs,
  _In_    LPD3DXMESH pScene,
  _In_    UINT       MaxNumClusters,
  _In_    UINT       NumClusters,
  _Inout_ UINT       *pSClusterIDs,
  _Inout_ UINT       *pNumSCs
);
```



## <a name="parameters"></a><span data-ttu-id="0cfea-108">參數</span><span class="sxs-lookup"><span data-stu-id="0cfea-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0cfea-109">*pClusterIDs* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0cfea-109">*pClusterIDs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cfea-110">類型： **[ **UINT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="0cfea-110">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0cfea-111">NumVerts 叢集識別碼的指標 (從壓縮的緩衝區解壓縮。 ) </span><span class="sxs-lookup"><span data-stu-id="0cfea-111">Pointer to a NumVerts cluster IDs (extracted from a compressed buffer.)</span></span>

</dd> <dt>

<span data-ttu-id="0cfea-112">*pScene* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0cfea-112">*pScene* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cfea-113">類型： **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="0cfea-113">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="0cfea-114">表示傳遞給模擬器之複合場景的網格指標。</span><span class="sxs-lookup"><span data-stu-id="0cfea-114">Pointer to a mesh that represents composite scene passed to the simulator.</span></span> <span data-ttu-id="0cfea-115">請參閱 [**ID3DXMesh**](id3dxmesh.md)。</span><span class="sxs-lookup"><span data-stu-id="0cfea-115">See [**ID3DXMesh**](id3dxmesh.md).</span></span>

</dd> <dt>

<span data-ttu-id="0cfea-116">*MaxNumClusters* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0cfea-116">*MaxNumClusters* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cfea-117">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0cfea-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0cfea-118">每個超級叢集配置的最大叢集數。</span><span class="sxs-lookup"><span data-stu-id="0cfea-118">Maximum number of clusters allocated per super cluster.</span></span>

</dd> <dt>

<span data-ttu-id="0cfea-119">*NumClusters* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0cfea-119">*NumClusters* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cfea-120">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0cfea-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0cfea-121">在模擬器中計算的群集數目。</span><span class="sxs-lookup"><span data-stu-id="0cfea-121">Number of clusters computed in the simulator.</span></span>

</dd> <dt>

<span data-ttu-id="0cfea-122">*pSClusterIDs* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="0cfea-122">*pSClusterIDs* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0cfea-123">類型： **[ **UINT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="0cfea-123">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0cfea-124">長度 *NumClusters* 陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="0cfea-124">Pointer to an array of length *NumClusters*.</span></span> <span data-ttu-id="0cfea-125">包含指派給對應叢集之超級叢集的索引。</span><span class="sxs-lookup"><span data-stu-id="0cfea-125">Contains the index of the super cluster to which the corresponding cluster was assigned.</span></span>

</dd> <dt>

<span data-ttu-id="0cfea-126">*pNumSCs* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="0cfea-126">*pNumSCs* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0cfea-127">類型： **[ **UINT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="0cfea-127">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0cfea-128">配置的超級叢集數目。</span><span class="sxs-lookup"><span data-stu-id="0cfea-128">Number of super clusters allocated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0cfea-129">傳回值</span><span class="sxs-lookup"><span data-stu-id="0cfea-129">Return value</span></span>

<span data-ttu-id="0cfea-130">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0cfea-130">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0cfea-131">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="0cfea-131">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="0cfea-132">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL、D3DXERR \_ INVALIDDATA、E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="0cfea-132">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="0cfea-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="0cfea-133">Requirements</span></span>



| <span data-ttu-id="0cfea-134">需求</span><span class="sxs-lookup"><span data-stu-id="0cfea-134">Requirement</span></span> | <span data-ttu-id="0cfea-135">值</span><span class="sxs-lookup"><span data-stu-id="0cfea-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0cfea-136">標頭</span><span class="sxs-lookup"><span data-stu-id="0cfea-136">Header</span></span><br/>  | <dl> <span data-ttu-id="0cfea-137"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="0cfea-137"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="0cfea-138">程式庫</span><span class="sxs-lookup"><span data-stu-id="0cfea-138">Library</span></span><br/> | <dl> <span data-ttu-id="0cfea-139"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="0cfea-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0cfea-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0cfea-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cfea-141">預先計算 Radiance 傳送函式</span><span class="sxs-lookup"><span data-stu-id="0cfea-141">Precomputed Radiance Transfer Functions</span></span>](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> </dl>

 

 

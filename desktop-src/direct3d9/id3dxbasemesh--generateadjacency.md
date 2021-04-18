---
description: 產生網格邊緣清單以及共用每個邊緣的臉部清單。
ms.assetid: 9d52290f-1c9e-43a7-b239-35cd54e36466
title: 'ID3DXBaseMesh：： GenerateAdjacency 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GenerateAdjacency
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b5b1d304878a4977bb14d6ef98ad7256b6c3181f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104386492"
---
# <a name="id3dxbasemeshgenerateadjacency-method"></a><span data-ttu-id="c408c-103">ID3DXBaseMesh：： GenerateAdjacency 方法</span><span class="sxs-lookup"><span data-stu-id="c408c-103">ID3DXBaseMesh::GenerateAdjacency method</span></span>

<span data-ttu-id="c408c-104">產生網格邊緣清單以及共用每個邊緣的臉部清單。</span><span class="sxs-lookup"><span data-stu-id="c408c-104">Generate a list of mesh edges, as well as a list of faces that share each edge.</span></span>

## <a name="syntax"></a><span data-ttu-id="c408c-105">語法</span><span class="sxs-lookup"><span data-stu-id="c408c-105">Syntax</span></span>


```C++
HRESULT GenerateAdjacency(
  [in] FLOAT Epsilon,
  [in] DWORD *pAdjacency
);
```



## <a name="parameters"></a><span data-ttu-id="c408c-106">參數</span><span class="sxs-lookup"><span data-stu-id="c408c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c408c-107">*Epsilon* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c408c-107">*Epsilon* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c408c-108">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c408c-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c408c-109">指定在位置中差異小於 epsilon 的頂點應視為重合。</span><span class="sxs-lookup"><span data-stu-id="c408c-109">Specifies that vertices that differ in position by less than epsilon should be treated as coincident.</span></span>

</dd> <dt>

<span data-ttu-id="c408c-110">*pAdjacency* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c408c-110">*pAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c408c-111">類型： **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="c408c-111">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="c408c-112">要填入相鄰臉部索引的每個臉部陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="c408c-112">Pointer to an array of three DWORDs per face to be filled with the indices of adjacent faces.</span></span> <span data-ttu-id="c408c-113">此陣列中的位元組數目必須至少為 3 \* [**ID3DXBaseMesh：： GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* sizeof (DWORD) 。</span><span class="sxs-lookup"><span data-stu-id="c408c-113">The number of bytes in this array must be at least 3 \* [**ID3DXBaseMesh::GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* sizeof(DWORD).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c408c-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="c408c-114">Return value</span></span>

<span data-ttu-id="c408c-115">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c408c-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c408c-116">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="c408c-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c408c-117">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="c408c-117">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="c408c-118">備註</span><span class="sxs-lookup"><span data-stu-id="c408c-118">Remarks</span></span>

<span data-ttu-id="c408c-119">在應用程式產生網格的相鄰資訊之後，可以將網格資料優化，以提升繪製效能。</span><span class="sxs-lookup"><span data-stu-id="c408c-119">After an application generates adjacency information for a mesh, the mesh data can be optimized for better drawing performance.</span></span>

<span data-ttu-id="c408c-120">相鄰緩衝區中的專案順序是由索引緩衝區中的頂點索引順序所決定。</span><span class="sxs-lookup"><span data-stu-id="c408c-120">The order of the entries in the adjacency buffer is determined by the order of the vertex indices in the index buffer.</span></span> <span data-ttu-id="c408c-121">連續的三角形0一律對應至角落0和1的索引之間的邊緣。</span><span class="sxs-lookup"><span data-stu-id="c408c-121">The adjacent triangle 0 always corresponds to the edge between the indices of the corners 0 and 1.</span></span> <span data-ttu-id="c408c-122">連續的三角形1一律對應至角落1和2的索引之間的邊緣，連續的三角形2則對應至角落2與0的索引之間的邊緣。</span><span class="sxs-lookup"><span data-stu-id="c408c-122">The adjacent triangle 1 always corresponds to the edge between the indices of the corners 1 and 2 while the adjacent triangle 2 corresponds to the edge between the indices of the corners 2 and 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="c408c-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="c408c-123">Requirements</span></span>



| <span data-ttu-id="c408c-124">需求</span><span class="sxs-lookup"><span data-stu-id="c408c-124">Requirement</span></span> | <span data-ttu-id="c408c-125">值</span><span class="sxs-lookup"><span data-stu-id="c408c-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c408c-126">標頭</span><span class="sxs-lookup"><span data-stu-id="c408c-126">Header</span></span><br/>  | <dl> <span data-ttu-id="c408c-127"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="c408c-127"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="c408c-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="c408c-128">Library</span></span><br/> | <dl> <span data-ttu-id="c408c-129"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c408c-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c408c-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c408c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c408c-131">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="c408c-131">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> <dt>

[<span data-ttu-id="c408c-132">**ID3DXMesh：： Optimize**</span><span class="sxs-lookup"><span data-stu-id="c408c-132">**ID3DXMesh::Optimize**</span></span>](id3dxmesh--optimize.md)
</dt> <dt>

[<span data-ttu-id="c408c-133">**ID3DXMesh::OptimizeInplace**</span><span class="sxs-lookup"><span data-stu-id="c408c-133">**ID3DXMesh::OptimizeInplace**</span></span>](id3dxmesh--optimizeinplace.md)
</dt> </dl>

 

 

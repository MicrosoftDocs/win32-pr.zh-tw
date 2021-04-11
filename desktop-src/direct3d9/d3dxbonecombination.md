---
description: 描述具有相同屬性和骨骼組合的網格子集。
ms.assetid: e6a4b3bb-d28d-44c2-a6df-f60f0412a70e
title: 'D3DXBONECOMBINATION 結構 (D3dx9mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXBONECOMBINATION
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 3553ba37d0d9376fa5912143fb58849f03c5a83a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104035369"
---
# <a name="d3dxbonecombination-structure"></a><span data-ttu-id="f4d6b-103">D3DXBONECOMBINATION 結構</span><span class="sxs-lookup"><span data-stu-id="f4d6b-103">D3DXBONECOMBINATION structure</span></span>

<span data-ttu-id="f4d6b-104">描述具有相同屬性和骨骼組合的網格子集。</span><span class="sxs-lookup"><span data-stu-id="f4d6b-104">Describes a subset of the mesh that has the same attribute and bone combination.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4d6b-105">語法</span><span class="sxs-lookup"><span data-stu-id="f4d6b-105">Syntax</span></span>


```C++
typedef struct D3DXBONECOMBINATION {
  DWORD AttribId;
  DWORD FaceStart;
  DWORD FaceCount;
  DWORD VertexStart;
  DWORD VertexCount;
  DWORD *BoneId;
} D3DXBONECOMBINATION, *LPD3DXBONECOMBINATION;
```



## <a name="members"></a><span data-ttu-id="f4d6b-106">成員</span><span class="sxs-lookup"><span data-stu-id="f4d6b-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="f4d6b-107">**AttribId**</span><span class="sxs-lookup"><span data-stu-id="f4d6b-107">**AttribId**</span></span>
</dt> <dd>

<span data-ttu-id="f4d6b-108">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f4d6b-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f4d6b-109">屬性資料表識別碼。</span><span class="sxs-lookup"><span data-stu-id="f4d6b-109">Attribute table identifier.</span></span>

</dd> <dt>

<span data-ttu-id="f4d6b-110">**FaceStart**</span><span class="sxs-lookup"><span data-stu-id="f4d6b-110">**FaceStart**</span></span>
</dt> <dd>

<span data-ttu-id="f4d6b-111">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f4d6b-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f4d6b-112">開始臉部。</span><span class="sxs-lookup"><span data-stu-id="f4d6b-112">Starting face.</span></span>

</dd> <dt>

<span data-ttu-id="f4d6b-113">**FaceCount**</span><span class="sxs-lookup"><span data-stu-id="f4d6b-113">**FaceCount**</span></span>
</dt> <dd>

<span data-ttu-id="f4d6b-114">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f4d6b-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f4d6b-115">臉部計數。</span><span class="sxs-lookup"><span data-stu-id="f4d6b-115">Face count.</span></span>

</dd> <dt>

<span data-ttu-id="f4d6b-116">**VertexStart**</span><span class="sxs-lookup"><span data-stu-id="f4d6b-116">**VertexStart**</span></span>
</dt> <dd>

<span data-ttu-id="f4d6b-117">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f4d6b-117">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f4d6b-118">正在啟動頂點。</span><span class="sxs-lookup"><span data-stu-id="f4d6b-118">Starting vertex.</span></span>

</dd> <dt>

<span data-ttu-id="f4d6b-119">**VertexCount**</span><span class="sxs-lookup"><span data-stu-id="f4d6b-119">**VertexCount**</span></span>
</dt> <dd>

<span data-ttu-id="f4d6b-120">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f4d6b-120">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f4d6b-121">頂點計數。</span><span class="sxs-lookup"><span data-stu-id="f4d6b-121">Vertex count.</span></span>

</dd> <dt>

<span data-ttu-id="f4d6b-122">**BoneId**</span><span class="sxs-lookup"><span data-stu-id="f4d6b-122">**BoneId**</span></span>
</dt> <dd>

<span data-ttu-id="f4d6b-123">類型： **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="f4d6b-123">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

</dd> <dd>

<span data-ttu-id="f4d6b-124">值陣列的指標，可識別可在單一繪圖呼叫中繪製的每個骨骼。</span><span class="sxs-lookup"><span data-stu-id="f4d6b-124">Pointer to an array of values that identify each of the bones that can be drawn in a single drawing call.</span></span> <span data-ttu-id="f4d6b-125">請注意，陣列的長度可以是可變長度，以容納 [**ConvertToIndexedBlendedMesh**](id3dxskininfo--converttoindexedblendedmesh.md)的可變長度骨骼組合。</span><span class="sxs-lookup"><span data-stu-id="f4d6b-125">Note that the array can be of variable length to accommodate variable length bone combinations of [**ConvertToIndexedBlendedMesh**](id3dxskininfo--converttoindexedblendedmesh.md).</span></span>

<span data-ttu-id="f4d6b-126">陣列的大小會根據所產生的網狀架構類型而有所不同。</span><span class="sxs-lookup"><span data-stu-id="f4d6b-126">The size of the array varies based on the type of mesh generated.</span></span> <span data-ttu-id="f4d6b-127">非索引的網狀陣列大小等於 [**ConvertToBlendedMesh**](id3dxskininfo--converttoblendedmesh.md)) 中每個頂點 (pMaxVertexInfl 的加權數目。</span><span class="sxs-lookup"><span data-stu-id="f4d6b-127">A non-indexed mesh array size is equal to the number of weights per vertex (pMaxVertexInfl in [**ConvertToBlendedMesh**](id3dxskininfo--converttoblendedmesh.md)).</span></span> <span data-ttu-id="f4d6b-128">索引的網狀陣列大小等於 [**ConvertToIndexedBlendedMesh**](id3dxskininfo--converttoindexedblendedmesh.md)) 中 (paletteSize 的骨骼矩陣調色板專案數目。</span><span class="sxs-lookup"><span data-stu-id="f4d6b-128">An indexed mesh array size is equal to the number of bone matrix palette entries (paletteSize in [**ConvertToIndexedBlendedMesh**](id3dxskininfo--converttoindexedblendedmesh.md)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f4d6b-129">備註</span><span class="sxs-lookup"><span data-stu-id="f4d6b-129">Remarks</span></span>

<span data-ttu-id="f4d6b-130">**D3DXBONECOMBINATION** 所描述之網格的子集可以在單一繪圖呼叫中轉譯。</span><span class="sxs-lookup"><span data-stu-id="f4d6b-130">The subset of the mesh described by **D3DXBONECOMBINATION** can be rendered in a single drawing call.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4d6b-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="f4d6b-131">Requirements</span></span>



| <span data-ttu-id="f4d6b-132">需求</span><span class="sxs-lookup"><span data-stu-id="f4d6b-132">Requirement</span></span> | <span data-ttu-id="f4d6b-133">值</span><span class="sxs-lookup"><span data-stu-id="f4d6b-133">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f4d6b-134">標頭</span><span class="sxs-lookup"><span data-stu-id="f4d6b-134">Header</span></span><br/> | <dl> <span data-ttu-id="f4d6b-135"><dt>D3dx9mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="f4d6b-135"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4d6b-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f4d6b-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4d6b-137">D3DX 結構</span><span class="sxs-lookup"><span data-stu-id="f4d6b-137">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 

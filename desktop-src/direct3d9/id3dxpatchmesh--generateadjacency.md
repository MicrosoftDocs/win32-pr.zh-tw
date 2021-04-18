---
description: 產生網格邊緣清單以及共用每個邊緣的修補程式。
ms.assetid: 024528c0-2c0d-4448-9b38-05cf8d6ffc63
title: 'ID3DXPatchMesh：： GenerateAdjacency 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.GenerateAdjacency
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 68de2a77b9d27391c57ec299ceb87d29166ee248
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104386428"
---
# <a name="id3dxpatchmeshgenerateadjacency-method"></a><span data-ttu-id="d5c77-103">ID3DXPatchMesh：： GenerateAdjacency 方法</span><span class="sxs-lookup"><span data-stu-id="d5c77-103">ID3DXPatchMesh::GenerateAdjacency method</span></span>

<span data-ttu-id="d5c77-104">產生網格邊緣清單以及共用每個邊緣的修補程式。</span><span class="sxs-lookup"><span data-stu-id="d5c77-104">Generate a list of mesh edges and the patches that share each edge.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5c77-105">語法</span><span class="sxs-lookup"><span data-stu-id="d5c77-105">Syntax</span></span>


```C++
HRESULT GenerateAdjacency(
  [in] FLOAT fTolerance
);
```



## <a name="parameters"></a><span data-ttu-id="d5c77-106">參數</span><span class="sxs-lookup"><span data-stu-id="d5c77-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5c77-107">*fTolerance* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d5c77-107">*fTolerance* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5c77-108">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d5c77-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d5c77-109">指定在位置中差異小於容錯的頂點應視為重合。</span><span class="sxs-lookup"><span data-stu-id="d5c77-109">Specifies that vertices that differ in position by less than the tolerance should be treated as coincident.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5c77-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="d5c77-110">Return value</span></span>

<span data-ttu-id="d5c77-111">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d5c77-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d5c77-112">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="d5c77-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d5c77-113">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="d5c77-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5c77-114">備註</span><span class="sxs-lookup"><span data-stu-id="d5c77-114">Remarks</span></span>

<span data-ttu-id="d5c77-115">在應用程式產生網格的相鄰資訊之後，可以將網格資料優化，以提升繪製效能。</span><span class="sxs-lookup"><span data-stu-id="d5c77-115">After an application generates adjacency information for a mesh, the mesh data can be optimized for better drawing performance.</span></span> <span data-ttu-id="d5c77-116">這個方法會判斷哪些修補程式在提供的容錯) 內 (相鄰。</span><span class="sxs-lookup"><span data-stu-id="d5c77-116">This method determines which patches are adjacent (within the provided tolerance).</span></span> <span data-ttu-id="d5c77-117">這項資訊會在內部使用，以優化鑲嵌式。</span><span class="sxs-lookup"><span data-stu-id="d5c77-117">This information is used internally to optimize tessellation.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5c77-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="d5c77-118">Requirements</span></span>



| <span data-ttu-id="d5c77-119">需求</span><span class="sxs-lookup"><span data-stu-id="d5c77-119">Requirement</span></span> | <span data-ttu-id="d5c77-120">值</span><span class="sxs-lookup"><span data-stu-id="d5c77-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d5c77-121">標頭</span><span class="sxs-lookup"><span data-stu-id="d5c77-121">Header</span></span><br/>  | <dl> <span data-ttu-id="d5c77-122"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="d5c77-122"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="d5c77-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="d5c77-123">Library</span></span><br/> | <dl> <span data-ttu-id="d5c77-124"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d5c77-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d5c77-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d5c77-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5c77-126">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="d5c77-126">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> <dt>

[<span data-ttu-id="d5c77-127">**ID3DXPatchMesh：： Optimize**</span><span class="sxs-lookup"><span data-stu-id="d5c77-127">**ID3DXPatchMesh::Optimize**</span></span>](id3dxpatchmesh--optimize.md)
</dt> </dl>

 

 

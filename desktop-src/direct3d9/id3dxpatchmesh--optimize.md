---
description: 將修補程式網格優化以進行有效率的鑲嵌。
ms.assetid: 0049e649-5fe5-45b4-9b09-14b7f99b4988
title: 'ID3DXPatchMesh：： Optimize 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.Optimize
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6fa66aadd0ef1f9f9f65747694fc311f80172449
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946262"
---
# <a name="id3dxpatchmeshoptimize-method"></a><span data-ttu-id="2de1b-103">ID3DXPatchMesh：： Optimize 方法</span><span class="sxs-lookup"><span data-stu-id="2de1b-103">ID3DXPatchMesh::Optimize method</span></span>

<span data-ttu-id="2de1b-104">將修補程式網格優化以進行有效率的鑲嵌。</span><span class="sxs-lookup"><span data-stu-id="2de1b-104">Optimizes the patch mesh for efficient tessellation.</span></span>

## <a name="syntax"></a><span data-ttu-id="2de1b-105">語法</span><span class="sxs-lookup"><span data-stu-id="2de1b-105">Syntax</span></span>


```C++
HRESULT Optimize(
  [in] DWORD Flags
);
```



## <a name="parameters"></a><span data-ttu-id="2de1b-106">參數</span><span class="sxs-lookup"><span data-stu-id="2de1b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2de1b-107">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="2de1b-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2de1b-108">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2de1b-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2de1b-109">目前未使用。</span><span class="sxs-lookup"><span data-stu-id="2de1b-109">Currently unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2de1b-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="2de1b-110">Return value</span></span>

<span data-ttu-id="2de1b-111">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2de1b-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2de1b-112">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="2de1b-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="2de1b-113">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，D3DXERR \_ CANNOTATTRSORT。</span><span class="sxs-lookup"><span data-stu-id="2de1b-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_CANNOTATTRSORT.</span></span>

## <a name="remarks"></a><span data-ttu-id="2de1b-114">備註</span><span class="sxs-lookup"><span data-stu-id="2de1b-114">Remarks</span></span>

<span data-ttu-id="2de1b-115">在應用程式產生網格的相鄰資訊之後，可以將網格資料優化 (重新排列) ，以提升繪製效能。</span><span class="sxs-lookup"><span data-stu-id="2de1b-115">After an application generates adjacency information for a mesh, the mesh data can be optimized (reordered) for better drawing performance.</span></span> <span data-ttu-id="2de1b-116">這個方法會判斷哪些修補程式在提供的容錯) 內 (相鄰。</span><span class="sxs-lookup"><span data-stu-id="2de1b-116">This method determines which patches are adjacent (within the provided tolerance).</span></span>

<span data-ttu-id="2de1b-117">相鄰資訊也可用來優化鑲嵌式。</span><span class="sxs-lookup"><span data-stu-id="2de1b-117">Adjacency information is also used to optimize tessellation.</span></span> <span data-ttu-id="2de1b-118">藉由呼叫 [**ID3DXPatchMesh：： tessellate**](id3dxpatchmesh--tessellate.md)，重複產生相鄰資訊一次並 tessellate。</span><span class="sxs-lookup"><span data-stu-id="2de1b-118">Generate adjacency information once and tessellate repeatedly by calling [**ID3DXPatchMesh::Tessellate**](id3dxpatchmesh--tessellate.md).</span></span> <span data-ttu-id="2de1b-119">執行的優化與實際使用的鑲嵌層級無關。</span><span class="sxs-lookup"><span data-stu-id="2de1b-119">The optimization performed is independent of the actual tessellation level used.</span></span> <span data-ttu-id="2de1b-120">但是，如果網格頂點變更，您就必須重新產生相鄰資訊。</span><span class="sxs-lookup"><span data-stu-id="2de1b-120">However, if the mesh vertices are changed, you must regenerate the adjacency information.</span></span>

## <a name="requirements"></a><span data-ttu-id="2de1b-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="2de1b-121">Requirements</span></span>



| <span data-ttu-id="2de1b-122">需求</span><span class="sxs-lookup"><span data-stu-id="2de1b-122">Requirement</span></span> | <span data-ttu-id="2de1b-123">值</span><span class="sxs-lookup"><span data-stu-id="2de1b-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2de1b-124">標頭</span><span class="sxs-lookup"><span data-stu-id="2de1b-124">Header</span></span><br/>  | <dl> <span data-ttu-id="2de1b-125"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="2de1b-125"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="2de1b-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="2de1b-126">Library</span></span><br/> | <dl> <span data-ttu-id="2de1b-127"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="2de1b-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2de1b-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2de1b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2de1b-129">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="2de1b-129">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> <dt>

[<span data-ttu-id="2de1b-130">**ID3DXPatchMesh::GenerateAdjacency**</span><span class="sxs-lookup"><span data-stu-id="2de1b-130">**ID3DXPatchMesh::GenerateAdjacency**</span></span>](id3dxpatchmesh--generateadjacency.md)
</dt> </dl>

 

 

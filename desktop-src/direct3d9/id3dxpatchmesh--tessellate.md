---
description: 根據鑲嵌式層級執行統一鑲嵌。
ms.assetid: 0fc701b4-0636-450e-b8e0-e7a490871316
title: 'ID3DXPatchMesh：： Tessellate 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.Tessellate
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b94b79a9decd2f44fa1675e257a2401e2ae8f7a6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106979886"
---
# <a name="id3dxpatchmeshtessellate-method"></a><span data-ttu-id="dee96-103">ID3DXPatchMesh：： Tessellate 方法</span><span class="sxs-lookup"><span data-stu-id="dee96-103">ID3DXPatchMesh::Tessellate method</span></span>

<span data-ttu-id="dee96-104">根據鑲嵌式層級執行統一鑲嵌。</span><span class="sxs-lookup"><span data-stu-id="dee96-104">Performs uniform tessellation based on the tessellation level.</span></span>

## <a name="syntax"></a><span data-ttu-id="dee96-105">語法</span><span class="sxs-lookup"><span data-stu-id="dee96-105">Syntax</span></span>


```C++
HRESULT Tessellate(
  [in] FLOAT      fTessLevel,
  [in] LPD3DXMESH pMesh
);
```



## <a name="parameters"></a><span data-ttu-id="dee96-106">參數</span><span class="sxs-lookup"><span data-stu-id="dee96-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dee96-107">*fTessLevel* \[在\]</span><span class="sxs-lookup"><span data-stu-id="dee96-107">*fTessLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dee96-108">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dee96-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dee96-109">鑲嵌式層級。</span><span class="sxs-lookup"><span data-stu-id="dee96-109">Tessellation level.</span></span> <span data-ttu-id="dee96-110">這是在現有頂點之間引進的頂點數目。</span><span class="sxs-lookup"><span data-stu-id="dee96-110">This is the number of vertices introduced between existing vertices.</span></span> <span data-ttu-id="dee96-111">此浮點數參數的範圍為 0 < fTessLevel <= 32。</span><span class="sxs-lookup"><span data-stu-id="dee96-111">The range of this float parameter is 0 < fTessLevel <= 32.</span></span>

</dd> <dt>

<span data-ttu-id="dee96-112">*pMesh* \[在\]</span><span class="sxs-lookup"><span data-stu-id="dee96-112">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dee96-113">類型： **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="dee96-113">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="dee96-114">產生的鑲嵌網格。</span><span class="sxs-lookup"><span data-stu-id="dee96-114">Resulting tessellated mesh.</span></span> <span data-ttu-id="dee96-115">請參閱 [**ID3DXMesh**](id3dxmesh.md)。</span><span class="sxs-lookup"><span data-stu-id="dee96-115">See [**ID3DXMesh**](id3dxmesh.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dee96-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="dee96-116">Return value</span></span>

<span data-ttu-id="dee96-117">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="dee96-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="dee96-118">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="dee96-118">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="dee96-119">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="dee96-119">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="dee96-120">備註</span><span class="sxs-lookup"><span data-stu-id="dee96-120">Remarks</span></span>

<span data-ttu-id="dee96-121">如果已使用 [**ID3DXPatchMesh：： Optimize**](id3dxpatchmesh--optimize.md)將修補程式網格優化，此函式將會更有效率地執行。</span><span class="sxs-lookup"><span data-stu-id="dee96-121">This function will perform more efficiently if the patch mesh has been optimized using [**ID3DXPatchMesh::Optimize**](id3dxpatchmesh--optimize.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dee96-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="dee96-122">Requirements</span></span>



| <span data-ttu-id="dee96-123">需求</span><span class="sxs-lookup"><span data-stu-id="dee96-123">Requirement</span></span> | <span data-ttu-id="dee96-124">值</span><span class="sxs-lookup"><span data-stu-id="dee96-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dee96-125">標頭</span><span class="sxs-lookup"><span data-stu-id="dee96-125">Header</span></span><br/>  | <dl> <span data-ttu-id="dee96-126"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="dee96-126"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="dee96-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="dee96-127">Library</span></span><br/> | <dl> <span data-ttu-id="dee96-128"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="dee96-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="dee96-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dee96-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dee96-130">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="dee96-130">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 

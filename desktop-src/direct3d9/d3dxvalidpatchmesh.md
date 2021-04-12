---
description: 驗證 patch 網狀，以傳回退化頂點和修補程式的數目。
ms.assetid: a95ff9d9-d476-42ac-8d7e-1dc42418f763
title: 'D3DXValidPatchMesh 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXValidPatchMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 87d7fbe15c78a8b768d845e6a23cc084b69f3e02
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946079"
---
# <a name="d3dxvalidpatchmesh-function"></a><span data-ttu-id="de5e2-103">D3DXValidPatchMesh 函式</span><span class="sxs-lookup"><span data-stu-id="de5e2-103">D3DXValidPatchMesh function</span></span>

<span data-ttu-id="de5e2-104">驗證 patch 網狀，以傳回退化頂點和修補程式的數目。</span><span class="sxs-lookup"><span data-stu-id="de5e2-104">Validates a patch mesh, returning the number of degenerate vertices and patches.</span></span>

## <a name="syntax"></a><span data-ttu-id="de5e2-105">語法</span><span class="sxs-lookup"><span data-stu-id="de5e2-105">Syntax</span></span>


```C++
HRESULT D3DXValidPatchMesh(
  _In_  LPD3DXPATCHMESH pMeshIn,
  _Out_ DWORD           *pNumDegenerateVertices,
  _Out_ DWORD           *pNumDegeneratePatches,
  _Out_ LPD3DXBUFFER    *ppErrorsAndWarnings
);
```



## <a name="parameters"></a><span data-ttu-id="de5e2-106">參數</span><span class="sxs-lookup"><span data-stu-id="de5e2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de5e2-107">*pMeshIn* \[在\]</span><span class="sxs-lookup"><span data-stu-id="de5e2-107">*pMeshIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de5e2-108">類型： **[ **LPD3DXPATCHMESH**](id3dxpatchmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="de5e2-108">Type: **[**LPD3DXPATCHMESH**](id3dxpatchmesh.md)**</span></span>

<span data-ttu-id="de5e2-109">[**ID3DXPatchMesh**](id3dxpatchmesh.md)介面的指標，代表要測試的修補程式網格。</span><span class="sxs-lookup"><span data-stu-id="de5e2-109">Pointer to an [**ID3DXPatchMesh**](id3dxpatchmesh.md) interface, representing the patch mesh to be tested.</span></span>

</dd> <dt>

<span data-ttu-id="de5e2-110">*pNumDegenerateVertices* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="de5e2-110">*pNumDegenerateVertices* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="de5e2-111">類型： **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="de5e2-111">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="de5e2-112">傳回修補程式網格中的退化頂點數目。</span><span class="sxs-lookup"><span data-stu-id="de5e2-112">Returns the number of degenerate vertices in the patch mesh.</span></span>

</dd> <dt>

<span data-ttu-id="de5e2-113">*pNumDegeneratePatches* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="de5e2-113">*pNumDegeneratePatches* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="de5e2-114">類型： **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="de5e2-114">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="de5e2-115">傳回修補程式網格中的退化修補程式數目。</span><span class="sxs-lookup"><span data-stu-id="de5e2-115">Returns the number of degenerate patches in the patch mesh.</span></span>

</dd> <dt>

<span data-ttu-id="de5e2-116">*ppErrorsAndWarnings* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="de5e2-116">*ppErrorsAndWarnings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="de5e2-117">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="de5e2-117">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="de5e2-118">傳回包含錯誤和警告字串的緩衝區指標，以說明在修補程式網格中找到的問題。</span><span class="sxs-lookup"><span data-stu-id="de5e2-118">Returns a pointer to a buffer containing a string of errors and warnings that explain the problems found in the patch mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de5e2-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="de5e2-119">Return value</span></span>

<span data-ttu-id="de5e2-120">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="de5e2-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="de5e2-121">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="de5e2-121">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="de5e2-122">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="de5e2-122">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="de5e2-123">備註</span><span class="sxs-lookup"><span data-stu-id="de5e2-123">Remarks</span></span>

<span data-ttu-id="de5e2-124">這個方法會檢查是否有不正確索引來驗證網格。</span><span class="sxs-lookup"><span data-stu-id="de5e2-124">This method validates the mesh by checking for invalid indices.</span></span> <span data-ttu-id="de5e2-125">您可以從偵錯工具輸出取得錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="de5e2-125">Error information is available from the debugger output.</span></span>

## <a name="requirements"></a><span data-ttu-id="de5e2-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="de5e2-126">Requirements</span></span>



| <span data-ttu-id="de5e2-127">需求</span><span class="sxs-lookup"><span data-stu-id="de5e2-127">Requirement</span></span> | <span data-ttu-id="de5e2-128">值</span><span class="sxs-lookup"><span data-stu-id="de5e2-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="de5e2-129">標頭</span><span class="sxs-lookup"><span data-stu-id="de5e2-129">Header</span></span><br/>  | <dl> <span data-ttu-id="de5e2-130"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="de5e2-130"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="de5e2-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="de5e2-131">Library</span></span><br/> | <dl> <span data-ttu-id="de5e2-132"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="de5e2-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="de5e2-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="de5e2-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de5e2-134">網格函數</span><span class="sxs-lookup"><span data-stu-id="de5e2-134">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 

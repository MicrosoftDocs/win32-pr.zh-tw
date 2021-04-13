---
description: 驗證網格。
ms.assetid: e5bec2f3-e914-4677-8114-77c71b8a586e
title: 'D3DXValidMesh 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXValidMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 469b9b32072107885417266266f804a955301668
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322820"
---
# <a name="d3dxvalidmesh-function"></a><span data-ttu-id="57fe3-103">D3DXValidMesh 函式</span><span class="sxs-lookup"><span data-stu-id="57fe3-103">D3DXValidMesh function</span></span>

<span data-ttu-id="57fe3-104">驗證網格。</span><span class="sxs-lookup"><span data-stu-id="57fe3-104">Validates a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="57fe3-105">語法</span><span class="sxs-lookup"><span data-stu-id="57fe3-105">Syntax</span></span>


```C++
HRESULT D3DXValidMesh(
  _In_        LPD3DXMESH   pMeshIn,
  _In_  const DWORD        *pAdjacency,
  _Out_       LPD3DXBUFFER *ppErrorsAndWarnings
);
```



## <a name="parameters"></a><span data-ttu-id="57fe3-106">參數</span><span class="sxs-lookup"><span data-stu-id="57fe3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57fe3-107">*pMeshIn* \[在\]</span><span class="sxs-lookup"><span data-stu-id="57fe3-107">*pMeshIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57fe3-108">類型： **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="57fe3-108">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="57fe3-109">[**ID3DXMesh**](id3dxmesh.md)介面的指標，代表要測試的網格。</span><span class="sxs-lookup"><span data-stu-id="57fe3-109">Pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the mesh to be tested.</span></span>

</dd> <dt>

<span data-ttu-id="57fe3-110">*pAdjacency* \[在\]</span><span class="sxs-lookup"><span data-stu-id="57fe3-110">*pAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57fe3-111">類型： **Const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="57fe3-111">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="57fe3-112">指標，指向每個臉部的三個 Dword 陣列，以指定要測試之網格中每個臉部的三個相鄰專案。</span><span class="sxs-lookup"><span data-stu-id="57fe3-112">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the mesh to be tested.</span></span>

</dd> <dt>

<span data-ttu-id="57fe3-113">*ppErrorsAndWarnings* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="57fe3-113">*ppErrorsAndWarnings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="57fe3-114">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="57fe3-114">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="57fe3-115">傳回包含錯誤和警告字串的緩衝區，以說明在網格中找到的問題。</span><span class="sxs-lookup"><span data-stu-id="57fe3-115">Returns a buffer containing a string of errors and warnings, which explain the problems found in the mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57fe3-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="57fe3-116">Return value</span></span>

<span data-ttu-id="57fe3-117">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="57fe3-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="57fe3-118">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="57fe3-118">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="57fe3-119">如果函式失敗，則傳回值可以是下列其中一項： D3DXERR \_ INVALIDMESH、D3DERR \_ INVALIDCALL、E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="57fe3-119">If the function fails, the return value can be one of the following: D3DXERR\_INVALIDMESH, D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="57fe3-120">備註</span><span class="sxs-lookup"><span data-stu-id="57fe3-120">Remarks</span></span>

<span data-ttu-id="57fe3-121">這個方法會檢查是否有不正確索引來驗證網格。</span><span class="sxs-lookup"><span data-stu-id="57fe3-121">This method validates the mesh by checking for invalid indices.</span></span> <span data-ttu-id="57fe3-122">您可以從偵錯工具輸出取得錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="57fe3-122">Error information is available from the debugger output.</span></span>

## <a name="requirements"></a><span data-ttu-id="57fe3-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="57fe3-123">Requirements</span></span>



| <span data-ttu-id="57fe3-124">需求</span><span class="sxs-lookup"><span data-stu-id="57fe3-124">Requirement</span></span> | <span data-ttu-id="57fe3-125">值</span><span class="sxs-lookup"><span data-stu-id="57fe3-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="57fe3-126">標頭</span><span class="sxs-lookup"><span data-stu-id="57fe3-126">Header</span></span><br/>  | <dl> <span data-ttu-id="57fe3-127"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="57fe3-127"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="57fe3-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="57fe3-128">Library</span></span><br/> | <dl> <span data-ttu-id="57fe3-129"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="57fe3-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="57fe3-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="57fe3-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57fe3-131">網格函數</span><span class="sxs-lookup"><span data-stu-id="57fe3-131">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 

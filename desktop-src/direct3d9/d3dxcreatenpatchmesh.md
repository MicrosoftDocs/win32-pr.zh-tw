---
description: 從三角形網格建立 N 修補程式網格。
ms.assetid: f565ed0b-72fc-4184-b423-f68b0acfafb0
title: 'D3DXCreateNPatchMesh 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateNPatchMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0ab73d1254700808bbd56b7b46f7781b27b188b7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106985910"
---
# <a name="d3dxcreatenpatchmesh-function"></a><span data-ttu-id="850a9-103">D3DXCreateNPatchMesh 函式</span><span class="sxs-lookup"><span data-stu-id="850a9-103">D3DXCreateNPatchMesh function</span></span>

<span data-ttu-id="850a9-104">從三角形網格建立 N 修補程式網格。</span><span class="sxs-lookup"><span data-stu-id="850a9-104">Creates an N-patch mesh from a triangle mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="850a9-105">語法</span><span class="sxs-lookup"><span data-stu-id="850a9-105">Syntax</span></span>


```C++
HRESULT D3DXCreateNPatchMesh(
  _In_    LPD3DXMESH      pMeshSysMem,
  _Inout_ LPD3DXPATCHMESH *pPatchMesh
);
```



## <a name="parameters"></a><span data-ttu-id="850a9-106">參數</span><span class="sxs-lookup"><span data-stu-id="850a9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="850a9-107">*pMeshSysMem* \[在\]</span><span class="sxs-lookup"><span data-stu-id="850a9-107">*pMeshSysMem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="850a9-108">類型： **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="850a9-108">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="850a9-109">代表三角形網格物件之 [**ID3DXMesh**](id3dxmesh.md) 介面指標的位址。</span><span class="sxs-lookup"><span data-stu-id="850a9-109">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface that represents the triangle mesh object.</span></span>

</dd> <dt>

<span data-ttu-id="850a9-110">*pPatchMesh* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="850a9-110">*pPatchMesh* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="850a9-111">類型： **[ **LPD3DXPATCHMESH**](id3dxpatchmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="850a9-111">Type: **[**LPD3DXPATCHMESH**](id3dxpatchmesh.md)\***</span></span>

<span data-ttu-id="850a9-112">[**ID3DXPatchMesh**](id3dxpatchmesh.md)介面指標的位址，表示所建立的 patch 網狀物件。</span><span class="sxs-lookup"><span data-stu-id="850a9-112">Address of a pointer to an [**ID3DXPatchMesh**](id3dxpatchmesh.md) interface that represents the created patch mesh object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="850a9-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="850a9-113">Return value</span></span>

<span data-ttu-id="850a9-114">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="850a9-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="850a9-115">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="850a9-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="850a9-116">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="850a9-116">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="850a9-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="850a9-117">Requirements</span></span>



| <span data-ttu-id="850a9-118">需求</span><span class="sxs-lookup"><span data-stu-id="850a9-118">Requirement</span></span> | <span data-ttu-id="850a9-119">值</span><span class="sxs-lookup"><span data-stu-id="850a9-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="850a9-120">標頭</span><span class="sxs-lookup"><span data-stu-id="850a9-120">Header</span></span><br/>  | <dl> <span data-ttu-id="850a9-121"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="850a9-121"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="850a9-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="850a9-122">Library</span></span><br/> | <dl> <span data-ttu-id="850a9-123"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="850a9-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="850a9-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="850a9-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="850a9-125">網格函數</span><span class="sxs-lookup"><span data-stu-id="850a9-125">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 





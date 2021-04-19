---
description: 取得網格頂點緩衝區。
ms.assetid: 4ea4e99b-5c2c-467b-8b5d-8174c446680a
title: 'ID3DXPatchMesh：： GetVertexBuffer 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.GetVertexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b8c3bb79d4c04db072adef857de195df7a0f0fff
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106974899"
---
# <a name="id3dxpatchmeshgetvertexbuffer-method"></a><span data-ttu-id="db19a-103">ID3DXPatchMesh：： GetVertexBuffer 方法</span><span class="sxs-lookup"><span data-stu-id="db19a-103">ID3DXPatchMesh::GetVertexBuffer method</span></span>

<span data-ttu-id="db19a-104">取得網格頂點緩衝區。</span><span class="sxs-lookup"><span data-stu-id="db19a-104">Gets the mesh vertex buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="db19a-105">語法</span><span class="sxs-lookup"><span data-stu-id="db19a-105">Syntax</span></span>


```C++
HRESULT GetVertexBuffer(
  [out] LPDIRECT3DVERTEXBUFFER9 *ppVB
);
```



## <a name="parameters"></a><span data-ttu-id="db19a-106">參數</span><span class="sxs-lookup"><span data-stu-id="db19a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db19a-107">*ppVB* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="db19a-107">*ppVB* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="db19a-108">類型： **[ **LPDIRECT3DVERTEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)\***</span><span class="sxs-lookup"><span data-stu-id="db19a-108">Type: **[**LPDIRECT3DVERTEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)\***</span></span>

<span data-ttu-id="db19a-109">頂點緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="db19a-109">Pointer to the vertex buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db19a-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="db19a-110">Return value</span></span>

<span data-ttu-id="db19a-111">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="db19a-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="db19a-112">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="db19a-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="db19a-113">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="db19a-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="db19a-114">備註</span><span class="sxs-lookup"><span data-stu-id="db19a-114">Remarks</span></span>

<span data-ttu-id="db19a-115">這個方法會採用統一鑲嵌。</span><span class="sxs-lookup"><span data-stu-id="db19a-115">This method assumes uniform tessellation.</span></span>

## <a name="requirements"></a><span data-ttu-id="db19a-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="db19a-116">Requirements</span></span>



| <span data-ttu-id="db19a-117">需求</span><span class="sxs-lookup"><span data-stu-id="db19a-117">Requirement</span></span> | <span data-ttu-id="db19a-118">值</span><span class="sxs-lookup"><span data-stu-id="db19a-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="db19a-119">標頭</span><span class="sxs-lookup"><span data-stu-id="db19a-119">Header</span></span><br/>  | <dl> <span data-ttu-id="db19a-120"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="db19a-120"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="db19a-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="db19a-121">Library</span></span><br/> | <dl> <span data-ttu-id="db19a-122"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="db19a-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="db19a-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="db19a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db19a-124">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="db19a-124">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 

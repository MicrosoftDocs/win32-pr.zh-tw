---
description: 取得網狀索引緩衝區。
ms.assetid: d9152f3b-c8e6-4def-8cf1-a517ca4d34e7
title: 'ID3DXPatchMesh：： GetIndexBuffer 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.GetIndexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c2730b90f77d33db519d2231a68ab7fdc2b520fd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986768"
---
# <a name="id3dxpatchmeshgetindexbuffer-method"></a><span data-ttu-id="744b1-103">ID3DXPatchMesh：： GetIndexBuffer 方法</span><span class="sxs-lookup"><span data-stu-id="744b1-103">ID3DXPatchMesh::GetIndexBuffer method</span></span>

<span data-ttu-id="744b1-104">取得網狀索引緩衝區。</span><span class="sxs-lookup"><span data-stu-id="744b1-104">Gets the mesh index buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="744b1-105">語法</span><span class="sxs-lookup"><span data-stu-id="744b1-105">Syntax</span></span>


```C++
HRESULT GetIndexBuffer(
  [out, retval] LPDIRECT3DINDEXBUFFER9 *ppIB
);
```



## <a name="parameters"></a><span data-ttu-id="744b1-106">參數</span><span class="sxs-lookup"><span data-stu-id="744b1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="744b1-107">*ppIB* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="744b1-107">*ppIB* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="744b1-108">類型： **[ **LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)\***</span><span class="sxs-lookup"><span data-stu-id="744b1-108">Type: **[**LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)\***</span></span>

<span data-ttu-id="744b1-109">索引緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="744b1-109">Pointer to the index buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="744b1-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="744b1-110">Return value</span></span>

<span data-ttu-id="744b1-111">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="744b1-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="744b1-112">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="744b1-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="744b1-113">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="744b1-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="744b1-114">備註</span><span class="sxs-lookup"><span data-stu-id="744b1-114">Remarks</span></span>

<span data-ttu-id="744b1-115">索引緩衝區包含頂點緩衝區中的頂點排序。</span><span class="sxs-lookup"><span data-stu-id="744b1-115">The index buffer contains the vertex ordering in the vertex buffer.</span></span> <span data-ttu-id="744b1-116">在呈現網格時，會使用索引緩衝區來存取頂點緩衝區。</span><span class="sxs-lookup"><span data-stu-id="744b1-116">The index buffer is used to access the vertex buffer when the mesh is rendered.</span></span>

## <a name="requirements"></a><span data-ttu-id="744b1-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="744b1-117">Requirements</span></span>



| <span data-ttu-id="744b1-118">需求</span><span class="sxs-lookup"><span data-stu-id="744b1-118">Requirement</span></span> | <span data-ttu-id="744b1-119">值</span><span class="sxs-lookup"><span data-stu-id="744b1-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="744b1-120">標頭</span><span class="sxs-lookup"><span data-stu-id="744b1-120">Header</span></span><br/>  | <dl> <span data-ttu-id="744b1-121"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="744b1-121"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="744b1-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="744b1-122">Library</span></span><br/> | <dl> <span data-ttu-id="744b1-123"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="744b1-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="744b1-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="744b1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="744b1-125">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="744b1-125">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 

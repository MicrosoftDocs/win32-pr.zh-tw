---
description: 取得頂點宣告。
ms.assetid: 53ff2fb5-68b6-4edd-b48f-e06df306ee3f
title: 'ID3DXPatchMesh：： GetDeclaration 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.GetDeclaration
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7d2d39192368fdca8ccaba7c51e64f60ea030568
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323411"
---
# <a name="id3dxpatchmeshgetdeclaration-method"></a><span data-ttu-id="66b91-103">ID3DXPatchMesh：： GetDeclaration 方法</span><span class="sxs-lookup"><span data-stu-id="66b91-103">ID3DXPatchMesh::GetDeclaration method</span></span>

<span data-ttu-id="66b91-104">取得頂點宣告。</span><span class="sxs-lookup"><span data-stu-id="66b91-104">Gets the vertex declaration.</span></span>

## <a name="syntax"></a><span data-ttu-id="66b91-105">語法</span><span class="sxs-lookup"><span data-stu-id="66b91-105">Syntax</span></span>


```C++
HRESULT GetDeclaration(
  [out] LPD3DVERTEXELEMENT9 pDeclaration
);
```



## <a name="parameters"></a><span data-ttu-id="66b91-106">參數</span><span class="sxs-lookup"><span data-stu-id="66b91-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66b91-107">*pDeclaration* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="66b91-107">*pDeclaration* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="66b91-108">類型： **[ **LPD3DVERTEXELEMENT9**](d3dvertexelement9.md)**</span><span class="sxs-lookup"><span data-stu-id="66b91-108">Type: **[**LPD3DVERTEXELEMENT9**](d3dvertexelement9.md)**</span></span>

<span data-ttu-id="66b91-109">描述網格頂點頂點格式的 [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) 元素陣列。</span><span class="sxs-lookup"><span data-stu-id="66b91-109">Array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) elements describing the vertex format of the mesh vertices.</span></span> <span data-ttu-id="66b91-110">此宣告子陣列的維度是 [**MAX \_ FVF \_ DECL \_ SIZE**](./max-fvf-decl-size.md)。</span><span class="sxs-lookup"><span data-stu-id="66b91-110">The dimension of this declarator array is [**MAX\_FVF\_DECL\_SIZE**](./max-fvf-decl-size.md).</span></span> <span data-ttu-id="66b91-111">頂點元素陣列的結尾是 [**D3DDECL \_ END**](d3ddecl-end.md) 宏。</span><span class="sxs-lookup"><span data-stu-id="66b91-111">The vertex element array ends with the [**D3DDECL\_END**](d3ddecl-end.md) macro.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66b91-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="66b91-112">Return value</span></span>

<span data-ttu-id="66b91-113">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="66b91-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="66b91-114">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="66b91-114">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="66b91-115">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="66b91-115">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="66b91-116">備註</span><span class="sxs-lookup"><span data-stu-id="66b91-116">Remarks</span></span>

<span data-ttu-id="66b91-117">專案的陣列包含結束宣告的 [**D3DDECL \_ 結束**](d3ddecl-end.md) 宏。</span><span class="sxs-lookup"><span data-stu-id="66b91-117">The array of elements includes the [**D3DDECL\_END**](d3ddecl-end.md) macro, which ends the declaration.</span></span>

## <a name="requirements"></a><span data-ttu-id="66b91-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="66b91-118">Requirements</span></span>



| <span data-ttu-id="66b91-119">需求</span><span class="sxs-lookup"><span data-stu-id="66b91-119">Requirement</span></span> | <span data-ttu-id="66b91-120">值</span><span class="sxs-lookup"><span data-stu-id="66b91-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="66b91-121">標頭</span><span class="sxs-lookup"><span data-stu-id="66b91-121">Header</span></span><br/>  | <dl> <span data-ttu-id="66b91-122"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="66b91-122"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="66b91-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="66b91-123">Library</span></span><br/> | <dl> <span data-ttu-id="66b91-124"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="66b91-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="66b91-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="66b91-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66b91-126">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="66b91-126">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 

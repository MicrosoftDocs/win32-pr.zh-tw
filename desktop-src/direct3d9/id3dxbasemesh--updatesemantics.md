---
description: 這種方法可讓使用者變更網格宣告，而不需要變更頂點緩衝區的資料版面配置。 只有當舊的和新的宣告格式具有相同的頂點大小時，呼叫才會有效。
ms.assetid: ed2ad479-e0f7-4580-a20a-d3649759876a
title: 'ID3DXBaseMesh：： UpdateSemantics 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.UpdateSemantics
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6e31a6fe424d085467bfa795c7ce7b2d445a1f69
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104035365"
---
# <a name="id3dxbasemeshupdatesemantics-method"></a><span data-ttu-id="2a597-104">ID3DXBaseMesh：： UpdateSemantics 方法</span><span class="sxs-lookup"><span data-stu-id="2a597-104">ID3DXBaseMesh::UpdateSemantics method</span></span>

<span data-ttu-id="2a597-105">這種方法可讓使用者變更網格宣告，而不需要變更頂點緩衝區的資料版面配置。</span><span class="sxs-lookup"><span data-stu-id="2a597-105">This method allows the user to change the mesh declaration without changing the data layout of the vertex buffer.</span></span> <span data-ttu-id="2a597-106">只有當舊的和新的宣告格式具有相同的頂點大小時，呼叫才會有效。</span><span class="sxs-lookup"><span data-stu-id="2a597-106">The call is valid only if the old and new declaration formats have the same vertex size.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a597-107">語法</span><span class="sxs-lookup"><span data-stu-id="2a597-107">Syntax</span></span>


```C++
HRESULT UpdateSemantics(
  [in, out] D3DVERTEXELEMENT9 Declaration
);
```



## <a name="parameters"></a><span data-ttu-id="2a597-108">參數</span><span class="sxs-lookup"><span data-stu-id="2a597-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a597-109">宣告 \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="2a597-109">*Declaration* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2a597-110">類型： **[ **D3DVERTEXELEMENT9**](d3dvertexelement9.md)**</span><span class="sxs-lookup"><span data-stu-id="2a597-110">Type: **[**D3DVERTEXELEMENT9**](d3dvertexelement9.md)**</span></span>

<span data-ttu-id="2a597-111">[**D3DVERTEXELEMENT9**](d3dvertexelement9.md)元素的陣列，描述網格頂點的頂點格式。</span><span class="sxs-lookup"><span data-stu-id="2a597-111">An array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) elements, describing the vertex format of the mesh vertices.</span></span> <span data-ttu-id="2a597-112">此宣告子陣列的上限是 [**\_ FVF \_ DECL \_ SIZE 的最大**](./max-fvf-decl-size.md)值。</span><span class="sxs-lookup"><span data-stu-id="2a597-112">The upper limit of this declarator array is [**MAX\_FVF\_DECL\_SIZE**](./max-fvf-decl-size.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a597-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="2a597-113">Return value</span></span>

<span data-ttu-id="2a597-114">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2a597-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2a597-115">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="2a597-115">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="2a597-116">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="2a597-116">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a597-117">備註</span><span class="sxs-lookup"><span data-stu-id="2a597-117">Remarks</span></span>

<span data-ttu-id="2a597-118">[**ID3DXBaseMesh：： CloneMesh**](id3dxbasemesh--clonemesh.md) 是用來重新格式化及變更頂點資料版面配置。</span><span class="sxs-lookup"><span data-stu-id="2a597-118">[**ID3DXBaseMesh::CloneMesh**](id3dxbasemesh--clonemesh.md) is used to reformat and change the vertex data layout.</span></span> <span data-ttu-id="2a597-119">例如，您可以使用它來新增不存在之法線、材質座標、色彩、權數等的空間。</span><span class="sxs-lookup"><span data-stu-id="2a597-119">For example, use it to to add space for normals, texture coordinates, colors, weights, etc. that were not present before.</span></span>

<span data-ttu-id="2a597-120">**ID3DXBaseMesh：： UpdateSemantics** 是使用不同的語義資訊來更新頂點宣告的方法，而不需要變更頂點緩衝區的版面配置。</span><span class="sxs-lookup"><span data-stu-id="2a597-120">**ID3DXBaseMesh::UpdateSemantics** is a method for updating the vertex declaration with different semantic information, without changing the layout of the vertex buffer.</span></span> <span data-ttu-id="2a597-121">例如，使用它將3D 紋理座標重定為 binormal 或正切函數，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="2a597-121">For example, use it to relabel a 3D texture coordinate as a binormal or tangent, or vice versa.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a597-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="2a597-122">Requirements</span></span>



| <span data-ttu-id="2a597-123">需求</span><span class="sxs-lookup"><span data-stu-id="2a597-123">Requirement</span></span> | <span data-ttu-id="2a597-124">值</span><span class="sxs-lookup"><span data-stu-id="2a597-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2a597-125">標頭</span><span class="sxs-lookup"><span data-stu-id="2a597-125">Header</span></span><br/>  | <dl> <span data-ttu-id="2a597-126"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="2a597-126"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="2a597-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="2a597-127">Library</span></span><br/> | <dl> <span data-ttu-id="2a597-128"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="2a597-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2a597-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2a597-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a597-130">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="2a597-130">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> <dt>

[<span data-ttu-id="2a597-131">**ID3DXBaseMesh::CloneMeshFVF**</span><span class="sxs-lookup"><span data-stu-id="2a597-131">**ID3DXBaseMesh::CloneMeshFVF**</span></span>](id3dxbasemesh--clonemeshfvf.md)
</dt> <dt>

[<span data-ttu-id="2a597-132">**D3DXDeclaratorFromFVF**</span><span class="sxs-lookup"><span data-stu-id="2a597-132">**D3DXDeclaratorFromFVF**</span></span>](d3dxdeclaratorfromfvf.md)
</dt> </dl>

 

 

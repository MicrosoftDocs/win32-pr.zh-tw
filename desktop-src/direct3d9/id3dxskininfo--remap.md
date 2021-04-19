---
description: 更新骨骼影響資訊，使其在重新排序之後符合頂點。 如果目標頂點緩衝區已從外部重新排序，則應該呼叫這個方法。
ms.assetid: bff5229f-e547-4ab3-84c6-58b15a7825e9
title: 'ID3DXSkinInfo：：重新對應方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.Remap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 657cf0977592a8e19e68b8aeb950c62d404e7cdb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106979869"
---
# <a name="id3dxskininforemap-method"></a><span data-ttu-id="b9844-104">ID3DXSkinInfo：：重新對應方法</span><span class="sxs-lookup"><span data-stu-id="b9844-104">ID3DXSkinInfo::Remap method</span></span>

<span data-ttu-id="b9844-105">更新骨骼影響資訊，使其在重新排序之後符合頂點。</span><span class="sxs-lookup"><span data-stu-id="b9844-105">Updates bone influence information to match vertices after they are reordered.</span></span> <span data-ttu-id="b9844-106">如果目標頂點緩衝區已從外部重新排序，則應該呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="b9844-106">This method should be called if the target vertex buffer has been reordered externally.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9844-107">語法</span><span class="sxs-lookup"><span data-stu-id="b9844-107">Syntax</span></span>


```C++
HRESULT Remap(
  [in] DWORD NumVertices,
  [in] DWORD *pVertexRemap
);
```



## <a name="parameters"></a><span data-ttu-id="b9844-108">參數</span><span class="sxs-lookup"><span data-stu-id="b9844-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9844-109">*NumVertices* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b9844-109">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9844-110">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b9844-110">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b9844-111">要重新對應的頂點數目。</span><span class="sxs-lookup"><span data-stu-id="b9844-111">Number of vertices to remap.</span></span>

</dd> <dt>

<span data-ttu-id="b9844-112">*pVertexRemap* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b9844-112">*pVertexRemap* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9844-113">類型： **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="b9844-113">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="b9844-114">DWORD 的陣列，其長度是由 NumVertices 所指定。</span><span class="sxs-lookup"><span data-stu-id="b9844-114">Array of DWORDS whose length is specified by NumVertices.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9844-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="b9844-115">Return value</span></span>

<span data-ttu-id="b9844-116">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b9844-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b9844-117">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="b9844-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b9844-118">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="b9844-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="b9844-119">備註</span><span class="sxs-lookup"><span data-stu-id="b9844-119">Remarks</span></span>

<span data-ttu-id="b9844-120">PVertexRemap 中的每個元素會指定該位置的先前頂點索引。</span><span class="sxs-lookup"><span data-stu-id="b9844-120">Each element in pVertexRemap specifies the previous vertex index for that position.</span></span> <span data-ttu-id="b9844-121">例如，如果頂點位於位置3，但已重新對應到位置5，則 pVertexRemap 的第五個元素應包含3個。</span><span class="sxs-lookup"><span data-stu-id="b9844-121">For example, if a vertex was in position 3 but has been remapped to position 5, then the fifth element of pVertexRemap should contain 3.</span></span> <span data-ttu-id="b9844-122">您可以使用 [**ID3DXMesh：： Optimize**](id3dxmesh--optimize.md) 傳回的頂點重新對應陣列。</span><span class="sxs-lookup"><span data-stu-id="b9844-122">The vertex remap array returned by [**ID3DXMesh::Optimize**](id3dxmesh--optimize.md) can be used.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9844-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="b9844-123">Requirements</span></span>



| <span data-ttu-id="b9844-124">需求</span><span class="sxs-lookup"><span data-stu-id="b9844-124">Requirement</span></span> | <span data-ttu-id="b9844-125">值</span><span class="sxs-lookup"><span data-stu-id="b9844-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b9844-126">標頭</span><span class="sxs-lookup"><span data-stu-id="b9844-126">Header</span></span><br/>  | <dl> <span data-ttu-id="b9844-127"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="b9844-127"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="b9844-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="b9844-128">Library</span></span><br/> | <dl> <span data-ttu-id="b9844-129"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="b9844-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b9844-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b9844-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9844-131">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="b9844-131">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> </dl>

 

 

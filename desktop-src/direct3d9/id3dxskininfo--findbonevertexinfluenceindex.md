---
description: 捕獲影響單一頂點之骨骼影響的索引。
ms.assetid: vs|directx_sdk|~\id3dxskininfo__findbonevertexinfluenceindex.htm
title: 'ID3DXSkinInfo：： FindBoneVertexInfluenceIndex 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.FindBoneVertexInfluenceIndex
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 05a86e98e5001092700fdec12f2a7afc33ddf082
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106976684"
---
# <a name="id3dxskininfofindbonevertexinfluenceindex-method"></a><span data-ttu-id="0812c-103">ID3DXSkinInfo：： FindBoneVertexInfluenceIndex 方法</span><span class="sxs-lookup"><span data-stu-id="0812c-103">ID3DXSkinInfo::FindBoneVertexInfluenceIndex method</span></span>

<span data-ttu-id="0812c-104">捕獲影響單一頂點之骨骼影響的索引。</span><span class="sxs-lookup"><span data-stu-id="0812c-104">Retrieves the index of the bone influence affecting a single vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="0812c-105">語法</span><span class="sxs-lookup"><span data-stu-id="0812c-105">Syntax</span></span>


```C++
HRESULT FindBoneVertexInfluenceIndex(
  [in]      DWORD boneNum,
  [in]      DWORD vertexNum,
  [in, out] DWORD *pInfluenceIndex
);
```



## <a name="parameters"></a><span data-ttu-id="0812c-106">參數</span><span class="sxs-lookup"><span data-stu-id="0812c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0812c-107">*boneNum* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0812c-107">*boneNum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0812c-108">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0812c-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0812c-109">骨骼的索引。</span><span class="sxs-lookup"><span data-stu-id="0812c-109">Index of the bone.</span></span> <span data-ttu-id="0812c-110">必須介於0和骨骼數目之間。</span><span class="sxs-lookup"><span data-stu-id="0812c-110">Must be between 0 and the number of bones.</span></span>

</dd> <dt>

<span data-ttu-id="0812c-111">*vertexNum* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0812c-111">*vertexNum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0812c-112">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0812c-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0812c-113">要尋找其骨骼影響之頂點的索引。</span><span class="sxs-lookup"><span data-stu-id="0812c-113">Index of the vertex for which the bone influence is to be found.</span></span> <span data-ttu-id="0812c-114">必須介於0和網格中頂點的數目之間。</span><span class="sxs-lookup"><span data-stu-id="0812c-114">Must be between 0 and the number of vertices in the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="0812c-115">*pInfluenceIndex* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="0812c-115">*pInfluenceIndex* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0812c-116">類型： **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="0812c-116">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0812c-117">影響 vertexNum 之骨骼影響索引的指標。</span><span class="sxs-lookup"><span data-stu-id="0812c-117">Pointer to the index of the bone influence that affects vertexNum.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0812c-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="0812c-118">Return value</span></span>

<span data-ttu-id="0812c-119">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0812c-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0812c-120">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="0812c-120">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="0812c-121">如果指定的骨骼不影響指定的頂點， \_ 則會傳回 FALSE。</span><span class="sxs-lookup"><span data-stu-id="0812c-121">If the specified bone does not influence the given vertex, S\_FALSE is returned.</span></span> <span data-ttu-id="0812c-122">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="0812c-122">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="0812c-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="0812c-123">Requirements</span></span>



| <span data-ttu-id="0812c-124">需求</span><span class="sxs-lookup"><span data-stu-id="0812c-124">Requirement</span></span> | <span data-ttu-id="0812c-125">值</span><span class="sxs-lookup"><span data-stu-id="0812c-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0812c-126">標頭</span><span class="sxs-lookup"><span data-stu-id="0812c-126">Header</span></span><br/>  | <dl> <span data-ttu-id="0812c-127"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="0812c-127"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="0812c-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="0812c-128">Library</span></span><br/> | <dl> <span data-ttu-id="0812c-129"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="0812c-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0812c-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0812c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0812c-131">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="0812c-131">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="0812c-132">**ID3DXSkinInfo::GetBoneVertexInfluence**</span><span class="sxs-lookup"><span data-stu-id="0812c-132">**ID3DXSkinInfo::GetBoneVertexInfluence**</span></span>](id3dxskininfo--getbonevertexinfluence.md)
</dt> <dt>

[<span data-ttu-id="0812c-133">**ID3DXSkinInfo::SetBoneVertexInfluence**</span><span class="sxs-lookup"><span data-stu-id="0812c-133">**ID3DXSkinInfo::SetBoneVertexInfluence**</span></span>](id3dxskininfo--setbonevertexinfluence.md)
</dt> <dt>

[<span data-ttu-id="0812c-134">**ID3DXSkinInfo::GetBoneInfluence**</span><span class="sxs-lookup"><span data-stu-id="0812c-134">**ID3DXSkinInfo::GetBoneInfluence**</span></span>](id3dxskininfo--getboneinfluence.md)
</dt> </dl>

 

 

---
description: 抓取受指定之骨骼影響影響的 blend 因數和頂點。
ms.assetid: bbed4766-e571-4a9e-b7e3-047052470cbe
title: 'ID3DXSkinInfo：： GetBoneVertexInfluence 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetBoneVertexInfluence
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6e3cb7c530ed72a65f9a3e8de6b0735b1a7ae5e4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322607"
---
# <a name="id3dxskininfogetbonevertexinfluence-method"></a><span data-ttu-id="1c5a6-103">ID3DXSkinInfo：： GetBoneVertexInfluence 方法</span><span class="sxs-lookup"><span data-stu-id="1c5a6-103">ID3DXSkinInfo::GetBoneVertexInfluence method</span></span>

<span data-ttu-id="1c5a6-104">抓取受指定之骨骼影響影響的 blend 因數和頂點。</span><span class="sxs-lookup"><span data-stu-id="1c5a6-104">Retrieves the blend factor and vertex affected by a specified bone influence.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c5a6-105">語法</span><span class="sxs-lookup"><span data-stu-id="1c5a6-105">Syntax</span></span>


```C++
HRESULT GetBoneVertexInfluence(
  [in]      DWORD boneNum,
  [in]      DWORD influenceNum,
  [in, out] FLOAT *pWeight,
  [in, out] DWORD *pVertexNum
);
```



## <a name="parameters"></a><span data-ttu-id="1c5a6-106">參數</span><span class="sxs-lookup"><span data-stu-id="1c5a6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c5a6-107">*boneNum* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1c5a6-107">*boneNum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c5a6-108">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1c5a6-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1c5a6-109">骨骼的索引。</span><span class="sxs-lookup"><span data-stu-id="1c5a6-109">Index of the bone.</span></span> <span data-ttu-id="1c5a6-110">必須介於0和骨骼數目之間。</span><span class="sxs-lookup"><span data-stu-id="1c5a6-110">Must be between 0 and the number of bones.</span></span>

</dd> <dt>

<span data-ttu-id="1c5a6-111">*influenceNum* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1c5a6-111">*influenceNum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c5a6-112">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1c5a6-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1c5a6-113">指定之骨骼之影響陣列的索引。</span><span class="sxs-lookup"><span data-stu-id="1c5a6-113">Index of the influence array of the specified bone.</span></span>

</dd> <dt>

<span data-ttu-id="1c5a6-114">*pWeight* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="1c5a6-114">*pWeight* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1c5a6-115">類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="1c5a6-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="1c5a6-116">受 influenceNum 影響的 blend 因數指標。</span><span class="sxs-lookup"><span data-stu-id="1c5a6-116">Pointer to the blend factor influenced by influenceNum.</span></span>

</dd> <dt>

<span data-ttu-id="1c5a6-117">*pVertexNum* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="1c5a6-117">*pVertexNum* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1c5a6-118">類型： **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="1c5a6-118">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="1c5a6-119">受 influenceNum 影響的頂點指標。</span><span class="sxs-lookup"><span data-stu-id="1c5a6-119">Pointer to the vertex influenced by influenceNum.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c5a6-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="1c5a6-120">Return value</span></span>

<span data-ttu-id="1c5a6-121">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1c5a6-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1c5a6-122">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="1c5a6-122">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="1c5a6-123">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="1c5a6-123">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c5a6-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="1c5a6-124">Requirements</span></span>



| <span data-ttu-id="1c5a6-125">需求</span><span class="sxs-lookup"><span data-stu-id="1c5a6-125">Requirement</span></span> | <span data-ttu-id="1c5a6-126">值</span><span class="sxs-lookup"><span data-stu-id="1c5a6-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1c5a6-127">標頭</span><span class="sxs-lookup"><span data-stu-id="1c5a6-127">Header</span></span><br/>  | <dl> <span data-ttu-id="1c5a6-128"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="1c5a6-128"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="1c5a6-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="1c5a6-129">Library</span></span><br/> | <dl> <span data-ttu-id="1c5a6-130"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="1c5a6-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1c5a6-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1c5a6-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c5a6-132">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="1c5a6-132">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="1c5a6-133">**ID3DXSkinInfo::SetBoneVertexInfluence**</span><span class="sxs-lookup"><span data-stu-id="1c5a6-133">**ID3DXSkinInfo::SetBoneVertexInfluence**</span></span>](id3dxskininfo--setbonevertexinfluence.md)
</dt> <dt>

[<span data-ttu-id="1c5a6-134">**ID3DXSkinInfo::FindBoneVertexInfluenceIndex**</span><span class="sxs-lookup"><span data-stu-id="1c5a6-134">**ID3DXSkinInfo::FindBoneVertexInfluenceIndex**</span></span>](id3dxskininfo--findbonevertexinfluenceindex.md)
</dt> <dt>

[<span data-ttu-id="1c5a6-135">**ID3DXSkinInfo::GetBoneInfluence**</span><span class="sxs-lookup"><span data-stu-id="1c5a6-135">**ID3DXSkinInfo::GetBoneInfluence**</span></span>](id3dxskininfo--getboneinfluence.md)
</dt> </dl>

 

 

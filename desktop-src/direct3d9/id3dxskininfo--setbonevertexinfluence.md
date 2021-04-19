---
description: 將骨骼的影響值設定在單一頂點上。
ms.assetid: 9283866f-3dfe-467d-a74f-77e89c2778c4
title: 'ID3DXSkinInfo：： SetBoneVertexInfluence 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.SetBoneVertexInfluence
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: db84cdf9a1647bc5302c421e52d50f812e74596e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106988161"
---
# <a name="id3dxskininfosetbonevertexinfluence-method"></a><span data-ttu-id="be014-103">ID3DXSkinInfo：： SetBoneVertexInfluence 方法</span><span class="sxs-lookup"><span data-stu-id="be014-103">ID3DXSkinInfo::SetBoneVertexInfluence method</span></span>

<span data-ttu-id="be014-104">將骨骼的影響值設定在單一頂點上。</span><span class="sxs-lookup"><span data-stu-id="be014-104">Sets an influence value of a bone on a single vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="be014-105">語法</span><span class="sxs-lookup"><span data-stu-id="be014-105">Syntax</span></span>


```C++
HRESULT SetBoneVertexInfluence(
  [in] DWORD boneNum,
  [in] DWORD influenceNum,
  [in] FLOAT weight
);
```



## <a name="parameters"></a><span data-ttu-id="be014-106">參數</span><span class="sxs-lookup"><span data-stu-id="be014-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be014-107">*boneNum* \[在\]</span><span class="sxs-lookup"><span data-stu-id="be014-107">*boneNum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be014-108">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="be014-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="be014-109">骨骼的索引。</span><span class="sxs-lookup"><span data-stu-id="be014-109">Index of the bone.</span></span> <span data-ttu-id="be014-110">必須介於0和骨骼數目之間。</span><span class="sxs-lookup"><span data-stu-id="be014-110">Must be between 0 and the number of bones.</span></span>

</dd> <dt>

<span data-ttu-id="be014-111">*influenceNum* \[在\]</span><span class="sxs-lookup"><span data-stu-id="be014-111">*influenceNum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be014-112">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="be014-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="be014-113">指定之骨骼之影響陣列的索引。</span><span class="sxs-lookup"><span data-stu-id="be014-113">Index of the influence array of the specified bone.</span></span>

</dd> <dt>

<span data-ttu-id="be014-114">*權數* \[在\]</span><span class="sxs-lookup"><span data-stu-id="be014-114">*weight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be014-115">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="be014-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="be014-116">指定之骨骼影響的 Blend 因數。</span><span class="sxs-lookup"><span data-stu-id="be014-116">Blend factor of the specified bone influence.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be014-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="be014-117">Return value</span></span>

<span data-ttu-id="be014-118">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="be014-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="be014-119">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="be014-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="be014-120">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="be014-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="be014-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="be014-121">Requirements</span></span>



| <span data-ttu-id="be014-122">需求</span><span class="sxs-lookup"><span data-stu-id="be014-122">Requirement</span></span> | <span data-ttu-id="be014-123">值</span><span class="sxs-lookup"><span data-stu-id="be014-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="be014-124">標頭</span><span class="sxs-lookup"><span data-stu-id="be014-124">Header</span></span><br/>  | <dl> <span data-ttu-id="be014-125"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="be014-125"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="be014-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="be014-126">Library</span></span><br/> | <dl> <span data-ttu-id="be014-127"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="be014-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="be014-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="be014-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be014-129">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="be014-129">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="be014-130">**ID3DXSkinInfo::GetBoneVertexInfluence**</span><span class="sxs-lookup"><span data-stu-id="be014-130">**ID3DXSkinInfo::GetBoneVertexInfluence**</span></span>](id3dxskininfo--getbonevertexinfluence.md)
</dt> <dt>

[<span data-ttu-id="be014-131">**ID3DXSkinInfo::FindBoneVertexInfluenceIndex**</span><span class="sxs-lookup"><span data-stu-id="be014-131">**ID3DXSkinInfo::FindBoneVertexInfluenceIndex**</span></span>](id3dxskininfo--findbonevertexinfluenceindex.md)
</dt> <dt>

[<span data-ttu-id="be014-132">**ID3DXSkinInfo::GetBoneInfluence**</span><span class="sxs-lookup"><span data-stu-id="be014-132">**ID3DXSkinInfo::GetBoneInfluence**</span></span>](id3dxskininfo--getboneinfluence.md)
</dt> </dl>

 

 

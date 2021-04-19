---
description: 設定骨骼的影響值。
ms.assetid: c6dc8a33-8f5c-47d0-8637-a2492b1e3089
title: 'ID3DXSkinInfo：： SetBoneInfluence 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.SetBoneInfluence
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 16ed3514c986dee89f964074d18a646bcf3a1249
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106998994"
---
# <a name="id3dxskininfosetboneinfluence-method"></a><span data-ttu-id="5249c-103">ID3DXSkinInfo：： SetBoneInfluence 方法</span><span class="sxs-lookup"><span data-stu-id="5249c-103">ID3DXSkinInfo::SetBoneInfluence method</span></span>

<span data-ttu-id="5249c-104">設定骨骼的影響值。</span><span class="sxs-lookup"><span data-stu-id="5249c-104">Sets the influence value for a bone.</span></span>

## <a name="syntax"></a><span data-ttu-id="5249c-105">語法</span><span class="sxs-lookup"><span data-stu-id="5249c-105">Syntax</span></span>


```C++
HRESULT SetBoneInfluence(
  [in]       DWORD Bone,
  [in]       DWORD numInfluences,
  [in] const DWORD *vertices,
  [in] const FLOAT *weights
);
```



## <a name="parameters"></a><span data-ttu-id="5249c-106">參數</span><span class="sxs-lookup"><span data-stu-id="5249c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5249c-107">*骨骼* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5249c-107">*Bone* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5249c-108">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5249c-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5249c-109">骨骼編號。</span><span class="sxs-lookup"><span data-stu-id="5249c-109">Bone number.</span></span>

</dd> <dt>

<span data-ttu-id="5249c-110">*numInfluences* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5249c-110">*numInfluences* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5249c-111">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5249c-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5249c-112">影響數目。</span><span class="sxs-lookup"><span data-stu-id="5249c-112">Number of influences.</span></span>

</dd> <dt>

<span data-ttu-id="5249c-113">*頂點* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5249c-113">*vertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5249c-114">類型： **Const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="5249c-114">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="5249c-115">由骨骼影響的頂點陣列。</span><span class="sxs-lookup"><span data-stu-id="5249c-115">The array of vertices influenced by a bone.</span></span>

</dd> <dt>

<span data-ttu-id="5249c-116">*加權* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5249c-116">*weights* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5249c-117">Type： **Const [**FLOAT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="5249c-117">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="5249c-118">由骨骼影響的加權陣列。</span><span class="sxs-lookup"><span data-stu-id="5249c-118">The array of weights influenced by a bone.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5249c-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="5249c-119">Return value</span></span>

<span data-ttu-id="5249c-120">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5249c-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5249c-121">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="5249c-121">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="5249c-122">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="5249c-122">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="5249c-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="5249c-123">Requirements</span></span>



| <span data-ttu-id="5249c-124">需求</span><span class="sxs-lookup"><span data-stu-id="5249c-124">Requirement</span></span> | <span data-ttu-id="5249c-125">值</span><span class="sxs-lookup"><span data-stu-id="5249c-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5249c-126">標頭</span><span class="sxs-lookup"><span data-stu-id="5249c-126">Header</span></span><br/>  | <dl> <span data-ttu-id="5249c-127"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="5249c-127"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="5249c-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="5249c-128">Library</span></span><br/> | <dl> <span data-ttu-id="5249c-129"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="5249c-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5249c-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5249c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5249c-131">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="5249c-131">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="5249c-132">**ID3DXSkinInfo::GetBoneInfluence**</span><span class="sxs-lookup"><span data-stu-id="5249c-132">**ID3DXSkinInfo::GetBoneInfluence**</span></span>](id3dxskininfo--getboneinfluence.md)
</dt> <dt>

[<span data-ttu-id="5249c-133">**ID3DXSkinInfo::GetNumBoneInfluences**</span><span class="sxs-lookup"><span data-stu-id="5249c-133">**ID3DXSkinInfo::GetNumBoneInfluences**</span></span>](id3dxskininfo--getnumboneinfluences.md)
</dt> </dl>

 

 

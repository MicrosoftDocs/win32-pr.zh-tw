---
description: 取得骨骼影響的頂點和加權。
ms.assetid: 84cb064b-b6b2-402d-81cc-8c02de6f8b52
title: 'ID3DXSkinInfo：： GetBoneInfluence 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetBoneInfluence
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8b4b31ab08aca476ced1cb28dfc5ed5bfe61d044
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106982856"
---
# <a name="id3dxskininfogetboneinfluence-method"></a><span data-ttu-id="df905-103">ID3DXSkinInfo：： GetBoneInfluence 方法</span><span class="sxs-lookup"><span data-stu-id="df905-103">ID3DXSkinInfo::GetBoneInfluence method</span></span>

<span data-ttu-id="df905-104">取得骨骼影響的頂點和加權。</span><span class="sxs-lookup"><span data-stu-id="df905-104">Gets the vertices and weights that a bone influences.</span></span>

## <a name="syntax"></a><span data-ttu-id="df905-105">語法</span><span class="sxs-lookup"><span data-stu-id="df905-105">Syntax</span></span>


```C++
HRESULT GetBoneInfluence(
  [in]      DWORD Bone,
  [in, out] DWORD *vertices,
  [in, out] FLOAT *weights
);
```



## <a name="parameters"></a><span data-ttu-id="df905-106">參數</span><span class="sxs-lookup"><span data-stu-id="df905-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df905-107">*骨骼* \[在\]</span><span class="sxs-lookup"><span data-stu-id="df905-107">*Bone* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df905-108">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="df905-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="df905-109">骨骼編號。</span><span class="sxs-lookup"><span data-stu-id="df905-109">Bone number.</span></span>

</dd> <dt>

<span data-ttu-id="df905-110">*頂點* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="df905-110">*vertices* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="df905-111">類型： **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="df905-111">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="df905-112">取得由骨骼影響的頂點陣列。</span><span class="sxs-lookup"><span data-stu-id="df905-112">Get the array of vertices influenced by a bone.</span></span>

</dd> <dt>

<span data-ttu-id="df905-113">*加權* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="df905-113">*weights* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="df905-114">類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="df905-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="df905-115">取得由骨骼影響的加權陣列。</span><span class="sxs-lookup"><span data-stu-id="df905-115">Get the array of weights influenced by a bone.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df905-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="df905-116">Return value</span></span>

<span data-ttu-id="df905-117">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="df905-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="df905-118">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="df905-118">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="df905-119">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="df905-119">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="df905-120">備註</span><span class="sxs-lookup"><span data-stu-id="df905-120">Remarks</span></span>

<span data-ttu-id="df905-121">使用 [**ID3DXSkinInfo：： GetNumBoneInfluences**](id3dxskininfo--getnumboneinfluences.md) 來找出骨骼影響的頂點數目。</span><span class="sxs-lookup"><span data-stu-id="df905-121">Use [**ID3DXSkinInfo::GetNumBoneInfluences**](id3dxskininfo--getnumboneinfluences.md) to find out how many vertices the bone influences.</span></span>

## <a name="requirements"></a><span data-ttu-id="df905-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="df905-122">Requirements</span></span>



| <span data-ttu-id="df905-123">需求</span><span class="sxs-lookup"><span data-stu-id="df905-123">Requirement</span></span> | <span data-ttu-id="df905-124">值</span><span class="sxs-lookup"><span data-stu-id="df905-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="df905-125">標頭</span><span class="sxs-lookup"><span data-stu-id="df905-125">Header</span></span><br/>  | <dl> <span data-ttu-id="df905-126"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="df905-126"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="df905-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="df905-127">Library</span></span><br/> | <dl> <span data-ttu-id="df905-128"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="df905-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="df905-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="df905-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df905-130">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="df905-130">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="df905-131">**ID3DXSkinInfo::SetBoneInfluence**</span><span class="sxs-lookup"><span data-stu-id="df905-131">**ID3DXSkinInfo::SetBoneInfluence**</span></span>](id3dxskininfo--setboneinfluence.md)
</dt> </dl>

 

 

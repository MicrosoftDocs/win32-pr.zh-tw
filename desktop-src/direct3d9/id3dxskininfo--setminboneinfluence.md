---
description: 設定最小的骨骼影響。 影響小於此值的值會被忽略。
ms.assetid: 9af19c9e-bb6e-4f93-973f-5c38f88eea3d
title: 'ID3DXSkinInfo：： SetMinBoneInfluence 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.SetMinBoneInfluence
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 03e3aeeed31a58231644784ba5070bc9422f7820
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106997367"
---
# <a name="id3dxskininfosetminboneinfluence-method"></a><span data-ttu-id="4be4a-104">ID3DXSkinInfo：： SetMinBoneInfluence 方法</span><span class="sxs-lookup"><span data-stu-id="4be4a-104">ID3DXSkinInfo::SetMinBoneInfluence method</span></span>

<span data-ttu-id="4be4a-105">設定最小的骨骼影響。</span><span class="sxs-lookup"><span data-stu-id="4be4a-105">Sets the minimum bone influence.</span></span> <span data-ttu-id="4be4a-106">影響小於此值的值會被忽略。</span><span class="sxs-lookup"><span data-stu-id="4be4a-106">Influence values smaller than this are ignored.</span></span>

## <a name="syntax"></a><span data-ttu-id="4be4a-107">語法</span><span class="sxs-lookup"><span data-stu-id="4be4a-107">Syntax</span></span>


```C++
HRESULT SetMinBoneInfluence(
  [in] FLOAT MinInfl
);
```



## <a name="parameters"></a><span data-ttu-id="4be4a-108">參數</span><span class="sxs-lookup"><span data-stu-id="4be4a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4be4a-109">*MinInfl* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4be4a-109">*MinInfl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4be4a-110">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4be4a-110">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4be4a-111">最小影響值。</span><span class="sxs-lookup"><span data-stu-id="4be4a-111">Minimum influence value.</span></span> <span data-ttu-id="4be4a-112">影響小於此值的值會被忽略。</span><span class="sxs-lookup"><span data-stu-id="4be4a-112">Influence values smaller than this are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4be4a-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="4be4a-113">Return value</span></span>

<span data-ttu-id="4be4a-114">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4be4a-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4be4a-115">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="4be4a-115">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="4be4a-116">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="4be4a-116">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="4be4a-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="4be4a-117">Requirements</span></span>



| <span data-ttu-id="4be4a-118">需求</span><span class="sxs-lookup"><span data-stu-id="4be4a-118">Requirement</span></span> | <span data-ttu-id="4be4a-119">值</span><span class="sxs-lookup"><span data-stu-id="4be4a-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4be4a-120">標頭</span><span class="sxs-lookup"><span data-stu-id="4be4a-120">Header</span></span><br/>  | <dl> <span data-ttu-id="4be4a-121"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="4be4a-121"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="4be4a-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="4be4a-122">Library</span></span><br/> | <dl> <span data-ttu-id="4be4a-123"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="4be4a-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4be4a-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4be4a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4be4a-125">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="4be4a-125">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="4be4a-126">**ID3DXSkinInfo::GetMinBoneInfluence**</span><span class="sxs-lookup"><span data-stu-id="4be4a-126">**ID3DXSkinInfo::GetMinBoneInfluence**</span></span>](id3dxskininfo--getminboneinfluence.md)
</dt> </dl>

 

 

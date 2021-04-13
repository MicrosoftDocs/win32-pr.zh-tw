---
description: 取得骨骼位移矩陣。
ms.assetid: 99d47635-ffae-4668-a37c-b15442148fa1
title: 'ID3DXSkinInfo：： GetBoneOffsetMatrix 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetBoneOffsetMatrix
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: fce108dc1d0eb08f198ae9375ac35ed149c5e760
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322615"
---
# <a name="id3dxskininfogetboneoffsetmatrix-method"></a><span data-ttu-id="4c1f0-103">ID3DXSkinInfo：： GetBoneOffsetMatrix 方法</span><span class="sxs-lookup"><span data-stu-id="4c1f0-103">ID3DXSkinInfo::GetBoneOffsetMatrix method</span></span>

<span data-ttu-id="4c1f0-104">取得骨骼位移矩陣。</span><span class="sxs-lookup"><span data-stu-id="4c1f0-104">Gets the bone offset matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c1f0-105">語法</span><span class="sxs-lookup"><span data-stu-id="4c1f0-105">Syntax</span></span>


```C++
LPD3DXMATRIX GetBoneOffsetMatrix(
  [in] DWORD Bone
);
```



## <a name="parameters"></a><span data-ttu-id="4c1f0-106">參數</span><span class="sxs-lookup"><span data-stu-id="4c1f0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c1f0-107">*骨骼* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4c1f0-107">*Bone* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c1f0-108">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4c1f0-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4c1f0-109">骨骼編號。</span><span class="sxs-lookup"><span data-stu-id="4c1f0-109">Bone number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c1f0-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="4c1f0-110">Return value</span></span>

<span data-ttu-id="4c1f0-111">類型： **[ **LPD3DXMATRIX**](d3dxmatrix.md)**</span><span class="sxs-lookup"><span data-stu-id="4c1f0-111">Type: **[**LPD3DXMATRIX**](d3dxmatrix.md)**</span></span>

<span data-ttu-id="4c1f0-112">傳回骨骼位移矩陣的指標。</span><span class="sxs-lookup"><span data-stu-id="4c1f0-112">Returns a pointer to the bone offset matrix.</span></span> <span data-ttu-id="4c1f0-113">請勿釋放此指標。</span><span class="sxs-lookup"><span data-stu-id="4c1f0-113">Do not free this pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c1f0-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="4c1f0-114">Requirements</span></span>



| <span data-ttu-id="4c1f0-115">需求</span><span class="sxs-lookup"><span data-stu-id="4c1f0-115">Requirement</span></span> | <span data-ttu-id="4c1f0-116">值</span><span class="sxs-lookup"><span data-stu-id="4c1f0-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4c1f0-117">標頭</span><span class="sxs-lookup"><span data-stu-id="4c1f0-117">Header</span></span><br/>  | <dl> <span data-ttu-id="4c1f0-118"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="4c1f0-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="4c1f0-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="4c1f0-119">Library</span></span><br/> | <dl> <span data-ttu-id="4c1f0-120"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="4c1f0-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4c1f0-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4c1f0-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c1f0-122">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="4c1f0-122">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="4c1f0-123">**SetBoneOffsetMatrix**</span><span class="sxs-lookup"><span data-stu-id="4c1f0-123">**SetBoneOffsetMatrix**</span></span>](id3dxskininfo--setboneoffsetmatrix.md)
</dt> <dt>

[<span data-ttu-id="4c1f0-124">**GetNumBones**</span><span class="sxs-lookup"><span data-stu-id="4c1f0-124">**GetNumBones**</span></span>](id3dxskininfo--getnumbones.md)
</dt> </dl>

 

 

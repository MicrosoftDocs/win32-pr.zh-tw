---
description: 從骨骼索引取得骨骼名稱。
ms.assetid: f56faf41-c119-4cdd-bb8a-86fc99ff5893
title: 'ID3DXSkinInfo：： GetBoneName 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetBoneName
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0566d423d277dc3f39f36f8c1fda297ec917eb7f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106976683"
---
# <a name="id3dxskininfogetbonename-method"></a><span data-ttu-id="b50b3-103">ID3DXSkinInfo：： GetBoneName 方法</span><span class="sxs-lookup"><span data-stu-id="b50b3-103">ID3DXSkinInfo::GetBoneName method</span></span>

<span data-ttu-id="b50b3-104">從骨骼索引取得骨骼名稱。</span><span class="sxs-lookup"><span data-stu-id="b50b3-104">Gets the bone name, from the bone index.</span></span>

## <a name="syntax"></a><span data-ttu-id="b50b3-105">語法</span><span class="sxs-lookup"><span data-stu-id="b50b3-105">Syntax</span></span>


```C++
LPCSTR GetBoneName(
  [in] DWORD Bone
);
```



## <a name="parameters"></a><span data-ttu-id="b50b3-106">參數</span><span class="sxs-lookup"><span data-stu-id="b50b3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b50b3-107">*骨骼* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b50b3-107">*Bone* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b50b3-108">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b50b3-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b50b3-109">骨骼編號。</span><span class="sxs-lookup"><span data-stu-id="b50b3-109">Bone number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b50b3-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="b50b3-110">Return value</span></span>

<span data-ttu-id="b50b3-111">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b50b3-111">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b50b3-112">傳回骨骼名稱。</span><span class="sxs-lookup"><span data-stu-id="b50b3-112">Returns the bone name.</span></span> <span data-ttu-id="b50b3-113">請勿釋放這個字串。</span><span class="sxs-lookup"><span data-stu-id="b50b3-113">Do not free this string.</span></span>

## <a name="requirements"></a><span data-ttu-id="b50b3-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="b50b3-114">Requirements</span></span>



| <span data-ttu-id="b50b3-115">需求</span><span class="sxs-lookup"><span data-stu-id="b50b3-115">Requirement</span></span> | <span data-ttu-id="b50b3-116">值</span><span class="sxs-lookup"><span data-stu-id="b50b3-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b50b3-117">標頭</span><span class="sxs-lookup"><span data-stu-id="b50b3-117">Header</span></span><br/>  | <dl> <span data-ttu-id="b50b3-118"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="b50b3-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="b50b3-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="b50b3-119">Library</span></span><br/> | <dl> <span data-ttu-id="b50b3-120"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="b50b3-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b50b3-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b50b3-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b50b3-122">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="b50b3-122">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="b50b3-123">**ID3DXSkinInfo::SetBoneName**</span><span class="sxs-lookup"><span data-stu-id="b50b3-123">**ID3DXSkinInfo::SetBoneName**</span></span>](id3dxskininfo--setbonename.md)
</dt> <dt>

[<span data-ttu-id="b50b3-124">**ID3DXSkinInfo::GetNumBones**</span><span class="sxs-lookup"><span data-stu-id="b50b3-124">**ID3DXSkinInfo::GetNumBones**</span></span>](id3dxskininfo--getnumbones.md)
</dt> </dl>

 

 

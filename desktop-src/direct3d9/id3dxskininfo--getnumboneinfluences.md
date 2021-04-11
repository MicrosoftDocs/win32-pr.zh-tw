---
description: 取得骨骼的影響數目。
ms.assetid: 6383f990-2989-46b3-a634-b3bb7bd1d65b
title: 'ID3DXSkinInfo：： GetNumBoneInfluences 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetNumBoneInfluences
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 712f54b0459bc3e62c61b59d001a5d27dd5a8837
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196173"
---
# <a name="id3dxskininfogetnumboneinfluences-method"></a><span data-ttu-id="04660-103">ID3DXSkinInfo：： GetNumBoneInfluences 方法</span><span class="sxs-lookup"><span data-stu-id="04660-103">ID3DXSkinInfo::GetNumBoneInfluences method</span></span>

<span data-ttu-id="04660-104">取得骨骼的影響數目。</span><span class="sxs-lookup"><span data-stu-id="04660-104">Gets the number of influences for a bone.</span></span>

## <a name="syntax"></a><span data-ttu-id="04660-105">語法</span><span class="sxs-lookup"><span data-stu-id="04660-105">Syntax</span></span>


```C++
DWORD GetNumBoneInfluences(
  [in] DWORD bone
);
```



## <a name="parameters"></a><span data-ttu-id="04660-106">參數</span><span class="sxs-lookup"><span data-stu-id="04660-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04660-107">*骨骼* \[在\]</span><span class="sxs-lookup"><span data-stu-id="04660-107">*bone* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04660-108">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="04660-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="04660-109">骨骼編號。</span><span class="sxs-lookup"><span data-stu-id="04660-109">Bone number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04660-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="04660-110">Return value</span></span>

<span data-ttu-id="04660-111">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="04660-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="04660-112">傳回對骨骼的影響數目。</span><span class="sxs-lookup"><span data-stu-id="04660-112">Returns the number of influences for a bone.</span></span>

## <a name="requirements"></a><span data-ttu-id="04660-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="04660-113">Requirements</span></span>



| <span data-ttu-id="04660-114">需求</span><span class="sxs-lookup"><span data-stu-id="04660-114">Requirement</span></span> | <span data-ttu-id="04660-115">值</span><span class="sxs-lookup"><span data-stu-id="04660-115">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="04660-116">標頭</span><span class="sxs-lookup"><span data-stu-id="04660-116">Header</span></span><br/>  | <dl> <span data-ttu-id="04660-117"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="04660-117"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="04660-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="04660-118">Library</span></span><br/> | <dl> <span data-ttu-id="04660-119"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="04660-119"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="04660-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="04660-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04660-121">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="04660-121">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> </dl>

 

 

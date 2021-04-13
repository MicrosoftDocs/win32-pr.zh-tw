---
description: 取得固定的函式頂點值。
ms.assetid: 9b80c4b9-2e5b-4965-99b9-ad6c459ef413
title: 'ID3DXSkinInfo：： GetFVF 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetFVF
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6d48cd9cea6efd6cb43e6da6877a7aaf42909c71
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322604"
---
# <a name="id3dxskininfogetfvf-method"></a><span data-ttu-id="3c379-103">ID3DXSkinInfo：： GetFVF 方法</span><span class="sxs-lookup"><span data-stu-id="3c379-103">ID3DXSkinInfo::GetFVF method</span></span>

<span data-ttu-id="3c379-104">取得固定的函式頂點值。</span><span class="sxs-lookup"><span data-stu-id="3c379-104">Gets the fixed function vertex value.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c379-105">語法</span><span class="sxs-lookup"><span data-stu-id="3c379-105">Syntax</span></span>


```C++
DWORD GetFVF();
```



## <a name="parameters"></a><span data-ttu-id="3c379-106">參數</span><span class="sxs-lookup"><span data-stu-id="3c379-106">Parameters</span></span>

<span data-ttu-id="3c379-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="3c379-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3c379-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="3c379-108">Return value</span></span>

<span data-ttu-id="3c379-109">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3c379-109">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3c379-110">傳回彈性頂點格式 (FVF) 代碼。</span><span class="sxs-lookup"><span data-stu-id="3c379-110">Returns the flexible vertex format (FVF) codes.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c379-111">備註</span><span class="sxs-lookup"><span data-stu-id="3c379-111">Remarks</span></span>

<span data-ttu-id="3c379-112">如果頂點格式無法直接對應至 FVF 程式碼，則這個方法會傳回0。</span><span class="sxs-lookup"><span data-stu-id="3c379-112">This method can return 0 if the vertex format cannot be mapped directly to an FVF code.</span></span> <span data-ttu-id="3c379-113">這會發生在從頂點宣告所建立的網格中，這些 FVF 碼沒有相同的順序和元素支援。</span><span class="sxs-lookup"><span data-stu-id="3c379-113">This will occur for a mesh created from a vertex declaration that doesn't have the same order and elements supported by the FVF codes.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c379-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="3c379-114">Requirements</span></span>



| <span data-ttu-id="3c379-115">需求</span><span class="sxs-lookup"><span data-stu-id="3c379-115">Requirement</span></span> | <span data-ttu-id="3c379-116">值</span><span class="sxs-lookup"><span data-stu-id="3c379-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3c379-117">標頭</span><span class="sxs-lookup"><span data-stu-id="3c379-117">Header</span></span><br/>  | <dl> <span data-ttu-id="3c379-118"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="3c379-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="3c379-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="3c379-119">Library</span></span><br/> | <dl> <span data-ttu-id="3c379-120"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="3c379-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3c379-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3c379-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c379-122">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="3c379-122">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="3c379-123">**ID3DXSkinInfo::SetFVF**</span><span class="sxs-lookup"><span data-stu-id="3c379-123">**ID3DXSkinInfo::SetFVF**</span></span>](id3dxskininfo--setfvf.md)
</dt> </dl>

 

 

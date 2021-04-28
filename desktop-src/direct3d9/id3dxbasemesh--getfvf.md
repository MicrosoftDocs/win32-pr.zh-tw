---
description: ID3DXBaseMesh：： GetFVF 方法-取得固定的函式頂點值。
ms.assetid: ed56ff2d-0366-426c-9f9a-7d1a7c5d1a7c
title: 'ID3DXBaseMesh：： GetFVF 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GetFVF
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4e37db51238137d67ba6e060ecfafb7d1361727e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115436"
---
# <a name="id3dxbasemeshgetfvf-method"></a><span data-ttu-id="352dc-103">ID3DXBaseMesh：： GetFVF 方法</span><span class="sxs-lookup"><span data-stu-id="352dc-103">ID3DXBaseMesh::GetFVF method</span></span>

<span data-ttu-id="352dc-104">取得固定的函式頂點值。</span><span class="sxs-lookup"><span data-stu-id="352dc-104">Gets the fixed function vertex value.</span></span>

## <a name="syntax"></a><span data-ttu-id="352dc-105">語法</span><span class="sxs-lookup"><span data-stu-id="352dc-105">Syntax</span></span>


```C++
DWORD GetFVF();
```



## <a name="parameters"></a><span data-ttu-id="352dc-106">參數</span><span class="sxs-lookup"><span data-stu-id="352dc-106">Parameters</span></span>

<span data-ttu-id="352dc-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="352dc-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="352dc-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="352dc-108">Return value</span></span>

<span data-ttu-id="352dc-109">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="352dc-109">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="352dc-110">傳回彈性頂點格式 (FVF) 代碼。</span><span class="sxs-lookup"><span data-stu-id="352dc-110">Returns the flexible vertex format (FVF) codes.</span></span>

## <a name="remarks"></a><span data-ttu-id="352dc-111">備註</span><span class="sxs-lookup"><span data-stu-id="352dc-111">Remarks</span></span>

<span data-ttu-id="352dc-112">如果頂點格式無法直接對應至 FVF 程式碼，則這個方法會傳回0。</span><span class="sxs-lookup"><span data-stu-id="352dc-112">This method can return 0 if the vertex format cannot be mapped directly to an FVF code.</span></span> <span data-ttu-id="352dc-113">這會發生在從頂點宣告所建立的網格中，這些 FVF 碼沒有相同的順序和元素支援。</span><span class="sxs-lookup"><span data-stu-id="352dc-113">This will occur for a mesh created from a vertex declaration that doesn't have the same order and elements supported by the FVF codes.</span></span>

## <a name="requirements"></a><span data-ttu-id="352dc-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="352dc-114">Requirements</span></span>



| <span data-ttu-id="352dc-115">需求</span><span class="sxs-lookup"><span data-stu-id="352dc-115">Requirement</span></span> | <span data-ttu-id="352dc-116">值</span><span class="sxs-lookup"><span data-stu-id="352dc-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="352dc-117">標頭</span><span class="sxs-lookup"><span data-stu-id="352dc-117">Header</span></span><br/>  | <dl> <span data-ttu-id="352dc-118"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="352dc-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="352dc-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="352dc-119">Library</span></span><br/> | <dl> <span data-ttu-id="352dc-120"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="352dc-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="352dc-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="352dc-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="352dc-122">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="352dc-122">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 

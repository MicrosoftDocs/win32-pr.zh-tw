---
description: 頂點快取優化提示。
ms.assetid: 891624cd-03dd-4ddd-93f5-4899e1470325
title: 'D3DDEVINFO_VCACHE 結構 (D3D9Types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_VCACHE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 80870c330adf185a869ac5e3543055c82fc7115c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106982871"
---
# <a name="d3ddevinfo_vcache-structure"></a><span data-ttu-id="7883b-103">D3DDEVINFO \_ VCACHE 結構</span><span class="sxs-lookup"><span data-stu-id="7883b-103">D3DDEVINFO\_VCACHE structure</span></span>

<span data-ttu-id="7883b-104">頂點快取優化提示。</span><span class="sxs-lookup"><span data-stu-id="7883b-104">Vertex cache optimization hints.</span></span>

## <a name="syntax"></a><span data-ttu-id="7883b-105">語法</span><span class="sxs-lookup"><span data-stu-id="7883b-105">Syntax</span></span>


```C++
typedef struct D3DDEVINFO_VCACHE {
  DWORD Pattern;
  DWORD OptMethod;
  DWORD CacheSize;
  DWORD MagicNumber;
} D3DDEVINFO_VCACHE, *LPD3DDEVINFO_VCACHE;
```



## <a name="members"></a><span data-ttu-id="7883b-106">成員</span><span class="sxs-lookup"><span data-stu-id="7883b-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="7883b-107">**模式**</span><span class="sxs-lookup"><span data-stu-id="7883b-107">**Pattern**</span></span>
</dt> <dd>

<span data-ttu-id="7883b-108">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7883b-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7883b-109">位模式。</span><span class="sxs-lookup"><span data-stu-id="7883b-109">Bit pattern.</span></span> <span data-ttu-id="7883b-110">傳回值必須是 FOURCC ( ' C '、' A '、' C '、' H ' ) 。</span><span class="sxs-lookup"><span data-stu-id="7883b-110">Return value must be the FOURCC ('C', 'A', 'C', 'H').</span></span>

</dd> <dt>

<span data-ttu-id="7883b-111">**OptMethod**</span><span class="sxs-lookup"><span data-stu-id="7883b-111">**OptMethod**</span></span>
</dt> <dd>

<span data-ttu-id="7883b-112">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7883b-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7883b-113">優化方法。</span><span class="sxs-lookup"><span data-stu-id="7883b-113">Optimizations method.</span></span> <span data-ttu-id="7883b-114">使用0可取得最長的停車線。</span><span class="sxs-lookup"><span data-stu-id="7883b-114">Use 0 to get the longest strips.</span></span> <span data-ttu-id="7883b-115">使用1可優化頂點快取使用。</span><span class="sxs-lookup"><span data-stu-id="7883b-115">Use 1 to optimize the vertex cache usage.</span></span>

</dd> <dt>

<span data-ttu-id="7883b-116">**CacheSize**</span><span class="sxs-lookup"><span data-stu-id="7883b-116">**CacheSize**</span></span>
</dt> <dd>

<span data-ttu-id="7883b-117">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7883b-117">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7883b-118">用來作為優化目標的快取大小。</span><span class="sxs-lookup"><span data-stu-id="7883b-118">Cache size used as a target for optimization.</span></span> <span data-ttu-id="7883b-119">只有當 OptMethod 是1時，才需要此項。</span><span class="sxs-lookup"><span data-stu-id="7883b-119">This is required only if OptMethod is 1.</span></span>

</dd> <dt>

<span data-ttu-id="7883b-120">**MagicNumber**</span><span class="sxs-lookup"><span data-stu-id="7883b-120">**MagicNumber**</span></span>
</dt> <dd>

<span data-ttu-id="7883b-121">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7883b-121">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7883b-122">由內部優化方法用來決定何時要重新開機停車。</span><span class="sxs-lookup"><span data-stu-id="7883b-122">Used by internal optimization methods to determine when to restart strips.</span></span> <span data-ttu-id="7883b-123">這無法由使用者設定或修改。</span><span class="sxs-lookup"><span data-stu-id="7883b-123">This cannot be set or modified by a user.</span></span> <span data-ttu-id="7883b-124">只有當 OptMethod 是1時，才需要此項。</span><span class="sxs-lookup"><span data-stu-id="7883b-124">This is required only if OptMethod is 1.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7883b-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="7883b-125">Requirements</span></span>



| <span data-ttu-id="7883b-126">需求</span><span class="sxs-lookup"><span data-stu-id="7883b-126">Requirement</span></span> | <span data-ttu-id="7883b-127">值</span><span class="sxs-lookup"><span data-stu-id="7883b-127">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7883b-128">標頭</span><span class="sxs-lookup"><span data-stu-id="7883b-128">Header</span></span><br/> | <dl> <span data-ttu-id="7883b-129"><dt>D3D9Types。h</dt></span><span class="sxs-lookup"><span data-stu-id="7883b-129"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7883b-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7883b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7883b-131">Direct3D 結構</span><span class="sxs-lookup"><span data-stu-id="7883b-131">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="7883b-132">**GetData**</span><span class="sxs-lookup"><span data-stu-id="7883b-132">**GetData**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)
</dt> </dl>

 

 

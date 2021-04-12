---
description: 描述呈現介面。
ms.assetid: cffa1555-1fa2-427d-8bcb-da0e61d82152
title: 'D3DXRTS_DESC 結構 (D3dx9core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXRTS_DESC
api_type:
- HeaderDef
api_location:
- d3dx9core.h
ms.openlocfilehash: 3a0b52f258956f7b62734ca97cc5d1bf5ed00ac3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946089"
---
# <a name="d3dxrts_desc-structure"></a><span data-ttu-id="18f71-103">D3DXRTS \_ DESC 結構</span><span class="sxs-lookup"><span data-stu-id="18f71-103">D3DXRTS\_DESC structure</span></span>

<span data-ttu-id="18f71-104">描述呈現介面。</span><span class="sxs-lookup"><span data-stu-id="18f71-104">Describes a render surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="18f71-105">語法</span><span class="sxs-lookup"><span data-stu-id="18f71-105">Syntax</span></span>


```C++
typedef struct D3DXRTS_DESC {
  UINT      Width;
  UINT      Height;
  D3DFORMAT Format;
  BOOL      DepthStencil;
  D3DFORMAT DepthStencilFormat;
} D3DXRTS_DESC, *LPD3DXRTS_DESC;
```



## <a name="members"></a><span data-ttu-id="18f71-106">成員</span><span class="sxs-lookup"><span data-stu-id="18f71-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="18f71-107">**寬度**</span><span class="sxs-lookup"><span data-stu-id="18f71-107">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="18f71-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="18f71-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="18f71-109">呈現介面的寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="18f71-109">Width of the render surface, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="18f71-110">**高度**</span><span class="sxs-lookup"><span data-stu-id="18f71-110">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="18f71-111">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="18f71-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="18f71-112">轉譯介面的高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="18f71-112">Height of the render surface, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="18f71-113">**格式**</span><span class="sxs-lookup"><span data-stu-id="18f71-113">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="18f71-114">類型： **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="18f71-114">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="18f71-115">[D3DFORMAT](d3dformat.md)列舉型別的成員，描述呈現介面的像素格式。</span><span class="sxs-lookup"><span data-stu-id="18f71-115">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the pixel format of the render surface.</span></span>

</dd> <dt>

<span data-ttu-id="18f71-116">**DepthStencil**</span><span class="sxs-lookup"><span data-stu-id="18f71-116">**DepthStencil**</span></span>
</dt> <dd>

<span data-ttu-id="18f71-117">類型： **[ **BOOL**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="18f71-117">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="18f71-118">若 **為 TRUE**，表示呈現介面支援深度樣板表面;否則，此成員會設定為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="18f71-118">If **TRUE**, the render surface supports a depth-stencil surface; otherwise this member is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="18f71-119">**DepthStencilFormat**</span><span class="sxs-lookup"><span data-stu-id="18f71-119">**DepthStencilFormat**</span></span>
</dt> <dd>

<span data-ttu-id="18f71-120">類型： **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="18f71-120">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="18f71-121">如果 DepthStencil 設定為 **TRUE**，這個參數就是 [D3DFORMAT](d3dformat.md) 列舉型別的成員，它會描述呈現介面的深度樣板格式。</span><span class="sxs-lookup"><span data-stu-id="18f71-121">If DepthStencil is set to **TRUE**, this parameter is a member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the depth-stencil format of the render surface.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="18f71-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="18f71-122">Requirements</span></span>



| <span data-ttu-id="18f71-123">需求</span><span class="sxs-lookup"><span data-stu-id="18f71-123">Requirement</span></span> | <span data-ttu-id="18f71-124">值</span><span class="sxs-lookup"><span data-stu-id="18f71-124">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="18f71-125">標頭</span><span class="sxs-lookup"><span data-stu-id="18f71-125">Header</span></span><br/> | <dl> <span data-ttu-id="18f71-126"><dt>D3dx9core。h</dt></span><span class="sxs-lookup"><span data-stu-id="18f71-126"><dt>D3dx9core.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18f71-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="18f71-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18f71-128">D3DX 結構</span><span class="sxs-lookup"><span data-stu-id="18f71-128">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="18f71-129">**ID3DXRenderToSurface::GetDesc**</span><span class="sxs-lookup"><span data-stu-id="18f71-129">**ID3DXRenderToSurface::GetDesc**</span></span>](id3dxrendertosurface--getdesc.md)
</dt> </dl>

 

 

---
description: 顯示模式屬性的相關資訊。
ms.assetid: df9d12b9-7acb-435b-9d54-0b095c871f0e
title: 'D3DDISPLAYMODEEX 結構 (D3d9types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDISPLAYMODEEX
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 5906b6b23cc83e6d2379f0c5923b08b220285708
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106976470"
---
# <a name="d3ddisplaymodeex-structure"></a><span data-ttu-id="277d0-103">D3DDISPLAYMODEEX 結構</span><span class="sxs-lookup"><span data-stu-id="277d0-103">D3DDISPLAYMODEEX structure</span></span>

<span data-ttu-id="277d0-104">顯示模式屬性的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="277d0-104">Information about the properties of a display mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="277d0-105">語法</span><span class="sxs-lookup"><span data-stu-id="277d0-105">Syntax</span></span>


```C++
typedef struct {
  UINT                Size;
  UINT                Width;
  UINT                Height;
  UINT                RefreshRate;
  D3DFORMAT           Format;
  D3DSCANLINEORDERING ScanLineOrdering;
} D3DDISPLAYMODEEX;
```



## <a name="members"></a><span data-ttu-id="277d0-106">成員</span><span class="sxs-lookup"><span data-stu-id="277d0-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="277d0-107">**大小**</span><span class="sxs-lookup"><span data-stu-id="277d0-107">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="277d0-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="277d0-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="277d0-109">此結構的大小。</span><span class="sxs-lookup"><span data-stu-id="277d0-109">The size of this structure.</span></span> <span data-ttu-id="277d0-110">這應該一律設定為 sizeof (D3DDISPLAYMODEEX) 。</span><span class="sxs-lookup"><span data-stu-id="277d0-110">This should always be set to sizeof(D3DDISPLAYMODEEX).</span></span>

</dd> <dt>

<span data-ttu-id="277d0-111">**寬度**</span><span class="sxs-lookup"><span data-stu-id="277d0-111">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="277d0-112">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="277d0-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="277d0-113">顯示模式的寬度。</span><span class="sxs-lookup"><span data-stu-id="277d0-113">Width of the display mode.</span></span>

</dd> <dt>

<span data-ttu-id="277d0-114">**高度**</span><span class="sxs-lookup"><span data-stu-id="277d0-114">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="277d0-115">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="277d0-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="277d0-116">顯示模式的高度。</span><span class="sxs-lookup"><span data-stu-id="277d0-116">Height of the display mode.</span></span>

</dd> <dt>

<span data-ttu-id="277d0-117">**RefreshRate**</span><span class="sxs-lookup"><span data-stu-id="277d0-117">**RefreshRate**</span></span>
</dt> <dd>

<span data-ttu-id="277d0-118">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="277d0-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="277d0-119">顯示模式的更新速率。</span><span class="sxs-lookup"><span data-stu-id="277d0-119">Refresh rate of the display mode.</span></span>

</dd> <dt>

<span data-ttu-id="277d0-120">**格式**</span><span class="sxs-lookup"><span data-stu-id="277d0-120">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="277d0-121">類型： **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="277d0-121">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="277d0-122">顯示模式的格式。</span><span class="sxs-lookup"><span data-stu-id="277d0-122">Format of the display mode.</span></span> <span data-ttu-id="277d0-123">請參閱 [D3DFORMAT](d3dformat.md)。</span><span class="sxs-lookup"><span data-stu-id="277d0-123">See [D3DFORMAT](d3dformat.md).</span></span>

</dd> <dt>

<span data-ttu-id="277d0-124">**ScanLineOrdering**</span><span class="sxs-lookup"><span data-stu-id="277d0-124">**ScanLineOrdering**</span></span>
</dt> <dd>

<span data-ttu-id="277d0-125">類型： **[ **D3DSCANLINEORDERING**](./d3dscanlineordering.md)**</span><span class="sxs-lookup"><span data-stu-id="277d0-125">Type: **[**D3DSCANLINEORDERING**](./d3dscanlineordering.md)**</span></span>

</dd> <dd>

<span data-ttu-id="277d0-126">指出 scanline 順序是漸進式或交錯式。</span><span class="sxs-lookup"><span data-stu-id="277d0-126">Indicates whether the scanline order is progressive or interlaced.</span></span> <span data-ttu-id="277d0-127">請參閱 [**D3DSCANLINEORDERING**](./d3dscanlineordering.md)。</span><span class="sxs-lookup"><span data-stu-id="277d0-127">See [**D3DSCANLINEORDERING**](./d3dscanlineordering.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="277d0-128">備註</span><span class="sxs-lookup"><span data-stu-id="277d0-128">Remarks</span></span>

<span data-ttu-id="277d0-129">此結構用於各種方法中，以建立和管理 Direct3D 9Ex 裝置 ([**IDirect3DDevice9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9ex)) 和 Swapchains ([**IDirect3DSwapChain9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dswapchain9ex)) 。</span><span class="sxs-lookup"><span data-stu-id="277d0-129">This structure is used in various methods to create and manage Direct3D 9Ex devices ([**IDirect3DDevice9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9ex)) and swapchains ([**IDirect3DSwapChain9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dswapchain9ex)).</span></span>

## <a name="requirements"></a><span data-ttu-id="277d0-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="277d0-130">Requirements</span></span>



| <span data-ttu-id="277d0-131">需求</span><span class="sxs-lookup"><span data-stu-id="277d0-131">Requirement</span></span> | <span data-ttu-id="277d0-132">值</span><span class="sxs-lookup"><span data-stu-id="277d0-132">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="277d0-133">標頭</span><span class="sxs-lookup"><span data-stu-id="277d0-133">Header</span></span><br/> | <dl> <span data-ttu-id="277d0-134"><dt>D3d9types。h</dt></span><span class="sxs-lookup"><span data-stu-id="277d0-134"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="277d0-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="277d0-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="277d0-136">Direct3D 結構</span><span class="sxs-lookup"><span data-stu-id="277d0-136">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 

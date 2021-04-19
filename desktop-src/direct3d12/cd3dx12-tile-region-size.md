---
title: 'CD3DX12_TILE_REGION_SIZE 結構 (D3dx12 .h) '
description: 協助程式結構，可讓您輕鬆地初始化 D3D12 \_ 圖格 \_ 區域 \_ 大小結構。
ms.assetid: 07D2D8DE-C35C-48EE-8E9E-36545B60C594
keywords:
- CD3DX12_TILE_REGION_SIZE 結構
topic_type:
- apiref
api_name:
- CD3DX12_TILE_REGION_SIZE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40f64046f2a7efa32af8b43adbcf7349f43b6ec3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106998997"
---
# <a name="cd3dx12_tile_region_size-structure"></a><span data-ttu-id="5c651-104">CD3DX12 \_ 圖格 \_ 區域 \_ 大小結構</span><span class="sxs-lookup"><span data-stu-id="5c651-104">CD3DX12\_TILE\_REGION\_SIZE structure</span></span>

<span data-ttu-id="5c651-105">協助程式結構，可讓您輕鬆地初始化 [**D3D12 \_ 圖格 \_ 區域 \_ 大小**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size) 結構。</span><span class="sxs-lookup"><span data-stu-id="5c651-105">A helper structure to enable easy initialization of a [**D3D12\_TILE\_REGION\_SIZE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c651-106">語法</span><span class="sxs-lookup"><span data-stu-id="5c651-106">Syntax</span></span>


```C++
struct CD3DX12_TILE_REGION_SIZE  : public D3D12_TILE_REGION_SIZE{
   CD3DX12_TILE_REGION_SIZE();
   explicit CD3DX12_TILE_REGION_SIZE(const D3D12_TILE_REGION_SIZE &o);
   CD3DX12_TILE_REGION_SIZE(UINT numTiles, BOOL useBox, UINT width, UINT16 height, UINT16 depth);
   operator const D3D12_TILE_REGION_SIZE&() const;
};
```



## <a name="members"></a><span data-ttu-id="5c651-107">成員</span><span class="sxs-lookup"><span data-stu-id="5c651-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="5c651-108">**CD3DX12 \_ 圖格 \_ 區域 \_ 大小 ()**</span><span class="sxs-lookup"><span data-stu-id="5c651-108">**CD3DX12\_TILE\_REGION\_SIZE()**</span></span>
</dt> <dd>

<span data-ttu-id="5c651-109">建立 CD3DX12 圖格區域大小的新、未初始化的實例 \_ \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="5c651-109">Creates a new, uninitialized, instance of a CD3DX12\_TILE\_REGION\_SIZE.</span></span>

</dd> <dt>

<span data-ttu-id="5c651-110">**明確的 CD3DX12 \_ 圖格 \_ 區域 \_ 大小 (const D3D12 \_ 磚 \_ 區域 \_ 大小 &o)**</span><span class="sxs-lookup"><span data-stu-id="5c651-110">**explicit CD3DX12\_TILE\_REGION\_SIZE(const D3D12\_TILE\_REGION\_SIZE &o)**</span></span>
</dt> <dd>

<span data-ttu-id="5c651-111">建立 CD3DX12 \_ 圖 \_ 格區域大小的新實例 \_ ，並以另一個 [**D3D12 \_ 磚 \_ 區域 \_ 大小**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size) 結構的內容進行初始化。</span><span class="sxs-lookup"><span data-stu-id="5c651-111">Creates a new instance of a CD3DX12\_TILE\_REGION\_SIZE, initialized with the contents of another [**D3D12\_TILE\_REGION\_SIZE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size) structure.</span></span>

</dd> <dt>

<span data-ttu-id="5c651-112">**CD3DX12 \_ 圖格 \_ 區域 \_ 大小 (UINT NumTiles、BOOL useBox、UINT width、UINT16 height、uint16 depth)**</span><span class="sxs-lookup"><span data-stu-id="5c651-112">**CD3DX12\_TILE\_REGION\_SIZE(UINT numTiles, BOOL useBox, UINT width, UINT16 height, UINT16 depth)**</span></span>
</dt> <dd>

<span data-ttu-id="5c651-113">建立 CD3DX12 圖格區域大小的新實例 \_ \_ ，並 \_ 初始化下列參數：</span><span class="sxs-lookup"><span data-stu-id="5c651-113">Creates a new instance of a CD3DX12\_TILE\_REGION\_SIZE, initializing the following parameters:</span></span>

<span data-ttu-id="5c651-114">UINT numTiles</span><span class="sxs-lookup"><span data-stu-id="5c651-114">UINT numTiles</span></span>

<span data-ttu-id="5c651-115">BOOL useBox</span><span class="sxs-lookup"><span data-stu-id="5c651-115">BOOL useBox</span></span>

<span data-ttu-id="5c651-116">UINT 寬度</span><span class="sxs-lookup"><span data-stu-id="5c651-116">UINT width</span></span>

<span data-ttu-id="5c651-117">UINT16 高度</span><span class="sxs-lookup"><span data-stu-id="5c651-117">UINT16 height</span></span>

<span data-ttu-id="5c651-118">UINT16 深度</span><span class="sxs-lookup"><span data-stu-id="5c651-118">UINT16 depth</span></span>

</dd> <dt>

<span data-ttu-id="5c651-119">**運算子 const D3D12 \_ 圖格 \_ 區域 \_ 大小& () const**</span><span class="sxs-lookup"><span data-stu-id="5c651-119">**operator const D3D12\_TILE\_REGION\_SIZE&() const**</span></span>
</dt> <dd>

<span data-ttu-id="5c651-120">針對父結構類型定義 & 的傳址運算子。</span><span class="sxs-lookup"><span data-stu-id="5c651-120">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5c651-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="5c651-121">Requirements</span></span>



| <span data-ttu-id="5c651-122">需求</span><span class="sxs-lookup"><span data-stu-id="5c651-122">Requirement</span></span> | <span data-ttu-id="5c651-123">值</span><span class="sxs-lookup"><span data-stu-id="5c651-123">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5c651-124">標頭</span><span class="sxs-lookup"><span data-stu-id="5c651-124">Header</span></span><br/> | <dl> <span data-ttu-id="5c651-125"><dt>D3dx12。h</dt></span><span class="sxs-lookup"><span data-stu-id="5c651-125"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c651-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5c651-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c651-127">**D3D12 \_ 圖格 \_ 區域 \_ 大小**</span><span class="sxs-lookup"><span data-stu-id="5c651-127">**D3D12\_TILE\_REGION\_SIZE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size)
</dt> <dt>

[<span data-ttu-id="5c651-128">D3D12 的 Helper 結構</span><span class="sxs-lookup"><span data-stu-id="5c651-128">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 






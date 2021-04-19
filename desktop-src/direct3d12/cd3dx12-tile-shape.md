---
title: 'CD3DX12_TILE_SHAPE 結構 (D3dx12 .h) '
description: 協助程式結構，可讓您輕鬆地初始化 D3D12 \_ 圖格 \_ 圖形結構。
ms.assetid: 0A5963F1-8CE5-4B03-B69F-83B2B801CC21
keywords:
- CD3DX12_TILE_SHAPE 結構
topic_type:
- apiref
api_name:
- CD3DX12_TILE_SHAPE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 998a14e1bd4898d83d049ea50bc056abaeb68544
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106992295"
---
# <a name="cd3dx12_tile_shape-structure"></a><span data-ttu-id="6bb4d-104">CD3DX12 \_ 圖格 \_ 圖形結構</span><span class="sxs-lookup"><span data-stu-id="6bb4d-104">CD3DX12\_TILE\_SHAPE structure</span></span>

<span data-ttu-id="6bb4d-105">協助程式結構，可讓您輕鬆地初始化 [**D3D12 \_ 圖格 \_ 圖形**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_shape) 結構。</span><span class="sxs-lookup"><span data-stu-id="6bb4d-105">A helper structure to enable easy initialization of a [**D3D12\_TILE\_SHAPE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_shape) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="6bb4d-106">語法</span><span class="sxs-lookup"><span data-stu-id="6bb4d-106">Syntax</span></span>


```C++
struct CD3DX12_TILE_SHAPE  : public D3D12_TILE_SHAPE{
   CD3DX12_TILE_SHAPE();
   explicit CD3DX12_TILE_SHAPE(const D3D12_TILE_SHAPE &o);
   CD3DX12_TILE_SHAPE(UINT widthInTexels, UINT heightInTexels, UINT depthInTexels);
   operator const D3D12_TILE_SHAPE&() const;
};
```



## <a name="members"></a><span data-ttu-id="6bb4d-107">成員</span><span class="sxs-lookup"><span data-stu-id="6bb4d-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="6bb4d-108">**CD3DX12 \_ 圖格 \_ 圖形 ()**</span><span class="sxs-lookup"><span data-stu-id="6bb4d-108">**CD3DX12\_TILE\_SHAPE()**</span></span>
</dt> <dd>

<span data-ttu-id="6bb4d-109">建立新的、未初始化的 CD3DX12 圖格 \_ \_ 圖形實例。</span><span class="sxs-lookup"><span data-stu-id="6bb4d-109">Creates a new, uninitialized, instance of a CD3DX12\_TILE\_SHAPE.</span></span>

</dd> <dt>

<span data-ttu-id="6bb4d-110">**明確的 CD3DX12 \_ 圖格 \_ 圖形 (const D3D12 \_ 磚 \_ 圖形 &o)**</span><span class="sxs-lookup"><span data-stu-id="6bb4d-110">**explicit CD3DX12\_TILE\_SHAPE(const D3D12\_TILE\_SHAPE &o)**</span></span>
</dt> <dd>

<span data-ttu-id="6bb4d-111">建立 CD3DX12 \_ 圖格圖形的新實例 \_ ，並使用另一個 [**D3D12 \_ 磚 \_ 圖形**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_shape) 結構的內容進行初始化。</span><span class="sxs-lookup"><span data-stu-id="6bb4d-111">Creates a new instance of a CD3DX12\_TILE\_SHAPE, initialized with the contents of another [**D3D12\_TILE\_SHAPE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_shape) structure.</span></span>

</dd> <dt>

<span data-ttu-id="6bb4d-112">**CD3DX12 \_ 圖格 \_ 圖形 (uint WIDTHINTEXELS、uint HEIGHTINTEXELS、uint depthInTexels)**</span><span class="sxs-lookup"><span data-stu-id="6bb4d-112">**CD3DX12\_TILE\_SHAPE(UINT widthInTexels, UINT heightInTexels, UINT depthInTexels)**</span></span>
</dt> <dd>

<span data-ttu-id="6bb4d-113">建立 CD3DX12 圖格圖形的新 \_ 實例 \_ ，並初始化下列參數：</span><span class="sxs-lookup"><span data-stu-id="6bb4d-113">Creates a new instance of a CD3DX12\_TILE\_SHAPE, initializing the following parameters:</span></span>

<span data-ttu-id="6bb4d-114">UINT widthInTexels</span><span class="sxs-lookup"><span data-stu-id="6bb4d-114">UINT widthInTexels</span></span>

<span data-ttu-id="6bb4d-115">UINT heightInTexels</span><span class="sxs-lookup"><span data-stu-id="6bb4d-115">UINT heightInTexels</span></span>

<span data-ttu-id="6bb4d-116">UINT depthInTexels</span><span class="sxs-lookup"><span data-stu-id="6bb4d-116">UINT depthInTexels</span></span>

</dd> <dt>

<span data-ttu-id="6bb4d-117">**operator const D3D12 \_ 圖格 \_ 圖形& () const**</span><span class="sxs-lookup"><span data-stu-id="6bb4d-117">**operator const D3D12\_TILE\_SHAPE&() const**</span></span>
</dt> <dd>

<span data-ttu-id="6bb4d-118">針對父結構類型定義 & 的傳址運算子。</span><span class="sxs-lookup"><span data-stu-id="6bb4d-118">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6bb4d-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="6bb4d-119">Requirements</span></span>



| <span data-ttu-id="6bb4d-120">需求</span><span class="sxs-lookup"><span data-stu-id="6bb4d-120">Requirement</span></span> | <span data-ttu-id="6bb4d-121">值</span><span class="sxs-lookup"><span data-stu-id="6bb4d-121">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6bb4d-122">標頭</span><span class="sxs-lookup"><span data-stu-id="6bb4d-122">Header</span></span><br/> | <dl> <span data-ttu-id="6bb4d-123"><dt>D3dx12。h</dt></span><span class="sxs-lookup"><span data-stu-id="6bb4d-123"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6bb4d-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6bb4d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bb4d-125">**D3D12 \_ 圖格 \_ 圖形**</span><span class="sxs-lookup"><span data-stu-id="6bb4d-125">**D3D12\_TILE\_SHAPE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_shape)
</dt> <dt>

[<span data-ttu-id="6bb4d-126">D3D12 的 Helper 結構</span><span class="sxs-lookup"><span data-stu-id="6bb4d-126">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 






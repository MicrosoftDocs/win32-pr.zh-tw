---
title: 'CD3DX12_VIEWPORT 結構 (D3dx12 .h) '
description: 協助程式結構，可讓您輕鬆地初始化 D3D12 的 \_ 視口結構。
ms.assetid: 1A824F54-596B-450E-A191-B60FBBBB60ED
keywords:
- CD3DX12_VIEWPORT 結構
topic_type:
- apiref
api_name:
- CD3DX12_VIEWPORT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da29adc50b62bd645070d9667bec1e5c7ce7ab15
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106985911"
---
# <a name="cd3dx12_viewport-structure"></a><span data-ttu-id="171c5-104">CD3DX12 的 \_ 視口結構</span><span class="sxs-lookup"><span data-stu-id="171c5-104">CD3DX12\_VIEWPORT structure</span></span>

<span data-ttu-id="171c5-105">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="171c5-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="171c5-106">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="171c5-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="171c5-107">協助程式結構，可讓您輕鬆地初始化 [**D3D12 的 \_ 視口**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_viewport) 結構。</span><span class="sxs-lookup"><span data-stu-id="171c5-107">A helper structure to enable easy initialization of a [**D3D12\_VIEWPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_viewport) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="171c5-108">語法</span><span class="sxs-lookup"><span data-stu-id="171c5-108">Syntax</span></span>


```C++
struct CD3DX12_VIEWPORT  : public D3D12_VIEWPORT{
   CD3DX12_VIEWPORT();
   explicit CD3DX12_VIEWPORT(const D3D12_VIEWPORT& o);
   explicit CD3DX12_VIEWPORT(FLOAT topLeftX, FLOAT topLeftY, FLOAT width, FLOAT height, FLOAT minDepth = D3D12_MIN_DEPTH, FLOAT maxDepth = D3D12_MAX_DEPTH);
   explicit CD3DX12_VIEWPORT(ID3D12Resource* pResource, UINT mipSlice = 0, FLOAT topLeftX = 0.0f, FLOAT topLeftY = 0.0f, FLOAT minDepth = D3D12_MIN_DEPTH, FLOAT maxDepth = D3D12_MAX_DEPTH);
   ~CD3DX12_VIEWPORT();
   operator const D3D12_VIEWPORT&() const;
};
```



## <a name="members"></a><span data-ttu-id="171c5-109">成員</span><span class="sxs-lookup"><span data-stu-id="171c5-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="171c5-110">**CD3DX12 \_ 視口 ()**</span><span class="sxs-lookup"><span data-stu-id="171c5-110">**CD3DX12\_VIEWPORT()**</span></span>
</dt> <dd>

<span data-ttu-id="171c5-111">建立 CD3DX12 區的新、未初始化的實例 \_ 。</span><span class="sxs-lookup"><span data-stu-id="171c5-111">Creates a new, uninitialized, instance of a CD3DX12\_VIEWPORT.</span></span>

</dd> <dt>

<span data-ttu-id="171c5-112">**明確的 CD3DX12 \_ 區 (CONST D3D12 \_ 視口& o)**</span><span class="sxs-lookup"><span data-stu-id="171c5-112">**explicit CD3DX12\_VIEWPORT(const D3D12\_VIEWPORT& o)**</span></span>
</dt> <dd>

<span data-ttu-id="171c5-113">建立 CD3DX12 區的新實例 \_ ，並初始化下列參數：</span><span class="sxs-lookup"><span data-stu-id="171c5-113">Creates a new instance of a CD3DX12\_VIEWPORT, initializing the following parameters:</span></span>

<span data-ttu-id="171c5-114">const D3D12 \_ 視口& o</span><span class="sxs-lookup"><span data-stu-id="171c5-114">const D3D12\_VIEWPORT& o</span></span>

</dd> <dt>

<span data-ttu-id="171c5-115">**明確的 CD3DX12 \_ 區 (Float topLeftX、Float topLeftY、float width、float height、Float minDepth = D3D12 \_ MIN \_ Depth、FLOAT maxDepth = D3D12 \_ MAX \_ depth)**</span><span class="sxs-lookup"><span data-stu-id="171c5-115">**explicit CD3DX12\_VIEWPORT(FLOAT topLeftX, FLOAT topLeftY, FLOAT width, FLOAT height, FLOAT minDepth = D3D12\_MIN\_DEPTH, FLOAT maxDepth = D3D12\_MAX\_DEPTH)**</span></span>
</dt> <dd>

<span data-ttu-id="171c5-116">建立 CD3DX12 區的新實例 \_ ，並初始化下列參數：</span><span class="sxs-lookup"><span data-stu-id="171c5-116">Creates a new instance of a CD3DX12\_VIEWPORT, initializing the following parameters:</span></span>

<span data-ttu-id="171c5-117">FLOAT topLeftX</span><span class="sxs-lookup"><span data-stu-id="171c5-117">FLOAT topLeftX</span></span>

<span data-ttu-id="171c5-118">FLOAT topLeftY</span><span class="sxs-lookup"><span data-stu-id="171c5-118">FLOAT topLeftY</span></span>

<span data-ttu-id="171c5-119">浮點數寬度</span><span class="sxs-lookup"><span data-stu-id="171c5-119">FLOAT width</span></span>

<span data-ttu-id="171c5-120">浮點數高度</span><span class="sxs-lookup"><span data-stu-id="171c5-120">FLOAT height</span></span>

<span data-ttu-id="171c5-121">FLOAT minDepth = D3D12 \_ MIN \_ DEPTH</span><span class="sxs-lookup"><span data-stu-id="171c5-121">FLOAT minDepth = D3D12\_MIN\_DEPTH</span></span>

<span data-ttu-id="171c5-122">FLOAT maxDepth = D3D12 \_ 最大 \_ 深度</span><span class="sxs-lookup"><span data-stu-id="171c5-122">FLOAT maxDepth = D3D12\_MAX\_DEPTH</span></span>

</dd> <dt>

<span data-ttu-id="171c5-123">**明確 \_ 的 CD3DX12 區 (ID3D12Resource \* PRESOURCE，UINT mipSlice = 0，FLOAT topLeftX = 0.0 f，float topLeftY = 0.0 f，FLOAT MINDEPTH = D3D12 \_ MIN \_ depth，float maxDepth = D3D12 \_ MAX \_ depth)**</span><span class="sxs-lookup"><span data-stu-id="171c5-123">**explicit CD3DX12\_VIEWPORT(ID3D12Resource\* pResource, UINT mipSlice = 0, FLOAT topLeftX = 0.0f, FLOAT topLeftY = 0.0f, FLOAT minDepth = D3D12\_MIN\_DEPTH, FLOAT maxDepth = D3D12\_MAX\_DEPTH)**</span></span>
</dt> <dd>

<span data-ttu-id="171c5-124">建立 CD3DX12 區的新實例 \_ ，並初始化下列參數：</span><span class="sxs-lookup"><span data-stu-id="171c5-124">Creates a new instance of a CD3DX12\_VIEWPORT, initializing the following parameters:</span></span>

<span data-ttu-id="171c5-125">ID3D12Resource \* pResource</span><span class="sxs-lookup"><span data-stu-id="171c5-125">ID3D12Resource\* pResource</span></span>

<span data-ttu-id="171c5-126">UINT mipSlice = 0</span><span class="sxs-lookup"><span data-stu-id="171c5-126">UINT mipSlice = 0</span></span>

<span data-ttu-id="171c5-127">FLOAT topLeftX = 0.0 f</span><span class="sxs-lookup"><span data-stu-id="171c5-127">FLOAT topLeftX = 0.0f</span></span>

<span data-ttu-id="171c5-128">FLOAT topLeftY = 0.0 f</span><span class="sxs-lookup"><span data-stu-id="171c5-128">FLOAT topLeftY = 0.0f</span></span>

<span data-ttu-id="171c5-129">FLOAT minDepth = D3D12 \_ MIN \_ DEPTH</span><span class="sxs-lookup"><span data-stu-id="171c5-129">FLOAT minDepth = D3D12\_MIN\_DEPTH</span></span>

<span data-ttu-id="171c5-130">FLOAT maxDepth = D3D12 \_ 最大 \_ 深度</span><span class="sxs-lookup"><span data-stu-id="171c5-130">FLOAT maxDepth = D3D12\_MAX\_DEPTH</span></span>

</dd> <dt>

<span data-ttu-id="171c5-131">**~ CD3DX12 的 \_ 視口 ()**</span><span class="sxs-lookup"><span data-stu-id="171c5-131">**~CD3DX12\_VIEWPORT()**</span></span>
</dt> <dd>

<span data-ttu-id="171c5-132">終結 D3DX12 區的實例 \_ 。</span><span class="sxs-lookup"><span data-stu-id="171c5-132">Destroys an instance of a D3DX12\_VIEWPORT.</span></span>

</dd> <dt>

<span data-ttu-id="171c5-133">**運算子 const D3D12 \_ 視口& () const**</span><span class="sxs-lookup"><span data-stu-id="171c5-133">**operator const D3D12\_VIEWPORT&() const**</span></span>
</dt> <dd>

<span data-ttu-id="171c5-134">針對父結構類型定義 & 的傳址運算子。</span><span class="sxs-lookup"><span data-stu-id="171c5-134">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="171c5-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="171c5-135">Requirements</span></span>



| <span data-ttu-id="171c5-136">需求</span><span class="sxs-lookup"><span data-stu-id="171c5-136">Requirement</span></span> | <span data-ttu-id="171c5-137">值</span><span class="sxs-lookup"><span data-stu-id="171c5-137">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="171c5-138">標頭</span><span class="sxs-lookup"><span data-stu-id="171c5-138">Header</span></span><br/> | <dl> <span data-ttu-id="171c5-139"><dt>D3dx12。h</dt></span><span class="sxs-lookup"><span data-stu-id="171c5-139"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="171c5-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="171c5-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="171c5-141">**D3D12 \_ 區**</span><span class="sxs-lookup"><span data-stu-id="171c5-141">**D3D12\_VIEWPORT**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_viewport)
</dt> <dt>

[<span data-ttu-id="171c5-142">D3D12 的 Helper 結構</span><span class="sxs-lookup"><span data-stu-id="171c5-142">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 






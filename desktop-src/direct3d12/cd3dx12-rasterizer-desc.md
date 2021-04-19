---
title: 'CD3DX12_RASTERIZER_DESC 結構 (D3dx12 .h) '
description: 協助程式結構，可讓您輕鬆地初始化 D3D12 的轉譯器 \_ \_ DESC 結構。
ms.assetid: 28AA8256-1CAF-484F-B219-0F0461BA947C
keywords:
- CD3DX12_RASTERIZER_DESC 結構
topic_type:
- apiref
api_name:
- CD3DX12_RASTERIZER_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 078b9e92d25cb5309b4cd97d35586192a37eed90
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106981991"
---
# <a name="cd3dx12_rasterizer_desc-structure"></a><span data-ttu-id="7c4c8-104">CD3DX12 轉譯器 \_ \_ DESC 結構</span><span class="sxs-lookup"><span data-stu-id="7c4c8-104">CD3DX12\_RASTERIZER\_DESC structure</span></span>

<span data-ttu-id="7c4c8-105">協助程式結構，可讓您輕鬆地初始化 D3D12 的轉譯器 [**\_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc) 結構。</span><span class="sxs-lookup"><span data-stu-id="7c4c8-105">A helper structure to enable easy initialization of a [**D3D12\_RASTERIZER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c4c8-106">語法</span><span class="sxs-lookup"><span data-stu-id="7c4c8-106">Syntax</span></span>


```C++
struct CD3DX12_RASTERIZER_DESC  : public D3D12_RASTERIZER_DESC{
   CD3DX12_RASTERIZER_DESC();
   explicit CD3DX12_RASTERIZER_DESC(const D3D12_RASTERIZER_DESC& o);
   explicit CD3DX12_RASTERIZER_DESC(CD3DX12_DEFAULT);
   explicit CD3DX12_RASTERIZER_DESC(D3D12_FILL_MODE fillMode, D3D12_CULL_MODE cullMode, BOOL frontCounterClockwise, INT depthBias, FLOAT depthBiasClamp, FLOAT slopeScaledDepthBias, BOOL depthClipEnable, BOOL multisampleEnable, BOOL antialiasedLineEnable, UINT forcedSampleCount, D3D12_CONSERVATIVE_RASTERIZATION_MODE conservativeRaster);
   ~CD3DX12_RASTERIZER_DESC();
   operator const D3D12_RASTERIZER_DESC&() const;
};
```



## <a name="members"></a><span data-ttu-id="7c4c8-107">成員</span><span class="sxs-lookup"><span data-stu-id="7c4c8-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="7c4c8-108">**CD3DX12 轉譯器 \_ \_ DESC ()**</span><span class="sxs-lookup"><span data-stu-id="7c4c8-108">**CD3DX12\_RASTERIZER\_DESC()**</span></span>
</dt> <dd>

<span data-ttu-id="7c4c8-109">建立新的、未初始化的 CD3DX12 轉譯器 \_ \_ DESC 實例。</span><span class="sxs-lookup"><span data-stu-id="7c4c8-109">Creates a new, uninitialized, instance of a CD3DX12\_RASTERIZER\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="7c4c8-110">**明確的 CD3DX12 轉譯器 \_ \_ desc (const D3D12 轉譯器 \_ \_ desc& o)**</span><span class="sxs-lookup"><span data-stu-id="7c4c8-110">**explicit CD3DX12\_RASTERIZER\_DESC(const D3D12\_RASTERIZER\_DESC& o)**</span></span>
</dt> <dd>

<span data-ttu-id="7c4c8-111">建立 CD3DX12 轉譯器 desc 的新 \_ 實例 \_ ，並以另一個 D3D12 的轉譯 [**器 \_ \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc) 結構的內容進行初始化。</span><span class="sxs-lookup"><span data-stu-id="7c4c8-111">Creates a new instance of a CD3DX12\_RASTERIZER\_DESC, initialized with the contents of another [**D3D12\_RASTERIZER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc) structure.</span></span>

</dd> <dt>

<span data-ttu-id="7c4c8-112">**明確的 CD3DX12 轉譯器 \_ \_ DESC (CD3DX12 \_ 預設)**</span><span class="sxs-lookup"><span data-stu-id="7c4c8-112">**explicit CD3DX12\_RASTERIZER\_DESC(CD3DX12\_DEFAULT)**</span></span>
</dt> <dd>

<span data-ttu-id="7c4c8-113">建立 CD3DX12 轉譯器 DESC 的新 \_ 實例 \_ ，並以預設參數初始化。</span><span class="sxs-lookup"><span data-stu-id="7c4c8-113">Creates a new instance of a CD3DX12\_RASTERIZER\_DESC, initialized with default parameters.</span></span>

``` syntax
        FillMode = D3D12_FILL_MODE_SOLID;  
        CullMode = D3D12_CULL_MODE_BACK;  
        FrontCounterClockwise = FALSE;  
        DepthBias = D3D12_DEFAULT_DEPTH_BIAS;  
        DepthBiasClamp = D3D12_DEFAULT_DEPTH_BIAS_CLAMP;  
        SlopeScaledDepthBias = D3D12_DEFAULT_SLOPE_SCALED_DEPTH_BIAS;  
        DepthClipEnable = TRUE;  
        MultisampleEnable = FALSE;  
        AntialiasedLineEnable = FALSE;  
        ForcedSampleCount = 0;  
        ConservativeRaster = D3D12_CONSERVATIVE_RASTERIZATION_MODE_OFF;  
```

</dd> <dt>

<span data-ttu-id="7c4c8-114">**明確的 CD3DX12 轉譯器 \_ \_ DESC (D3D12 \_ FILL \_ mode fillMode、D3D12 \_ 剔除 \_ MODE CullMode、BOOL FrontCounterClockwise、INT DepthBias、FLOAT DepthBiasClamp、FLOAT SlopeScaledDepthBias、BOOL DepthClipEnable、BOOL MultisampleEnable、BOOL antialiasedLineEnable、UINT forcedSampleCount、D3D12 保守式點陣 \_ \_ \_ 模式 conservativeRaster)**</span><span class="sxs-lookup"><span data-stu-id="7c4c8-114">**explicit CD3DX12\_RASTERIZER\_DESC(D3D12\_FILL\_MODE fillMode, D3D12\_CULL\_MODE cullMode, BOOL frontCounterClockwise, INT depthBias, FLOAT depthBiasClamp, FLOAT slopeScaledDepthBias, BOOL depthClipEnable, BOOL multisampleEnable, BOOL antialiasedLineEnable, UINT forcedSampleCount, D3D12\_CONSERVATIVE\_RASTERIZATION\_MODE conservativeRaster)**</span></span>
</dt> <dd>

<span data-ttu-id="7c4c8-115">建立 CD3DX12 轉譯器 DESC 的新 \_ 實例 \_ ，並初始化下列參數：</span><span class="sxs-lookup"><span data-stu-id="7c4c8-115">Creates a new instance of a CD3DX12\_RASTERIZER\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="7c4c8-116">[**D3D12 \_填滿 \_ 模式**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_fill_mode) fillMode</span><span class="sxs-lookup"><span data-stu-id="7c4c8-116">[**D3D12\_FILL\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_fill_mode) fillMode</span></span>

<span data-ttu-id="7c4c8-117">[**D3D12 \_挑選 \_ 模式**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cull_mode) cullMode</span><span class="sxs-lookup"><span data-stu-id="7c4c8-117">[**D3D12\_CULL\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cull_mode) cullMode</span></span>

<span data-ttu-id="7c4c8-118">BOOL frontCounterClockwise</span><span class="sxs-lookup"><span data-stu-id="7c4c8-118">BOOL frontCounterClockwise</span></span>

<span data-ttu-id="7c4c8-119">INT depthBias</span><span class="sxs-lookup"><span data-stu-id="7c4c8-119">INT depthBias</span></span>

<span data-ttu-id="7c4c8-120">FLOAT depthBiasClamp</span><span class="sxs-lookup"><span data-stu-id="7c4c8-120">FLOAT depthBiasClamp</span></span>

<span data-ttu-id="7c4c8-121">FLOAT slopeScaledDepthBias</span><span class="sxs-lookup"><span data-stu-id="7c4c8-121">FLOAT slopeScaledDepthBias</span></span>

<span data-ttu-id="7c4c8-122">BOOL depthClipEnable</span><span class="sxs-lookup"><span data-stu-id="7c4c8-122">BOOL depthClipEnable</span></span>

<span data-ttu-id="7c4c8-123">BOOL multisampleEnable</span><span class="sxs-lookup"><span data-stu-id="7c4c8-123">BOOL multisampleEnable</span></span>

<span data-ttu-id="7c4c8-124">BOOL antialiasedLineEnable</span><span class="sxs-lookup"><span data-stu-id="7c4c8-124">BOOL antialiasedLineEnable</span></span>

<span data-ttu-id="7c4c8-125">UINT forcedSampleCount</span><span class="sxs-lookup"><span data-stu-id="7c4c8-125">UINT forcedSampleCount</span></span>

<span data-ttu-id="7c4c8-126">[**D3D12 \_保守的 \_ 點陣化 \_ 模式**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_conservative_rasterization_mode) conservativeRaster</span><span class="sxs-lookup"><span data-stu-id="7c4c8-126">[**D3D12\_CONSERVATIVE\_RASTERIZATION\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_conservative_rasterization_mode) conservativeRaster</span></span>

</dd> <dt>

<span data-ttu-id="7c4c8-127">**~ CD3DX12 轉譯器 \_ \_ DESC ()**</span><span class="sxs-lookup"><span data-stu-id="7c4c8-127">**~CD3DX12\_RASTERIZER\_DESC()**</span></span>
</dt> <dd>

<span data-ttu-id="7c4c8-128">終結 CD3DX12 轉譯器 DESC 的 \_ 實例 \_ 。</span><span class="sxs-lookup"><span data-stu-id="7c4c8-128">Destroys an instance of a CD3DX12\_RASTERIZER\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="7c4c8-129">**運算子 const D3D12 轉譯器 \_ \_ DESC& () const**</span><span class="sxs-lookup"><span data-stu-id="7c4c8-129">**operator const D3D12\_RASTERIZER\_DESC&() const**</span></span>
</dt> <dd>

<span data-ttu-id="7c4c8-130">針對父結構類型定義 & 的傳址運算子。</span><span class="sxs-lookup"><span data-stu-id="7c4c8-130">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7c4c8-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="7c4c8-131">Requirements</span></span>



| <span data-ttu-id="7c4c8-132">需求</span><span class="sxs-lookup"><span data-stu-id="7c4c8-132">Requirement</span></span> | <span data-ttu-id="7c4c8-133">值</span><span class="sxs-lookup"><span data-stu-id="7c4c8-133">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="7c4c8-134">標頭</span><span class="sxs-lookup"><span data-stu-id="7c4c8-134">Header</span></span><br/> | <dl> <span data-ttu-id="7c4c8-135"><dt>D3dx12。h</dt></span><span class="sxs-lookup"><span data-stu-id="7c4c8-135"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c4c8-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7c4c8-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c4c8-137">**D3D12 轉譯器 \_ \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="7c4c8-137">**D3D12\_RASTERIZER\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc)
</dt> <dt>

[<span data-ttu-id="7c4c8-138">D3D12 的 Helper 結構</span><span class="sxs-lookup"><span data-stu-id="7c4c8-138">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 






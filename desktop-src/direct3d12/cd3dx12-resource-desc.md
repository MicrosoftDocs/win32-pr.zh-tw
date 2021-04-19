---
title: 'CD3DX12_RESOURCE_DESC 結構 (D3dx12 .h) '
description: 協助程式結構，可讓您輕鬆地初始化 D3D12 \_ 資源 \_ DESC 結構。
ms.assetid: F18D41BE-8AEF-444E-AC8B-EC57C63BF083
keywords:
- CD3DX12_RESOURCE_DESC 結構
topic_type:
- apiref
api_name:
- CD3DX12_RESOURCE_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b341646b2dee7f469235c0b0bc9bb4550e56ff5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106991497"
---
# <a name="cd3dx12_resource_desc-structure"></a><span data-ttu-id="19574-104">CD3DX12 \_ 資源 \_ DESC 結構</span><span class="sxs-lookup"><span data-stu-id="19574-104">CD3DX12\_RESOURCE\_DESC structure</span></span>

<span data-ttu-id="19574-105">協助程式結構，可讓您輕鬆地初始化 [**D3D12 \_ 資源 \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc) 結構。</span><span class="sxs-lookup"><span data-stu-id="19574-105">A helper structure to enable easy initialization of a [**D3D12\_RESOURCE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="19574-106">語法</span><span class="sxs-lookup"><span data-stu-id="19574-106">Syntax</span></span>


```C++
struct CD3DX12_RESOURCE_DESC  : public D3D12_RESOURCE_DESC{
                        CD3DX12_RESOURCE_DESC();
                        explicit CD3DX12_RESOURCE_DESC(const D3D12_RESOURCE_DESC& o);
                        CD3DX12_RESOURCE_DESC(D3D12_RESOURCE_DIMENSION dimension, UINT64 alignment, UINT64 width, UINT height, UINT16 depthOrArraySize, UINT16 mipLevels, DXGI_FORMAT format, UINT sampleCount, UINT sampleQuality, D3D12_TEXTURE_LAYOUT layout, D3D12_RESOURCE_FLAGS flags);
  CD3DX12_RESOURCE_DESC static inline Buffer(const D3D12_RESOURCE_ALLOCATION_INFO& resAllocInfo, D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE);
  CD3DX12_RESOURCE_DESC static inline Buffer(UINT64 width, D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE, UINT64 alignment = 0);
  CD3DX12_RESOURCE_DESC static inline Tex1D(DXGI_FORMAT format, UINT64 width, UINT16 arraySize = 1, UINT16 mipLevels = 0, D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE, D3D12_TEXTURE_LAYOUT layout = D3D12_TEXTURE_LAYOUT_UNKNOWN, UINT64 alignment = 0);
  CD3DX12_RESOURCE_DESC static inline Tex2D(DXGI_FORMAT format, UINT64 width, UINT height, UINT16 arraySize = 1, UINT16 mipLevels = 0, UINT sampleCount = 1, UINT sampleQuality = 0, D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE, D3D12_TEXTURE_LAYOUT layout = D3D12_TEXTURE_LAYOUT_UNKNOWN, UINT64 alignment = 0);
  CD3DX12_RESOURCE_DESC static inline Tex3D(DXGI_FORMAT format, UINT64 width, UINT height, UINT16 depth, UINT16 mipLevels = 0, D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE, D3D12_TEXTURE_LAYOUT layout = D3D12_TEXTURE_LAYOUT_UNKNOWN, UINT64 alignment = 0);
  UINT16                inline Depth() const;
  UINT16                inline ArraySize() const;
  UINT8                 inline PlaneCount(ID3D12Device* pDevice) const;
  UINT                  inline Subresources(ID3D12Device* pDevice) const;
  UINT                  inline CalcSubresource(UINT MipSlice, UINT ArraySlice, UINT PlaneSlice);
                        operator const D3D12_RESOURCE_DESC&() const;
                        operator == (const D3D12_RESOURCE_DESC& l, const D3D12_RESOURCE_DESC& r);
                        operator !=  (const D3D12_RESOURCE_DESC& l, const D3D12_RESOURCE_DESC& r);
};
```



## <a name="members"></a><span data-ttu-id="19574-107">成員</span><span class="sxs-lookup"><span data-stu-id="19574-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="19574-108">**CD3DX12 \_ 資源 \_ DESC ()**</span><span class="sxs-lookup"><span data-stu-id="19574-108">**CD3DX12\_RESOURCE\_DESC()**</span></span>
</dt> <dd>

<span data-ttu-id="19574-109">建立 CD3DX12 資源 DESC 的新、未初始化的 \_ 實例 \_ 。</span><span class="sxs-lookup"><span data-stu-id="19574-109">Creates a new, uninitialized, instance of a CD3DX12\_RESOURCE\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="19574-110">**明確的 CD3DX12 \_ 資源 \_ desc (const D3D12 \_ 資源 \_ desc& o)**</span><span class="sxs-lookup"><span data-stu-id="19574-110">**explicit CD3DX12\_RESOURCE\_DESC(const D3D12\_RESOURCE\_DESC& o)**</span></span>
</dt> <dd>

<span data-ttu-id="19574-111">建立 CD3DX12 資源 desc 的新實例 \_ \_ ，並使用另一個 [**D3D12 \_ 資源 \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc) 結構的內容進行初始化。</span><span class="sxs-lookup"><span data-stu-id="19574-111">Creates a new instance of a CD3DX12\_RESOURCE\_DESC, initialized with the contents of another [**D3D12\_RESOURCE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc) structure.</span></span>

</dd> <dt>

<span data-ttu-id="19574-112">**CD3DX12 \_ 資源 \_ DESC (D3D12 \_ 資源 \_ 的維度維度、uint64 對齊、uint64 寬度、UINT 高度、Uint16 depthOrArraySize、uint16 mipLevels、DXGI \_ 格式格式、UINT SAMPLECOUNT、uint sampleQuality、D3D12 \_ 材質配置版面配置 \_ 、D3D12 \_ 資源旗標 \_ 旗標)**</span><span class="sxs-lookup"><span data-stu-id="19574-112">**CD3DX12\_RESOURCE\_DESC(D3D12\_RESOURCE\_DIMENSION dimension, UINT64 alignment, UINT64 width, UINT height, UINT16 depthOrArraySize, UINT16 mipLevels, DXGI\_FORMAT format, UINT sampleCount, UINT sampleQuality, D3D12\_TEXTURE\_LAYOUT layout, D3D12\_RESOURCE\_FLAGS flags)**</span></span>
</dt> <dd>

<span data-ttu-id="19574-113">建立 CD3DX12 資源 DESC 的新實例 \_ \_ ，並初始化下列參數：</span><span class="sxs-lookup"><span data-stu-id="19574-113">Creates a new instance of a CD3DX12\_RESOURCE\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="19574-114">[**D3D12 \_資源 \_ 維度**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension) 維度</span><span class="sxs-lookup"><span data-stu-id="19574-114">[**D3D12\_RESOURCE\_DIMENSION**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension) dimension</span></span>

<span data-ttu-id="19574-115">UINT64 對齊</span><span class="sxs-lookup"><span data-stu-id="19574-115">UINT64 alignment</span></span>

<span data-ttu-id="19574-116">UINT64 寬度</span><span class="sxs-lookup"><span data-stu-id="19574-116">UINT64 width</span></span>

<span data-ttu-id="19574-117">UINT 高度</span><span class="sxs-lookup"><span data-stu-id="19574-117">UINT height</span></span>

<span data-ttu-id="19574-118">UINT16 depthOrArraySize</span><span class="sxs-lookup"><span data-stu-id="19574-118">UINT16 depthOrArraySize</span></span>

<span data-ttu-id="19574-119">UINT16 mipLevels</span><span class="sxs-lookup"><span data-stu-id="19574-119">UINT16 mipLevels</span></span>

<span data-ttu-id="19574-120">[**DXGI \_格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) 格式</span><span class="sxs-lookup"><span data-stu-id="19574-120">[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) format</span></span>

<span data-ttu-id="19574-121">UINT sampleCount</span><span class="sxs-lookup"><span data-stu-id="19574-121">UINT sampleCount</span></span>

<span data-ttu-id="19574-122">UINT sampleQuality</span><span class="sxs-lookup"><span data-stu-id="19574-122">UINT sampleQuality</span></span>

<span data-ttu-id="19574-123">[**D3D12 \_材質 \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) 配置版面配置</span><span class="sxs-lookup"><span data-stu-id="19574-123">[**D3D12\_TEXTURE\_LAYOUT**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) layout</span></span>

<span data-ttu-id="19574-124">[**D3D12 \_資源 \_ 旗**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) 標旗標</span><span class="sxs-lookup"><span data-stu-id="19574-124">[**D3D12\_RESOURCE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) flags</span></span>

</dd> <dt>

<span data-ttu-id="19574-125">**靜態內嵌緩衝區 (const D3D12 \_ 資源 \_ 分配 \_ 資訊& resAllocInfo、D3D12 \_ 資源 \_ 旗標旗標 = D3D12 \_ 資源 \_ 旗標 \_ 無)**</span><span class="sxs-lookup"><span data-stu-id="19574-125">**static inline Buffer(const D3D12\_RESOURCE\_ALLOCATION\_INFO& resAllocInfo, D3D12\_RESOURCE\_FLAGS flags = D3D12\_RESOURCE\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="19574-126">指定初始化下列參數的函式：</span><span class="sxs-lookup"><span data-stu-id="19574-126">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="19574-127">[**D3D12 \_資源 \_ 分配 \_ 資訊**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& resAllocInfo</span><span class="sxs-lookup"><span data-stu-id="19574-127">[**D3D12\_RESOURCE\_ALLOCATION\_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& resAllocInfo</span></span>

<span data-ttu-id="19574-128"> (opt) [**D3D12 \_ 資源 \_ 旗**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) 標旗標 = D3D12 \_ 資源 \_ 旗標 \_ 無</span><span class="sxs-lookup"><span data-stu-id="19574-128">(opt) [**D3D12\_RESOURCE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) flags = D3D12\_RESOURCE\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="19574-129">**靜態內嵌緩衝區 (UINT64 寬度，D3D12 \_ 資源 \_ 旗標旗標 = D3D12 \_ 資源 \_ 旗標 \_ 無，UINT64 對齊 = 0)**</span><span class="sxs-lookup"><span data-stu-id="19574-129">**static inline Buffer(UINT64 width, D3D12\_RESOURCE\_FLAGS flags = D3D12\_RESOURCE\_FLAG\_NONE, UINT64 alignment = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="19574-130">指定初始化下列參數的函式：</span><span class="sxs-lookup"><span data-stu-id="19574-130">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="19574-131">UINT64 寬度</span><span class="sxs-lookup"><span data-stu-id="19574-131">UINT64 width</span></span>

<span data-ttu-id="19574-132"> (opt) [**D3D12 \_ 資源 \_ 旗**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) 標旗標 = D3D12 \_ 資源 \_ 旗標 \_ 無</span><span class="sxs-lookup"><span data-stu-id="19574-132">(opt) [**D3D12\_RESOURCE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) flags = D3D12\_RESOURCE\_FLAG\_NONE</span></span>

<span data-ttu-id="19574-133"> (opt) UINT64 對齊 = 0</span><span class="sxs-lookup"><span data-stu-id="19574-133">(opt) UINT64 alignment = 0</span></span>

</dd> <dt>

<span data-ttu-id="19574-134">**靜態內嵌 Tex1D (DXGI \_ 格式格式、UINT64 寬度、UINT16 arraySize = 1、UINT16 mipLevels = 0、D3D12 \_ 資源 \_ 旗標旗標 = D3D12 \_ 資源 \_ 旗標 \_ 無、D3D12 \_ 紋理配置版面配置 \_ = D3D12 \_ 紋理配置未知、 \_ \_ UINT64 對齊 = 0)**</span><span class="sxs-lookup"><span data-stu-id="19574-134">**static inline Tex1D(DXGI\_FORMAT format, UINT64 width, UINT16 arraySize = 1, UINT16 mipLevels = 0, D3D12\_RESOURCE\_FLAGS flags = D3D12\_RESOURCE\_FLAG\_NONE, D3D12\_TEXTURE\_LAYOUT layout = D3D12\_TEXTURE\_LAYOUT\_UNKNOWN, UINT64 alignment = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="19574-135">指定初始化下列參數的函式：</span><span class="sxs-lookup"><span data-stu-id="19574-135">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="19574-136">[**DXGI \_格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) 格式</span><span class="sxs-lookup"><span data-stu-id="19574-136">[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) format</span></span>

<span data-ttu-id="19574-137">UINT64 寬度</span><span class="sxs-lookup"><span data-stu-id="19574-137">UINT64 width</span></span>

<span data-ttu-id="19574-138"> (opt) UINT16 arraySize = 1</span><span class="sxs-lookup"><span data-stu-id="19574-138">(opt) UINT16 arraySize = 1</span></span>

<span data-ttu-id="19574-139"> (opt) UINT16 mipLevels = 0</span><span class="sxs-lookup"><span data-stu-id="19574-139">(opt) UINT16 mipLevels = 0</span></span>

<span data-ttu-id="19574-140"> (opt) [**D3D12 \_ 資源 \_ 旗**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) 標旗標 = D3D12 \_ 資源 \_ 旗標 \_ 無</span><span class="sxs-lookup"><span data-stu-id="19574-140">(opt) [**D3D12\_RESOURCE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) flags = D3D12\_RESOURCE\_FLAG\_NONE</span></span>

<span data-ttu-id="19574-141"> (opt) [**D3D12 \_ 材質 \_ 版面**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) 配置版面配置 = D3D12 \_ 材質配置 \_ \_ 不明</span><span class="sxs-lookup"><span data-stu-id="19574-141">(opt) [**D3D12\_TEXTURE\_LAYOUT**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) layout = D3D12\_TEXTURE\_LAYOUT\_UNKNOWN</span></span>

<span data-ttu-id="19574-142"> (opt) UINT64 對齊 = 0</span><span class="sxs-lookup"><span data-stu-id="19574-142">(opt) UINT64 alignment = 0</span></span>

</dd> <dt>

<span data-ttu-id="19574-143">**靜態內嵌 Tex2D (DXGI \_ 格式格式、UINT64 寬度、UINT 高度、UINT16 arraySize = 1、UINT16 mipLevels = 0、UINT sampleCount = 1、UINT sampleQuality = 0、D3D12 \_ 資源 \_ 旗標旗標 = D3D12 \_ 資源 \_ 旗標 \_ 無、D3D12 的 \_ 材質配置版面配置 = D3D12 紋理配置未知、 \_ \_ \_ \_ UINT64 對齊 = 0)**</span><span class="sxs-lookup"><span data-stu-id="19574-143">**static inline Tex2D(DXGI\_FORMAT format, UINT64 width, UINT height, UINT16 arraySize = 1, UINT16 mipLevels = 0, UINT sampleCount = 1, UINT sampleQuality = 0, D3D12\_RESOURCE\_FLAGS flags = D3D12\_RESOURCE\_FLAG\_NONE, D3D12\_TEXTURE\_LAYOUT layout = D3D12\_TEXTURE\_LAYOUT\_UNKNOWN, UINT64 alignment = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="19574-144">指定初始化下列參數的函式：</span><span class="sxs-lookup"><span data-stu-id="19574-144">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="19574-145">[**DXGI \_格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) 格式</span><span class="sxs-lookup"><span data-stu-id="19574-145">[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) format</span></span>

<span data-ttu-id="19574-146">UINT64 寬度</span><span class="sxs-lookup"><span data-stu-id="19574-146">UINT64 width</span></span>

<span data-ttu-id="19574-147">UINT 高度</span><span class="sxs-lookup"><span data-stu-id="19574-147">UINT height</span></span>

<span data-ttu-id="19574-148"> (opt) UINT16 arraySize = 1</span><span class="sxs-lookup"><span data-stu-id="19574-148">(opt) UINT16 arraySize = 1</span></span>

<span data-ttu-id="19574-149"> (opt) UINT16 mipLevels = 0</span><span class="sxs-lookup"><span data-stu-id="19574-149">(opt) UINT16 mipLevels = 0</span></span>

<span data-ttu-id="19574-150"> (opt) UINT sampleCount = 1</span><span class="sxs-lookup"><span data-stu-id="19574-150">(opt) UINT sampleCount = 1</span></span>

<span data-ttu-id="19574-151"> (opt) UINT sampleQuality = 0</span><span class="sxs-lookup"><span data-stu-id="19574-151">(opt) UINT sampleQuality = 0</span></span>

<span data-ttu-id="19574-152"> (opt) [**D3D12 \_ 資源 \_ 旗**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) 標旗標 = D3D12 \_ 資源 \_ 旗標 \_ 無</span><span class="sxs-lookup"><span data-stu-id="19574-152">(opt) [**D3D12\_RESOURCE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) flags = D3D12\_RESOURCE\_FLAG\_NONE</span></span>

<span data-ttu-id="19574-153"> (opt) [**D3D12 \_ 材質 \_ 版面**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) 配置版面配置 = D3D12 \_ 材質配置 \_ \_ 不明</span><span class="sxs-lookup"><span data-stu-id="19574-153">(opt) [**D3D12\_TEXTURE\_LAYOUT**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) layout = D3D12\_TEXTURE\_LAYOUT\_UNKNOWN</span></span>

<span data-ttu-id="19574-154"> (opt) UINT64 對齊 = 0</span><span class="sxs-lookup"><span data-stu-id="19574-154">(opt) UINT64 alignment = 0</span></span>

</dd> <dt>

<span data-ttu-id="19574-155">**靜態內嵌 Tex3D (DXGI \_ 格式格式、UINT64 寬度、UINT 高度、uint16 深度、Uint16 mipLevels = 0、D3D12 \_ 資源 \_ 旗標旗標 = D3D12 \_ 資源 \_ 旗標 \_ 無、D3D12 \_ 紋理配置版面配置 \_ = D3D12 \_ 紋理配置未知、 \_ \_ UINT64 對齊 = 0)**</span><span class="sxs-lookup"><span data-stu-id="19574-155">**static inline Tex3D(DXGI\_FORMAT format, UINT64 width, UINT height, UINT16 depth, UINT16 mipLevels = 0, D3D12\_RESOURCE\_FLAGS flags = D3D12\_RESOURCE\_FLAG\_NONE, D3D12\_TEXTURE\_LAYOUT layout = D3D12\_TEXTURE\_LAYOUT\_UNKNOWN, UINT64 alignment = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="19574-156">指定初始化下列參數的函式：</span><span class="sxs-lookup"><span data-stu-id="19574-156">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="19574-157">[**DXGI \_格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) 格式</span><span class="sxs-lookup"><span data-stu-id="19574-157">[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) format</span></span>

<span data-ttu-id="19574-158">UINT64 寬度</span><span class="sxs-lookup"><span data-stu-id="19574-158">UINT64 width</span></span>

<span data-ttu-id="19574-159">UINT 高度</span><span class="sxs-lookup"><span data-stu-id="19574-159">UINT height</span></span>

<span data-ttu-id="19574-160">UINT16 深度</span><span class="sxs-lookup"><span data-stu-id="19574-160">UINT16 depth</span></span>

<span data-ttu-id="19574-161"> (opt) UINT16 mipLevels = 0</span><span class="sxs-lookup"><span data-stu-id="19574-161">(opt) UINT16 mipLevels = 0</span></span>

<span data-ttu-id="19574-162"> (opt) [**D3D12 \_ 資源 \_ 旗**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) 標旗標 = D3D12 \_ 資源 \_ 旗標 \_ 無</span><span class="sxs-lookup"><span data-stu-id="19574-162">(opt) [**D3D12\_RESOURCE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) flags = D3D12\_RESOURCE\_FLAG\_NONE</span></span>

<span data-ttu-id="19574-163"> (opt) [**D3D12 \_ 材質 \_ 版面**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) 配置版面配置 = D3D12 \_ 材質配置 \_ \_ 不明</span><span class="sxs-lookup"><span data-stu-id="19574-163">(opt) [**D3D12\_TEXTURE\_LAYOUT**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) layout = D3D12\_TEXTURE\_LAYOUT\_UNKNOWN</span></span>

<span data-ttu-id="19574-164"> (opt) UINT64 對齊 = 0</span><span class="sxs-lookup"><span data-stu-id="19574-164">(opt) UINT64 alignment = 0</span></span>

</dd> <dt>

<span data-ttu-id="19574-165">**內嵌深度 () 常數**</span><span class="sxs-lookup"><span data-stu-id="19574-165">**inline Depth() const**</span></span>
</dt> <dd>

<span data-ttu-id="19574-166">如果 Dimension = = [**D3D12 \_ 資源 \_ 維度**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension)TEXTURE3D，則會傳回 \_ DepthOrArraySize。</span><span class="sxs-lookup"><span data-stu-id="19574-166">If Dimension == [**D3D12\_RESOURCE\_DIMENSION**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension)\_TEXTURE3D, returns DepthOrArraySize.</span></span> <span data-ttu-id="19574-167">如果 Dimension！ = D3D12 \_ 資源 \_ 維度 \_ TEXTURE3D，則傳回1。</span><span class="sxs-lookup"><span data-stu-id="19574-167">If Dimension != D3D12\_RESOURCE\_DIMENSION\_TEXTURE3D, returns 1.</span></span>

</dd> <dt>

<span data-ttu-id="19574-168">**內嵌 ArraySize () 常數**</span><span class="sxs-lookup"><span data-stu-id="19574-168">**inline ArraySize() const**</span></span>
</dt> <dd>

<span data-ttu-id="19574-169">如果 Dimension！ = D3D12 \_ 資源 \_ 維度 \_ TEXTURE3D，則傳回 DepthOrArraySize。</span><span class="sxs-lookup"><span data-stu-id="19574-169">If Dimension != D3D12\_RESOURCE\_DIMENSION\_TEXTURE3D, returns DepthOrArraySize.</span></span> <span data-ttu-id="19574-170">如果 Dimension = = D3D12 \_ 資源 \_ 維度 \_ TEXTURE3D，則傳回1。</span><span class="sxs-lookup"><span data-stu-id="19574-170">If Dimension == D3D12\_RESOURCE\_DIMENSION\_TEXTURE3D, returns 1.</span></span> <span data-ttu-id="19574-171">請參閱 [**D3D12 \_ 資源 \_ 維度**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension) \_ TEXTURE3D。</span><span class="sxs-lookup"><span data-stu-id="19574-171">See [**D3D12\_RESOURCE\_DIMENSION**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension)\_TEXTURE3D.</span></span>

</dd> <dt>

<span data-ttu-id="19574-172">**內嵌 PlaneCount (ID3D12Device \* pDevice) const**</span><span class="sxs-lookup"><span data-stu-id="19574-172">**inline PlaneCount(ID3D12Device\* pDevice) const**</span></span>
</dt> <dd>

<span data-ttu-id="19574-173">傳回 D3D12GetFormatPlaneCount (pDevice，格式) 。</span><span class="sxs-lookup"><span data-stu-id="19574-173">Returns D3D12GetFormatPlaneCount(pDevice, Format).</span></span> <span data-ttu-id="19574-174">請參閱 [**D3D12GetFormatPlaneCount**](d3d12getformatplanecount.md) 和 [**ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device)。</span><span class="sxs-lookup"><span data-stu-id="19574-174">See [**D3D12GetFormatPlaneCount**](d3d12getformatplanecount.md) and [**ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device).</span></span>

</dd> <dt>

<span data-ttu-id="19574-175">**內嵌子資源 (ID3D12Device \* pDevice) const**</span><span class="sxs-lookup"><span data-stu-id="19574-175">**inline Subresources(ID3D12Device\* pDevice) const**</span></span>
</dt> <dd>

<span data-ttu-id="19574-176">傳回計算為 MipLevels \* ArraySize () \* PlaneCount (pDevice) 的子資源數目。</span><span class="sxs-lookup"><span data-stu-id="19574-176">Returns the number of subresources, calculated as MipLevels \* ArraySize() \* PlaneCount(pDevice).</span></span>

</dd> <dt>

<span data-ttu-id="19574-177">**內嵌 CalcSubresource (UINT MipSlice、UINT ArraySlice、UINT PlaneSlice)**</span><span class="sxs-lookup"><span data-stu-id="19574-177">**inline CalcSubresource(UINT MipSlice, UINT ArraySlice, UINT PlaneSlice)**</span></span>
</dt> <dd>

<span data-ttu-id="19574-178">使用 [**D3D12CalcSubresource**](d3d12calcsubresource.md)計算 subresource 索引。</span><span class="sxs-lookup"><span data-stu-id="19574-178">Calculates a subresource index, by using [**D3D12CalcSubresource**](d3d12calcsubresource.md).</span></span>

</dd> <dt>

<span data-ttu-id="19574-179">**operator const D3D12 \_ 資源 \_ DESC& () const**</span><span class="sxs-lookup"><span data-stu-id="19574-179">**operator const D3D12\_RESOURCE\_DESC&() const**</span></span>
</dt> <dd>

<span data-ttu-id="19574-180">針對父結構類型定義 & 的傳址運算子。</span><span class="sxs-lookup"><span data-stu-id="19574-180">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> <dt>

<span data-ttu-id="19574-181">**operator = = (const D3D12 \_ 資源 \_ DESC& l，const D3D12 \_ resource \_ desc& r)**</span><span class="sxs-lookup"><span data-stu-id="19574-181">**operator == (const D3D12\_RESOURCE\_DESC& l, const D3D12\_RESOURCE\_DESC& r)**</span></span>
</dt> <dd>

<span data-ttu-id="19574-182">如果每個結構的所有成員都相同，則傳回 true。</span><span class="sxs-lookup"><span data-stu-id="19574-182">Returns true if all members of each structure are identical.</span></span>

</dd> <dt>

<span data-ttu-id="19574-183">**operator！ = (const D3D12 \_ 資源 \_ desc& l，const D3D12 \_ resource \_ desc& r)**</span><span class="sxs-lookup"><span data-stu-id="19574-183">**operator != (const D3D12\_RESOURCE\_DESC& l, const D3D12\_RESOURCE\_DESC& r)**</span></span>
</dt> <dd>

<span data-ttu-id="19574-184">如果每個結構的所有成員都相同，則傳回 false。</span><span class="sxs-lookup"><span data-stu-id="19574-184">Returns false if all members of each structure are identical.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="19574-185">規格需求</span><span class="sxs-lookup"><span data-stu-id="19574-185">Requirements</span></span>



| <span data-ttu-id="19574-186">需求</span><span class="sxs-lookup"><span data-stu-id="19574-186">Requirement</span></span> | <span data-ttu-id="19574-187">值</span><span class="sxs-lookup"><span data-stu-id="19574-187">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="19574-188">標頭</span><span class="sxs-lookup"><span data-stu-id="19574-188">Header</span></span><br/> | <dl> <span data-ttu-id="19574-189"><dt>D3dx12。h</dt></span><span class="sxs-lookup"><span data-stu-id="19574-189"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19574-190">另請參閱</span><span class="sxs-lookup"><span data-stu-id="19574-190">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19574-191">**D3D12 \_ 資源 \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="19574-191">**D3D12\_RESOURCE\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc)
</dt> <dt>

[<span data-ttu-id="19574-192">D3D12 的 Helper 結構</span><span class="sxs-lookup"><span data-stu-id="19574-192">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 


---
title: 'CD3DX12_SUBRESOURCE_FOOTPRINT 結構 (D3dx12 .h) '
description: 協助程式結構，可讓您輕鬆地初始化 D3D12 \_ SUBRESOURCE \_ 足跡結構。
ms.assetid: 17266FB0-41B5-4A70-A896-206B54F5E76F
keywords:
- CD3DX12_SUBRESOURCE_FOOTPRINT 結構
topic_type:
- apiref
api_name:
- CD3DX12_SUBRESOURCE_FOOTPRINT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab58e9a007d736222d9525d7a064456a1a9a7f14
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106976460"
---
# <a name="cd3dx12_subresource_footprint-structure"></a><span data-ttu-id="df268-104">CD3DX12 \_ SUBRESOURCE \_ 足跡結構</span><span class="sxs-lookup"><span data-stu-id="df268-104">CD3DX12\_SUBRESOURCE\_FOOTPRINT structure</span></span>

<span data-ttu-id="df268-105">協助程式結構，可讓您輕鬆地初始化 [**D3D12 \_ SUBRESOURCE \_ 足跡**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint) 結構。</span><span class="sxs-lookup"><span data-stu-id="df268-105">A helper structure to enable easy initialization of a [**D3D12\_SUBRESOURCE\_FOOTPRINT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="df268-106">語法</span><span class="sxs-lookup"><span data-stu-id="df268-106">Syntax</span></span>


```C++
struct CD3DX12_SUBRESOURCE_FOOTPRINT  : public D3D12_SUBRESOURCE_FOOTPRINT{
   CD3DX12_SUBRESOURCE_FOOTPRINT();
   explicit CD3DX12_SUBRESOURCE_FOOTPRINT(const D3D12_SUBRESOURCE_FOOTPRINT &o);
   CD3DX12_SUBRESOURCE_FOOTPRINT(DXGI_FORMAT format, UINT width, UINT height, UINT depth, UINT rowPitch);
   explicit CD3DX12_SUBRESOURCE_FOOTPRINT(const D3D12_RESOURCE_DESC& resDesc, UINT rowPitch);
   operator const D3D12_SUBRESOURCE_FOOTPRINT&() const;
};
```



## <a name="members"></a><span data-ttu-id="df268-107">成員</span><span class="sxs-lookup"><span data-stu-id="df268-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="df268-108">**CD3DX12 \_ SUBRESOURCE \_ 足跡 ()**</span><span class="sxs-lookup"><span data-stu-id="df268-108">**CD3DX12\_SUBRESOURCE\_FOOTPRINT()**</span></span>
</dt> <dd>

<span data-ttu-id="df268-109">建立新的、未初始化的 CD3DX12 \_ SUBRESOURCE 足跡實例 \_ 。</span><span class="sxs-lookup"><span data-stu-id="df268-109">Creates a new, uninitialized, instance of a CD3DX12\_SUBRESOURCE\_FOOTPRINT.</span></span>

</dd> <dt>

<span data-ttu-id="df268-110">**明確的 CD3DX12 \_ SUBRESOURCE \_ 足跡 (const D3D12 \_ SUBRESOURCE 使用量 \_ &o)**</span><span class="sxs-lookup"><span data-stu-id="df268-110">**explicit CD3DX12\_SUBRESOURCE\_FOOTPRINT(const D3D12\_SUBRESOURCE\_FOOTPRINT &o)**</span></span>
</dt> <dd>

<span data-ttu-id="df268-111">建立 CD3DX12 SUBRESOURCE 使用量的新實例 \_ \_ ，並以另一個 [**D3D12 \_ SUBRESOURCE \_ 足跡**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint) 結構的內容進行初始化。</span><span class="sxs-lookup"><span data-stu-id="df268-111">Creates a new instance of a CD3DX12\_SUBRESOURCE\_FOOTPRINT, initialized with the contents of another [**D3D12\_SUBRESOURCE\_FOOTPRINT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint) structure.</span></span>

</dd> <dt>

<span data-ttu-id="df268-112">**CD3DX12 \_ SUBRESOURCE \_ 足跡 (DXGI \_ 格式格式、UINT width、UINT height、UINT Depth、uint rowPitch)**</span><span class="sxs-lookup"><span data-stu-id="df268-112">**CD3DX12\_SUBRESOURCE\_FOOTPRINT(DXGI\_FORMAT format, UINT width, UINT height, UINT depth, UINT rowPitch)**</span></span>
</dt> <dd>

<span data-ttu-id="df268-113">建立 CD3DX12 SUBRESOURCE 足跡的新實例 \_ \_ ，並初始化下列參數：</span><span class="sxs-lookup"><span data-stu-id="df268-113">Creates a new instance of a CD3DX12\_SUBRESOURCE\_FOOTPRINT, initializing the following parameters:</span></span>

<span data-ttu-id="df268-114">[**DXGI \_格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) 格式</span><span class="sxs-lookup"><span data-stu-id="df268-114">[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) format</span></span>

<span data-ttu-id="df268-115">UINT 寬度</span><span class="sxs-lookup"><span data-stu-id="df268-115">UINT width</span></span>

<span data-ttu-id="df268-116">UINT 高度</span><span class="sxs-lookup"><span data-stu-id="df268-116">UINT height</span></span>

<span data-ttu-id="df268-117">UINT 深度</span><span class="sxs-lookup"><span data-stu-id="df268-117">UINT depth</span></span>

<span data-ttu-id="df268-118">UINT rowPitch</span><span class="sxs-lookup"><span data-stu-id="df268-118">UINT rowPitch</span></span>

</dd> <dt>

<span data-ttu-id="df268-119">**明確的 CD3DX12 \_ SUBRESOURCE \_ 足跡 (const D3D12 \_ 資源 \_ DESC& resDesc，UINT rowPitch)**</span><span class="sxs-lookup"><span data-stu-id="df268-119">**explicit CD3DX12\_SUBRESOURCE\_FOOTPRINT(const D3D12\_RESOURCE\_DESC& resDesc, UINT rowPitch)**</span></span>
</dt> <dd>

<span data-ttu-id="df268-120">建立 CD3DX12 SUBRESOURCE 足跡的新實例 \_ \_ ，並初始化下列參數：</span><span class="sxs-lookup"><span data-stu-id="df268-120">Creates a new instance of a CD3DX12\_SUBRESOURCE\_FOOTPRINT, initializing the following parameters:</span></span>

<span data-ttu-id="df268-121">[**D3D12 \_資源 \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc)& resDesc</span><span class="sxs-lookup"><span data-stu-id="df268-121">[**D3D12\_RESOURCE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc)& resDesc</span></span>

<span data-ttu-id="df268-122">UINT rowPitch</span><span class="sxs-lookup"><span data-stu-id="df268-122">UINT rowPitch</span></span>

</dd> <dt>

<span data-ttu-id="df268-123">**operator const D3D12 \_ SUBRESOURCE \_& () const**</span><span class="sxs-lookup"><span data-stu-id="df268-123">**operator const D3D12\_SUBRESOURCE\_FOOTPRINT&() const**</span></span>
</dt> <dd>

<span data-ttu-id="df268-124">針對父結構類型定義 & 的傳址運算子。</span><span class="sxs-lookup"><span data-stu-id="df268-124">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="df268-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="df268-125">Requirements</span></span>



| <span data-ttu-id="df268-126">需求</span><span class="sxs-lookup"><span data-stu-id="df268-126">Requirement</span></span> | <span data-ttu-id="df268-127">值</span><span class="sxs-lookup"><span data-stu-id="df268-127">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="df268-128">標頭</span><span class="sxs-lookup"><span data-stu-id="df268-128">Header</span></span><br/> | <dl> <span data-ttu-id="df268-129"><dt>D3dx12。h</dt></span><span class="sxs-lookup"><span data-stu-id="df268-129"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df268-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="df268-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df268-131">**D3D12 \_ SUBRESOURCE \_ 足跡**</span><span class="sxs-lookup"><span data-stu-id="df268-131">**D3D12\_SUBRESOURCE\_FOOTPRINT**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint)
</dt> <dt>

[<span data-ttu-id="df268-132">D3D12 的 Helper 結構</span><span class="sxs-lookup"><span data-stu-id="df268-132">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 


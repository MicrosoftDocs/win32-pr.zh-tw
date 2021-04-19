---
title: 'CD3DX12_TEXTURE_COPY_LOCATION 結構 (D3dx12 .h) '
description: 協助程式結構，可讓您輕鬆地初始化 D3D12 \_ 材質 \_ 複製 \_ 位置結構。
ms.assetid: 8BA93729-2FFB-4C09-88B0-779049BAF385
keywords:
- CD3DX12_TEXTURE_COPY_LOCATION 結構
topic_type:
- apiref
api_name:
- CD3DX12_TEXTURE_COPY_LOCATION
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5143137f92e38662660588dd89a527f59644126
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "107000222"
---
# <a name="cd3dx12_texture_copy_location-structure"></a><span data-ttu-id="17fe2-104">CD3DX12 \_ 材質 \_ 複製 \_ 位置結構</span><span class="sxs-lookup"><span data-stu-id="17fe2-104">CD3DX12\_TEXTURE\_COPY\_LOCATION structure</span></span>

<span data-ttu-id="17fe2-105">協助程式結構，可讓您輕鬆地初始化 [**D3D12 \_ 材質 \_ 複製 \_ 位置**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location) 結構。</span><span class="sxs-lookup"><span data-stu-id="17fe2-105">A helper structure to enable easy initialization of a [**D3D12\_TEXTURE\_COPY\_LOCATION**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="17fe2-106">語法</span><span class="sxs-lookup"><span data-stu-id="17fe2-106">Syntax</span></span>


```C++
struct CD3DX12_TEXTURE_COPY_LOCATION  : public D3D12_TEXTURE_COPY_LOCATION{
   CD3DX12_TEXTURE_COPY_LOCATION();
   explicit CD3DX12_TEXTURE_COPY_LOCATION(const D3D12_TEXTURE_COPY_LOCATION &o);
   CD3DX12_TEXTURE_COPY_LOCATION(ID3D12Resource* pRes);
   CD3DX12_TEXTURE_COPY_LOCATION(ID3D12Resource* pRes, D3D12_PLACED_SUBRESOURCE_FOOTPRINT const& Footprint);
   CD3DX12_TEXTURE_COPY_LOCATION(ID3D12Resource* pRes, UINT Sub);
};
```



## <a name="members"></a><span data-ttu-id="17fe2-107">成員</span><span class="sxs-lookup"><span data-stu-id="17fe2-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="17fe2-108">**CD3DX12 \_ 材質 \_ 複製 \_ 位置 ()**</span><span class="sxs-lookup"><span data-stu-id="17fe2-108">**CD3DX12\_TEXTURE\_COPY\_LOCATION()**</span></span>
</dt> <dd>

<span data-ttu-id="17fe2-109">建立 CD3DX12 \_ 材質複製位置的新、未初始化的 \_ 實例 \_ 。</span><span class="sxs-lookup"><span data-stu-id="17fe2-109">Creates a new, uninitialized, instance of a CD3DX12\_TEXTURE\_COPY\_LOCATION.</span></span>

</dd> <dt>

<span data-ttu-id="17fe2-110">**明確 CD3DX12 \_ 材質 \_ 複製 \_ 位置 (const D3D12 \_ 材質 \_ 複製 \_ 位置 &o)**</span><span class="sxs-lookup"><span data-stu-id="17fe2-110">**explicit CD3DX12\_TEXTURE\_COPY\_LOCATION(const D3D12\_TEXTURE\_COPY\_LOCATION &o)**</span></span>
</dt> <dd>

<span data-ttu-id="17fe2-111">建立 CD3DX12 \_ 材質複製位置的新實例 \_ \_ ，並使用另一個 [**D3D12 \_ 材質 \_ 複製 \_ 位置**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location) 結構的內容進行初始化。</span><span class="sxs-lookup"><span data-stu-id="17fe2-111">Creates a new instance of a CD3DX12\_TEXTURE\_COPY\_LOCATION, initialized with the contents of another [**D3D12\_TEXTURE\_COPY\_LOCATION**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location) structure.</span></span>

</dd> <dt>

<span data-ttu-id="17fe2-112">**CD3DX12 \_ 材質 \_ 複製 \_ 位置 (ID3D12Resource \* 按)**</span><span class="sxs-lookup"><span data-stu-id="17fe2-112">**CD3DX12\_TEXTURE\_COPY\_LOCATION(ID3D12Resource\* pRes)**</span></span>
</dt> <dd>

<span data-ttu-id="17fe2-113">建立 CD3DX12 \_ 材質複製位置的新實例 \_ ，並 \_ 初始化下列參數：</span><span class="sxs-lookup"><span data-stu-id="17fe2-113">Creates a new instance of a CD3DX12\_TEXTURE\_COPY\_LOCATION, initializing the following parameters:</span></span>

<span data-ttu-id="17fe2-114">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \*壓力</span><span class="sxs-lookup"><span data-stu-id="17fe2-114">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\* pRes</span></span>

</dd> <dt>

<span data-ttu-id="17fe2-115">**CD3DX12 \_ 材質 \_ 複製 \_ 位置 (ID3D12RESOURCE \* 按，D3D12 將 SUBRESOURCE 耗用量 \_ \_ \_ 常數& 足跡)**</span><span class="sxs-lookup"><span data-stu-id="17fe2-115">**CD3DX12\_TEXTURE\_COPY\_LOCATION(ID3D12Resource\* pRes, D3D12\_PLACED\_SUBRESOURCE\_FOOTPRINT const& Footprint)**</span></span>
</dt> <dd>

<span data-ttu-id="17fe2-116">建立 CD3DX12 \_ 材質複製位置的新實例 \_ ，並 \_ 初始化下列參數：</span><span class="sxs-lookup"><span data-stu-id="17fe2-116">Creates a new instance of a CD3DX12\_TEXTURE\_COPY\_LOCATION, initializing the following parameters:</span></span>

<span data-ttu-id="17fe2-117">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \*壓力</span><span class="sxs-lookup"><span data-stu-id="17fe2-117">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\* pRes</span></span>

<span data-ttu-id="17fe2-118">[**D3D12 \_將 \_ SUBRESOURCE \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint) 的耗用量常數& 足跡</span><span class="sxs-lookup"><span data-stu-id="17fe2-118">[**D3D12\_PLACED\_SUBRESOURCE\_FOOTPRINT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint) const& Footprint</span></span>

</dd> <dt>

<span data-ttu-id="17fe2-119">**CD3DX12 \_ 材質 \_ 複製 \_ 位置 (ID3D12RESOURCE \* 按，UINT Sub)**</span><span class="sxs-lookup"><span data-stu-id="17fe2-119">**CD3DX12\_TEXTURE\_COPY\_LOCATION(ID3D12Resource\* pRes, UINT Sub)**</span></span>
</dt> <dd>

<span data-ttu-id="17fe2-120">建立 CD3DX12 \_ 材質複製位置的新實例 \_ ，並 \_ 初始化下列參數：</span><span class="sxs-lookup"><span data-stu-id="17fe2-120">Creates a new instance of a CD3DX12\_TEXTURE\_COPY\_LOCATION, initializing the following parameters:</span></span>

<span data-ttu-id="17fe2-121">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \*壓力</span><span class="sxs-lookup"><span data-stu-id="17fe2-121">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\* pRes</span></span>

<span data-ttu-id="17fe2-122">UINT Sub</span><span class="sxs-lookup"><span data-stu-id="17fe2-122">UINT Sub</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="17fe2-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="17fe2-123">Requirements</span></span>



| <span data-ttu-id="17fe2-124">需求</span><span class="sxs-lookup"><span data-stu-id="17fe2-124">Requirement</span></span> | <span data-ttu-id="17fe2-125">值</span><span class="sxs-lookup"><span data-stu-id="17fe2-125">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="17fe2-126">標頭</span><span class="sxs-lookup"><span data-stu-id="17fe2-126">Header</span></span><br/> | <dl> <span data-ttu-id="17fe2-127"><dt>D3dx12。h</dt></span><span class="sxs-lookup"><span data-stu-id="17fe2-127"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17fe2-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="17fe2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17fe2-129">**D3D12 \_ 材質 \_ 複製 \_ 位置**</span><span class="sxs-lookup"><span data-stu-id="17fe2-129">**D3D12\_TEXTURE\_COPY\_LOCATION**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location)
</dt> <dt>

[<span data-ttu-id="17fe2-130">D3D12 的 Helper 結構</span><span class="sxs-lookup"><span data-stu-id="17fe2-130">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 






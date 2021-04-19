---
title: 'CD3DX12_RESOURCE_ALLOCATION_INFO 結構 (D3dx12 .h) '
description: 協助程式結構，可讓您輕鬆地初始化 D3D12 \_ 資源 \_ 分配 \_ 資訊結構。
ms.assetid: 81FC8D0E-2C15-42D3-9E06-1FE193F707C6
keywords:
- CD3DX12_RESOURCE_ALLOCATION_INFO 結構
topic_type:
- apiref
api_name:
- CD3DX12_RESOURCE_ALLOCATION_INFO
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08542c7460b2fadf381f85dc271167258e31fb46
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106981245"
---
# <a name="cd3dx12_resource_allocation_info-structure"></a><span data-ttu-id="de054-104">CD3DX12 \_ 資源 \_ 分配 \_ 資訊結構</span><span class="sxs-lookup"><span data-stu-id="de054-104">CD3DX12\_RESOURCE\_ALLOCATION\_INFO structure</span></span>

<span data-ttu-id="de054-105">協助程式結構，可讓您輕鬆地初始化 [**D3D12 \_ 資源 \_ 分配 \_ 資訊**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info) 結構。</span><span class="sxs-lookup"><span data-stu-id="de054-105">A helper structure to enable easy initialization of a [**D3D12\_RESOURCE\_ALLOCATION\_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="de054-106">語法</span><span class="sxs-lookup"><span data-stu-id="de054-106">Syntax</span></span>


```C++
struct CD3DX12_RESOURCE_ALLOCATION_INFO  : public D3D12_RESOURCE_ALLOCATION_INFO{
   CD3DX12_RESOURCE_ALLOCATION_INFO();
   explicit CD3DX12_RESOURCE_ALLOCATION_INFO(const D3D12_RESOURCE_ALLOCATION_INFO& o);
   CD3DX12_RESOURCE_ALLOCATION_INFO(UINT64 size, UINT64 alignment);
   operator const D3D12_RESOURCE_ALLOCATION_INFO&() const;
};
```



## <a name="members"></a><span data-ttu-id="de054-107">成員</span><span class="sxs-lookup"><span data-stu-id="de054-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="de054-108">**CD3DX12 \_ 資源 \_ 分配 \_ 資訊 ()**</span><span class="sxs-lookup"><span data-stu-id="de054-108">**CD3DX12\_RESOURCE\_ALLOCATION\_INFO()**</span></span>
</dt> <dd>

<span data-ttu-id="de054-109">建立 CD3DX12 \_ 資源配置資訊的新、未初始化的 \_ 實例 \_ 。</span><span class="sxs-lookup"><span data-stu-id="de054-109">Creates a new, uninitialized, instance of a CD3DX12\_RESOURCE\_ALLOCATION\_INFO.</span></span>

</dd> <dt>

<span data-ttu-id="de054-110">**明確 CD3DX12 \_ 資源 \_ 分配 \_ 資訊 (const D3D12 \_ 資源 \_ 分配 \_ 資訊& o)**</span><span class="sxs-lookup"><span data-stu-id="de054-110">**explicit CD3DX12\_RESOURCE\_ALLOCATION\_INFO(const D3D12\_RESOURCE\_ALLOCATION\_INFO& o)**</span></span>
</dt> <dd>

<span data-ttu-id="de054-111">建立 CD3DX12 \_ 資源配置資訊的新實例 \_ \_ ，並使用另一個 [**D3D12 \_ 資源 \_ 分配 \_ 資訊**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info) 結構的內容進行初始化。</span><span class="sxs-lookup"><span data-stu-id="de054-111">Creates a new instance of a CD3DX12\_RESOURCE\_ALLOCATION\_INFO, initialized with the contents of another [**D3D12\_RESOURCE\_ALLOCATION\_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info) structure.</span></span>

</dd> <dt>

<span data-ttu-id="de054-112">**CD3DX12 \_ 資源 \_ 分配 \_ 資訊 (UINT64 大小，uint64 對齊)**</span><span class="sxs-lookup"><span data-stu-id="de054-112">**CD3DX12\_RESOURCE\_ALLOCATION\_INFO(UINT64 size, UINT64 alignment)**</span></span>
</dt> <dd>

<span data-ttu-id="de054-113">建立 CD3DX12 \_ 資源配置資訊的新實例 \_ ，並 \_ 初始化下列參數：</span><span class="sxs-lookup"><span data-stu-id="de054-113">Creates a new instance of a CD3DX12\_RESOURCE\_ALLOCATION\_INFO, initializing the following parameters:</span></span>

<span data-ttu-id="de054-114">UINT64 大小</span><span class="sxs-lookup"><span data-stu-id="de054-114">UINT64 size</span></span>

<span data-ttu-id="de054-115">UINT64 對齊</span><span class="sxs-lookup"><span data-stu-id="de054-115">UINT64 alignment</span></span>

</dd> <dt>

<span data-ttu-id="de054-116">**運算子 const D3D12 \_ 資源 \_ 分配 \_ 資訊& () const**</span><span class="sxs-lookup"><span data-stu-id="de054-116">**operator const D3D12\_RESOURCE\_ALLOCATION\_INFO&() const**</span></span>
</dt> <dd>

<span data-ttu-id="de054-117">針對父結構類型定義 & 的傳址運算子。</span><span class="sxs-lookup"><span data-stu-id="de054-117">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="de054-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="de054-118">Requirements</span></span>



| <span data-ttu-id="de054-119">需求</span><span class="sxs-lookup"><span data-stu-id="de054-119">Requirement</span></span> | <span data-ttu-id="de054-120">值</span><span class="sxs-lookup"><span data-stu-id="de054-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="de054-121">標頭</span><span class="sxs-lookup"><span data-stu-id="de054-121">Header</span></span><br/> | <dl> <span data-ttu-id="de054-122"><dt>D3dx12。h</dt></span><span class="sxs-lookup"><span data-stu-id="de054-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de054-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="de054-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de054-124">**D3D12 \_ 資源 \_ 分配 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="de054-124">**D3D12\_RESOURCE\_ALLOCATION\_INFO**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)
</dt> <dt>

[<span data-ttu-id="de054-125">D3D12 的 Helper 結構</span><span class="sxs-lookup"><span data-stu-id="de054-125">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 






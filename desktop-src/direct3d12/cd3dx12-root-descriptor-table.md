---
title: 'CD3DX12_ROOT_DESCRIPTOR_TABLE 結構 (D3dx12 .h) '
description: 協助程式結構，可讓您輕鬆地初始化 D3D12 \_ 根 \_ 描述元 \_ 資料表結構。
ms.assetid: 154B4C50-4E94-471C-A44E-F120A84F007C
keywords:
- CD3DX12_ROOT_DESCRIPTOR_TABLE 結構
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_DESCRIPTOR_TABLE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f675624526a959e6cf92172383b12590c36fc408
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106982860"
---
# <a name="cd3dx12_root_descriptor_table-structure"></a><span data-ttu-id="fab9f-104">CD3DX12 \_ 根 \_ 描述元 \_ 資料表結構</span><span class="sxs-lookup"><span data-stu-id="fab9f-104">CD3DX12\_ROOT\_DESCRIPTOR\_TABLE structure</span></span>

<span data-ttu-id="fab9f-105">協助程式結構，可讓您輕鬆地初始化 [**D3D12 \_ 根描述元 \_ \_ 資料表**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) 結構。</span><span class="sxs-lookup"><span data-stu-id="fab9f-105">A helper structure to enable easy initialization of a [**D3D12\_ROOT\_DESCRIPTOR\_TABLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="fab9f-106">語法</span><span class="sxs-lookup"><span data-stu-id="fab9f-106">Syntax</span></span>


```C++
struct CD3DX12_ROOT_DESCRIPTOR_TABLE  : public D3D12_ROOT_DESCRIPTOR_TABLE{
       CD3DX12_ROOT_DESCRIPTOR_TABLE();
       explicit CD3DX12_ROOT_DESCRIPTOR_TABLE(const D3D12_ROOT_DESCRIPTOR_TABLE &o);
       CD3DX12_ROOT_DESCRIPTOR_TABLE(UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE* _pDescriptorRanges);
  void inline Init(UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE* _pDescriptorRanges);
  void static inline Init(D3D12_ROOT_DESCRIPTOR_TABLE &rootDescriptorTable, UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE* _pDescriptorRanges);
};
```



## <a name="members"></a><span data-ttu-id="fab9f-107">成員</span><span class="sxs-lookup"><span data-stu-id="fab9f-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="fab9f-108">**CD3DX12 \_ 根 \_ 描述元 \_ 資料表 ()**</span><span class="sxs-lookup"><span data-stu-id="fab9f-108">**CD3DX12\_ROOT\_DESCRIPTOR\_TABLE()**</span></span>
</dt> <dd>

<span data-ttu-id="fab9f-109">建立 CD3DX12 根描述中繼資料表的新、未初始化的實例 \_ \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="fab9f-109">Creates a new, uninitialized, instance of a CD3DX12\_ROOT\_DESCRIPTOR\_TABLE.</span></span>

</dd> <dt>

<span data-ttu-id="fab9f-110">**明確 CD3DX12 的 \_ 根 \_ 描述元 \_ 資料表 (const D3D12 \_ 根描述元 \_ \_ 資料表 &o)**</span><span class="sxs-lookup"><span data-stu-id="fab9f-110">**explicit CD3DX12\_ROOT\_DESCRIPTOR\_TABLE(const D3D12\_ROOT\_DESCRIPTOR\_TABLE &o)**</span></span>
</dt> <dd>

<span data-ttu-id="fab9f-111">建立 CD3DX12 根描述中繼資料表的新實例 \_ \_ \_ ，並以另一個 [**D3D12 \_ 根 \_ 描述元 \_ 資料表**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) 結構的內容進行初始化。</span><span class="sxs-lookup"><span data-stu-id="fab9f-111">Creates a new instance of a CD3DX12\_ROOT\_DESCRIPTOR\_TABLE, initialized with the contents of another [**D3D12\_ROOT\_DESCRIPTOR\_TABLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) structure.</span></span>

</dd> <dt>

<span data-ttu-id="fab9f-112">**CD3DX12 \_ 根 \_ 描述元 \_ 資料表 (UINT NUMDESCRIPTORRANGES，const D3D12 \_ 描述項 \_ 範圍 \* \_ pDescriptorRanges)**</span><span class="sxs-lookup"><span data-stu-id="fab9f-112">**CD3DX12\_ROOT\_DESCRIPTOR\_TABLE(UINT numDescriptorRanges, const D3D12\_DESCRIPTOR\_RANGE\* \_pDescriptorRanges)**</span></span>
</dt> <dd>

<span data-ttu-id="fab9f-113">建立 CD3DX12 根描述中繼資料表的新實例 \_ \_ ，並 \_ 初始化下列參數：</span><span class="sxs-lookup"><span data-stu-id="fab9f-113">Creates a new instance of a CD3DX12\_ROOT\_DESCRIPTOR\_TABLE, initializing the following parameters:</span></span>

<span data-ttu-id="fab9f-114">UINT numDescriptorRanges</span><span class="sxs-lookup"><span data-stu-id="fab9f-114">UINT numDescriptorRanges</span></span>

<span data-ttu-id="fab9f-115">[**D3D12 \_描述項 \_ 範圍**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) \* \_ pDescriptorRanges</span><span class="sxs-lookup"><span data-stu-id="fab9f-115">[**D3D12\_DESCRIPTOR\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range)\* \_pDescriptorRanges</span></span>

</dd> <dt>

<span data-ttu-id="fab9f-116">**內嵌 Init (UINT numDescriptorRanges、const D3D12 \_ 描述項 \_ 範圍 \* \_ pDescriptorRanges)**</span><span class="sxs-lookup"><span data-stu-id="fab9f-116">**inline Init(UINT numDescriptorRanges, const D3D12\_DESCRIPTOR\_RANGE\* \_pDescriptorRanges)**</span></span>
</dt> <dd>

<span data-ttu-id="fab9f-117">指定初始化下列參數的函式：</span><span class="sxs-lookup"><span data-stu-id="fab9f-117">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="fab9f-118">UINT numDescriptorRanges</span><span class="sxs-lookup"><span data-stu-id="fab9f-118">UINT numDescriptorRanges</span></span>

<span data-ttu-id="fab9f-119">[**D3D12 \_描述項 \_ 範圍**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) \* \_ pDescriptorRanges</span><span class="sxs-lookup"><span data-stu-id="fab9f-119">[**D3D12\_DESCRIPTOR\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range)\* \_pDescriptorRanges</span></span>

</dd> <dt>

<span data-ttu-id="fab9f-120">**靜態內嵌 Init (D3D12 \_ 根 \_ 描述元 \_ 資料表 &RootDescriptorTable、UINT NUMDESCRIPTORRANGES、const D3D12 \_ 描述項 \_ 範圍 \* \_ pDescriptorRanges)**</span><span class="sxs-lookup"><span data-stu-id="fab9f-120">**static inline Init(D3D12\_ROOT\_DESCRIPTOR\_TABLE &rootDescriptorTable, UINT numDescriptorRanges, const D3D12\_DESCRIPTOR\_RANGE\* \_pDescriptorRanges)**</span></span>
</dt> <dd>

<span data-ttu-id="fab9f-121">指定初始化下列參數的函式：</span><span class="sxs-lookup"><span data-stu-id="fab9f-121">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="fab9f-122">[**D3D12 \_根 \_ 描述元 \_ 資料表**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) &rootDescriptorTable</span><span class="sxs-lookup"><span data-stu-id="fab9f-122">[**D3D12\_ROOT\_DESCRIPTOR\_TABLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) &rootDescriptorTable</span></span>

<span data-ttu-id="fab9f-123">UINT numDescriptorRanges</span><span class="sxs-lookup"><span data-stu-id="fab9f-123">UINT numDescriptorRanges</span></span>

<span data-ttu-id="fab9f-124">[**D3D12 \_描述項 \_ 範圍**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) \* \_ pDescriptorRanges</span><span class="sxs-lookup"><span data-stu-id="fab9f-124">[**D3D12\_DESCRIPTOR\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range)\* \_pDescriptorRanges</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fab9f-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="fab9f-125">Requirements</span></span>



| <span data-ttu-id="fab9f-126">需求</span><span class="sxs-lookup"><span data-stu-id="fab9f-126">Requirement</span></span> | <span data-ttu-id="fab9f-127">值</span><span class="sxs-lookup"><span data-stu-id="fab9f-127">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="fab9f-128">標頭</span><span class="sxs-lookup"><span data-stu-id="fab9f-128">Header</span></span><br/> | <dl> <span data-ttu-id="fab9f-129"><dt>D3dx12。h</dt></span><span class="sxs-lookup"><span data-stu-id="fab9f-129"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fab9f-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fab9f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fab9f-131">**D3D12 \_ 根 \_ 描述元 \_ 資料表**</span><span class="sxs-lookup"><span data-stu-id="fab9f-131">**D3D12\_ROOT\_DESCRIPTOR\_TABLE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table)
</dt> <dt>

[<span data-ttu-id="fab9f-132">D3D12 的 Helper 結構</span><span class="sxs-lookup"><span data-stu-id="fab9f-132">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 






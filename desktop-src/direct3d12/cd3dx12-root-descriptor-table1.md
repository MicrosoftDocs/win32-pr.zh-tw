---
title: 'CD3DX12_ROOT_DESCRIPTOR_TABLE1 結構 (D3dx12 .h) '
description: 協助程式結構，可讓您輕鬆地初始化 D3D12 \_ 根目錄 \_ 描述元 \_ TABLE1 結構。
ms.assetid: 82AC1948-92AA-4A4D-B443-717E9BF3046D
keywords:
- CD3DX12_ROOT_DESCRIPTOR_TABLE1 結構
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_DESCRIPTOR_TABLE1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e3538e5e1e199fdb6f8c7473af4996ccd7b7f1f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106982240"
---
# <a name="cd3dx12_root_descriptor_table1-structure"></a><span data-ttu-id="16982-104">CD3DX12 \_ 根目錄 \_ 描述元 \_ TABLE1 結構</span><span class="sxs-lookup"><span data-stu-id="16982-104">CD3DX12\_ROOT\_DESCRIPTOR\_TABLE1 structure</span></span>

<span data-ttu-id="16982-105">協助程式結構，可讓您輕鬆地初始化 [**D3D12 \_ 根目錄描述元 \_ \_ TABLE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1) 結構。</span><span class="sxs-lookup"><span data-stu-id="16982-105">A helper structure to enable easy initialization of a [**D3D12\_ROOT\_DESCRIPTOR\_TABLE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="16982-106">語法</span><span class="sxs-lookup"><span data-stu-id="16982-106">Syntax</span></span>


```C++
struct CD3DX12_ROOT_DESCRIPTOR_TABLE1  : public D3D12_ROOT_DESCRIPTOR_TABLE1{
       CD3DX12_ROOT_DESCRIPTOR_TABLE1();
       explicit CD3DX12_ROOT_DESCRIPTOR_TABLE1(const D3D12_ROOT_DESCRIPTOR_TABLE1 &o);
       CD3DX12_ROOT_DESCRIPTOR_TABLE1(UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE1* _pDescriptorRanges);
  void inline Init(UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE1* _pDescriptorRanges);
  void static inline Init(D3D12_ROOT_DESCRIPTOR_TABLE1 &rootDescriptorTable, UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE1* _pDescriptorRanges);
};
```



## <a name="members"></a><span data-ttu-id="16982-107">成員</span><span class="sxs-lookup"><span data-stu-id="16982-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="16982-108">**CD3DX12 \_ 根目錄 \_ 描述項 \_ TABLE1 ()**</span><span class="sxs-lookup"><span data-stu-id="16982-108">**CD3DX12\_ROOT\_DESCRIPTOR\_TABLE1()**</span></span>
</dt> <dd>

<span data-ttu-id="16982-109">建立新的、未初始化的 CD3DX12 \_ 根目錄描述項 \_ \_ TABLE1 實例。</span><span class="sxs-lookup"><span data-stu-id="16982-109">Creates a new, uninitialized, instance of a CD3DX12\_ROOT\_DESCRIPTOR\_TABLE1.</span></span>

</dd> <dt>

<span data-ttu-id="16982-110">**明確 CD3DX12 的 \_ 根目錄 \_ 描述項 \_ TABLE1 (const D3D12 \_ 根目錄描述項 \_ \_ table1 &o)**</span><span class="sxs-lookup"><span data-stu-id="16982-110">**explicit CD3DX12\_ROOT\_DESCRIPTOR\_TABLE1(const D3D12\_ROOT\_DESCRIPTOR\_TABLE1 &o)**</span></span>
</dt> <dd>

<span data-ttu-id="16982-111">建立 CD3DX12 根目錄描述元 table1 的新實例 \_ \_ \_ ，並以另一個 [**D3D12 \_ 根 \_ 描述元 \_ table1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1) 結構的內容進行初始化。</span><span class="sxs-lookup"><span data-stu-id="16982-111">Creates a new instance of a CD3DX12\_ROOT\_DESCRIPTOR\_TABLE1, initialized with the contents of another [**D3D12\_ROOT\_DESCRIPTOR\_TABLE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1) structure.</span></span>

</dd> <dt>

<span data-ttu-id="16982-112">**CD3DX12 \_ 根目錄 \_ 描述項 \_ TABLE1 (UINT NUMDESCRIPTORRANGES，const D3D12 \_ 描述項 \_ RANGE1 \* \_ pDescriptorRanges)**</span><span class="sxs-lookup"><span data-stu-id="16982-112">**CD3DX12\_ROOT\_DESCRIPTOR\_TABLE1(UINT numDescriptorRanges, const D3D12\_DESCRIPTOR\_RANGE1\* \_pDescriptorRanges)**</span></span>
</dt> <dd>

<span data-ttu-id="16982-113">建立 CD3DX12 根目錄描述元 TABLE1 的新實例 \_ \_ ，並 \_ 初始化下列參數：</span><span class="sxs-lookup"><span data-stu-id="16982-113">Creates a new instance of a CD3DX12\_ROOT\_DESCRIPTOR\_TABLE1, initializing the following parameters:</span></span>

<span data-ttu-id="16982-114">UINT numDescriptorRanges</span><span class="sxs-lookup"><span data-stu-id="16982-114">UINT numDescriptorRanges</span></span>

<span data-ttu-id="16982-115">const [**D3D12 \_ 描述項 \_ RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) \* \_ pDescriptorRanges</span><span class="sxs-lookup"><span data-stu-id="16982-115">const [**D3D12\_DESCRIPTOR\_RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1)\* \_pDescriptorRanges</span></span>

</dd> <dt>

<span data-ttu-id="16982-116">**內嵌 Init (UINT numDescriptorRanges、const D3D12 \_ 描述項 \_ RANGE1 \* \_ pDescriptorRanges)**</span><span class="sxs-lookup"><span data-stu-id="16982-116">**inline Init(UINT numDescriptorRanges, const D3D12\_DESCRIPTOR\_RANGE1\* \_pDescriptorRanges)**</span></span>
</dt> <dd>

<span data-ttu-id="16982-117">指定初始化下列參數的函式：</span><span class="sxs-lookup"><span data-stu-id="16982-117">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="16982-118">UINT numDescriptorRanges</span><span class="sxs-lookup"><span data-stu-id="16982-118">UINT numDescriptorRanges</span></span>

<span data-ttu-id="16982-119">const [**D3D12 \_ 描述項 \_ RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) \* \_ pDescriptorRanges</span><span class="sxs-lookup"><span data-stu-id="16982-119">const [**D3D12\_DESCRIPTOR\_RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1)\* \_pDescriptorRanges</span></span>

</dd> <dt>

<span data-ttu-id="16982-120">**靜態內嵌 Init (D3D12 \_ 根目錄 \_ 描述項 \_ TABLE1 &RootDescriptorTable、UINT NUMDESCRIPTORRANGES、const D3D12 \_ 描述項 \_ RANGE1 \* \_ pDescriptorRanges)**</span><span class="sxs-lookup"><span data-stu-id="16982-120">**static inline Init(D3D12\_ROOT\_DESCRIPTOR\_TABLE1 &rootDescriptorTable, UINT numDescriptorRanges, const D3D12\_DESCRIPTOR\_RANGE1\* \_pDescriptorRanges)**</span></span>
</dt> <dd>

<span data-ttu-id="16982-121">指定初始化下列參數的函式：</span><span class="sxs-lookup"><span data-stu-id="16982-121">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="16982-122">[**D3D12 \_根目錄 \_ 描述項 \_ TABLE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1) &rootDescriptorTable</span><span class="sxs-lookup"><span data-stu-id="16982-122">[**D3D12\_ROOT\_DESCRIPTOR\_TABLE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1) &rootDescriptorTable</span></span>

<span data-ttu-id="16982-123">UINT numDescriptorRanges</span><span class="sxs-lookup"><span data-stu-id="16982-123">UINT numDescriptorRanges</span></span>

<span data-ttu-id="16982-124">const [**D3D12 \_ 描述項 \_ RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) \* \_ pDescriptorRanges</span><span class="sxs-lookup"><span data-stu-id="16982-124">const [**D3D12\_DESCRIPTOR\_RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1)\* \_pDescriptorRanges</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="16982-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="16982-125">Requirements</span></span>



| <span data-ttu-id="16982-126">需求</span><span class="sxs-lookup"><span data-stu-id="16982-126">Requirement</span></span> | <span data-ttu-id="16982-127">值</span><span class="sxs-lookup"><span data-stu-id="16982-127">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="16982-128">標頭</span><span class="sxs-lookup"><span data-stu-id="16982-128">Header</span></span><br/> | <dl> <span data-ttu-id="16982-129"><dt>D3dx12。h</dt></span><span class="sxs-lookup"><span data-stu-id="16982-129"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16982-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="16982-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16982-131">**D3D12 \_ 根目錄 \_ 描述元 \_ TABLE1**</span><span class="sxs-lookup"><span data-stu-id="16982-131">**D3D12\_ROOT\_DESCRIPTOR\_TABLE1**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1)
</dt> <dt>

[<span data-ttu-id="16982-132">D3D12 的 Helper 結構</span><span class="sxs-lookup"><span data-stu-id="16982-132">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 






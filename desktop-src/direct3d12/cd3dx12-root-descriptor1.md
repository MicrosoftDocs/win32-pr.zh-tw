---
title: 'CD3DX12_ROOT_DESCRIPTOR1 結構 (D3dx12 .h) '
description: 協助程式結構，可讓您輕鬆地初始化 D3D12 \_ 根 \_ DESCRIPTOR1 結構。
ms.assetid: 664822BF-5C27-4541-953F-219894547A6C
keywords:
- CD3DX12_ROOT_DESCRIPTOR1 結構
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_DESCRIPTOR1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66cb64509c82c11180ca3e1d2937dff5d077897d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106977140"
---
# <a name="cd3dx12_root_descriptor1-structure"></a><span data-ttu-id="65cb6-104">CD3DX12 \_ 根 \_ DESCRIPTOR1 結構</span><span class="sxs-lookup"><span data-stu-id="65cb6-104">CD3DX12\_ROOT\_DESCRIPTOR1 structure</span></span>

<span data-ttu-id="65cb6-105">協助程式結構，可讓您輕鬆地初始化 [**D3D12 \_ 根 \_ DESCRIPTOR1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1) 結構。</span><span class="sxs-lookup"><span data-stu-id="65cb6-105">A helper structure to enable easy initialization of a [**D3D12\_ROOT\_DESCRIPTOR1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="65cb6-106">語法</span><span class="sxs-lookup"><span data-stu-id="65cb6-106">Syntax</span></span>


```C++
struct CD3DX12_ROOT_DESCRIPTOR1  : public D3D12_ROOT_DESCRIPTOR1{
       CD3DX12_ROOT_DESCRIPTOR1();
       explicit CD3DX12_ROOT_DESCRIPTOR1(const D3D12_ROOT_DESCRIPTOR1 &o);
       CD3DX12_ROOT_DESCRIPTOR1(UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE);
  void inline Init(UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE);
  void static inline Init(D3D12_ROOT_DESCRIPTOR1 &table, UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE);
};
```



## <a name="members"></a><span data-ttu-id="65cb6-107">成員</span><span class="sxs-lookup"><span data-stu-id="65cb6-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="65cb6-108">**CD3DX12 \_ ROOT \_ DESCRIPTOR1 ()**</span><span class="sxs-lookup"><span data-stu-id="65cb6-108">**CD3DX12\_ROOT\_DESCRIPTOR1()**</span></span>
</dt> <dd>

<span data-ttu-id="65cb6-109">建立新的、未初始化的 CD3DX12 \_ 根 DESCRIPTOR1 實例 \_ 。</span><span class="sxs-lookup"><span data-stu-id="65cb6-109">Creates a new, uninitialized, instance of a CD3DX12\_ROOT\_DESCRIPTOR1.</span></span>

</dd> <dt>

<span data-ttu-id="65cb6-110">**明確 CD3DX12 \_ 根 \_ DESCRIPTOR1 (const D3D12 \_ root \_ DESCRIPTOR1 &o)**</span><span class="sxs-lookup"><span data-stu-id="65cb6-110">**explicit CD3DX12\_ROOT\_DESCRIPTOR1(const D3D12\_ROOT\_DESCRIPTOR1 &o)**</span></span>
</dt> <dd>

<span data-ttu-id="65cb6-111">建立 CD3DX12 根 DESCRIPTOR1 的新實例 \_ \_ ，並以另一個 [**D3D12 \_ 根 \_ DESCRIPTOR1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1) 結構的內容進行初始化。</span><span class="sxs-lookup"><span data-stu-id="65cb6-111">Creates a new instance of a CD3DX12\_ROOT\_DESCRIPTOR1, initialized with the contents of another [**D3D12\_ROOT\_DESCRIPTOR1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1) structure.</span></span>

</dd> <dt>

<span data-ttu-id="65cb6-112">**CD3DX12 \_ ROOT \_ DESCRIPTOR1 (uint SHADERREGISTER，uint registerSpace = 0，D3D12 \_ 根描述元旗標 \_ 旗標 \_ = D3D12 \_ 根目錄描述元旗標 \_ \_ \_ 無)**</span><span class="sxs-lookup"><span data-stu-id="65cb6-112">**CD3DX12\_ROOT\_DESCRIPTOR1(UINT shaderRegister, UINT registerSpace = 0, D3D12\_ROOT\_DESCRIPTOR\_FLAGS flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="65cb6-113">建立 CD3DX12 根 DESCRIPTOR1 的新實例 \_ \_ ，並初始化下列參數：</span><span class="sxs-lookup"><span data-stu-id="65cb6-113">Creates a new instance of a CD3DX12\_ROOT\_DESCRIPTOR1, initializing the following parameters:</span></span>

<span data-ttu-id="65cb6-114">UINT shaderRegister</span><span class="sxs-lookup"><span data-stu-id="65cb6-114">UINT shaderRegister</span></span>

<span data-ttu-id="65cb6-115">UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="65cb6-115">UINT registerSpace = 0</span></span>

<span data-ttu-id="65cb6-116">[**D3D12 \_根 \_ 描述 \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) 元旗標旗標 = D3D12 \_ 根目錄 \_ 描述元旗標 \_ \_ 無</span><span class="sxs-lookup"><span data-stu-id="65cb6-116">[**D3D12\_ROOT\_DESCRIPTOR\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="65cb6-117">**內嵌 Init (UINT shaderRegister，UINT registerSpace = 0，D3D12 \_ 根描述元旗標旗標 \_ \_ = D3D12 根目錄描述元旗標 \_ \_ \_ \_ 無)**</span><span class="sxs-lookup"><span data-stu-id="65cb6-117">**inline Init(UINT shaderRegister, UINT registerSpace = 0, D3D12\_ROOT\_DESCRIPTOR\_FLAGS flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="65cb6-118">指定初始化下列參數的函式：</span><span class="sxs-lookup"><span data-stu-id="65cb6-118">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="65cb6-119">UINT shaderRegister</span><span class="sxs-lookup"><span data-stu-id="65cb6-119">UINT shaderRegister</span></span>

<span data-ttu-id="65cb6-120">UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="65cb6-120">UINT registerSpace = 0</span></span>

<span data-ttu-id="65cb6-121">[**D3D12 \_根 \_ 描述 \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) 元旗標旗標 = D3D12 \_ 根目錄 \_ 描述元旗標 \_ \_ 無</span><span class="sxs-lookup"><span data-stu-id="65cb6-121">[**D3D12\_ROOT\_DESCRIPTOR\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="65cb6-122">**靜態內嵌 Init (D3D12 \_ 根 \_ DESCRIPTOR1 &資料表、uint SHADERREGISTER、uint registerSpace = 0、D3D12 \_ 根目錄描述元旗標 \_ \_ = D3D12 \_ 根目錄描述項旗標 \_ \_ \_ 無)**</span><span class="sxs-lookup"><span data-stu-id="65cb6-122">**static inline Init(D3D12\_ROOT\_DESCRIPTOR1 &table, UINT shaderRegister, UINT registerSpace = 0, D3D12\_ROOT\_DESCRIPTOR\_FLAGS flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="65cb6-123">指定初始化下列參數的函式：</span><span class="sxs-lookup"><span data-stu-id="65cb6-123">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="65cb6-124">[**D3D12 \_根 \_ DESCRIPTOR1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1) &資料表</span><span class="sxs-lookup"><span data-stu-id="65cb6-124">[**D3D12\_ROOT\_DESCRIPTOR1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1) &table</span></span>

<span data-ttu-id="65cb6-125">UINT shaderRegister</span><span class="sxs-lookup"><span data-stu-id="65cb6-125">UINT shaderRegister</span></span>

<span data-ttu-id="65cb6-126">UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="65cb6-126">UINT registerSpace = 0</span></span>

<span data-ttu-id="65cb6-127">[**D3D12 \_根 \_ 描述 \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) 元旗標旗標 = D3D12 \_ 根目錄 \_ 描述元旗標 \_ \_ 無</span><span class="sxs-lookup"><span data-stu-id="65cb6-127">[**D3D12\_ROOT\_DESCRIPTOR\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="65cb6-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="65cb6-128">Requirements</span></span>



| <span data-ttu-id="65cb6-129">需求</span><span class="sxs-lookup"><span data-stu-id="65cb6-129">Requirement</span></span> | <span data-ttu-id="65cb6-130">值</span><span class="sxs-lookup"><span data-stu-id="65cb6-130">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="65cb6-131">標頭</span><span class="sxs-lookup"><span data-stu-id="65cb6-131">Header</span></span><br/> | <dl> <span data-ttu-id="65cb6-132"><dt>D3dx12。h</dt></span><span class="sxs-lookup"><span data-stu-id="65cb6-132"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65cb6-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="65cb6-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65cb6-134">**D3D12 \_ 根 \_ DESCRIPTOR1**</span><span class="sxs-lookup"><span data-stu-id="65cb6-134">**D3D12\_ROOT\_DESCRIPTOR1**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1)
</dt> <dt>

[<span data-ttu-id="65cb6-135">D3D12 的 Helper 結構</span><span class="sxs-lookup"><span data-stu-id="65cb6-135">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 






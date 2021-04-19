---
title: 'CD3DX12_ROOT_DESCRIPTOR 結構 (D3dx12 .h) '
description: 協助程式結構，可讓您輕鬆地初始化 D3D12 \_ 根目錄 \_ 描述元結構。
ms.assetid: DB05BAB7-DD30-4EC7-8D66-C0B2D8DD7BAC
keywords:
- CD3DX12_ROOT_DESCRIPTOR 結構
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_DESCRIPTOR
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 710064436e0287b570700ff5812b728ca62be56d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106989224"
---
# <a name="cd3dx12_root_descriptor-structure"></a><span data-ttu-id="cc136-104">CD3DX12 \_ 根目錄 \_ 描述元結構</span><span class="sxs-lookup"><span data-stu-id="cc136-104">CD3DX12\_ROOT\_DESCRIPTOR structure</span></span>

<span data-ttu-id="cc136-105">協助程式結構，可讓您輕鬆地初始化 [**D3D12 \_ 根目錄 \_ 描述**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor) 元結構。</span><span class="sxs-lookup"><span data-stu-id="cc136-105">A helper structure to enable easy initialization of a [**D3D12\_ROOT\_DESCRIPTOR**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc136-106">語法</span><span class="sxs-lookup"><span data-stu-id="cc136-106">Syntax</span></span>


```C++
struct CD3DX12_ROOT_DESCRIPTOR  : public D3D12_ROOT_DESCRIPTOR{
       CD3DX12_ROOT_DESCRIPTOR();
       explicit CD3DX12_ROOT_DESCRIPTOR(const D3D12_ROOT_DESCRIPTOR &o);
       CD3DX12_ROOT_DESCRIPTOR(UINT shaderRegister, UINT registerSpace = 0);
  void inline Init(UINT shaderRegister, UINT registerSpace = 0);
  void static inline Init(D3D12_ROOT_DESCRIPTOR &table, UINT shaderRegister, UINT registerSpace = 0);
};
```



## <a name="members"></a><span data-ttu-id="cc136-107">成員</span><span class="sxs-lookup"><span data-stu-id="cc136-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="cc136-108">**CD3DX12 \_ 根目錄 \_ 描述元 ()**</span><span class="sxs-lookup"><span data-stu-id="cc136-108">**CD3DX12\_ROOT\_DESCRIPTOR()**</span></span>
</dt> <dd>

<span data-ttu-id="cc136-109">建立新的、未初始化的 CD3DX12 \_ 根目錄描述項實例 \_ 。</span><span class="sxs-lookup"><span data-stu-id="cc136-109">Creates a new, uninitialized, instance of a CD3DX12\_ROOT\_DESCRIPTOR.</span></span>

</dd> <dt>

<span data-ttu-id="cc136-110">**明確 CD3DX12 的 \_ 根 \_ 描述元 (const D3D12 \_ 根描述元 \_ &o)**</span><span class="sxs-lookup"><span data-stu-id="cc136-110">**explicit CD3DX12\_ROOT\_DESCRIPTOR(const D3D12\_ROOT\_DESCRIPTOR &o)**</span></span>
</dt> <dd>

<span data-ttu-id="cc136-111">建立 CD3DX12 根描述元的新 \_ 實例 \_ ，並以另一個 [**D3D12 \_ 根 \_ 描述**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor) 元結構的內容進行初始化。</span><span class="sxs-lookup"><span data-stu-id="cc136-111">Creates a new instance of a CD3DX12\_ROOT\_DESCRIPTOR, initialized with the contents of another [**D3D12\_ROOT\_DESCRIPTOR**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor) structure.</span></span>

</dd> <dt>

<span data-ttu-id="cc136-112">**CD3DX12 \_ 根 \_ 描述元 (uint SHADERREGISTER，uint registerSpace = 0)**</span><span class="sxs-lookup"><span data-stu-id="cc136-112">**CD3DX12\_ROOT\_DESCRIPTOR(UINT shaderRegister, UINT registerSpace = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="cc136-113">建立 CD3DX12 根描述元的新 \_ 實例 \_ ，並初始化下列參數：</span><span class="sxs-lookup"><span data-stu-id="cc136-113">Creates a new instance of a CD3DX12\_ROOT\_DESCRIPTOR, initializing the following parameters:</span></span>

<span data-ttu-id="cc136-114">UINT shaderRegister</span><span class="sxs-lookup"><span data-stu-id="cc136-114">UINT shaderRegister</span></span>

<span data-ttu-id="cc136-115"> (opt) UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="cc136-115">(opt) UINT registerSpace = 0</span></span>

</dd> <dt>

<span data-ttu-id="cc136-116">**內嵌 Init (UINT shaderRegister，UINT registerSpace = 0)**</span><span class="sxs-lookup"><span data-stu-id="cc136-116">**inline Init(UINT shaderRegister, UINT registerSpace = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="cc136-117">指定初始化下列參數的函式：</span><span class="sxs-lookup"><span data-stu-id="cc136-117">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="cc136-118">UINT shaderRegister</span><span class="sxs-lookup"><span data-stu-id="cc136-118">UINT shaderRegister</span></span>

<span data-ttu-id="cc136-119"> (opt) UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="cc136-119">(opt) UINT registerSpace = 0</span></span>

</dd> <dt>

<span data-ttu-id="cc136-120">**靜態內嵌 Init (D3D12 \_ 根 \_ 描述元 &資料表、uint SHADERREGISTER、uint registerSpace = 0)**</span><span class="sxs-lookup"><span data-stu-id="cc136-120">**static inline Init(D3D12\_ROOT\_DESCRIPTOR &table, UINT shaderRegister, UINT registerSpace = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="cc136-121">指定初始化下列參數的函式：</span><span class="sxs-lookup"><span data-stu-id="cc136-121">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="cc136-122">[**D3D12 \_根 \_ 描述**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor) 元 &資料表</span><span class="sxs-lookup"><span data-stu-id="cc136-122">[**D3D12\_ROOT\_DESCRIPTOR**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor) &table</span></span>

<span data-ttu-id="cc136-123">UINT shaderRegister</span><span class="sxs-lookup"><span data-stu-id="cc136-123">UINT shaderRegister</span></span>

<span data-ttu-id="cc136-124"> (opt) UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="cc136-124">(opt) UINT registerSpace = 0</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cc136-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="cc136-125">Requirements</span></span>



| <span data-ttu-id="cc136-126">需求</span><span class="sxs-lookup"><span data-stu-id="cc136-126">Requirement</span></span> | <span data-ttu-id="cc136-127">值</span><span class="sxs-lookup"><span data-stu-id="cc136-127">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="cc136-128">標頭</span><span class="sxs-lookup"><span data-stu-id="cc136-128">Header</span></span><br/> | <dl> <span data-ttu-id="cc136-129"><dt>D3dx12。h</dt></span><span class="sxs-lookup"><span data-stu-id="cc136-129"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc136-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cc136-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc136-131">**D3D12 \_ 根目錄 \_ 描述元**</span><span class="sxs-lookup"><span data-stu-id="cc136-131">**D3D12\_ROOT\_DESCRIPTOR**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor)
</dt> <dt>

[<span data-ttu-id="cc136-132">D3D12 的 Helper 結構</span><span class="sxs-lookup"><span data-stu-id="cc136-132">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 






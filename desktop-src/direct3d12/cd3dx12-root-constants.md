---
title: 'CD3DX12_ROOT_CONSTANTS 結構 (D3dx12 .h) '
description: Helper 結構，可讓您輕鬆地初始化 D3D12 \_ 根 \_ 常數結構。
ms.assetid: 2F517DCE-BC0C-4678-9C25-D826036F99A8
keywords:
- CD3DX12_ROOT_CONSTANTS 結構
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_CONSTANTS
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7a1f81a429b083400adad60f316cc90c4ede1d9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106993860"
---
# <a name="cd3dx12_root_constants-structure"></a><span data-ttu-id="022b6-104">CD3DX12 \_ 根 \_ 常數結構</span><span class="sxs-lookup"><span data-stu-id="022b6-104">CD3DX12\_ROOT\_CONSTANTS structure</span></span>

<span data-ttu-id="022b6-105">Helper 結構，可讓您輕鬆地初始化 [**D3D12 \_ 根 \_ 常數**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) 結構。</span><span class="sxs-lookup"><span data-stu-id="022b6-105">A helper structure to enable easy initialization of a [**D3D12\_ROOT\_CONSTANTS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="022b6-106">語法</span><span class="sxs-lookup"><span data-stu-id="022b6-106">Syntax</span></span>


```C++
struct CD3DX12_ROOT_CONSTANTS  : public D3D12_ROOT_CONSTANTS{
       CD3DX12_ROOT_CONSTANTS();
       explicit CD3DX12_ROOT_CONSTANTS(const D3D12_ROOT_CONSTANTS &o);
       CD3DX12_ROOT_CONSTANTS(UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0);
  void inline Init(UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0);
  void static inline Init(D3D12_ROOT_CONSTANTS &rootConstants, UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0);
};
```



## <a name="members"></a><span data-ttu-id="022b6-107">成員</span><span class="sxs-lookup"><span data-stu-id="022b6-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="022b6-108">**CD3DX12 \_ 根 \_ 常數 ()**</span><span class="sxs-lookup"><span data-stu-id="022b6-108">**CD3DX12\_ROOT\_CONSTANTS()**</span></span>
</dt> <dd>

<span data-ttu-id="022b6-109">建立 CD3DX12 根常數的新、未初始化的 \_ 實例 \_ 。</span><span class="sxs-lookup"><span data-stu-id="022b6-109">Creates a new, uninitialized, instance of a CD3DX12\_ROOT\_CONSTANTS.</span></span>

</dd> <dt>

<span data-ttu-id="022b6-110">**明確 CD3DX12 的 \_ 根 \_ 常數 (const D3D12 \_ 根 \_ 常數 &o)**</span><span class="sxs-lookup"><span data-stu-id="022b6-110">**explicit CD3DX12\_ROOT\_CONSTANTS(const D3D12\_ROOT\_CONSTANTS &o)**</span></span>
</dt> <dd>

<span data-ttu-id="022b6-111">建立 CD3DX12 根常數的新實例 \_ \_ ，並以另一個 [**D3D12 \_ 根 \_ 常數**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) 結構的內容進行初始化。</span><span class="sxs-lookup"><span data-stu-id="022b6-111">Creates a new instance of a CD3DX12\_ROOT\_CONSTANTS, initialized with the contents of another [**D3D12\_ROOT\_CONSTANTS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) structure.</span></span>

</dd> <dt>

<span data-ttu-id="022b6-112">**CD3DX12 \_ 根 \_ 常數 (uint NUM32BITVALUES、uint SHADERREGISTER、uint registerSpace = 0)**</span><span class="sxs-lookup"><span data-stu-id="022b6-112">**CD3DX12\_ROOT\_CONSTANTS(UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="022b6-113">建立 CD3DX12 根常數的新實例 \_ \_ ，並初始化下列參數：</span><span class="sxs-lookup"><span data-stu-id="022b6-113">Creates a new instance of a CD3DX12\_ROOT\_CONSTANTS, initializing the following parameters:</span></span>

<span data-ttu-id="022b6-114">UINT num32BitValues</span><span class="sxs-lookup"><span data-stu-id="022b6-114">UINT num32BitValues</span></span>

<span data-ttu-id="022b6-115">UINT shaderRegister</span><span class="sxs-lookup"><span data-stu-id="022b6-115">UINT shaderRegister</span></span>

<span data-ttu-id="022b6-116"> (opt) UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="022b6-116">(opt) UINT registerSpace = 0</span></span>

</dd> <dt>

<span data-ttu-id="022b6-117">**內嵌初始 (UINT num32BitValues、UINT shaderRegister、UINT registerSpace = 0)**</span><span class="sxs-lookup"><span data-stu-id="022b6-117">**inline Init(UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="022b6-118">指定初始化下列參數的函式：</span><span class="sxs-lookup"><span data-stu-id="022b6-118">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="022b6-119">UINT num32BitValues</span><span class="sxs-lookup"><span data-stu-id="022b6-119">UINT num32BitValues</span></span>

<span data-ttu-id="022b6-120">UINT shaderRegister</span><span class="sxs-lookup"><span data-stu-id="022b6-120">UINT shaderRegister</span></span>

<span data-ttu-id="022b6-121"> (opt) UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="022b6-121">(opt) UINT registerSpace = 0</span></span>

</dd> <dt>

<span data-ttu-id="022b6-122">**靜態內嵌 Init (D3D12 \_ 根 \_ 常數 &ROOTCONSTANTS、uint NUM32BITVALUES、uint SHADERREGISTER、UINT registerSpace = 0)**</span><span class="sxs-lookup"><span data-stu-id="022b6-122">**static inline Init(D3D12\_ROOT\_CONSTANTS &rootConstants, UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="022b6-123">指定初始化下列參數的函式：</span><span class="sxs-lookup"><span data-stu-id="022b6-123">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="022b6-124">[**D3D12 \_根 \_ 常數**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) &rootConstants</span><span class="sxs-lookup"><span data-stu-id="022b6-124">[**D3D12\_ROOT\_CONSTANTS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) &rootConstants</span></span>

<span data-ttu-id="022b6-125">UINT num32BitValues</span><span class="sxs-lookup"><span data-stu-id="022b6-125">UINT num32BitValues</span></span>

<span data-ttu-id="022b6-126">UINT shaderRegister</span><span class="sxs-lookup"><span data-stu-id="022b6-126">UINT shaderRegister</span></span>

<span data-ttu-id="022b6-127"> (opt) UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="022b6-127">(opt) UINT registerSpace = 0</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="022b6-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="022b6-128">Requirements</span></span>



| <span data-ttu-id="022b6-129">需求</span><span class="sxs-lookup"><span data-stu-id="022b6-129">Requirement</span></span> | <span data-ttu-id="022b6-130">值</span><span class="sxs-lookup"><span data-stu-id="022b6-130">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="022b6-131">標頭</span><span class="sxs-lookup"><span data-stu-id="022b6-131">Header</span></span><br/> | <dl> <span data-ttu-id="022b6-132"><dt>D3dx12。h</dt></span><span class="sxs-lookup"><span data-stu-id="022b6-132"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="022b6-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="022b6-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="022b6-134">**D3D12 \_ 根 \_ 常數**</span><span class="sxs-lookup"><span data-stu-id="022b6-134">**D3D12\_ROOT\_CONSTANTS**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants)
</dt> <dt>

[<span data-ttu-id="022b6-135">D3D12 的 Helper 結構</span><span class="sxs-lookup"><span data-stu-id="022b6-135">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 






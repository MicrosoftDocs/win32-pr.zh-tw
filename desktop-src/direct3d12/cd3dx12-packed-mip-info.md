---
title: 'CD3DX12_PACKED_MIP_INFO 結構 (D3dx12 .h) '
description: 協助程式結構，可讓您輕鬆地初始化 D3D12 \_ 壓縮 \_ MIP \_ 資訊結構。
ms.assetid: B3549D78-C354-48FC-A012-1F835DBD585E
keywords:
- CD3DX12_PACKED_MIP_INFO 結構
topic_type:
- apiref
api_name:
- CD3DX12_PACKED_MIP_INFO
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f4565bbac6189cffc5358213437463b4abc0322
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106997372"
---
# <a name="cd3dx12_packed_mip_info-structure"></a><span data-ttu-id="82e5b-104">CD3DX12 \_ 封裝的 \_ MIP \_ 資訊結構</span><span class="sxs-lookup"><span data-stu-id="82e5b-104">CD3DX12\_PACKED\_MIP\_INFO structure</span></span>

<span data-ttu-id="82e5b-105">協助程式結構，可讓您輕鬆地初始化 [**D3D12 \_ 壓縮 \_ MIP \_ 資訊**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_packed_mip_info) 結構。</span><span class="sxs-lookup"><span data-stu-id="82e5b-105">A helper structure to enable easy initialization of a [**D3D12\_PACKED\_MIP\_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_packed_mip_info) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="82e5b-106">語法</span><span class="sxs-lookup"><span data-stu-id="82e5b-106">Syntax</span></span>


```C++
struct CD3DX12_PACKED_MIP_INFO  : public D3D12_PACKED_MIP_INFO{
   CD3DX12_PACKED_MIP_INFO();
   explicit CD3DX12_PACKED_MIP_INFO(const D3D12_PACKED_MIP_INFO &o);
   CD3DX12_PACKED_MIP_INFO(UINT8 numStandardMips, UINT8 numPackedMips, UINT numTilesForPackedMips, UINT startTileIndexInOverallResource);
   operator const D3D12_PACKED_MIP_INFO&() const;
};
```



## <a name="members"></a><span data-ttu-id="82e5b-107">成員</span><span class="sxs-lookup"><span data-stu-id="82e5b-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="82e5b-108">**CD3DX12 \_ 封裝的 \_ MIP \_ INFO ()**</span><span class="sxs-lookup"><span data-stu-id="82e5b-108">**CD3DX12\_PACKED\_MIP\_INFO()**</span></span>
</dt> <dd>

<span data-ttu-id="82e5b-109">建立 CD3DX12 \_ 壓縮 MIP 資訊之未初始化的新實例 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="82e5b-109">Creates a new, uninitialized, instance of a CD3DX12\_PACKED\_MIP\_INFO.</span></span>

</dd> <dt>

<span data-ttu-id="82e5b-110">**明確 CD3DX12 \_ 壓縮 \_ mip \_ 資訊 (const D3D12 \_ 封裝的 \_ mip \_ info &o)**</span><span class="sxs-lookup"><span data-stu-id="82e5b-110">**explicit CD3DX12\_PACKED\_MIP\_INFO(const D3D12\_PACKED\_MIP\_INFO &o)**</span></span>
</dt> <dd>

<span data-ttu-id="82e5b-111">建立 CD3DX12 \_ 壓縮 mip 資訊的新實例 \_ \_ ，並使用另一個 [**D3D12 壓縮的 \_ \_ mip \_ 資訊**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_packed_mip_info) 結構的內容進行初始化。</span><span class="sxs-lookup"><span data-stu-id="82e5b-111">Creates a new instance of a CD3DX12\_PACKED\_MIP\_INFO, initialized with the contents of another [**D3D12\_PACKED\_MIP\_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_packed_mip_info) structure.</span></span>

</dd> <dt>

<span data-ttu-id="82e5b-112">**CD3DX12 \_ 封裝的 \_ MIP \_ INFO (UINT8 NumStandardMips、UINT8 NumPackedMips、UINT NumTilesForPackedMips、UINT startTileIndexInOverallResource)**</span><span class="sxs-lookup"><span data-stu-id="82e5b-112">**CD3DX12\_PACKED\_MIP\_INFO(UINT8 numStandardMips, UINT8 numPackedMips, UINT numTilesForPackedMips, UINT startTileIndexInOverallResource)**</span></span>
</dt> <dd>

<span data-ttu-id="82e5b-113">建立 CD3DX12 \_ 壓縮 MIP 資訊的新實例 \_ ，並 \_ 初始化下列參數：</span><span class="sxs-lookup"><span data-stu-id="82e5b-113">Creates a new instance of a CD3DX12\_PACKED\_MIP\_INFO, initializing the following parameters:</span></span>

<span data-ttu-id="82e5b-114">UINT8 numStandardMips</span><span class="sxs-lookup"><span data-stu-id="82e5b-114">UINT8 numStandardMips</span></span>

<span data-ttu-id="82e5b-115">UINT8 numPackedMips</span><span class="sxs-lookup"><span data-stu-id="82e5b-115">UINT8 numPackedMips</span></span>

<span data-ttu-id="82e5b-116">UINT numTilesForPackedMips</span><span class="sxs-lookup"><span data-stu-id="82e5b-116">UINT numTilesForPackedMips</span></span>

<span data-ttu-id="82e5b-117">UINT startTileIndexInOverallResource</span><span class="sxs-lookup"><span data-stu-id="82e5b-117">UINT startTileIndexInOverallResource</span></span>

</dd> <dt>

<span data-ttu-id="82e5b-118">**運算子 const D3D12 \_ 壓縮 \_ MIP \_ INFO& () const**</span><span class="sxs-lookup"><span data-stu-id="82e5b-118">**operator const D3D12\_PACKED\_MIP\_INFO&() const**</span></span>
</dt> <dd>

<span data-ttu-id="82e5b-119">針對父結構類型定義 & 的傳址運算子。</span><span class="sxs-lookup"><span data-stu-id="82e5b-119">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="82e5b-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="82e5b-120">Requirements</span></span>



| <span data-ttu-id="82e5b-121">需求</span><span class="sxs-lookup"><span data-stu-id="82e5b-121">Requirement</span></span> | <span data-ttu-id="82e5b-122">值</span><span class="sxs-lookup"><span data-stu-id="82e5b-122">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="82e5b-123">標頭</span><span class="sxs-lookup"><span data-stu-id="82e5b-123">Header</span></span><br/> | <dl> <span data-ttu-id="82e5b-124"><dt>D3dx12。h</dt></span><span class="sxs-lookup"><span data-stu-id="82e5b-124"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82e5b-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="82e5b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82e5b-126">**D3D12 \_ 封裝的 \_ MIP \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="82e5b-126">**D3D12\_PACKED\_MIP\_INFO**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_packed_mip_info)
</dt> <dt>

[<span data-ttu-id="82e5b-127">D3D12 的 Helper 結構</span><span class="sxs-lookup"><span data-stu-id="82e5b-127">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 






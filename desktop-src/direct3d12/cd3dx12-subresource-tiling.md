---
title: 'CD3DX12_SUBRESOURCE_TILING 結構 (D3dx12 .h) '
description: 協助程式結構，可讓您輕鬆地初始化 D3D12 \_ SUBRESOURCE \_ 平鋪結構。
ms.assetid: 102E5E25-300B-40F2-A953-E40AD7EE61AD
keywords:
- CD3DX12_SUBRESOURCE_TILING 結構
topic_type:
- apiref
api_name:
- CD3DX12_SUBRESOURCE_TILING
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07677c8a8367f58016a0236cf0b5558b852bef01
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106992296"
---
# <a name="cd3dx12_subresource_tiling-structure"></a><span data-ttu-id="db2df-104">CD3DX12 \_ SUBRESOURCE \_ 平鋪結構</span><span class="sxs-lookup"><span data-stu-id="db2df-104">CD3DX12\_SUBRESOURCE\_TILING structure</span></span>

<span data-ttu-id="db2df-105">協助程式結構，可讓您輕鬆地初始化 [**D3D12 \_ SUBRESOURCE \_ 平鋪**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_tiling) 結構。</span><span class="sxs-lookup"><span data-stu-id="db2df-105">A helper structure to enable easy initialization of a [**D3D12\_SUBRESOURCE\_TILING**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_tiling) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="db2df-106">語法</span><span class="sxs-lookup"><span data-stu-id="db2df-106">Syntax</span></span>


```C++
struct CD3DX12_SUBRESOURCE_TILING  : public D3D12_SUBRESOURCE_TILING{
   CD3DX12_SUBRESOURCE_TILING();
   explicit CD3DX12_SUBRESOURCE_TILING(const D3D12_SUBRESOURCE_TILING &o);
   CD3DX12_SUBRESOURCE_TILING(UINT widthInTiles, UINT16 heightInTiles, UINT16 depthInTiles, UINT startTileIndexInOverallResource);
   operator const D3D12_SUBRESOURCE_TILING&() const;
};
```



## <a name="members"></a><span data-ttu-id="db2df-107">成員</span><span class="sxs-lookup"><span data-stu-id="db2df-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="db2df-108">**CD3DX12 \_ SUBRESOURCE \_ () 平並排**</span><span class="sxs-lookup"><span data-stu-id="db2df-108">**CD3DX12\_SUBRESOURCE\_TILING()**</span></span>
</dt> <dd>

<span data-ttu-id="db2df-109">建立新的、未初始化的 CD3DX12 \_ SUBRESOURCE \_ 平鋪實例。</span><span class="sxs-lookup"><span data-stu-id="db2df-109">Creates a new, uninitialized, instance of a CD3DX12\_SUBRESOURCE\_TILING.</span></span>

</dd> <dt>

<span data-ttu-id="db2df-110">**明確的 CD3DX12 SUBRESOURCE 並排顯示 \_ \_ (const D3D12 \_ SUBRESOURCE \_ 平鋪 &o)**</span><span class="sxs-lookup"><span data-stu-id="db2df-110">**explicit CD3DX12\_SUBRESOURCE\_TILING(const D3D12\_SUBRESOURCE\_TILING &o)**</span></span>
</dt> <dd>

<span data-ttu-id="db2df-111">建立 CD3DX12 \_ SUBRESOURCE 平鋪的新實例 \_ ，並以另一個 [**D3D12 \_ SUBRESOURCE \_ 平鋪**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_tiling) 結構的內容進行初始化。</span><span class="sxs-lookup"><span data-stu-id="db2df-111">Creates a new instance of a CD3DX12\_SUBRESOURCE\_TILING, initialized with the contents of another [**D3D12\_SUBRESOURCE\_TILING**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_tiling) structure.</span></span>

</dd> <dt>

<span data-ttu-id="db2df-112">**CD3DX12 \_ SUBRESOURCE \_ (UINT WIDTHINTILES、uint16 HEIGHTINTILES、uint16 DEPTHINTILES、UINT startTileIndexInOverallResource)**</span><span class="sxs-lookup"><span data-stu-id="db2df-112">**CD3DX12\_SUBRESOURCE\_TILING(UINT widthInTiles, UINT16 heightInTiles, UINT16 depthInTiles, UINT startTileIndexInOverallResource)**</span></span>
</dt> <dd>

<span data-ttu-id="db2df-113">建立 CD3DX12 \_ SUBRESOURCE 平鋪的新實例 \_ ，並初始化下列參數：</span><span class="sxs-lookup"><span data-stu-id="db2df-113">Creates a new instance of a CD3DX12\_SUBRESOURCE\_TILING, initializing the following parameters:</span></span>

<span data-ttu-id="db2df-114">UINT widthInTiles</span><span class="sxs-lookup"><span data-stu-id="db2df-114">UINT widthInTiles</span></span>

<span data-ttu-id="db2df-115">UINT16 heightInTiles</span><span class="sxs-lookup"><span data-stu-id="db2df-115">UINT16 heightInTiles</span></span>

<span data-ttu-id="db2df-116">UINT16 depthInTiles</span><span class="sxs-lookup"><span data-stu-id="db2df-116">UINT16 depthInTiles</span></span>

<span data-ttu-id="db2df-117">UINT startTileIndexInOverallResource</span><span class="sxs-lookup"><span data-stu-id="db2df-117">UINT startTileIndexInOverallResource</span></span>

</dd> <dt>

<span data-ttu-id="db2df-118">**運算子 const D3D12 \_ SUBRESOURCE \_& () const**</span><span class="sxs-lookup"><span data-stu-id="db2df-118">**operator const D3D12\_SUBRESOURCE\_TILING&() const**</span></span>
</dt> <dd>

<span data-ttu-id="db2df-119">針對父結構類型定義 & 的傳址運算子。</span><span class="sxs-lookup"><span data-stu-id="db2df-119">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="db2df-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="db2df-120">Requirements</span></span>



| <span data-ttu-id="db2df-121">需求</span><span class="sxs-lookup"><span data-stu-id="db2df-121">Requirement</span></span> | <span data-ttu-id="db2df-122">值</span><span class="sxs-lookup"><span data-stu-id="db2df-122">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="db2df-123">標頭</span><span class="sxs-lookup"><span data-stu-id="db2df-123">Header</span></span><br/> | <dl> <span data-ttu-id="db2df-124"><dt>D3dx12。h</dt></span><span class="sxs-lookup"><span data-stu-id="db2df-124"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db2df-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="db2df-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db2df-126">**D3D12 \_ SUBRESOURCE \_ 平鋪**</span><span class="sxs-lookup"><span data-stu-id="db2df-126">**D3D12\_SUBRESOURCE\_TILING**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_tiling)
</dt> <dt>

[<span data-ttu-id="db2df-127">D3D12 的 Helper 結構</span><span class="sxs-lookup"><span data-stu-id="db2df-127">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 






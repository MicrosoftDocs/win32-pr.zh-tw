---
title: 'CD3DX12_TILED_RESOURCE_COORDINATE 結構 (D3dx12 .h) '
description: 協助程式結構，可讓您輕鬆地初始化 D3D12 並排顯示的 \_ \_ 資源 \_ 座標結構。
ms.assetid: B337ED04-E2C6-4B89-80F1-92C0854A6AF2
keywords:
- CD3DX12_TILED_RESOURCE_COORDINATE 結構
topic_type:
- apiref
api_name:
- CD3DX12_TILED_RESOURCE_COORDINATE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 281afeab8d1172e9cae749512612129dd001161b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106993859"
---
# <a name="cd3dx12_tiled_resource_coordinate-structure"></a><span data-ttu-id="cd707-104">CD3DX12 並排顯示的 \_ \_ 資源 \_ 座標結構</span><span class="sxs-lookup"><span data-stu-id="cd707-104">CD3DX12\_TILED\_RESOURCE\_COORDINATE structure</span></span>

<span data-ttu-id="cd707-105">協助程式結構，可讓您輕鬆地初始化 D3D12 並排顯示的 [**\_ \_ 資源 \_ 座標**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) 結構。</span><span class="sxs-lookup"><span data-stu-id="cd707-105">A helper structure to enable easy initialization of a [**D3D12\_TILED\_RESOURCE\_COORDINATE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd707-106">語法</span><span class="sxs-lookup"><span data-stu-id="cd707-106">Syntax</span></span>


```C++
struct CD3DX12_TILED_RESOURCE_COORDINATE  : public D3D12_TILED_RESOURCE_COORDINATE{
   CD3DX12_TILED_RESOURCE_COORDINATE();
   explicit CD3DX12_TILED_RESOURCE_COORDINATE(const D3D12_TILED_RESOURCE_COORDINATE &o);
   CD3DX12_TILED_RESOURCE_COORDINATE(UINT x, UINT y, UINT z, UINT subresource);
   operator const D3D12_TILED_RESOURCE_COORDINATE&() const;
};
```



## <a name="members"></a><span data-ttu-id="cd707-107">成員</span><span class="sxs-lookup"><span data-stu-id="cd707-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="cd707-108">**CD3DX12 並排顯示的 \_ \_ 資源 \_ 座標 ()**</span><span class="sxs-lookup"><span data-stu-id="cd707-108">**CD3DX12\_TILED\_RESOURCE\_COORDINATE()**</span></span>
</dt> <dd>

<span data-ttu-id="cd707-109">建立新的、未初始化的實例，其為 CD3DX12 並排顯示的 \_ \_ 資源 \_ 座標。</span><span class="sxs-lookup"><span data-stu-id="cd707-109">Creates a new, uninitialized, instance of a CD3DX12\_TILED\_RESOURCE\_COORDINATE.</span></span>

</dd> <dt>

<span data-ttu-id="cd707-110">**明確 CD3DX12 的並排 \_ \_ 資源 \_ 座標 (const D3D12 並排顯示 \_ \_ 資源 \_ 座標 &o)**</span><span class="sxs-lookup"><span data-stu-id="cd707-110">**explicit CD3DX12\_TILED\_RESOURCE\_COORDINATE(const D3D12\_TILED\_RESOURCE\_COORDINATE &o)**</span></span>
</dt> <dd>

<span data-ttu-id="cd707-111">建立 CD3DX12 平並排資源座標的新實例 \_ \_ \_ ，並以另一個 [**D3D12 並排 \_ \_ 資源 \_ 座標**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) 結構的內容進行初始化。</span><span class="sxs-lookup"><span data-stu-id="cd707-111">Creates a new instance of a CD3DX12\_TILED\_RESOURCE\_COORDINATE, initialized with the contents of another [**D3D12\_TILED\_RESOURCE\_COORDINATE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) structure.</span></span>

</dd> <dt>

<span data-ttu-id="cd707-112">**CD3DX12 並排顯示 \_ \_ \_ 的資源座標 (UINT x、UINT y、UINT z、uint subresource)**</span><span class="sxs-lookup"><span data-stu-id="cd707-112">**CD3DX12\_TILED\_RESOURCE\_COORDINATE(UINT x, UINT y, UINT z, UINT subresource)**</span></span>
</dt> <dd>

<span data-ttu-id="cd707-113">建立 CD3DX12 平並排資源座標的新實例 \_ \_ ，並 \_ 初始化下列參數：</span><span class="sxs-lookup"><span data-stu-id="cd707-113">Creates a new instance of a CD3DX12\_TILED\_RESOURCE\_COORDINATE, initializing the following parameters:</span></span>

<span data-ttu-id="cd707-114">UINT x</span><span class="sxs-lookup"><span data-stu-id="cd707-114">UINT x</span></span>

<span data-ttu-id="cd707-115">UINT y</span><span class="sxs-lookup"><span data-stu-id="cd707-115">UINT y</span></span>

<span data-ttu-id="cd707-116">UINT z</span><span class="sxs-lookup"><span data-stu-id="cd707-116">UINT z</span></span>

<span data-ttu-id="cd707-117">UINT subresource</span><span class="sxs-lookup"><span data-stu-id="cd707-117">UINT subresource</span></span>

</dd> <dt>

<span data-ttu-id="cd707-118">**運算子 const D3D12 並排顯示 \_ \_ 資源 \_ 座標& () const**</span><span class="sxs-lookup"><span data-stu-id="cd707-118">**operator const D3D12\_TILED\_RESOURCE\_COORDINATE&() const**</span></span>
</dt> <dd>

<span data-ttu-id="cd707-119">針對父結構類型定義 & 的傳址運算子。</span><span class="sxs-lookup"><span data-stu-id="cd707-119">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cd707-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="cd707-120">Requirements</span></span>



| <span data-ttu-id="cd707-121">需求</span><span class="sxs-lookup"><span data-stu-id="cd707-121">Requirement</span></span> | <span data-ttu-id="cd707-122">值</span><span class="sxs-lookup"><span data-stu-id="cd707-122">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="cd707-123">標頭</span><span class="sxs-lookup"><span data-stu-id="cd707-123">Header</span></span><br/> | <dl> <span data-ttu-id="cd707-124"><dt>D3dx12。h</dt></span><span class="sxs-lookup"><span data-stu-id="cd707-124"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd707-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cd707-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd707-126">**D3D12 並排顯示的 \_ \_ 資源 \_ 座標**</span><span class="sxs-lookup"><span data-stu-id="cd707-126">**D3D12\_TILED\_RESOURCE\_COORDINATE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate)
</dt> <dt>

[<span data-ttu-id="cd707-127">D3D12 的 Helper 結構</span><span class="sxs-lookup"><span data-stu-id="cd707-127">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 






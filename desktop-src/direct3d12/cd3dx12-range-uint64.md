---
title: 'CD3DX12_RANGE_UINT64 結構 (D3dx12 .h) '
description: 協助程式結構，可讓您輕鬆地初始化 D3D12 \_ 範圍 \_ UINT64 結構。
ms.assetid: 789A2C46-B7D4-462E-9C10-69FD63D27491
keywords:
- CD3DX12_RANGE_UINT64 結構
topic_type:
- apiref
api_name:
- CD3DX12_RANGE_UINT64
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89c408197afb1254cae922c402939f6f169708d4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106988620"
---
# <a name="cd3dx12_range_uint64-structure"></a><span data-ttu-id="c3872-104">CD3DX12 \_ 範圍 \_ UINT64 結構</span><span class="sxs-lookup"><span data-stu-id="c3872-104">CD3DX12\_RANGE\_UINT64 structure</span></span>

<span data-ttu-id="c3872-105">協助程式結構，可讓您輕鬆地初始化 [**D3D12 \_ 範圍 \_ UINT64**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range_uint64) 結構。</span><span class="sxs-lookup"><span data-stu-id="c3872-105">A helper structure to enable easy initialization of a [**D3D12\_RANGE\_UINT64**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range_uint64) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3872-106">語法</span><span class="sxs-lookup"><span data-stu-id="c3872-106">Syntax</span></span>


```C++
struct CD3DX12_RANGE_UINT64  : public D3D12_RANGE_UINT64{
  CD3DX12_RANGE_UINT64 CD3DX12_RANGE_UINT64();
  CD3DX12_RANGE_UINT64 explicit CD3DX12_RANGE_UINT64(const D3D12_RANGE_UINT64 &o);
  CD3DX12_RANGE_UINT64 CD3DX12_RANGE_UINT64(UINT64 begin, UINT64 end);
                       operator const D3D12_RANGE_UINT64&() const;
};
```



## <a name="members"></a><span data-ttu-id="c3872-107">成員</span><span class="sxs-lookup"><span data-stu-id="c3872-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="c3872-108">**CD3DX12 \_ 範圍 \_ UINT64 ()**</span><span class="sxs-lookup"><span data-stu-id="c3872-108">**CD3DX12\_RANGE\_UINT64()**</span></span>
</dt> <dd>

<span data-ttu-id="c3872-109">建立 CD3DX12 範圍 UINT64 的新、未初始化的 \_ 實例 \_ 。</span><span class="sxs-lookup"><span data-stu-id="c3872-109">Creates a new, uninitialized, instance of a CD3DX12\_RANGE\_UINT64.</span></span>

</dd> <dt>

<span data-ttu-id="c3872-110">**明確 CD3DX12 \_ 範圍 \_ uint64 (const D3D12 \_ range \_ uint64 &o)**</span><span class="sxs-lookup"><span data-stu-id="c3872-110">**explicit CD3DX12\_RANGE\_UINT64(const D3D12\_RANGE\_UINT64 &o)**</span></span>
</dt> <dd>

<span data-ttu-id="c3872-111">建立 CD3DX12 範圍 uint64 的新實例 \_ \_ ，並以從 [**D3D12 \_ 範圍 \_ uint64**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range_uint64) 結構複製而來的值進行初始化。</span><span class="sxs-lookup"><span data-stu-id="c3872-111">Creates a new instance of a CD3DX12\_RANGE\_UINT64, initialized with values copied from a [**D3D12\_RANGE\_UINT64**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range_uint64) structure.</span></span>

</dd> <dt>

<span data-ttu-id="c3872-112">**CD3DX12 \_ 範圍 \_ UINT64 (uint64 BEGIN，uint64 end)**</span><span class="sxs-lookup"><span data-stu-id="c3872-112">**CD3DX12\_RANGE\_UINT64(UINT64 begin, UINT64 end)**</span></span>
</dt> <dd>

<span data-ttu-id="c3872-113">建立 CD3DX12 深度樣板 DESC1 的新 \_ 實例 \_ \_ ，並以參數清單中傳遞的值進行初始化。</span><span class="sxs-lookup"><span data-stu-id="c3872-113">Creates a new instance of a CD3DX12\_DEPTH\_STENCIL\_DESC1, initialized with the values passed in the parameter list.</span></span>

</dd> <dt>

<span data-ttu-id="c3872-114">**運算子 const D3D12 \_ RANGE \_ UINT64& () const**</span><span class="sxs-lookup"><span data-stu-id="c3872-114">**operator const D3D12\_RANGE\_UINT64&() const**</span></span>
</dt> <dd>

<span data-ttu-id="c3872-115">隱含轉換成 D3D12 \_ 範圍 \_ UINT64 結構。</span><span class="sxs-lookup"><span data-stu-id="c3872-115">Implicit conversion to a D3D12\_RANGE\_UINT64 structure.</span></span> <span data-ttu-id="c3872-116">因為 D3D12 \_ 範圍 \_ UINT64 是 CD3DX12 範圍 uint64 的基礎 \_ 類型 \_ ，所以物件會直接傳回為 const D3D12 \_ RANGE \_ uint64 參考本身。</span><span class="sxs-lookup"><span data-stu-id="c3872-116">Because D3D12\_RANGE\_UINT64 is the underlying type of CD3DX12\_RANGE\_UINT64, the object is simply returned as a const D3D12\_RANGE\_UINT64 reference to itself.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c3872-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="c3872-117">Requirements</span></span>



| <span data-ttu-id="c3872-118">需求</span><span class="sxs-lookup"><span data-stu-id="c3872-118">Requirement</span></span> | <span data-ttu-id="c3872-119">值</span><span class="sxs-lookup"><span data-stu-id="c3872-119">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c3872-120">標頭</span><span class="sxs-lookup"><span data-stu-id="c3872-120">Header</span></span><br/> | <dl> <span data-ttu-id="c3872-121"><dt>D3dx12。h</dt></span><span class="sxs-lookup"><span data-stu-id="c3872-121"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3872-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c3872-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3872-123">D3D12 的 Helper 結構</span><span class="sxs-lookup"><span data-stu-id="c3872-123">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="c3872-124">**D3D12 \_ 範圍 \_ UINT64**</span><span class="sxs-lookup"><span data-stu-id="c3872-124">**D3D12\_RANGE\_UINT64**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range_uint64)
</dt> </dl>

 

 






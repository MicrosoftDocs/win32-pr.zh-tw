---
title: 'CD3DX12_RECT 結構 (D3dx12 .h) '
description: 協助程式結構，可讓您輕鬆地初始化 D3D12 \_ RECT 結構。
ms.assetid: FBF01294-1448-4D9A-BA6B-27D5D59C2958
keywords:
- CD3DX12_RECT 結構
topic_type:
- apiref
api_name:
- CD3DX12_RECT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e6d8c133f14b531433ceb2239377ea85ba212af
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106976690"
---
# <a name="cd3dx12_rect-structure"></a><span data-ttu-id="6f4a2-104">CD3DX12 \_ RECT 結構</span><span class="sxs-lookup"><span data-stu-id="6f4a2-104">CD3DX12\_RECT structure</span></span>

<span data-ttu-id="6f4a2-105">協助程式結構，可讓您輕鬆地初始化 [**D3D12 \_ RECT**](d3d12-rect.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="6f4a2-105">A helper structure to enable easy initialization of a [**D3D12\_RECT**](d3d12-rect.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f4a2-106">語法</span><span class="sxs-lookup"><span data-stu-id="6f4a2-106">Syntax</span></span>


```C++
struct CD3DX12_RECT  : public D3D12_RECT{
   CD3DX12_RECT();
   explicit CD3DX12_RECT(const D3D12_RECT& o);
   explicit CD3DX12_RECT(LONG Left, LONG Top, LONG Right, LONG Bottom);
   ~CD3DX12_RECT();
   operator const D3D12_RECT&() const;
};
```



## <a name="members"></a><span data-ttu-id="6f4a2-107">成員</span><span class="sxs-lookup"><span data-stu-id="6f4a2-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="6f4a2-108">**CD3DX12 \_ RECT ()**</span><span class="sxs-lookup"><span data-stu-id="6f4a2-108">**CD3DX12\_RECT()**</span></span>
</dt> <dd>

<span data-ttu-id="6f4a2-109">建立 CD3DX12 RECT 的新、未初始化的實例 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6f4a2-109">Creates a new, uninitialized, instance of a CD3DX12\_RECT.</span></span>

</dd> <dt>

<span data-ttu-id="6f4a2-110">**明確的 CD3DX12 \_ RECT (CONST D3D12 \_ rect& o)**</span><span class="sxs-lookup"><span data-stu-id="6f4a2-110">**explicit CD3DX12\_RECT(const D3D12\_RECT& o)**</span></span>
</dt> <dd>

<span data-ttu-id="6f4a2-111">建立 CD3DX12 RECT 的新實例 \_ ，並使用另一個 [**D3D12 \_ RECT**](d3d12-rect.md) 結構的內容進行初始化。</span><span class="sxs-lookup"><span data-stu-id="6f4a2-111">Creates a new instance of a CD3DX12\_RECT, initialized with the contents of another [**D3D12\_RECT**](d3d12-rect.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="6f4a2-112">**明確的 CD3DX12 \_ 矩形 (Long 左方、Long Top、Long Right、Long 下)**</span><span class="sxs-lookup"><span data-stu-id="6f4a2-112">**explicit CD3DX12\_RECT(LONG Left, LONG Top, LONG Right, LONG Bottom)**</span></span>
</dt> <dd>

<span data-ttu-id="6f4a2-113">建立 CD3DX12 RECT 的新實例 \_ ，並初始化下列參數：</span><span class="sxs-lookup"><span data-stu-id="6f4a2-113">Creates a new instance of a CD3DX12\_RECT, initializing the following parameters:</span></span>

<span data-ttu-id="6f4a2-114">長左方</span><span class="sxs-lookup"><span data-stu-id="6f4a2-114">LONG Left</span></span>

<span data-ttu-id="6f4a2-115">長頂端</span><span class="sxs-lookup"><span data-stu-id="6f4a2-115">LONG Top</span></span>

<span data-ttu-id="6f4a2-116">長右邊</span><span class="sxs-lookup"><span data-stu-id="6f4a2-116">LONG Right</span></span>

<span data-ttu-id="6f4a2-117">長底部</span><span class="sxs-lookup"><span data-stu-id="6f4a2-117">LONG Bottom</span></span>

</dd> <dt>

<span data-ttu-id="6f4a2-118">**~ CD3DX12 \_ RECT ()**</span><span class="sxs-lookup"><span data-stu-id="6f4a2-118">**~CD3DX12\_RECT()**</span></span>
</dt> <dd>

<span data-ttu-id="6f4a2-119">終結 CD3DX12 RECT 的實例 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6f4a2-119">Destroys an instance of a CD3DX12\_RECT.</span></span>

</dd> <dt>

<span data-ttu-id="6f4a2-120">**運算子 const D3D12 \_ RECT& () const**</span><span class="sxs-lookup"><span data-stu-id="6f4a2-120">**operator const D3D12\_RECT&() const**</span></span>
</dt> <dd>

<span data-ttu-id="6f4a2-121">針對父結構類型定義 & 的傳址運算子。</span><span class="sxs-lookup"><span data-stu-id="6f4a2-121">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6f4a2-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="6f4a2-122">Requirements</span></span>



| <span data-ttu-id="6f4a2-123">需求</span><span class="sxs-lookup"><span data-stu-id="6f4a2-123">Requirement</span></span> | <span data-ttu-id="6f4a2-124">值</span><span class="sxs-lookup"><span data-stu-id="6f4a2-124">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6f4a2-125">標頭</span><span class="sxs-lookup"><span data-stu-id="6f4a2-125">Header</span></span><br/> | <dl> <span data-ttu-id="6f4a2-126"><dt>D3dx12。h</dt></span><span class="sxs-lookup"><span data-stu-id="6f4a2-126"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f4a2-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6f4a2-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f4a2-128">**D3D12 \_ RECT**</span><span class="sxs-lookup"><span data-stu-id="6f4a2-128">**D3D12\_RECT**</span></span>](d3d12-rect.md)
</dt> <dt>

[<span data-ttu-id="6f4a2-129">D3D12 的 Helper 結構</span><span class="sxs-lookup"><span data-stu-id="6f4a2-129">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 






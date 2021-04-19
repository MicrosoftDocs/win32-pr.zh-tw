---
title: 'CD3DX12_RANGE 結構 (D3dx12 .h) '
description: 協助程式結構，可讓您輕鬆地初始化 D3D12 \_ 範圍結構。
ms.assetid: 5D5192BF-D14C-487B-A214-F8428E82AF0E
keywords:
- CD3DX12_RANGE 結構
topic_type:
- apiref
api_name:
- CD3DX12_RANGE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66b6b92cd24a981d48252f5ad457f7ac0320e2d7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106999307"
---
# <a name="cd3dx12_range-structure"></a><span data-ttu-id="1d2fd-104">CD3DX12 \_ 範圍結構</span><span class="sxs-lookup"><span data-stu-id="1d2fd-104">CD3DX12\_RANGE structure</span></span>

<span data-ttu-id="1d2fd-105">協助程式結構，可讓您輕鬆地初始化 [**D3D12 \_ 範圍**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range) 結構。</span><span class="sxs-lookup"><span data-stu-id="1d2fd-105">A helper structure to enable easy initialization of a [**D3D12\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d2fd-106">語法</span><span class="sxs-lookup"><span data-stu-id="1d2fd-106">Syntax</span></span>


```C++
struct CD3DX12_RANGE  : public D3D12_RANGE{
   CD3DX12_RANGE();
   explicit CD3DX12_RANGE(const D3D12_RANGE &o);
   CD3DX12_RANGE(SIZE_T begin, SIZE_T end);
   operator const D3D12_RANGE&() const;
};
```



## <a name="members"></a><span data-ttu-id="1d2fd-107">成員</span><span class="sxs-lookup"><span data-stu-id="1d2fd-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="1d2fd-108">**CD3DX12 \_ 範圍 ()**</span><span class="sxs-lookup"><span data-stu-id="1d2fd-108">**CD3DX12\_RANGE()**</span></span>
</dt> <dd>

<span data-ttu-id="1d2fd-109">建立新的、未初始化的 CD3DX12 範圍實例 \_ 。</span><span class="sxs-lookup"><span data-stu-id="1d2fd-109">Creates a new, uninitialized, instance of a CD3DX12\_RANGE.</span></span>

</dd> <dt>

<span data-ttu-id="1d2fd-110">**明確 CD3DX12 \_ 範圍 (CONST D3D12 \_ 範圍 &o)**</span><span class="sxs-lookup"><span data-stu-id="1d2fd-110">**explicit CD3DX12\_RANGE(const D3D12\_RANGE &o)**</span></span>
</dt> <dd>

<span data-ttu-id="1d2fd-111">建立 CD3DX12 範圍的新實例 \_ ，並使用另一個 [**D3D12 \_ 範圍**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range) 結構的內容進行初始化。</span><span class="sxs-lookup"><span data-stu-id="1d2fd-111">Creates a new instance of a CD3DX12\_RANGE, initialized with the contents of another [**D3D12\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range) structure.</span></span>

</dd> <dt>

<span data-ttu-id="1d2fd-112">**CD3DX12 \_ 範圍 (大小 \_ t 開頭，大小 \_ t 結束)**</span><span class="sxs-lookup"><span data-stu-id="1d2fd-112">**CD3DX12\_RANGE(SIZE\_T begin, SIZE\_T end)**</span></span>
</dt> <dd>

<span data-ttu-id="1d2fd-113">建立 CD3DX12 範圍的新實例 \_ ，並初始化下列參數：</span><span class="sxs-lookup"><span data-stu-id="1d2fd-113">Creates a new instance of a CD3DX12\_RANGE, initializing the following parameters:</span></span>

<span data-ttu-id="1d2fd-114">大小 \_ T 開始</span><span class="sxs-lookup"><span data-stu-id="1d2fd-114">SIZE\_T begin</span></span>

<span data-ttu-id="1d2fd-115">大小 \_ T 結束</span><span class="sxs-lookup"><span data-stu-id="1d2fd-115">SIZE\_T end</span></span>

</dd> <dt>

<span data-ttu-id="1d2fd-116">**運算子 const D3D12 \_ 範圍& () const**</span><span class="sxs-lookup"><span data-stu-id="1d2fd-116">**operator const D3D12\_RANGE&() const**</span></span>
</dt> <dd>

<span data-ttu-id="1d2fd-117">針對父結構類型定義 & 的傳址運算子。</span><span class="sxs-lookup"><span data-stu-id="1d2fd-117">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1d2fd-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="1d2fd-118">Requirements</span></span>



| <span data-ttu-id="1d2fd-119">需求</span><span class="sxs-lookup"><span data-stu-id="1d2fd-119">Requirement</span></span> | <span data-ttu-id="1d2fd-120">值</span><span class="sxs-lookup"><span data-stu-id="1d2fd-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="1d2fd-121">標頭</span><span class="sxs-lookup"><span data-stu-id="1d2fd-121">Header</span></span><br/> | <dl> <span data-ttu-id="1d2fd-122"><dt>D3dx12。h</dt></span><span class="sxs-lookup"><span data-stu-id="1d2fd-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d2fd-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1d2fd-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d2fd-124">**D3D12 \_ 範圍**</span><span class="sxs-lookup"><span data-stu-id="1d2fd-124">**D3D12\_RANGE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range)
</dt> <dt>

[<span data-ttu-id="1d2fd-125">D3D12 的 Helper 結構</span><span class="sxs-lookup"><span data-stu-id="1d2fd-125">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 






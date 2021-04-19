---
title: 'CD3DX12_BOX 結構 (D3dx12 .h) '
description: 協助程式結構，可讓您輕鬆地初始化 D3D12 \_ BOX 結構。
ms.assetid: 7E1A352C-D664-4538-BA78-91493980559D
keywords:
- CD3DX12_BOX 結構
topic_type:
- apiref
api_name:
- CD3DX12_BOX
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.topic: reference
ms.localizationpriority: low
ms.date: 05/31/2018
ms.openlocfilehash: c689c9bfe611651248280f7536bd91a9f4d003d4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106982196"
---
# <a name="cd3dx12_box-structure"></a><span data-ttu-id="434c7-104">CD3DX12 \_ BOX 結構</span><span class="sxs-lookup"><span data-stu-id="434c7-104">CD3DX12\_BOX structure</span></span>

<span data-ttu-id="434c7-105">協助程式結構，可讓您輕鬆地初始化 [**D3D12 \_ BOX**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_box) 結構。</span><span class="sxs-lookup"><span data-stu-id="434c7-105">A helper structure to enable easy initialization of a [**D3D12\_BOX**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_box) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="434c7-106">語法</span><span class="sxs-lookup"><span data-stu-id="434c7-106">Syntax</span></span>


```C++
struct CD3DX12_BOX  : public D3D12_BOX{
   CD3DX12_BOX();
   explicit CD3DX12_BOX(const D3D12_BOX& o);
   explicit CD3DX12_BOX(LONG Left, LONG Right);
   explicit CD3DX12_BOX(LONG Left, LONG Top, LONG Right, LONG Bottom);
   explicit CD3DX12_BOX(LONG Left, LONG Top, LONG Front, LONG Right, LONG Bottom, LONG Back);
   ~CD3DX12_BOX();
   operator const D3D12_BOX&() const;
};
```



## <a name="members"></a><span data-ttu-id="434c7-107">成員</span><span class="sxs-lookup"><span data-stu-id="434c7-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="434c7-108">**CD3DX12 \_ BOX ()**</span><span class="sxs-lookup"><span data-stu-id="434c7-108">**CD3DX12\_BOX()**</span></span>
</dt> <dd>

<span data-ttu-id="434c7-109">建立新的、未初始化的 CD3DX12 BOX 實例 \_ 。</span><span class="sxs-lookup"><span data-stu-id="434c7-109">Creates a new, uninitialized, instance of a CD3DX12\_BOX.</span></span>

</dd> <dt>

<span data-ttu-id="434c7-110">**明確的 CD3DX12 \_ box (CONST D3D12 \_ box& o)**</span><span class="sxs-lookup"><span data-stu-id="434c7-110">**explicit CD3DX12\_BOX(const D3D12\_BOX& o)**</span></span>
</dt> <dd>

<span data-ttu-id="434c7-111">建立 CD3DX12 方塊的新實例 \_ ，並使用另一個 [**D3D12 \_ 框**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_box) 結構的內容進行初始化。</span><span class="sxs-lookup"><span data-stu-id="434c7-111">Creates a new instance of a CD3DX12\_BOX, initialized with the contents of another [**D3D12\_BOX**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_box) structure.</span></span>

</dd> <dt>

<span data-ttu-id="434c7-112">**明確的 CD3DX12 方塊 \_ (Long Left、Long Right)**</span><span class="sxs-lookup"><span data-stu-id="434c7-112">**explicit CD3DX12\_BOX(LONG Left, LONG Right)**</span></span>
</dt> <dd>

<span data-ttu-id="434c7-113">建立 CD3DX12 BOX 的新實例 \_ ，並初始化下列參數：</span><span class="sxs-lookup"><span data-stu-id="434c7-113">Creates a new instance of a CD3DX12\_BOX, initializing the following parameters:</span></span>

<span data-ttu-id="434c7-114">長左方</span><span class="sxs-lookup"><span data-stu-id="434c7-114">LONG Left</span></span>

<span data-ttu-id="434c7-115">長右邊</span><span class="sxs-lookup"><span data-stu-id="434c7-115">LONG Right</span></span>

</dd> <dt>

<span data-ttu-id="434c7-116">**明確的 CD3DX12 方塊 \_ (Long 左方、Long Top、Long Right、Long 下)**</span><span class="sxs-lookup"><span data-stu-id="434c7-116">**explicit CD3DX12\_BOX(LONG Left, LONG Top, LONG Right, LONG Bottom)**</span></span>
</dt> <dd>

<span data-ttu-id="434c7-117">建立 CD3DX12 BOX 的新實例 \_ ，並初始化下列參數：</span><span class="sxs-lookup"><span data-stu-id="434c7-117">Creates a new instance of a CD3DX12\_BOX, initializing the following parameters:</span></span>

<span data-ttu-id="434c7-118">長左方</span><span class="sxs-lookup"><span data-stu-id="434c7-118">LONG Left</span></span>

<span data-ttu-id="434c7-119">長頂端</span><span class="sxs-lookup"><span data-stu-id="434c7-119">LONG Top</span></span>

<span data-ttu-id="434c7-120">長右邊</span><span class="sxs-lookup"><span data-stu-id="434c7-120">LONG Right</span></span>

<span data-ttu-id="434c7-121">長底部</span><span class="sxs-lookup"><span data-stu-id="434c7-121">LONG Bottom</span></span>

</dd> <dt>

<span data-ttu-id="434c7-122">**明確的 CD3DX12 方塊 \_ (Long 左方、Long Top、Long Front、Right、LONG long、Long 後)**</span><span class="sxs-lookup"><span data-stu-id="434c7-122">**explicit CD3DX12\_BOX(LONG Left, LONG Top, LONG Front, LONG Right, LONG Bottom, LONG Back)**</span></span>
</dt> <dd>

<span data-ttu-id="434c7-123">建立 CD3DX12 BOX 的新實例 \_ ，並初始化下列參數：</span><span class="sxs-lookup"><span data-stu-id="434c7-123">Creates a new instance of a CD3DX12\_BOX, initializing the following parameters:</span></span>

<span data-ttu-id="434c7-124">長左方</span><span class="sxs-lookup"><span data-stu-id="434c7-124">LONG Left</span></span>

<span data-ttu-id="434c7-125">長頂端</span><span class="sxs-lookup"><span data-stu-id="434c7-125">LONG Top</span></span>

<span data-ttu-id="434c7-126">長 Front</span><span class="sxs-lookup"><span data-stu-id="434c7-126">LONG Front</span></span>

<span data-ttu-id="434c7-127">長右邊</span><span class="sxs-lookup"><span data-stu-id="434c7-127">LONG Right</span></span>

<span data-ttu-id="434c7-128">長底部</span><span class="sxs-lookup"><span data-stu-id="434c7-128">LONG Bottom</span></span>

<span data-ttu-id="434c7-129">長回來</span><span class="sxs-lookup"><span data-stu-id="434c7-129">LONG Back</span></span>

</dd> <dt>

<span data-ttu-id="434c7-130">**~ CD3DX12 \_ BOX ()**</span><span class="sxs-lookup"><span data-stu-id="434c7-130">**~CD3DX12\_BOX()**</span></span>
</dt> <dd>

<span data-ttu-id="434c7-131">終結 CD3DX12 BOX 的實例 \_ 。</span><span class="sxs-lookup"><span data-stu-id="434c7-131">Destroys an instance of a CD3DX12\_BOX.</span></span>

</dd> <dt>

<span data-ttu-id="434c7-132">**運算子 const D3D12 \_ BOX& () const**</span><span class="sxs-lookup"><span data-stu-id="434c7-132">**operator const D3D12\_BOX&() const**</span></span>
</dt> <dd>

<span data-ttu-id="434c7-133">針對父結構類型定義 & 的傳址運算子。</span><span class="sxs-lookup"><span data-stu-id="434c7-133">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="434c7-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="434c7-134">Requirements</span></span>



| <span data-ttu-id="434c7-135">需求</span><span class="sxs-lookup"><span data-stu-id="434c7-135">Requirement</span></span> | <span data-ttu-id="434c7-136">值</span><span class="sxs-lookup"><span data-stu-id="434c7-136">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="434c7-137">標頭</span><span class="sxs-lookup"><span data-stu-id="434c7-137">Header</span></span><br/> | <dl> <span data-ttu-id="434c7-138"><dt>D3dx12。h</dt></span><span class="sxs-lookup"><span data-stu-id="434c7-138"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="434c7-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="434c7-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="434c7-140">**D3D12 \_ BOX**</span><span class="sxs-lookup"><span data-stu-id="434c7-140">**D3D12\_BOX**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_box)
</dt> <dt>

[<span data-ttu-id="434c7-141">D3D12 的 Helper 結構</span><span class="sxs-lookup"><span data-stu-id="434c7-141">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 






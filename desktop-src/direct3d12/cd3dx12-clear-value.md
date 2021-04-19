---
title: 'CD3DX12_CLEAR_VALUE 結構 (D3dx12 .h) '
description: 協助程式結構，可讓您輕鬆地初始化 D3D12 的 \_ 清除 \_ 值結構。
ms.assetid: C3E2FAF4-79C4-49CA-B7D3-1FED69C8F7A7
keywords:
- CD3DX12_CLEAR_VALUE 結構
topic_type:
- apiref
api_name:
- CD3DX12_CLEAR_VALUE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b9dc7afc62c6e9a3e229e6f5bdc4287bf4b85a9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "107000571"
---
# <a name="cd3dx12_clear_value-structure"></a><span data-ttu-id="e2b50-104">CD3DX12 \_ 清除 \_ 值結構</span><span class="sxs-lookup"><span data-stu-id="e2b50-104">CD3DX12\_CLEAR\_VALUE structure</span></span>

<span data-ttu-id="e2b50-105">協助程式結構，可讓您輕鬆地初始化 [**D3D12 的 \_ 清除 \_ 值**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_clear_value) 結構。</span><span class="sxs-lookup"><span data-stu-id="e2b50-105">A helper structure to enable easy initialization of a [**D3D12\_CLEAR\_VALUE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_clear_value) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2b50-106">語法</span><span class="sxs-lookup"><span data-stu-id="e2b50-106">Syntax</span></span>


```C++
struct CD3DX12_CLEAR_VALUE  : public D3D12_CLEAR_VALUE{
   CD3DX12_CLEAR_VALUE();
   explicit CD3DX12_CLEAR_VALUE(const D3D12_CLEAR_VALUE &o);
   CD3DX12_CLEAR_VALUE(DXGI_FORMAT format, const FLOAT color[ 4 ]);
   CD3DX12_CLEAR_VALUE(DXGI_FORMAT format, FLOAT depth, UINT8 stencil);
   operator const D3D12_CLEAR_VALUE&() const;
};
```



## <a name="members"></a><span data-ttu-id="e2b50-107">成員</span><span class="sxs-lookup"><span data-stu-id="e2b50-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="e2b50-108">**CD3DX12 \_ CLEAR \_ VALUE ()**</span><span class="sxs-lookup"><span data-stu-id="e2b50-108">**CD3DX12\_CLEAR\_VALUE()**</span></span>
</dt> <dd>

<span data-ttu-id="e2b50-109">建立 CD3DX12 清除值的新、未初始化的 \_ 實例 \_ 。</span><span class="sxs-lookup"><span data-stu-id="e2b50-109">Creates a new, uninitialized, instance of a CD3DX12\_CLEAR\_VALUE.</span></span>

</dd> <dt>

<span data-ttu-id="e2b50-110">**明確的 CD3DX12 \_ clear \_ 值 (const D3D12 \_ clear \_ value &o)**</span><span class="sxs-lookup"><span data-stu-id="e2b50-110">**explicit CD3DX12\_CLEAR\_VALUE(const D3D12\_CLEAR\_VALUE &o)**</span></span>
</dt> <dd>

<span data-ttu-id="e2b50-111">建立 CD3DX12 清除值的新實例 \_ \_ ，並使用另一個 [**D3D12 \_ 清除 \_ 值**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_clear_value) 結構的內容進行初始化。</span><span class="sxs-lookup"><span data-stu-id="e2b50-111">Creates a new instance of a CD3DX12\_CLEAR\_VALUE, initialized with the contents of another [**D3D12\_CLEAR\_VALUE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_clear_value) structure.</span></span>

</dd> <dt>

<span data-ttu-id="e2b50-112">**CD3DX12 \_ CLEAR \_ VALUE (DXGI \_ 格式格式，const FLOAT color \[ 4 \])**</span><span class="sxs-lookup"><span data-stu-id="e2b50-112">**CD3DX12\_CLEAR\_VALUE(DXGI\_FORMAT format, const FLOAT color\[ 4 \])**</span></span>
</dt> <dd>

<span data-ttu-id="e2b50-113">建立 CD3DX12 清除值的新實例 \_ \_ ，並初始化下列參數：</span><span class="sxs-lookup"><span data-stu-id="e2b50-113">Creates a new instance of a CD3DX12\_CLEAR\_VALUE, initializing the following parameters:</span></span>

<span data-ttu-id="e2b50-114">[**DXGI \_格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) 格式</span><span class="sxs-lookup"><span data-stu-id="e2b50-114">[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) format</span></span>

<span data-ttu-id="e2b50-115">浮點數色彩 \[ 4 \]</span><span class="sxs-lookup"><span data-stu-id="e2b50-115">FLOAT color\[ 4 \]</span></span>

</dd> <dt>

<span data-ttu-id="e2b50-116">**CD3DX12 \_ CLEAR \_ 值 (DXGI \_ 格式格式、浮點數深度、UINT8 樣板)**</span><span class="sxs-lookup"><span data-stu-id="e2b50-116">**CD3DX12\_CLEAR\_VALUE(DXGI\_FORMAT format, FLOAT depth, UINT8 stencil)**</span></span>
</dt> <dd>

<span data-ttu-id="e2b50-117">建立 CD3DX12 清除值的新實例 \_ \_ ，並初始化下列參數：</span><span class="sxs-lookup"><span data-stu-id="e2b50-117">Creates a new instance of a CD3DX12\_CLEAR\_VALUE, initializing the following parameters:</span></span>

<span data-ttu-id="e2b50-118">[**DXGI \_格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) 格式</span><span class="sxs-lookup"><span data-stu-id="e2b50-118">[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) format</span></span>

<span data-ttu-id="e2b50-119">浮點數深度</span><span class="sxs-lookup"><span data-stu-id="e2b50-119">FLOAT depth</span></span>

<span data-ttu-id="e2b50-120">UINT8 樣板</span><span class="sxs-lookup"><span data-stu-id="e2b50-120">UINT8 stencil</span></span>

</dd> <dt>

<span data-ttu-id="e2b50-121">**運算子 const D3D12 \_ CLEAR \_ VALUE& () const**</span><span class="sxs-lookup"><span data-stu-id="e2b50-121">**operator const D3D12\_CLEAR\_VALUE&() const**</span></span>
</dt> <dd>

<span data-ttu-id="e2b50-122">針對父結構類型定義 & 的傳址運算子。</span><span class="sxs-lookup"><span data-stu-id="e2b50-122">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e2b50-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="e2b50-123">Requirements</span></span>



| <span data-ttu-id="e2b50-124">需求</span><span class="sxs-lookup"><span data-stu-id="e2b50-124">Requirement</span></span> | <span data-ttu-id="e2b50-125">值</span><span class="sxs-lookup"><span data-stu-id="e2b50-125">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e2b50-126">標頭</span><span class="sxs-lookup"><span data-stu-id="e2b50-126">Header</span></span><br/> | <dl> <span data-ttu-id="e2b50-127"><dt>D3dx12。h</dt></span><span class="sxs-lookup"><span data-stu-id="e2b50-127"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2b50-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e2b50-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2b50-129">**D3D12 \_ CLEAR \_ 值**</span><span class="sxs-lookup"><span data-stu-id="e2b50-129">**D3D12\_CLEAR\_VALUE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_clear_value)
</dt> <dt>

[<span data-ttu-id="e2b50-130">D3D12 的 Helper 結構</span><span class="sxs-lookup"><span data-stu-id="e2b50-130">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 


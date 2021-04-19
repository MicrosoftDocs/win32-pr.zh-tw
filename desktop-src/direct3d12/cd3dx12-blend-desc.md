---
title: 'CD3DX12_BLEND_DESC 結構 (D3dx12 .h) '
description: 協助程式結構，可讓您輕鬆地初始化 D3D12 \_ BLEND \_ DESC 結構。
ms.assetid: D37BB62E-904B-4953-9119-21F3B37570C0
keywords:
- CD3DX12_BLEND_DESC 結構
topic_type:
- apiref
api_name:
- CD3DX12_BLEND_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddb88ce003f74251c3ce34a2ca47ae2fb55f892d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106976463"
---
# <a name="cd3dx12_blend_desc-structure"></a><span data-ttu-id="d7071-104">CD3DX12 \_ BLEND \_ DESC 結構</span><span class="sxs-lookup"><span data-stu-id="d7071-104">CD3DX12\_BLEND\_DESC structure</span></span>

<span data-ttu-id="d7071-105">協助程式結構，可讓您輕鬆地初始化 [**D3D12 \_ BLEND \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc) 結構。</span><span class="sxs-lookup"><span data-stu-id="d7071-105">A helper structure to enable easy initialization of a [**D3D12\_BLEND\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7071-106">語法</span><span class="sxs-lookup"><span data-stu-id="d7071-106">Syntax</span></span>


```C++
struct CD3DX12_BLEND_DESC  : public D3D12_BLEND_DESC{
   CD3DX12_BLEND_DESC();
   explicit CD3DX12_BLEND_DESC(const D3D12_BLEND_DESC& o);
   explicit CD3DX12_BLEND_DESC(CD3DX12_DEFAULT);
   ~CD3DX12_BLEND_DESC();
   operator const D3D12_BLEND_DESC&() const;
};
```



## <a name="members"></a><span data-ttu-id="d7071-107">成員</span><span class="sxs-lookup"><span data-stu-id="d7071-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="d7071-108">**CD3DX12 \_ BLEND \_ DESC ()**</span><span class="sxs-lookup"><span data-stu-id="d7071-108">**CD3DX12\_BLEND\_DESC()**</span></span>
</dt> <dd>

<span data-ttu-id="d7071-109">建立新的、未初始化的 CD3DX12 \_ BLEND DESC 實例 \_ 。</span><span class="sxs-lookup"><span data-stu-id="d7071-109">Creates a new, uninitialized, instance of a CD3DX12\_BLEND\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="d7071-110">**明確 CD3DX12 \_ blend \_ desc (const D3D12 \_ blend \_ desc& o)**</span><span class="sxs-lookup"><span data-stu-id="d7071-110">**explicit CD3DX12\_BLEND\_DESC(const D3D12\_BLEND\_DESC& o)**</span></span>
</dt> <dd>

<span data-ttu-id="d7071-111">建立 CD3DX12 BLEND desc 的新實例 \_ \_ ，並使用另一個 [**D3D12 \_ BLEND \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc) 結構的內容進行初始化。</span><span class="sxs-lookup"><span data-stu-id="d7071-111">Creates a new instance of a CD3DX12\_BLEND\_DESC, initialized with the contents of another [**D3D12\_BLEND\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc) structure.</span></span>

</dd> <dt>

<span data-ttu-id="d7071-112">**明確的 CD3DX12 \_ BLEND \_ DESC (CD3DX12 \_ 預設)**</span><span class="sxs-lookup"><span data-stu-id="d7071-112">**explicit CD3DX12\_BLEND\_DESC(CD3DX12\_DEFAULT)**</span></span>
</dt> <dd>

<span data-ttu-id="d7071-113">建立 CD3DX12 BLEND DESC 的新實例 \_ \_ ，並以預設參數初始化。</span><span class="sxs-lookup"><span data-stu-id="d7071-113">Creates a new instance of a CD3DX12\_BLEND\_DESC, initialized with default parameters.</span></span>



| <span data-ttu-id="d7071-114">狀態</span><span class="sxs-lookup"><span data-stu-id="d7071-114">State</span></span>                                   | <span data-ttu-id="d7071-115">預設值</span><span class="sxs-lookup"><span data-stu-id="d7071-115">Default Value</span></span>                    |
|-----------------------------------------|----------------------------------|
| <span data-ttu-id="d7071-116">AlphaToCoverageEnable</span><span class="sxs-lookup"><span data-stu-id="d7071-116">AlphaToCoverageEnable</span></span>                   | <span data-ttu-id="d7071-117">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="d7071-117">**FALSE**</span></span>                        |
| <span data-ttu-id="d7071-118">IndependentBlendEnable</span><span class="sxs-lookup"><span data-stu-id="d7071-118">IndependentBlendEnable</span></span>                  | <span data-ttu-id="d7071-119">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="d7071-119">**FALSE**</span></span>                        |
| <span data-ttu-id="d7071-120">RenderTarget \[ 0 \] 。BlendEnable</span><span class="sxs-lookup"><span data-stu-id="d7071-120">RenderTarget\[0\].BlendEnable</span></span>           | <span data-ttu-id="d7071-121">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="d7071-121">**FALSE**</span></span>                        |
| <span data-ttu-id="d7071-122">RenderTarget \[ 0 \] 。LogicOpEnable</span><span class="sxs-lookup"><span data-stu-id="d7071-122">RenderTarget\[0\].LogicOpEnable</span></span>         | <span data-ttu-id="d7071-123">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="d7071-123">**FALSE**</span></span>                        |
| <span data-ttu-id="d7071-124">RenderTarget \[ 0 \] 。SrcBlend</span><span class="sxs-lookup"><span data-stu-id="d7071-124">RenderTarget\[0\].SrcBlend</span></span>              | <span data-ttu-id="d7071-125">D3D12 \_ BLEND \_ 1</span><span class="sxs-lookup"><span data-stu-id="d7071-125">D3D12\_BLEND\_ONE</span></span>                |
| <span data-ttu-id="d7071-126">RenderTarget \[ 0 \] 。DestBlend</span><span class="sxs-lookup"><span data-stu-id="d7071-126">RenderTarget\[0\].DestBlend</span></span>             | <span data-ttu-id="d7071-127">D3D12 \_ BLEND \_ 零</span><span class="sxs-lookup"><span data-stu-id="d7071-127">D3D12\_BLEND\_ZERO</span></span>               |
| <span data-ttu-id="d7071-128">RenderTarget \[ 0 \] 。BlendOp</span><span class="sxs-lookup"><span data-stu-id="d7071-128">RenderTarget\[0\].BlendOp</span></span>               | <span data-ttu-id="d7071-129">D3D12 \_ BLEND \_ OP \_ 新增</span><span class="sxs-lookup"><span data-stu-id="d7071-129">D3D12\_BLEND\_OP\_ADD</span></span>            |
| <span data-ttu-id="d7071-130">RenderTarget \[ 0 \] 。SrcBlendAlpha</span><span class="sxs-lookup"><span data-stu-id="d7071-130">RenderTarget\[0\].SrcBlendAlpha</span></span>         | <span data-ttu-id="d7071-131">D3D12 \_ BLEND \_ 1</span><span class="sxs-lookup"><span data-stu-id="d7071-131">D3D12\_BLEND\_ONE</span></span>                |
| <span data-ttu-id="d7071-132">RenderTarget \[ 0 \] 。DestBlendAlpha</span><span class="sxs-lookup"><span data-stu-id="d7071-132">RenderTarget\[0\].DestBlendAlpha</span></span>        | <span data-ttu-id="d7071-133">D3D12 \_ BLEND \_ 零</span><span class="sxs-lookup"><span data-stu-id="d7071-133">D3D12\_BLEND\_ZERO</span></span>               |
| <span data-ttu-id="d7071-134">RenderTarget \[ 0 \] 。BlendOpAlpha</span><span class="sxs-lookup"><span data-stu-id="d7071-134">RenderTarget\[0\].BlendOpAlpha</span></span>          | <span data-ttu-id="d7071-135">D3D12 \_ BLEND \_ OP \_ 新增</span><span class="sxs-lookup"><span data-stu-id="d7071-135">D3D12\_BLEND\_OP\_ADD</span></span>            |
| <span data-ttu-id="d7071-136">RenderTarget \[ 0 \] 。LogicOp</span><span class="sxs-lookup"><span data-stu-id="d7071-136">RenderTarget\[0\].LogicOp</span></span>               | <span data-ttu-id="d7071-137">D3D12 \_ 邏輯 \_ OP \_ NOOP</span><span class="sxs-lookup"><span data-stu-id="d7071-137">D3D12\_LOGIC\_OP\_NOOP</span></span>           |
| <span data-ttu-id="d7071-138">RenderTarget \[ 0 \] 。RenderTargetWriteMask</span><span class="sxs-lookup"><span data-stu-id="d7071-138">RenderTarget\[0\].RenderTargetWriteMask</span></span> | <span data-ttu-id="d7071-139">D3D12 \_ 色彩 \_ 寫入 \_ \_ 全部啟用</span><span class="sxs-lookup"><span data-stu-id="d7071-139">D3D12\_COLOR\_WRITE\_ENABLE\_ALL</span></span> |



 

</dd> <dt>

<span data-ttu-id="d7071-140">**~ CD3DX12 \_ BLEND \_ DESC ()**</span><span class="sxs-lookup"><span data-stu-id="d7071-140">**~CD3DX12\_BLEND\_DESC()**</span></span>
</dt> <dd>

<span data-ttu-id="d7071-141">終結 CD3DX12 BLEND DESC 的實例 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="d7071-141">Destroys an instance of a CD3DX12\_BLEND\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="d7071-142">**運算子 const D3D12 \_ BLEND \_ DESC& () const**</span><span class="sxs-lookup"><span data-stu-id="d7071-142">**operator const D3D12\_BLEND\_DESC&() const**</span></span>
</dt> <dd>

<span data-ttu-id="d7071-143">針對父結構類型定義 & 的傳址運算子。</span><span class="sxs-lookup"><span data-stu-id="d7071-143">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d7071-144">規格需求</span><span class="sxs-lookup"><span data-stu-id="d7071-144">Requirements</span></span>



| <span data-ttu-id="d7071-145">需求</span><span class="sxs-lookup"><span data-stu-id="d7071-145">Requirement</span></span> | <span data-ttu-id="d7071-146">值</span><span class="sxs-lookup"><span data-stu-id="d7071-146">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d7071-147">標頭</span><span class="sxs-lookup"><span data-stu-id="d7071-147">Header</span></span><br/> | <dl> <span data-ttu-id="d7071-148"><dt>D3dx12。h</dt></span><span class="sxs-lookup"><span data-stu-id="d7071-148"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7071-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d7071-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7071-150">**D3D12 \_ BLEND \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="d7071-150">**D3D12\_BLEND\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc)
</dt> <dt>

[<span data-ttu-id="d7071-151">D3D12 的 Helper 結構</span><span class="sxs-lookup"><span data-stu-id="d7071-151">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 






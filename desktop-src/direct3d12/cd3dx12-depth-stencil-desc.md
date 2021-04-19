---
title: 'CD3DX12_DEPTH_STENCIL_DESC 結構 (D3dx12 .h) '
description: 協助程式結構，可讓您輕鬆地初始化 D3D12 \_ 深度樣板 \_ \_ DESC 結構。
ms.assetid: D3DB04C3-4564-45A4-830A-E63B8D308B33
keywords:
- CD3DX12_DEPTH_STENCIL_DESC 結構
topic_type:
- apiref
api_name:
- CD3DX12_DEPTH_STENCIL_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f36a071251a12c4d27d06586775c01759b88d38
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106975654"
---
# <a name="cd3dx12_depth_stencil_desc-structure"></a><span data-ttu-id="6d1e0-104">CD3DX12 \_ 深度 \_ 樣板 \_ DESC 結構</span><span class="sxs-lookup"><span data-stu-id="6d1e0-104">CD3DX12\_DEPTH\_STENCIL\_DESC structure</span></span>

<span data-ttu-id="6d1e0-105">協助程式結構，可讓您輕鬆地初始化 [**D3D12 \_ 深度樣板 \_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc) 結構。</span><span class="sxs-lookup"><span data-stu-id="6d1e0-105">A helper structure to enable easy initialization of a [**D3D12\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d1e0-106">語法</span><span class="sxs-lookup"><span data-stu-id="6d1e0-106">Syntax</span></span>


```C++
struct CD3DX12_DEPTH_STENCIL_DESC  : public D3D12_DEPTH_STENCIL_DESC{
   CD3DX12_DEPTH_STENCIL_DESC();
   explicit CD3DX12_DEPTH_STENCIL_DESC(const D3D12_DEPTH_STENCIL_DESC& o);
   explicit CD3DX12_DEPTH_STENCIL_DESC(CD3DX12_DEFAULT);
   explicit CD3DX12_DEPTH_STENCIL_DESC(BOOL depthEnable, D3D12_DEPTH_WRITE_MASK depthWriteMask, D3D12_COMPARISON_FUNC depthFunc, BOOL stencilEnable, UINT8 stencilReadMask, UINT8 stencilWriteMask, D3D12_STENCIL_OP frontStencilFailOp, D3D12_STENCIL_OP frontStencilDepthFailOp, D3D12_STENCIL_OP frontStencilPassOp, D3D12_COMPARISON_FUNC frontStencilFunc, D3D12_STENCIL_OP backStencilFailOp, D3D12_STENCIL_OP backStencilDepthFailOp, D3D12_STENCIL_OP backStencilPassOp, D3D12_COMPARISON_FUNC backStencilFunc);
   ~CD3DX12_DEPTH_STENCIL_DESC();
   operator const D3D12_DEPTH_STENCIL_DESC&() const;
};
```



## <a name="members"></a><span data-ttu-id="6d1e0-107">成員</span><span class="sxs-lookup"><span data-stu-id="6d1e0-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="6d1e0-108">**CD3DX12 \_ 深度 \_ 樣板 \_ DESC ()**</span><span class="sxs-lookup"><span data-stu-id="6d1e0-108">**CD3DX12\_DEPTH\_STENCIL\_DESC()**</span></span>
</dt> <dd>

<span data-ttu-id="6d1e0-109">建立 D3DX12 深度樣板 DESC 的新、未初始化的實例 \_ \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="6d1e0-109">Creates a new, uninitialized, instance of a D3DX12\_DEPTH\_STENCIL\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="6d1e0-110">**明確 CD3DX12 \_ 深度 \_ 樣板 \_ DESC (const D3D12 \_ depth \_ 樣板 \_ desc& o)**</span><span class="sxs-lookup"><span data-stu-id="6d1e0-110">**explicit CD3DX12\_DEPTH\_STENCIL\_DESC(const D3D12\_DEPTH\_STENCIL\_DESC& o)**</span></span>
</dt> <dd>

<span data-ttu-id="6d1e0-111">建立 D3DX12 深度樣板 desc 的新 \_ 實例 \_ \_ ，並以另一個 [**D3D12 \_ 深度樣板 \_ \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc) 結構的內容進行初始化。</span><span class="sxs-lookup"><span data-stu-id="6d1e0-111">Creates a new instance of a D3DX12\_DEPTH\_STENCIL\_DESC, initialized with the contents of another [**D3D12\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc) structure.</span></span>

</dd> <dt>

<span data-ttu-id="6d1e0-112">**明確 CD3DX12 \_ 深度 \_ 樣板 \_ DESC (CD3DX12 \_ 預設)**</span><span class="sxs-lookup"><span data-stu-id="6d1e0-112">**explicit CD3DX12\_DEPTH\_STENCIL\_DESC(CD3DX12\_DEFAULT)**</span></span>
</dt> <dd>

<span data-ttu-id="6d1e0-113">建立 D3DX12 深度樣板 DESC 的新 \_ 實例 \_ \_ ，並以預設參數初始化。</span><span class="sxs-lookup"><span data-stu-id="6d1e0-113">Creates a new instance of a D3DX12\_DEPTH\_STENCIL\_DESC, initialized with default parameters.</span></span>

``` syntax
        DepthEnable = TRUE;  
        DepthWriteMask = D3D12_DEPTH_WRITE_MASK_ALL;  
        DepthFunc = D3D12_COMPARISON_FUNC_LESS;  
        StencilEnable = FALSE;  
        StencilReadMask = D3D12_DEFAULT_STENCIL_READ_MASK;  
        StencilWriteMask = D3D12_DEFAULT_STENCIL_WRITE_MASK;  
        const D3D12_DEPTH_STENCILOP_DESC defaultStencilOp =  
        { D3D12_STENCIL_OP_KEEP, D3D12_STENCIL_OP_KEEP, D3D12_STENCIL_OP_KEEP, D3D12_COMPARISON_FUNC_ALWAYS };  
        FrontFace = defaultStencilOp;  
        BackFace = defaultStencilOp;  
```

</dd> <dt>

<span data-ttu-id="6d1e0-114">**明確的 CD3DX12 \_ 深度樣板 \_ \_ DESC (BOOL depthEnable、D3D12 \_ DEPTH \_ WRITE \_ MASK depthWriteMask、D3D12 \_ 比較 \_ FUNC DEPTHFUNC、BOOL STENCILENABLE、UINT8 StencilReadMask、UINT8 stencilWriteMask、D3D12 樣板 op frontStencilFailOp、 \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ D3D12 樣板 op frontStencilDepthFailOp、D3D12 樣板 op frontStencilPassOp、D3D12 比較 func frontStencilFunc、D3D12 樣板 op backStencilFailOp、D3D12 樣板 op backStencilDepthFailOp、D3D12 樣板 op backStencilPassOp、D3D12 比較 func backStencilFunc)**</span><span class="sxs-lookup"><span data-stu-id="6d1e0-114">**explicit CD3DX12\_DEPTH\_STENCIL\_DESC(BOOL depthEnable, D3D12\_DEPTH\_WRITE\_MASK depthWriteMask, D3D12\_COMPARISON\_FUNC depthFunc, BOOL stencilEnable, UINT8 stencilReadMask, UINT8 stencilWriteMask, D3D12\_STENCIL\_OP frontStencilFailOp, D3D12\_STENCIL\_OP frontStencilDepthFailOp, D3D12\_STENCIL\_OP frontStencilPassOp, D3D12\_COMPARISON\_FUNC frontStencilFunc, D3D12\_STENCIL\_OP backStencilFailOp, D3D12\_STENCIL\_OP backStencilDepthFailOp, D3D12\_STENCIL\_OP backStencilPassOp, D3D12\_COMPARISON\_FUNC backStencilFunc)**</span></span>
</dt> <dd>

<span data-ttu-id="6d1e0-115">建立 D3DX12 深度樣板 DESC 的新 \_ 實例 \_ \_ ，並初始化下列參數：</span><span class="sxs-lookup"><span data-stu-id="6d1e0-115">Creates a new instance of a D3DX12\_DEPTH\_STENCIL\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="6d1e0-116">BOOL depthEnable</span><span class="sxs-lookup"><span data-stu-id="6d1e0-116">BOOL depthEnable</span></span>

<span data-ttu-id="6d1e0-117">[**D3D12 \_深度 \_ 寫入 \_ 遮罩**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_depth_write_mask) depthWriteMask</span><span class="sxs-lookup"><span data-stu-id="6d1e0-117">[**D3D12\_DEPTH\_WRITE\_MASK**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_depth_write_mask) depthWriteMask</span></span>

<span data-ttu-id="6d1e0-118">[**D3D12 \_比較 \_ FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) depthFunc</span><span class="sxs-lookup"><span data-stu-id="6d1e0-118">[**D3D12\_COMPARISON\_FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) depthFunc</span></span>

<span data-ttu-id="6d1e0-119">BOOL stencilEnable</span><span class="sxs-lookup"><span data-stu-id="6d1e0-119">BOOL stencilEnable</span></span>

<span data-ttu-id="6d1e0-120">UINT8 stencilReadMask</span><span class="sxs-lookup"><span data-stu-id="6d1e0-120">UINT8 stencilReadMask</span></span>

<span data-ttu-id="6d1e0-121">UINT8 stencilWriteMask</span><span class="sxs-lookup"><span data-stu-id="6d1e0-121">UINT8 stencilWriteMask</span></span>

<span data-ttu-id="6d1e0-122">[**D3D12 \_樣板 \_ OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) frontStencilFailOp</span><span class="sxs-lookup"><span data-stu-id="6d1e0-122">[**D3D12\_STENCIL\_OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) frontStencilFailOp</span></span>

<span data-ttu-id="6d1e0-123">[**D3D12 \_樣板 \_ OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) frontStencilDepthFailOp</span><span class="sxs-lookup"><span data-stu-id="6d1e0-123">[**D3D12\_STENCIL\_OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) frontStencilDepthFailOp</span></span>

<span data-ttu-id="6d1e0-124">[**D3D12 \_樣板 \_ OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) frontStencilPassOp</span><span class="sxs-lookup"><span data-stu-id="6d1e0-124">[**D3D12\_STENCIL\_OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) frontStencilPassOp</span></span>

<span data-ttu-id="6d1e0-125">[**D3D12 \_比較 \_ FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) frontStencilFunc</span><span class="sxs-lookup"><span data-stu-id="6d1e0-125">[**D3D12\_COMPARISON\_FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) frontStencilFunc</span></span>

<span data-ttu-id="6d1e0-126">[**D3D12 \_樣板 \_ OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) backStencilFailOp</span><span class="sxs-lookup"><span data-stu-id="6d1e0-126">[**D3D12\_STENCIL\_OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) backStencilFailOp</span></span>

<span data-ttu-id="6d1e0-127">[**D3D12 \_樣板 \_ OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) backStencilDepthFailOp</span><span class="sxs-lookup"><span data-stu-id="6d1e0-127">[**D3D12\_STENCIL\_OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) backStencilDepthFailOp</span></span>

<span data-ttu-id="6d1e0-128">[**D3D12 \_樣板 \_ OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) backStencilPassOp</span><span class="sxs-lookup"><span data-stu-id="6d1e0-128">[**D3D12\_STENCIL\_OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) backStencilPassOp</span></span>

<span data-ttu-id="6d1e0-129">[**D3D12 \_比較 \_ FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) backStencilFunc</span><span class="sxs-lookup"><span data-stu-id="6d1e0-129">[**D3D12\_COMPARISON\_FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) backStencilFunc</span></span>

</dd> <dt>

<span data-ttu-id="6d1e0-130">**~ CD3DX12 \_ 深度 \_ 樣板 \_ DESC ()**</span><span class="sxs-lookup"><span data-stu-id="6d1e0-130">**~CD3DX12\_DEPTH\_STENCIL\_DESC()**</span></span>
</dt> <dd>

<span data-ttu-id="6d1e0-131">終結 CD3DX12 深度樣板 DESC 的 \_ 實例 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="6d1e0-131">Destroys an instance of a CD3DX12\_DEPTH\_STENCIL\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="6d1e0-132">**運算子 const D3D12 \_ 深度 \_ 樣板 \_ DESC& () const**</span><span class="sxs-lookup"><span data-stu-id="6d1e0-132">**operator const D3D12\_DEPTH\_STENCIL\_DESC&() const**</span></span>
</dt> <dd>

<span data-ttu-id="6d1e0-133">針對父結構類型定義 & 的傳址運算子。</span><span class="sxs-lookup"><span data-stu-id="6d1e0-133">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6d1e0-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="6d1e0-134">Requirements</span></span>



| <span data-ttu-id="6d1e0-135">需求</span><span class="sxs-lookup"><span data-stu-id="6d1e0-135">Requirement</span></span> | <span data-ttu-id="6d1e0-136">值</span><span class="sxs-lookup"><span data-stu-id="6d1e0-136">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6d1e0-137">標頭</span><span class="sxs-lookup"><span data-stu-id="6d1e0-137">Header</span></span><br/> | <dl> <span data-ttu-id="6d1e0-138"><dt>D3dx12。h</dt></span><span class="sxs-lookup"><span data-stu-id="6d1e0-138"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d1e0-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6d1e0-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d1e0-140">**D3D12 \_ 深度 \_ 樣板 \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="6d1e0-140">**D3D12\_DEPTH\_STENCIL\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc)
</dt> <dt>

[<span data-ttu-id="6d1e0-141">D3D12 的 Helper 結構</span><span class="sxs-lookup"><span data-stu-id="6d1e0-141">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 






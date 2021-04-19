---
title: 'CD3DX12_DEPTH_STENCIL_DESC1 結構 (D3dx12 .h) '
description: 協助程式結構，可讓您輕鬆地初始化 D3D12 \_ 深度樣板 \_ \_ DESC1 結構。
ms.assetid: 8EB008F9-212D-486E-9C62-D7BA9D3C6807
keywords:
- CD3DX12_DEPTH_STENCIL_DESC1 結構
topic_type:
- apiref
api_name:
- CD3DX12_DEPTH_STENCIL_DESC1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 976c05ec4f3ca85ccfcebb6a13dbe408ba05c64e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106982195"
---
# <a name="cd3dx12_depth_stencil_desc1-structure"></a><span data-ttu-id="07d8a-104">CD3DX12 \_ 深度 \_ 樣板 \_ DESC1 結構</span><span class="sxs-lookup"><span data-stu-id="07d8a-104">CD3DX12\_DEPTH\_STENCIL\_DESC1 structure</span></span>

<span data-ttu-id="07d8a-105">協助程式結構，可讓您輕鬆地初始化 [**D3D12 \_ 深度樣板 \_ \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1) 結構。</span><span class="sxs-lookup"><span data-stu-id="07d8a-105">A helper structure to enable easy initialization of a [**D3D12\_DEPTH\_STENCIL\_DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="07d8a-106">語法</span><span class="sxs-lookup"><span data-stu-id="07d8a-106">Syntax</span></span>


```C++
struct CD3DX12_DEPTH_STENCIL_DESC1  : public D3D12_DEPTH_STENCIL_DESC1{
  CD3DX12_DEPTH_STENCIL_DESC1 CD3DX12_DEPTH_STENCIL_DESC1();
  CD3DX12_DEPTH_STENCIL_DESC1 explicit CD3DX12_DEPTH_STENCIL_DESC1(const D3D12_DEPTH_STENCIL_DESC1& o);
  CD3DX12_DEPTH_STENCIL_DESC1 explicit CD3DX12_DEPTH_STENCIL_DESC1(const D3D12_DEPTH_STENCIL_DESC& o);
  CD3DX12_DEPTH_STENCIL_DESC1 explicit CD3DX12_DEPTH_STENCIL_DESC1(CD3DX12_DEFAULT);
  CD3DX12_DEPTH_STENCIL_DESC1 explicit CD3DX12_DEPTH_STENCIL_DESC1(BOOL depthEnable, D3D12_DEPTH_WRITE_MASK depthWriteMask, D3D12_COMPARISON_FUNC depthFunc, BOOL stencilEnable, UINT8 stencilReadMask, UINT8 stencilWriteMask, D3D12_STENCIL_OP frontStencilFailOp, D3D12_STENCIL_OP frontStencilDepthFailOp, D3D12_STENCIL_OP frontStencilPassOp, D3D12_COMPARISON_FUNC frontStencilFunc, D3D12_STENCIL_OP backStencilFailOp, D3D12_STENCIL_OP backStencilDepthFailOp, D3D12_STENCIL_OP backStencilPassOp, D3D12_COMPARISON_FUNC backStencilFunc, BOOL depthBoundsTestEnable);
                              ~CD3DX12_DEPTH_STENCIL_DESC1();
                              operator const D3D12_DEPTH_STENCIL_DESC1&() const;
                              operator const D3D12_DEPTH_STENCIL_DESC() const;
};
```



## <a name="members"></a><span data-ttu-id="07d8a-107">成員</span><span class="sxs-lookup"><span data-stu-id="07d8a-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="07d8a-108">**CD3DX12 \_ 深度 \_ 樣板 \_ DESC1 ()**</span><span class="sxs-lookup"><span data-stu-id="07d8a-108">**CD3DX12\_DEPTH\_STENCIL\_DESC1()**</span></span>
</dt> <dd>

<span data-ttu-id="07d8a-109">建立新的、未初始化的 CD3DX12 深度樣板 \_ \_ DESC1 實例 \_ 。</span><span class="sxs-lookup"><span data-stu-id="07d8a-109">Creates a new, uninitialized, instance of a CD3DX12\_DEPTH\_STENCIL\_DESC1.</span></span>

</dd> <dt>

<span data-ttu-id="07d8a-110">**明確的 CD3DX12 \_ 深度樣板 \_ \_ DESC1 (const D3D12 \_ DEPTH 樣板 \_ \_ DESC1& o)**</span><span class="sxs-lookup"><span data-stu-id="07d8a-110">**explicit CD3DX12\_DEPTH\_STENCIL\_DESC1(const D3D12\_DEPTH\_STENCIL\_DESC1& o)**</span></span>
</dt> <dd>

<span data-ttu-id="07d8a-111">建立 CD3DX12 深度樣板 DESC1 的新 \_ 實例 \_ \_ ，並以從 [**D3D12 \_ 深度樣板 \_ \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1) 結構複製而來的值進行初始化。</span><span class="sxs-lookup"><span data-stu-id="07d8a-111">Creates a new instance of a CD3DX12\_DEPTH\_STENCIL\_DESC1, initialized with values copied from a [**D3D12\_DEPTH\_STENCIL\_DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1) structure.</span></span>

</dd> <dt>

<span data-ttu-id="07d8a-112">**明確的 CD3DX12 \_ 深度樣板 \_ \_ DESC1 (const D3D12 \_ 深度樣板 \_ \_ DESC& o)**</span><span class="sxs-lookup"><span data-stu-id="07d8a-112">**explicit CD3DX12\_DEPTH\_STENCIL\_DESC1(const D3D12\_DEPTH\_STENCIL\_DESC& o)**</span></span>
</dt> <dd>

<span data-ttu-id="07d8a-113">建立 CD3DX12 深度樣板 DESC1 的新 \_ 實例 \_ \_ ，並以從 [**D3D12 \_ 深度樣板 \_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc) 結構複製而來的值進行初始化</span><span class="sxs-lookup"><span data-stu-id="07d8a-113">Creates a new instance of a CD3DX12\_DEPTH\_STENCIL\_DESC1, initialized with values copied from a [**D3D12\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc) structure</span></span>

<span data-ttu-id="07d8a-114">以及將其他 **DepthBoundsTestEnable** 成員設為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="07d8a-114">and the additional **DepthBoundsTestEnable** member set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="07d8a-115">**明確的 CD3DX12 \_ 深度樣板 \_ \_ DESC1 (CD3DX12 \_ 預設)**</span><span class="sxs-lookup"><span data-stu-id="07d8a-115">**explicit CD3DX12\_DEPTH\_STENCIL\_DESC1(CD3DX12\_DEFAULT)**</span></span>
</dt> <dd>

<span data-ttu-id="07d8a-116">建立 CD3DX12 深度樣板 DESC1 的新 \_ 實例 \_ \_ ，並使用 D3DX12 所指定的預設狀態進行初始化：</span><span class="sxs-lookup"><span data-stu-id="07d8a-116">Creates a new instance of a CD3DX12\_DEPTH\_STENCIL\_DESC1, initialized with the default state prescribed by D3DX12:</span></span>

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
    DepthBoundsTestEnable = FALSE;
          
```

</dd> <dt>

<span data-ttu-id="07d8a-117">**明確的 CD3DX12 \_ 深度樣板 \_ \_ DESC1 (BOOL depthEnable、D3D12 \_ DEPTH \_ WRITE \_ MASK depthWriteMask、D3D12 \_ 比較 \_ FUNC DEPTHFUNC、BOOL STENCILENABLE、UINT8 StencilReadMask、UINT8 stencilWriteMask、D3D12 樣板 op frontStencilFailOp、 \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ D3D12 樣板 op frontStencilDepthFailOp、D3D12 樣板 op frontStencilPassOp、D3D12 比較 Func frontStencilFunc、D3D12 樣板 op backStencilFailOp、D3D12 comparison op backStencilDepthFailOp、D3D12 樣板 op backStencilPassOp、D3D12 比較 func backStencilFunc、BOOL depthBoundsTestEnable)**</span><span class="sxs-lookup"><span data-stu-id="07d8a-117">**explicit CD3DX12\_DEPTH\_STENCIL\_DESC1(BOOL depthEnable, D3D12\_DEPTH\_WRITE\_MASK depthWriteMask, D3D12\_COMPARISON\_FUNC depthFunc, BOOL stencilEnable, UINT8 stencilReadMask, UINT8 stencilWriteMask, D3D12\_STENCIL\_OP frontStencilFailOp, D3D12\_STENCIL\_OP frontStencilDepthFailOp, D3D12\_STENCIL\_OP frontStencilPassOp, D3D12\_COMPARISON\_FUNC frontStencilFunc, D3D12\_STENCIL\_OP backStencilFailOp, D3D12\_STENCIL\_OP backStencilDepthFailOp, D3D12\_STENCIL\_OP backStencilPassOp, D3D12\_COMPARISON\_FUNC backStencilFunc, BOOL depthBoundsTestEnable)**</span></span>
</dt> <dd>

<span data-ttu-id="07d8a-118">建立 CD3DX12 深度樣板 DESC1 的新 \_ 實例 \_ \_ ，並以參數清單中傳遞的值進行初始化。</span><span class="sxs-lookup"><span data-stu-id="07d8a-118">Creates a new instance of a CD3DX12\_DEPTH\_STENCIL\_DESC1, initialized with the values passed in the parameter list.</span></span>

</dd> <dt>

<span data-ttu-id="07d8a-119">**~ CD3DX12 \_ 深度 \_ 樣板 \_ DESC1 ()**</span><span class="sxs-lookup"><span data-stu-id="07d8a-119">**~CD3DX12\_DEPTH\_STENCIL\_DESC1()**</span></span>
</dt> <dd>

<span data-ttu-id="07d8a-120">終結 D3DX12 深度樣板 DESC1 的 \_ 實例 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="07d8a-120">Destroys an instance of a D3DX12\_DEPTH\_STENCIL\_DESC1.</span></span>

</dd> <dt>

<span data-ttu-id="07d8a-121">**運算子 const D3D12 \_ DEPTH \_ 樣板 \_ DESC1& () const**</span><span class="sxs-lookup"><span data-stu-id="07d8a-121">**operator const D3D12\_DEPTH\_STENCIL\_DESC1&() const**</span></span>
</dt> <dd>

<span data-ttu-id="07d8a-122">隱含轉換成 D3D12 \_ 深度樣板 \_ \_ DESC1 結構。</span><span class="sxs-lookup"><span data-stu-id="07d8a-122">Implicit conversion to a D3D12\_DEPTH\_STENCIL\_DESC1 structure.</span></span> <span data-ttu-id="07d8a-123">因為 D3D12 \_ 深度 \_ 樣板 \_ DESC1 是 CD3DX12 深度樣板 DESC1 的基礎類型 \_ \_ ，所以 \_ 物件只會以 const D3D12 \_ 深度樣板 \_ DESC1 參考的形式傳回 \_ 。</span><span class="sxs-lookup"><span data-stu-id="07d8a-123">Because D3D12\_DEPTH\_STENCIL\_DESC1 is the underlying type of CD3DX12\_DEPTH\_STENCIL\_DESC1, the object is simply returned as a const D3D12\_DEPTH\_STENCIL\_DESC1 reference to itself.</span></span>

</dd> <dt>

<span data-ttu-id="07d8a-124">**運算子 const D3D12 \_ 深度 \_ 樣板 \_ DESC () const**</span><span class="sxs-lookup"><span data-stu-id="07d8a-124">**operator const D3D12\_DEPTH\_STENCIL\_DESC() const**</span></span>
</dt> <dd>

<span data-ttu-id="07d8a-125">隱含轉換成 D3D12 \_ 深度樣板 \_ DESC 的 \_ 結構值。</span><span class="sxs-lookup"><span data-stu-id="07d8a-125">Implicit conversion to a D3D12\_DEPTH\_STENCIL\_DESC structure value.</span></span> <span data-ttu-id="07d8a-126">由於 D3D12 \_ 深度 \_ 樣板 \_ DESC 不是 CD3DX12 深度樣板 DESC1 的基礎類型 \_ \_ ，因此 \_ 會建立新的 D3D12 \_ 深度樣板 \_ \_ desc 實例，並以傳值方式傳回。</span><span class="sxs-lookup"><span data-stu-id="07d8a-126">Because D3D12\_DEPTH\_STENCIL\_DESC is not the underlying type of CD3DX12\_DEPTH\_STENCIL\_DESC1, a new D3D12\_DEPTH\_STENCIL\_DESC instance is created and returned by value.</span></span> <span data-ttu-id="07d8a-127">請注意，D3D12 \_ 深度樣板 \_ \_ DESC 不包含 **DepthBoundsTestEnable** 成員，因此此值會在轉換時遺失。</span><span class="sxs-lookup"><span data-stu-id="07d8a-127">Note that D3D12\_DEPTH\_STENCIL\_DESC does not include the **DepthBoundsTestEnable** member, so this value is lost in the conversion.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="07d8a-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="07d8a-128">Requirements</span></span>



| <span data-ttu-id="07d8a-129">需求</span><span class="sxs-lookup"><span data-stu-id="07d8a-129">Requirement</span></span> | <span data-ttu-id="07d8a-130">值</span><span class="sxs-lookup"><span data-stu-id="07d8a-130">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="07d8a-131">標頭</span><span class="sxs-lookup"><span data-stu-id="07d8a-131">Header</span></span><br/> | <dl> <span data-ttu-id="07d8a-132"><dt>D3dx12。h</dt></span><span class="sxs-lookup"><span data-stu-id="07d8a-132"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07d8a-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="07d8a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07d8a-134">D3D12 的 Helper 結構</span><span class="sxs-lookup"><span data-stu-id="07d8a-134">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="07d8a-135">**D3D12 \_ 深度 \_ 樣板 \_ DESC1**</span><span class="sxs-lookup"><span data-stu-id="07d8a-135">**D3D12\_DEPTH\_STENCIL\_DESC1**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1)
</dt> <dt>

[<span data-ttu-id="07d8a-136">**D3D12 \_ 深度 \_ 樣板 \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="07d8a-136">**D3D12\_DEPTH\_STENCIL\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc)
</dt> </dl>

 

 






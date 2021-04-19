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
# <a name="cd3dx12_depth_stencil_desc1-structure"></a>CD3DX12 \_ 深度 \_ 樣板 \_ DESC1 結構

協助程式結構，可讓您輕鬆地初始化 [**D3D12 \_ 深度樣板 \_ \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1) 結構。

## <a name="syntax"></a>語法


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



## <a name="members"></a>成員

<dl> <dt>

**CD3DX12 \_ 深度 \_ 樣板 \_ DESC1 ()**
</dt> <dd>

建立新的、未初始化的 CD3DX12 深度樣板 \_ \_ DESC1 實例 \_ 。

</dd> <dt>

**明確的 CD3DX12 \_ 深度樣板 \_ \_ DESC1 (const D3D12 \_ DEPTH 樣板 \_ \_ DESC1& o)**
</dt> <dd>

建立 CD3DX12 深度樣板 DESC1 的新 \_ 實例 \_ \_ ，並以從 [**D3D12 \_ 深度樣板 \_ \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1) 結構複製而來的值進行初始化。

</dd> <dt>

**明確的 CD3DX12 \_ 深度樣板 \_ \_ DESC1 (const D3D12 \_ 深度樣板 \_ \_ DESC& o)**
</dt> <dd>

建立 CD3DX12 深度樣板 DESC1 的新 \_ 實例 \_ \_ ，並以從 [**D3D12 \_ 深度樣板 \_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc) 結構複製而來的值進行初始化

以及將其他 **DepthBoundsTestEnable** 成員設為 **FALSE**。

</dd> <dt>

**明確的 CD3DX12 \_ 深度樣板 \_ \_ DESC1 (CD3DX12 \_ 預設)**
</dt> <dd>

建立 CD3DX12 深度樣板 DESC1 的新 \_ 實例 \_ \_ ，並使用 D3DX12 所指定的預設狀態進行初始化：

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

**明確的 CD3DX12 \_ 深度樣板 \_ \_ DESC1 (BOOL depthEnable、D3D12 \_ DEPTH \_ WRITE \_ MASK depthWriteMask、D3D12 \_ 比較 \_ FUNC DEPTHFUNC、BOOL STENCILENABLE、UINT8 StencilReadMask、UINT8 stencilWriteMask、D3D12 樣板 op frontStencilFailOp、 \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ D3D12 樣板 op frontStencilDepthFailOp、D3D12 樣板 op frontStencilPassOp、D3D12 比較 Func frontStencilFunc、D3D12 樣板 op backStencilFailOp、D3D12 comparison op backStencilDepthFailOp、D3D12 樣板 op backStencilPassOp、D3D12 比較 func backStencilFunc、BOOL depthBoundsTestEnable)**
</dt> <dd>

建立 CD3DX12 深度樣板 DESC1 的新 \_ 實例 \_ \_ ，並以參數清單中傳遞的值進行初始化。

</dd> <dt>

**~ CD3DX12 \_ 深度 \_ 樣板 \_ DESC1 ()**
</dt> <dd>

終結 D3DX12 深度樣板 DESC1 的 \_ 實例 \_ \_ 。

</dd> <dt>

**運算子 const D3D12 \_ DEPTH \_ 樣板 \_ DESC1& () const**
</dt> <dd>

隱含轉換成 D3D12 \_ 深度樣板 \_ \_ DESC1 結構。 因為 D3D12 \_ 深度 \_ 樣板 \_ DESC1 是 CD3DX12 深度樣板 DESC1 的基礎類型 \_ \_ ，所以 \_ 物件只會以 const D3D12 \_ 深度樣板 \_ DESC1 參考的形式傳回 \_ 。

</dd> <dt>

**運算子 const D3D12 \_ 深度 \_ 樣板 \_ DESC () const**
</dt> <dd>

隱含轉換成 D3D12 \_ 深度樣板 \_ DESC 的 \_ 結構值。 由於 D3D12 \_ 深度 \_ 樣板 \_ DESC 不是 CD3DX12 深度樣板 DESC1 的基礎類型 \_ \_ ，因此 \_ 會建立新的 D3D12 \_ 深度樣板 \_ \_ desc 實例，並以傳值方式傳回。 請注意，D3D12 \_ 深度樣板 \_ \_ DESC 不包含 **DepthBoundsTestEnable** 成員，因此此值會在轉換時遺失。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx12。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3D12 的 Helper 結構](helper-structures-for-d3d12.md)
</dt> <dt>

[**D3D12 \_ 深度 \_ 樣板 \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1)
</dt> <dt>

[**D3D12 \_ 深度 \_ 樣板 \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc)
</dt> </dl>

 

 






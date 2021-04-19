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
# <a name="cd3dx12_depth_stencil_desc-structure"></a>CD3DX12 \_ 深度 \_ 樣板 \_ DESC 結構

協助程式結構，可讓您輕鬆地初始化 [**D3D12 \_ 深度樣板 \_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc) 結構。

## <a name="syntax"></a>語法


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



## <a name="members"></a>成員

<dl> <dt>

**CD3DX12 \_ 深度 \_ 樣板 \_ DESC ()**
</dt> <dd>

建立 D3DX12 深度樣板 DESC 的新、未初始化的實例 \_ \_ \_ 。

</dd> <dt>

**明確 CD3DX12 \_ 深度 \_ 樣板 \_ DESC (const D3D12 \_ depth \_ 樣板 \_ desc& o)**
</dt> <dd>

建立 D3DX12 深度樣板 desc 的新 \_ 實例 \_ \_ ，並以另一個 [**D3D12 \_ 深度樣板 \_ \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc) 結構的內容進行初始化。

</dd> <dt>

**明確 CD3DX12 \_ 深度 \_ 樣板 \_ DESC (CD3DX12 \_ 預設)**
</dt> <dd>

建立 D3DX12 深度樣板 DESC 的新 \_ 實例 \_ \_ ，並以預設參數初始化。

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

**明確的 CD3DX12 \_ 深度樣板 \_ \_ DESC (BOOL depthEnable、D3D12 \_ DEPTH \_ WRITE \_ MASK depthWriteMask、D3D12 \_ 比較 \_ FUNC DEPTHFUNC、BOOL STENCILENABLE、UINT8 StencilReadMask、UINT8 stencilWriteMask、D3D12 樣板 op frontStencilFailOp、 \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ D3D12 樣板 op frontStencilDepthFailOp、D3D12 樣板 op frontStencilPassOp、D3D12 比較 func frontStencilFunc、D3D12 樣板 op backStencilFailOp、D3D12 樣板 op backStencilDepthFailOp、D3D12 樣板 op backStencilPassOp、D3D12 比較 func backStencilFunc)**
</dt> <dd>

建立 D3DX12 深度樣板 DESC 的新 \_ 實例 \_ \_ ，並初始化下列參數：

BOOL depthEnable

[**D3D12 \_深度 \_ 寫入 \_ 遮罩**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_depth_write_mask) depthWriteMask

[**D3D12 \_比較 \_ FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) depthFunc

BOOL stencilEnable

UINT8 stencilReadMask

UINT8 stencilWriteMask

[**D3D12 \_樣板 \_ OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) frontStencilFailOp

[**D3D12 \_樣板 \_ OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) frontStencilDepthFailOp

[**D3D12 \_樣板 \_ OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) frontStencilPassOp

[**D3D12 \_比較 \_ FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) frontStencilFunc

[**D3D12 \_樣板 \_ OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) backStencilFailOp

[**D3D12 \_樣板 \_ OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) backStencilDepthFailOp

[**D3D12 \_樣板 \_ OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) backStencilPassOp

[**D3D12 \_比較 \_ FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) backStencilFunc

</dd> <dt>

**~ CD3DX12 \_ 深度 \_ 樣板 \_ DESC ()**
</dt> <dd>

終結 CD3DX12 深度樣板 DESC 的 \_ 實例 \_ \_ 。

</dd> <dt>

**運算子 const D3D12 \_ 深度 \_ 樣板 \_ DESC& () const**
</dt> <dd>

針對父結構類型定義 & 的傳址運算子。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx12。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**D3D12 \_ 深度 \_ 樣板 \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc)
</dt> <dt>

[D3D12 的 Helper 結構](helper-structures-for-d3d12.md)
</dt> </dl>

 

 






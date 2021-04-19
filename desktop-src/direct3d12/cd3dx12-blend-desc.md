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
# <a name="cd3dx12_blend_desc-structure"></a>CD3DX12 \_ BLEND \_ DESC 結構

協助程式結構，可讓您輕鬆地初始化 [**D3D12 \_ BLEND \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc) 結構。

## <a name="syntax"></a>語法


```C++
struct CD3DX12_BLEND_DESC  : public D3D12_BLEND_DESC{
   CD3DX12_BLEND_DESC();
   explicit CD3DX12_BLEND_DESC(const D3D12_BLEND_DESC& o);
   explicit CD3DX12_BLEND_DESC(CD3DX12_DEFAULT);
   ~CD3DX12_BLEND_DESC();
   operator const D3D12_BLEND_DESC&() const;
};
```



## <a name="members"></a>成員

<dl> <dt>

**CD3DX12 \_ BLEND \_ DESC ()**
</dt> <dd>

建立新的、未初始化的 CD3DX12 \_ BLEND DESC 實例 \_ 。

</dd> <dt>

**明確 CD3DX12 \_ blend \_ desc (const D3D12 \_ blend \_ desc& o)**
</dt> <dd>

建立 CD3DX12 BLEND desc 的新實例 \_ \_ ，並使用另一個 [**D3D12 \_ BLEND \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc) 結構的內容進行初始化。

</dd> <dt>

**明確的 CD3DX12 \_ BLEND \_ DESC (CD3DX12 \_ 預設)**
</dt> <dd>

建立 CD3DX12 BLEND DESC 的新實例 \_ \_ ，並以預設參數初始化。



| 狀態                                   | 預設值                    |
|-----------------------------------------|----------------------------------|
| AlphaToCoverageEnable                   | **FALSE**                        |
| IndependentBlendEnable                  | **FALSE**                        |
| RenderTarget \[ 0 \] 。BlendEnable           | **FALSE**                        |
| RenderTarget \[ 0 \] 。LogicOpEnable         | **FALSE**                        |
| RenderTarget \[ 0 \] 。SrcBlend              | D3D12 \_ BLEND \_ 1                |
| RenderTarget \[ 0 \] 。DestBlend             | D3D12 \_ BLEND \_ 零               |
| RenderTarget \[ 0 \] 。BlendOp               | D3D12 \_ BLEND \_ OP \_ 新增            |
| RenderTarget \[ 0 \] 。SrcBlendAlpha         | D3D12 \_ BLEND \_ 1                |
| RenderTarget \[ 0 \] 。DestBlendAlpha        | D3D12 \_ BLEND \_ 零               |
| RenderTarget \[ 0 \] 。BlendOpAlpha          | D3D12 \_ BLEND \_ OP \_ 新增            |
| RenderTarget \[ 0 \] 。LogicOp               | D3D12 \_ 邏輯 \_ OP \_ NOOP           |
| RenderTarget \[ 0 \] 。RenderTargetWriteMask | D3D12 \_ 色彩 \_ 寫入 \_ \_ 全部啟用 |



 

</dd> <dt>

**~ CD3DX12 \_ BLEND \_ DESC ()**
</dt> <dd>

終結 CD3DX12 BLEND DESC 的實例 \_ \_ 。

</dd> <dt>

**運算子 const D3D12 \_ BLEND \_ DESC& () const**
</dt> <dd>

針對父結構類型定義 & 的傳址運算子。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx12。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**D3D12 \_ BLEND \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc)
</dt> <dt>

[D3D12 的 Helper 結構](helper-structures-for-d3d12.md)
</dt> </dl>

 

 






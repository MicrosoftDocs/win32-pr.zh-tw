---
title: 'CD3DX12_RASTERIZER_DESC 結構 (D3dx12 .h) '
description: 協助程式結構，可讓您輕鬆地初始化 D3D12 的轉譯器 \_ \_ DESC 結構。
ms.assetid: 28AA8256-1CAF-484F-B219-0F0461BA947C
keywords:
- CD3DX12_RASTERIZER_DESC 結構
topic_type:
- apiref
api_name:
- CD3DX12_RASTERIZER_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 078b9e92d25cb5309b4cd97d35586192a37eed90
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106981991"
---
# <a name="cd3dx12_rasterizer_desc-structure"></a>CD3DX12 轉譯器 \_ \_ DESC 結構

協助程式結構，可讓您輕鬆地初始化 D3D12 的轉譯器 [**\_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc) 結構。

## <a name="syntax"></a>語法


```C++
struct CD3DX12_RASTERIZER_DESC  : public D3D12_RASTERIZER_DESC{
   CD3DX12_RASTERIZER_DESC();
   explicit CD3DX12_RASTERIZER_DESC(const D3D12_RASTERIZER_DESC& o);
   explicit CD3DX12_RASTERIZER_DESC(CD3DX12_DEFAULT);
   explicit CD3DX12_RASTERIZER_DESC(D3D12_FILL_MODE fillMode, D3D12_CULL_MODE cullMode, BOOL frontCounterClockwise, INT depthBias, FLOAT depthBiasClamp, FLOAT slopeScaledDepthBias, BOOL depthClipEnable, BOOL multisampleEnable, BOOL antialiasedLineEnable, UINT forcedSampleCount, D3D12_CONSERVATIVE_RASTERIZATION_MODE conservativeRaster);
   ~CD3DX12_RASTERIZER_DESC();
   operator const D3D12_RASTERIZER_DESC&() const;
};
```



## <a name="members"></a>成員

<dl> <dt>

**CD3DX12 轉譯器 \_ \_ DESC ()**
</dt> <dd>

建立新的、未初始化的 CD3DX12 轉譯器 \_ \_ DESC 實例。

</dd> <dt>

**明確的 CD3DX12 轉譯器 \_ \_ desc (const D3D12 轉譯器 \_ \_ desc& o)**
</dt> <dd>

建立 CD3DX12 轉譯器 desc 的新 \_ 實例 \_ ，並以另一個 D3D12 的轉譯 [**器 \_ \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc) 結構的內容進行初始化。

</dd> <dt>

**明確的 CD3DX12 轉譯器 \_ \_ DESC (CD3DX12 \_ 預設)**
</dt> <dd>

建立 CD3DX12 轉譯器 DESC 的新 \_ 實例 \_ ，並以預設參數初始化。

``` syntax
        FillMode = D3D12_FILL_MODE_SOLID;  
        CullMode = D3D12_CULL_MODE_BACK;  
        FrontCounterClockwise = FALSE;  
        DepthBias = D3D12_DEFAULT_DEPTH_BIAS;  
        DepthBiasClamp = D3D12_DEFAULT_DEPTH_BIAS_CLAMP;  
        SlopeScaledDepthBias = D3D12_DEFAULT_SLOPE_SCALED_DEPTH_BIAS;  
        DepthClipEnable = TRUE;  
        MultisampleEnable = FALSE;  
        AntialiasedLineEnable = FALSE;  
        ForcedSampleCount = 0;  
        ConservativeRaster = D3D12_CONSERVATIVE_RASTERIZATION_MODE_OFF;  
```

</dd> <dt>

**明確的 CD3DX12 轉譯器 \_ \_ DESC (D3D12 \_ FILL \_ mode fillMode、D3D12 \_ 剔除 \_ MODE CullMode、BOOL FrontCounterClockwise、INT DepthBias、FLOAT DepthBiasClamp、FLOAT SlopeScaledDepthBias、BOOL DepthClipEnable、BOOL MultisampleEnable、BOOL antialiasedLineEnable、UINT forcedSampleCount、D3D12 保守式點陣 \_ \_ \_ 模式 conservativeRaster)**
</dt> <dd>

建立 CD3DX12 轉譯器 DESC 的新 \_ 實例 \_ ，並初始化下列參數：

[**D3D12 \_填滿 \_ 模式**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_fill_mode) fillMode

[**D3D12 \_挑選 \_ 模式**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cull_mode) cullMode

BOOL frontCounterClockwise

INT depthBias

FLOAT depthBiasClamp

FLOAT slopeScaledDepthBias

BOOL depthClipEnable

BOOL multisampleEnable

BOOL antialiasedLineEnable

UINT forcedSampleCount

[**D3D12 \_保守的 \_ 點陣化 \_ 模式**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_conservative_rasterization_mode) conservativeRaster

</dd> <dt>

**~ CD3DX12 轉譯器 \_ \_ DESC ()**
</dt> <dd>

終結 CD3DX12 轉譯器 DESC 的 \_ 實例 \_ 。

</dd> <dt>

**運算子 const D3D12 轉譯器 \_ \_ DESC& () const**
</dt> <dd>

針對父結構類型定義 & 的傳址運算子。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx12。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**D3D12 轉譯器 \_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc)
</dt> <dt>

[D3D12 的 Helper 結構](helper-structures-for-d3d12.md)
</dt> </dl>

 

 






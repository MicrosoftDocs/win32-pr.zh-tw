---
title: 'CD3DX12_STATIC_SAMPLER_DESC 結構 (D3dx12 .h) '
description: 協助程式結構，可讓您輕鬆地初始化 D3D12 \_ 靜態 \_ 取樣器 \_ DESC 結構。
ms.assetid: C402415D-7BD5-4E23-82C9-B29B0B5669B8
keywords:
- CD3DX12_STATIC_SAMPLER_DESC 結構
topic_type:
- apiref
api_name:
- CD3DX12_STATIC_SAMPLER_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d6b10749f7a56d928e0a4218d534cc2a8ec4fab
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106982193"
---
# <a name="cd3dx12_static_sampler_desc-structure"></a>CD3DX12 \_ 靜態 \_ 取樣器 \_ DESC 結構

協助程式結構，可讓您輕鬆地初始化 [**D3D12 \_ 靜態取樣器 \_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) 結構。

## <a name="syntax"></a>語法


```C++
struct CD3DX12_STATIC_SAMPLER_DESC  : public D3D12_STATIC_SAMPLER_DESC{
       CD3DX12_STATIC_SAMPLER_DESC();
       explicit CD3DX12_STATIC_SAMPLER_DESC(const D3D12_STATIC_SAMPLER_DESC &o);
       CD3DX12_STATIC_SAMPLER_DESC(UINT shaderRegister, D3D12_FILTER filter = D3D12_FILTER_ANISOTROPIC, D3D12_TEXTURE_ADDRESS_MODE addressU = D3D12_TEXTURE_ADDRESS_MODE_WRAP, D3D12_TEXTURE_ADDRESS_MODE addressV = D3D12_TEXTURE_ADDRESS_MODE_WRAP, D3D12_TEXTURE_ADDRESS_MODE addressW = D3D12_TEXTURE_ADDRESS_MODE_WRAP, FLOAT mipLODBias = 0, UINT maxAnisotropy = 16, D3D12_COMPARISON_FUNC comparisonFunc = D3D12_COMPARISON_FUNC_LESS_EQUAL, D3D12_STATIC_BORDER_COLOR borderColor = D3D12_STATIC_BORDER_COLOR_OPAQUE_WHITE, FLOAT minLOD = 0.f, FLOAT maxLOD = D3D12_FLOAT32_MAX, D3D12_SHADER_VISIBILITY shaderVisibility = D3D12_SHADER_VISIBILITY_ALL, UINT registerSpace = 0);
  void static inline Init(D3D12_STATIC_SAMPLER_DESC &samplerDesc, UINT shaderRegister, D3D12_FILTER filter = D3D12_FILTER_ANISOTROPIC, D3D12_TEXTURE_ADDRESS_MODE addressU = D3D12_TEXTURE_ADDRESS_MODE_WRAP, D3D12_TEXTURE_ADDRESS_MODE addressV = D3D12_TEXTURE_ADDRESS_MODE_WRAP, D3D12_TEXTURE_ADDRESS_MODE addressW = D3D12_TEXTURE_ADDRESS_MODE_WRAP, FLOAT mipLODBias = 0, UINT maxAnisotropy = 16, D3D12_COMPARISON_FUNC comparisonFunc = D3D12_COMPARISON_FUNC_LESS_EQUAL, D3D12_STATIC_BORDER_COLOR borderColor = D3D12_STATIC_BORDER_COLOR_OPAQUE_WHITE, FLOAT minLOD = 0.f, FLOAT maxLOD = D3D12_FLOAT32_MAX, D3D12_SHADER_VISIBILITY shaderVisibility = D3D12_SHADER_VISIBILITY_ALL, UINT registerSpace = 0);
  void inline Init(UINT shaderRegister, D3D12_FILTER filter = D3D12_FILTER_ANISOTROPIC, D3D12_TEXTURE_ADDRESS_MODE addressU = D3D12_TEXTURE_ADDRESS_MODE_WRAP, D3D12_TEXTURE_ADDRESS_MODE addressV = D3D12_TEXTURE_ADDRESS_MODE_WRAP, D3D12_TEXTURE_ADDRESS_MODE addressW = D3D12_TEXTURE_ADDRESS_MODE_WRAP, FLOAT mipLODBias = 0, UINT maxAnisotropy = 16, D3D12_COMPARISON_FUNC comparisonFunc = D3D12_COMPARISON_FUNC_LESS_EQUAL, D3D12_STATIC_BORDER_COLOR borderColor = D3D12_STATIC_BORDER_COLOR_OPAQUE_WHITE, FLOAT minLOD = 0.f, FLOAT maxLOD = D3D12_FLOAT32_MAX, D3D12_SHADER_VISIBILITY shaderVisibility = D3D12_SHADER_VISIBILITY_ALL, UINT registerSpace = 0);
};
```



## <a name="members"></a>成員

<dl> <dt>

**CD3DX12 \_ 靜態 \_ 取樣器 \_ DESC ()**
</dt> <dd>

建立 CD3DX12 靜態取樣器 DESC 的新、未初始化的實例 \_ \_ \_ 。

</dd> <dt>

**明確 CD3DX12 \_ 靜態 \_ 取樣器 \_ DESC (const D3D12 \_ static 取樣器 \_ \_ desc &o)**
</dt> <dd>

建立 CD3DX12 靜態取樣器 desc 的新實例 \_ \_ \_ ，並以另一個 [**D3D12 \_ 靜態 \_ 取樣器 \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) 結構的內容進行初始化。

</dd> <dt>

**CD3DX12 \_ 靜態 \_ 取樣 \_ 器 DESC (UINT shaderRegister，D3D12 \_ filter filter = D3D12 \_ FILTER \_ 各向異性，D3D12 \_ 材質 \_ address \_ MODE addressU = D3D12 \_ 材質 \_ address \_ mode \_ wrap，D3D12 \_ 材質 \_ address \_ mode addressV = D3D12 \_ 材質 \_ address \_ mode \_ Wrap，D3D12 \_ 紋理 \_ 位址 \_ 模式 ADDRESSW = D3D12 \_ 材質 \_ 位址 \_ 模式 \_ WRAP，FLOAT MIPLODBIAS = 0，UINT maxAnisotropy = 16，D3D12 \_ 比較 \_ func comparisonFunc = D3D12 \_ 比較 \_ func \_ 小於 \_ 等於，D3D12 \_ 靜態 \_ 框線 \_ 色彩邊框型 = D3D12 \_ 靜態 \_ 框線色彩不 \_ \_ 透明 \_ 白色，float minLOD = 0。 f，float maxLOD = D3D12 的 \_ \_ 最大值，D3D12 \_ 著色器可見度 shaderVisibility = \_ \_ \_ \_ 0)**
</dt> <dd>

建立 CD3DX12 靜態取樣器 DESC 的新實例 \_ \_ ，並 \_ 初始化下列參數：

UINT shaderRegister

 (opt) [**D3D12 \_ 篩選**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter) 條件 = D3D12 \_ 篩選 \_ 條件

 (opt) [**D3D12 \_ 材質 \_ 位址 \_ 模式**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressU = D3D12 \_ 材質 \_ 位址 \_ 模式 \_ 換行

 (opt) [**D3D12 \_ 材質 \_ 位址 \_ 模式**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressV = D3D12 \_ 材質 \_ 位址 \_ 模式 \_ 換行

 (opt) [**D3D12 \_ 材質 \_ 位址 \_ 模式**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressW = D3D12 \_ 材質 \_ 位址 \_ 模式 \_ 換行

 (opt) FLOAT mipLODBias = 0

 (opt) UINT maxAnisotropy = 16

 (opt) [**D3D12 \_ 比較 \_ FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) comparisonFunc = D3D12 \_ 比較 \_ func \_ 小於 \_ 相等

 (opt) [**D3D12 \_ 靜態 \_ 框線 \_ 色彩邊框型**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color) = D3D12 \_ 靜態 \_ 框線色彩不 \_ \_ 透明 \_ 白色

 (opt) FLOAT minLOD = 0 f

 (opt) FLOAT maxLOD = D3D12 \_ FLOAT32 \_ MAX

 (opt) [**D3D12 \_ 著色器 \_ 可見度**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility)shaderVisibility = D3D12 \_ 著色器 \_ 可見度 \_

 (opt) UINT registerSpace = 0

</dd> <dt>

**靜態內嵌 Init (D3D12 \_ 靜態 \_ 取樣 \_ 器 DESC &SamplerDesc、UINT shaderRegister、D3D12 \_ FILTER filter = D3D12 \_ FILTER 非 \_ 等、D3D12 \_ 紋理 \_ 位址 \_ 模式 addressU = D3D12 \_ 紋理 \_ 位址 \_ 模式 \_ wrap、D3D12 \_ 材質 \_ 位址 \_ 模式 addressV = D3D12 \_ 材質 \_ 位址 \_ 模式 \_ 換行、D3D12 \_ 紋理 \_ 位址 \_ 模式 ADDRESSW = D3D12 \_ 材質 \_ 位址 \_ 模式 \_ WRAP，FLOAT MIPLODBIAS = 0，UINT maxAnisotropy = 16，D3D12 \_ 比較 \_ func comparisonFunc = D3D12 \_ 比較 \_ func \_ 小於 \_ 等於，D3D12 \_ 靜態 \_ 框線 \_ 色彩邊框型 = D3D12 \_ 靜態 \_ 框線色彩不 \_ \_ 透明 \_ 白色，float minLOD = 0。 f，float maxLOD = D3D12 的 \_ \_ 最大值，D3D12 \_ 著色器 \_ 可見度 shaderVisibility = \_ \_ \_ 0)**
</dt> <dd>

指定初始化下列參數的函式：

[**D3D12 \_靜態 \_ 取樣器 \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) &samplerDesc

UINT shaderRegister

 (opt) [**D3D12 \_ 篩選**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter) 條件 = D3D12 \_ 篩選 \_ 條件

 (opt) [**D3D12 \_ 材質 \_ 位址 \_ 模式**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressU = D3D12 \_ 材質 \_ 位址 \_ 模式 \_ 換行

 (opt) [**D3D12 \_ 材質 \_ 位址 \_ 模式**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressV = D3D12 \_ 材質 \_ 位址 \_ 模式 \_ 換行

 (opt) [**D3D12 \_ 材質 \_ 位址 \_ 模式**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressW = D3D12 \_ 材質 \_ 位址 \_ 模式 \_ 換行

 (opt) FLOAT mipLODBias = 0

 (opt) UINT maxAnisotropy = 16

 (opt) [**D3D12 \_ 比較 \_ FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) comparisonFunc = D3D12 \_ 比較 \_ func \_ 小於 \_ 相等

 (opt) [**D3D12 \_ 靜態 \_ 框線 \_ 色彩邊框型**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color) = D3D12 \_ 靜態 \_ 框線色彩不 \_ \_ 透明 \_ 白色

 (opt) FLOAT minLOD = 0 f

 (opt) FLOAT maxLOD = D3D12 \_ FLOAT32 \_ MAX

 (opt) [**D3D12 \_ 著色器 \_ 可見度**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility)shaderVisibility = D3D12 \_ 著色器 \_ 可見度 \_

 (opt) UINT registerSpace = 0

</dd> <dt>

**內嵌 Init (UINT shaderRegister、D3D12 \_ filter filter = D3D12 \_ FILTER \_ 各向異性、D3D12 \_ 材質 \_ address \_ mode addressU = D3D12 \_ 材質 \_ Address \_ MODE \_ WRAP、D3D12 \_ 材質 \_ address \_ Mode addressV = D3D12 \_ 材質 \_ address \_ Mode \_ wrap、D3D12 \_ 紋理 \_ 位址 \_ 模式 addressW = D3D12 \_ 材質 \_ 位址 \_ 模式 \_ WRAP，FLOAT MipLODBias = 0，UINT maxAnisotropy = 16，D3D12 \_ 比較 \_ func comparisonFunc = D3D12 \_ 比較 \_ func \_ 小於 \_ 等於，D3D12 \_ 靜態 \_ 框線 \_ 色彩邊框型 = D3D12 \_ 靜態 \_ 框線色彩不 \_ \_ 透明 \_ 白色，float minLOD = 0。 f，float maxLOD = D3D12 的 \_ \_ 最大值，D3D12 \_ 著色器 \_ 可見度 shaderVisibility = \_ \_ \_ 0)**
</dt> <dd>

指定初始化下列參數的函式：

UINT shaderRegister

 (opt) [**D3D12 \_ 篩選**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter) 條件 = D3D12 \_ 篩選 \_ 條件

 (opt) [**D3D12 \_ 材質 \_ 位址 \_ 模式**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressU = D3D12 \_ 材質 \_ 位址 \_ 模式 \_ 換行

 (opt) [**D3D12 \_ 材質 \_ 位址 \_ 模式**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressV = D3D12 \_ 材質 \_ 位址 \_ 模式 \_ 換行

 (opt) [**D3D12 \_ 材質 \_ 位址 \_ 模式**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressW = D3D12 \_ 材質 \_ 位址 \_ 模式 \_ 換行

 (opt) FLOAT mipLODBias = 0

 (opt) UINT maxAnisotropy = 16

 (opt) [**D3D12 \_ 比較 \_ FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) comparisonFunc = D3D12 \_ 比較 \_ func \_ 小於 \_ 相等

 (opt) [**D3D12 \_ 靜態 \_ 框線 \_ 色彩邊框型**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color) = D3D12 \_ 靜態 \_ 框線色彩不 \_ \_ 透明 \_ 白色

 (opt) FLOAT minLOD = 0 f

 (opt) FLOAT maxLOD = D3D12 \_ FLOAT32 \_ MAX

 (opt) [**D3D12 \_ 著色器 \_ 可見度**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility)shaderVisibility = D3D12 \_ 著色器 \_ 可見度 \_

 (opt) UINT registerSpace = 0

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx12。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**D3D12 \_ 靜態 \_ 取樣器 \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)
</dt> <dt>

[D3D12 的 Helper 結構](helper-structures-for-d3d12.md)
</dt> </dl>

 

 






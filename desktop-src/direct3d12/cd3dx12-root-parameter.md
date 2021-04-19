---
title: 'CD3DX12_ROOT_PARAMETER 結構 (D3dx12 .h) '
description: 協助程式結構，可讓您輕鬆地初始化 D3D12 \_ 根 \_ 參數結構。
ms.assetid: CDDF84D0-4E66-4CF2-999B-3F401E8DD17F
keywords:
- CD3DX12_ROOT_PARAMETER 結構
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_PARAMETER
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9099b0839b6b55676d5a8afdfb913948e70bbb7f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106981808"
---
# <a name="cd3dx12_root_parameter-structure"></a>CD3DX12 \_ 根 \_ 參數結構

協助程式結構，可讓您輕鬆地初始化 [**D3D12 \_ 根 \_ 參數**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) 結構。

## <a name="syntax"></a>語法


```C++
struct CD3DX12_ROOT_PARAMETER  : public D3D12_ROOT_PARAMETER{
       CD3DX12_ROOT_PARAMETER();
       explicit CD3DX12_ROOT_PARAMETER(const D3D12_ROOT_PARAMETER &o);
  void static inline InitAsDescriptorTable(D3D12_ROOT_PARAMETER &rootParam, UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE* pDescriptorRanges, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsConstants(D3D12_ROOT_PARAMETER &rootParam, UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsConstantBufferView(D3D12_ROOT_PARAMETER &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsShaderResourceView(D3D12_ROOT_PARAMETER &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsUnorderedAccessView(D3D12_ROOT_PARAMETER &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsDescriptorTable(UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE* pDescriptorRanges, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsConstants(UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsConstantBufferView(UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsShaderResourceView(UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsUnorderedAccessView(UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
};
```



## <a name="members"></a>成員

<dl> <dt>

**CD3DX12 \_ 根 \_ 參數 ()**
</dt> <dd>

建立 CD3DX12 根參數的新、未初始化的 \_ 實例 \_ 。

</dd> <dt>

**明確 CD3DX12 的 \_ 根 \_ 參數 (const D3D12 \_ 根 \_ 參數 &o)**
</dt> <dd>

建立 CD3DX12 根參數的新實例 \_ \_ ，並使用另一個 [**D3D12 \_ 根 \_ 參數**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) 結構的內容進行初始化。

</dd> <dt>

**靜態內嵌 InitAsDescriptorTable (D3D12 \_ 根 \_ 參數 &ROOTPARAM、UINT numDescriptorRanges、const D3D12 \_ 描述項 \_ 範圍 \* pDescriptorRanges、D3D12 \_ 著色器 \_ 可見度可見度 = D3D12 \_ 著色器 \_ 可見度 \_ 所有)**
</dt> <dd>

指定初始化下列參數的函式：

[**D3D12 \_根 \_ 參數**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam

UINT numDescriptorRanges

[**D3D12 \_描述項 \_ 範圍**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) \* pDescriptorRanges

 (opt) [**D3D12 \_ 著色器 \_ 可見度**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) 可見度 = D3D12 \_ 著色器 \_ 可見 \_ 性

</dd> <dt>

**靜態內嵌 InitAsConstants (D3D12 \_ 根 \_ 參數 &ROOTPARAM、uint NUM32BITVALUES、UINT SHADERREGISTER、UINT registerSpace = 0、D3D12 \_ 著色器 \_ 可見度可見度 = D3D12 \_ 著色器 \_ 可見度 \_ 所有)**
</dt> <dd>

指定初始化下列參數的函式：

[**D3D12 \_根 \_ 參數**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam

UINT num32BitValues

UINT shaderRegister

 (opt) UINT registerSpace = 0

 (opt) [**D3D12 \_ 著色器 \_ 可見度**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) 可見度 = D3D12 \_ 著色器 \_ 可見 \_ 性

</dd> <dt>

**靜態內嵌 InitAsConstantBufferView (D3D12 \_ 根 \_ 參數 &ROOTPARAM、UINT SHADERREGISTER、UINT registerSpace = 0、D3D12 \_ 著色器 \_ 可見度可見度 = D3D12 \_ 著色器 \_ 可見度 \_ 所有)**
</dt> <dd>

指定初始化下列參數的函式：

[**D3D12 \_根 \_ 參數**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam

UINT shaderRegister

 (opt) UINT registerSpace = 0

 (opt) [**D3D12 \_ 著色器 \_ 可見度**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) 可見度 = D3D12 \_ 著色器 \_ 可見 \_ 性

</dd> <dt>

**靜態內嵌 InitAsShaderResourceView (D3D12 \_ 根 \_ 參數 &ROOTPARAM、UINT SHADERREGISTER、UINT registerSpace = 0、D3D12 \_ 著色器 \_ 可見度可見度 = D3D12 \_ 著色器 \_ 可見度 \_ 所有)**
</dt> <dd>

指定初始化下列參數的函式：

[**D3D12 \_根 \_ 參數**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam

UINT shaderRegister

 (opt) UINT registerSpace = 0

 (opt) [**D3D12 \_ 著色器 \_ 可見度**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) 可見度 = D3D12 \_ 著色器 \_ 可見 \_ 性

</dd> <dt>

**靜態內嵌 InitAsUnorderedAccessView (D3D12 \_ 根 \_ 參數 &ROOTPARAM、UINT SHADERREGISTER、UINT registerSpace = 0、D3D12 \_ 著色器 \_ 可見度可見度 = D3D12 \_ 著色器 \_ 可見度 \_ 所有)**
</dt> <dd>

指定初始化下列參數的函式：

[**D3D12 \_根 \_ 參數**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam

UINT shaderRegister

 (opt) UINT registerSpace = 0

 (opt) [**D3D12 \_ 著色器 \_ 可見度**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) 可見度 = D3D12 \_ 著色器 \_ 可見 \_ 性

</dd> <dt>

**內嵌 InitAsDescriptorTable (UINT numDescriptorRanges，const D3D12 \_ 描述項 \_ 範圍 \* pDescriptorRanges，D3D12 \_ 著色器 \_ 可見度可見度 = D3D12 \_ 著色器 \_ 可見度 \_ 所有)**
</dt> <dd>

指定初始化下列參數的函式：

UINT numDescriptorRanges

[**D3D12 \_描述項 \_ 範圍**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) \* pDescriptorRanges

 (opt) [**D3D12 \_ 著色器 \_ 可見度**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) 可見度 = D3D12 \_ 著色器 \_ 可見 \_ 性

</dd> <dt>

**內嵌 InitAsConstants (UINT num32BitValues、UINT shaderRegister、UINT registerSpace = 0、D3D12 \_ 著色器 \_ 可見度可見度 = D3D12 \_ 著色器 \_ 可見度 \_ 所有)**
</dt> <dd>

指定初始化下列參數的函式：

UINT num32BitValues

UINT shaderRegister

 (opt) UINT registerSpace = 0

 (opt) [**D3D12 \_ 著色器 \_ 可見度**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) 可見度 = D3D12 \_ 著色器 \_ 可見 \_ 性

</dd> <dt>

**內嵌 InitAsConstantBufferView (UINT shaderRegister、UINT registerSpace = 0、D3D12 \_ 著色器 \_ 可見度可見度 = D3D12 \_ 著色器 \_ 可見度 \_ 所有)**
</dt> <dd>

指定初始化下列參數的函式：

UINT shaderRegister

 (opt) UINT registerSpace = 0

 (opt) [**D3D12 \_ 著色器 \_ 可見度**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) 可見度 = D3D12 \_ 著色器 \_ 可見 \_ 性

</dd> <dt>

**內嵌 InitAsShaderResourceView (UINT shaderRegister、UINT registerSpace = 0、D3D12 \_ 著色器 \_ 可見度可見度 = D3D12 \_ 著色器 \_ 可見度 \_ 所有)**
</dt> <dd>

指定初始化下列參數的函式：

UINT shaderRegister

 (opt) UINT registerSpace = 0

 (opt) [**D3D12 \_ 著色器 \_ 可見度**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) 可見度 = D3D12 \_ 著色器 \_ 可見 \_ 性

</dd> <dt>

**內嵌 InitAsUnorderedAccessView (UINT shaderRegister、UINT registerSpace = 0、D3D12 \_ 著色器 \_ 可見度可見度 = D3D12 \_ 著色器 \_ 可見度 \_ 所有)**
</dt> <dd>

指定初始化下列參數的函式：

UINT shaderRegister

 (opt) UINT registerSpace = 0

 (opt) [**D3D12 \_ 著色器 \_ 可見度**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) 可見度 = D3D12 \_ 著色器 \_ 可見 \_ 性

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx12。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**D3D12 \_ 根 \_ 參數**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter)
</dt> <dt>

[D3D12 的 Helper 結構](helper-structures-for-d3d12.md)
</dt> </dl>

 

 






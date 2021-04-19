---
title: 'CD3DX12_ROOT_PARAMETER1 結構 (D3dx12 .h) '
description: 協助程式結構，可讓您輕鬆地初始化 D3D12 \_ 根 \_ PARAMETER1 結構。
ms.assetid: CDE0C02E-0112-4FD9-A4A2-36E8C326715C
keywords:
- CD3DX12_ROOT_PARAMETER1 結構
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_PARAMETER1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d582016b26df0d57f7792afd30fc4fcbf3ba97b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106989223"
---
# <a name="cd3dx12_root_parameter1-structure"></a>CD3DX12 \_ 根 \_ PARAMETER1 結構

協助程式結構，可讓您輕鬆地初始化 [**D3D12 \_ 根 \_ PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) 結構。

## <a name="syntax"></a>語法


```C++
struct CD3DX12_ROOT_PARAMETER1  : public D3D12_ROOT_PARAMETER1{
       CD3DX12_ROOT_PARAMETER1();
       explicit CD3DX12_ROOT_PARAMETER1(const D3D12_ROOT_PARAMETER1 &o);
  void static inline InitAsDescriptorTable(D3D12_ROOT_PARAMETER1 &rootParam, UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE1* pDescriptorRanges, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsConstants(D3D12_ROOT_PARAMETER1 &rootParam, UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsConstantBufferView(D3D12_ROOT_PARAMETER1 &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsShaderResourceView(D3D12_ROOT_PARAMETER1 &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsUnorderedAccessView(D3D12_ROOT_PARAMETER1 &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsDescriptorTable(UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE1* pDescriptorRanges, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsConstants(UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsConstantBufferView(UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsShaderResourceView(UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsUnorderedAccessView(UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
};
```



## <a name="members"></a>成員

<dl> <dt>

**CD3DX12 \_ ROOT \_ PARAMETER1 ()**
</dt> <dd>

建立新的、未初始化的 CD3DX12 \_ 根 PARAMETER1 實例 \_ 。

</dd> <dt>

**明確 CD3DX12 \_ 根 \_ PARAMETER1 (const D3D12 \_ root \_ PARAMETER1 &o)**
</dt> <dd>

建立 CD3DX12 根 PARAMETER1 的新實例 \_ \_ ，並以另一個 [**D3D12 \_ 根 \_ PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) 結構的內容進行初始化。

</dd> <dt>

**靜態內嵌 InitAsDescriptorTable (D3D12 \_ 根 \_ PARAMETER1 &ROOTPARAM、UINT numDescriptorRanges、const D3D12 \_ 描述項 \_ RANGE1 \* pDescriptorRanges、D3D12 \_ 著色器 \_ 可見度可見度 = D3D12 \_ 著色器 \_ 可見度 \_ 所有)**
</dt> <dd>

指定初始化下列參數的函式：

[**D3D12 \_ROOT \_ PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &rootParam

UINT numDescriptorRanges

const [**D3D12 \_ 描述項 \_ RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) \* pDescriptorRanges

[**D3D12 \_著色器 \_ 可見度**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility)可見度 = D3D12 \_ 著色器 \_ 可見度 \_

</dd> <dt>

**靜態內嵌 InitAsConstants (D3D12 \_ 根 \_ PARAMETER1 &ROOTPARAM、UINT NUM32BITVALUES、UINT SHADERREGISTER、UINT registerSpace = 0、D3D12 \_ 著色器 \_ 可見度可見度 = D3D12 \_ 著色器 \_ 可見度 \_ 所有)**
</dt> <dd>

指定初始化下列參數的函式：

[**D3D12 \_ROOT \_ PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &rootParam

UINT num32BitValues

UINT shaderRegister

UINT registerSpace = 0

[**D3D12 \_著色器 \_ 可見度**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility)可見度 = D3D12 \_ 著色器 \_ 可見度 \_

</dd> <dt>

**靜態內嵌 InitAsConstantBufferView (D3D12 \_ 根 \_ PARAMETER1 &ROOTPARAM，UINT SHADERREGISTER，UINT registerSpace = 0，D3D12 \_ 根目錄描述元旗標 \_ \_ 旗標 = D3D12 \_ 根目錄 \_ 描述項旗標 \_ \_ 無，D3D12 \_ 著色器可見 \_ 性 = D3D12 \_ 著色器 \_ 可見度 \_ 所有)**
</dt> <dd>

指定初始化下列參數的函式：

[**D3D12 \_ROOT \_ PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &rootParam

UINT shaderRegister

UINT registerSpace = 0

[**D3D12 \_根 \_ 描述 \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) 元旗標旗標 = D3D12 \_ 根目錄 \_ 描述元旗標 \_ \_ 無

[**D3D12 \_著色器 \_ 可見度**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility)可見度 = D3D12 \_ 著色器 \_ 可見度 \_

</dd> <dt>

**靜態內嵌 InitAsShaderResourceView (D3D12 \_ 根 \_ PARAMETER1 &ROOTPARAM，UINT SHADERREGISTER，UINT registerSpace = 0，D3D12 \_ 根目錄描述元旗標 \_ \_ 旗標 = D3D12 \_ 根目錄 \_ 描述項旗標 \_ \_ 無，D3D12 \_ 著色器可見 \_ 性 = D3D12 \_ 著色器 \_ 可見度 \_ 所有)**
</dt> <dd>

指定初始化下列參數的函式：

[**D3D12 \_ROOT \_ PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &rootParam

UINT shaderRegister

UINT registerSpace = 0

[**D3D12 \_根 \_ 描述 \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) 元旗標旗標 = D3D12 \_ 根目錄 \_ 描述元旗標 \_ \_ 無

[**D3D12 \_著色器 \_ 可見度**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility)可見度 = D3D12 \_ 著色器 \_ 可見度 \_

</dd> <dt>

**靜態內嵌 InitAsUnorderedAccessView (D3D12 \_ 根 \_ PARAMETER1 &ROOTPARAM，UINT SHADERREGISTER，UINT registerSpace = 0，D3D12 \_ 根目錄描述元旗標 \_ \_ 旗標 = D3D12 \_ 根目錄 \_ 描述項旗標 \_ \_ 無，D3D12 \_ 著色器可見 \_ 性 = D3D12 \_ 著色器 \_ 可見度 \_ 所有)**
</dt> <dd>

指定初始化下列參數的函式：

[**D3D12 \_ROOT \_ PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &rootParam

UINT shaderRegister

UINT registerSpace = 0

[**D3D12 \_根 \_ 描述 \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) 元旗標旗標 = D3D12 \_ 根目錄 \_ 描述元旗標 \_ \_ 無

[**D3D12 \_著色器 \_ 可見度**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility)可見度 = D3D12 \_ 著色器 \_ 可見度 \_

</dd> <dt>

**內嵌 InitAsDescriptorTable (UINT numDescriptorRanges、const D3D12 \_ 描述項 \_ RANGE1 \* pDescriptorRanges、D3D12 \_ 著色器 \_ 可見度 = D3D12 \_ 著色器 \_ 可見度 \_ 所有)**
</dt> <dd>

指定初始化下列參數的函式：

UINT numDescriptorRanges

const [**D3D12 \_ 描述項 \_ RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) \* pDescriptorRanges

[**D3D12 \_著色器 \_ 可見度**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility)可見度 = D3D12 \_ 著色器 \_ 可見度 \_

</dd> <dt>

**內嵌 InitAsConstants (UINT num32BitValues、UINT shaderRegister、UINT registerSpace = 0、D3D12 \_ 著色器 \_ 可見度可見度 = D3D12 \_ 著色器 \_ 可見度 \_ 所有)**
</dt> <dd>

指定初始化下列參數的函式：

UINT num32BitValues

UINT shaderRegister

UINT registerSpace = 0

[**D3D12 \_著色器 \_ 可見度**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility)可見度 = D3D12 \_ 著色器 \_ 可見度 \_

</dd> <dt>

**inline InitAsConstantBufferView (UINT shaderRegister，UINT registerSpace = 0，D3D12 \_ 根 \_ 描述元 \_ 旗標旗標 = D3D12 \_ 根目錄描述項旗標 \_ \_ \_ 無，D3D12 \_ 著色器 \_ 可見度 = D3D12 \_ 著色器 \_ 可見度 \_ 所有)**
</dt> <dd>

指定初始化下列參數的函式：

UINT shaderRegister

UINT registerSpace = 0

[**D3D12 \_根 \_ 描述 \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) 元旗標旗標 = D3D12 \_ 根目錄 \_ 描述元旗標 \_ \_ 無

[**D3D12 \_著色器 \_ 可見度**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility)可見度 = D3D12 \_ 著色器 \_ 可見度 \_

</dd> <dt>

**inline InitAsShaderResourceView (UINT shaderRegister，UINT registerSpace = 0，D3D12 \_ 根 \_ 描述元 \_ 旗標旗標 = D3D12 \_ 根目錄描述項旗標 \_ \_ \_ 無，D3D12 \_ 著色器 \_ 可見度 = D3D12 \_ 著色器 \_ 可見度 \_ 所有)**
</dt> <dd>

指定初始化下列參數的函式：

UINT shaderRegister

UINT registerSpace = 0

[**D3D12 \_根 \_ 描述 \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) 元旗標旗標 = D3D12 \_ 根目錄 \_ 描述元旗標 \_ \_ 無

[**D3D12 \_著色器 \_ 可見度**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility)可見度 = D3D12 \_ 著色器 \_ 可見度 \_

</dd> <dt>

**inline InitAsUnorderedAccessView (UINT shaderRegister，UINT registerSpace = 0，D3D12 \_ 根 \_ 描述元 \_ 旗標旗標 = D3D12 \_ 根目錄描述項旗標 \_ \_ \_ 無，D3D12 \_ 著色器 \_ 可見度 = D3D12 \_ 著色器 \_ 可見度 \_ 所有)**
</dt> <dd>

指定初始化下列參數的函式：

UINT shaderRegister

UINT registerSpace = 0

[**D3D12 \_根 \_ 描述 \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) 元旗標旗標 = D3D12 \_ 根目錄 \_ 描述元旗標 \_ \_ 無

[**D3D12 \_著色器 \_ 可見度**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility)可見度 = D3D12 \_ 著色器 \_ 可見度 \_

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx12。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**D3D12 \_ 根 \_ PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1)
</dt> <dt>

[D3D12 的 Helper 結構](helper-structures-for-d3d12.md)
</dt> </dl>

 

 






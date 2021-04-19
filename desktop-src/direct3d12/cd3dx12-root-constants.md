---
title: 'CD3DX12_ROOT_CONSTANTS 結構 (D3dx12 .h) '
description: Helper 結構，可讓您輕鬆地初始化 D3D12 \_ 根 \_ 常數結構。
ms.assetid: 2F517DCE-BC0C-4678-9C25-D826036F99A8
keywords:
- CD3DX12_ROOT_CONSTANTS 結構
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_CONSTANTS
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7a1f81a429b083400adad60f316cc90c4ede1d9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106993860"
---
# <a name="cd3dx12_root_constants-structure"></a>CD3DX12 \_ 根 \_ 常數結構

Helper 結構，可讓您輕鬆地初始化 [**D3D12 \_ 根 \_ 常數**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) 結構。

## <a name="syntax"></a>語法


```C++
struct CD3DX12_ROOT_CONSTANTS  : public D3D12_ROOT_CONSTANTS{
       CD3DX12_ROOT_CONSTANTS();
       explicit CD3DX12_ROOT_CONSTANTS(const D3D12_ROOT_CONSTANTS &o);
       CD3DX12_ROOT_CONSTANTS(UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0);
  void inline Init(UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0);
  void static inline Init(D3D12_ROOT_CONSTANTS &rootConstants, UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0);
};
```



## <a name="members"></a>成員

<dl> <dt>

**CD3DX12 \_ 根 \_ 常數 ()**
</dt> <dd>

建立 CD3DX12 根常數的新、未初始化的 \_ 實例 \_ 。

</dd> <dt>

**明確 CD3DX12 的 \_ 根 \_ 常數 (const D3D12 \_ 根 \_ 常數 &o)**
</dt> <dd>

建立 CD3DX12 根常數的新實例 \_ \_ ，並以另一個 [**D3D12 \_ 根 \_ 常數**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) 結構的內容進行初始化。

</dd> <dt>

**CD3DX12 \_ 根 \_ 常數 (uint NUM32BITVALUES、uint SHADERREGISTER、uint registerSpace = 0)**
</dt> <dd>

建立 CD3DX12 根常數的新實例 \_ \_ ，並初始化下列參數：

UINT num32BitValues

UINT shaderRegister

 (opt) UINT registerSpace = 0

</dd> <dt>

**內嵌初始 (UINT num32BitValues、UINT shaderRegister、UINT registerSpace = 0)**
</dt> <dd>

指定初始化下列參數的函式：

UINT num32BitValues

UINT shaderRegister

 (opt) UINT registerSpace = 0

</dd> <dt>

**靜態內嵌 Init (D3D12 \_ 根 \_ 常數 &ROOTCONSTANTS、uint NUM32BITVALUES、uint SHADERREGISTER、UINT registerSpace = 0)**
</dt> <dd>

指定初始化下列參數的函式：

[**D3D12 \_根 \_ 常數**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) &rootConstants

UINT num32BitValues

UINT shaderRegister

 (opt) UINT registerSpace = 0

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx12。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**D3D12 \_ 根 \_ 常數**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants)
</dt> <dt>

[D3D12 的 Helper 結構](helper-structures-for-d3d12.md)
</dt> </dl>

 

 






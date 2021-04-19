---
title: 'CD3DX12_ROOT_DESCRIPTOR 結構 (D3dx12 .h) '
description: 協助程式結構，可讓您輕鬆地初始化 D3D12 \_ 根目錄 \_ 描述元結構。
ms.assetid: DB05BAB7-DD30-4EC7-8D66-C0B2D8DD7BAC
keywords:
- CD3DX12_ROOT_DESCRIPTOR 結構
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_DESCRIPTOR
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 710064436e0287b570700ff5812b728ca62be56d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106989224"
---
# <a name="cd3dx12_root_descriptor-structure"></a>CD3DX12 \_ 根目錄 \_ 描述元結構

協助程式結構，可讓您輕鬆地初始化 [**D3D12 \_ 根目錄 \_ 描述**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor) 元結構。

## <a name="syntax"></a>語法


```C++
struct CD3DX12_ROOT_DESCRIPTOR  : public D3D12_ROOT_DESCRIPTOR{
       CD3DX12_ROOT_DESCRIPTOR();
       explicit CD3DX12_ROOT_DESCRIPTOR(const D3D12_ROOT_DESCRIPTOR &o);
       CD3DX12_ROOT_DESCRIPTOR(UINT shaderRegister, UINT registerSpace = 0);
  void inline Init(UINT shaderRegister, UINT registerSpace = 0);
  void static inline Init(D3D12_ROOT_DESCRIPTOR &table, UINT shaderRegister, UINT registerSpace = 0);
};
```



## <a name="members"></a>成員

<dl> <dt>

**CD3DX12 \_ 根目錄 \_ 描述元 ()**
</dt> <dd>

建立新的、未初始化的 CD3DX12 \_ 根目錄描述項實例 \_ 。

</dd> <dt>

**明確 CD3DX12 的 \_ 根 \_ 描述元 (const D3D12 \_ 根描述元 \_ &o)**
</dt> <dd>

建立 CD3DX12 根描述元的新 \_ 實例 \_ ，並以另一個 [**D3D12 \_ 根 \_ 描述**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor) 元結構的內容進行初始化。

</dd> <dt>

**CD3DX12 \_ 根 \_ 描述元 (uint SHADERREGISTER，uint registerSpace = 0)**
</dt> <dd>

建立 CD3DX12 根描述元的新 \_ 實例 \_ ，並初始化下列參數：

UINT shaderRegister

 (opt) UINT registerSpace = 0

</dd> <dt>

**內嵌 Init (UINT shaderRegister，UINT registerSpace = 0)**
</dt> <dd>

指定初始化下列參數的函式：

UINT shaderRegister

 (opt) UINT registerSpace = 0

</dd> <dt>

**靜態內嵌 Init (D3D12 \_ 根 \_ 描述元 &資料表、uint SHADERREGISTER、uint registerSpace = 0)**
</dt> <dd>

指定初始化下列參數的函式：

[**D3D12 \_根 \_ 描述**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor) 元 &資料表

UINT shaderRegister

 (opt) UINT registerSpace = 0

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx12。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**D3D12 \_ 根目錄 \_ 描述元**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor)
</dt> <dt>

[D3D12 的 Helper 結構](helper-structures-for-d3d12.md)
</dt> </dl>

 

 






---
title: 'CD3DX12_ROOT_DESCRIPTOR1 結構 (D3dx12 .h) '
description: 協助程式結構，可讓您輕鬆地初始化 D3D12 \_ 根 \_ DESCRIPTOR1 結構。
ms.assetid: 664822BF-5C27-4541-953F-219894547A6C
keywords:
- CD3DX12_ROOT_DESCRIPTOR1 結構
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_DESCRIPTOR1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66cb64509c82c11180ca3e1d2937dff5d077897d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106977140"
---
# <a name="cd3dx12_root_descriptor1-structure"></a>CD3DX12 \_ 根 \_ DESCRIPTOR1 結構

協助程式結構，可讓您輕鬆地初始化 [**D3D12 \_ 根 \_ DESCRIPTOR1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1) 結構。

## <a name="syntax"></a>語法


```C++
struct CD3DX12_ROOT_DESCRIPTOR1  : public D3D12_ROOT_DESCRIPTOR1{
       CD3DX12_ROOT_DESCRIPTOR1();
       explicit CD3DX12_ROOT_DESCRIPTOR1(const D3D12_ROOT_DESCRIPTOR1 &o);
       CD3DX12_ROOT_DESCRIPTOR1(UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE);
  void inline Init(UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE);
  void static inline Init(D3D12_ROOT_DESCRIPTOR1 &table, UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE);
};
```



## <a name="members"></a>成員

<dl> <dt>

**CD3DX12 \_ ROOT \_ DESCRIPTOR1 ()**
</dt> <dd>

建立新的、未初始化的 CD3DX12 \_ 根 DESCRIPTOR1 實例 \_ 。

</dd> <dt>

**明確 CD3DX12 \_ 根 \_ DESCRIPTOR1 (const D3D12 \_ root \_ DESCRIPTOR1 &o)**
</dt> <dd>

建立 CD3DX12 根 DESCRIPTOR1 的新實例 \_ \_ ，並以另一個 [**D3D12 \_ 根 \_ DESCRIPTOR1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1) 結構的內容進行初始化。

</dd> <dt>

**CD3DX12 \_ ROOT \_ DESCRIPTOR1 (uint SHADERREGISTER，uint registerSpace = 0，D3D12 \_ 根描述元旗標 \_ 旗標 \_ = D3D12 \_ 根目錄描述元旗標 \_ \_ \_ 無)**
</dt> <dd>

建立 CD3DX12 根 DESCRIPTOR1 的新實例 \_ \_ ，並初始化下列參數：

UINT shaderRegister

UINT registerSpace = 0

[**D3D12 \_根 \_ 描述 \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) 元旗標旗標 = D3D12 \_ 根目錄 \_ 描述元旗標 \_ \_ 無

</dd> <dt>

**內嵌 Init (UINT shaderRegister，UINT registerSpace = 0，D3D12 \_ 根描述元旗標旗標 \_ \_ = D3D12 根目錄描述元旗標 \_ \_ \_ \_ 無)**
</dt> <dd>

指定初始化下列參數的函式：

UINT shaderRegister

UINT registerSpace = 0

[**D3D12 \_根 \_ 描述 \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) 元旗標旗標 = D3D12 \_ 根目錄 \_ 描述元旗標 \_ \_ 無

</dd> <dt>

**靜態內嵌 Init (D3D12 \_ 根 \_ DESCRIPTOR1 &資料表、uint SHADERREGISTER、uint registerSpace = 0、D3D12 \_ 根目錄描述元旗標 \_ \_ = D3D12 \_ 根目錄描述項旗標 \_ \_ \_ 無)**
</dt> <dd>

指定初始化下列參數的函式：

[**D3D12 \_根 \_ DESCRIPTOR1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1) &資料表

UINT shaderRegister

UINT registerSpace = 0

[**D3D12 \_根 \_ 描述 \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) 元旗標旗標 = D3D12 \_ 根目錄 \_ 描述元旗標 \_ \_ 無

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx12。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**D3D12 \_ 根 \_ DESCRIPTOR1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1)
</dt> <dt>

[D3D12 的 Helper 結構](helper-structures-for-d3d12.md)
</dt> </dl>

 

 






---
title: 'CD3DX12_ROOT_DESCRIPTOR_TABLE 結構 (D3dx12 .h) '
description: 協助程式結構，可讓您輕鬆地初始化 D3D12 \_ 根 \_ 描述元 \_ 資料表結構。
ms.assetid: 154B4C50-4E94-471C-A44E-F120A84F007C
keywords:
- CD3DX12_ROOT_DESCRIPTOR_TABLE 結構
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_DESCRIPTOR_TABLE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f675624526a959e6cf92172383b12590c36fc408
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106982860"
---
# <a name="cd3dx12_root_descriptor_table-structure"></a>CD3DX12 \_ 根 \_ 描述元 \_ 資料表結構

協助程式結構，可讓您輕鬆地初始化 [**D3D12 \_ 根描述元 \_ \_ 資料表**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) 結構。

## <a name="syntax"></a>語法


```C++
struct CD3DX12_ROOT_DESCRIPTOR_TABLE  : public D3D12_ROOT_DESCRIPTOR_TABLE{
       CD3DX12_ROOT_DESCRIPTOR_TABLE();
       explicit CD3DX12_ROOT_DESCRIPTOR_TABLE(const D3D12_ROOT_DESCRIPTOR_TABLE &o);
       CD3DX12_ROOT_DESCRIPTOR_TABLE(UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE* _pDescriptorRanges);
  void inline Init(UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE* _pDescriptorRanges);
  void static inline Init(D3D12_ROOT_DESCRIPTOR_TABLE &rootDescriptorTable, UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE* _pDescriptorRanges);
};
```



## <a name="members"></a>成員

<dl> <dt>

**CD3DX12 \_ 根 \_ 描述元 \_ 資料表 ()**
</dt> <dd>

建立 CD3DX12 根描述中繼資料表的新、未初始化的實例 \_ \_ \_ 。

</dd> <dt>

**明確 CD3DX12 的 \_ 根 \_ 描述元 \_ 資料表 (const D3D12 \_ 根描述元 \_ \_ 資料表 &o)**
</dt> <dd>

建立 CD3DX12 根描述中繼資料表的新實例 \_ \_ \_ ，並以另一個 [**D3D12 \_ 根 \_ 描述元 \_ 資料表**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) 結構的內容進行初始化。

</dd> <dt>

**CD3DX12 \_ 根 \_ 描述元 \_ 資料表 (UINT NUMDESCRIPTORRANGES，const D3D12 \_ 描述項 \_ 範圍 \* \_ pDescriptorRanges)**
</dt> <dd>

建立 CD3DX12 根描述中繼資料表的新實例 \_ \_ ，並 \_ 初始化下列參數：

UINT numDescriptorRanges

[**D3D12 \_描述項 \_ 範圍**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) \* \_ pDescriptorRanges

</dd> <dt>

**內嵌 Init (UINT numDescriptorRanges、const D3D12 \_ 描述項 \_ 範圍 \* \_ pDescriptorRanges)**
</dt> <dd>

指定初始化下列參數的函式：

UINT numDescriptorRanges

[**D3D12 \_描述項 \_ 範圍**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) \* \_ pDescriptorRanges

</dd> <dt>

**靜態內嵌 Init (D3D12 \_ 根 \_ 描述元 \_ 資料表 &RootDescriptorTable、UINT NUMDESCRIPTORRANGES、const D3D12 \_ 描述項 \_ 範圍 \* \_ pDescriptorRanges)**
</dt> <dd>

指定初始化下列參數的函式：

[**D3D12 \_根 \_ 描述元 \_ 資料表**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) &rootDescriptorTable

UINT numDescriptorRanges

[**D3D12 \_描述項 \_ 範圍**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) \* \_ pDescriptorRanges

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx12。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**D3D12 \_ 根 \_ 描述元 \_ 資料表**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table)
</dt> <dt>

[D3D12 的 Helper 結構](helper-structures-for-d3d12.md)
</dt> </dl>

 

 






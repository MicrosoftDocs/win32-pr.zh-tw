---
title: 'CD3DX12_SUBRESOURCE_RANGE_UINT64 結構 (D3dx12 .h) '
description: 協助程式結構，可讓您輕鬆地初始化 D3D12 \_ SUBRESOURCE \_ 範圍 \_ UINT64 結構。
ms.assetid: 607A60ED-98D2-4A77-9A7A-6B54342EA101
keywords:
- CD3DX12_SUBRESOURCE_RANGE_UINT64 結構
topic_type:
- apiref
api_name:
- CD3DX12_SUBRESOURCE_RANGE_UINT64
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2aea83d993c0c7b58ded8d0b92374d1dcbacdcc8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106976689"
---
# <a name="cd3dx12_subresource_range_uint64-structure"></a>CD3DX12 \_ SUBRESOURCE \_ 範圍 \_ UINT64 結構

協助程式結構，可讓您輕鬆地初始化 [**D3D12 \_ SUBRESOURCE \_ 範圍 \_ UINT64**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_range_uint64) 結構。

## <a name="syntax"></a>語法


```C++
struct CD3DX12_SUBRESOURCE_RANGE_UINT64  : public D3D12_SUBRESOURCE_RANGE_UINT64{
  CD3DX12_SUBRESOURCE_RANGE_UINT64 CD3DX12_SUBRESOURCE_RANGE_UINT64();
  CD3DX12_SUBRESOURCE_RANGE_UINT64 explicit CD3DX12_SUBRESOURCE_RANGE_UINT64(const D3D12_SUBRESOURCE_RANGE_UINT64 &o);
  CD3DX12_SUBRESOURCE_RANGE_UINT64 CD3DX12_SUBRESOURCE_RANGE_UINT64(UINT subresource, const D3D12_RANGE_UINT64& range);
  CD3DX12_SUBRESOURCE_RANGE_UINT64 CD3DX12_SUBRESOURCE_RANGE_UINT64(UINT subresource, UINT64 begin, UINT64 end);
                                   operator const D3D12_SUBRESOURCE_RANGE_UINT64&() const;
};
```



## <a name="members"></a>成員

<dl> <dt>

**CD3DX12 \_ SUBRESOURCE \_ 範圍 \_ UINT64 ()**
</dt> <dd>

建立 CD3DX12 \_ SUBRESOURCE 範圍 UINT64 的新、未初始化的 \_ 實例 \_ 。

</dd> <dt>

**明確的 CD3DX12 \_ SUBRESOURCE \_ 範圍 \_ UINT64 (const D3D12 \_ SUBRESOURCE \_ range \_ uint64 &o)**
</dt> <dd>

建立 CD3DX12 \_ SUBRESOURCE 範圍 uint64 的新實例 \_ \_ ，並以從 [**D3D12 \_ SUBRESOURCE \_ 範圍 \_ uint64**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_range_uint64) 結構複製而來的值進行初始化。

</dd> <dt>

**CD3DX12 \_ SUBRESOURCE \_ 範圍 \_ uint64 (UINT SUBRESOURCE、const D3D12 \_ 範圍 \_ uint64& 範圍)**
</dt> <dd>

建立 CD3DX12 深度樣板 DESC1 的新 \_ 實例 \_ \_ ，並以參數清單中傳遞的值進行初始化。

</dd> <dt>

**CD3DX12 \_ SUBRESOURCE \_ 範圍 \_ UINT64 (UINT SUBRESOURCE，UINT64 begin，uint64 end)**
</dt> <dd>

建立 CD3DX12 深度樣板 DESC1 的新 \_ 實例 \_ \_ ，並以參數清單中傳遞的值進行初始化。

</dd> <dt>

**operator const D3D12 \_ SUBRESOURCE \_ RANGE \_ UINT64& () const**
</dt> <dd>

隱含轉換成 D3D12 \_ SUBRESOURCE \_ 範圍 \_ UINT64 結構。 因為 D3D12 \_ SUBRESOURCE \_ 範圍 \_ uint64 是 CD3DX12 \_ SUBRESOURCE 範圍 uint64 的基礎 \_ 類型 \_ ，所以物件只會以 const D3D12 \_ 深度樣板 \_ DESC1 參考的形式傳回 \_ 。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx12。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3D12 的 Helper 結構](helper-structures-for-d3d12.md)
</dt> <dt>

[**D3D12 \_ SUBRESOURCE \_ 範圍 \_ UINT64**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_range_uint64)
</dt> </dl>

 

 






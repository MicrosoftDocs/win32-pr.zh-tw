---
title: 'CD3DX12_RESOURCE_BARRIER 結構 (D3dx12 .h) '
description: 協助程式結構，可讓您輕鬆地初始化 D3D12 \_ 資源 \_ 關卡結構。
ms.assetid: 89E0F38C-8802-46E6-9583-95C5D853CD99
keywords:
- CD3DX12_RESOURCE_BARRIER 結構
topic_type:
- apiref
api_name:
- CD3DX12_RESOURCE_BARRIER
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8eaa9b19a8bc7dcebba5982313bb362dbcee6157
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106992353"
---
# <a name="cd3dx12_resource_barrier-structure"></a>CD3DX12 \_ 資源 \_ 關卡結構

協助程式結構，可讓您輕鬆地初始化 [**D3D12 \_ 資源 \_ 關卡**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier) 結構。

## <a name="syntax"></a>語法


```C++
struct CD3DX12_RESOURCE_BARRIER  : public D3D12_RESOURCE_BARRIER{
                           CD3DX12_RESOURCE_BARRIER();
                           explicit CD3DX12_RESOURCE_BARRIER(const D3D12_RESOURCE_BARRIER &o);
  CD3DX12_RESOURCE_BARRIER static inline Transition(ID3D12Resource* pResource, D3D12_RESOURCE_STATES stateBefore, D3D12_RESOURCE_STATES stateAfter, UINT subresource = D3D12_RESOURCE_BARRIER_ALL_SUBRESOURCES, D3D12_RESOURCE_BARRIER_FLAGS flags = D3D12_RESOURCE_BARRIER_FLAG_NONE);
  CD3DX12_RESOURCE_BARRIER static inline Aliasing(ID3D12Resource* pResourceBefore, ID3D12Resource* pResourceAfter);
  CD3DX12_RESOURCE_BARRIER static inline UAV(ID3D12Resource* pResource);
                           operator const D3D12_RESOURCE_BARRIER&() const;
};
```



## <a name="members"></a>成員

<dl> <dt>

**CD3DX12 \_ 資源 \_ 屏障 ()**
</dt> <dd>

建立 CD3DX12 資源屏障的新、未初始化的 \_ 實例 \_ 。

</dd> <dt>

**明確的 CD3DX12 \_ 資源 \_ 屏障 (const D3D12 \_ 資源 \_ 屏障 &o)**
</dt> <dd>

建立 CD3DX12 資源屏障的新實例 \_ \_ ，並以另一個 [**D3D12 \_ 資源 \_ 屏障**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier)的內容進行初始化。

</dd> <dt>

**靜態內嵌轉換 (ID3D12Resource \* pResource、D3D12 \_ 資源 \_ 狀態 stateBefore、D3D12 \_ 資源 \_ 狀態 STATEAFTER、UINT subresource = D3D12 \_ 資源 \_ 屏障 \_ ALL \_ 子資源、D3D12 \_ 資源 \_ 屏障 \_ 旗標旗標 = D3D12 \_ 資源 \_ 屏障 \_ 旗標 \_ 無)**
</dt> <dd>

使用下列參數，在資源狀態之間轉換：

[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \*pResource

[**D3D12 \_資源 \_ 狀態**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states) stateBefore

[**D3D12 \_資源 \_ 狀態**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states) stateAfter

 (opt) UINT subresource = [ **D3D12 \_ 資源 \_ 屏障 \_ 所有 \_ 子資源**](constants.md)

 (opt) [**D3D12 \_ 資源 \_ 屏障 \_ 旗**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_barrier_flags) 標旗標 = D3D12 \_ 資源 \_ 屏障 \_ 旗標 \_ 無

</dd> <dt>

**靜態內嵌別名 (ID3D12Resource \* pResourceBefore、ID3D12Resource \* pResourceAfter)**
</dt> <dd>

在關卡轉換之前和之後建立資源的別名。 參數：

[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \*pResourceBefore

[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \*pResourceAfter

</dd> <dt>

**靜態內嵌 UAV (ID3D12Resource \* pResource)**
</dt> <dd>

建立資源的未排序存取- (UAV) 。 參數：

[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \*pResource

</dd> <dt>

**operator const D3D12 \_ 資源 \_ 屏障& () const**
</dt> <dd>

針對父結構類型定義 & 的傳址運算子。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx12。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**D3D12 \_ 資源 \_ 屏障**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier)
</dt> <dt>

[D3D12 的 Helper 結構](helper-structures-for-d3d12.md)
</dt> </dl>

 

 






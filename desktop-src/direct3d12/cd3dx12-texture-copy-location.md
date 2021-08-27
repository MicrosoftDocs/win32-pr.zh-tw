---
title: 'CD3DX12_TEXTURE_COPY_LOCATION 結構 (D3dx12 .h) '
description: 協助程式結構，可讓您輕鬆地初始化 D3D12 \_ 材質 \_ 複製 \_ 位置結構。
ms.assetid: 8BA93729-2FFB-4C09-88B0-779049BAF385
keywords:
- CD3DX12_TEXTURE_COPY_LOCATION 結構
topic_type:
- apiref
api_name:
- CD3DX12_TEXTURE_COPY_LOCATION
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d0a1ee179d2400bc04df9c3214d97d3c7a861357f33b7805e492a24f769bdba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119638"
---
# <a name="cd3dx12_texture_copy_location-structure"></a>CD3DX12 \_ 材質 \_ 複製 \_ 位置結構

協助程式結構，可讓您輕鬆地初始化 [**D3D12 \_ 材質 \_ 複製 \_ 位置**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location) 結構。

## <a name="syntax"></a>語法


```C++
struct CD3DX12_TEXTURE_COPY_LOCATION  : public D3D12_TEXTURE_COPY_LOCATION{
   CD3DX12_TEXTURE_COPY_LOCATION();
   explicit CD3DX12_TEXTURE_COPY_LOCATION(const D3D12_TEXTURE_COPY_LOCATION &o);
   CD3DX12_TEXTURE_COPY_LOCATION(ID3D12Resource* pRes);
   CD3DX12_TEXTURE_COPY_LOCATION(ID3D12Resource* pRes, D3D12_PLACED_SUBRESOURCE_FOOTPRINT const& Footprint);
   CD3DX12_TEXTURE_COPY_LOCATION(ID3D12Resource* pRes, UINT Sub);
};
```



## <a name="members"></a>成員

<dl> <dt>

**CD3DX12 \_ 材質 \_ 複製 \_ 位置 ()**
</dt> <dd>

建立 CD3DX12 \_ 材質複製位置的新、未初始化的 \_ 實例 \_ 。

</dd> <dt>

**明確 CD3DX12 \_ 材質 \_ 複製 \_ 位置 (const D3D12 \_ 材質 \_ 複製 \_ 位置 &o)**
</dt> <dd>

建立 CD3DX12 \_ 材質複製位置的新實例 \_ \_ ，並使用另一個 [**D3D12 \_ 材質 \_ 複製 \_ 位置**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location) 結構的內容進行初始化。

</dd> <dt>

**CD3DX12 \_ 材質 \_ 複製 \_ 位置 (ID3D12Resource \* 按)**
</dt> <dd>

建立 CD3DX12 \_ 材質複製位置的新實例 \_ ，並 \_ 初始化下列參數：

[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \*壓力

</dd> <dt>

**CD3DX12 \_ 材質 \_ 複製 \_ 位置 (ID3D12RESOURCE \* 按，D3D12 將 SUBRESOURCE 耗用量 \_ \_ \_ 常數& 足跡)**
</dt> <dd>

建立 CD3DX12 \_ 材質複製位置的新實例 \_ ，並 \_ 初始化下列參數：

[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \*壓力

[**D3D12 \_將 \_ SUBRESOURCE \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint) 的耗用量常數& 足跡

</dd> <dt>

**CD3DX12 \_ 材質 \_ 複製 \_ 位置 (ID3D12RESOURCE \* 按，UINT Sub)**
</dt> <dd>

建立 CD3DX12 \_ 材質複製位置的新實例 \_ ，並 \_ 初始化下列參數：

[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \*壓力

UINT Sub

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx12。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**D3D12 \_ 材質 \_ 複製 \_ 位置**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location)
</dt> <dt>

[D3D12 的 Helper 結構](helper-structures-for-d3d12.md)
</dt> </dl>

 

 






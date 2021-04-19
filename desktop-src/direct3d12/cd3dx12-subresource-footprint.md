---
title: 'CD3DX12_SUBRESOURCE_FOOTPRINT 結構 (D3dx12 .h) '
description: 協助程式結構，可讓您輕鬆地初始化 D3D12 \_ SUBRESOURCE \_ 足跡結構。
ms.assetid: 17266FB0-41B5-4A70-A896-206B54F5E76F
keywords:
- CD3DX12_SUBRESOURCE_FOOTPRINT 結構
topic_type:
- apiref
api_name:
- CD3DX12_SUBRESOURCE_FOOTPRINT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab58e9a007d736222d9525d7a064456a1a9a7f14
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106976460"
---
# <a name="cd3dx12_subresource_footprint-structure"></a>CD3DX12 \_ SUBRESOURCE \_ 足跡結構

協助程式結構，可讓您輕鬆地初始化 [**D3D12 \_ SUBRESOURCE \_ 足跡**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint) 結構。

## <a name="syntax"></a>語法


```C++
struct CD3DX12_SUBRESOURCE_FOOTPRINT  : public D3D12_SUBRESOURCE_FOOTPRINT{
   CD3DX12_SUBRESOURCE_FOOTPRINT();
   explicit CD3DX12_SUBRESOURCE_FOOTPRINT(const D3D12_SUBRESOURCE_FOOTPRINT &o);
   CD3DX12_SUBRESOURCE_FOOTPRINT(DXGI_FORMAT format, UINT width, UINT height, UINT depth, UINT rowPitch);
   explicit CD3DX12_SUBRESOURCE_FOOTPRINT(const D3D12_RESOURCE_DESC& resDesc, UINT rowPitch);
   operator const D3D12_SUBRESOURCE_FOOTPRINT&() const;
};
```



## <a name="members"></a>成員

<dl> <dt>

**CD3DX12 \_ SUBRESOURCE \_ 足跡 ()**
</dt> <dd>

建立新的、未初始化的 CD3DX12 \_ SUBRESOURCE 足跡實例 \_ 。

</dd> <dt>

**明確的 CD3DX12 \_ SUBRESOURCE \_ 足跡 (const D3D12 \_ SUBRESOURCE 使用量 \_ &o)**
</dt> <dd>

建立 CD3DX12 SUBRESOURCE 使用量的新實例 \_ \_ ，並以另一個 [**D3D12 \_ SUBRESOURCE \_ 足跡**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint) 結構的內容進行初始化。

</dd> <dt>

**CD3DX12 \_ SUBRESOURCE \_ 足跡 (DXGI \_ 格式格式、UINT width、UINT height、UINT Depth、uint rowPitch)**
</dt> <dd>

建立 CD3DX12 SUBRESOURCE 足跡的新實例 \_ \_ ，並初始化下列參數：

[**DXGI \_格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) 格式

UINT 寬度

UINT 高度

UINT 深度

UINT rowPitch

</dd> <dt>

**明確的 CD3DX12 \_ SUBRESOURCE \_ 足跡 (const D3D12 \_ 資源 \_ DESC& resDesc，UINT rowPitch)**
</dt> <dd>

建立 CD3DX12 SUBRESOURCE 足跡的新實例 \_ \_ ，並初始化下列參數：

[**D3D12 \_資源 \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc)& resDesc

UINT rowPitch

</dd> <dt>

**operator const D3D12 \_ SUBRESOURCE \_& () const**
</dt> <dd>

針對父結構類型定義 & 的傳址運算子。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx12。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**D3D12 \_ SUBRESOURCE \_ 足跡**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint)
</dt> <dt>

[D3D12 的 Helper 結構](helper-structures-for-d3d12.md)
</dt> </dl>

 


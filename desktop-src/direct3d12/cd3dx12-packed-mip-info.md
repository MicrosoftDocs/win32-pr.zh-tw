---
title: 'CD3DX12_PACKED_MIP_INFO 結構 (D3dx12 .h) '
description: 協助程式結構，可讓您輕鬆地初始化 D3D12 \_ 壓縮 \_ MIP \_ 資訊結構。
ms.assetid: B3549D78-C354-48FC-A012-1F835DBD585E
keywords:
- CD3DX12_PACKED_MIP_INFO 結構
topic_type:
- apiref
api_name:
- CD3DX12_PACKED_MIP_INFO
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f4565bbac6189cffc5358213437463b4abc0322
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106997372"
---
# <a name="cd3dx12_packed_mip_info-structure"></a>CD3DX12 \_ 封裝的 \_ MIP \_ 資訊結構

協助程式結構，可讓您輕鬆地初始化 [**D3D12 \_ 壓縮 \_ MIP \_ 資訊**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_packed_mip_info) 結構。

## <a name="syntax"></a>語法


```C++
struct CD3DX12_PACKED_MIP_INFO  : public D3D12_PACKED_MIP_INFO{
   CD3DX12_PACKED_MIP_INFO();
   explicit CD3DX12_PACKED_MIP_INFO(const D3D12_PACKED_MIP_INFO &o);
   CD3DX12_PACKED_MIP_INFO(UINT8 numStandardMips, UINT8 numPackedMips, UINT numTilesForPackedMips, UINT startTileIndexInOverallResource);
   operator const D3D12_PACKED_MIP_INFO&() const;
};
```



## <a name="members"></a>成員

<dl> <dt>

**CD3DX12 \_ 封裝的 \_ MIP \_ INFO ()**
</dt> <dd>

建立 CD3DX12 \_ 壓縮 MIP 資訊之未初始化的新實例 \_ \_ 。

</dd> <dt>

**明確 CD3DX12 \_ 壓縮 \_ mip \_ 資訊 (const D3D12 \_ 封裝的 \_ mip \_ info &o)**
</dt> <dd>

建立 CD3DX12 \_ 壓縮 mip 資訊的新實例 \_ \_ ，並使用另一個 [**D3D12 壓縮的 \_ \_ mip \_ 資訊**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_packed_mip_info) 結構的內容進行初始化。

</dd> <dt>

**CD3DX12 \_ 封裝的 \_ MIP \_ INFO (UINT8 NumStandardMips、UINT8 NumPackedMips、UINT NumTilesForPackedMips、UINT startTileIndexInOverallResource)**
</dt> <dd>

建立 CD3DX12 \_ 壓縮 MIP 資訊的新實例 \_ ，並 \_ 初始化下列參數：

UINT8 numStandardMips

UINT8 numPackedMips

UINT numTilesForPackedMips

UINT startTileIndexInOverallResource

</dd> <dt>

**運算子 const D3D12 \_ 壓縮 \_ MIP \_ INFO& () const**
</dt> <dd>

針對父結構類型定義 & 的傳址運算子。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx12。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**D3D12 \_ 封裝的 \_ MIP \_ 資訊**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_packed_mip_info)
</dt> <dt>

[D3D12 的 Helper 結構](helper-structures-for-d3d12.md)
</dt> </dl>

 

 






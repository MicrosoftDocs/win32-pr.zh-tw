---
description: 測量紋理和索引頂點的快取點擊率效能。
ms.assetid: 70bc4e93-0a34-485b-bdcc-028c24b52f62
title: 'D3DDEVINFO_D3D9CACHEUTILIZATION 結構 (D3D9Types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_D3D9CACHEUTILIZATION
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 94f77549d0ea2a9c59d7de8367a6133085cc2771
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104514569"
---
# <a name="d3ddevinfo_d3d9cacheutilization-structure"></a>D3DDEVINFO \_ D3D9CACHEUTILIZATION 結構

測量紋理和索引頂點的快取點擊率效能。

## <a name="syntax"></a>語法


```C++
typedef struct D3DDEVINFO_D3D9CACHEUTILIZATION {
  FLOAT TextureCacheHitRate;
  FLOAT PostTransformVertexCacheHitRate;
} D3DDEVINFO_D3D9CACHEUTILIZATION, *LPD3DDEVINFO_D3D9CACHEUTILIZATION;
```



## <a name="members"></a>成員

<dl> <dt>

**TextureCacheHitRate**
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

在紋理快取中尋找材質的點擊率。 這假設有紋理快取。 使用許多大型紋理來增加詳細資料偏差，以使用最詳細的材質，或使用自訂著色器程式碼在大型紋理上產生近乎隨機的材質存取模式，可能會大幅影響紋理快取點擊率。

</dd> <dt>

**PostTransformVertexCacheHitRate**
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

在頂點快取中尋找已轉換頂點的點擊率。 GPU 的設計目的是要轉換索引的頂點，並可將其儲存在頂點快取中。 如果您使用的是網格， [**D3DXOptimizeFaces**](d3dxoptimizefaces.md) 或 [**D3DXOptimizeVertices**](d3dxoptimizevertices.md) 可能會導致更好的頂點快取使用。

</dd> </dl>

## <a name="remarks"></a>備註

有效率的快取通常較接近90% 的點擊率，而且效率不佳的快取通常會接近10% 的點擊率 (但低百分比不一定是) 的問題。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3D9Types。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 結構](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)
</dt> </dl>

 

 

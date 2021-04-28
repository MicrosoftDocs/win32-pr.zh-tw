---
description: D3DX10_MESHOPT 列舉-指定要執行的網格優化類型。
ms.assetid: 20d1da8c-8c3d-4045-9a37-d534a8682716
title: 'D3DX10_MESHOPT 列舉 (D3DX10Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_MESHOPT
api_type:
- HeaderDef
api_location:
- D3DX10Mesh.h
ms.openlocfilehash: 7b3085cf9970f2c1f6fe3748cc4db8f4fb2b2a78
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105446"
---
# <a name="d3dx10_meshopt-enumeration"></a>D3DX10 \_ MESHOPT 列舉

指定要執行的網格優化類型。

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DX10_MESHOPT { 
  D3DX10_MESHOPT_COMPACT             = 0x01000000,
  D3DX10_MESHOPT_ATTR_SORT           = 0x02000000,
  D3DX10_MESHOPT_VERTEX_CACHE        = 0x04000000,
  D3DX10_MESHOPT_STRIP_REORDER       = 0x08000000,
  D3DX10_MESHOPT_IGNORE_VERTS        = 0x10000000,
  D3DX10_MESHOPT_DO_NOT_SPLIT        = 0x20000000,
  D3DX10_MESHOPT_DEVICE_INDEPENDENT  = 0x00400000
} D3DX10_MESHOPT, *LPD3DX10_MESHOPT;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="D3DX10_MESHOPT_COMPACT"></span><span id="d3dx10_meshopt_compact"></span>**D3DX10 \_ MESHOPT \_ COMPACT**
</dt> <dd>

重新排序臉部以移除未使用的頂點和臉部。

</dd> <dt>

<span id="D3DX10_MESHOPT_ATTR_SORT"></span><span id="d3dx10_meshopt_attr_sort"></span>**D3DX10 \_ MESHOPT \_ ATTR \_ 排序**
</dt> <dd>

重新排列臉部以針對較少的屬性套件組合狀態變更和增強的 DrawSubset 效能進行優化。

</dd> <dt>

<span id="D3DX10_MESHOPT_VERTEX_CACHE"></span><span id="d3dx10_meshopt_vertex_cache"></span>**D3DX10 \_ MESHOPT \_ 頂點快取 \_**
</dt> <dd>

重新排列臉部以增加頂點快取的快取點擊率。

</dd> <dt>

<span id="D3DX10_MESHOPT_STRIP_REORDER"></span><span id="d3dx10_meshopt_strip_reorder"></span>**D3DX10 \_ MESHOPT \_ 帶狀 \_ 重新排序**
</dt> <dd>

重新排列臉部以將相鄰三角形的最大長度重新排序。

</dd> <dt>

<span id="D3DX10_MESHOPT_IGNORE_VERTS"></span><span id="d3dx10_meshopt_ignore_verts"></span>**D3DX10 \_ MESHOPT \_ 忽略 \_ VERTS**
</dt> <dd>

僅將臉部優化;請勿將頂點優化。

</dd> <dt>

<span id="D3DX10_MESHOPT_DO_NOT_SPLIT"></span><span id="d3dx10_meshopt_do_not_split"></span>**D3DX10 \_ MESHOPT \_ 不 \_ \_ 分割**
</dt> <dd>

屬性排序時，請勿分割屬性群組之間共用的頂點。

</dd> <dt>

<span id="D3DX10_MESHOPT_DEVICE_INDEPENDENT"></span><span id="d3dx10_meshopt_device_independent"></span>**\_ \_ 獨立于 D3DX10 MESHOPT 裝置 \_**
</dt> <dd>

影響頂點快取大小。 使用此旗標可指定在舊版硬體上運作正常的預設頂點快取大小。

</dd> </dl>

## <a name="remarks"></a>備註

D3DXMESHOPT \_ STRIPREORDER 和 D3DXMESHOPT \_ VERTEXCACHE 優化旗標彼此互斥。

\_此列舉已移除 D3DXMESHOPT SHAREVB 旗標。 \_ \_ 在 D3DXMESH 中，請改用 D3DXMESH VB SHARE。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3DX10Mesh。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 列舉](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 





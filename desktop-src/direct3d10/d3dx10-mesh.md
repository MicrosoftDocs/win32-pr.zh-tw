---
description: D3DX10_MESH 列舉旗標，用來指定網格的建立選項。
ms.assetid: 1a5a6b3f-34f4-4338-9ffe-8f95f6f0c385
title: 'D3DX10_MESH 列舉 (D3DX10Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_MESH
api_type:
- HeaderDef
api_location:
- D3DX10Mesh.h
ms.openlocfilehash: 2659783b0443396508465f9498eec86950f825bc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105436"
---
# <a name="d3dx10_mesh-enumeration"></a>D3DX10 \_ 網格列舉

用來指定網格之建立選項的旗標。

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DX10_MESH { 
  D3DX10_MESH_32_BIT        = 0x001,
  D3DX10_MESH_GS_ADJACENCY  = 0x004
} D3DX10_MESH, *LPD3DX10_MESH;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="D3DX10_MESH_32_BIT"></span><span id="d3dx10_mesh_32_bit"></span>**D3DX10 \_ 網格 \_ 32 \_ 位**
</dt> <dd>

網格有32位的索引，而不是16位的索引。 請參閱＜備註＞。

</dd> <dt>

<span id="D3DX10_MESH_GS_ADJACENCY"></span><span id="d3dx10_mesh_gs_adjacency"></span>**D3DX10 \_ 網格 \_ GS \_ 相鄰**
</dt> <dd>

指示網格包含幾何著色器的相鄰資料。

</dd> </dl>

## <a name="remarks"></a>備註

32位網格 (D3DXMESH 32 位 \_) 理論上可支援 (2 ³²) -1 臉部和頂點。 不過，為在32位作業系統上大的網狀架構配置記憶體並不實用。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3DX10Mesh。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 列舉](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 





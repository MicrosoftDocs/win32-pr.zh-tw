---
description: 指定要從裝置捨棄哪些網格資料片段。 搭配 ID3DX10Mesh 使用：:D iscard。
ms.assetid: 8b3c22ab-1337-4a66-ae32-17bd1b73f624
title: 'D3DX10_MESH_DISCARD_FLAGS 列舉 (D3DX10Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_MESH_DISCARD_FLAGS
api_type:
- HeaderDef
api_location:
- D3DX10Mesh.h
ms.openlocfilehash: d4b98550a2f3a896ed7b99f3e16f33a399a58035497e44420709ee8a0726901b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119989468"
---
# <a name="d3dx10_mesh_discard_flags-enumeration"></a>D3DX10 \_ 網格 \_ 捨棄 \_ 旗標列舉

指定要從裝置捨棄哪些網格資料片段。 搭配 [**ID3DX10Mesh 使用：:D iscard**](id3dx10mesh-discard.md)。

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DX10_MESH_DISCARD_FLAGS { 
  D3DX10_MESH_DISCARD_ATTRIBUTE_BUFFER  = 0x01,
  D3DX10_MESH_DISCARD_ATTRIBUTE_TABLE   = 0x02,
  D3DX10_MESH_DISCARD_POINTREPS         = 0x04,
  D3DX10_MESH_DISCARD_ADJACENCY         = 0x08,
  D3DX10_MESH_DISCARD_DEVICE_BUFFERS    = 0x10
} D3DX10_MESH_DISCARD_FLAGS, *LPD3DX10_MESH_DISCARD_FLAGS;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="D3DX10_MESH_DISCARD_ATTRIBUTE_BUFFER"></span><span id="d3dx10_mesh_discard_attribute_buffer"></span>**D3DX10 \_ 網格 \_ 捨棄 \_ 屬性 \_ 緩衝區**
</dt> <dd>

捨棄屬性緩衝區。

</dd> <dt>

<span id="D3DX10_MESH_DISCARD_ATTRIBUTE_TABLE"></span><span id="d3dx10_mesh_discard_attribute_table"></span>**D3DX10 \_ 網格 \_ 捨棄 \_ 屬性 \_ 表**
</dt> <dd>

捨棄屬性資料表。

</dd> <dt>

<span id="D3DX10_MESH_DISCARD_POINTREPS"></span><span id="d3dx10_mesh_discard_pointreps"></span>**D3DX10 \_ 網格 \_ 捨棄 \_ POINTREPS**
</dt> <dd>

捨棄指標代表緩衝區。

</dd> <dt>

<span id="D3DX10_MESH_DISCARD_ADJACENCY"></span><span id="d3dx10_mesh_discard_adjacency"></span>**D3DX10 \_ 網格 \_ 捨棄 \_ 相鄰**
</dt> <dd>

捨棄相鄰緩衝區。

</dd> <dt>

<span id="D3DX10_MESH_DISCARD_DEVICE_BUFFERS"></span><span id="d3dx10_mesh_discard_device_buffers"></span>**D3DX10 \_ 網格 \_ 捨棄 \_ 裝置 \_ 緩衝區**
</dt> <dd>

使用 [**ID3DX10Mesh：： CommitToDevice**](id3dx10mesh-committodevice.md)) 捨棄認可至裝置 (的緩衝區。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3DX10Mesh。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 列舉](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 





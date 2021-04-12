---
description: 將頂點焊接在一起的選項。
ms.assetid: e73af63d-ed02-4fbc-8386-e8a40b0465ea
title: 'D3DXWELDEPSILONSFLAGS 列舉 (D3dx9mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _D3DXWELDEPSILONSFLAGS
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 9e67c8b0f0bf93c9da181a5bba9a694525bd9819
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322992"
---
# <a name="d3dxweldepsilonsflags-enumeration"></a>D3DXWELDEPSILONSFLAGS 列舉

將頂點焊接在一起的選項。

## <a name="syntax"></a>Syntax


```C++
enum _D3DXWELDEPSILONSFLAGS {
  D3DXWELDEPSILONS_WELDALL              = 1, 
  D3DXWELDEPSILONS_WELDPARTIALMATCHES   = 2, 
  D3DXWELDEPSILONS_DONOTREMOVEVERTICES  = 4, 
  D3DXWELDEPSILONS_DONOTSPLIT           = 8 

};
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="D3DXWELDEPSILONS_WELDALL"></span><span id="d3dxweldepsilons_weldall"></span>**D3DXWELDEPSILONS \_ WELDALL**
</dt> <dd>

將位於相同位置的所有頂點焊接在一起。 使用這個旗標可避免頂點元件之間的 epsilon 比較。

</dd> <dt>

<span id="D3DXWELDEPSILONS_WELDPARTIALMATCHES"></span><span id="d3dxweldepsilons_weldpartialmatches"></span>**D3DXWELDEPSILONS \_ WELDPARTIALMATCHES**
</dt> <dd>

如果指定的頂點元件在 epsilon 內，請修改部分相符的頂點，使這兩個元件相同。 如果所有元件相等，請移除其中一個頂點。

</dd> <dt>

<span id="D3DXWELDEPSILONS_DONOTREMOVEVERTICES"></span><span id="d3dxweldepsilons_donotremovevertices"></span>**D3DXWELDEPSILONS \_ DONOTREMOVEVERTICES**
</dt> <dd>

指示焊縫只允許修改頂點，而不會移除。 只有在設定 D3DXWELDEPSILONS WELDPARTIALMATCHES 時，此旗標才有效 \_ 。 將頂點修改為相等，但不允許移除頂點會很有用。

</dd> <dt>

<span id="D3DXWELDEPSILONS_DONOTSPLIT"></span><span id="d3dxweldepsilons_donotsplit"></span>**D3DXWELDEPSILONS \_ DONOTSPLIT**
</dt> <dd>

指示焊縫不要分割位於不同屬性群組中的頂點。 使用 D3DXMESHOPT ATTRSORT 旗標呼叫 [**ID3DXMesh：： Optimize**](id3dxmesh--optimize.md) 方法時 \_ ， \_ 也會設定 D3DXMESHOPT DONOTSPLIT 旗標。 設定此旗標可能會減緩軟體頂點處理。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx9mesh。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 列舉](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[**D3DXWeldVertices**](d3dxweldvertices.md)
</dt> </dl>

 

 





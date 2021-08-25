---
description: 定義要在頂點上執行的作業，以準備進行網格清理。
ms.assetid: f222acaa-fa82-4591-b7c2-b520cb648ed5
title: 'D3DXCLEANTYPE 列舉 (D3dx9mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCLEANTYPE
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 2517c59d5505a8f2892ef0aee1d3884b8d489625637002d6e69a4f86434237fd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894108"
---
# <a name="d3dxcleantype-enumeration"></a>D3DXCLEANTYPE 列舉

定義要在頂點上執行的作業，以準備進行網格清理。

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DXCLEANTYPE { 
  D3DXCLEAN_BACKFACING      = 1,
  D3DXCLEAN_BOWTIES         = 2,
  D3DXCLEAN_SKINNING        = D3DXCLEAN_BACKFACING,
  D3DXCLEAN_OPTIMIZATION    = D3DXCLEAN_BACKFACING,
  D3DXCLEAN_SIMPLIFICATION  = D3DXCLEAN_BACKFACING | D3DXCLEAN_BOWTIES
} D3DXCLEANTYPE, *LPD3DXCLEANTYPE;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="D3DXCLEAN_BACKFACING"></span><span id="d3dxclean_backfacing"></span>**D3DXCLEAN \_ BACKFACING**
</dt> <dd>

共用相同頂點索引的合併三角形，但以相反方向指向的臉部法線 () 的回溯三角形。 除非三角形未藉由新增複寫頂點來分割，否則兩個三角形的網狀相鄰資料可能會發生衝突。

</dd> <dt>

<span id="D3DXCLEAN_BOWTIES"></span><span id="d3dxclean_bowties"></span>**D3DXCLEAN \_ BOWTIES**
</dt> <dd>

如果頂點是兩個三角形風扇的頂點 () ，而網格操作將會影響其中一個風扇，然後將共用頂點分割成兩個新頂點。 Bowties 可能會對移除頂點的作業（例如網格簡化）造成問題，因為移除一個頂點會影響兩組不同的三角形。

</dd> <dt>

<span id="D3DXCLEAN_SKINNING"></span><span id="d3dxclean_skinning"></span>**D3DXCLEAN \_ 外觀**
</dt> <dd>

使用此旗標來防止在設定網格操作時進行無限迴圈。

</dd> <dt>

<span id="D3DXCLEAN_OPTIMIZATION"></span><span id="d3dxclean_optimization"></span>**D3DXCLEAN \_ 優化**
</dt> <dd>

使用此旗標來防止網格優化作業期間的無限迴圈。

</dd> <dt>

<span id="D3DXCLEAN_SIMPLIFICATION"></span><span id="d3dxclean_simplification"></span>**D3DXCLEAN \_ 簡化**
</dt> <dd>

使用此旗標來防止網格簡化作業期間的無限迴圈。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx9mesh。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 列舉](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 





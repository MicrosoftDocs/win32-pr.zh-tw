---
description: D3DXQUATERNION 結構 (D3DX10Math) -描述四元數。
ms.assetid: e6cb45b2-3132-4315-b02d-a3dfc444f8cc
title: 'D3DXQUATERNION 結構 (D3DX10Math .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQUATERNION
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: dac880607cf482b409c407b43992747af4aa39a9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103246"
---
# <a name="d3dxquaternion-structure-d3dx10mathh"></a>D3DXQUATERNION 結構 (D3DX10Math .h) 

描述四元數。

## <a name="syntax"></a>語法


```C++
typedef struct D3DXQUATERNION {
  FLOAT x;
  FLOAT y;
  FLOAT z;
  FLOAT w;
} D3DXQUATERNION, *LPD3DXQUATERNION;
```



## <a name="members"></a>成員

<dl> <dt>

**x**
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

X 元件。

</dd> <dt>

**y**
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Y 元件。

</dd> <dt>

**Z**
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Z 元件。

</dd> <dt>

**w**
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

W 元件。

</dd> </dl>

## <a name="remarks"></a>備註

四元數會將第四個元素新增至 \[ 定義向量的 x、y、z \] 值，進而產生任意的4d 向量。 但是，下列說明單元四元數的每個元素如何與軸角度旋轉相關聯 (其中 q 代表單位四元數 (x、y、z、w) 、軸已正規化，而 theta 則是所需的 y 軸) 的 CCW 旋轉：


```
q.x = sin(theta/2) * axis.x
q.y = sin(theta/2) * axis.y
q.z = sin(theta/2) * axis.z
q.w = cos(theta/2)
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3DX10Math。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 結構](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 

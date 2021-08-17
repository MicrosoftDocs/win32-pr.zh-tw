---
description: 定義矩形。
ms.assetid: a8590411-fd34-4048-a41f-b4155d955573
title: 'D3DRECT 結構 (D3D9Types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DRECT
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 5e202ae058cdc30b79e2cc579a064b597d0013f7447e70f0fd6d996d9740a830
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117732282"
---
# <a name="d3drect-structure"></a>D3DRECT 結構

定義矩形。

## <a name="syntax"></a>語法


```C++
typedef struct D3DRECT {
  LONG x1;
  LONG y1;
  LONG x2;
  LONG y2;
} D3DRECT;
```



## <a name="members"></a>成員

<dl> <dt>

**x1**
</dt> <dd>

類型： **[ **LONG**](../winprog/windows-data-types.md)**

</dd> <dd>

矩形左上角的 X 座標。

</dd> <dt>

**y1**
</dt> <dd>

類型： **[ **LONG**](../winprog/windows-data-types.md)**

</dd> <dd>

矩形左上角的 Y 座標。

</dd> <dt>

**x2**
</dt> <dd>

類型： **[ **LONG**](../winprog/windows-data-types.md)**

</dd> <dd>

矩形右下角的 x 座標。

</dd> <dt>

**y2**
</dt> <dd>

類型： **[ **LONG**](../winprog/windows-data-types.md)**

</dd> <dd>

矩形右下角的 y 座標。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3D9Types。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 結構](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**清除**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear)
</dt> </dl>

 

 

---
description: 定義磁片區。
ms.assetid: 415a96bc-1621-4691-b87a-98ca22f0bf07
title: 'D3DBOX 結構 (D3D9Types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DBOX
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 9b7e01641348594e962f546a431700db799600a08571bbb7cfaf13396e671036
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118805511"
---
# <a name="d3dbox-structure"></a>D3DBOX 結構

定義磁片區。

## <a name="syntax"></a>語法


```C++
typedef struct D3DBOX {
  UINT Left;
  UINT Top;
  UINT Right;
  UINT Bottom;
  UINT Front;
  UINT Back;
} D3DBOX, *LPD3DBOX;
```



## <a name="members"></a>成員

<dl> <dt>

**離開**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

方塊左邊的位置（X 軸）。

</dd> <dt>

**前幾個**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Y 軸上方塊頂端的位置。

</dd> <dt>

**對**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

X 軸右邊方塊的位置。

</dd> <dt>

**下層**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Y 軸上方塊底部的位置。

</dd> <dt>

**Front**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Z 軸上方塊前端的位置。

</dd> <dt>

**上一步**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Z 軸上方塊背面的位置。

</dd> </dl>

## <a name="remarks"></a>備註

**D3DBOX** 包含左、上和前邊緣;但是，不包含右邊、下邊緣和後端邊緣。 例如，一個全100單元的方塊，並從0開始 (因此，包括最多和包含99的點) 會以0代表左邊的成員，並針對右邊的成員以100的值表示。 請注意，不會針對右邊的成員使用99的值。

針對 **D3DBOX** 觀察到的順序限制是由左到右、由上到下，以及前端。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3D9Types。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 結構](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 

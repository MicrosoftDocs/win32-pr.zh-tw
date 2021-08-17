---
description: 描述動畫播放軌，並指定在指定時間的軌跡粗細、速度和位置。
ms.assetid: f1469b6f-861f-4b7d-a187-933092a5d257
title: 'D3DXTRACK_DESC 結構 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTRACK_DESC
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: cddabb3ea79951e35831c2cdc32e11baeb5c7c1c4ce174fd29d9382edb391953
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117731115"
---
# <a name="d3dxtrack_desc-structure"></a>D3DXTRACK \_ DESC 結構

描述動畫播放軌，並指定在指定時間的軌跡粗細、速度和位置。

## <a name="syntax"></a>語法


```C++
typedef struct D3DXTRACK_DESC {
  D3DXPRIORITY_TYPE Priority;
  FLOAT             Weight;
  FLOAT             Speed;
  DOUBLE            Position;
  BOOL              Enable;
} D3DXTRACK_DESC, *LPD3DXTRACK_DESC;
```



## <a name="members"></a>成員

<dl> <dt>

**優先順序**
</dt> <dd>

類型： **[ **D3DXPRIORITY \_ 類型**](./d3dxpriority-type.md)**

</dd> <dd>

優先權類型，如 [**D3DXPRIORITY \_ 類型**](./d3dxpriority-type.md)中所定義。

</dd> <dt>

**Weight**
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

加權值。 權數會決定此追蹤與其他追蹤的比例。

</dd> <dt>

**速度**
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

速度值。 這種方式類似于乘數，可用來調整追蹤的期間。

</dd> <dt>

**位置**
</dt> <dd>

類型： **[ **DOUBLE**](../winprog/windows-data-types.md)**

</dd> <dd>

曲目的時間位置，以目前動畫集的當地時間範圍為限。

</dd> <dt>

**啟用**
</dt> <dd>

類型： **[ **BOOL**](../winprog/windows-data-types.md)**

</dd> <dd>

追蹤啟用/停用。 若要啟用，請將設定為 **TRUE**。 若要停用，請設定為 **FALSE**。

</dd> </dl>

## <a name="remarks"></a>備註

具有相同優先權的追蹤會混合在一起，而這兩個結果值接著會使用優先順序 blend 因數進行混合。 播放軌必須有一個動畫集 (另存) 與其相關聯。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx9anim。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 結構](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 

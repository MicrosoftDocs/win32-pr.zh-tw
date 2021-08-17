---
description: 描述動畫事件。
ms.assetid: ddcdd143-bcbd-450c-a4df-914797a562e6
title: 'D3DXEVENT_DESC 結構 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXEVENT_DESC
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: d5569eccd5b99939cd50797ee73593ce5a2bfc8ddd60236e05218ddcca7f4383
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117731806"
---
# <a name="d3dxevent_desc-structure"></a>D3DXEVENT \_ DESC 結構

描述動畫事件。

## <a name="syntax"></a>語法


```C++
typedef struct D3DXEVENT_DESC {
  D3DXEVENT_TYPE      Type;
  UINT                Track;
  DOUBLE              StartTime;
  DOUBLE              Duration;
  D3DXTRANSITION_TYPE Transition;
  union {
    FLOAT  Weight;
    FLOAT  Speed;
    DOUBLE Position;
    BOOL   Enable;
  };
} D3DXEVENT_DESC, *LPD3DXEVENT_DESC;
```



## <a name="members"></a>成員

<dl> <dt>

**類型**
</dt> <dd>

類型： **[ **D3DXEVENT \_ 類型**](./d3dxevent-type.md)**

</dd> <dd>

事件種類，如 [**D3DXEVENT \_ 類型**](./d3dxevent-type.md)中所定義。

</dd> <dt>

**Track**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

事件追蹤識別碼。

</dd> <dt>

**StartTime**
</dt> <dd>

類型： **[ **DOUBLE**](../winprog/windows-data-types.md)**

</dd> <dd>

全球時間的事件開始時間。

</dd> <dt>

**有效期間**
</dt> <dd>

類型： **[ **DOUBLE**](../winprog/windows-data-types.md)**

</dd> <dd>

全球時間事件的持續時間。

</dd> <dt>

**轉換**
</dt> <dd>

類型： **[ **D3DXTRANSITION \_ 類型**](./d3dxtransition-type.md)**

</dd> <dd>

事件的轉換樣式，如 [**D3DXTRANSITION \_ 類型**](./d3dxtransition-type.md)中所定義。

</dd> <dt>

**Weight**
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

追蹤事件的加權。

</dd> <dt>

**速度**
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

追蹤事件的速度。

</dd> <dt>

**位置**
</dt> <dd>

類型： **[ **DOUBLE**](../winprog/windows-data-types.md)**

</dd> <dd>

追蹤事件的位置。

</dd> <dt>

**啟用**
</dt> <dd>

類型： **[ **BOOL**](../winprog/windows-data-types.md)**

</dd> <dd>

啟用旗標。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx9anim。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 結構](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 

---
description: 定義光源類型。
ms.assetid: 90ad82d3-ffa8-42bb-9d9c-cf28a416c32d
title: 'D3DLIGHTTYPE 列舉 (D3D9Types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DLIGHTTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 83c94db3126443f757f01a69d7d773417f70683a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106976715"
---
# <a name="d3dlighttype-enumeration"></a>D3DLIGHTTYPE 列舉

定義光源類型。

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DLIGHTTYPE { 
  D3DLIGHT_POINT        = 1,
  D3DLIGHT_SPOT         = 2,
  D3DLIGHT_DIRECTIONAL  = 3,
  D3DLIGHT_FORCE_DWORD  = 0x7fffffff
} D3DLIGHTTYPE, *LPD3DLIGHTTYPE;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="D3DLIGHT_POINT"></span><span id="d3dlight_point"></span>**D3DLIGHT \_ 點**
</dt> <dd>

Light 是點來源。 光線在空間中有一個位置，而 radiates 光的方向。

</dd> <dt>

<span id="D3DLIGHT_SPOT"></span><span id="d3dlight_spot"></span>**D3DLIGHT \_ 位置**
</dt> <dd>

Light 是焦點來源。 這種光線就像點燈，只不過照明僅限於錐形。 此光線類型具有方向和數個其他參數，可決定所產生之錐形的形狀。 如需這些參數的詳細資訊，請參閱 [**D3DLIGHT9**](d3dlight9.md) 結構。

</dd> <dt>

<span id="D3DLIGHT_DIRECTIONAL"></span><span id="d3dlight_directional"></span>**D3DLIGHT \_ 方向**
</dt> <dd>

Light 是方向性光源。 這相當於使用無限距離的點光源來源。

</dd> <dt>

<span id="D3DLIGHT_FORCE_DWORD"></span><span id="d3dlight_force_dword"></span>**D3DLIGHT \_ 強制 \_ DWORD**
</dt> <dd>

強制此列舉的大小編譯為32位。 如果沒有這個值，某些編譯器會允許此列舉編譯成32位以外的大小。 不使用這個值。

</dd> </dl>

## <a name="remarks"></a>備註

方向光源的速度比點光源稍微快一點，但點燈看起來比較好。 聚光燈提供有趣的視覺效果，但需要花費很多時間來計算。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3D9Types。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 列舉](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DLIGHT9**](d3dlight9.md)
</dt> </dl>

 

 





---
description: 定義要指派動畫播放軌的優先順序類型。
ms.assetid: 7bd83e31-09c4-4376-a22d-ed8023b78e84
title: 'D3DXPRIORITY_TYPE 列舉 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPRIORITY_TYPE
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 5e6d82807cbd0e93e7a1127db80726c0ec06b5da
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104386449"
---
# <a name="d3dxpriority_type-enumeration"></a>D3DXPRIORITY \_ 類型列舉

定義要指派動畫播放軌的優先順序類型。

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DXPRIORITY_TYPE { 
  D3DXPRIORITY_LOW          = 0,
  D3DXPRIORITY_HIGH         = 1,
  D3DXPRIORITY_FORCE_DWORD  = 0x7fffffff
} D3DXPRIORITY_TYPE, *LPD3DXPRIORITY_TYPE;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="D3DXPRIORITY_LOW"></span><span id="d3dxpriority_low"></span>**D3DXPRIORITY \_ 低**
</dt> <dd>

在低優先順序 blend 與高優先順序 blend 混合之前，應該先混合所有低優先順序的追蹤。

</dd> <dt>

<span id="D3DXPRIORITY_HIGH"></span><span id="d3dxpriority_high"></span>**D3DXPRIORITY \_ HIGH**
</dt> <dd>

在高優先順序 blend 與低優先順序 blend 混合之前，應該先混合所有高優先順序的追蹤。

</dd> <dt>

<span id="D3DXPRIORITY_FORCE_DWORD"></span><span id="d3dxpriority_force_dword"></span>**D3DXPRIORITY \_ 強制 \_ DWORD**
</dt> <dd>

強制此列舉的大小編譯為32位。 如果沒有這個值，某些編譯器會允許此列舉編譯成32位以外的大小。 不使用這個值。

</dd> </dl>

## <a name="remarks"></a>備註

具有相同優先權的追蹤會混合在一起，而這兩個結果值接著會使用優先順序 blend 因數進行混合。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx9anim。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 列舉](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 





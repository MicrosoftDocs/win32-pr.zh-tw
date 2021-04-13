---
description: 定義描述霧化模式的常數。
ms.assetid: cd83c914-bc1d-4f66-b5a6-7984b7ec52cd
title: 'D3DFOGMODE 列舉 (D3D9Types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DFOGMODE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 8436a52edbb9460c6945c1526513629939ec444b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323072"
---
# <a name="d3dfogmode-enumeration"></a>D3DFOGMODE 列舉

定義描述霧化模式的常數。

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DFOGMODE { 
  D3DFOG_NONE         = 0,
  D3DFOG_EXP          = 1,
  D3DFOG_EXP2         = 2,
  D3DFOG_LINEAR       = 3,
  D3DFOG_FORCE_DWORD  = 0x7fffffff
} D3DFOGMODE, *LPD3DFOGMODE;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="D3DFOG_NONE"></span><span id="d3dfog_none"></span>**D3DFOG \_ 無**
</dt> <dd>

沒有霧化效果。

</dd> <dt>

<span id="D3DFOG_EXP"></span><span id="d3dfog_exp"></span>**D3DFOG \_ EXP**
</dt> <dd>

根據下列公式，會以指數方式增強霧化效果。

![霧化的公式-效果強度](images/fogexp.png)

</dd> <dt>

<span id="D3DFOG_EXP2"></span><span id="d3dfog_exp2"></span>**D3DFOG \_ EXP2**
</dt> <dd>

霧化效果會根據下列公式，以指數方式從距離的平方開始增強。

![以距離為基礎的霧化效果濃度公式](images/fogexp2.png)

</dd> <dt>

<span id="D3DFOG_LINEAR"></span><span id="d3dfog_linear"></span>**D3DFOG \_ 線性**
</dt> <dd>

您可以根據下列公式，開始與結束點之間的霧化效果呈線性增加。

![以開始和結束點為基礎之霧化效果濃度的公式](images/fogliner.png)

這是目前唯一支援的霧化模式。

</dd> <dt>

<span id="D3DFOG_FORCE_DWORD"></span><span id="d3dfog_force_dword"></span>**D3DFOG \_ 強制 \_ DWORD**
</dt> <dd>

強制此列舉的大小編譯為32位。 如果沒有這個值，某些編譯器會允許此列舉編譯成32位以外的大小。 不使用這個值。

</dd> </dl>

## <a name="remarks"></a>備註

D3DRS \_ FOGTABLEMODE 和 D3DRS FOGVERTEXMODE 轉譯狀態會使用這個列舉型別中的值 \_ 。

霧化可視為可見度的量值：霧化方程式所產生的霧化值越低，物件就越不可見。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3D9Types。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 列舉](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)
</dt> </dl>

 

 

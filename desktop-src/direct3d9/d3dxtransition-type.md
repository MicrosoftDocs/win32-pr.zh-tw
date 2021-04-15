---
description: 定義網格動畫值之間的轉換樣式。
ms.assetid: 4416ef28-ba6b-47ca-be7d-831daad619e5
title: 'D3DXTRANSITION_TYPE 列舉 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTRANSITION_TYPE
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 0ca6ef7f9dcee8e865a1cd4089aecd1bc239d5d4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946086"
---
# <a name="d3dxtransition_type-enumeration"></a>D3DXTRANSITION \_ 類型列舉

定義網格動畫值之間的轉換樣式。

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DXTRANSITION_TYPE { 
  D3DXTRANSITION_LINEAR         = 0x000,
  D3DXTRANSITION_EASEINEASEOUT  = 0x001,
  D3DXTRANSITION_FORCE_DWORD    = 0x7fffffff
} D3DXTRANSITION_TYPE, *LPD3DXTRANSITION_TYPE;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="D3DXTRANSITION_LINEAR"></span><span id="d3dxtransition_linear"></span>**D3DXTRANSITION \_ 線性**
</dt> <dd>

值之間的線性轉換。

</dd> <dt>

<span id="D3DXTRANSITION_EASEINEASEOUT"></span><span id="d3dxtransition_easeineaseout"></span>**D3DXTRANSITION \_ EASEINEASEOUT**
</dt> <dd>

在值之間進行輕鬆、容易放大的曲線轉換。

</dd> <dt>

<span id="D3DXTRANSITION_FORCE_DWORD"></span><span id="d3dxtransition_force_dword"></span>**D3DXTRANSITION \_ 強制 \_ DWORD**
</dt> <dd>

強制此列舉的大小編譯為32位。 如果沒有這個值，某些編譯器會允許此列舉編譯成32位以外的大小。 不使用這個值。

</dd> </dl>

## <a name="remarks"></a>備註

從輕鬆放大到簡化的遞增計算方式如下所示：

<dl> Q (t) = 2 (x-y) t ³ + 3 (y-x) t ² + x  
</dl>

其中的斜坡是函數 Q (t) 具有下列屬性：

-   Q (t) 是三個曲線。
-   問 (t) 在 x 和 y 之間進行插補，作為 t 範圍從0到1。
-   Q (t) 是在 t = 0 和 t = 1 時水準。

這會以數學方式轉譯成：

<dl> 問 (t) = At ³ + Bt ² + Ct + D (因此，Q ' (t) = 3At ² + 2Bt + C)   
2a) Q (0) = x  
2b) Q (1) = y  
3a) Q ' (0) = 0  
3b) Q ' (1) = 0  
</dl>

解決 A、B、C、D：

<dl> D = x 從 2a)  (  
從 3a) 的 C = 0 (  
3A + 2B = 0 (自 3b)   
A + B = y x (從2b 和 D = x)   
</dl>

因此：

<dl> A = 2 (x-y) ，B = 3 (y-x) ，C = 0，D = x  
</dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx9anim。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 列舉](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 





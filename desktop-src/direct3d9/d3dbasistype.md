---
description: 定義高序位修補程式介面的基礎類型。
ms.assetid: 18c31c77-7ba3-449c-af4a-717b8c1dced1
title: 'D3DBASISTYPE 列舉 (D3D9Types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DBASISTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 7e166f56aa2625c868d3e2e2223efbb577e05bf5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104116189"
---
# <a name="d3dbasistype-enumeration"></a>D3DBASISTYPE 列舉

定義高序位修補程式介面的基礎類型。

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DBASISTYPE { 
  D3DBASIS_BEZIER       = 0,
  D3DBASIS_BSPLINE      = 1,
  D3DBASIS_CATMULL_ROM  = 2,
  D3DBASIS_FORCE_DWORD  = 0x7fffffff
} D3DBASISTYPE, *LPD3DBASISTYPE;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="D3DBASIS_BEZIER"></span><span id="d3dbasis_bezier"></span>**D3DBASIS \_ 貝塞爾**
</dt> <dd>

輸入頂點會被視為一連串的貝塞爾修補程式。 指定的頂點數目必須可被4整除。 這項準則以外的網格部分將不會呈現。 在每次呼叫所轉譯之介面內部的子修補程式之間，會採用完整的持續性。 只保證每個子修補角落角落的頂點都位於產生的介面上。

</dd> <dt>

<span id="D3DBASIS_BSPLINE"></span><span id="d3dbasis_bspline"></span>**D3DBASIS \_ BSPLINE**
</dt> <dd>

輸入頂點會被視為 B 曲線介面的控制點。 轉譯的 apertures 數目會比該方向的 apertures 數少兩倍。 一般情況下，產生的介面不包含指定的控制項頂點。

</dd> <dt>

<span id="D3DBASIS_CATMULL_ROM"></span><span id="d3dbasis_catmull_rom"></span>**D3DBASIS \_ CATMULL \_ ROM**
</dt> <dd>

插插值基礎會定義介面，讓介面能通過指定的所有輸入頂點。 在 DirectX 8 中，這是 D3DBASIS 的 \_ 插補。

</dd> <dt>

<span id="D3DBASIS_FORCE_DWORD"></span><span id="d3dbasis_force_dword"></span>**D3DBASIS \_ 強制 \_ DWORD**
</dt> <dd>

強制此列舉的大小編譯為32位。 如果沒有這個值，某些編譯器會允許此列舉編譯成32位以外的大小。 不使用這個值。

</dd> </dl>

## <a name="remarks"></a>備註

**D3DBASISTYPE** 的成員會指定在鑲嵌期間用來評估高序位修補程式介面基本的形式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3D9Types。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 列舉](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DRECTPATCH \_ 資訊**](d3drectpatch-info.md)
</dt> <dt>

[**D3DTRIPATCH \_ 資訊**](d3dtripatch-info.md)
</dt> </dl>

 

 





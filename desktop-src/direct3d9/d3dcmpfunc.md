---
description: 定義支援的比較函數。
ms.assetid: 999af3eb-a208-4312-acee-373192ea69e4
title: 'D3DCMPFUNC 列舉 (D3D9Types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCMPFUNC
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 1fa8d0c9288e6c0d516e7fc9b8a07237f553dd6c86072f1895edf9a79c297077
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989106"
---
# <a name="d3dcmpfunc-enumeration"></a>D3DCMPFUNC 列舉

定義支援的比較函數。

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DCMPFUNC { 
  D3DCMP_NEVER         = 1,
  D3DCMP_LESS          = 2,
  D3DCMP_EQUAL         = 3,
  D3DCMP_LESSEQUAL     = 4,
  D3DCMP_GREATER       = 5,
  D3DCMP_NOTEQUAL      = 6,
  D3DCMP_GREATEREQUAL  = 7,
  D3DCMP_ALWAYS        = 8,
  D3DCMP_FORCE_DWORD   = 0x7fffffff
} D3DCMPFUNC, *LPD3DCMPFUNC;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="D3DCMP_NEVER"></span><span id="d3dcmp_never"></span>**D3DCMP \_ 永不**
</dt> <dd>

一律會使測試失敗。

</dd> <dt>

<span id="D3DCMP_LESS"></span><span id="d3dcmp_less"></span>**D3DCMP \_ LESS**
</dt> <dd>

如果值小於目前圖元的值，則接受新的圖元。

</dd> <dt>

<span id="D3DCMP_EQUAL"></span><span id="d3dcmp_equal"></span>**D3DCMP \_ 相等**
</dt> <dd>

如果圖元值等於目前圖元的值，則接受新的圖元。

</dd> <dt>

<span id="D3DCMP_LESSEQUAL"></span><span id="d3dcmp_lessequal"></span>**D3DCMP \_ LESSEQUAL**
</dt> <dd>

如果值小於或等於目前圖元的值，則接受新的圖元。

</dd> <dt>

<span id="D3DCMP_GREATER"></span><span id="d3dcmp_greater"></span>**D3DCMP \_ 更大**
</dt> <dd>

如果其值大於目前圖元的值，則接受新的圖元。

</dd> <dt>

<span id="D3DCMP_NOTEQUAL"></span><span id="d3dcmp_notequal"></span>**D3DCMP \_ NOTEQUAL**
</dt> <dd>

如果其值不等於目前圖元的值，則接受新的圖元。

</dd> <dt>

<span id="D3DCMP_GREATEREQUAL"></span><span id="d3dcmp_greaterequal"></span>**D3DCMP \_ GREATEREQUAL**
</dt> <dd>

如果其值大於或等於目前圖元的值，則接受新的圖元。

</dd> <dt>

<span id="D3DCMP_ALWAYS"></span><span id="d3dcmp_always"></span>**\_一律 D3DCMP**
</dt> <dd>

一律傳遞測試。

</dd> <dt>

<span id="D3DCMP_FORCE_DWORD"></span><span id="d3dcmp_force_dword"></span>**D3DCMP \_ 強制 \_ DWORD**
</dt> <dd>

強制此列舉的大小編譯為32位。 如果沒有這個值，某些編譯器會允許此列舉編譯成32位以外的大小。 不使用這個值。

</dd> </dl>

## <a name="remarks"></a>備註

此列舉型別中的值會定義 D3DRS \_ ZFUNC、D3DRS \_ ALPHAFUNC 和 D3DRS STENCILFUNC 轉譯狀態的支援比較函數 \_ 。

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

 

 

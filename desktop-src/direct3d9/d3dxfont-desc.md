---
description: 定義字型的屬性。
ms.assetid: 6f456f26-3410-4205-a013-e3c12bf0feb1
title: 'D3DXFONT_DESC 結構 (D3dx9core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFONT_DESC
api_type:
- HeaderDef
api_location:
- d3dx9core.h
ms.openlocfilehash: d7c142787e4e4fac5be53763a3c19fd86a27efd9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106992715"
---
# <a name="d3dxfont_desc-structure"></a>D3DXFONT \_ DESC 結構

定義字型的屬性。

## <a name="syntax"></a>語法


```C++
typedef struct D3DXFONT_DESC {
  INT   Height;
  UINT  Width;
  UINT  Weight;
  UINT  MipLevels;
  BOOL  Italic;
  BYTE  CharSet;
  BYTE  OutputPrecision;
  BYTE  Quality;
  BYTE  PitchAndFamily;
  TCHAR FaceName;
} D3DXFONT_DESC, *LPD3DXFONT_DESC;
```



## <a name="members"></a>成員

<dl> <dt>

**高度**
</dt> <dd>

類型： **[ **INT**](../winprog/windows-data-types.md)**

</dd> <dd>

字型字元資料格或字元的高度（以邏輯單位表示）。

</dd> <dt>

**寬度**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

字型中字元的寬度（以邏輯單位表示）。

</dd> <dt>

**Weight**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

字型的權數，範圍介於0到1000之間。

</dd> <dt>

**MipLevels**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

要求的 mip 層級數目。 如果此值為零或 D3DX \_ 預設值，則會建立完整的 mipmap 鏈。 如果值為1，則紋理空間的對應方式會與螢幕空間相同。

</dd> <dt>

**斜體**
</dt> <dd>

類型： **[ **BOOL**](../winprog/windows-data-types.md)**

</dd> <dd>

針對斜體字型，設定為 **TRUE** 。

</dd> <dt>

**字元集**
</dt> <dd>

類型： **[**位元組**](../winprog/windows-data-types.md)**

</dd> <dd>

字元集。

</dd> <dt>

**OutputPrecision**
</dt> <dd>

類型： **[**位元組**](../winprog/windows-data-types.md)**

</dd> <dd>

輸出精確度。 輸出精確度定義輸出必須符合要求的字型高度、寬度、字元方向、行距、音調和字型類型的程度。

</dd> <dt>

**品質**
</dt> <dd>

類型： **[**位元組**](../winprog/windows-data-types.md)**

</dd> <dd>

輸出品質。

</dd> <dt>

**PitchAndFamily**
</dt> <dd>

類型： **[**位元組**](../winprog/windows-data-types.md)**

</dd> <dd>

字型的音調和系列。

</dd> <dt>

**FaceName**
</dt> <dd>

類型： **TCHAR**

</dd> <dd>

以 null 終止的字串，或指定字型字型名稱的字元。 字串的長度不能超過32個字元，包括結束的 null 字元。 如果 FaceName 是空字串，則會使用符合其他指定屬性的第一個字型。 如果編譯器設定需要 Unicode，則資料類型 TCHAR 會解析為 WCHAR;否則，資料型別會解析為 CHAR。 請參閱＜備註＞。

</dd> </dl>

## <a name="remarks"></a>備註

編譯器設定也會決定結構類型。 如果已定義 Unicode，D3DXFONT \_ DESC 結構類型會解析為 D3DXFONT \_ DESCW; 否則，結構類型會解析為 D3DXFONT \_ DESCA。

GDI [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) 結構中提供上述成員的可能值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx9core。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 結構](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**GetDesc**](id3dxfont--getdesc.md)
</dt> </dl>

 

 

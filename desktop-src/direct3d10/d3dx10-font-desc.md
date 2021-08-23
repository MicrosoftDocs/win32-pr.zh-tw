---
description: 定義字型屬性。
ms.assetid: 66e8a320-2b83-4766-a9a7-5571ee6c9f2a
title: 'D3DX10_FONT_DESC 結構 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_FONT_DESC
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: f3ee6dea032475eb94a723229751d9523c12d118f7319da8f0296cc8c8c42a2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634948"
---
# <a name="d3dx10_font_desc-structure"></a>D3DX10 \_ 字型 \_ DESC 結構

定義字型屬性。

## <a name="syntax"></a>語法


```C++
typedef struct D3DX10_FONT_DESC {
  INT   Height;
  UINT  Width;
  UINT  Weight;
  UINT  MipLevels;
  BOOL  Italic;
  BYTE  CharSet;
  BYTE  OutputPrecision;
  BYTE  Quality;
  BYTE  PitchAndFamily;
  TCHAR FaceName[LF_FACESIZE];
} D3DX10_FONT_DESC, *LPD3DX10_FONT_DESC;
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

要求的 mipmap 層級數目。 如果此值為零或 D3DX \_ 預設值，則會建立完整的 mipmap 鏈。 如果值為1，則紋理空間的對應方式會與螢幕空間相同。

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

**FaceName \[ LF \_ FACESIZE\]**
</dt> <dd>

類型： **TCHAR**

</dd> <dd>

以 Null 終止的字串，指定字型的字型名稱。 字串的長度不能超過32個字元，包括結束的 **Null** 字元。 如果 FaceName 是空字串，則會使用符合其他指定屬性的第一個字型。 如果編譯器設定需要 Unicode，則資料類型 TCHAR 會解析為 WCHAR;否則，資料型別會解析為 CHAR。 請參閱＜備註＞。

</dd> </dl>

## <a name="remarks"></a>備註

編譯器設定也會決定結構類型。 如果已定義 Unicode，D3DX10 \_ 字型 \_ DESC 結構類型會解析為 D3DX10 \_ 字型 \_ DESCW; 否則，結構類型會解析成 D3DX10 \_ 字型 \_ DESCA。

GDI [LOGFONT](/previous-versions//ms533931(v=vs.85)) 結構中提供上述成員的可能值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3DX10。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 結構](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 

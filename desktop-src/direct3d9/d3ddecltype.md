---
description: 定義頂點宣告資料類型。
ms.assetid: 993fc7e4-4752-4bce-82d0-0a034fdc69c0
title: 'D3DDECLTYPE 列舉 (D3D9Types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDECLTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 3edb3f936772a7265c627f10eeb7aeb4f461701e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322728"
---
# <a name="d3ddecltype-enumeration"></a>D3DDECLTYPE 列舉

定義頂點宣告資料類型。

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DDECLTYPE { 
  D3DDECLTYPE_FLOAT1     = 0,
  D3DDECLTYPE_FLOAT2     = 1,
  D3DDECLTYPE_FLOAT3     = 2,
  D3DDECLTYPE_FLOAT4     = 3,
  D3DDECLTYPE_D3DCOLOR   = 4,
  D3DDECLTYPE_UBYTE4     = 5,
  D3DDECLTYPE_SHORT2     = 6,
  D3DDECLTYPE_SHORT4     = 7,
  D3DDECLTYPE_UBYTE4N    = 8,
  D3DDECLTYPE_SHORT2N    = 9,
  D3DDECLTYPE_SHORT4N    = 10,
  D3DDECLTYPE_USHORT2N   = 11,
  D3DDECLTYPE_USHORT4N   = 12,
  D3DDECLTYPE_UDEC3      = 13,
  D3DDECLTYPE_DEC3N      = 14,
  D3DDECLTYPE_FLOAT16_2  = 15,
  D3DDECLTYPE_FLOAT16_4  = 16,
  D3DDECLTYPE_UNUSED     = 17
} D3DDECLTYPE, *LPD3DDECLTYPE;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="D3DDECLTYPE_FLOAT1"></span><span id="d3ddecltype_float1"></span>**D3DDECLTYPE \_ FLOAT1**
</dt> <dd>

一個元件 float 展開至 (浮點數、0、0、1) 。

</dd> <dt>

<span id="D3DDECLTYPE_FLOAT2"></span><span id="d3ddecltype_float2"></span>**D3DDECLTYPE \_ FLOAT2**
</dt> <dd>

雙元件 float 展開至 (浮點數、浮點數、0、1) 。

</dd> <dt>

<span id="D3DDECLTYPE_FLOAT3"></span><span id="d3ddecltype_float3"></span>**D3DDECLTYPE \_ FLOAT3**
</dt> <dd>

將三個元件 float 展開至 (float、float、float、1) 。

</dd> <dt>

<span id="D3DDECLTYPE_FLOAT4"></span><span id="d3ddecltype_float4"></span>**D3DDECLTYPE \_ FLOAT4**
</dt> <dd>

四個元件 float 展開至 (浮點數、浮點數、浮點數) 。

</dd> <dt>

<span id="D3DDECLTYPE_D3DCOLOR"></span><span id="d3ddecltype_d3dcolor"></span>**D3DDECLTYPE \_ D3DCOLOR**
</dt> <dd>

四個元件、已封裝、不帶正負號的位元組對應至0到1個範圍。 輸入是 [**D3DCOLOR**](d3dcolor.md) ，並已展開為 RGBA 順序。

</dd> <dt>

<span id="D3DDECLTYPE_UBYTE4"></span><span id="d3ddecltype_ubyte4"></span>**D3DDECLTYPE \_ UBYTE4**
</dt> <dd>

四個元件、不帶正負號的位元組。

</dd> <dt>

<span id="D3DDECLTYPE_SHORT2"></span><span id="d3ddecltype_short2"></span>**D3DDECLTYPE \_ SHORT2**
</dt> <dd>

雙元件的帶正負號的簡短擴充至 (值、值、0、1) 。

</dd> <dt>

<span id="D3DDECLTYPE_SHORT4"></span><span id="d3ddecltype_short4"></span>**D3DDECLTYPE \_ SHORT4**
</dt> <dd>

四個元件的帶正負號的簡短擴充至 (值、值、值、值) 。

</dd> <dt>

<span id="D3DDECLTYPE_UBYTE4N"></span><span id="d3ddecltype_ubyte4n"></span>**D3DDECLTYPE \_ UBYTE4N**
</dt> <dd>

四個元件的位元組，其中每個位元組都以正規化方式除以 255.0 f。

</dd> <dt>

<span id="D3DDECLTYPE_SHORT2N"></span><span id="d3ddecltype_short2n"></span>**D3DDECLTYPE \_ SHORT2N**
</dt> <dd>

正規化的兩個元件（帶正負號）會展開為 (第一個簡短/32767.0、第二個簡短/32767.0、0、1) 。

</dd> <dt>

<span id="D3DDECLTYPE_SHORT4N"></span><span id="d3ddecltype_short4n"></span>**D3DDECLTYPE \_ SHORT4N**
</dt> <dd>

正規化，四個元件的帶正負號的簡短，展開為 (first short/32767.0，第二個 short/32767.0，第三個簡短/32767.0，第四個 short/32767.0) 。

</dd> <dt>

<span id="D3DDECLTYPE_USHORT2N"></span><span id="d3ddecltype_ushort2n"></span>**D3DDECLTYPE \_ USHORT2N**
</dt> <dd>

正規化、雙元件、不帶正負號的簡短、展開為 (first short/65535.0、short short/65535.0、0、1) 。

</dd> <dt>

<span id="D3DDECLTYPE_USHORT4N"></span><span id="d3ddecltype_ushort4n"></span>**D3DDECLTYPE \_ USHORT4N**
</dt> <dd>

正規化、四個元件、不帶正負號的簡短、展開為 (first short/65535.0、second short/65535.0、第三個簡短/65535.0、第四個 short/65535.0) 。

</dd> <dt>

<span id="D3DDECLTYPE_UDEC3"></span><span id="d3ddecltype_udec3"></span>**D3DDECLTYPE \_ UDEC3**
</dt> <dd>

將三個元件、不帶正負號的 10 10 10 格式擴充為 (值、值、值、1) 。

</dd> <dt>

<span id="D3DDECLTYPE_DEC3N"></span><span id="d3ddecltype_dec3n"></span>**D3DDECLTYPE \_ DEC3N**
</dt> <dd>

三個元件、帶正負號的 10 10 10 格式正規化和展開為 (v \[ 0 \] /511.0、v \[ 1 \] /511.0、v \[ 2 \] /511.0、1) 。

</dd> <dt>

<span id="D3DDECLTYPE_FLOAT16_2"></span><span id="d3ddecltype_float16_2"></span>**D3DDECLTYPE \_ FLOAT16 \_ 2**
</dt> <dd>

雙元件、16位、浮點數展開至 (值、值、0、1) 。

</dd> <dt>

<span id="D3DDECLTYPE_FLOAT16_4"></span><span id="d3ddecltype_float16_4"></span>**D3DDECLTYPE \_ FLOAT16 \_ 4**
</dt> <dd>

四個元件、16位、浮點數展開至 (值、值、值、值) 。

</dd> <dt>

<span id="D3DDECLTYPE_UNUSED"></span><span id="d3ddecltype_unused"></span>**\_未使用 D3DDECLTYPE**
</dt> <dd>

宣告中的類型欄位未使用。 這是設計來與 D3DDECLMETHOD \_ UV 和 D3DDECLMETHOD LOOKUPPRESAMPLED 搭配使用 \_ 。

</dd> </dl>

## <a name="remarks"></a>備註

頂點資料是使用 [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) 結構的陣列來宣告。 陣列中的每個元素都包含一個頂點宣告資料類型。

使用 DirectX Cap 檢視器工具 (DXCapsViewer.exe) 來查看裝置支援的類型。 您可以從 DirectX SDK 取得此工具，並瞭解其相關資訊。 如需有關 DirectX SDK 的資訊，請參閱 [什麼是 DIRECTX sdk？](../directx-sdk--august-2009-.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3D9Types。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 列舉](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DDECLMETHOD**](./d3ddeclmethod.md)
</dt> </dl>

 

 

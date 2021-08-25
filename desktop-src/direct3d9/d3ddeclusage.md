---
description: 識別頂點資料的用途。
ms.assetid: ee9b46c2-b779-480c-9b5c-6d189d2af014
title: 'D3DDECLUSAGE 列舉 (D3D9Types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDECLUSAGE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 707a5b7b886ac9366733e1b17322ac61c7d9703cb6ef8ac1e095cf1300fd508d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857508"
---
# <a name="d3ddeclusage-enumeration"></a>D3DDECLUSAGE 列舉

識別頂點資料的用途。

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DDECLUSAGE { 
  D3DDECLUSAGE_POSITION      = 0,
  D3DDECLUSAGE_BLENDWEIGHT   = 1,
  D3DDECLUSAGE_BLENDINDICES  = 2,
  D3DDECLUSAGE_NORMAL        = 3,
  D3DDECLUSAGE_PSIZE         = 4,
  D3DDECLUSAGE_TEXCOORD      = 5,
  D3DDECLUSAGE_TANGENT       = 6,
  D3DDECLUSAGE_BINORMAL      = 7,
  D3DDECLUSAGE_TESSFACTOR    = 8,
  D3DDECLUSAGE_POSITIONT     = 9,
  D3DDECLUSAGE_COLOR         = 10,
  D3DDECLUSAGE_FOG           = 11,
  D3DDECLUSAGE_DEPTH         = 12,
  D3DDECLUSAGE_SAMPLE        = 13
} D3DDECLUSAGE, *LPD3DDECLUSAGE;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="D3DDECLUSAGE_POSITION"></span><span id="d3ddeclusage_position"></span>**D3DDECLUSAGE \_ 位置**
</dt> <dd>

將資料從 (-1、-1) 到 (1、1) 等位置。 使用 D3DDECLUSAGE \_ 位置搭配0的使用方式索引，以指定固定函式頂點處理和 n patch 鑲嵌的未轉換位置。 使用 D3DDECLUSAGE \_ 位置搭配1的使用方式索引，在固定的函式頂點著色器中指定頂點補間的未轉換位置。

</dd> <dt>

<span id="D3DDECLUSAGE_BLENDWEIGHT"></span><span id="d3ddeclusage_blendweight"></span>**D3DDECLUSAGE \_ BLENDWEIGHT**
</dt> <dd>

混合權數資料。 使用 D3DDECLUSAGE \_ BLENDWEIGHT 搭配使用方式索引0，以指定用於索引和非索引頂點混合的 blend 加權。

</dd> <dt>

<span id="D3DDECLUSAGE_BLENDINDICES"></span><span id="d3ddeclusage_blendindices"></span>**D3DDECLUSAGE \_ BLENDINDICES**
</dt> <dd>

混合索引資料。 使用 D3DDECLUSAGE \_ BLENDINDICES 搭配使用索引0，以指定索引的調色板外觀的矩陣索引。

</dd> <dt>

<span id="D3DDECLUSAGE_NORMAL"></span><span id="d3ddeclusage_normal"></span>**D3DDECLUSAGE \_ 正常**
</dt> <dd>

頂點一般資料。 使用 D3DDECLUSAGE \_ NORMAL 搭配0的使用方式索引，以指定固定函式頂點處理和 n patch 鑲嵌的頂點法線。 使用 D3DDECLUSAGE \_ NORMAL 搭配1的使用方式索引，為頂點補間的固定函數頂點處理指定頂點法線。

</dd> <dt>

<span id="D3DDECLUSAGE_PSIZE"></span><span id="d3ddeclusage_psize"></span>**D3DDECLUSAGE \_ PSIZE**
</dt> <dd>

點大小資料。 使用 D3DDECLUSAGE \_ PSIZE 搭配使用方式索引0，以指定轉譯器的安裝程式引擎所使用的點大小屬性，以針對點 sprite 功能將點展開至四個點。

</dd> <dt>

<span id="D3DDECLUSAGE_TEXCOORD"></span><span id="d3ddeclusage_texcoord"></span>**D3DDECLUSAGE \_ TEXCOORD**
</dt> <dd>

材質座標資料。 使用 D3DDECLUSAGE \_ TEXCOORD、n 可指定固定函式頂點處理中的材質座標，以及 ps 3 0 之前的圖元著色器 \_ \_ 。 這些可以用來傳遞使用者定義的資料。

</dd> <dt>

<span id="D3DDECLUSAGE_TANGENT"></span><span id="d3ddeclusage_tangent"></span>**D3DDECLUSAGE \_ 正切函數**
</dt> <dd>

頂點正切資料。

</dd> <dt>

<span id="D3DDECLUSAGE_BINORMAL"></span><span id="d3ddeclusage_binormal"></span>**D3DDECLUSAGE \_ BINORMAL**
</dt> <dd>

頂點 binormal 資料。

</dd> <dt>

<span id="D3DDECLUSAGE_TESSFACTOR"></span><span id="d3ddeclusage_tessfactor"></span>**D3DDECLUSAGE \_ TESSFACTOR**
</dt> <dd>

單一正整數浮點值。 使用 D3DDECLUSAGE \_ TESSFACTOR 搭配使用方式索引0，以指定鑲嵌式單位中所使用的鑲嵌因數來控制鑲嵌率。 如需資料類型的詳細資訊，請參閱 D3DDECLTYPE \_ FLOAT1。

</dd> <dt>

<span id="D3DDECLUSAGE_POSITIONT"></span><span id="d3ddeclusage_positiont"></span>**D3DDECLUSAGE \_ POSITIONT**
</dt> <dd>

頂點資料包含已轉換的位置資料，範圍從 (0、0) 到 (的資料區寬度、視口高度) 。 使用 D3DDECLUSAGE \_ POSITIONT 搭配使用索引0，以指定轉換的位置。 當設定包含此的宣告時，管線不會執行頂點處理。

</dd> <dt>

<span id="D3DDECLUSAGE_COLOR"></span><span id="d3ddeclusage_color"></span>**D3DDECLUSAGE \_ 色彩**
</dt> <dd>

頂點資料包含漫射或反射色彩。 使用 \_ 具有0之使用方式索引的 D3DDECLUSAGE 色彩，在固定函式頂點著色器和圖元著色器中指定在 ps \_ 3 0 之前的擴散色彩 \_ 。 使用 D3DDECLUSAGE \_ 色彩搭配1的使用方式索引，以指定固定函式頂點著色器中的反射色彩，以及 ps 3 0 之前的圖元著色器 \_ \_ 。

</dd> <dt>

<span id="D3DDECLUSAGE_FOG"></span><span id="d3ddeclusage_fog"></span>**D3DDECLUSAGE \_ 霧化**
</dt> <dd>

頂點資料包含霧化資料。 使用 D3DDECLUSAGE \_ 霧化搭配0的使用方式索引，以指定圖元網底完成後使用的霧化 blend 值。 這適用于 ps 3 0 版之前的圖元著色器 \_ \_ 。

</dd> <dt>

<span id="D3DDECLUSAGE_DEPTH"></span><span id="d3ddeclusage_depth"></span>**D3DDECLUSAGE \_ 深度**
</dt> <dd>

頂點資料包含深度資料。

</dd> <dt>

<span id="D3DDECLUSAGE_SAMPLE"></span><span id="d3ddeclusage_sample"></span>**D3DDECLUSAGE \_ 範例**
</dt> <dd>

頂點資料包含取樣器資料。 使用 D3DDECLUSAGE \_ 範例搭配0的使用方式索引，以指定要查閱的置換值。 只能搭配 D3DDECLUSAGE \_ LOOKUPPRESAMPLED 或 D3DDECLUSAGE \_ LOOKUP 使用。

</dd> </dl>

## <a name="remarks"></a>備註

頂點資料是使用 [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) 結構的陣列來宣告。 陣列中的每個元素都包含使用類型。

如需有關頂點宣告的詳細資訊，請參閱 [ (Direct3D 9) 的頂點 ](vertex-declaration.md)宣告。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3D9Types。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 列舉](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[ (Direct3D 9) 的頂點宣告 ](vertex-declaration.md)
</dt> </dl>

 

 





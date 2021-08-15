---
description: 定義頂點資料版面配置。 每個頂點都可以包含一或多個資料類型，而每個資料類型都是由頂點元素所描述。
ms.assetid: 6f3c40a0-b28e-48d6-acad-ef80a919c5d7
title: 'D3DVERTEXELEMENT9 結構 (D3D9Types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DVERTEXELEMENT9
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: cda5b92170ef21f7bb66233f0748afe0c780837bbcb0eee9ef3c970880070422
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118527292"
---
# <a name="d3dvertexelement9-structure"></a>D3DVERTEXELEMENT9 結構

定義頂點資料版面配置。 每個頂點都可以包含一或多個資料類型，而每個資料類型都是由頂點元素所描述。

## <a name="syntax"></a>語法


```C++
typedef struct D3DVERTEXELEMENT9 {
  WORD Stream;
  WORD Offset;
  BYTE Type;
  BYTE Method;
  BYTE Usage;
  BYTE UsageIndex;
} D3DVERTEXELEMENT9, *LPD3DVERTEXELEMENT9;
```



## <a name="members"></a>成員

<dl> <dt>

**串流**
</dt> <dd>

類型： **[ **WORD**](../winprog/windows-data-types.md)**

</dd> <dd>

資料流程號碼。

</dd> <dt>

**Offset**
</dt> <dd>

類型： **[ **WORD**](../winprog/windows-data-types.md)**

</dd> <dd>

從頂點資料的開頭位移到與特定資料類型相關聯的資料。

</dd> <dt>

**類型**
</dt> <dd>

類型： **[**位元組**](../winprog/windows-data-types.md)**

</dd> <dd>

以 [**D3DDECLTYPE**](./d3ddecltype.md)指定的資料類型。 定義資料大小的數個預先定義類型的其中一個。 某些方法具有隱含類型。

</dd> <dt>

**方法**
</dt> <dd>

類型： **[**位元組**](../winprog/windows-data-types.md)**

</dd> <dd>

方法會指定鑲嵌處理，以決定鑲嵌如何解讀 (或) 頂點資料上運作。 如需詳細資訊，請參閱 [**D3DDECLMETHOD**](./d3ddeclmethod.md)。

</dd> <dt>

**使用量**
</dt> <dd>

類型： **[**位元組**](../winprog/windows-data-types.md)**

</dd> <dd>

定義將使用資料的目標;也就是說，頂點資料版面配置和頂點著色器之間的互通性。 每個使用方式都會將頂點宣告系結至頂點著色器。 在某些情況下，它們會有特殊的解讀。 例如， \_ N patch 鑲嵌會使用指定 D3DDECLUSAGE NORMAL 或 D3DDECLUSAGE POSITION 的元素 \_ 來設定鑲嵌。 如需可用的語法清單，請參閱 [**D3DDECLUSAGE**](./d3ddeclusage.md) 。 D3DDECLUSAGE \_ TEXCOORD 可用於使用者定義的欄位， (沒有定義) 的現有用法。

</dd> <dt>

**UsageIndex**
</dt> <dd>

類型： **[**位元組**](../winprog/windows-data-types.md)**

</dd> <dd>

修改使用方式資料，以允許使用者指定多個使用類型。

</dd> </dl>

## <a name="remarks"></a>備註

頂點資料是使用 **D3DVERTEXELEMENT9** 結構的陣列來定義。 使用 [**D3DDECL \_ END**](d3ddecl-end.md) 宣告宣告中的最後一個元素。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3D9Types。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 結構](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[ (Direct3D 9) 的頂點宣告 ](vertex-declaration.md)
</dt> </dl>

 

 

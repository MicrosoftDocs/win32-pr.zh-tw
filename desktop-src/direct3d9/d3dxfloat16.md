---
description: 描述16位浮點向量。
ms.assetid: f823a327-f07a-44e9-b58a-7865e11e80eb
title: 'D3DXFLOAT16 結構 (D3dx9math .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFLOAT16
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: 4b469c770b811ed11ec21b21d2b449df1fd75b1c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106981828"
---
# <a name="d3dxfloat16-structure-d3dx9mathh"></a>D3DXFLOAT16 結構 (D3dx9math .h) 

描述16位浮點向量。

## <a name="syntax"></a>語法


```C++
typedef struct D3DXFLOAT16 {
  WORD Value;
} D3DXFLOAT16, *LPD3DXFLOAT16;
```



## <a name="members"></a>成員

<dl> <dt>

**值**
</dt> <dd>

類型： **[ **WORD**](../winprog/windows-data-types.md)**

</dd> <dd>

16位的資料。

</dd> </dl>

## <a name="remarks"></a>備註

C + + 程式設計人員可以利用 [**D3DXFLOAT16 擴充**](d3dxfloat16-extensions.md)功能來利用運算子多載和類型轉換，以執行多載的函式和指派、一元和二元 (，包括相等) 運算子。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx9math。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 結構](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 

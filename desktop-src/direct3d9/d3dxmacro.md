---
description: 描述效果物件所使用的預處理器定義。
ms.assetid: 43413b79-e331-4466-b288-bd4439c135a2
title: 'D3DXMACRO 結構 (D3dx9shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMACRO
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: fa78c69ffe0c25b66e73da6fd9139c3b1f69661e5237c3c03e4dd2d8a377461d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118095945"
---
# <a name="d3dxmacro-structure"></a>D3DXMACRO 結構

描述效果物件所使用的預處理器定義。

## <a name="syntax"></a>語法


```C++
typedef struct D3DXMACRO {
  LPCSTR Name;
  LPCSTR Definition;
} D3DXMACRO, *LPD3DXMACRO;
```



## <a name="members"></a>成員

<dl> <dt>

**名稱**
</dt> <dd>

類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

預處理器名稱。

</dd> <dt>

**定義**
</dt> <dd>

類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

定義名稱。

</dd> </dl>

## <a name="remarks"></a>備註

若要在多行中使用 **D3DXMACRO**，請在每一個換行字元前面加上反斜線 (例如 \# C 語言) 中的定義。 例如：


```
sample=
macro.Name = "DO_CODE_BLOCK";
macro.Definition =
    "/* here is a block of code */\\\n"
    "{ do something ... }\\\n";
```



請注意行結尾的3個反斜線字元。 前兩個需要輸出單一 ' \\ '，後面接著分行符號 " \\ n"。 （選擇性）您也可能想要使用 " \\ \\ \\ r \\ n" 來終止您的行。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx9shader。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[效果結構](dx9-graphics-reference-effects-structures.md)
</dt> <dt>

[**D3DXCreateEffectFromFile**](d3dxcreateeffectfromfile.md)
</dt> </dl>

 

 

---
description: 使用提供的 Alpha、紅色、綠色及藍色值，初始化色彩。
ms.assetid: e862ba1b-fdcf-4058-8835-e58b4fc5e21a
title: 'D3DCOLOR_ARGB 宏 (D3d9types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLOR_ARGB
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: bd0138c435c15c0c2ac026487471554e0edf0afa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322747"
---
# <a name="d3dcolor_argb-macro"></a>D3DCOLOR \_ ARGB 宏

使用提供的 Alpha、紅色、綠色及藍色值，初始化色彩。

## <a name="syntax"></a>語法


```C++
D3DCOLOR D3DCOLOR_ARGB(
   int a,
   int r,
   int g,
   int b
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*的* 
</dt> <dd>

色彩的 Alpha 元件。 這個值必須介於0到255之間。

</dd> <dt>

*r* 
</dt> <dd>

色彩的紅色元件。 這個值必須介於0到255之間。

</dd> <dt>

*G* 
</dt> <dd>

色彩的綠色元件。 這個值必須介於0到255之間。

</dd> <dt>

*b* 
</dt> <dd>

色彩的藍色元件。 這個值必須介於0到255之間。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回對應至提供之 ARGB 值的 [D3DCOLOR](d3dcolor.md) 值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3d9types。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[巨集](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[**D3DCOLOR \_ RGBA**](d3dcolor-rgba.md)
</dt> <dt>

[**D3DCOLOR \_ XRGB**](d3dcolor-xrgb.md)
</dt> </dl>

 

 





---
description: 使用提供的紅色、綠色、藍色和 Alpha 浮點值，初始化色彩。
ms.assetid: 61825e33-4150-47cd-97f2-2144434a45e2
title: 'D3DCOLOR_COLORVALUE 宏 (D3d9types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLOR_COLORVALUE
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: f4ee10003e0f4fdeae937d8ac786b4d389a91ec0326c2d6288d10af2a63e2286
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751228"
---
# <a name="d3dcolor_colorvalue-macro"></a>D3DCOLOR \_ COLORVALUE 宏

使用提供的紅色、綠色、藍色和 Alpha 浮點值，初始化色彩。

## <a name="syntax"></a>語法


```C++
D3DCOLOR D3DCOLOR_COLORVALUE(
   float r,
   float g,
   float b,
   float a
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*r* 
</dt> <dd>

色彩的紅色元件。 這個值必須是範圍0.0 到1.0 的浮點值。

</dd> <dt>

*G* 
</dt> <dd>

色彩的綠色元件。 這個值必須是範圍0.0 到1.0 的浮點值。

</dd> <dt>

*b* 
</dt> <dd>

色彩的藍色元件。 這個值必須是範圍0.0 到1.0 的浮點值。

</dd> <dt>

*的* 
</dt> <dd>

色彩的 Alpha 元件。 這個值必須是範圍0.0 到1.0 的浮點值。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回對應至提供的 RGBA 值的 [**D3DCOLOR**](d3dcolor.md) 值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3d9types。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[巨集](dx9-graphics-reference-d3d-macros.md)
</dt> </dl>

 

 





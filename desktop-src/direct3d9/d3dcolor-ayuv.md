---
description: 使用 (a、y、u、v) 值來初始化色彩。
ms.assetid: 47b65aab-511a-44c1-ab94-973bc2da7e04
title: 'D3DCOLOR_AYUV 宏 (D3d9types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLOR_AYUV
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 62a34e94fbdc6c47ed034a46bdae6e9b32a7c95d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106976468"
---
# <a name="d3dcolor_ayuv-macro"></a>D3DCOLOR \_ AYUV 宏

使用 (a、y、u、v) 值來初始化色彩。

## <a name="syntax"></a>語法


```C++
D3DCOLOR D3DCOLOR_AYUV(
   int a,
   int y,
   int u,
   int v
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*的* 
</dt> <dd>

色彩的 Alpha 元件。 這個值必須介於0到255之間。

</dd> <dt>

*y* 
</dt> <dd>

色彩的亮度成分。 這個值必須介於0到255之間。

</dd> <dt>

*u* 
</dt> <dd>

色彩的藍色亮度。 這個值必須介於0到255之間。

</dd> <dt>

*V* 
</dt> <dd>

色彩的紅色亮度。 這個值必須介於0到255之間。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回對應至提供之 ARGB 值的 [D3DCOLOR](d3dcolor.md) 值。

## <a name="remarks"></a>備註

您可以使用下列方程式來轉換成亮度和色彩差異，以將 RGB 色彩縮減為每圖元16位：


```C++
y (luminance) = 0.299*red + 0.587*green + 0.114*blue
u = blue - luminance
v = red - luminance 
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3d9types。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[巨集](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[**D3DCOLOR \_ ARGB**](d3dcolor-argb.md)
</dt> <dt>

[**D3DCOLOR \_ XYUV**](d3dcolor-xyuv.md)
</dt> </dl>

 

 





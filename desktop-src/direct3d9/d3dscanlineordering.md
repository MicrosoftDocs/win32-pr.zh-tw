---
description: 旗標，指出轉譯器用來在介面上建立影像的方法。
ms.assetid: 55cf790e-ebe9-4791-a2be-a90fc76bae57
title: 'D3DSCANLINEORDERING 列舉 (D3d9types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSCANLINEORDERING
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: e5265387973c3c1605ac0022d88df3afa676dda614d7cc238e29a1ddd4a73f5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119987228"
---
# <a name="d3dscanlineordering-enumeration"></a>D3DSCANLINEORDERING 列舉

旗標，指出轉譯器用來在介面上建立影像的方法。

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DSCANLINEORDERING { 
  D3DSCANLINEORDERING_PROGRESSIVE  = 1,
  D3DSCANLINEORDERING_INTERLACED   = 2
} D3DSCANLINEORDERING, *LPD3DSCANLINEORDERING;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="D3DSCANLINEORDERING_PROGRESSIVE"></span><span id="d3dscanlineordering_progressive"></span>**D3DSCANLINEORDERING \_ 漸進式**
</dt> <dd>

映射會從第一個 scanline 建立到最後一個，而不會略過任何。

</dd> <dt>

<span id="D3DSCANLINEORDERING_INTERLACED"></span><span id="d3dscanlineordering_interlaced"></span>**交錯式 D3DSCANLINEORDERING \_**
</dt> <dd>

影像是使用交錯的方法所建立，在奇數的行程上繪製奇數行，甚至是在偶數的階段繪製。

</dd> </dl>

## <a name="remarks"></a>備註

此列舉會用來做為 [**D3DDISPLAYMODEFILTER**](d3ddisplaymodefilter.md) 和 [**D3DDISPLAYMODEEX**](d3ddisplaymodeex.md)中的成員。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3d9types。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 列舉](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 





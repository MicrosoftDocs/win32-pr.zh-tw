---
description: 將弧度轉換為度數。
ms.assetid: 1b19af39-ca23-4364-9121-f532d7fed099
title: 'D3DXToDegree (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXToDegree
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: 284e59d8bb0a5b6f866286d67aa8c743716e333333d6c865077ce2cfd51778a5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119008"
---
# <a name="d3dxtodegree"></a>D3DXToDegree

將弧度轉換為度數。

``` syntax
#define D3DXToDegree(radian) ((radian) * (180.0f / D3DX_PI))
```

## <a name="parameters"></a>參數



| 參數                                                           | 描述                                              |
|---------------------------------------------------------------------|----------------------------------------------------------|
| <span id="radian"></span><span id="RADIAN"></span>弧度<br/> | 要轉換成度數的值（以弧度為單位）。<br/> |



 

## <a name="return-value"></a>傳回值

宏會傳回弧度值（以度為單位）。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx9math。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[巨集](dx9-graphics-reference-d3dx-macros.md)
</dt> <dt>

[**D3DXToRadian**](d3dxtoradian.md)
</dt> <dt>

[D3DX \_ PI](other-d3dx-constants.md)
</dt> </dl>

 

 





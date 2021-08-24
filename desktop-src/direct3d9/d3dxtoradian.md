---
description: 將度數轉換成弧度。
ms.assetid: 450806bd-db2f-47be-ae80-c261088b1bb8
title: 'D3DXToRadian (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXToRadian
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: 81f15ca3c117cb3020165bb820d221d416198893b45285931fa6cf3b1f66eea1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749648"
---
# <a name="d3dxtoradian"></a>D3DXToRadian

將度數轉換成弧度。

``` syntax
#define D3DXToRadian(degree) ((degree) * (D3DX_PI / 180.0f))
```

## <a name="parameters"></a>參數



| 參數                                                           | 描述                                              |
|---------------------------------------------------------------------|----------------------------------------------------------|
| <span id="degree"></span><span id="DEGREE"></span>程度<br/> | 要轉換成弧度的值（以度為單位）。<br/> |



 

## <a name="return-value"></a>傳回值

宏會傳回以弧度為單位的度值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx9math。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[巨集](dx9-graphics-reference-d3dx-macros.md)
</dt> <dt>

[**D3DXToDegree**](d3dxtodegree.md)
</dt> <dt>

[D3DX \_ PI](other-d3dx-constants.md)
</dt> </dl>

 

 





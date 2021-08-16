---
description: 識別後續的轉換矩陣，這些矩陣可以用來 blend 頂點，方法是使用對應的矩陣，以及在頂點格式中指定的混合 (搶鮮版（Beta）) 加權值。
ms.assetid: cab444c2-b245-4d1a-a90c-745c92a2ea89
title: 'D3DTS_WORLDn (D3d9types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTS_WORLDn
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 7026308192f43b7290dedcb9572772c9eda45acdc87d018480bd59202a2dc2df
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119398"
---
# <a name="d3dts_worldn"></a>D3DTS \_ WORLDn

識別後續的轉換矩陣，這些矩陣可以用來 blend 頂點，方法是使用對應的矩陣，以及在頂點格式中指定的混合 (搶鮮版（Beta）) 加權值。

``` syntax
#define D3DTS_WORLDn 
#define D3DTS_WORLD1 D3DTS_WORLDMATRIX(1)
#define D3DTS_WORLD2 D3DTS_WORLDMATRIX(2)
#define D3DTS_WORLD3 D3DTS_WORLDMATRIX(3)
```

## <a name="remarks"></a>備註

這些宏是為了促進現有的應用程式與 Direct3D 9 的移植而提供。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3d9types。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[巨集](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[**SetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform)
</dt> <dt>

[**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md)
</dt> </dl>

 

 

---
description: 描述矩陣。
ms.assetid: d6b98a32-e745-4724-b8ce-a81a3f5416f3
title: 'D3DMATRIX (D3D9Types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DMATRIX
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: ee4c67a4a743d3bff1cfc5ca88b6691e995f78a9fb01fe36aabc4ae6aca66e6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117732363"
---
# <a name="d3dmatrix"></a>D3DMATRIX

描述矩陣。

``` syntax
typedef struct _D3DMATRIX {
    union {
        struct {
            float        _11, _12, _13, _14;
            float        _21, _22, _23, _24;
            float        _31, _32, _33, _34;
            float        _41, _42, _43, _44;

        };
        float m[4][4];
    };
} D3DMATRIX;
```

衍生類型： \* LPD3DMATRIX

## <a name="members"></a>成員



| 項目                                                        | 描述                                                                                                                                                                                                     |
|-------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="_ij"></span><span id="_IJ"></span>\_Ij<br/> | 代表4x4 矩陣的浮點數陣列，其中 i 是資料列編號，而 j 是資料行編號。 例如， \_ 34 表示與 \[ ₃₄相同 \] ，第三個數據列和第四個數據行中的元件。<br/> |



 

## <a name="remarks"></a>備註

在 Direct3D 中， \_ 投射矩陣的34元素不能是負數。 如果您的應用程式需要在這個位置使用負值，則應該改為將整個投射矩陣調整為-1。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3D9Types。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 結構](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettransform)
</dt> <dt>

[**MultiplyTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-multiplytransform)
</dt> <dt>

[**SetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform)
</dt> <dt>

**SetTransform**
</dt> <dt>

[**D3DXMATRIX**](d3dxmatrix.md)
</dt> <dt>

[轉換 (Direct3D 9) ](transforms.md)
</dt> </dl>

 

 

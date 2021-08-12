---
description: 在效果中建立程式材質填充的版本權杖。 D3DXFillxxxTX 函數會使用這個宏。
ms.assetid: b11b6229-27a3-4813-9642-9e33bcd0da7a
title: 'D3DXTX_VERSION (D3DX9Shader) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTX_VERSION
api_type:
- HeaderDef
api_location:
- D3DX9Shader.h
ms.openlocfilehash: 1a343930f55323016895007f858a7fe188418eeab24b16859c2d773e39c9e73b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118524099"
---
# <a name="d3dxtx_version"></a>D3DXTX \_ 版本

在效果中建立程式材質填充的版本權杖。 D3DXFillxxxTX 函數會使用這個宏。

``` syntax
#define D3DXTX_VERSION (_Major, _Minor) (('T' << 24) | ('X' << 16) | ((_Major) << 8) | (_Minor))
```

## <a name="return-value"></a>傳回值

宏會傳回程序的材質版本戳記。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3DX9Shader。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[巨集](dx9-graphics-reference-d3dx-macros.md)
</dt> <dt>

[**D3DXFillTextureTX**](d3dxfilltexturetx.md)
</dt> <dt>

[**D3DXFillCubeTextureTX**](d3dxfillcubetexturetx.md)
</dt> <dt>

[**D3DXFillVolumeTextureTX**](d3dxfillvolumetexturetx.md)
</dt> </dl>

 

 





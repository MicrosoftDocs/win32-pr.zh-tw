---
description: 識別要設定為世界轉換矩陣的轉換矩陣。
ms.assetid: 2bf7ac8a-43d8-460e-a400-3b33e96441db
title: 'D3DTS_WORLD 宏 (D3d9types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTS_WORLD
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: c3c8f0ac30230a747fba34d9962791b4b331d647
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106976473"
---
# <a name="d3dts_world-macro"></a>D3DTS \_ WORLD 宏

識別要設定為世界轉換矩陣的轉換矩陣。

## <a name="syntax"></a>語法


```C++
D3DTRANSFORMSTATETYPE D3DTS_WORLD(void);
```



## <a name="parameters"></a>參數

這個宏沒有任何參數。

## <a name="return-value"></a>傳回值

[**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md)相當於 [**D3DTS \_ WORLDMATRIX (0)**](./d3dts-worldmatrix.md)。

## <a name="remarks"></a>備註

這個宏是為了加速將現有應用程式移植到 Direct3D 9 的目的而提供。

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

 

 

---
description: 傳回2D 向量的長度。
ms.assetid: 376fd2ca-c89d-41e7-a15c-a79d7281d010
title: 'D3DXVec2Length 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Length
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1753098d164cd67e79770a0ecfcf5db4d047c1a0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106975664"
---
# <a name="d3dxvec2length-function"></a>D3DXVec2Length 函式

傳回2D 向量的長度。

## <a name="syntax"></a>語法


```C++
FLOAT D3DXVec2Length(
  _In_ const D3DXVECTOR2 *pV
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pV* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR2**](d3dxvector2.md) \***

來源 [**D3DXVECTOR2**](d3dxvector2.md) 結構的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

向量的長度。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9math。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[數學函數](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXVec2LengthSq**](d3dxvec2lengthsq.md)
</dt> </dl>

 

 

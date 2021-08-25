---
description: 建立轉譯矩陣。
ms.assetid: a3565a06-22af-4ded-8835-da4c7ae81805
title: 'D3DXMatrixTranslation 函式 (D3DX10Math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixTranslation
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 5e6b5daf7bc3504e9ab79bc9ea5db70057e1b1e0f7dc20e8fd53a09958c2deb7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028698"
---
# <a name="d3dxmatrixtranslation-function-d3dx10mathh"></a>D3DXMatrixTranslation 函式 (D3DX10Math) 

建立轉譯矩陣。

## <a name="syntax"></a>語法


```C++
D3DXMATRIX* D3DXMatrixTranslation(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      x,
  _In_    FLOAT      y,
  _In_    FLOAT      z
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*不悅* \[in、out\]
</dt> <dd>

類型： **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

將成為轉譯矩陣的矩陣。 請參閱 [**D3DXMATRIX**](d3d10-d3dxmatrix.md)。

</dd> <dt>

*x* \[ 于\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

轉譯的 x 元件。

</dd> <dt>

*y* \[ in\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

轉譯的 y 元件。

</dd> <dt>

*z* \[ in\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

轉譯的 z 元件。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

轉移矩陣。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX10Math。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3DX10 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[數學函數](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 

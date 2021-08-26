---
description: D3DXFloat32To16Array 函式 (D3dx9math) -將32位浮點數的陣列轉換成16位浮點數。
ms.assetid: 00f7ae77-d2b5-4244-8fe9-6fea475700b7
title: 'D3DXFloat32To16Array 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFloat32To16Array
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2d4b02a85a22d8490b36ad32511af0d85294045502d4e32ba82b757ac34e21ea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120027728"
---
# <a name="d3dxfloat32to16array-function-d3dx9mathh"></a>D3DXFloat32To16Array 函式 (D3dx9math) 

將32位浮點數的陣列轉換成16位浮點數。

## <a name="syntax"></a>語法


```C++
D3DXFLOAT16* D3DXFloat32To16Array(
  _Inout_       D3DXFLOAT16 *pOut,
  _In_    const FLOAT       *pIn,
  _In_          UINT        n
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*不悅* \[in、out\]
</dt> <dd>

類型： **[ **D3DXFLOAT16**](d3dxfloat16.md)\***

16位浮點數陣列的指標。

</dd> <dt>

*pIn* \[在\]
</dt> <dd>

Type： **Const [**FLOAT**](../winprog/windows-data-types.md) \***

32位浮點數陣列的指標。

</dd> <dt>

*n* \[ in\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

陣列中的項目數。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **D3DXFLOAT16**](d3dxfloat16.md)\***

16位浮點數陣列的指標。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9math。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[數學函數](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 

---
description: 將32位浮點數的陣列轉換成16位浮點數。
ms.assetid: 2114cf25-cc83-4c4a-9db5-ecc0f8ff1e85
title: 'D3DXFloat32To16Array 函式 (D3DX10Math) '
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: a4c116212be0ffa71ee35939d0a30a40cbb773b3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106974882"
---
# <a name="d3dxfloat32to16array-function-d3dx10mathh"></a>D3DXFloat32To16Array 函式 (D3DX10Math) 

將32位浮點數的陣列轉換成16位浮點數。

## <a name="syntax"></a>語法


```C++
D3DXFLOAT16* D3DXFloat32To16Array(
  _In_       D3DXFLOAT16 *pOut,
  _In_ const FLOAT       *pIn,
  _In_       UINT        n
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*不悅* \[在\]
</dt> <dd>

類型： **[ **D3DXFLOAT16**](../direct3d9/d3dxfloat16.md)\***

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

類型： **[ **D3DXFLOAT16**](../direct3d9/d3dxfloat16.md)\***

16位浮點數陣列的指標。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX10Math。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3DX10 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[數學函數](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 

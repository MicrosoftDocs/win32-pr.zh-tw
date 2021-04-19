---
description: 計算兩個球形諧波函式的乘積 (f 和 g) 。 這兩個函數的順序都是 N = 6。
ms.assetid: 3b68b238-c1ae-4ab8-89ed-bdf815463143
title: 'D3DXSHMultiply6 函式 (D3DX10Math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHMultiply6
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 0768bb8be1f2f23693a431a2c0ea8f3d5a6846d2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106985897"
---
# <a name="d3dxshmultiply6-function"></a>D3DXSHMultiply6 函式

計算兩個球形諧波函式的乘積 (f 和 g) 。 這兩個函數的順序都是 N = 6。

## <a name="syntax"></a>語法


```C++
FLOAT* D3DXSHMultiply6(
  _In_       FLOAT *pOut,
  _In_ const FLOAT *pF,
  _In_ const FLOAT *pG
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*不悅* \[在\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***

輸出 SH 係數的指標-基礎函數 *Y* lm 會儲存在 l ² + *m* + l。 順序 *N* 決定陣列的長度，其中應該一律為 *N*²係數。

</dd> <dt>

*pF* \[在\]
</dt> <dd>

Type： **Const [**FLOAT**](../winprog/windows-data-types.md) \***

第一個函數的輸入 SH 係數。

</dd> <dt>

*pG* \[在\]
</dt> <dd>

Type： **Const [**FLOAT**](../winprog/windows-data-types.md) \***

第二組輸入 SH 係數。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***

SH 輸出係數的指標。

## <a name="remarks"></a>備註

Order N = 6 的兩個 SH 函數的乘積會產生 order 2 × *n-1* = 11 的 sh 函式，但結果會被截斷。 這表示產品與 ( *f* × *g*  =  *g* × *f* ) 但不會關聯 ( *f* x ( *g* × *h* ) ≠ ( *f* × *g* ) × *h* ) 。

此函式會使用下列方程式：


```
pOut[i] = int(y_i(s) * f(s) * g(s))
```



其中，y \_ i (s) 是第 i 個 sh 基礎函式，其中 f (s) 和 g () 使用下列 SH 函數：


```
sum_i(y_i(s)*c_i)
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX10Math。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3DX10 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[數學函數](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 

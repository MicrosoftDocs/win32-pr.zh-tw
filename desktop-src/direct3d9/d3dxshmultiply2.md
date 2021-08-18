---
description: 以 SH (f 和 g) ，計算兩個函式的乘積。
ms.assetid: 632400a4-2ac9-438d-85f7-869101f350c8
title: 'D3DXSHMultiply2 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHMultiply2
- D3DXSHMultiply3
- D3DXSHMultiply4
- D3DXSHMultiply5
- D3DXSHMultiply6
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: 00219ed1c38105562591b63e6bef64b949b2ab4443aed68e0e6b9d64cb156cc7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119849688"
---
# <a name="d3dxshmultiply2-function-d3dx9mathh"></a>D3DXSHMultiply2 函式 (D3dx9math) 

以 SH (f 和 g) ，計算兩個函式的乘積。

## <a name="syntax"></a>語法


```C++
FLOAT* D3DXSHMultiply2(
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

輸出 SH 係數-基礎函數 Ylm 的指標會儲存在 l \* l + m + l。

</dd> <dt>

*pF* \[在\]
</dt> <dd>

Type： **Const [**FLOAT**](../winprog/windows-data-types.md) \***

輸入 SH coeffs for first 函數。

</dd> <dt>

*pG* \[在\]
</dt> <dd>

Type： **Const [**FLOAT**](../winprog/windows-data-types.md) \***

第二組輸入 SH coeffs。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***

SH 輸出係數的指標。

## <a name="remarks"></a>備註

順序是介於2和6（含）之間的數位。 因此，此頁面實際上記載了數個函數： D3DXSHMultiply2、D3DXSHMultiply3、.。。D3DXSHMultiply6.

使用 SH (f 和 g) 來計算兩個函式的乘積，其中 *不悅* \[ i \] = int (y \_ i (s) \* f (s) \* g (s) ) ，其中的 y \_ i () 是第 i 個 sh 基礎函式，f (s) 和 g (s) 是 SH 函式 (sum i (y () \_ \_ \* c \_ i) ) 。 順序 O 決定陣列的長度，其中應該一律為 O ^ 2 係數。 一般而言，order O 的兩個 SH 函數的乘積會產生 order 2 的 SH 函 \* 式，但結果會被截斷。 這表示產品與 (f \* g = = g \* f) 但不會將 (f \* (g \* h) ！ = (f \* g) h \* 相關聯。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx9math。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[數學函數](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 

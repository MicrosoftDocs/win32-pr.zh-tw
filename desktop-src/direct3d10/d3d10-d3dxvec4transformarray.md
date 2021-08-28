---
description: 將陣列 (x、y、z、w) 由指定的矩陣進行轉換。
ms.assetid: afd5cccb-e22f-4726-a84e-9eac1c1c277f
title: 'D3DXVec4TransformArray 函式 (D3DX10Math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4TransformArray
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 2c6fdcdd2a404e4122a0c8c66995fdabaf1284dfa67ebade888d2964c0c1fb8a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119852798"
---
# <a name="d3dxvec4transformarray-function-d3dx10mathh"></a>D3DXVec4TransformArray 函式 (D3DX10Math) 

將陣列 (x、y、z、w) 由指定的矩陣進行轉換。

## <a name="syntax"></a>語法


```C++
D3DXVECTOR4* D3DXVec4TransformArray(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_          UINT        OutStride,
  _In_    const D3DXVECTOR4 *pV,
  _In_          UINT        VStride,
  _In_    const D3DXMATRIX  *pM,
  _In_          UINT        n
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*不悅* \[in、out\]
</dt> <dd>

類型： **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***

[**D3DXVECTOR4**](d3d10-d3dxvector4.md)陣列的指標，這是作業的結果。

</dd> <dt>

*OutStride* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

輸出資料流程中向量之間的 Stride。

</dd> <dt>

*pV* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***

來源 D3DXVECTOR4 陣列的指標。

</dd> <dt>

*VStride* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

輸入資料流程中向量之間的 Stride。

</dd> <dt>

*pM* \[在\]
</dt> <dd>

Type： **Const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

來源 [**D3DXMATRIX**](d3d10-d3dxmatrix.md) 結構的指標。

</dd> <dt>

*n* \[ in\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

陣列中的元素數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***

[**D3DXVECTOR4**](d3d10-d3dxvector4.md)結構的指標，此結構是已轉換的陣列。

## <a name="remarks"></a>備註

此函式會將陣列 pV (x、y、z、w) 由矩陣 pM 進行轉換。

此函式的傳回值與 *不悅* 參數中所傳回的值相同。 如此一來， **D3DXVec4TransformArray** 函式就可以用來做為另一個函式的參數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3DX10Math。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[數學函數](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 

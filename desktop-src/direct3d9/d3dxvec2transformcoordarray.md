---
description: 將陣列 (x、y、0、1) 由指定的矩陣轉換，然後將結果投射回 w = 1。
ms.assetid: 23c88bed-344b-4b3a-bb92-e50cbe96daf9
title: 'D3DXVec2TransformCoordArray 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2TransformCoordArray
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e924f9c008efe76490f9f51903a1c31f254e0001
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986743"
---
# <a name="d3dxvec2transformcoordarray-function-d3dx9mathh"></a>D3DXVec2TransformCoordArray 函式 (D3dx9math) 

將陣列 (x、y、0、1) 由指定的矩陣轉換，然後將結果投射回 w = 1。

## <a name="syntax"></a>語法


```C++
D3DXVECTOR2* D3DXVec2TransformCoordArray(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_          UINT        OutStride,
  _In_    const D3DXVECTOR2 *pV,
  _In_          UINT        VStride,
  _In_    const D3DXMATRIX  *pM,
  _In_          UINT        n
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*不悅* \[in、out\]
</dt> <dd>

類型： **[ **D3DXVECTOR2**](d3dxvector2.md)\***

[**D3DXVECTOR2**](d3dxvector2.md)結構的指標，此結構是作業的結果。

</dd> <dt>

*OutStride* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

輸出資料流程中向量之間的 Stride。

</dd> <dt>

*pV* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR2**](d3dxvector2.md) \***

來源 [**D3DXVECTOR2**](d3dxvector2.md) 陣列的指標。

</dd> <dt>

*VStride* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

輸入資料流程中向量之間的 Stride。

</dd> <dt>

*pM* \[在\]
</dt> <dd>

Type： **Const [**D3DXMATRIX**](d3dxmatrix.md) \***

來源 [**D3DXMATRIX**](d3dxmatrix.md) 結構的指標。

</dd> <dt>

*n* \[ in\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

陣列中的元素數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **D3DXVECTOR2**](d3dxvector2.md)\***

[**D3DXVECTOR4**](d3dxvector4.md)轉換陣列的指標。

## <a name="remarks"></a>備註

此函式會將陣列 *pV* (x、y、0、1) 由矩陣 *pM* 轉換，然後將結果投射回 w = 1。

此函式的傳回值與 *不悅* 參數中所傳回的值相同。 如此一來， **D3DXVec2TransformCoordArray** 函式就可以用來做為另一個函式的參數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9math。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[數學函數](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 

---
description: D3DXSHAdd 函式 (D3dx9math) -新增兩個球面調和 (SH) 向量;換句話說，不悅 \[ i \] = pA \[ i \] + pB \[ i \] 。
ms.assetid: 12775c90-ed9d-4931-a449-2571816dd079
title: 'D3DXSHAdd 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHAdd
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7333d1803b9f7ea7b056ff78ffd053bd6086184b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117956"
---
# <a name="d3dxshadd-function-d3dx9mathh"></a>D3DXSHAdd 函式 (D3dx9math) 

將兩個球面調和新增 (SH) 向量;換句話說，不悅 \[ i \] = pA \[ i \] + pB \[ i \] 。

## <a name="syntax"></a>語法


```C++
FLOAT* D3DXSHAdd(
  _Out_       FLOAT *pOut,
  _In_        UINT  Order,
  _In_  const FLOAT *pA,
  _In_  const FLOAT *pB
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*不悅* \[擴展\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***

SH 輸出係數的指標。 評估會產生順序²係數。 請參閱＜備註＞。

</dd> <dt>

*訂單* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

SH 評估的順序。 必須在 [D3DXSH \_ MINORDER](other-d3dx-constants.md) 到 D3DXSH \_ MAXORDER （含）的範圍內。 評估會產生順序²係數。 評估的程度是順序-1。

</dd> <dt>

*pA* \[在\]
</dt> <dd>

Type： **Const [**FLOAT**](../winprog/windows-data-types.md) \***

第一個 SH 向量的指標。

</dd> <dt>

*pB* \[在\]
</dt> <dd>

Type： **Const [**FLOAT**](../winprog/windows-data-types.md) \***

第二個 SH 向量的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***

SH 輸出係數的指標。

## <a name="remarks"></a>備註

基礎函數 Ylm 的每個係數都會儲存在記憶體位置 l ² + m + l，其中：

-   l 是基礎函數的程度。
-   m 是指定 l 值的基礎函數索引，範圍從-l 到 l （含）。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9math。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[數學函數](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[預先計算 Radiance Transfer (Direct3D 9) ](precomputed-radiance-transfer.md)
</dt> </dl>

 

 

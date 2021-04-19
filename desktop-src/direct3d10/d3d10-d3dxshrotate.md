---
description: 將球形調和 (SH) 向量旋轉指定的矩陣。
ms.assetid: 22ed379a-ce08-46df-9cc1-8d5fde87c179
title: 'D3DXSHRotate 函式 (D3DX10) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHRotate
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 1cdff4a74cb92943db2bd6dc9f207dbac2208afa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106993902"
---
# <a name="d3dxshrotate-function-d3dx10h"></a>D3DXSHRotate 函式 (D3DX10) 

將球形調和 (SH) 向量旋轉指定的矩陣。

## <a name="syntax"></a>語法


```C++
FLOAT* D3DXSHRotate(
  _In_       FLOAT      *pOut,
  _In_       UINT       Order,
  _In_ const D3DXMATRIX *pMatrix,
  _In_ const FLOAT      *pIn
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*不悅* \[在\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***

球面調和 (SH) 輸出係數的指標。 評估會產生順序²係數。 此指標不應使用 pIn 別名。 請參閱＜備註＞。

</dd> <dt>

*訂單* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

SH 評估的順序。 必須在 D3DXSH \_ MINORDER 到 D3DXSH \_ MAXORDER （含）的範圍內。 評估會產生順序²係數。 評估的程度是順序-1。

</dd> <dt>

*pMatrix* \[在\]
</dt> <dd>

Type： **Const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

旋轉矩陣的指標。 旋轉子矩陣必須是垂直的，且具有單位行列式。

</dd> <dt>

*pIn* \[在\]
</dt> <dd>

Type： **Const [**FLOAT**](../winprog/windows-data-types.md) \***

旋轉的 SH 係數指標。

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
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX10。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>D3DX10 .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[數學函數](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 

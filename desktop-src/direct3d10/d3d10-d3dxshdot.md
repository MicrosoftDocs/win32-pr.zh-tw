---
description: D3DXSHDot 函數 (D3DX10) -計算兩個球面調和 (SH) 向量的點乘積。
ms.assetid: 30f0e858-4c31-4b25-9979-754d996a7d48
title: 'D3DXSHDot 函式 (D3DX10) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHDot
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 3ea3e839ff7a5fc038cf40a6402db4a358da8b39
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108626"
---
# <a name="d3dxshdot-function-d3dx10h"></a>D3DXSHDot 函式 (D3DX10) 

計算兩個球形調和 (SH) 向量的點乘積。

## <a name="syntax"></a>語法


```C++
FLOAT D3DXSHDot(
  _In_       UINT  Order,
  _In_ const FLOAT *pA,
  _In_ const FLOAT *pB
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*訂單* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

球形調和 (SH) 評估的順序。 必須在 D3DXSH \_ MINORDER 到 D3DXSH \_ MAXORDER （含）的範圍內。 評估會產生順序²係數。 評估的程度是順序-1。

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

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

SH 輸出係數。

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

 

 

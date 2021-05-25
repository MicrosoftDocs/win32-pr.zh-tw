---
description: D3DXComputeIMTFromSignal 用來描述輸入網格 u、v 空間中使用者定義信號的函式原型。 函式會在提供的 u、v 座標上評估維度 uSignalDimension 的程式性信號。
ms.assetid: 97b07dbc-6b84-46d2-acc7-db81d94538f7
title: LPD3DXIMTSIGNALCALLBACK
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dbf75bf1a3fc05b217feef8446636efaae55b3b
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/24/2021
ms.locfileid: "110342833"
---
# <a name="lpd3dximtsignalcallback"></a>LPD3DXIMTSIGNALCALLBACK

[**D3DXComputeIMTFromSignal**](d3dxcomputeimtfromsignal.md)用來描述輸入網格 u、v 空間中使用者定義信號的函式原型。 函式會在提供的 u、v 座標上評估維度 uSignalDimension 的程式性信號。

## <a name="syntax"></a>語法


```
typedef HRESULT (WINAPI* LPD3DXIMTSIGNALCALLBACK)
     (CONST D3DXVECTOR2 *uv,
      UINT uPrimitiveID,
      UINT uSignalDimension,
      VOID *pUserData,
      FLOAT *pfSignalOut);
```



## <a name="parameters"></a>參數

\[在 \] uv-包含頂點材質座標的向量指標。

\[在 \] uPrimitiveId 中-應計算其信號之網格上的輸入三角形索引。

\[在 \] uSignalDimension 中-要儲存在信號資料陣列中的浮點數 (pfSignalOut) 。

\[在 \] pUserData 中-傳遞至 [**D3DXComputeIMTFromSignal**](d3dxcomputeimtfromsignal.md)的 pUserData 指標。

\[out \] pfSignalOut-浮點數的陣列，其中包含信號資料。

## <a name="return-value"></a>傳回值

必須實作為此函式，才能傳回 S \_ OK。

## <a name="remarks"></a>備註

宣告回呼函數時，請務必指定 [**Windows 資料類型**](../winprog/windows-data-types.md) 呼叫慣例。 否則，可能會發生堆疊溢位。



| 需求               | 值            |
|----------------|-------------|
| 標頭         | d3dx9mesh。h |
| 匯入程式庫 | d3dx9 .lib   |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[回呼函式](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> </dl>

 

 

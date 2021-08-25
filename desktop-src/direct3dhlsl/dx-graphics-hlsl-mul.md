---
title: mul
description: 使用矩陣數學乘以 x 和 y。 內部維度 x 資料行和 y 資料列必須相等。
ms.assetid: 9945388a-d802-4dbe-bdb7-4eadb8751c39
keywords:
- mul HLSL
topic_type:
- apiref
api_name:
- mul
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e6362c734cbbf30defa8fed75f28c6f39397d75977488d9efc170d2647a9b3d3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950358"
---
# <a name="mul"></a>mul

使用矩陣數學乘以 x 和 y。 內部維度 x 資料行和 y 資料列必須相等。



| ret mul (x，y)  |
|---------------|



 

## <a name="parameters"></a>參數



| 項目                                                   | 描述                                                                           |
|--------------------------------------------------------|---------------------------------------------------------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/> | \[在 \] [x 輸入值] 中。 如果 x 是向量，則會將它視為資料列向量。<br/>    |
| <span id="y"></span><span id="Y"></span>*Y*<br/> | \[（在 \] y 輸入值中）。 如果 y 是向量，則會將它視為資料行向量。<br/> |



 

## <a name="return-value"></a>傳回值

X 乘以 y 的結果。 結果具有 dimension x 資料列 x y 資料行。

## <a name="type-description"></a>類型描述

此函式有9個多載版本;多載版本會針對輸入引數的類型和大小，處理不同的案例。



| 版本 | 名稱 | 目的 | [**範本類型**](dx-graphics-hlsl-intrinsic-functions.md) | [**元件類型**](dx-graphics-hlsl-intrinsic-functions.md) | 大小                                                                     |
|---------|------|---------|---------------------------------------------------------------|----------------------------------------------------------------|--------------------------------------------------------------------------|
| 1       |      |         |                                                               |                                                                |                                                                          |
|         | x    | in      | 純量 (scalar)                                                        | float、int                                                     | 1                                                                        |
|         | y    | in      | 純量 (scalar)                                                        | 與輸入 x 相同                                                | 1                                                                        |
|         | Ret  | out     | 純量 (scalar)                                                        | 與輸入 x 相同                                                | 1                                                                        |
| 2       |      |         |                                                               |                                                                |                                                                          |
|         | x    | in      | 純量 (scalar)                                                        | float、int                                                     | 1                                                                        |
|         | y    | in      | 向量                                                        | float、int                                                     | 任意                                                                      |
|         | Ret  | out     | 向量                                                        | float、int                                                     | ) 為輸入 y 的相同維度 (s                                             |
| 3       |      |         |                                                               |                                                                |                                                                          |
|         | x    | in      | 純量 (scalar)                                                        | float、int                                                     | 1                                                                        |
|         | y    | in      | 矩陣                                                        | float、int                                                     | 任意                                                                      |
|         | Ret  | out     | 矩陣                                                        | 與輸入 y 相同                                                | ) 為輸入 y 的相同維度 (s                                             |
| 4       |      |         |                                                               |                                                                |                                                                          |
|         | x    | in      | 向量                                                        | float、int                                                     | 任意                                                                      |
|         | y    | in      | 純量 (scalar)                                                        | float、int                                                     | 1                                                                        |
|         | Ret  | out     | 向量                                                        | float、int                                                     | ) 為輸入 x 的相同維度 (s                                             |
| 5       |      |         |                                                               |                                                                |                                                                          |
|         | x    | in      | 向量                                                        | float、int                                                     | 任意                                                                      |
|         | y    | in      | 向量                                                        | float、int                                                     | ) 為輸入 x 的相同維度 (s                                             |
|         | Ret  | out     | 純量 (scalar)                                                        | float、int                                                     | 1                                                                        |
| 6       |      |         |                                                               |                                                                |                                                                          |
|         | x    | in      | 向量                                                        | float、int                                                     | 任意                                                                      |
|         | y    | in      | 矩陣                                                        | float、int                                                     | rows = 相同維度 (s) 做為輸入 x，資料行 = 任意                       |
|         | Ret  | out     | 向量                                                        | float、int                                                     | 相同維度 (s) 作為輸入 y 資料行                                     |
| 7       |      |         |                                                               |                                                                |                                                                          |
|         | x    | in      | 矩陣                                                        | float、int                                                     | 任意                                                                      |
|         | y    | in      | 純量 (scalar)                                                        | float、int                                                     | 1                                                                        |
|         | Ret  | out     | 矩陣                                                        | float、int                                                     | ) 為輸入 x 的相同維度 (s                                             |
| 8       |      |         |                                                               |                                                                |                                                                          |
|         | x    | in      | 矩陣                                                        | float、int                                                     | 任意                                                                      |
|         | y    | in      | 向量                                                        | float、int                                                     | 輸入 x 中的資料行數目                                             |
|         | Ret  | out     | 向量                                                        | float、int                                                     | 輸入 x 中的資料列數目                                                |
| 9       |      |         |                                                               |                                                                |                                                                          |
|         | x    | in      | 矩陣                                                        | float、int                                                     | 任意                                                                      |
|         | y    | in      | 矩陣                                                        | float、int                                                     | rows = 輸入 x 中的資料行數目                                      |
|         | Ret  | out     | 矩陣                                                        | float、int                                                     | rows = 輸入 x 中的資料列數目，資料行 = 輸入 y 中的資料行數目 |



 

## <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此函數。



| 著色器模型                                                                       | 支援 |
|------------------------------------------------------------------------------------|-----------|
| [著色器模型 1 (DIRECTX HLSL) ](dx-graphics-hlsl-sm1.md) 和更高的著色器模型 | 是       |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**(DirectX HLSL) 內建函式**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 






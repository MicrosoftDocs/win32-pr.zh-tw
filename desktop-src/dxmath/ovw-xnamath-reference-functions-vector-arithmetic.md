---
description: 列出向量算術函數。
ms.assetid: d7ed4516-74a6-81ec-79a2-2e39cf112d11
title: 向量算術函數
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64ad5149153b736ddf6d2f2af5b9671e32651f86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106978851"
---
# <a name="vector-arithmetic-functions"></a>向量算術函數

列出向量算術函數。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                   | 描述                                                                                                               |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**XMVectorAbs**](/windows/win32/api/directxmath/nf-directxmath-xmvectorabs)<br/>                                           | 計算 [**XMVECTOR**](xmvector-data-type.md)之每個元件的絕對值。<br/>                    |
| [**XMVectorAdd**](/windows/win32/api/directxmath/nf-directxmath-xmvectoradd)<br/>                                           | 計算兩個向量的總和。<br/>                                                                               |
| [**XMVectorAddAngles**](/windows/win32/api/directxmath/nf-directxmath-xmvectoraddangles)<br/>                               | 新增代表角度的兩個向量。<br/>                                                                          |
| [**XMVectorCeiling**](/windows/win32/api/directxmath/nf-directxmath-xmvectorceiling)<br/>                                   | 計算 [**XMVECTOR**](xmvector-data-type.md)之每個元件的最高上限。<br/>                           |
| [**XMVectorClamp**](/windows/win32/api/directxmath/nf-directxmath-xmvectorclamp)<br/>                                       | 將向量的元件個至指定的最小和最大範圍。<br/>                                    |
| [**XMVectorDivide**](/windows/win32/api/directxmath/nf-directxmath-xmvectordivide)<br/>                                     | 將一個實例除以 `XMVECTOR` 第二個實例，並在第三個實例中傳回結果。<br/>             |
| [**XMVectorFloor**](/windows/win32/api/directxmath/nf-directxmath-xmvectorfloor)<br/>                                       | 計算 [**XMVECTOR**](xmvector-data-type.md)之每個元件的樓層。<br/>                             |
| [**XMVectorIsInfinite**](/windows/win32/api/directxmath/nf-directxmath-xmvectorisinfinite)<br/>                             | 在向量上執行 +/-無限大的每個元件測試。<br/>                                                    |
| [**XMVectorIsNaN**](/windows/win32/api/directxmath/nf-directxmath-xmvectorisnan)<br/>                                       | 在向量上執行每個元件的 NaN 測試。<br/>                                                                 |
| [**XMVectorMax**](/windows/win32/api/directxmath/nf-directxmath-xmvectormax)<br/>                                           | 進行兩個向量之間的個別元件比較，並傳回包含最大元件的向量。<br/>  |
| [**XMVectorMin**](/windows/win32/api/directxmath/nf-directxmath-xmvectormin)<br/>                                           | 在兩個向量之間進行個別元件的比較，並傳回包含最小元件的向量。<br/> |
| [**XMVectorMod**](/windows/win32/api/directxmath/nf-directxmath-xmvectormod)<br/>                                           | 計算兩個向量之商的每個元件浮點餘數。<br/>                            |
| [**XMVectorModAngles**](/windows/win32/api/directxmath/nf-directxmath-xmvectormodangles)<br/>                               | 計算每個元件的角度模數2PI。<br/>                                                                   |
| [**XMVectorMultiply**](/windows/win32/api/directxmath/nf-directxmath-xmvectormultiply)<br/>                                 | 計算兩個向量的每個元件乘積。<br/>                                                             |
| [**XMVectorMultiplyAdd**](/windows/win32/api/directxmath/nf-directxmath-xmvectormultiplyadd)<br/>                           | 計算新增至第三個向量的前兩個向量乘積。<br/>                                       |
| [**XMVectorNegate**](/windows/win32/api/directxmath/nf-directxmath-xmvectornegate)<br/>                                     | 計算向量的負。<br/>                                                                             |
| [**XMVectorNegativeMultiplySubtract**](/windows/win32/api/directxmath/nf-directxmath-xmvectornegativemultiplysubtract)<br/> | 計算第三個向量和前兩個向量乘積的差異。<br/>                            |
| [**XMVectorPow**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpow)<br/>                                           | 將 *V1* 計算為 *V2* 的乘冪。<br/>                                                                     |
| [**XMVectorReciprocal**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreciprocal)<br/>                             | 計算向量的每個元件。<br/>                                                             |
| [**XMVectorReciprocalEst**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreciprocalest)<br/>                       | 估計向量的每個元件。<br/>                                                            |
| [**XMVectorReciprocalSqrt**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreciprocalsqrt)<br/>                     | 計算向量的每個元件的交互平方根。<br/>                                                 |
| [**XMVectorReciprocalSqrtEst**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreciprocalsqrtest)<br/>               | 估計向量的每個元件的交互平方根。<br/>                                                |
| [**XMVectorRound**](/windows/win32/api/directxmath/nf-directxmath-xmvectorround)<br/>                                       | 將向量的每個元件四捨五入至最接近的整數。<br/>                                                      |
| [**XMVectorSaturate**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsaturate)<br/>                                 | 將向量的每個元件從 0.0 f 到 1.0 f 的範圍充滿。<br/>                                                |
| [**XMVectorScale**](/windows/win32/api/directxmath/nf-directxmath-xmvectorscale)<br/>                                       | 純量會將向量乘以浮點值。<br/>                                                          |
| [**XMVectorSqrt**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsqrt)<br/>                                         | 計算向量的每個元件平方根。<br/>                                                            |
| [**XMVectorSqrtEst**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsqrtest)<br/>                                   | 估計向量的每個元件平方根。<br/>                                                           |
| [**XMVectorSubtract**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsubtract)<br/>                                 | 計算兩個向量的差異。<br/>                                                                        |
| [**XMVectorSubtractAngles**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsubtractangles)<br/>                     | 減去代表角度的兩個向量。<br/>                                                                     |
| [**XMVectorSum**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsum)<br/>                                           | 計算 [**XMVECTOR**](xmvector-data-type.md)元件的水準總和。<br/>                    |
| [**XMVectorTruncate**](/windows/win32/api/directxmath/nf-directxmath-xmvectortruncate)<br/>                                 | 將向量的每個元件四捨五入為最接近的整數值（以零為方向）。<br/>                       |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectXMath 程式庫向量函數](ovw-xnamath-reference-functions-vector.md)
</dt> </dl>

 

 

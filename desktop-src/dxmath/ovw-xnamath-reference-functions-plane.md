---
description: 列出 DirectXMath 所提供的平面函數。
ms.assetid: 6505e72e-4af5-5db3-4fc0-f83fa77692b1
title: DirectXMath 程式庫平面函式
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b3f450b4dbaa5ed1b4348ad8b090210c14e2022
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983383"
---
# <a name="directxmath-library-plane-functions"></a>DirectXMath 程式庫平面函式

列出 DirectXMath 所提供的平面函數。

這些函式會使用 XMVECTOR 4 向量來代表平面方程式的係數，Ax + By + Cz + D = 0，其中 X 元件為 A，Y 元件為 B，Z 元件為 C，而 W 元件為 D。

## <a name="in-this-section"></a>本節內容



| 主題                                                               | 描述                                                                                                      |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [**XMPlaneDot**](/windows/win32/api/directxmath/nf-directxmath-xmplanedot)<br/>                         | 計算輸入平面與4D 向量之間的點乘積。<br/>                                    |
| [**XMPlaneDotCoord**](/windows/win32/api/directxmath/nf-directxmath-xmplanedotcoord)<br/>               | 計算輸入平面和3D 向量之間的點乘積。<br/>                                    |
| [**XMPlaneDotNormal**](/windows/win32/api/directxmath/nf-directxmath-xmplanedotnormal)<br/>             | 計算平面的一般向量和3D 向量之間的點乘積。<br/>                      |
| [**XMPlaneEqual**](/windows/win32/api/directxmath/nf-directxmath-xmplaneequal)<br/>                     | 判斷兩個平面是否相等。<br/>                                                                   |
| [**XMPlaneFromPointNormal**](/windows/win32/api/directxmath/nf-directxmath-xmplanefrompointnormal)<br/> | 計算平面的方程式，從平面中的某個點，到一般向量。<br/>           |
| [**XMPlaneFromPoints**](/windows/win32/api/directxmath/nf-directxmath-xmplanefrompoints)<br/>           | 計算平面中的三個點所構成平面的方程式。<br/>                          |
| [**XMPlaneIntersectLine**](/windows/win32/api/directxmath/nf-directxmath-xmplaneintersectline)<br/>     | 尋找平面和直線之間的交集。<br/>                                                    |
| [**XMPlaneIntersectPlane**](/windows/win32/api/directxmath/nf-directxmath-xmplaneintersectplane)<br/>   | 尋找兩個平面的交集。<br/>                                                                 |
| [**XMPlaneIsInfinite**](/windows/win32/api/directxmath/nf-directxmath-xmplaneisinfinite)<br/>           | 測試平面的任何係數是否為正數或負無限大。<br/>                    |
| [**XMPlaneIsNaN**](/windows/win32/api/directxmath/nf-directxmath-xmplaneisnan)<br/>                     | 測試平面的任何係數是否為 NaN。<br/>                                            |
| [**XMPlaneNearEqual**](/windows/win32/api/directxmath/nf-directxmath-xmplanenearequal)<br/>             | 判斷兩個平面是否幾乎相等。<br/>                                                       |
| [**XMPlaneNormalize**](/windows/win32/api/directxmath/nf-directxmath-xmplanenormalize)<br/>             | 正規化平面的係數，讓 x、y 和 z 的係數形成一個單元一般向量。<br/> |
| [**XMPlaneNormalizeEst**](/windows/win32/api/directxmath/nf-directxmath-xmplanenormalizeest)<br/>       | 預估平面的係數，讓 x、y 和 z 的係數形成一個單元一般向量。<br/>  |
| [**XMPlaneNotEqual**](/windows/win32/api/directxmath/nf-directxmath-xmplanenotequal)<br/>               | 判斷兩個平面是否不相等。<br/>                                                                 |
| [**XMPlaneTransform**](/windows/win32/api/directxmath/nf-directxmath-xmplanetransform)<br/>             | 依指定的矩陣轉換平面。<br/>                                                                 |
| [**XMPlaneTransformStream**](/windows/win32/api/directxmath/nf-directxmath-xmplanetransformstream)<br/> | 依指定的矩陣轉換平面的資料流程。<br/>                                                      |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectXMath 程式庫函式](ovw-xnamath-reference-functions.md)
</dt> </dl>

 

 

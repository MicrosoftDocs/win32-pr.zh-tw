---
description: 列出 DirectXMath 提供的矩陣函數。
ms.assetid: d59d0dcc-deae-3f7e-55c5-0c5ff383343b
title: DirectXMath 程式庫矩陣函數
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a91ecdef8389bf60594d370c2b3de01995bc1169
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826763"
---
# <a name="directxmath-library-matrix-functions"></a>DirectXMath 程式庫矩陣函數

列出 DirectXMath 提供的矩陣函數。

> [!Note]  
> DirectXMath 使用 ' handedness ' 提供矩陣函式的左手式和右手版本，但一律採用資料列主要格式。

 

## <a name="in-this-section"></a>本節內容



| 主題                                                                                               | 描述                                                                                                                            |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**XMMatrixAffineTransformation**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixaffinetransformation)<br/>                     | 建立仿射轉換矩陣。<br/>                                                                                     |
| [**XMMatrixAffineTransformation2D**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixaffinetransformation2d)<br/>                 | 在 xy 平面中建立2D 仿射轉換矩陣。 <br/>                                                                  |
| [**XMMatrixDecompose**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixdecompose)<br/>                                           | 將一般3D 轉換矩陣細分為其純量、旋轉和平移元件。<br/>                   |
| [**XMMatrixDeterminant**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixdeterminant)<br/>                                       | 計算矩陣的行列式。<br/>                                                                                       |
| [**XMMatrixIdentity**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixidentity)<br/>                                             | 建立身分識別矩陣。<br/>                                                                                                 |
| [**XMMatrixInverse**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixinverse)<br/>                                               | 計算矩陣的反向。<br/>                                                                                           |
| [**XMMatrixIsIdentity**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixisidentity)<br/>                                         | 測試矩陣是否為識別矩陣。<br/>                                                                              |
| [**XMMatrixIsInfinite**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixisinfinite)<br/>                                         | 測試矩陣的任何元素是否為正無限大或負無限大。<br/>                                            |
| [**XMMatrixIsNaN**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixisnan)<br/>                                                   | 測試矩陣的任何元素是否為 NaN。<br/>                                                                      |
| [**XMMatrixLookAtLH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixlookatlh)<br/>                                             | 使用相機位置、向上方向與焦點建置左手座標系統的視圖矩陣。<br/>       |
| [**XMMatrixLookAtRH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixlookatrh)<br/>                                             | 使用相機位置、向上方向與焦點建置右手座標系統的視圖矩陣。<br/>      |
| [**XMMatrixLookToLH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixlooktolh)<br/>                                             | 使用相機位置、向上方向與相機方向建置左手座標系統的視圖矩陣。<br/>  |
| [**XMMatrixLookToRH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixlooktorh)<br/>                                             | 使用相機位置、向上方向與相機方向建置右手座標系統的視圖矩陣。<br/> |
| [**XMMatrixMultiply**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixmultiply)<br/>                                             | 計算兩個矩陣的乘積。<br/>                                                                                       |
| [**XMMatrixMultiplyTranspose**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixmultiplytranspose)<br/>                           | 計算兩個矩陣的乘積的變換。<br/>                                                                      |
| [**XMMatrixOrthographicLH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixorthographiclh)<br/>                                 | 建置左手座標系統的正交投影矩陣。<br/>                                                 |
| [**XMMatrixOrthographicOffCenterLH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixorthographicoffcenterlh)<br/>               | 建置左手座標系統的自訂正交投影矩陣。<br/>                                           |
| [**XMMatrixOrthographicOffCenterRH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixorthographicoffcenterrh)<br/>               | 建置右手座標系統的自訂正交投影矩陣。<br/>                                          |
| [**XMMatrixOrthographicRH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixorthographicrh)<br/>                                 | 建置右手座標系統的正交投影矩陣。<br/>                                                |
| [**XMMatrixPerspectiveFovLH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixperspectivefovlh)<br/>                             | 根據視野範圍建置左手透視投影矩陣。<br/>                                                |
| [**XMMatrixPerspectiveFovRH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixperspectivefovrh)<br/>                             | 根據視野範圍建置右手透視投影矩陣。<br/>                                               |
| [**XMMatrixPerspectiveLH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixperspectivelh)<br/>                                   | 建置左手透視投影矩陣。<br/>                                                                         |
| [**XMMatrixPerspectiveOffCenterLH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixperspectiveoffcenterlh)<br/>                 | 建置自訂版本的左手透視投影矩陣。<br/>                                                     |
| [**XMMatrixPerspectiveOffCenterRH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixperspectiveoffcenterrh)<br/>                 | 建置自訂版本的右手透視投影矩陣。<br/>                                                    |
| [**XMMatrixPerspectiveRH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixperspectiverh)<br/>                                   | 建置右手透視投影矩陣。<br/>                                                                        |
| [**XMMatrixReflect**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixreflect)<br/>                                               | 建立轉換矩陣，其設計目的是要透過給定的平面來反映向量。<br/>                                           |
| [**XMMatrixRotationAxis**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationaxis)<br/>                                     | 建立圍繞任意軸旋轉的矩陣。<br/>                                                                      |
| [**XMMatrixRotationNormal**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationnormal)<br/>                                 | 建立可圍繞任意一般向量旋轉的矩陣。<br/>                                                             |
| [**XMMatrixRotationQuaternion**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationquaternion)<br/>                         | 從四元數建立旋轉矩陣。<br/>                                                                                 |
| [**XMMatrixRotationRollPitchYaw**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationrollpitchyaw)<br/>                     | 根據指定的音調、偏擺和 (歐拉角度) 來建立旋轉矩陣。<br/>                                              |
| [**XMMatrixRotationRollPitchYawFromVector**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationrollpitchyawfromvector)<br/> | 根據包含歐拉角度的向量來建立旋轉矩陣 (音調、偏擺和變換) 。<br/>                              |
| [**XMMatrixRotationX**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationx)<br/>                                           | 建立圍繞 X 軸旋轉的矩陣。<br/>                                                                             |
| [**XMMatrixRotationY**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationy)<br/>                                           | 建立圍繞 y 軸旋轉的矩陣。<br/>                                                                             |
| [**XMMatrixRotationZ**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationz)<br/>                                           | 建立圍繞 Z 軸旋轉的矩陣。<br/>                                                                             |
| [**XMMatrixScaling**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixscaling)<br/>                                               | 建立沿著 X 軸、y 軸和 Z 軸縮放的矩陣。<br/>                                                           |
| [**XMMatrixScalingFromVector**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixscalingfromvector)<br/>                           | 從3D 向量建立縮放矩陣。<br/>                                                                                   |
| [**XMMatrixSet**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixset)<br/>                                                       | 建立具有 **float** 值的矩陣。<br/>                                                                                     |
| [**XMMatrixShadow**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixshadow)<br/>                                                 | 建立將幾何壓平合併成平面的轉換矩陣。<br/>                                                         |
| [**XMMatrixTransformation**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixtransformation)<br/>                                 | 建立轉換矩陣。<br/>                                                                                             |
| [**XMMatrixTransformation2D**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixtransformation2d)<br/>                             | 在 xy 平面中建立2D 轉換矩陣。<br/>                                                                          |
| [**XMMatrixTranslation**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixtranslation)<br/>                                       | 從指定的位移建立平移矩陣。<br/>                                                                     |
| [**XMMatrixTranslationFromVector**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixtranslationfromvector)<br/>                   | 從向量建立轉譯矩陣。<br/>                                                                                  |
| [**XMMatrixTranspose**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixtranspose)<br/>                                           | 計算矩陣的變換。<br/>                                                                                         |
| [**XMMatrixVectorTensorProduct**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixvectortensorproduct)<br/>                                           | 計算2個向量的外部 tensor 乘積。<br/>                                                                                         |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectXMath 程式庫函式](ovw-xnamath-reference-functions.md)
</dt> </dl>

 

 

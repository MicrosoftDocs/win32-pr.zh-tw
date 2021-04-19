---
description: 列出 DirectXMath 所提供的四元數函數。
ms.assetid: 2d397c98-d0cd-08e0-6104-cca31bb6bd11
title: DirectXMath 程式庫四元數函數
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b085e336b19c9258a113b0442f339118f802146
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106995829"
---
# <a name="directxmath-library-quaternion-functions"></a>DirectXMath 程式庫四元數函數

列出 DirectXMath 所提供的四元數函數。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                                       | 描述                                                                                                     |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**XMQuaternionBaryCentric**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionbarycentric)<br/>                                       | 使用指定的四元數，傳回 barycentric 座標中的點。<br/>                         |
| [**XMQuaternionBaryCentricV**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionbarycentricv)<br/>                                     | 使用指定的四元數，傳回 barycentric 座標中的點。<br/>                         |
| [**XMQuaternionConjugate**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionconjugate)<br/>                                           | 計算四元數的共軛。<br/>                                                              |
| [**XMQuaternionDot**](/windows/win32/api/directxmath/nf-directxmath-xmquaterniondot)<br/>                                                       | 計算兩個四元數的點乘積。<br/>                                                         |
| [**XMQuaternionEqual**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionequal)<br/>                                                   | 測試兩個四元數是否相等。<br/>                                                             |
| [**XMQuaternionExp**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionexp)<br/>                                                       | 計算給定純四元數的指數。<br/>                                                 |
| [**XMQuaternionIdentity**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionidentity)<br/>                                             | 傳回識別四元數。<br/>                                                                     |
| [**XMQuaternionInverse**](/windows/win32/api/directxmath/nf-directxmath-xmquaternioninverse)<br/>                                               | 計算四元數的反向。<br/>                                                                |
| [**XMQuaternionIsIdentity**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionisidentity)<br/>                                         | 測試特定四元數是否為識別四元數。<br/>                                      |
| [**XMQuaternionIsInfinite**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionisinfinite)<br/>                                         | 測試四元數的任何元件是否為正數或負無限大。<br/>                  |
| [**XMQuaternionIsNaN**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionisnan)<br/>                                                   | 測試四元數的任何元件是否為 NaN。<br/>                                                 |
| [**XMQuaternionLength**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionlength)<br/>                                                 | 計算四元數的大小。<br/>                                                              |
| [**XMQuaternionLengthSq**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionlengthsq)<br/>                                             | 計算四元數大小的平方。<br/>                                                |
| [**XMQuaternionLn**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionln)<br/>                                                         | 計算指定單位四元數的自然對數。<br/>                                           |
| [**XMQuaternionMultiply**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionmultiply)<br/>                                             | 計算兩個四元數的乘積。<br/>                                                             |
| [**XMQuaternionNormalize**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionnormalize)<br/>                                           | 標準化四元數。<br/>                                                                             |
| [**XMQuaternionNormalizeEst**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionnormalizeest)<br/>                                     | 估計四元數的正規化版本。<br/>                                                    |
| [**XMQuaternionNotEqual**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionnotequal)<br/>                                             | 測試兩個四元數是否不相等。<br/>                                                         |
| [**XMQuaternionReciprocalLength**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionreciprocallength)<br/>                             | 計算四元數的倒數幅度。<br/>                                            |
| [**XMQuaternionRotationAxis**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionrotationaxis)<br/>                                     | 計算軸的旋轉四元數。<br/>                                                        |
| [**XMQuaternionRotationMatrix**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionrotationmatrix)<br/>                                 | 計算旋轉矩陣中的旋轉四元數。<br/>                                               |
| [**XMQuaternionRotationNormal**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionrotationnormal)<br/>                                 | 計算一般向量的旋轉四元數。<br/>                                              |
| [**XMQuaternionRotationRollPitchYaw**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionrotationrollpitchyaw)<br/>                     | 根據音調、偏擺和滾動 (歐拉角度) 來計算旋轉四元數。<br/>                     |
| [**XMQuaternionRotationRollPitchYawFromVector**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionrotationrollpitchyawfromvector)<br/> | 根據包含歐拉角度的向量來計算旋轉四元數 (音調、偏擺和滾動) 。<br/> |
| [**XMQuaternionSlerp**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionslerp)<br/>                                                   | 使用球面線性插補，在兩個單位四元數之間進行插補。<br/>                     |
| [**XMQuaternionSlerpV**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionslerpv)<br/>                                                 | 使用球面線性插補，在兩個單位四元數之間進行插補。<br/>                     |
| [**XMQuaternionSquad**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionsquad)<br/>                                                   | 使用球面四邊形插補，在四個單位四元數之間進行插補。<br/>                |
| [**XMQuaternionSquadSetup**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionsquadsetup)<br/>                                         | 提供球形四邊形插補的安裝控制點位址。<br/>                   |
| [**XMQuaternionSquadV**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionsquadv)<br/>                                                 | 使用球面四邊形插補，在四個單位四元數之間進行插補。<br/>                |
| [**XMQuaternionToAxisAngle**](/windows/win32/api/directxmath/nf-directxmath-xmquaterniontoaxisangle)<br/>                                       | 針對指定的四元數計算軸和旋轉的角度。<br/>                       |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectXMath 程式庫函式](ovw-xnamath-reference-functions.md)
</dt> </dl>

 

 

---
description: D3DXMath 是適用于 Direct3D 應用程式的數學協助程式程式庫。
ms.assetid: 3067d47f-9b1d-2051-fa24-2094418ea272
title: 使用 D3DXMath
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d463129a453a2b319dd72790bd4546dd90f63a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848472"
---
# <a name="working-with-d3dxmath"></a>使用 D3DXMath

D3DXMath 是適用于 Direct3D 應用程式的數學協助程式程式庫。 D3DXMath 是長期的，包含在 D3DX 9 和 D3DX 10，以及將日期傳回至舊版 DirectX。

> [!Note]  
> D3DX 公用程式程式庫 (D3DX 9、D3DX 10 和 D3DX 11) 已針對 Windows 8 取代，因此強烈建議您遷移至 DirectXMath，而不是使用 D3DXMath。

 

DirectXMath 在 D3DXMath 中共用許多相同的功能，而內部 D3DXMath 包含許多處理器特定的優化。 主要差異在於 D3DXMath 裝載于 D3DX9 中 \* 。Dll 和 D3DX10 \* 。Dll 和很少的函式都是內嵌的。 DirectXMath 程式庫呼叫慣例是明確的 SIMD，而 D3DXMath 必須執行負載和儲存轉換以實行 SIMD 優化。

## <a name="mixing-directxmath-and-d3dxmath"></a>混合 DirectXMath 和 D3DXMath

D3DX11 不包含 D3DXMath，但一般而言，我們建議改用 DirectXMath。 不過，您可以繼續連結至應用程式中的 D3DX9 和/或 D3DX10，因此您可以繼續使用 D3DXMath，或同時在您的應用程式中使用 D3DXMath 和 DirectXMath。

在一般情況中，將 XMVECTOR 轉換 \* 為接受 D3DXVECTOR4 的函式， \* 或將 XMMATRIX 轉換 \* 為採用 D3DXMATRIX 的函式 \* 是正常的。 不過，反向是不安全的，因為 XMVECTOR 和 XMMATRIX 必須是16位元組對齊，而 D3DXVECTOR4 和 D3DXMATRIX 則沒有這類需求。 若無法遵守此需求，可能會在執行時間產生不正確對齊例外狀況。

您可以安全地將 XMVECTOR \* 轉型為採用 D3DXVECTOR2 \* 或 D3DXVECTOR3 的函 \* 式，但反之亦然。 對齊考慮和 D3DXVECTOR2 和 D3DXVECTOR3 的事實都是較小的結構，使這項作業成為不安全的作業。

> [!Note]  
> D3DX (，因此 D3DXMath) 被視為舊版，並不適用于在 Windows 8 上執行的 Windows Store 應用程式，且不會包含在適用于桌面應用程式的 Windows 8 SDK 中。

 

## <a name="using-directxmath-with-direct3d"></a>搭配使用 DirectXMath 與 Direct3D

使用 Direct3D 時，DirectXMath 和 D3DXMath 都是選擇性的。 Direct3D 9 將 D3DMATRIX 和 D3DCOLOR 定義為 Direct3D API 的一部分，以支援 (現在是舊版) 固定函式管線。 D3DX9 中的 D3DXMath 會以常見的圖形數學運算來擴充這些 Direct3D 9 類型。 針對 Direct3D 2.x 和 Direct3D 11，API 只會使用可程式化的管線，因此矩陣或色彩值沒有 API 特定的結構。 當較新的 Api 需要色彩值時，它們會取得浮點值的明確陣列，或 HLSL 著色器所解讀之常數資料的一般緩衝區。 HLSL 本身可以支援資料列的主要或資料行主要矩陣格式，因此配置完全由您 (如需詳細資訊，請參閱 HLSL、 [矩陣順序](../direct3dhlsl/dx-graphics-hlsl-per-component-math.md);如果您在著色器中使用資料行主要矩陣格式，則在將 DirectXMath 矩陣資料放入常數緩衝區結構) 時，您需要將它變換。 雖然是選擇性的，DirectXMath 和 D3DXMath 程式庫都提供一般圖形相關的功能，因此在執行 Direct3D 程式設計時非常方便。

您可以安全地將 XMVECTOR 轉換 \* 為 D3DVECTOR \* 或 XMMATRIX \* ，以 D3DMATRIX， \* 因為 Direct3D 9 對內送資料結構沒有任何對齊假設。 將 XMCOLOR 轉換成 D3DCOLOR 也是安全的。 您可以透過 XMStoreColor () 將色彩的 4-float 標記法轉換成 XMCOLOR，以取得相當於 D3DCOLOR 的 8:8:8:8 32 位 DWORD。

使用 Direct3D 2.x 或 Direct3D 11 時，您通常會使用 DirectXMath 型別來建立每個常數緩衝區的結構，而在這些情況下，主要取決於您控制對齊方式以使其有效率的能力，或使用 XMStore \* () 作業將 XMVECTOR 和 XMMATRIX 資料轉換成正確的資料類型。 呼叫 Direct3D 2.x 或 Direct3D 11 Api （需要有 float \[ 4 \] 個色彩值陣列）時，您可以轉換 \* \* 包含色彩資料的 XMVECTOR 或 XMFLOAT4。

## <a name="porting-from-d3dxmath"></a>從 D3DXMath 移植



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>D3DXMath 類型</th>
<th>DirectXMath 對等專案</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3DXFLOAT16</td>
<td><a href="half-data-type.md"><strong>一半</strong></a></td>
</tr>
<tr class="even">
<td>D3DXMATRIX</td>
<td><a href="/windows/desktop/api/directxmath/ns-directxmath-xmfloat4x4"><strong>XMFLOAT4X4</strong></a></td>
</tr>
<tr class="odd">
<td>D3DXMATRIXA16</td>
<td><a href="/windows/desktop/api/directxmath/ns-directxmath-xmmatrix"><strong>XMMATRIX</strong></a>或<a href="/previous-versions/windows/desktop/legacy/ee419623(v=vs.85)"> <strong>XMFLOAT4X4A</strong></a></td>
</tr>
<tr class="even">
<td>D3DXQUATERNION<br/> D3DXPLANE<br/> D3DXCOLOR<br/></td>
<td>使用<a href="xmvector-data-type.md"><strong>XMVECTOR</strong></a> ，而不是具有唯一的類型，因此您可能需要使用<a href="/windows/desktop/api/directxmath/ns-directxmath-xmfloat4"> <strong>XMFLOAT4</strong></a>
<blockquote>
[!Note]<br />
[<strong>D3DXQUATERNION：： operator *</strong>] (。/direct3d9/d3dxquaternion-extensions.md) 會呼叫 <a href="/windows/desktop/direct3d9/d3dxquaternionmultiply"><strong>D3DXQuaternionMultiply</strong></a> 函數，這會將兩個四元數相乘。 但是，除非您明確使用 <a href="/windows/desktop/api/directxmath/nf-directxmath-xmquaternionmultiply"><strong>XMQuaternionMultiply</strong></a> 函式，否則當您在四元數上使用 <a href="xmvector-operator-mul.md"><strong>XMVECTOR：： operator *</strong></a> 時，會得到不正確的答案。
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>D3DXVECTOR2</td>
<td><a href="/windows/desktop/api/directxmath/ns-directxmath-xmfloat2"><strong>XMFLOAT2</strong></a></td>
</tr>
<tr class="even">
<td>D3DXVECTOR2_16F</td>
<td><a href="/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmhalf2"><strong>XMHALF2</strong></a></td>
</tr>
<tr class="odd">
<td>D3DXVECTOR3</td>
<td><a href="/windows/desktop/api/directxmath/ns-directxmath-xmfloat3"><strong>XMFLOAT3</strong></a></td>
</tr>
<tr class="even">
<td>D3DXVECTOR4</td>
<td><a href="/windows/desktop/api/directxmath/ns-directxmath-xmfloat4"><strong>XMFLOAT4</strong></a> (或您可以保證資料是16位元組對齊、 <a href="xmvector-data-type.md"><strong>XMVECTOR</strong></a> 或 <a href="/previous-versions/windows/desktop/legacy/ee419609(v=vs.85)"><strong>XMFLOAT4A</strong></a> ) <br/></td>
</tr>
<tr class="odd">
<td>D3DXVECTOR4_16F</td>
<td><a href="/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmhalf4"><strong>XMHALF4</strong></a></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> XNAMath 中沒有直接對等的 D3DXVECTOR3 \_ 16F。

 



| D3DXMath 宏 | DirectXMath 對等專案                            |
|----------------|---------------------------------------------------|
| D3DX \_ PI       | [XM \_ PI](ovw-xnamath-reference-constants.md)     |
| D3DX \_ 1BYPI    | [XM \_ 1DIVPI](ovw-xnamath-reference-constants.md) |
| D3DXToRadian   | [**XMConvertToRadians**](/windows/desktop/api/DirectXMath/nf-directxmath-xmconverttoradians)  |
| D3DXToDegree   | [**XMConvertToDegrees**](/windows/desktop/api/DirectXMath/nf-directxmath-xmconverttodegrees)  |



 



| D3DXMath 函式                  | DirectXMath 對等專案                                                                                                                                                                                                                           |
|------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DXBoxBoundProbe                  | [**BoundingBox：：交集 (XMVECTOR、XMVECTOR、float&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-intersects(fxmvector_fxmvector_float_))                                                                                                                                                          |
| D3DXComputeBoundingBox             | [**BoundingBox：： CreateFromPoints**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-createfrompoints)                                                                                                                                                                          |
| D3DXComputeBoundingSphere          | [**BoundingSphere::CreateFromPoints**](/windows/win32/api/directxcollision/nf-directxcollision-boundingsphere-createfrompoints)                                                                                                                                                                      |
| D3DXSphereBoundProbe               | [**BoundingSphere：：交集 (XMVECTOR、XMVECTOR、float&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingsphere-intersects(fxmvector_fxmvector_float_))                                                                                                                                                    |
| D3DXIntersectTriFunction           | [**TriangleTests：：交集**](ovw-xnamath-triangletests.md)                                                                                                                                                                                   |
| D3DXFloat32To16Array               | [**XMConvertFloatToHalfStream**](/windows/win32/api/directxpackedvector/nf-directxpackedvector-xmconvertfloattohalfstream)                                                                                                                                                                                 |
| D3DXFloat16To32Array               | [**XMConvertHalfToFloatStream**](/windows/win32/api/directxpackedvector/nf-directxpackedvector-xmconverthalftofloatstream)                                                                                                                                                                                 |
| D3DXVec2Length                     | [**XMVector2Length**](/windows/win32/api/directxmath/nf-directxmath-xmvector2length)或 [ **XMVector2LengthEst**](/windows/win32/api/directxmath/nf-directxmath-xmvector2lengthest)                                                                                                                                                   |
| D3DXVec2LengthSq                   | [**XMVector2LengthSq**](/windows/win32/api/directxmath/nf-directxmath-xmvector2lengthsq)                                                                                                                                                                                                   |
| D3DXVec2Dot                        | [**XMVector2Dot**](/windows/win32/api/directxmath/nf-directxmath-xmvector2dot)                                                                                                                                                                                                             |
| D3DXVec2CCW                        | [**XMVector2Cross**](/windows/win32/api/directxmath/nf-directxmath-xmvector2cross)                                                                                                                                                                                                         |
| D3DXVec2Add                        | [**XMVectorAdd**](/windows/win32/api/directxmath/nf-directxmath-xmvectoradd)                                                                                                                                                                                                               |
| D3DXVec2Subtract                   | [**XMVectorSubtract**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsubtract)                                                                                                                                                                                                     |
| D3DXVec2Minimize                   | [**XMVectorMin**](/windows/win32/api/directxmath/nf-directxmath-xmvectormin)                                                                                                                                                                                                               |
| D3DXVec2Maximize                   | [**XMVectorMax**](/windows/win32/api/directxmath/nf-directxmath-xmvectormax)                                                                                                                                                                                                               |
| D3DXVec2Scale                      | [**XMVectorScale**](/windows/win32/api/directxmath/nf-directxmath-xmvectorscale)                                                                                                                                                                                                           |
| D3DXVec2Lerp                       | [**XMVectorLerp**](/windows/win32/api/directxmath/nf-directxmath-xmvectorlerp)或 [ **XMVectorLerpV**](/windows/win32/api/directxmath/nf-directxmath-xmvectorlerpv)                                                                                                                                                                   |
| D3DXVec2Normalize                  | [**XMVector2Normalize**](/windows/win32/api/directxmath/nf-directxmath-xmvector2normalize)或 [ **XMVector2NormalizeEst**](/windows/win32/api/directxmath/nf-directxmath-xmvector2normalizeest)                                                                                                                                       |
| D3DXVec2Hermite                    | [**XMVectorHermite**](/windows/win32/api/directxmath/nf-directxmath-xmvectorhermite)或 [ **XMVectorHermiteV**](/windows/win32/api/directxmath/nf-directxmath-xmvectorhermitev)                                                                                                                                                       |
| D3DXVec2CatmullRom                 | [**XMVectorCatmullRom**](/windows/win32/api/directxmath/nf-directxmath-xmvectorcatmullrom)或 [ **XMVectorCatmullRomV**](/windows/win32/api/directxmath/nf-directxmath-xmvectorcatmullromv)                                                                                                                                           |
| D3DXVec2BaryCentric                | [**XMVectorBaryCentric**](/windows/win32/api/directxmath/nf-directxmath-xmvectorbarycentric)或 [ **XMVectorBaryCentricV**](/windows/win32/api/directxmath/nf-directxmath-xmvectorbarycentricv)                                                                                                                                       |
| D3DXVec2Transform                  | [**XMVector2Transform**](/windows/win32/api/directxmath/nf-directxmath-xmvector2transform)                                                                                                                                                                                                 |
| D3DXVec2TransformCoord             | [**XMVector2TransformCoord**](/windows/win32/api/directxmath/nf-directxmath-xmvector2transformcoord)                                                                                                                                                                                       |
| D3DXVec2TransformNormal            | [**XMVector2TransformNormal**](/windows/win32/api/directxmath/nf-directxmath-xmvector2transformnormal)                                                                                                                                                                                     |
| D3DXVec2TransformArray             | [**XMVector2TransformStream**](/windows/win32/api/directxmath/nf-directxmath-xmvector2transformstream)                                                                                                                                                                                     |
| D3DXVec2TransformCoordArray        | [**XMVector2TransformCoordStream**](/windows/win32/api/directxmath/nf-directxmath-xmvector2transformcoordstream)                                                                                                                                                                           |
| D3DXVec2TransformNormalArray       | [**XMVector2TransformNormalStream**](/windows/win32/api/directxmath/nf-directxmath-xmvector2transformnormalstream)                                                                                                                                                                         |
| D3DXVec3Length                     | [**XMVector3Length**](/windows/win32/api/directxmath/nf-directxmath-xmvector3length)或 [ **XMVector3LengthEst**](/windows/win32/api/directxmath/nf-directxmath-xmvector3lengthest)                                                                                                                                                   |
| D3DXVec3LengthSq                   | [**XMVector3LengthSq**](/windows/win32/api/directxmath/nf-directxmath-xmvector3lengthsq)                                                                                                                                                                                                   |
| D3DXVec3Dot                        | [**XMVector3Dot**](/windows/win32/api/directxmath/nf-directxmath-xmvector3dot)                                                                                                                                                                                                             |
| D3DXVec3Cross                      | [**XMVector3Cross**](/windows/win32/api/directxmath/nf-directxmath-xmvector3cross)                                                                                                                                                                                                         |
| D3DXVec3Add                        | [**XMVectorAdd**](/windows/win32/api/directxmath/nf-directxmath-xmvectoradd)                                                                                                                                                                                                               |
| D3DXVec3Subtract                   | [**XMVectorSubtract**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsubtract)                                                                                                                                                                                                     |
| D3DXVec3Minimize                   | [**XMVectorMin**](/windows/win32/api/directxmath/nf-directxmath-xmvectormin)                                                                                                                                                                                                               |
| D3DXVec3Maximize                   | [**XMVectorMax**](/windows/win32/api/directxmath/nf-directxmath-xmvectormax)                                                                                                                                                                                                               |
| D3DXVec3Scale                      | [**XMVectorScale**](/windows/win32/api/directxmath/nf-directxmath-xmvectorscale)                                                                                                                                                                                                           |
| D3DXVec3Lerp                       | [**XMVectorLerp**](/windows/win32/api/directxmath/nf-directxmath-xmvectorlerp)或 [ **XMVectorLerpV**](/windows/win32/api/directxmath/nf-directxmath-xmvectorlerpv)                                                                                                                                                                   |
| D3DXVec3Normalize                  | [**XMVector3Normalize**](/windows/win32/api/directxmath/nf-directxmath-xmvector3normalize)或 [ **XMVector3NormalizeEst**](/windows/win32/api/directxmath/nf-directxmath-xmvector3normalizeest)                                                                                                                                       |
| D3DXVec3Hermite                    | [**XMVectorHermite**](/windows/win32/api/directxmath/nf-directxmath-xmvectorhermite)或 [ **XMVectorHermiteV**](/windows/win32/api/directxmath/nf-directxmath-xmvectorhermitev)                                                                                                                                                       |
| D3DXVec3CatmullRom                 | [**XMVectorCatmullRom**](/windows/win32/api/directxmath/nf-directxmath-xmvectorcatmullrom)或 [ **XMVectorCatmullRomV**](/windows/win32/api/directxmath/nf-directxmath-xmvectorcatmullromv)                                                                                                                                           |
| D3DXVec3BaryCentric                | [**XMVectorBaryCentric**](/windows/win32/api/directxmath/nf-directxmath-xmvectorbarycentric)或 [ **XMVectorBaryCentricV**](/windows/win32/api/directxmath/nf-directxmath-xmvectorbarycentricv)                                                                                                                                       |
| D3DXVec3Transform                  | [**XMVector3Transform**](/windows/win32/api/directxmath/nf-directxmath-xmvector3transform)                                                                                                                                                                                                 |
| D3DXVec3TransformCoord             | [**XMVector3TransformCoord**](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformcoord)                                                                                                                                                                                       |
| D3DXVec3TransformNormal            | [**XMVector3TransformNormal**](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformnormal)                                                                                                                                                                                     |
| D3DXVec3TransformArray             | [**XMVector3TransformStream**](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformstream)                                                                                                                                                                                     |
| D3DXVec3TransformCoordArray        | [**XMVector3TransformCoordStream**](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformcoordstream)                                                                                                                                                                           |
| D3DXVec3TransformNormalArray       | [**XMVector3TransformNormalStream**](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformnormalstream)                                                                                                                                                                         |
| D3DXVec3Project                    | [**XMVector3Project**](/windows/win32/api/directxmath/nf-directxmath-xmvector3project)                                                                                                                                                                                                     |
| D3DXVec3Unproject                  | [**XMVector3Unproject**](/windows/win32/api/directxmath/nf-directxmath-xmvector3unproject)                                                                                                                                                                                                 |
| D3DXVec3ProjectArray               | [**XMVector3ProjectStream**](/windows/win32/api/directxmath/nf-directxmath-xmvector3projectstream)                                                                                                                                                                                         |
| D3DXVec3UnprojectArray             | [**XMVector3UnprojectStream**](/windows/win32/api/directxmath/nf-directxmath-xmvector3unprojectstream)                                                                                                                                                                                     |
| D3DXVec4Length                     | [**XMVector4Length**](/windows/win32/api/directxmath/nf-directxmath-xmvector4length)或 [ **XMVector4LengthEst**](/windows/win32/api/directxmath/nf-directxmath-xmvector4lengthest)                                                                                                                                                   |
| D3DXVec4LengthSq                   | [**XMVector4LengthSq**](/windows/win32/api/directxmath/nf-directxmath-xmvector4lengthsq)                                                                                                                                                                                                   |
| D3DXVec4Dot                        | [**XMVector4Dot**](/windows/win32/api/directxmath/nf-directxmath-xmvector4dot)                                                                                                                                                                                                             |
| D3DXVec4Add                        | [**XMVectorAdd**](/windows/win32/api/directxmath/nf-directxmath-xmvectoradd)                                                                                                                                                                                                               |
| D3DXVec4Subtract                   | [**XMVectorSubtract**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsubtract)                                                                                                                                                                                                     |
| D3DXVec4Minimize                   | [**XMVectorMin**](/windows/win32/api/directxmath/nf-directxmath-xmvectormin)                                                                                                                                                                                                               |
| D3DXVec4Maximize                   | [**XMVectorMax**](/windows/win32/api/directxmath/nf-directxmath-xmvectormax)                                                                                                                                                                                                               |
| D3DXVec4Scale                      | [**XMVectorScale**](/windows/win32/api/directxmath/nf-directxmath-xmvectorscale)                                                                                                                                                                                                           |
| D3DXVec4Lerp                       | [**XMVectorLerp**](/windows/win32/api/directxmath/nf-directxmath-xmvectorlerp)或 [ **XMVectorLerpV**](/windows/win32/api/directxmath/nf-directxmath-xmvectorlerpv)                                                                                                                                                                   |
| D3DXVec4Cross                      | [**XMVector4Cross**](/windows/win32/api/directxmath/nf-directxmath-xmvector4cross)                                                                                                                                                                                                         |
| D3DXVec4Normalize                  | [**XMVector4Normalize**](/windows/win32/api/directxmath/nf-directxmath-xmvector4normalize)或 [ **XMVector4NormalizeEst**](/windows/win32/api/directxmath/nf-directxmath-xmvector4normalizeest)                                                                                                                                       |
| D3DXVec4Hermite                    | [**XMVectorHermite**](/windows/win32/api/directxmath/nf-directxmath-xmvectorhermite)或 [ **XMVectorHermiteV**](/windows/win32/api/directxmath/nf-directxmath-xmvectorhermitev)                                                                                                                                                       |
| D3DXVec4CatmullRom                 | [**XMVectorCatmullRom**](/windows/win32/api/directxmath/nf-directxmath-xmvectorcatmullrom)或 [ **XMVectorCatmullRomV**](/windows/win32/api/directxmath/nf-directxmath-xmvectorcatmullromv)                                                                                                                                           |
| D3DXVec4BaryCentric                | [**XMVectorBaryCentric**](/windows/win32/api/directxmath/nf-directxmath-xmvectorbarycentric)或 [ **XMVectorBaryCentricV**](/windows/win32/api/directxmath/nf-directxmath-xmvectorbarycentricv)                                                                                                                                       |
| D3DXVec4Transform                  | [**XMVector4Transform**](/windows/win32/api/directxmath/nf-directxmath-xmvector4transform)                                                                                                                                                                                                 |
| D3DXVec4TransformArray             | [**XMVector4TransformStream**](/windows/win32/api/directxmath/nf-directxmath-xmvector4transformstream)                                                                                                                                                                                     |
| D3DXMatrixIdentity                 | [**XMMatrixIdentity**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixidentity)                                                                                                                                                                                                     |
| D3DXMatrixDeterminant              | [**XMMatrixDeterminant**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixdeterminant)                                                                                                                                                                                               |
| D3DXMatrixDecompose                | [**XMMatrixDecompose**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixdecompose)                                                                                                                                                                                                   |
| D3DXMatrixTranspose                | [**XMMatrixTranspose**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixtranspose)                                                                                                                                                                                                   |
| D3DXMatrixMultiply                 | [**XMMatrixMultiply**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixmultiply)                                                                                                                                                                                                     |
| D3DXMatrixMultiplyTranspose        | [**XMMatrixMultiplyTranspose**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixmultiplytranspose)                                                                                                                                                                                   |
| D3DXMatrixInverse                  | [**XMMatrixInverse**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixinverse)                                                                                                                                                                                                       |
| D3DXMatrixScaling                  | [**XMMatrixScaling**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixscaling)                                                                                                                                                                                                       |
| D3DXMatrixTranslation              | [**XMMatrixTranslation**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixtranslation)                                                                                                                                                                                               |
| D3DXMatrixRotationX                | [**XMMatrixRotationX**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationx)                                                                                                                                                                                                   |
| D3DXMatrixRotationY                | [**XMMatrixRotationY**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationy)                                                                                                                                                                                                   |
| D3DXMatrixRotationZ                | [**XMMatrixRotationZ**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationz)                                                                                                                                                                                                   |
| D3DXMatrixRotationAxis             | [**XMMatrixRotationAxis**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationaxis)                                                                                                                                                                                             |
| D3DXMatrixRotationQuaternion       | [**XMMatrixRotationQuaternion**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationquaternion)                                                                                                                                                                                 |
| D3DXMatrixRotationYawPitchRoll     | [**XMMatrixRotationRollPitchYaw**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationrollpitchyaw) (注意參數的順序不同： D3DXMatrixRotationYawPitchRoll 會採用偏擺、音調、變換、 **XMMatrixRotationRollPitchYaw** 接受音調、偏擺、變換)                  |
| D3DXMatrixTransformation           | [**XMMatrixTransformation**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixtransformation)                                                                                                                                                                                         |
| D3DXMatrixTransformation2D         | [**XMMatrixTransformation2D**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixtransformation2d)                                                                                                                                                                                     |
| D3DXMatrixAffineTransformation     | [**XMMatrixAffineTransformation**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixaffinetransformation)                                                                                                                                                                             |
| D3DXMatrixAffineTransformation2D   | [**XMMatrixAffineTransformation2D**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixaffinetransformation2d)                                                                                                                                                                         |
| D3DXMatrixLookAtRH                 | [**XMMatrixLookAtRH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixlookatrh)                                                                                                                                                                                                     |
| D3DXMatrixLookAtLH                 | [**XMMatrixLookAtLH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixlookatlh)                                                                                                                                                                                                     |
| D3DXMatrixPerspectiveRH            | [**XMMatrixPerspectiveRH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixperspectiverh)                                                                                                                                                                                           |
| D3DXMatrixPerspectiveLH            | [**XMMatrixPerspectiveLH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixperspectivelh)                                                                                                                                                                                           |
| D3DXMatrixPerspectiveFovRH         | [**XMMatrixPerspectiveFovRH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixperspectivefovrh)                                                                                                                                                                                     |
| D3DXMatrixPerspectiveFovLH         | [**XMMatrixPerspectiveFovLH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixperspectivefovlh)                                                                                                                                                                                     |
| D3DXMatrixPerspectiveOffCenterRH   | [**XMMatrixPerspectiveOffCenterRH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixperspectiveoffcenterrh)                                                                                                                                                                         |
| D3DXMatrixPerspectiveOffCenterLH   | [**XMMatrixPerspectiveOffCenterLH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixperspectiveoffcenterlh)                                                                                                                                                                         |
| D3DXMatrixOrthoRH                  | [**XMMatrixOrthographicRH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixorthographicrh)                                                                                                                                                                                         |
| D3DXMatrixOrthoLH                  | [**XMMatrixOrthographicLH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixorthographiclh)                                                                                                                                                                                         |
| D3DXMatrixOrthoOffCenterRH         | [**XMMatrixOrthographicOffCenterRH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixorthographicoffcenterrh)                                                                                                                                                                       |
| D3DXMatrixOrthoOffCenterLH         | [**XMMatrixOrthographicOffCenterLH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixorthographicoffcenterlh)                                                                                                                                                                       |
| D3DXMatrixShadow                   | [**XMMatrixShadow**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixshadow)                                                                                                                                                                                                         |
| D3DXMatrixReflect                  | [**XMMatrixReflect**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixreflect)                                                                                                                                                                                                       |
| D3DXQuaternionLength               | [**XMQuaternionLength**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionlength)                                                                                                                                                                                                 |
| D3DXQuaternionLengthSq             | [**XMQuaternionLengthSq**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionlengthsq)                                                                                                                                                                                             |
| D3DXQuaternionDot                  | [**XMQuaternionDot**](/windows/win32/api/directxmath/nf-directxmath-xmquaterniondot)                                                                                                                                                                                                       |
| D3DXQuaternionIdentity             | [**XMQuaternionIdentity**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionidentity)                                                                                                                                                                                             |
| D3DXQuaternionIsIdentity           | [**XMQuaternionIsIdentity**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionisidentity)                                                                                                                                                                                         |
| D3DXQuaternionConjugate            | [**XMQuaternionConjugate**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionconjugate)                                                                                                                                                                                           |
| D3DXQuaternionToAxisAngle          | [**XMQuaternionToAxisAngle**](/windows/win32/api/directxmath/nf-directxmath-xmquaterniontoaxisangle)                                                                                                                                                                                       |
| D3DXQuaternionRotationMatrix       | [**XMQuaternionRotationMatrix**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionrotationmatrix)                                                                                                                                                                                 |
| D3DXQuaternionRotationAxis         | [**XMQuaternionRotationAxis**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionrotationaxis)                                                                                                                                                                                     |
| D3DXQuaternionRotationYawPitchRoll | [**XMQuaternionRotationRollPitchYaw**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionrotationrollpitchyaw) (注意參數的順序不同： D3DXQuaternionRotationYawPitchRoll 會採用偏擺、音調、變換、 **XMQuaternionRotationRollPitchYaw** 接受音調、偏擺、變換)  |
| D3DXQuaternionMultiply             | [**XMQuaternionMultiply**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionmultiply)                                                                                                                                                                                             |
| D3DXQuaternionNormalize            | [**XMQuaternionNormalize**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionnormalize)或 [ **XMQuaternionNormalizeEst**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionnormalizeest)                                                                                                                           |
| D3DXQuaternionInverse              | [**XMQuaternionInverse**](/windows/win32/api/directxmath/nf-directxmath-xmquaternioninverse)                                                                                                                                                                                               |
| D3DXQuaternionLn                   | [**XMQuaternionLn**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionln)                                                                                                                                                                                                         |
| D3DXQuaternionExp                  | [**XMQuaternionExp**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionexp)                                                                                                                                                                                                       |
| D3DXQuaternionSlerp                | [**XMQuaternionSlerp**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionslerp)或 [ **XMQuaternionSlerpV**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionslerpv)                                                                                                                                               |
| D3DXQuaternionSquad                | [**XMQuaternionSquad**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionsquad)或 [ **XMQuaternionSquadV**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionsquadv)                                                                                                                                               |
| D3DXQuaternionSquadSetup           | [**XMQuaternionSquadSetup**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionsquadsetup)                                                                                                                                                                                         |
| D3DXQuaternionBaryCentric          | [**XMQuaternionBaryCentric**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionbarycentric)或 [ **XMQuaternionBaryCentricV**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionbarycentricv)                                                                                                                       |
| D3DXPlaneDot                       | [**XMPlaneDot**](/windows/win32/api/directxmath/nf-directxmath-xmplanedot)                                                                                                                                                                                                                 |
| D3DXPlaneDotCoord                  | [**XMPlaneDotCoord**](/windows/win32/api/directxmath/nf-directxmath-xmplanedotcoord)                                                                                                                                                                                                       |
| D3DXPlaneDotNormal                 | [**XMPlaneDotNormal**](/windows/win32/api/directxmath/nf-directxmath-xmplanedotnormal)                                                                                                                                                                                                     |
| D3DXPlaneScale                     | [**XMVectorScale**](/windows/win32/api/directxmath/nf-directxmath-xmvectorscale)                                                                                                                                                                                                           |
| D3DXPlaneNormalize                 | [**XMPlaneNormalize**](/windows/win32/api/directxmath/nf-directxmath-xmplanenormalize)或 [ **XMPlaneNormalizeEst**](/windows/win32/api/directxmath/nf-directxmath-xmplanenormalizeest)                                                                                                                                               |
| D3DXPlaneIntersectLine             | [**XMPlaneIntersectLine**](/windows/win32/api/directxmath/nf-directxmath-xmplaneintersectline)                                                                                                                                                                                             |
| D3DXPlaneFromPointNormal           | [**XMPlaneFromPointNormal**](/windows/win32/api/directxmath/nf-directxmath-xmplanefrompointnormal)                                                                                                                                                                                         |
| D3DXPlaneFromPoints                | [**XMPlaneFromPoints**](/windows/win32/api/directxmath/nf-directxmath-xmplanefrompoints)                                                                                                                                                                                                   |
| D3DXPlaneTransform                 | [**XMPlaneTransform**](/windows/win32/api/directxmath/nf-directxmath-xmplanetransform)                                                                                                                                                                                                     |
| D3DXPlaneTransformArray            | [**XMPlaneTransformStream**](/windows/win32/api/directxmath/nf-directxmath-xmplanetransformstream)                                                                                                                                                                                         |
| D3DXColorNegative                  | [**XMColorNegative**](/windows/win32/api/directxmath/nf-directxmath-xmcolornegative)                                                                                                                                                                                                       |
| D3DXColorAdd                       | [**XMVectorAdd**](/windows/win32/api/directxmath/nf-directxmath-xmvectoradd)                                                                                                                                                                                                               |
| D3DXColorSubtract                  | [**XMVectorSubtract**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsubtract)                                                                                                                                                                                                     |
| D3DXColorScale                     | [**XMVectorScale**](/windows/win32/api/directxmath/nf-directxmath-xmvectorscale)                                                                                                                                                                                                           |
| D3DXColorModulate                  | [**XMColorModulate**](/windows/win32/api/directxmath/nf-directxmath-xmcolormodulate)                                                                                                                                                                                                       |
| D3DXColorLerp                      | [**XMVectorLerp**](/windows/win32/api/directxmath/nf-directxmath-xmvectorlerp)或 [ **XMVectorLerpV**](/windows/win32/api/directxmath/nf-directxmath-xmvectorlerpv)                                                                                                                                                                   |
| D3DXColorAdjustSaturation          | [**XMColorAdjustSaturation**](/windows/win32/api/directxmath/nf-directxmath-xmcoloradjustsaturation)                                                                                                                                                                                       |
| D3DXColorAdjustContrast            | [**XMColorAdjustContrast**](/windows/win32/api/directxmath/nf-directxmath-xmcoloradjustcontrast)                                                                                                                                                                                           |
| D3DXFresnelTerm                    | [**XMFresnelTerm**](/windows/win32/api/directxmath/nf-directxmath-xmfresnelterm)                                                                                                                                                                                                           |



 

> [!Note]  
> 適用于 DirectXMath 的[球面諧波](https://github.com/Microsoft/DirectXMath/tree/master/SHMath)函式會分開提供。 沒有與 **ID3DXMatrixStack** 相等的 DirectXMath。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectXMath 程式設計指南](ovw-xnamath-progguide.md)
</dt> </dl>

 

 

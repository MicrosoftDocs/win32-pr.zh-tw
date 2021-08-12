---
description: 在整個 Direct3D 中，頂點描述位置及方向。 原始物件中的每個頂點都由給予它位置、色彩、紋理座標的向量，以及給予它方向的標準向量所述。
ms.assetid: f18b235c-97ff-4779-8584-8e96b62c7ca3
title: " (Direct3D 9 的向量、頂點和四元數) "
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 601b6a71dcb00356d4de4637a6aabb1eba5c02e49c62380b32732351d15bfcb4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118290437"
---
# <a name="vectors-vertices-and-quaternions-direct3d-9"></a> (Direct3D 9 的向量、頂點和四元數) 

在整個 Direct3D 中，頂點描述位置及方向。 原始物件中的每個頂點都由給予它位置、色彩、紋理座標的向量，以及給予它方向的標準向量所述。

四元數會將第四個元素新增至 \[ \] 定義三個分量向量的 x、y、z 值。 四元數是通常用於 3D 旋轉之矩陣方法的替代方法。 四元數代表 3D 空間中的軸以及圍繞該軸的旋轉。 例如，四元數可能表示 (1,1,2) 軸及 1 弧度旋轉。 四元數載有重要資訊，但其真正的力量來自於您可以在其上執行兩項作業︰組合和內插補點。

對四元數執行組合類似於結合它們。 兩個四元數的組合如下圖表示。

![四元數標記法的圖例](images/quateq.png)

兩個套用到幾何之四元數的組合表示「圍繞軸₂ 和旋轉角度₂ 旋轉幾何，然後圍繞軸₁ 和旋轉角度₁ 旋轉幾何。」 在此情況下，Q 代表圍繞單一軸的旋轉，這是先套用 q₂ 再套用 q₁ 到幾何的結果。

使用四元數內插補點，應用程式可以計算從某個軸和方向到另一個軸和方向順暢且合理的路徑。 因此，q₁ 和 q₂ 之間內插補點提供從某個方向動畫到另一個方向的簡單方法。

當您一起使用組合和內插補點時，它讓您輕鬆進行看似複雜的幾何操作。 例如，想像您有想要旋轉到特定方向的幾何。 您知道您想要將它圍繞軸₂ 旋轉 r₂ 度，然後圍繞軸₁ 旋轉 r₁ 度，但您不知道最終四元數。 使用組合，您可能會在幾何上組合兩個旋轉，取得單一四元數結果。 然後，您可以從原始四元數到組合四元數內插值，達到平滑轉換。

D3DX 公用程式程式庫包含可協助您使用四元數的函數。 例如， [**D3DXQuaternionRotationAxis**](d3dxquaternionrotationaxis.md) 函式會將旋轉值新增至定義旋轉軸的向量，並將結果傳回 [**D3DXQUATERNION**](d3dxquaternion.md) 結構所定義的四元數。 此外， [**D3DXQuaternionMultiply**](d3dxquaternionmultiply.md) 函數會撰寫四元數，而 [**D3DXQuaternionSlerp**](d3dxquaternionslerp.md) 則會在兩個四元數之間執行球形線性插補。

Direct3D 應用程式可使用下列函式來簡化處理四元數的工作。

-   [**D3DXQuaternionBaryCentric**](d3dxquaternionbarycentric.md)
-   [**D3DXQuaternionConjugate**](d3dxquaternionconjugate.md)
-   [**D3DXQuaternionDot**](d3dxquaterniondot.md)
-   [**D3DXQuaternionExp**](d3dxquaternionexp.md)
-   [**D3DXQuaternionIdentity**](d3dxquaternionidentity.md)
-   [**D3DXQuaternionInverse**](d3dxquaternioninverse.md)
-   [**D3DXQuaternionIsIdentity**](d3dxquaternionisidentity.md)
-   [**D3DXQuaternionLength**](d3dxquaternionlength.md)
-   [**D3DXQuaternionLengthSq**](d3dxquaternionlengthsq.md)
-   [**D3DXQuaternionLn**](d3dxquaternionln.md)
-   [**D3DXQuaternionMultiply**](d3dxquaternionmultiply.md)
-   [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md)
-   [**D3DXQuaternionRotationAxis**](d3dxquaternionrotationaxis.md)
-   [**D3DXQuaternionRotationMatrix**](d3dxquaternionrotationmatrix.md)
-   [**D3DXQuaternionRotationYawPitchRoll**](d3dxquaternionrotationyawpitchroll.md)
-   [**D3DXQuaternionSlerp**](d3dxquaternionslerp.md)
-   [**D3DXQuaternionSquad**](d3dxquaternionsquad.md)
-   [**D3DXQuaternionToAxisAngle**](d3dxquaterniontoaxisangle.md)

Direct3D 應用程式可使用下列函式來簡化使用三個元件向量的工作。

-   [**D3DXVec3Add**](d3dxvec3add.md)
-   [**D3DXVec3BaryCentric**](d3dxvec3barycentric.md)
-   [**D3DXVec3CatmullRom**](d3dxvec3catmullrom.md)
-   [**D3DXVec3Cross**](d3dxvec3cross.md)
-   [**D3DXVec3Dot**](d3dxvec3dot.md)
-   [**D3DXVec3Hermite**](d3dxvec3hermite.md)
-   [**D3DXVec3Length**](d3dxvec3length.md)
-   [**D3DXVec3LengthSq**](d3dxvec3lengthsq.md)
-   [**D3DXVec3Lerp**](d3dxvec3lerp.md)
-   [**D3DXVec3Maximize**](d3dxvec3maximize.md)
-   [**D3DXVec3Minimize**](d3dxvec3minimize.md)
-   [**D3DXVec3Normalize**](d3dxvec3normalize.md)
-   [**D3DXVec3Project**](d3dxvec3project.md)
-   [**D3DXVec3Scale**](d3dxvec3scale.md)
-   [**D3DXVec3Subtract**](d3dxvec3subtract.md)
-   [**D3DXVec3Transform**](d3dxvec3transform.md)
-   [**D3DXVec3TransformCoord**](d3dxvec3transformcoord.md)
-   [**D3DXVec3TransformNormal**](d3dxvec3transformnormal.md)
-   [**D3DXVec3Unproject**](d3dxvec3unproject.md)

D3DX 公用程式程式庫所提供的 [數學](dx9-graphics-reference-d3dx-functions-math.md) 函式包含許多額外的函式，可簡化使用雙和四個元件向量的工作。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[座標系統和幾何](coordinate-systems-and-geometry.md)
</dt> </dl>

 

 




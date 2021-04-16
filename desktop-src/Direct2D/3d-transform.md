---
title: 3D 轉換效果
description: 使用3D 轉換效果將任意4x4 轉換矩陣套用至影像。
ms.assetid: BC2F2837-40F0-4293-A190-8B5F81BB01B6
keywords:
- 3d 轉換效果
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fabe0c2c220038802b5218b54187a1ff89268bfa
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/28/2021
ms.locfileid: "104561958"
---
# <a name="3d-transform-effect"></a>3D 轉換效果

使用3D 轉換效果將任意4x4 轉換矩陣套用至影像。

此效果會將矩陣 (M？ ) 您提供給來源影像的邊角頂點 (\[ x y z 1 \]) 使用此計算：

\[x<sub>r</sub> y<sub>r</sub> z<sub>r</sub> 1 \] = \[ x y z 1 \] \* M？

這項效果的 CLSID 是 CLSID \_ D2D13DTransform。

-   [範例影像](#example-image)
-   [效果屬性](#effect-properties)
    -   [插補模式](#interpolation-modes)
    -   [框線模式](#border-modes)
-   [4x4 轉換矩陣類別](#4x4-transform-matrix-class)
-   [需求](#requirements)
-   [相關主題](#related-topics)

## <a name="example-image"></a>範例影像



| 之前                                                        |
|---------------------------------------------------------------|
| ![轉換之前的影像。](images/default-before.jpg) |
| After                                                         |
| ![轉換後的影像。](images/24-3dtransform.png)  |



 


```C++
ComPtr<ID2D1Effect> D2D13DTransformEffect;
m_d2dContext->CreateEffect(CLSID_D2D13DTransform, &D2D13DTransformEffect);

D2D13DTransformEffect->SetInput(0, bitmap);

// You can use the helper methods in D2D1::Matrix4x4F to create common matrix transformations.
D2D1_MATRIX_4X4_F matrix = 
    D2D1::Matrix4x4F::Translation(0.0f, -192.0f, 0.0f) *
    D2D1::Matrix4x4F::RotationY(30.0f) *
    D2D1::Matrix4x4F::Translation(0.0f, 192.0f, 0.0f);

D2D13DTransformEffect->SetValue(D2D1_3DTRANSFORM_PROP_TRANSFORM_MATRIX, matrix);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(D2D13DTransformEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>效果屬性



<table>
<thead>
<tr class="header">
<th>顯示名稱和索引列舉</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>InterpolationMode<br/> D2D1_3DTRANSFORM_PROP_INTERPOLATION_MODE<br/></td>
<td>效果在影像上使用的插補模式。 有5種調整模式的品質和速度。<br/> 類型為 D2D1_3DTRANSFORM_INTERPOLATION_MODE。<br/> 預設值為 D2D1_3DTRANSFORM_INTERPOLATION_MODE_LINEAR。<br/></td>
</tr>
<tr class="even">
<td>BorderMode<br/> D2D1_3DTRANSFORM_PROP_BORDER_MODE<br/></td>
<td>用來計算影像（軟或硬）框線的模式。 如需詳細資訊，請參閱 <a href="https://www.bing.com/search?q=Border+modes">框線模式</a> 。<br/> 類型為 D2D1_BORDER_MODE。<br/> 預設值為 D2D1_BORDER_MODE_SOFT。<br/></td>
</tr>
<tr class="odd">
<td>TransformMatrix<br/> D2D1_3DTRANSFORM_PROP_TRANSFORM_MATRIX<br/></td>
<td>套用至投射平面的4x4 轉換矩陣。 下列矩陣計算可用來將某個3D 座標系統的點對應到轉換的2D 座標系統。 <br/><img src="images/3d-transform-matrix1.png" alt="3D Depth Matrix" />其中：<dl> X、Y、Z = 輸入投射平面座標<br />
M<sub>x、y</sub> = 轉換矩陣元素<br />
X、Y、Z = 輸出投射平面座標<br />
</dl> <br/> 個別的矩陣元素未系結，而且沒有單位。 <br/> 類型為 D2D1_MATRIX_4X4_F。<br/> 預設值為 Matrix4x4F (1、0、0、0、0、1、0、0、0、0、1、0、0、0、0、1) 。<br/></td>
</tr>
</tbody>
</table>



 

### <a name="interpolation-modes"></a>插補模式



| 列舉型別                                                   | 描述                                                                                                                                                |
|---------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ \_ \_ \_ 最接近 \_ 鄰近的 D2D1 3DTRANSFORM 插補模式     | 範例最接近的單一點，並使用該點。 這個模式會使用較少的處理時間，但會輸出最低品質的影像。                                 |
| D2D1 \_ 3DTRANSFORM \_ 插補 \_ 模式 \_ 線性                | 使用四個點取樣和線性插補。 這個模式所使用的處理時間比最近的鄰近模式更多，但會輸出較高品質的影像。 |
| D2D1 \_ 3DTRANSFORM \_ 插補 \_ 模式 \_ 立方                 | 使用16個範例三核心來進行插補。 這個模式會使用大部分的處理時間，但會輸出較高品質的影像。                              |
| D2D1 \_ 3DTRANSFORM \_ 插補 \_ 模式 \_ 多 \_ 樣本 \_ 線性 | 使用單一圖元內的4個線性樣本來取得良好的邊緣消除鋸齒。 這種模式適合用來在具有少量圖元的影像上相應減少量。    |
| D2D1 \_ 3DTRANSFORM \_ 插補 \_ 模式 \_ 各向異性           | 根據點陣圖的轉換圖形，使用非等向篩選來取樣模式。                                                           |



 

> [!Note]  
> 如果您未選取模式，效果會預設為 D2D1 \_ 3DTRANSFORM \_ 插補 \_ 模式 \_ 線性。

 

> [!Note]  
> 當調整時，非等向模式會產生 mipmap，不過，如果您在輸入至此效果的效果上將快取 **的屬性設** 為 true，則每次都不會針對足夠的小型影像產生 mipmap。

 

### <a name="border-modes"></a>框線模式



| Name                     | 描述                                                                                                      |
|--------------------------|------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ 框線 \_ 模式 \_ 軟 | 效果會在插補時以透明黑色圖元來填補影像，進而產生軟邊緣。<br/> |
| D2D1 \_ 框線 \_ 模式 \_ 硬性 | 效果會將輸出個至輸入影像的大小。 <br/>                                         |



 

## <a name="4x4-transform-matrix-class"></a>4x4 轉換矩陣類別

Direct2D 提供4x4 矩陣類別，以提供協助程式函式來轉換3個維度中的影像。 如需詳細資訊和所有類別成員的描述，請參閱 [**Matrix4x4F**](/windows/desktop/api/d2d1_1helper/nl-d2d1_1helper-matrix4x4f) 主題。



| 函式                                | 描述                                                                                    | Matrix                                                 |
|-----------------------------------------|------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| Matrix4x4F：： Scale (X、Y、Z)               | 產生會以 X、Y 和/或 Z 方向調整投射平面的轉換矩陣。 | ![scale3d 矩陣](images/3d-transform-matrix2.png)     |
| SkewX (X)                                 | 產生會以 X 方向扭曲投射平面的轉換矩陣。               | ![顯示 X 方向的扭曲矩陣。](images/matrix4x4-skewx.png)             |
| SkewY (Y)                                 | 產生會在 Y 方向扭曲投射平面的轉換矩陣。               | ![扭曲矩陣](images/matrix4x4-skewy.png)             |
| 轉譯 (X、Y、Z)                     | 產生會以 X、Y 或 Z 方向轉譯投射平面的轉換矩陣。 | ![轉譯矩陣](images/3d-transform-matrix4.png)   |
| RotationX (X)                             | 產生會旋轉 X 軸之投射平面的轉換矩陣。               | ![旋轉 x 矩陣](images/3d-transform-matrix5.png)    |
| RotationY (Y)                             | 產生會旋轉 Y 軸的投射平面的轉換矩陣。               | ![旋轉 y 矩陣](images/3d-transform-matrix6.png)    |
| RotationZ (Z)                             | 產生會旋轉 Z 軸的投射平面的轉換矩陣。               | ![旋轉 z 矩陣](images/3d-transform-matrix7.png)    |
| PerspectiveProjection (D)                 | 深度值為 D 的透視圖轉換。                                          | ![透視圖矩陣](images/3d-transform-matrix8.png) |
| RotationArbitraryAxis (X、Y、Z、度數)  | 針對您指定的軸旋轉投射平面。                                       |                                                        |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端 | 適用于 Windows 7 desktop app 的 Windows 8 和平臺更新 \[ \| windows Store 應用程式\] |
| 最低支援的伺服器 | 適用于 Windows 7 desktop app 的 Windows 8 和平臺更新 \[ \| windows Store 應用程式\] |
| 標頭                   | d2d1effects。h                                                                      |
| 程式庫                  | d2d1 .lib，dxguid .lib                                                               |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 


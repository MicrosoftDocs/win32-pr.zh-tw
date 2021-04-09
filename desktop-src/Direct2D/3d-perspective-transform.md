---
title: 3D 透視轉換效果
description: 使用3D 透視轉換效果，將影像旋轉為3個尺寸，就像從距離觀看一樣。
ms.assetid: 0E1A940E-2DCA-4772-BB68-7E5EF5CEF833
keywords:
- 3d 透視轉換效果
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ed2b1c5131319dd711d2c7802a0bfabceaaa32e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844427"
---
# <a name="3d-perspective-transform-effect"></a>3D 透視轉換效果

使用3D 透視轉換效果，將影像旋轉為3個尺寸，就像從距離觀看一樣。

3D 的觀點轉換比3D 轉換效果更為方便，但只會公開功能的子集。 您可以計算完整的3D 轉換矩陣，並使用 [3d 轉換](3d-transform.md) 效果將更多任意的轉換矩陣套用至影像。

這項效果的 CLSID 是 CLSID \_ D2D13DPerspectiveTransform。

-   [範例影像](#example-image)
-   [效果屬性](#effect-properties)
-   [插補模式](#interpolation-modes)
-   [框線模式](#border-modes)
-   [輸出點陣圖](#output-bitmap)
-   [需求](#requirements)
-   [相關主題](#related-topics)

## <a name="example-image"></a>範例影像



| 之前                                                               |
|----------------------------------------------------------------------|
| ![效果之前的影像。](images/default-before.jpg)           |
| After                                                                |
| ![效果之後的影像。](images/23-3dperspectivetransform.png) |



 


```C++
ComPtr<ID2D1Effect> perspectiveTransformEffect;
m_d2dContext->CreateEffect(CLSID_D2D13DPerspectiveTransform, &perspectiveTransformEffect);

perspectiveTransformEffect->SetInput(0, bitmap);

perspectiveTransformEffect->SetValue(D2D1_3DPERSPECTIVETRANSFORM_PROP_PERSPECTIVE_ORIGIN, D2D1::Vector3F(0.0f, 192.0f, 0.0f));
perspectiveTransformEffect->SetValue(D2D1_3DPERSPECTIVETRANSFORM_PROP_ROTATION, D2D1::Vector3F(0.0f, 30.0f, 0.0f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(perspectiveTransformEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>效果屬性



| 顯示名稱和索引列舉                                                              | Description                                                                                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| InterpolationMode<br/> D2D1 \_ 3DPERSPECTIVETRANSFORM \_ 的 \_ 內插補點 \_ 模式<br/> | 效果在影像上使用的插補模式。 有5種調整模式的品質和速度。<br/> 類型為 D2D1 \_ 3DPERSPECTIVETRANSFORM \_ 插補 \_ 模式。<br/> 預設值為 D2D1 \_ 3DPERSPECTIVETRANSFORM \_ 插補 \_ 模式 \_ 線性。<br/>              |
| BorderMode<br/> D2D1 \_ 3DPERSPECTIVETRANSFORM \_ 的 \_ 樣式框線 \_ 模式<br/>               | 用來計算影像（軟或硬）框線的模式。 如需詳細資訊，請參閱 [框線模式](https://www.bing.com/search?q=Border+modes) 。<br/> 類型為 D2D1 \_ 框線 \_ 模式。<br/> 預設值為 [D2D1 \_ 框線 \_ 模式] \_ 。<br/>                                                              |
| 深度<br/> D2D1 \_ 3DPERSPECTIVETRANSFORM \_ 的 \_ 深度<br/>                           | 從 *PerspectiveOrigin* 到投射平面的距離。 在 Dip 中指定的值必須大於0。<br/> 類型為 FLOAT。<br/> 預設值為 1000.0 f。<br/>                                                                                               |
| PerspectiveOrigin<br/> D2D1 \_ 3DPERSPECTIVETRANSFORM \_ 的 \_ 觀點 \_ 來源<br/> | 3D 場景中檢視器的 X 和 Y 位置。 這個屬性是 \_ \_ 定義為： (point X，point Y) 的 D2D1 向量2f。 單位為 Dip。<br/> 您可以使用 *Depth* 屬性來設定 Z 值。<br/> 類型為 D2D1 \_ VECTOR \_ 2f。<br/> 預設值為 {0.0 f，0.0 f}。<br/> |
| LocalOffset<br/> D2D1 \_ 3DPERSPECTIVETRANSFORM \_ 的 \_ 局部 \_ 位移<br/>             | 效果在旋轉投射平面之前所執行的轉譯。 這個屬性是 \_ \_ 定義為： (X、Y、Z) 的 D2D1 向量3F。 單位為 Dip。<br/> 類型為 D2D1 \_ VECTOR \_ 3F。<br/> 預設值為 {0.0 f、0.0 f、0.0 f}。<br/>                                        |
| GlobalOffset<br/> D2D1 \_ 3DPERSPECTIVETRANSFORM \_ 的 \_ 通用 \_ 位移<br/>           | 效果在旋轉投射平面之後所執行的轉譯。 這個屬性是 \_ \_ 定義為： (X、Y、Z) 的 D2D1 向量3F。 單位為 Dip。<br/> 類型為 D2D1 \_ VECTOR \_ 3F。<br/> 預設值為 {0.0 f、0.0 f、0.0 f}。<br/>                                         |
| RotationOrigin<br/> D2D1 \_ 3DPERSPECTIVETRANSFORM 的型 \_ \_ 旋轉 \_ 來源<br/>       | 效果所執行之旋轉的中心點。 這個屬性是 \_ \_ 定義為： (X、Y、Z) 的 D2D1 向量3F。 單位為 Dip。<br/> 類型為 D2D1 \_ VECTOR \_ 3F。<br/> 預設值為 {0.0 f、0.0 f、0.0 f}。<br/>                                                            |
| 旋轉<br/> D2D1 \_ 3DPERSPECTIVETRANSFORM 的型 \_ \_ 旋轉<br/>                     | 每個軸的旋轉角度。 這個屬性是 \_ \_ 定義為： (X、Y、Z) 的 D2D1 向量3F。 單位是以度為單位。<br/> 類型為 D2D1 \_ VECTOR \_ 3F。<br/> 預設值為 {0.0 f、0.0 f、0.0 f}。<br/>                                                                         |



 

## <a name="interpolation-modes"></a>插補模式



| 列舉型別                                                              | 描述                                                                                                                                                |
|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ \_ \_ \_ 最接近 \_ 鄰近的 D2D1 3DPERSPECTIVETRANSFORM 插補模式     | 範例最接近的單一點，並使用該點。 這個模式會使用較少的處理時間，但會輸出最低品質的影像。                                 |
| D2D1 \_ 3DPERSPECTIVETRANSFORM \_ 插補 \_ 模式 \_ 線性                | 使用四個點取樣和線性插補。 這個模式所使用的處理時間比最近的鄰近模式更多，但會輸出較高品質的影像。 |
| D2D1 \_ 3DPERSPECTIVETRANSFORM \_ 插補 \_ 模式 \_ 立方                 | 使用16個範例三核心來進行插補。 這個模式會使用大部分的處理時間，但會輸出較高品質的影像。                              |
| D2D1 \_ 3DPERSPECTIVETRANSFORM \_ 插補 \_ 模式 \_ 多 \_ 樣本 \_ 線性 | 使用單一圖元內的4個線性樣本來取得良好的邊緣消除鋸齒。 這種模式適合用來在具有少量圖元的影像上相應減少量。    |
| D2D1 \_ 3DPERSPECTIVETRANSFORM \_ 插補 \_ 模式 \_ 各向異性           | 根據點陣圖的轉換圖形，使用非等向篩選來取樣模式。                                                           |



 

> [!Note]  
> 如果您未選取模式，效果會預設為 D2D1 \_ 3DPERSPECTIVETRANSFORM \_ 插補 \_ 模式 \_ 線性。

 

> [!Note]  
> 當調整時，非等向模式會產生 mipmap，不過，如果您在輸入至此效果的效果上將快取 **的屬性設** 為 true，則每次都不會針對足夠的小型影像產生 mipmap。

 

## <a name="border-modes"></a>框線模式



| Name                     | 描述                                                                                                      |
|--------------------------|------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ 框線 \_ 模式 \_ 軟 | 效果會在插補時以透明黑色圖元來填補影像，進而產生軟邊緣。<br/> |
| D2D1 \_ 框線 \_ 模式 \_ 硬性 | 效果會將輸出個至輸入影像的大小。 <br/>                                         |



 

## <a name="output-bitmap"></a>輸出點陣圖

輸出點陣圖的大小取決於套用至影像的轉換矩陣。

效果會執行轉換作業，然後在結果周圍套用周框方塊。 輸出點陣圖是周框方塊的大小。

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

 


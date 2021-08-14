---
title: '轉換 (DirectComposition) '
description: 本主題討論 Microsoft DirectComposition 對二維 (2D) 仿射 (線性) 轉換的支援，並說明 DirectComposition 支援的轉換類型。
ms.assetid: a0f41cc6-e848-4831-8063-609e17d9b4c6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c8cc34975ab8304300a1523269808775107f4ce0554432da8c3c04a01f25881
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118504771"
---
# <a name="transforms-directcomposition"></a>轉換 (DirectComposition) 

> [!NOTE]
> 針對 Windows 10 上的應用程式，我們建議使用 Windows 的撰寫 api，而不是 DirectComposition。 如需詳細資訊，請參閱 [使用視覺分層將您的桌面應用程式現代化](/windows/uwp/composition/visual-layer-in-desktop-apps)。

本主題討論 Microsoft DirectComposition 對二維 (2D) 仿射 (線性) 轉換的支援，並說明 DirectComposition 支援的轉換類型。

DirectComposition 也支援3D 的觀點轉換，但因為它們需要建立中繼點陣圖，所以 DirectComposition 會將它們視為效果，而不是轉換。 如需3D 透視圖轉換效果的詳細資訊，請參閱 [效果](effects.md)。

本主題包含下列章節：

-   [什麼是 DirectComposition 2D 轉換？](#what-is-a-directcomposition-2d-transform)
-   [DirectComposition 2D 座標空間](#the-directcomposition-2d-coordinate-space)
-   [支援仿射2D 轉換](#support-for-affine-2d-transforms)
-   [矩陣2D 轉換](#matrix-2d-transforms)
-   [轉換群組](#transform-groups)
-   [轉換動畫](#transform-animation)
-   [相關主題](#related-topics)

## <a name="what-is-a-directcomposition-2d-transform"></a>什麼是 DirectComposition 2D 轉換？

2D 轉換可讓您藉由將視覺效果移至另一個位置 (轉譯) ，讓它變得更大或更小 (調整) 、將它 (旋轉) ，或扭曲其形狀 (扭曲) 。

2D 轉換的達成方式是將視覺效果的點從某個位置對應到相同座標空間內的另一個位置，或從某個座標空間對應到另一個位置。 這項對應是由稱為轉換矩陣的值表所描述，定義為三個數據列的集合，其中有三個浮點值的資料行，如下表所示。

:::row:::
    :::column:::
        M11Default：1。0<br/>
        M21Default：0。0<br/>
        M31OffsetX：0。0
    :::column-end:::
    :::column:::
        M12Default：0。0<br/>
        M22Default：1。0<br/>
        M32OffsetY：0。0
    :::column-end:::
    :::column:::
        0.0<br/>
        0.0<br/>
        1.0
    :::column-end:::
:::row-end:::

仿射2D 轉換的轉換矩陣是從上一個轉換矩陣省略第三個數據行的3到2個矩陣。 下表顯示此矩陣的版面配置。

:::row:::
    :::column:::
        M11Default：1。0<br/>
        M21Default：0。0<br/>
        M31OffsetX：0。0
    :::column-end:::
    :::column:::
        M12Default：0。0<br/>
        M22Default：1。0<br/>
        M32OffsetY：0。0
    :::column-end:::
:::row-end:::

> [!Note]  
> 將2D 轉換套用至身歷聲內容時，DirectComposition 不會執行任何特殊處理。 這表示在套用2D 轉換時，3D 內容可能會失真。

 

## <a name="the-directcomposition-2d-coordinate-space"></a>DirectComposition 2D 座標空間

DirectComposition 會使用左手式2D 座標空間;也就是說，正 X 軸的值會增加到右邊，且 y 軸值會向下增加。 視覺效果的位置相對於原點，也就是 X 軸和 y 軸相交 (0，0) 的點，如下圖所示。

![左手座標空間的 X 軸和 y 軸](images/coordinatespace.png)

藉由在 3 x 2 轉換矩陣中操作值，您可以旋轉、縮放、扭曲和轉譯兩個維度中的物件。 例如，如果您將 OffsetX 設定為100，並將 OffsetY 設為200，則會將物件移至右邊的100圖元和下200圖元。

## <a name="support-for-affine-2d-transforms"></a>支援仿射2D 轉換

下表說明 DirectComposition 所支援的仿射2D 轉換類型，並列出您可以用來執行各種類型轉換的介面。



| 轉換/介面                                                                               | 描述                                                                                              | 圖例                                                                                                                      |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| 輪替 2D [**idcompositionrotatetransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrotatetransform) \[ 換行\]          | 依據指定的中心點，以指定的角度旋轉視覺效果。                                 | ![以順時針方向與原始正方形中央旋轉45度的圖例](images/rotate.png)               |
| 調整 2D [**idcompositionscaletransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionscaletransform)的 \[ 新行\]             | 依指定的中心點依指定的因素調整視覺效果。                                 | ![調整130% 的正方形圖例](images/scale.png)                                                                  |
| 扭曲 2D [**idcompositionskewtransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionskewtransform) \[ 換行\]                | 沿著 X 軸和 y 軸上的指定角度扭曲視覺效果，以及圍繞指定的中心點。 | ![從 y 軸逆時針算起30度的正方形圖例](images/skew.png)                                   |
| 轉譯 2D [**idcompositiontranslatetransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositiontranslatetransform) \[ 換行\] | 以 X 軸和 y 軸的方向變更視覺效果的位置。                               | ![正方形的圖，沿著正 X 軸移動20個單位，沿著正 y 軸移動10個單位](images/translate.png) |



 

## <a name="matrix-2d-transforms"></a>矩陣2D 轉換

[**IDCompositionMatrixTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionmatrixtransform)介面可讓您定義自己的三2仿射2d 轉換矩陣，並將其套用至視覺效果。 如果您需要套用無法透過其他 DirectComposition 轉換介面使用的仿射2D 轉換類型，這個介面會很有用。 您可以藉由填妥 [**D2D \_ 矩陣 \_ 3X2 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) 結構，並將它傳遞至 [**IDCompositionMatrixTransform：： SetMatrix**](/windows/win32/api/dcomp/nf-dcomp-idcompositionmatrixtransform-setmatrix) 方法，來定義矩陣。

## <a name="transform-groups"></a>轉換群組

您可以使用轉換群組，將多個轉換合併成一個。 轉換群組定義的轉換物件集合，其矩陣會以集合中指定的順序相乘。 接著會將產生的轉換矩陣套用至視覺效果。 轉換群組會產生與個別套用每個轉換相同的結果。

請記住，轉換群組中的轉換物件順序很重要。 例如，如果先旋轉視覺效果，然後進行縮放，然後轉譯，結果會與第一次轉譯視覺效果，然後旋轉然後縮放的結果不同。 DirectComposition 一律會依照在集合中指定的順序，將轉換套用至視覺效果。

若要建立轉換群組，請先建立要包含在群組中的轉換物件，然後將轉換物件指標的陣列傳遞至 [**IDCompositionDevice：： CreateTransformGroup**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtransformgroup) 方法。 建立轉換群組之後，您無法新增或移除任何轉換物件。 不過，您可以修改集合中個別轉換物件的屬性，而變更將會反映在產生的轉換矩陣中。

## <a name="transform-animation"></a>轉換動畫

轉換的屬性可進行動畫。 當屬性有動畫時，DirectComposition 會變更一段時間的屬性值，而不是一次全部變更。 這在建立轉換時特別有用。 如需詳細資訊，請參閱 [動畫](animation.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectComposition 概念](directcomposition-concepts.md)
</dt> </dl>

 

 

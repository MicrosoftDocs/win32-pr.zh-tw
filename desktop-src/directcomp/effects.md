---
title: '效果 (DirectComposition) '
description: 本主題討論 Microsoft DirectComposition 效果的基本概念，並說明 DirectComposition 支援的效果類型。
ms.assetid: 805B17D2-2F6B-4C25-8C6D-41FFA5DFC774
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cfd1ca154dcbc7e55ca65cc34d04cfa7d73ccee
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375672"
---
# <a name="effects-directcomposition"></a>效果 (DirectComposition) 

> [!NOTE]
> 針對 Windows 10 上的應用程式，我們建議使用 DirectComposition，而不是使用。 如需詳細資訊，請參閱 [使用視覺分層將您的桌面應用程式現代化](/windows/uwp/composition/visual-layer-in-desktop-apps)。

本主題討論 Microsoft DirectComposition 效果的基本概念，並說明 DirectComposition 支援的效果類型。

本主題包含下列幾節：

-   [什麼是 DirectComposition 效果？](#what-is-a-directcomposition-effect)
-   [不透明度](#opacity)
-   [3D 透視轉換效果](#3d-perspective-transform-effects)
    -   [DirectComposition 3D 座標空間](#the-directcomposition-3d-coordinate-space)
    -   [3D 旋轉轉換效果](#3d-rotation-transform-effect)
    -   [3D 縮放轉換效果](#3d-scaling-transform-effect)
    -   [3D 轉譯轉換效果](#3d-translation-transform-effect)
    -   [3D 矩陣轉換效果](#3d-matrix-transform-effect)
    -   [3D 轉換效果群組](#3d-transform-effect-group)
-   [效果物件](#effect-objects)
-   [相關主題](#related-topics)

## <a name="what-is-a-directcomposition-effect"></a>什麼是 DirectComposition 效果？

DirectComposition *效果* 是一種點陣圖作業，會在視覺效果的點陣化期間套用，以某種方式變更視覺效果的外觀。

DirectComposition 會建立效果，方法是取得視覺化子樹，然後將它轉譯成單一點陣圖，然後再套用效果。 例如，若要建立3D 外觀轉換效果，DirectComposition 會產生視覺子樹狀結構的影像，然後將影像紋理至3D 平面，此平面會根據3D 轉換效果的產生矩陣進行轉換。

DirectComposition 支援下列類型的效果。



| 效果類型                                                   | Description                                                                |
|---------------------------------------------------------------|----------------------------------------------------------------------------|
| [不透明度](#opacity)                                           | 設定整個視覺效果的不透明度。                                      |
| [3D 透視轉換](#3d-perspective-transform-effects) | 將三維 (3D) 透視圖效果轉換成視覺效果。 |



 

> [!Note]  
> 將效果套用至3D 身歷聲內容時，DirectComposition 不會執行任何特殊處理。 這表示在套用效果時，3D 內容可能會失真。

 

## <a name="opacity"></a>不透明度

不透明度效果可讓您設定在呈現視覺效果時，套用至整個視覺效果的不透明度因數。 它與 Alpha 遮罩不同之處在于，相同的不透明度因數會套用至視覺效果中的所有圖元。 指定不透明度的值範圍為 0 (完全透明) 為 1 (完全不透明) 。

不透明度因數會從父代套用至子視覺效果，但是不會在個別子視覺效果的屬性值中指出嵌套不透明度設定的可見效果。 比方說，如果根視覺效果有 50% (0.5) 不透明度，其中一個子系具有20% 的 (0.2) 不透明度，該子系的淨不透明度會轉譯為 10% (0.1) ，但子系的不透明度屬性值仍會是0.2。

## <a name="3d-perspective-transform-effects"></a>3D 透視轉換效果

本節說明 DirectComposition 用於執行3D 透視圖轉換效果的座標空間。 它也會說明 DirectComposition 支援的3D 透視圖轉換效果類型。

-   [DirectComposition 3D 座標空間](#the-directcomposition-3d-coordinate-space)
-   [3D 旋轉轉換效果](#3d-rotation-transform-effect)
-   [3D 縮放轉換效果](#3d-scaling-transform-effect)
-   [3D 轉譯轉換效果](#3d-translation-transform-effect)
-   [3D 矩陣轉換效果](#3d-matrix-transform-effect)
-   [3D 轉換效果群組](#3d-transform-effect-group)

> [!Note]  
> 在 DirectComposition 中，將3D 效果套用至視覺化樹狀結構中的多個層級，其運作方式與使用完整3D 引擎（例如 Microsoft Direct3D）時的方式相同。 例如，假設有一個具有單一子視覺效果的父視覺效果。 如果子視覺效果在 z 方向向前旋轉 (圍繞90度的 y 軸) ，則子視覺效果邊緣的邊緣會顯示檢視器，因此我們預期視覺效果將不會顯示 (因為點陣圖沒有真正的深度) 。 如果父視覺效果接著以負 z 方向向前旋轉 (y 軸) 90 度，則可能會預期子視覺效果會變成完全可見的 (，因為轉換會將每個) 都否定。 不過，在 DirectComposition 中不是這樣。 子視覺效果將不會顯示，因為它已「壓平合併為」父點陣圖。

 

### <a name="the-directcomposition-3d-coordinate-space"></a>DirectComposition 3D 座標空間

3D 轉換效果的 DirectComposition 座標空間會找出點陣圖介面左上角的原點 (0、0、0) ，其中正 X 軸的值會往右、正 y 軸的值往下往下，而從原點往外的正 Z 軸值朝檢視器往外移動。 下圖顯示 DirectComposition 3D 座標空間。

![directcompostion 3d 座標空間](images/3d-coordinate-space.png)

### <a name="3d-rotation-transform-effect"></a>3D 旋轉轉換效果

3D 旋轉轉換效果會依據旋轉軸向量 \[ x、y、z \] 位於指定中心 (點的旋轉軸向量 x、y、z) 來旋轉三個維度中的視覺效果。 角度是以度為單位來指定。 預設的旋轉軸向量為 \[ 0、0、-1 \] ，而預設中心點是 (0、0、0) 。

使用 [**IDCompositionDevice：： CreateRotateTransform3D**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createrotatetransform3d) 方法來建立3d 旋轉轉換物件。 方法會抓取 [**IDCompositionRotateTransform3D**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrotatetransform3d) 介面，讓您用來設定物件的屬性。

### <a name="3d-scaling-transform-effect"></a>3D 縮放轉換效果

3D 縮放轉換效果可讓視覺效果更大或更小。 它會以 x、y、z) 的中心點縮放視覺效果， \[ \] (x，y，z。 預設中心點是 (0、0、0) 。

使用 [**IDCompositionDevice：： CreateScaleTransform3D**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createscaletransform3d) 方法來建立3d 縮放轉換物件。 方法會抓取 [**IDCompositionScaleTransform3D**](/windows/win32/api/dcomp/nn-dcomp-idcompositionscaletransform3d) 介面，讓您用來設定物件的屬性。

### <a name="3d-translation-transform-effect"></a>3D 轉譯轉換效果

3D 轉譯轉換效果會以 \[ x、y、z 方向變更視覺效果的位置 \] 。

使用 [**IDCompositionDevice：： CreateTranslateTransform3D**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtranslatetransform3d) 方法來建立3d 轉譯轉換物件。 方法會抓取 [**IDCompositionTranslateTransform3D**](/windows/win32/api/dcomp/nn-dcomp-idcompositiontranslatetransform3d) 介面，讓您用來設定物件的屬性。

### <a name="3d-matrix-transform-effect"></a>3D 矩陣轉換效果

[**IDCompositionMatrixTransform3D**](/windows/win32/api/dcomp/nn-dcomp-idcompositionmatrixtransform)介面可讓您定義自己的 4 4 轉換矩陣，並將其套用至視覺效果。 如果您需要套用無法透過其他 DirectComposition 3D 轉換效果介面使用的3D 透視圖轉換效果類型，這個介面會很有用。 您可以藉由填滿 [**D3DMATRIX**](/windows/desktop/direct3d10/d3d10-d3dmatrix) 結構，並將它傳遞至 [**IDCompositionMatrixTransform3D：： SetMatrix**](/windows/win32/api/dcomp/nf-dcomp-idcompositionmatrixtransform-setmatrix) 方法，來定義矩陣。 或者，您可以使用 [**IDCompositionMatrixTransform3D：： SetMatrixElement**](/previous-versions/windows/desktop/legacy/hh437429(v=vs.85)) 方法來設定矩陣的每個元素。

### <a name="3d-transform-effect-group"></a>3D 轉換效果群組

[**IDCompositionDevice：： CreateTransform3DGroup**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtransform3dgroup)會建立3d 轉換效果的集合，您可以將其套用至視覺效果做為群組。 陣列可包含任意數目的轉換物件，而且可以包含矩陣、旋轉、縮放和轉譯轉換。 3D 轉換物件的集合會產生轉換，其值為集合中個別轉換矩陣的矩陣乘法。

群組中個別轉換的順序很重要。 例如，如果您第一次旋轉，然後進行調整，然後轉譯，則會得到不同的結果，而不是您第一次轉譯、接著旋轉然後調整規模。 DirectComposition 遵循在轉換3D 群組內指定3D 轉換的順序，與2D 轉換的方式相同。 此外，3D 透視轉換會在套用目前視覺效果中的所有3D 轉換之後，將視覺樹狀結構壓平合併。 這樣做的目的是為了確保場景盡可能接近3D。

## <a name="effect-objects"></a>效果物件

若要將效果套用至視覺效果，您必須先建立並設定效果物件的屬性，該物件表示您想要在視覺效果上產生的效果類型。 然後，您必須將效果物件套用至視覺效果的效果屬性。

若要建立效果物件，請使用下列其中一個 [**IDCompositionDevice**](/windows/win32/api/dcomp/nn-dcomp-idcompositiondevice) 介面方法，針對您想要的效果類型建立效果物件。 下列方法會建立效果物件：

-   [**CreateMatrixTransform3D**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-creatematrixtransform3d)
-   [**CreateRotateTransform3D**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createrotatetransform3d)
-   [**CreateScaleTransform3D**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createscaletransform3d)
-   [**CreateTranslateTransform3D**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtranslatetransform3d)

上述每個方法都會抓取介面，您可用來設定新建立之效果物件的屬性。 您可以視需要使用介面方法來設定屬性，以產生您想要的視覺效果。

效果物件的大部分屬性都可以動畫顯示。 若要建立特定屬性的動畫，請建立一個動畫物件，並將它套用至您想要建立動畫的屬性;否則，請將屬性設定為會產生您想要之效果的靜態值。 如需有關製作屬性動畫的詳細資訊，請參閱 [動畫](animation.md)。

若要將效果物件套用至視覺效果，請呼叫 [**IDCompositionVisual：： SetEffect**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-seteffect) 方法。 當您將效果套用至視覺效果時，效果會套用至根于該視覺效果的整個視覺化子樹。 比方說，如果您將視覺效果的不透明度設定為50%，視覺效果子樹中所有子視覺效果的不透明度將會降低50%。 您可以將相同的效果物件套用至一或多個視覺效果。 如果您在將效果物件套用至視覺效果之後修改其屬性，則會重新撰寫所有視覺效果以反映變更。

藉由使用效果群組物件，您可以同時將多個效果套用至視覺效果。 首先，呼叫 [**IDCompositionDevice：： CreateEffectGroup**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createeffectgroup) 來建立效果群組物件，然後使用物件的 [**IDCompositionEffectGroup**](/windows/win32/api/dcomp/nn-dcomp-idcompositioneffectgroup) 介面，將效果新增至該群組。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectComposition 概念](directcomposition-concepts.md)
</dt> </dl>

 

 
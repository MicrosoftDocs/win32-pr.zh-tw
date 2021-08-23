---
title: 轉換概觀
description: 介紹適用于 Windows 7 的 Microsoft Direct2D 轉換 API。 Direct2D 可讓 Win32 開發人員執行2D 圖形轉換。
ms.assetid: eea8177d-c19e-4972-a9a6-ad5d541b090f
keywords:
- Direct2D，轉換總覽
- Direct2D，座標系統
- Direct2D，轉譯目標
- Direct2D、2-d 轉換
- 2-d 轉換
- 轉換，關於
- 轉換，轉譯目標
- 轉換，物件
- 轉譯目標，轉換
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80f2fad970af1d231adab691ad9345377c585b839053625ad49b3d8f7a9e203a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119833098"
---
# <a name="transforms-overview"></a>轉換概觀

本主題討論 Direct2D 轉換的基本概念，並包含各種轉換的範例。 其中包含下列部分：

-   [什麼是 Direct2D 轉換？](#what-is-a-direct2d-transform)
-   [Direct2D 座標空間](#the-direct2d-coordinate-space)
-   [建立轉換矩陣](#creating-transformation-matrices)
-   [轉譯目標轉換](#rendering-target-transforms)
-   [筆刷轉換](#brush-transforms)
-   [幾何轉換](#geometry-transforms)
-   [轉譯目標轉換如何影響剪輯](#how-a-render-target-transform-affects-clips)
-   [總結](#summary)
-   [相關主題](#related-topics)

## <a name="what-is-a-direct2d-transform"></a>什麼是 Direct2D 轉換？

轉換會指定如何將物件的點從某個座標空間對應到另一個座標空間，或從某個位置對應到相同座標空間內的另一個位置。 這項對應是由轉換矩陣所描述，定義為三個數據列的集合，其中有三個數據行的 FLOAT 值，如下表所示。



|    &nbsp;       |       &nbsp;    |  &nbsp; |
|-----------------|-----------------|-----|
| M11Default：1。0 | M12Default：0。0 | 0.0 |
| M21Default：0。0 | M22Default：1。0 | 0.0 |
| M31OffsetX：0。0 | M32OffsetY：0。0 | 1.0 |



 

在此矩陣中，M11、M12、M21 和 M22 成員定義了可以調整、旋轉或扭曲物件的線性轉換;OffsetX 和 OffsetY 成員會定義要在進行線性轉換之後套用的轉譯。 對於仿射轉換，第三個數據行中的值一律是0.0、0.0 和1.0。

因為 Direct2D 僅支援仿射 (線性) 轉換，所以其轉換矩陣會定義為 3 x 2 矩陣，並省略前一個轉換矩陣的第三個數據行。 下表顯示 Direct2D 轉換矩陣的版面配置。



|    &nbsp;       |       &nbsp;    | 
|-----------------|-----------------|
| M11Default：1。0 | M12Default：0。0 |
| M21Default：0。0 | M22Default：1。0 |
| M31OffsetX：0。0 | M32OffsetY：0。0 |



 

在 Direct2D 中，這個 3 x 2 矩陣是以 [**D2D1 \_ 矩陣 \_ 3X2**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) 結構表示。 為了簡化常見的矩陣作業，Direct2D 也提供名為 [**Matrix3x2F**](/windows/win32/api/d2d1helper/nl-d2d1helper-matrix3x2f)的類別，該類別衍生自 **D2D1 \_ 矩陣 \_ 3X2** 結構。

[**Matrix3x2F**](/windows/win32/api/d2d1helper/nl-d2d1helper-matrix3x2f)的預設的函式會將物件保留為未初始化。 若要取出識別矩陣，請使用 [**Matrix3x2F：： identity**](/windows/desktop/api/d2d1helper/nf-d2d1helper-identitymatrix)。

將身分識別轉換套用至物件時，不會變更物件的位置、形狀或大小。 它類似于將數位乘以1不會變更數位的方式。 換句話說，身分識別轉換會單獨保留點的座標，而且不會將點移至新位置。 身分識別轉換以外的任何轉換將會修改物件的位置、形狀及/或大小。

轉換全都是關於座標，而且瞭解 Direct2D 座標空間對於瞭解轉換的使用而言很重要。

## <a name="the-direct2d-coordinate-space"></a>Direct2D 座標空間

Direct2D 使用左手座標空間;也就是說，正 X 軸的值會增加到右邊，且 y 軸值會向下增加。 畫面上的所有內容都是相對於原點的位置，也就是 X 軸和 y 軸交集 (0，0) 的位置，如下圖所示。 Direct2D 呈現目標使用此座標空間。

![左方座標空間的 X 軸和 y 軸圖例](images/coordinatespace.png)

藉由操作轉換矩陣中的值，您可以旋轉、縮放、扭曲和移動 (轉譯) 物件。 例如，如果您將 OffsetX 設定為100，並將 OffsetY 設為200，則會將物件移至右邊的100圖元和下200圖元。

若要顯示物件移動的效果，您必須套用轉譯轉換來呈現目標、筆刷或幾何。 將轉換套用到轉譯目標會影響整個畫面，而將轉換套用至筆刷或幾何時，只會影響該特定筆刷或幾何。 若要建立轉換矩陣，請使用 [**Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) 類別。

## <a name="creating-transformation-matrices"></a>建立轉換矩陣

若要建立旋轉、縮放、扭曲和轉譯轉換， [**Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) 類別會提供下表所示的靜態方法。 資料表的 [範例] 資料行包含示範如何使用每個轉換方法的「如何」主題的連結。



| 方法                                                                   | 描述                                                                                                     | 範例                                            | 圖例                                                                                                                            |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [**matrix3x2f：：旋轉**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-rotation)                          | 建立具有指定角度和中心點的旋轉轉換。                                | [如何旋轉物件](how-to-rotate.md)       | ![以順時針方向與原始正方形中央旋轉45度的圖例](images/rotate-ovw.png)                 |
| [**matrix3x2f：： scale**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-scale(d2d1_size_f_d2d1_point_2f)) | 建立具有指定比例因數和中心點的縮放轉換。                           | [如何調整物件](how-to-scale.md)         | ![調整130% 的正方形圖例](images/scale-ovw.png)                                                                           |
| [**matrix3x2f：：扭曲**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-skew)                              | 建立具有指定 X 軸和 y 軸值和中心點的扭曲轉換。                 | [如何扭曲物件](how-to-skew.md)           | ![從 y 軸逆時針算起30度的正方形圖例](images/skew-ovw.png)                                     |
| [**matrix3x2f：：轉譯**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-translation(d2d1_size_f))                | 建立轉譯轉換，並指定 X 軸和 y 軸方向的置換。 | [如何轉譯物件](how-to-translate.md) | ![正方形的圖，沿著正 X 軸移動20個單位，沿著正 y 軸移動10個單位](images/translation-ovw.png) |



 

## <a name="rendering-target-transforms"></a>轉譯目標轉換

轉譯目標是繼承自 [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) 介面的資源。 它會建立用來繪製和執行實際繪圖作業的資源。 它也提供轉換座標空間的方法。 您可以呼叫 [**ID2D1RenderTarget：： SetTransform**](id2d1rendertarget-settransform.md) 方法，將指定的轉換套用至轉譯目標。 所有後續繪圖作業都會出現在已轉換的空間中。

若要轉譯內容，請使用呈現目標的繪圖方法。 開始繪製之前，請先呼叫 [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) 方法。 若要完成轉譯內容，請呼叫 [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) 方法。 如需範例，請參閱 [如何將多個轉換套用至物件](how-to-apply-multiple-transforms.md)。

## <a name="brush-transforms"></a>筆刷轉換

您可以藉由呼叫 [**SetTransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_))來調整筆刷上的轉換。 針對這項轉換，您可以將筆刷視為大型紙張以及不同轉譯基本專案， (文字、幾何、矩形等) 作為樣板。 當您調整筆刷轉換時，就像是在樣板下滑動大量紙張，而不變更樣板本身的位置。 您可以使用這項技術，將文字從黃色淡化成黑色，使其遠離3D 空間。

當筆刷轉換是身分識別轉換時，筆刷會顯示在其繪製所在之轉譯目標的相同座標空間中。 筆刷轉換可讓呼叫者改變筆刷座標組應至此空間的方式。

在 Direct2D 中指定的筆刷空間，與 Windows Presentation Foundation (WPF) 不同。 在 Direct2D 中，筆刷空間不會相對於正在繪製的物件，而是轉譯目標的目前座標系統（由筆刷轉換轉換）（如果有的話）。 若要讓筆刷填滿在 WPF 中完成的物件，您必須將筆刷空間原點轉譯為物件之周框方塊的左上角，然後調整筆刷空間，讓基底磚填滿物件的周框方塊。

如需筆刷轉換的詳細資訊，請參閱 [Direct2D 筆刷總覽](direct2d-brushes-overview.md)。

## <a name="geometry-transforms"></a>幾何轉換

當您調整、移動、轉譯或扭曲幾何時，可以直接將轉換套用至特定幾何，而不是會影響整個畫面的轉譯目標轉換。 轉譯目標轉換通常會影響幾何的筆觸和填滿。 相反地，geometry 轉換只會影響幾何的填滿，因為轉換會在繪製之前套用至幾何。

> [!Note]  
> 從 Windows 8 開始，如果您將筆劃類型設定為 [**D2D1 \_ stroke \_ 轉換 \_ 類型 \_ 固定**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_stroke_transform_type)或 [**D2D1 \_ 筆劃 \_ 轉換 \_ 類型的 \_ 細**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_stroke_transform_type)項，則世界轉換不會影響筆劃。

 

您可以藉由呼叫 [**ID2D1Factory：： CreateTransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)) 來建立 [**ID2D1TransformedGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1transformedgeometry) 物件，藉以調整幾何的轉換。 如需幾何轉換的詳細資訊，請參閱 [Direct2D 幾何總覽](direct2d-geometries-overview.md)。

## <a name="how-a-render-target-transform-affects-clips"></a>轉譯目標轉換如何影響剪輯

轉譯目標上的轉換會影響以軸對齊的剪輯之周框方塊的計算方式。 呼叫 [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) 時， *clipRect* 參數會由在轉譯目標上設定的目前世界轉換進行轉換。 將轉換套用至 *clipRect* 之後，就會計算 *clipRect* 的軸對齊周框方塊。 為了提高效率，會將內容裁剪成此軸對齊的周框方塊，而不是傳入的原始 *clipRect* 。 下圖顯示如何將旋轉轉換套用到轉譯目標、產生的 *clipRect* 和計算軸對齊的周框方塊。

1.  假設下圖中的矩形是對齊螢幕圖元的呈現目標。

    ![ (呈現目標) 的矩形圖例](images/pushaxisalignedclip-step1-rendertarget.png)

2.  將旋轉轉換套用至呈現目標。 在下圖中，黑色矩形代表原始轉譯目標，紅色虛線矩形表示已轉換的轉譯目標。

    ![原始矩形和旋轉矩形的圖例 (轉換的轉譯目標) ](images/pushaxisalignedclip-step2-transformed.png)

3.  呼叫 [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) 之後，會將旋轉轉換套用至 *clipRect*。 在下圖中，藍色矩形代表已轉換的 *clipRect*。

    ![小藍色矩形的圖例， (在旋轉矩形內的 cliprect)  (轉換的轉譯目標) ](images/pushaxisalignedclip-step3-cliprecttransformed.png)

4.  計算軸對齊的周框方塊。 在下圖中，綠色虛線矩形表示周框方塊。 所有的內容都會裁剪到此軸對齊的周框方塊。

    ![小藍色矩形上的綠色周框方塊的圖例 (cliprect) ](images/pushaxisalignedclip-step4-boundingbox.png)

## <a name="summary"></a>總結

Direct2D 可讓您輕鬆地以簡化的座標空間和相關類別來轉換二維物件。 藉由使用各種類型的轉換，您可以平移、旋轉、扭曲及調整您的物件，以達到許多令人印象深刻的視覺效果。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct2D 參考](reference.md)
</dt> </dl>

 

 
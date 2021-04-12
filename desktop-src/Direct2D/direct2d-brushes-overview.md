---
title: 筆刷概觀
description: 描述 Direct2D 所提供之不同類型的筆刷。
ms.assetid: 7a31d9e7-0521-40ee-b2c1-592dfaf5301e
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 7c8b4c4762a03650f150a74d3207d12767e1fb4e
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/20/2020
ms.locfileid: "104383206"
---
# <a name="brushes-overview"></a>筆刷概觀

本總覽說明如何建立和使用 [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush)、 [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)、 [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)和 [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) 物件，以純色、漸層和點陣圖繪製區域。 包含以下幾節。

## <a name="prerequisites"></a>必要條件

本總覽假設您已經熟悉基本 Direct2D 應用程式的結構，如 [建立簡單的 Direct2D 應用程式](direct2d-quickstart.md)中所述。

## <a name="brush-types"></a>筆刷類型

筆刷「繪製」具有其輸出的區域。 不同的筆刷有不同類型的輸出。 Direct2D 提供四筆刷型別： [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) 以純色繪製區域、以線性漸層 [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) 、以放射狀漸層 [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) ，以及使用點陣圖 [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) 。

> [!NOTE]  
> 從 Windows 8 開始，您也可以使用類似于點陣圖筆刷的 [**ID2D1ImageBrush**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1imagebrush)，但您也可以使用基本類型。

所有筆刷都繼承自 [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush) ，並共用一組通用功能 (設定和取得不透明度，以及將筆刷轉換) ;它們是由 [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) 所建立，而且是與裝置相關的資源：您的應用程式應該在初始化使用筆刷的轉譯目標時建立筆刷，並在每次轉譯目標需要重新建立時重新建立筆刷。  (需資源的詳細資訊，請參閱 [資源總覽](resources-and-resource-domains.md)。 ) 

下圖顯示每個不同筆刷類型的範例。

![純色筆刷、線性漸層筆刷、放射狀漸層筆刷和點陣圖筆刷的視覺效果圖例](images/brushes-ovw-brushes.png)

## <a name="color-basics"></a>色彩基本概念

在使用 [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) 或漸層筆刷繪製之前，您需要選擇色彩。 在 Direct2D 中，色彩是以 [**D2D1 \_ 色 \_ F**](d2d1-color-f.md) 結構表示 (這實際上只是 Direct3D、 [D3DCOLORVALUE](../direct3d9/d3dcolorvalue.md)) 所使用結構的新名稱。

在 Windows 8 之前， [**D2D1 \_ COLOR \_ F**](d2d1-color-f.md) 使用 sRGB 編碼。 sRGB 編碼會將色彩分成四個元件：紅色、綠色、藍色和 Alpha。 每個元件都是以一般範圍為 0.0 到 1.0 的浮點值代表。 值為 0.0 時，表示完全沒有該色彩，而值為 1.0 時，則表示全部為該色彩。 就 Alpha 元件而言，0.0 代表完全透明的色彩，1.0 則代表完全不透明的色彩。

從 Windows 8 開始， [**D2D1 \_ 色彩 \_ F**](d2d1-color-f.md) 也接受 scRGB 編碼。 scRGB 是的超集合，可允許高於1.0 和0.0 以下的色彩值。

若要定義色彩，您可以使用 [**D2D1 \_ color \_ F**](d2d1-color-f.md) 結構並自行將其欄位初始化，或使用 [**D2D1：： ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) 類別來協助您建立色彩。 **ColorF** 類別提供數個用來定義色彩的函式。 如果未在函式中指定 Alpha 值，則預設為1.0。

-   使用 [**ColorF (Enum，FLOAT)**](/previous-versions/windows/desktop/legacy/dd370909(v=vs.85)) 的函式來指定預先定義的色彩和 Alpha 色板值。 Alpha 色板值的範圍是從0.0 到1.0，其中0.0 代表完全透明的色彩，而1.0 則代表完全不透明的色彩。 下圖顯示數個預先定義的色彩及其十六進位對等用法。 如需預先定義之色彩的完整清單，請參閱 [**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) 類別的 [色彩常數] 區段。

    ![預先定義的色彩圖例](images/brushes-ovw-colors.png)

    下列範例會建立預先定義的色彩，並使用它來指定 [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush)的色彩。

```C++
hr = m_pRenderTarget->CreateSolidColorBrush(
    D2D1::ColorF(D2D1::ColorF::Black, 1.0f),
    &m_pBlackBrush
    );
```

-   使用 [**ColorF (float，float，float，float)**](/windows/win32/api/d2d1helper/nf-d2d1helper-colorf-colorf(float_float_float_float)) 的函式來指定紅色、綠色、藍色和 Alpha 序列中的色彩，其中每個元素的值介於0.0 到1.0 之間。

    下列範例會指定色彩的紅色、綠色、藍色和 Alpha 值。

```C++
    ID2D1SolidColorBrush *pGridBrush = NULL;
    hr = pCompatibleRenderTarget->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF(0.93f, 0.94f, 0.96f, 1.0f)),
        &pGridBrush
        );
```

-   使用 [**ColorF (UINT32，FLOAT)**](/windows/win32/api/d2d1helper/nf-d2d1helper-colorf-colorf(uint32_float)) 的函式來指定色彩和 Alpha 值的十六進位值，如下列範例所示。
```C++
    hr = m_pRenderTarget->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF(0x9ACD32, 1.0f)),  
        &m_pYellowGreenBrush
        );
```

### <a name="alpha-modes"></a>Alpha 模式

無論您使用筆刷之轉譯目標的 Alpha 模式為何， [**D2D1 \_ 色彩 \_ F**](d2d1-color-f.md) 值一律會轉譯為純 Alpha。

## <a name="using-solid-color-brushes"></a>使用純色筆刷

若要建立純色筆刷，請呼叫 [**ID2D1RenderTarget：： CreateSolidColorBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) 方法，它會傳回 HRESULT 和 [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) 物件。 下圖顯示以黑色色彩筆刷繪製的正方形，並以具有0x9ACD32 色彩值的純色筆刷繪製。

![以純色筆刷繪製的正方形圖例](images/brushes-ovw-solidcolor.png)

下列程式碼示範如何建立和使用黑色色彩筆刷，以及色彩值為0x9ACD32 的筆刷來填滿和繪製此正方形。


```C++
    ID2D1SolidColorBrush *m_pBlackBrush;
    ID2D1SolidColorBrush *m_pYellowGreenBrush;
```




```C++
if (SUCCEEDED(hr))
{
    hr = m_pRenderTarget->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF::Black, 1.0f),
        &m_pBlackBrush
        );
}

// Create a solid color brush with its rgb value 0x9ACD32.
if (SUCCEEDED(hr))
{
    hr = m_pRenderTarget->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF(0x9ACD32, 1.0f)),  
        &m_pYellowGreenBrush
        );
}
```




```C++
m_pRenderTarget->FillRectangle(&rcBrushRect, m_pYellowGreenBrush);
m_pRenderTarget->DrawRectangle(&rcBrushRect, m_pBlackBrush, 1, NULL);
```



與其他筆刷不同，建立 [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) 是相當便宜的作業。 每次轉譯時，您都可以建立 **ID2D1SolidColorBrush** 物件，而不會影響效能。 這種方法不建議用於漸層或點陣圖筆刷。

## <a name="using-linear-gradient-brushes"></a>使用線性漸層筆刷

[**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)會使用沿著直線漸層（漸層軸）定義的線性漸層繪製區域。 您可以使用 [**ID2D1GradientStop**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) 物件來指定漸層的色彩，以及沿著漸層軸的位置。 您也可以修改漸層軸，讓您建立水準和垂直漸層，以及反轉漸層方向。 若要建立線性漸層筆刷，請呼叫 [**ID2D1RenderTarget：： CreateLinearGradientBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush)) 方法。

下圖顯示的正方形會以具有兩個預先定義色彩 "黃" 和 "ForestGreen" 的 [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) 繪製。

![以黃色和樹系綠色的線性漸層筆刷繪製的正方形圖例](images/brushes-ovw-lineargradient.png)

若要建立上圖所示的漸層，請完成下列步驟：

1.  宣告兩個 [**D2D1 \_ 梯度 \_ 停**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) 用物件。 每個漸層停駐點都會指定色彩和位置。 0.0 的位置表示漸層的開頭，而1.0 的位置則表示漸層的結束。

    下列程式碼會建立兩個 [**D2D1 \_ 梯度 \_ 停**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) 用物件的陣列。 第一個停止會在位置0指定色彩 "黃"，而第二個停止會在位置1指定 "ForestGreen" 色彩。

```C++
    // Create an array of gradient stops to put in the gradient stop
    // collection that will be used in the gradient brush.
    ID2D1GradientStopCollection *pGradientStops = NULL;

    D2D1_GRADIENT_STOP gradientStops[2];
    gradientStops[0].color = D2D1::ColorF(D2D1::ColorF::Yellow, 1);
    gradientStops[0].position = 0.0f;
    gradientStops[1].color = D2D1::ColorF(D2D1::ColorF::ForestGreen, 1);
    gradientStops[1].position = 1.0f;
```

    

2.  建立 [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection)。 下列範例會呼叫 [**CreateGradientStopCollection**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection))，傳入 D2D1 漸層 [**\_ \_ 停**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) 駐物件的陣列、漸層停駐點的數目 (2) 、在插補的 [**D2D1 \_ GAMMA \_ 2 \_ 2**](/windows/win32/api/d2d1/ne-d2d1-d2d1_gamma) ，以及延伸模式的 [**D2D1 \_ 擴充 \_ 模式 \_ 夾具**](/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode) 。

```C++
    // Create the ID2D1GradientStopCollection from a previously
    // declared array of D2D1_GRADIENT_STOP structs.
    hr = m_pRenderTarget->CreateGradientStopCollection(
        gradientStops,
        2,
        D2D1_GAMMA_2_2,
        D2D1_EXTEND_MODE_CLAMP,
        &pGradientStops
        );
```

    

3.  建立 [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)。 下一個範例會呼叫 [**CreateLinearGradientBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush)) 方法，並將包含起點的線性漸層筆刷屬性（ (0、0) 和在上一個步驟中建立的漸層停駐) 150 150 (點）傳遞給它。
```C++
    // The line that determines the direction of the gradient starts at
    // the upper-left corner of the square and ends at the lower-right corner.

    if (SUCCEEDED(hr))
    {
        hr = m_pRenderTarget->CreateLinearGradientBrush(
            D2D1::LinearGradientBrushProperties(
                D2D1::Point2F(0, 0),
                D2D1::Point2F(150, 150)),
            pGradientStops,
            &m_pLinearGradientBrush
            );
    }
```

    

4.  使用 [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)。 下一個程式碼範例會使用筆刷來填滿矩形。
```C++
    m_pRenderTarget->FillRectangle(&rcBrushRect, m_pLinearGradientBrush);
```

    

## <a name="more-about-gradient-stops"></a>深入瞭解漸層停駐點

D2D1 漸層 [**\_ 停駐 \_ 點**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) 是漸層筆刷的基本組建區塊。 漸層停駐點指定沿著漸層軸的色彩和位置。 介於0.0 到1.0 之間的漸層位置值範圍。 越接近0.0，色彩就越接近漸層的開頭;接近1.0，色彩越接近漸層的結尾。

下圖強調漸層停駐點。 圓形會標示漸層停駐點的位置，而虛線則會顯示漸層軸。

![線性漸層筆刷的圖例，其中四個沿著軸停止](images/4stoplineargradient.png)

第一個漸層停駐點會在0.0 的位置指定黃色。 第二個漸層停駐點會在0.25 的位置指定紅色的色彩。 從左至右，沿著漸層軸，這兩個停駐點的色彩會逐漸從黃色變更為紅色。 第三個漸層停駐點會在0.75 的位置指定藍色色彩。 第二個和第三個漸層之間的色彩會逐漸從紅色變更為藍色。 第四個漸層停駐點會在1.0 的位置指定綠色綠色。 第三和第四個漸層之間的色彩會逐漸從藍色變更為綠色。

## <a name="the-gradient-axis"></a>漸層軸

如先前所述，線性漸層筆刷的漸層停駐點沿著直線（漸層軸）放置。 當您建立線性漸層筆刷時，可以使用 [**D2D1 線性漸層 \_ \_ \_ 筆刷 \_ 屬性**](/windows/win32/api/d2d1/ns-d2d1-d2d1_linear_gradient_brush_properties)結構的 **startPoint** 和 **端點** 欄位，來指定線條的方向和大小。 建立筆刷之後，您可以藉由呼叫筆刷的 [**SetStartPoint**](/windows/win32/api/d2d1/nf-d2d1-id2d1lineargradientbrush-setstartpoint) 和 [**task.setendpoint**](/windows/win32/api/d2d1/nf-d2d1-id2d1lineargradientbrush-setendpoint) 方法來調整漸層軸。 藉由操作筆刷的起點和終點，您可以建立水準和垂直漸層、反轉漸層方向等。

例如，在下圖中，起始點設定為 (0、0) 和結束點，以 (150，50) ;這會建立從左上角開始的對角線漸層，並延伸至繪製區域的右下角。 當您將起點設定為 (0，25) ，而結束點設定為 (150，25) 時，會建立水準漸層。 同樣地，將起點設為 (75，0) ，而結束點設定為 (75，50) 會建立垂直漸層。 將起點設定為 (0，50) ，結束點至 (150，0) 會建立從左下角開始並延伸至繪製區域右上角的對角線漸層。

![橫跨相同矩形的四個不同漸層軸的圖例](images/linear-gradients.png)

## <a name="using-radial-gradient-brushes"></a>使用放射狀漸層筆刷

不同于沿著漸層軸混合兩個或多個色彩的 [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)， [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) 會繪製具有放射漸層的區域，以將兩個或多個色彩混合在橢圓形上。 當 **ID2D1LinearGradientBrush** 使用起點和終點來定義其漸層軸時， **ID2D1RadialGradientBrush** 會藉由指定中心、水準和垂直半徑和漸層原點位移來定義其漸層橢圓。

如同 [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)， [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) 會使用 [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) 來指定漸層中的色彩和位置。

下圖顯示以 [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)繪製的圓形。 圓形有兩個漸層停駐點：第一個會在0.0 的位置指定預先定義的色彩 "黃"，而第二個則指定在1.0 位置的預先定義色彩 "ForestGreen"。 漸層的中心有 (75、75) 、 (0、0) 的漸層原點位移，以及75的 x 和 y 半徑。

![以放射狀漸層筆刷繪製的圓形圖例](images/brushes-ovw-radials.png)

下列程式碼範例示範如何使用具有兩色色的 [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) 繪製此圓形：「黃色」在0.0 的位置，而「ForestGreen」在1.0。 類似于建立 [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)，此範例會呼叫 [**CreateGradientStopCollection**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)) ，以從漸層停駐點的陣列建立 [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) 。


```C++
// Create an array of gradient stops to put in the gradient stop
// collection that will be used in the gradient brush.
ID2D1GradientStopCollection *pGradientStops = NULL;

D2D1_GRADIENT_STOP gradientStops[2];
gradientStops[0].color = D2D1::ColorF(D2D1::ColorF::Yellow, 1);
gradientStops[0].position = 0.0f;
gradientStops[1].color = D2D1::ColorF(D2D1::ColorF::ForestGreen, 1);
gradientStops[1].position = 1.0f;
// Create the ID2D1GradientStopCollection from a previously
// declared array of D2D1_GRADIENT_STOP structs.
hr = m_pRenderTarget->CreateGradientStopCollection(
    gradientStops,
    2,
    D2D1_GAMMA_2_2,
    D2D1_EXTEND_MODE_CLAMP,
    &pGradientStops
    );
```



若要建立 [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)，請使用 [**ID2D1RenderTarget：： CreateRadialGradientBrush**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createradialgradientbrush) 方法。 **CreateRadialGradientBrush** 會採用三個參數。 第一個參數是 D2D1 星形漸層 [**\_ \_ \_ 筆刷 \_ 屬性**](/windows/win32/api/d2d1/ns-d2d1-d2d1_radial_gradient_brush_properties) ，會指定漸層的中心、漸層原點位移和水準和垂直半徑。 第二個參數是描述色彩及其在漸層中之位置的 [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) ，而第三個參數是接收新 **ID2D1RadialGradientBrush** 參考之指標的位址。 某些多載會採用額外的參數，也就是 [**D2D1 \_ 筆刷 \_ 屬性**](/windows/win32/api/d2d1/ns-d2d1-d2d1_brush_properties) 結構，指定不透明度值和要套用至新筆刷的轉換。

下一個範例會呼叫 [**CreateRadialGradientBrush**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createradialgradientbrush)，傳入漸層停駐的陣列，以及將 *中間* 值設定為 (75、75) 、將 *gradientOriginOffset* 設為 (0、0) 和 *radiusX* 和 *radiusY* 兩者都設為75的星形漸層筆刷屬性。


```C++
// The center of the gradient is in the center of the box.
// The gradient origin offset was set to zero(0, 0) or center in this case.
if (SUCCEEDED(hr))
{
    hr = m_pRenderTarget->CreateRadialGradientBrush(
        D2D1::RadialGradientBrushProperties(
            D2D1::Point2F(75, 75),
            D2D1::Point2F(0, 0),
            75,
            75),
        pGradientStops,
        &m_pRadialGradientBrush
        );
}
```



最後一個範例會使用筆刷來填滿橢圓形。


```C++
m_pRenderTarget->FillEllipse(ellipse, m_pRadialGradientBrush);
m_pRenderTarget->DrawEllipse(ellipse, m_pBlackBrush, 1, NULL);
```



### <a name="configuring-a-radial-gradient"></a>設定放射狀漸層

*Center*、 *gradientOriginOffset*、 *radiusX* 和/或 *radiusY* 的不同值會產生不同的漸層。 下圖顯示幾個具有不同漸層原點位移的放射狀漸層，並建立從不同角度照亮圓形的光線外觀。

![使用不同來源位移繪製放射狀漸層筆刷的相同圓形圖例](images/radialgradient.png)

## <a name="using-bitmap-brushes"></a>使用點陣圖筆刷

[**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush)繪製一個具有點陣圖 (的區域，) 由 [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap)物件表示。

下圖顯示以植物點陣圖繪製的正方形。

![以植物點陣圖繪製的正方形圖例](images/brushes-ovw-bitmap.png)

下列範例顯示如何使用 [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush)繪製此正方形。

第一個範例會初始化與筆刷搭配使用的 [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) 。 **ID2D1Bitmap** 由範例中其他位置所定義的 Helper 方法 LoadResourceBitmap 提供。


```C++
// Create the bitmap to be used by the bitmap brush.
if (SUCCEEDED(hr))
{
    hr = LoadResourceBitmap(
        m_pRenderTarget,
        m_pWICFactory,
        L"FERN",
        L"Image",
        &m_pBitmap
        );
}
```



若要建立點陣圖筆刷，請呼叫 [**ID2D1RenderTarget：： CreateBitmapBrush**](id2d1rendertarget-createbitmapbrush.md) 方法，並指定要繪製的 [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) 。 方法會傳回 **HRESULT** 和 [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) 物件。 某些 **CreateBitmapBrush** 多載可讓您藉由接受 [**D2D1 \_ 筆刷 \_ 屬性**](/windows/win32/api/d2d1/ns-d2d1-d2d1_brush_properties) 和 [**D2D1 \_ 點陣圖 \_ 筆刷 \_ 屬性**](/windows/win32/api/d2d1/ns-d2d1-d2d1_bitmap_brush_properties) 結構，來指定其他選項。


```C++
if (SUCCEEDED(hr))
{
    hr = m_pRenderTarget->CreateBitmapBrush(
        m_pBitmap,
        &m_pBitmapBrush
        );
}
```



下一個範例會使用筆刷來填滿矩形。


```C++
m_pRenderTarget->FillRectangle(&rcBrushRect, m_pBitmapBrush);
```



## <a name="configuring-extend-modes"></a>設定延伸模式

有時候，漸層筆刷的漸層或點陣圖筆刷的點陣圖，並不會完全填滿正在繪製的區域。

-   當 [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush)發生這種情況時，Direct2D 會使用筆刷的水準 ([**SetExtendModeX**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmapbrush-setextendmodex)) 和垂直 ([**SetExtendModeY**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmapbrush-setextendmodey)) 延伸模式設定，以決定如何填滿剩餘的區域。

-   當漸層筆刷發生這種情況時，Direct2D 會決定如何使用您在呼叫 [**CreateGradientStopCollection**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection))時所指定的 [**D2D1 \_ 延伸 \_ 模式**](/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode)參數值來填滿剩餘的區域，以建立漸層筆刷的 [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection)。

下圖顯示 [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush)的擴充模式的每個可能組合的結果： [**D2D1 \_ 擴充 \_ 模式的 \_ 夾具**](/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode) (夾具) 、 **D2D1 \_ 延伸 \_ 模式 \_ 包裝** (換行) ，以及 **D2D1 \_ 擴充 \_ 鏡像** (鏡像) 。

![來自各種擴充模式的原始影像和產生影像的圖例](images/bitmapwrap-clamp-mirror.png)

下列範例顯示如何將點陣圖筆刷的 x 和 y 擴充模式設定為 [**D2D1 \_ 擴充 \_ 鏡像**](/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode)。 然後使用 [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush)繪製矩形。


```C++
m_pBitmapBrush->SetExtendModeX(D2D1_EXTEND_MODE_MIRROR);
m_pBitmapBrush->SetExtendModeY(D2D1_EXTEND_MODE_MIRROR);

m_pRenderTarget->FillRectangle(exampleRectangle, m_pBitmapBrush);
```



它會產生如下圖所示的輸出。

![鏡像 x 方向和 y 方向之後的原始影像和產生影像的圖例](images/brushes-ovw-bitmapmirrormirror.png)

## <a name="transforming-brushes"></a>轉換筆刷

當您使用筆刷繪製時，它會在呈現目標的座標空間中繪製。 筆刷不會自動自行定位，以配合正在繪製的物件;根據預設，它們會在呈現目標的原點 (0、0) 開始繪製。

您可以藉由設定起點和終點，將 [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) 所定義的漸層「移動」至目的地區域。 同樣地，您可以藉由變更中央和半徑來移動 [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) 所定義的漸層。

若要將 [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) 的內容對齊正在繪製的區域，您可以使用 [**SetTransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f)) 方法將點陣圖轉譯為所需的位置。 此轉換只會影響筆刷;它不會影響呈現目標所繪製的任何其他內容。

下圖顯示使用 [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) 填滿位於 (100，100) 之矩形的效果。 左圖上的圖例顯示填滿矩形的結果，而不會轉換筆刷：點陣圖是在轉譯目標的原點繪製。 如此一來，矩形中只會出現點陣圖的一部分。 右邊的圖例顯示轉換 **ID2D1BitmapBrush** 的結果，使其內容會向右移動50圖元，並向下移動50圖元。 點陣圖現在會填滿矩形。

![以點陣圖筆刷繪製，而不轉換筆刷和轉換筆刷的正方形圖例](images/brushes-ovw-transform.png)

下列程式碼示範如何完成這項工作。 首先，將翻譯套用至 [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush)，並沿著 y 軸沿著 X 軸和50圖元向下移動筆刷50圖元。 然後使用 **ID2D1BitmapBrush** 來填滿左上角的矩形，其位於 (100、100) ，而右下角的 (200，200) 。


```cpp
// Create the bitmap to be used by the bitmap brush.
if (SUCCEEDED(hr))
{
    hr = LoadResourceBitmap(
        m_pRenderTarget,
        m_pWICFactory,
        L"FERN",
        L"Image",
        &m_pBitmap
        );
   
}

if (SUCCEEDED(hr))
{
    hr = m_pRenderTarget->CreateBitmapBrush(
        m_pBitmap,
        &m_pBitmapBrush
        );
}

D2D1_RECT_F rcTransformedBrushRect = D2D1::RectF(100, 100, 200, 200);

// Demonstrate the effect of transforming a bitmap brush.
m_pBitmapBrush->SetTransform(
     D2D1::Matrix3x2F::Translation(D2D1::SizeF(50,50))
     );

// To see the content of the rcTransformedBrushRect, comment
// out this statement.
m_pRenderTarget->FillRectangle(
     &rcTransformedBrushRect, 
     m_pBitmapBrush
     );

m_pRenderTarget->DrawRectangle(rcTransformedBrushRect, m_pBlackBrush, 1, NULL);
```

## <a name="related-topics"></a>相關主題

* [Direct2D 參考](reference.md)
* [如何建立純色筆刷](how-to-create-a-solid-color-brush.md)
* [如何建立線性漸層筆刷](how-to-create-a-linear-gradient-brush.md)
* [如何建立放射狀漸層筆刷](how-to-create-a-radial-gradient-brush.md)
* [如何建立點陣圖筆刷](how-to-create-a-bitmap-brush.md)

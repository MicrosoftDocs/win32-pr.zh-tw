---
description: 本主題說明如何在 XPS OM 中使用不同類型的筆刷。
ms.assetid: 392ca1d5-283e-4eed-ae21-6477c469014d
title: XPS OM 筆刷
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0557757bfaf81156b2015525d35897cfb042e44b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106985632"
---
# <a name="xps-om-brushes"></a>XPS OM 筆刷

本主題說明如何在 XPS OM 中使用不同類型的筆刷。

XPS OM 中的筆刷以 [**IXpsOMBrush 介面**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush) 為基礎，並包含下列各項：

<dl> 磚筆刷

-   [**IXpsOMTileBrush 介面**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomtilebrush)
-   [**IXpsOMSolidColorBrush 介面**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush)
-   [**IXpsOMVisualBrush 介面**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualbrush)
-   [**IXpsOMImageBrush 介面**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimagebrush)

  
漸層筆刷

-   [**IXpsOMGradientBrush 介面**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientbrush)
-   [**IXpsOMLinearGradientBrush 介面**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomlineargradientbrush)
-   [**IXpsOMRadialGradientBrush 介面**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomradialgradientbrush)

  
</dl>

## <a name="code-examples"></a>程式碼範例

### <a name="create-a-solid-color-brush"></a>建立單色筆刷

下列程式碼範例會從程式碼中定義的色彩值建立單色筆刷。


```C++
    HRESULT                hr = S_OK;

    XPS_COLOR              xpsColor;
    IXpsOMSolidColorBrush  *brush;

    // creates a solid red brush
    xpsColor.colorType = XPS_COLOR_TYPE_SRGB;
    xpsColor.value.sRGB.alpha = 0xFF;
    xpsColor.value.sRGB.red = 0xFF;
    xpsColor.value.sRGB.green = 0x00;
    xpsColor.value.sRGB.blue = 0x00;

    hr = xpsFactory->CreateSolidColorBrush(
       &xpsColor, 
       NULL, 
       reinterpret_cast<IXpsOMSolidColorBrush**>(&brush));
    
    // use brush

    // when finished with brush, release pointer
    brush->Release();
```



### <a name="create-a-visual-brush"></a>建立視覺筆刷

下列程式碼範例會從視覺物件建立筆刷。


```C++
    HRESULT                       hr = S_OK;
    IXpsOMVisualBrush             *brush;

    XPS_RECT viewBoxRect = {0,0,0,0};
    XPS_RECT viewPortRect = {0,0,0,0};

    // set viewBoxRect to define the portion of the visual to use
    // as the brush.
    //
    // set viewPortRect to define the location and size of the 
    // the brush in the destination 
    //
    // create the brush
    hr = xpsFactory->CreateVisualBrush (
        &viewBoxRect,
        &viewPortRect,
        reinterpret_cast<IXpsOMVisualBrush**>(&brush));

    // assign the visual object
    //   brushVisual points to a visual
    //   that is defined outside of this example

    hr = brush->SetVisualLocal (brushVisual);
    
    // use brush
    
    // when finished with brush, release pointer
    brush->Release();
    
```



### <a name="create-an-image-brush"></a>建立影像筆刷

請參閱在 [XPS OM 中放置影像](place-images-in-an-xps-om.md)的程式碼範例。

### <a name="create-a-linear-gradient-brush"></a>建立線性漸層筆刷

下列程式碼範例會建立線性漸層筆刷。 漸層有兩個漸層停駐點。


```C++
    HRESULT                       hr = S_OK;
    XPS_COLOR                     xpsColorStop;
    IXpsOMGradientStop            *xpsGradientStop1, *xpsGradientStop2;
    IXpsOMLinearGradientBrush     *brush;
    XPS_POINT                     startPoint, endPoint;

    // define the start color
    xpsColorStop.colorType        = XPS_COLOR_TYPE_SRGB;
    xpsColorStop.value.sRGB.alpha = 0xFF;
    xpsColorStop.value.sRGB.red   = 0xE4;
    xpsColorStop.value.sRGB.green = 0x3B;
    xpsColorStop.value.sRGB.blue  = 0x2F;
    
    // create a gradient stop by setting the color and location 
    // for the beginning of the gradient
    hr = xpsFactory->CreateGradientStop(
        &xpsColorStop, 
        NULL, 
        0.0f,
        &xpsGradientStop1);
    startPoint.x = 375.75f;
    startPoint.y = 18.0f;

    // define the end color
    xpsColorStop.colorType        = XPS_COLOR_TYPE_SRGB;
    xpsColorStop.value.sRGB.alpha = 0xFF;
    xpsColorStop.value.sRGB.red   = 0xEF;
    xpsColorStop.value.sRGB.green = 0x79;
    xpsColorStop.value.sRGB.blue  = 0x2F;

    // create a gradient stop by setting the color and  location
    //  for the end of the gradient
    hr = xpsFactory->CreateGradientStop(
        &xpsColorStop,
        NULL, 
        1.0f, 
        &xpsGradientStop2);
    endPoint.x   = 375.75f;
    endPoint.y   = 134.6f;

    // create the brush
    hr = xpsFactory->CreateLinearGradientBrush(
        xpsGradientStop1, 
        xpsGradientStop2, 
        &startPoint, 
        &endPoint, 
        &brush);
    // release gradient stops after creating brush
    xpsGradientStop1->Release();
    xpsGradientStop2->Release();

    // when finished with brush, release pointer to brush
    brush->Release();
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IXpsOMGradientBrush 介面**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientbrush)
</dt> <dt>

[**IXpsOMImageBrush 介面**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimagebrush)
</dt> <dt>

[**IXpsOMLinearGradientBrush 介面**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomlineargradientbrush)
</dt> <dt>

[**IXpsOMRadialGradientBrush 介面**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomradialgradientbrush)
</dt> <dt>

[**IXpsOMSolidColorBrush 介面**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush)
</dt> <dt>

[**IXpsOMTileBrush 介面**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomtilebrush)
</dt> <dt>

[**IXpsOMVisualBrush 介面**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualbrush)
</dt> <dt>

[**XPS \_ 色彩**](xps-color.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 




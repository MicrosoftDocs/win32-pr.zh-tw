---
title: 如何使用矩形剪輯物件裁剪
description: 本主題將示範如何使用矩形剪輯物件來裁剪視覺效果或視覺化樹狀結構。
ms.assetid: 377EF49A-F9F2-4A72-9D22-DEC33803AD0D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d26019f37949b0111ee9b5958fa3fba2c9507cb
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/20/2020
ms.locfileid: "104024306"
---
# <a name="how-to-clip-with-a-rectangle-clip-object"></a>如何使用矩形剪輯物件裁剪

> [!NOTE]
> 針對 Windows 10 上的應用程式，我們建議使用 DirectComposition，而不是使用。 如需詳細資訊，請參閱 [使用視覺分層將您的桌面應用程式現代化](/windows/uwp/composition/visual-layer-in-desktop-apps)。

本主題將示範如何使用矩形剪輯物件來裁剪視覺效果或視覺化樹狀結構。

本主題中的範例會定義以滑鼠位置為中心的矩形剪輯，並將剪輯套用至在組合目標視窗的工作區中央的視覺效果。 這個螢幕擷取畫面顯示將矩形剪輯物件套用至視覺效果的結果。

![將矩形剪輯物件套用至視覺效果的結果](images/clipwithrectangleclipobject.png)

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   [DirectComposition](directcomposition-portal.md)
-   [Direct3D 11 圖形](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11)
-   [DirectX Graphic Infrastructure (DXGI) ](/windows/desktop/direct3ddxgi/dx-graphics-dxgi)

### <a name="prerequisites"></a>必要條件

-   C/C++
-   Microsoft Win32
-   元件物件模型 (COM)

## <a name="instructions"></a>指示

### <a name="step-1-initialize-directcomposition-objects"></a>步驟1：初始化 DirectComposition 物件

1.  建立裝置物件和組合目標物件。
2.  建立視覺效果、設定其內容，並將它新增至視覺化樹狀結構。

如需詳細資訊，請參閱 [如何初始化 DirectComposition](initialize-directcomposition.md)。

### <a name="step-2-create-the-rectangle-clip-object"></a>步驟2：建立矩形剪輯物件

您可以使用 [**IDCompositionDevice：： CreateRectangleClip**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createrectangleclip) 方法來建立矩形剪輯物件的實例。


```C++
    HRESULT hr = S_OK;
    
    // Create the rectangle clip object.
    if (m_pClip == NULL)
    {
        hr = m_pDevice->CreateRectangleClip(&m_pClip);
    }
```



### <a name="step-3-set-the-properties-of-the-rectangle-clip-object"></a>步驟3：設定矩形剪輯物件的屬性

呼叫矩形剪輯物件之 [**IDCompositionRectangleClip**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrectangleclip) 介面的方法，以設定剪切矩形的屬性。

下列範例會定義以目前滑鼠位置為中心的剪輯矩形。 `m_offsetX`和 `m_offsetY` 成員變數包含視覺效果的 OffsetX 和 OffsetY 屬性值。


```C++
    if (SUCCEEDED(hr))
    {
        // Get the location of the mouse.
        POINT ptMouse = { };
        GetCursorPos(&ptMouse);
        ScreenToClient(m_hwnd, &ptMouse);

        // Create a 100-by-100 pixel rectangular clip that is 
        // centered at the mouse location, and is mapped to
        // the rectangle of the visual.
        m_pClip->SetLeft((ptMouse.x - m_offsetX) - 50.f);
        m_pClip->SetTop((ptMouse.y - m_offsetY) - 50.f);
        m_pClip->SetRight((ptMouse.x - m_offsetX) + 50.f);
        m_pClip->SetBottom((ptMouse.y - m_offsetY) + 50.f);
    }
```



請注意， [**IDCompositionRectangleClip**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrectangleclip) 介面包含下列方法，以定義具有圓角的剪輯矩形：

-   [**SetTopLeftRadiusX**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settopleftradiusx(float))
-   [**SetTopLeftRadiusY**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settopleftradiusy(float))
-   [**SetTopRightRadiusX**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settoprightradiusx(float))
-   [**SetTopRightRadiusY**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settoprightradiusy(float))

### <a name="step-4-set-the-clip-property-of-the-visual"></a>步驟4：設定視覺效果的剪輯屬性

使用 [**IDCompositionVisual：： SetClip**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(idcompositionclip)) 方法，將視覺效果的剪輯屬性與矩形剪輯物件產生關聯。


```C++
    if (SUCCEEDED(hr))
    {
        // Set the rectangle clip object as the Clip property 
        // of the visual.
        hr = m_pVisual->SetClip(m_pClip);
    }
```



### <a name="step-5-commit-the-composition"></a>步驟5：認可組合

呼叫 [**IDCompositionDevice：： commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) 方法，將命令批次認可至 Microsoft DirectComposition 進行處理。 套用剪輯矩形的結果會出現在目標視窗中。


```C++
    if (SUCCEEDED(hr))
    {
        // Commit the visual to be composed and displayed.
        hr = m_pDevice->Commit();  
    }
```



### <a name="step-6-free-the-directcomposition-objects"></a>步驟6：釋放 DirectComposition 物件

當您不再需要時，請務必釋放矩形剪輯物件，以及裝置物件、組合目標物件和任何視覺物件。 下列範例會呼叫應用程式定義的 [**SafeRelease**](/windows/desktop/medfound/saferelease) 宏來釋放 DirectComposition 物件。


```C++
    SafeRelease(&m_pClip);
    SafeRelease(&m_pDevice);
    SafeRelease(&m_pD3D11Device);
    SafeRelease(&m_pCompTarget);
    SafeRelease(&m_pVisual);
    SafeRelease(&m_pSurface);
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[裁剪](clipping.md)
</dt> </dl>

 

 
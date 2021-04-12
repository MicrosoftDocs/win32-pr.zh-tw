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
# <a name="brushes-overview"></a><span data-ttu-id="21a70-103">筆刷概觀</span><span class="sxs-lookup"><span data-stu-id="21a70-103">Brushes overview</span></span>

<span data-ttu-id="21a70-104">本總覽說明如何建立和使用 [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush)、 [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)、 [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)和 [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) 物件，以純色、漸層和點陣圖繪製區域。</span><span class="sxs-lookup"><span data-stu-id="21a70-104">This overview describes how to create and use [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush), [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush), and [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) objects to paint areas with solid colors, gradients, and bitmaps.</span></span> <span data-ttu-id="21a70-105">包含以下幾節。</span><span class="sxs-lookup"><span data-stu-id="21a70-105">It contains the following sections.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="21a70-106">必要條件</span><span class="sxs-lookup"><span data-stu-id="21a70-106">Prerequisites</span></span>

<span data-ttu-id="21a70-107">本總覽假設您已經熟悉基本 Direct2D 應用程式的結構，如 [建立簡單的 Direct2D 應用程式](direct2d-quickstart.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="21a70-107">This overview assumes that you are familiar with the structure of a basic Direct2D application, as described in [Creating a Simple Direct2D Application](direct2d-quickstart.md).</span></span>

## <a name="brush-types"></a><span data-ttu-id="21a70-108">筆刷類型</span><span class="sxs-lookup"><span data-stu-id="21a70-108">Brush types</span></span>

<span data-ttu-id="21a70-109">筆刷「繪製」具有其輸出的區域。</span><span class="sxs-lookup"><span data-stu-id="21a70-109">A brush "paints" an area with its output.</span></span> <span data-ttu-id="21a70-110">不同的筆刷有不同類型的輸出。</span><span class="sxs-lookup"><span data-stu-id="21a70-110">Different brushes have different types of output.</span></span> <span data-ttu-id="21a70-111">Direct2D 提供四筆刷型別： [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) 以純色繪製區域、以線性漸層 [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) 、以放射狀漸層 [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) ，以及使用點陣圖 [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) 。</span><span class="sxs-lookup"><span data-stu-id="21a70-111">Direct2D provides four brush types: [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) paints an area with a solid color, [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) with a linear gradient, [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) with a radial gradient, and [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) with a bitmap.</span></span>

> [!NOTE]  
> <span data-ttu-id="21a70-112">從 Windows 8 開始，您也可以使用類似于點陣圖筆刷的 [**ID2D1ImageBrush**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1imagebrush)，但您也可以使用基本類型。</span><span class="sxs-lookup"><span data-stu-id="21a70-112">Starting with Windows 8, you can also use [**ID2D1ImageBrush**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1imagebrush), which is similar to a bitmap brush, but you can use primitives, too.</span></span>

<span data-ttu-id="21a70-113">所有筆刷都繼承自 [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush) ，並共用一組通用功能 (設定和取得不透明度，以及將筆刷轉換) ;它們是由 [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) 所建立，而且是與裝置相關的資源：您的應用程式應該在初始化使用筆刷的轉譯目標時建立筆刷，並在每次轉譯目標需要重新建立時重新建立筆刷。</span><span class="sxs-lookup"><span data-stu-id="21a70-113">All brushes inherit from [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush) and share a set of common features (setting and getting opacity, and transforming brushes); they are created by [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) and are device-dependent resources: your application should create brushes after it initializes the render target with which the brushes will be used, and recreate the brushes whenever the render target needs recreated.</span></span> <span data-ttu-id="21a70-114"> (需資源的詳細資訊，請參閱 [資源總覽](resources-and-resource-domains.md)。 ) </span><span class="sxs-lookup"><span data-stu-id="21a70-114">(For more information about resources, see [Resources Overview](resources-and-resource-domains.md).)</span></span>

<span data-ttu-id="21a70-115">下圖顯示每個不同筆刷類型的範例。</span><span class="sxs-lookup"><span data-stu-id="21a70-115">The following illustration shows examples of each of the different brush types.</span></span>

![純色筆刷、線性漸層筆刷、放射狀漸層筆刷和點陣圖筆刷的視覺效果圖例](images/brushes-ovw-brushes.png)

## <a name="color-basics"></a><span data-ttu-id="21a70-117">色彩基本概念</span><span class="sxs-lookup"><span data-stu-id="21a70-117">Color basics</span></span>

<span data-ttu-id="21a70-118">在使用 [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) 或漸層筆刷繪製之前，您需要選擇色彩。</span><span class="sxs-lookup"><span data-stu-id="21a70-118">Before you paint with an [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) or a gradient brush, you need to choose colors.</span></span> <span data-ttu-id="21a70-119">在 Direct2D 中，色彩是以 [**D2D1 \_ 色 \_ F**](d2d1-color-f.md) 結構表示 (這實際上只是 Direct3D、 [D3DCOLORVALUE](../direct3d9/d3dcolorvalue.md)) 所使用結構的新名稱。</span><span class="sxs-lookup"><span data-stu-id="21a70-119">In Direct2D, colors are represented by the [**D2D1\_COLOR\_F**](d2d1-color-f.md) structure (which is actually just a new name for the structure that is used by Direct3D, [D3DCOLORVALUE](../direct3d9/d3dcolorvalue.md)).</span></span>

<span data-ttu-id="21a70-120">在 Windows 8 之前， [**D2D1 \_ COLOR \_ F**](d2d1-color-f.md) 使用 sRGB 編碼。</span><span class="sxs-lookup"><span data-stu-id="21a70-120">Prior to Windows 8, [**D2D1\_COLOR\_F**](d2d1-color-f.md) uses sRGB encoding.</span></span> <span data-ttu-id="21a70-121">sRGB 編碼會將色彩分成四個元件：紅色、綠色、藍色和 Alpha。</span><span class="sxs-lookup"><span data-stu-id="21a70-121">sRGB encoding divides colors into four components: red, green, blue, and alpha.</span></span> <span data-ttu-id="21a70-122">每個元件都是以一般範圍為 0.0 到 1.0 的浮點值代表。</span><span class="sxs-lookup"><span data-stu-id="21a70-122">Each component is represented by a floating point value with a normal range of 0.0 to 1.0.</span></span> <span data-ttu-id="21a70-123">值為 0.0 時，表示完全沒有該色彩，而值為 1.0 時，則表示全部為該色彩。</span><span class="sxs-lookup"><span data-stu-id="21a70-123">A value of 0.0 indicates the complete absence of that color, while a value of 1.0 indicates that the color is fully present.</span></span> <span data-ttu-id="21a70-124">就 Alpha 元件而言，0.0 代表完全透明的色彩，1.0 則代表完全不透明的色彩。</span><span class="sxs-lookup"><span data-stu-id="21a70-124">For the alpha component, 0.0 represents a fully transparent color and 1.0 represents a fully opaque color.</span></span>

<span data-ttu-id="21a70-125">從 Windows 8 開始， [**D2D1 \_ 色彩 \_ F**](d2d1-color-f.md) 也接受 scRGB 編碼。</span><span class="sxs-lookup"><span data-stu-id="21a70-125">Starting in Windows 8, [**D2D1\_COLOR\_F**](d2d1-color-f.md) also accepts scRGB encoding.</span></span> <span data-ttu-id="21a70-126">scRGB 是的超集合，可允許高於1.0 和0.0 以下的色彩值。</span><span class="sxs-lookup"><span data-stu-id="21a70-126">scRGB is a superset of that allows color values above 1.0 and below 0.0.</span></span>

<span data-ttu-id="21a70-127">若要定義色彩，您可以使用 [**D2D1 \_ color \_ F**](d2d1-color-f.md) 結構並自行將其欄位初始化，或使用 [**D2D1：： ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) 類別來協助您建立色彩。</span><span class="sxs-lookup"><span data-stu-id="21a70-127">To define a color, you can use the [**D2D1\_COLOR\_F**](d2d1-color-f.md) structure and initialize its fields yourself, or you can use the [**D2D1::ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) class to help you create the color.</span></span> <span data-ttu-id="21a70-128">**ColorF** 類別提供數個用來定義色彩的函式。</span><span class="sxs-lookup"><span data-stu-id="21a70-128">The **ColorF** class provides several constructors for defining colors.</span></span> <span data-ttu-id="21a70-129">如果未在函式中指定 Alpha 值，則預設為1.0。</span><span class="sxs-lookup"><span data-stu-id="21a70-129">If the alpha value is not specified in the constructors, it defaults to 1.0.</span></span>

-   <span data-ttu-id="21a70-130">使用 [**ColorF (Enum，FLOAT)**](/previous-versions/windows/desktop/legacy/dd370909(v=vs.85)) 的函式來指定預先定義的色彩和 Alpha 色板值。</span><span class="sxs-lookup"><span data-stu-id="21a70-130">Use the [**ColorF(Enum, FLOAT)**](/previous-versions/windows/desktop/legacy/dd370909(v=vs.85)) constructor to specify a predefined color and an alpha channel value.</span></span> <span data-ttu-id="21a70-131">Alpha 色板值的範圍是從0.0 到1.0，其中0.0 代表完全透明的色彩，而1.0 則代表完全不透明的色彩。</span><span class="sxs-lookup"><span data-stu-id="21a70-131">An alpha channel value ranges from 0.0 to 1.0, where 0.0 represents a fully transparent color and 1.0 represents a fully opaque color.</span></span> <span data-ttu-id="21a70-132">下圖顯示數個預先定義的色彩及其十六進位對等用法。</span><span class="sxs-lookup"><span data-stu-id="21a70-132">The following illustration shows several predefined colors and their hexadecimal equivalents.</span></span> <span data-ttu-id="21a70-133">如需預先定義之色彩的完整清單，請參閱 [**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) 類別的 [色彩常數] 區段。</span><span class="sxs-lookup"><span data-stu-id="21a70-133">For a complete list of predefined colors, see the Color constants section of the [**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) class.</span></span>

    ![預先定義的色彩圖例](images/brushes-ovw-colors.png)

    <span data-ttu-id="21a70-135">下列範例會建立預先定義的色彩，並使用它來指定 [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush)的色彩。</span><span class="sxs-lookup"><span data-stu-id="21a70-135">The following example creates a predefined color and uses it to specify the color of an [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush).</span></span>

```C++
hr = m_pRenderTarget->CreateSolidColorBrush(
    D2D1::ColorF(D2D1::ColorF::Black, 1.0f),
    &m_pBlackBrush
    );
```

-   <span data-ttu-id="21a70-136">使用 [**ColorF (float，float，float，float)**](/windows/win32/api/d2d1helper/nf-d2d1helper-colorf-colorf(float_float_float_float)) 的函式來指定紅色、綠色、藍色和 Alpha 序列中的色彩，其中每個元素的值介於0.0 到1.0 之間。</span><span class="sxs-lookup"><span data-stu-id="21a70-136">Use the [**ColorF(FLOAT, FLOAT, FLOAT, FLOAT)**](/windows/win32/api/d2d1helper/nf-d2d1helper-colorf-colorf(float_float_float_float)) constructor to specify a color in the sequence of a red, green, blue, and alpha, where each element has a value between 0.0 and 1.0.</span></span>

    <span data-ttu-id="21a70-137">下列範例會指定色彩的紅色、綠色、藍色和 Alpha 值。</span><span class="sxs-lookup"><span data-stu-id="21a70-137">The following example specifies the red, green, blue, and alpha values for a color.</span></span>

```C++
    ID2D1SolidColorBrush *pGridBrush = NULL;
    hr = pCompatibleRenderTarget->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF(0.93f, 0.94f, 0.96f, 1.0f)),
        &pGridBrush
        );
```

-   <span data-ttu-id="21a70-138">使用 [**ColorF (UINT32，FLOAT)**](/windows/win32/api/d2d1helper/nf-d2d1helper-colorf-colorf(uint32_float)) 的函式來指定色彩和 Alpha 值的十六進位值，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="21a70-138">Use the [**ColorF(UINT32, FLOAT)**](/windows/win32/api/d2d1helper/nf-d2d1helper-colorf-colorf(uint32_float)) constructor to specify the hexadecimal value of a color and an alpha value, as shown in the following example.</span></span>
```C++
    hr = m_pRenderTarget->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF(0x9ACD32, 1.0f)),  
        &m_pYellowGreenBrush
        );
```

### <a name="alpha-modes"></a><span data-ttu-id="21a70-139">Alpha 模式</span><span class="sxs-lookup"><span data-stu-id="21a70-139">Alpha modes</span></span>

<span data-ttu-id="21a70-140">無論您使用筆刷之轉譯目標的 Alpha 模式為何， [**D2D1 \_ 色彩 \_ F**](d2d1-color-f.md) 值一律會轉譯為純 Alpha。</span><span class="sxs-lookup"><span data-stu-id="21a70-140">Regardless of the alpha mode of the render target with which you use a brush, [**D2D1\_COLOR\_F**](d2d1-color-f.md) values are always interpreted as straight alpha.</span></span>

## <a name="using-solid-color-brushes"></a><span data-ttu-id="21a70-141">使用純色筆刷</span><span class="sxs-lookup"><span data-stu-id="21a70-141">Using solid color brushes</span></span>

<span data-ttu-id="21a70-142">若要建立純色筆刷，請呼叫 [**ID2D1RenderTarget：： CreateSolidColorBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) 方法，它會傳回 HRESULT 和 [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) 物件。</span><span class="sxs-lookup"><span data-stu-id="21a70-142">To create a solid color brush, call the [**ID2D1RenderTarget::CreateSolidColorBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) method, which returns an HRESULT and an [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) object.</span></span> <span data-ttu-id="21a70-143">下圖顯示以黑色色彩筆刷繪製的正方形，並以具有0x9ACD32 色彩值的純色筆刷繪製。</span><span class="sxs-lookup"><span data-stu-id="21a70-143">The following illustration shows a square that is stroked with a black color brush and painted with a solid color brush that has the color value of 0x9ACD32.</span></span>

![以純色筆刷繪製的正方形圖例](images/brushes-ovw-solidcolor.png)

<span data-ttu-id="21a70-145">下列程式碼示範如何建立和使用黑色色彩筆刷，以及色彩值為0x9ACD32 的筆刷來填滿和繪製此正方形。</span><span class="sxs-lookup"><span data-stu-id="21a70-145">The following code shows how to create and use a black color brush and a brush with a color value of 0x9ACD32 to fill and draw this square.</span></span>


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



<span data-ttu-id="21a70-146">與其他筆刷不同，建立 [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) 是相當便宜的作業。</span><span class="sxs-lookup"><span data-stu-id="21a70-146">Unlike other brushes, creating an [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) is a relatively inexpensive operation.</span></span> <span data-ttu-id="21a70-147">每次轉譯時，您都可以建立 **ID2D1SolidColorBrush** 物件，而不會影響效能。</span><span class="sxs-lookup"><span data-stu-id="21a70-147">You may create **ID2D1SolidColorBrush** objects each time you render with little to no performance impact.</span></span> <span data-ttu-id="21a70-148">這種方法不建議用於漸層或點陣圖筆刷。</span><span class="sxs-lookup"><span data-stu-id="21a70-148">This approach is not recommended for gradient or bitmap brushes.</span></span>

## <a name="using-linear-gradient-brushes"></a><span data-ttu-id="21a70-149">使用線性漸層筆刷</span><span class="sxs-lookup"><span data-stu-id="21a70-149">Using linear gradient brushes</span></span>

<span data-ttu-id="21a70-150">[**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)會使用沿著直線漸層（漸層軸）定義的線性漸層繪製區域。</span><span class="sxs-lookup"><span data-stu-id="21a70-150">An [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) paints an area with a linear gradient defined along a line, the gradient axis.</span></span> <span data-ttu-id="21a70-151">您可以使用 [**ID2D1GradientStop**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) 物件來指定漸層的色彩，以及沿著漸層軸的位置。</span><span class="sxs-lookup"><span data-stu-id="21a70-151">You specify the gradient's colors and their location along the gradient axis using [**ID2D1GradientStop**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) objects.</span></span> <span data-ttu-id="21a70-152">您也可以修改漸層軸，讓您建立水準和垂直漸層，以及反轉漸層方向。</span><span class="sxs-lookup"><span data-stu-id="21a70-152">You may also modify the gradient axis, which enables you to create horizontal and vertical gradient and to reverse the gradient direction.</span></span> <span data-ttu-id="21a70-153">若要建立線性漸層筆刷，請呼叫 [**ID2D1RenderTarget：： CreateLinearGradientBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush)) 方法。</span><span class="sxs-lookup"><span data-stu-id="21a70-153">To create a linear gradient brush, call the [**ID2D1RenderTarget::CreateLinearGradientBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush)) method.</span></span>

<span data-ttu-id="21a70-154">下圖顯示的正方形會以具有兩個預先定義色彩 "黃" 和 "ForestGreen" 的 [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) 繪製。</span><span class="sxs-lookup"><span data-stu-id="21a70-154">The following illustration shows a square that is painted with an [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) that has two predefined colors, "Yellow" and "ForestGreen".</span></span>

![以黃色和樹系綠色的線性漸層筆刷繪製的正方形圖例](images/brushes-ovw-lineargradient.png)

<span data-ttu-id="21a70-156">若要建立上圖所示的漸層，請完成下列步驟：</span><span class="sxs-lookup"><span data-stu-id="21a70-156">To create the gradient shown in the preceding illustration, complete these steps:</span></span>

1.  <span data-ttu-id="21a70-157">宣告兩個 [**D2D1 \_ 梯度 \_ 停**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) 用物件。</span><span class="sxs-lookup"><span data-stu-id="21a70-157">Declare two [**D2D1\_GRADIENT\_STOP**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) objects.</span></span> <span data-ttu-id="21a70-158">每個漸層停駐點都會指定色彩和位置。</span><span class="sxs-lookup"><span data-stu-id="21a70-158">Each gradient stop specifies a color and a position.</span></span> <span data-ttu-id="21a70-159">0.0 的位置表示漸層的開頭，而1.0 的位置則表示漸層的結束。</span><span class="sxs-lookup"><span data-stu-id="21a70-159">A position of 0.0 indicates the beginning of the gradient, while a position of 1.0 indicates the end of the gradient.</span></span>

    <span data-ttu-id="21a70-160">下列程式碼會建立兩個 [**D2D1 \_ 梯度 \_ 停**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) 用物件的陣列。</span><span class="sxs-lookup"><span data-stu-id="21a70-160">The following code creates an array of two [**D2D1\_GRADIENT\_STOP**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) objects.</span></span> <span data-ttu-id="21a70-161">第一個停止會在位置0指定色彩 "黃"，而第二個停止會在位置1指定 "ForestGreen" 色彩。</span><span class="sxs-lookup"><span data-stu-id="21a70-161">The first stop specifies the color "Yellow" at a position 0, and the second stop specifies the color "ForestGreen" at position 1.</span></span>

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

    

2.  <span data-ttu-id="21a70-162">建立 [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection)。</span><span class="sxs-lookup"><span data-stu-id="21a70-162">Create an [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection).</span></span> <span data-ttu-id="21a70-163">下列範例會呼叫 [**CreateGradientStopCollection**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection))，傳入 D2D1 漸層 [**\_ \_ 停**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) 駐物件的陣列、漸層停駐點的數目 (2) 、在插補的 [**D2D1 \_ GAMMA \_ 2 \_ 2**](/windows/win32/api/d2d1/ne-d2d1-d2d1_gamma) ，以及延伸模式的 [**D2D1 \_ 擴充 \_ 模式 \_ 夾具**](/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode) 。</span><span class="sxs-lookup"><span data-stu-id="21a70-163">The following example calls [**CreateGradientStopCollection**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)), passing in the array of [**D2D1\_GRADIENT\_STOP**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) objects, the number of gradient stops (2), [**D2D1\_GAMMA\_2\_2**](/windows/win32/api/d2d1/ne-d2d1-d2d1_gamma) for interpolation, and [**D2D1\_EXTEND\_MODE\_CLAMP**](/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode) for the extend mode.</span></span>

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

    

3.  <span data-ttu-id="21a70-164">建立 [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)。</span><span class="sxs-lookup"><span data-stu-id="21a70-164">Create the [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush).</span></span> <span data-ttu-id="21a70-165">下一個範例會呼叫 [**CreateLinearGradientBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush)) 方法，並將包含起點的線性漸層筆刷屬性（ (0、0) 和在上一個步驟中建立的漸層停駐) 150 150 (點）傳遞給它。</span><span class="sxs-lookup"><span data-stu-id="21a70-165">The next example calls the [**CreateLinearGradientBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush)) method and passes it the linear gradient brush properties that contain the start point at (0, 0) and the end point at (150, 150), and the gradient stops created in the previous step.</span></span>
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

    

4.  <span data-ttu-id="21a70-166">使用 [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)。</span><span class="sxs-lookup"><span data-stu-id="21a70-166">Use the [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush).</span></span> <span data-ttu-id="21a70-167">下一個程式碼範例會使用筆刷來填滿矩形。</span><span class="sxs-lookup"><span data-stu-id="21a70-167">The next code example uses the brush to fille a rectangle.</span></span>
```C++
    m_pRenderTarget->FillRectangle(&rcBrushRect, m_pLinearGradientBrush);
```

    

## <a name="more-about-gradient-stops"></a><span data-ttu-id="21a70-168">深入瞭解漸層停駐點</span><span class="sxs-lookup"><span data-stu-id="21a70-168">More about gradient stops</span></span>

<span data-ttu-id="21a70-169">D2D1 漸層 [**\_ 停駐 \_ 點**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) 是漸層筆刷的基本組建區塊。</span><span class="sxs-lookup"><span data-stu-id="21a70-169">The [**D2D1\_GRADIENT\_STOP**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) is the basic building block of a gradient brush.</span></span> <span data-ttu-id="21a70-170">漸層停駐點指定沿著漸層軸的色彩和位置。</span><span class="sxs-lookup"><span data-stu-id="21a70-170">A gradient stop specifies the color and the position along the gradient axis.</span></span> <span data-ttu-id="21a70-171">介於0.0 到1.0 之間的漸層位置值範圍。</span><span class="sxs-lookup"><span data-stu-id="21a70-171">The value of the gradient position ranges between 0.0 and 1.0.</span></span> <span data-ttu-id="21a70-172">越接近0.0，色彩就越接近漸層的開頭;接近1.0，色彩越接近漸層的結尾。</span><span class="sxs-lookup"><span data-stu-id="21a70-172">The closer it is to 0.0, the closer the color is to the start of the gradient; the closer it is to 1.0, the closer the color is to the end of the gradient.</span></span>

<span data-ttu-id="21a70-173">下圖強調漸層停駐點。</span><span class="sxs-lookup"><span data-stu-id="21a70-173">The following illustration highlights the gradient stops.</span></span> <span data-ttu-id="21a70-174">圓形會標示漸層停駐點的位置，而虛線則會顯示漸層軸。</span><span class="sxs-lookup"><span data-stu-id="21a70-174">The circle marks the position of gradient stops and a dashed line shows the gradient axis.</span></span>

![線性漸層筆刷的圖例，其中四個沿著軸停止](images/4stoplineargradient.png)

<span data-ttu-id="21a70-176">第一個漸層停駐點會在0.0 的位置指定黃色。</span><span class="sxs-lookup"><span data-stu-id="21a70-176">The first gradient stop specifies the color yellow at a position of 0.0.</span></span> <span data-ttu-id="21a70-177">第二個漸層停駐點會在0.25 的位置指定紅色的色彩。</span><span class="sxs-lookup"><span data-stu-id="21a70-177">The second gradient stop specifies red color at a position of 0.25.</span></span> <span data-ttu-id="21a70-178">從左至右，沿著漸層軸，這兩個停駐點的色彩會逐漸從黃色變更為紅色。</span><span class="sxs-lookup"><span data-stu-id="21a70-178">From left to right along the gradient axis, the colors between these two stops gradually change from yellow to red.</span></span> <span data-ttu-id="21a70-179">第三個漸層停駐點會在0.75 的位置指定藍色色彩。</span><span class="sxs-lookup"><span data-stu-id="21a70-179">The third gradient stop specifies blue color at a position of 0.75.</span></span> <span data-ttu-id="21a70-180">第二個和第三個漸層之間的色彩會逐漸從紅色變更為藍色。</span><span class="sxs-lookup"><span data-stu-id="21a70-180">The colors between the second and third gradient stops gradually change from red to blue.</span></span> <span data-ttu-id="21a70-181">第四個漸層停駐點會在1.0 的位置指定綠色綠色。</span><span class="sxs-lookup"><span data-stu-id="21a70-181">The fourth gradient stop specifies lime green at a position of 1.0.</span></span> <span data-ttu-id="21a70-182">第三和第四個漸層之間的色彩會逐漸從藍色變更為綠色。</span><span class="sxs-lookup"><span data-stu-id="21a70-182">The colors between the third and fourth gradient stops gradually change from blue to lime green.</span></span>

## <a name="the-gradient-axis"></a><span data-ttu-id="21a70-183">漸層軸</span><span class="sxs-lookup"><span data-stu-id="21a70-183">The gradient axis</span></span>

<span data-ttu-id="21a70-184">如先前所述，線性漸層筆刷的漸層停駐點沿著直線（漸層軸）放置。</span><span class="sxs-lookup"><span data-stu-id="21a70-184">As mentioned previously, gradient stops of a linear gradient brush are positioned along a line, the gradient axis.</span></span> <span data-ttu-id="21a70-185">當您建立線性漸層筆刷時，可以使用 [**D2D1 線性漸層 \_ \_ \_ 筆刷 \_ 屬性**](/windows/win32/api/d2d1/ns-d2d1-d2d1_linear_gradient_brush_properties)結構的 **startPoint** 和 **端點** 欄位，來指定線條的方向和大小。</span><span class="sxs-lookup"><span data-stu-id="21a70-185">You can specify the orientation and size of the line using the **startPoint** and **endPoint** fields of the [**D2D1\_LINEAR\_GRADIENT\_BRUSH\_PROPERTIES**](/windows/win32/api/d2d1/ns-d2d1-d2d1_linear_gradient_brush_properties) structure when you create a linear gradient brush.</span></span> <span data-ttu-id="21a70-186">建立筆刷之後，您可以藉由呼叫筆刷的 [**SetStartPoint**](/windows/win32/api/d2d1/nf-d2d1-id2d1lineargradientbrush-setstartpoint) 和 [**task.setendpoint**](/windows/win32/api/d2d1/nf-d2d1-id2d1lineargradientbrush-setendpoint) 方法來調整漸層軸。</span><span class="sxs-lookup"><span data-stu-id="21a70-186">After you've created a brush, you can adjust the gradient axis by calling the brush's [**SetStartPoint**](/windows/win32/api/d2d1/nf-d2d1-id2d1lineargradientbrush-setstartpoint) and [**SetEndPoint**](/windows/win32/api/d2d1/nf-d2d1-id2d1lineargradientbrush-setendpoint) methods.</span></span> <span data-ttu-id="21a70-187">藉由操作筆刷的起點和終點，您可以建立水準和垂直漸層、反轉漸層方向等。</span><span class="sxs-lookup"><span data-stu-id="21a70-187">By manipulating the brush's start point and end point, you can create horizontal and vertical gradients, reverse the gradient direction, and more.</span></span>

<span data-ttu-id="21a70-188">例如，在下圖中，起始點設定為 (0、0) 和結束點，以 (150，50) ;這會建立從左上角開始的對角線漸層，並延伸至繪製區域的右下角。</span><span class="sxs-lookup"><span data-stu-id="21a70-188">For example, in the following illustration, the start point is set to (0,0) and the end point to (150, 50); this creates a diagonal gradient that starts at the upper-left corner and extends to the lower-right corner of the area being painted.</span></span> <span data-ttu-id="21a70-189">當您將起點設定為 (0，25) ，而結束點設定為 (150，25) 時，會建立水準漸層。</span><span class="sxs-lookup"><span data-stu-id="21a70-189">When you set the start point to (0, 25) and the end point to (150, 25), a horizontal gradient is created.</span></span> <span data-ttu-id="21a70-190">同樣地，將起點設為 (75，0) ，而結束點設定為 (75，50) 會建立垂直漸層。</span><span class="sxs-lookup"><span data-stu-id="21a70-190">Similarly, setting the start point to (75, 0) and the end point to (75, 50) creates a vertical gradient.</span></span> <span data-ttu-id="21a70-191">將起點設定為 (0，50) ，結束點至 (150，0) 會建立從左下角開始並延伸至繪製區域右上角的對角線漸層。</span><span class="sxs-lookup"><span data-stu-id="21a70-191">Setting the start point to (0, 50) and the end point to (150, 0) creates a diagonal gradient that starts at the lower-left corner and extends to the upper-right corner of the area being painted.</span></span>

![橫跨相同矩形的四個不同漸層軸的圖例](images/linear-gradients.png)

## <a name="using-radial-gradient-brushes"></a><span data-ttu-id="21a70-193">使用放射狀漸層筆刷</span><span class="sxs-lookup"><span data-stu-id="21a70-193">Using radial gradient brushes</span></span>

<span data-ttu-id="21a70-194">不同于沿著漸層軸混合兩個或多個色彩的 [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)， [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) 會繪製具有放射漸層的區域，以將兩個或多個色彩混合在橢圓形上。</span><span class="sxs-lookup"><span data-stu-id="21a70-194">Unlike an [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), which blends two or more colors along a gradient axis, an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) paints an area with a radial gradient that blends two or more colors across an ellipse.</span></span> <span data-ttu-id="21a70-195">當 **ID2D1LinearGradientBrush** 使用起點和終點來定義其漸層軸時， **ID2D1RadialGradientBrush** 會藉由指定中心、水準和垂直半徑和漸層原點位移來定義其漸層橢圓。</span><span class="sxs-lookup"><span data-stu-id="21a70-195">While a **ID2D1LinearGradientBrush** defines its gradient axis with a start point and an end point, a **ID2D1RadialGradientBrush** defines its gradient ellipse by specifying a center, horizontal and vertical radii, and a gradient origin offset.</span></span>

<span data-ttu-id="21a70-196">如同 [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)， [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) 會使用 [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) 來指定漸層中的色彩和位置。</span><span class="sxs-lookup"><span data-stu-id="21a70-196">Like an [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) uses an [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) to specify the colors and positions in the gradient.</span></span>

<span data-ttu-id="21a70-197">下圖顯示以 [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)繪製的圓形。</span><span class="sxs-lookup"><span data-stu-id="21a70-197">The following illustration shows a circle painted with an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush).</span></span> <span data-ttu-id="21a70-198">圓形有兩個漸層停駐點：第一個會在0.0 的位置指定預先定義的色彩 "黃"，而第二個則指定在1.0 位置的預先定義色彩 "ForestGreen"。</span><span class="sxs-lookup"><span data-stu-id="21a70-198">The circle has two gradient stops: the first specifies a predefined color "Yellow" at a position of 0.0, and the second specifies a predefined color "ForestGreen" at a position of 1.0.</span></span> <span data-ttu-id="21a70-199">漸層的中心有 (75、75) 、 (0、0) 的漸層原點位移，以及75的 x 和 y 半徑。</span><span class="sxs-lookup"><span data-stu-id="21a70-199">The gradient has a center of (75, 75), a gradient origin offset of (0, 0), and an x- and y-radius of 75.</span></span>

![以放射狀漸層筆刷繪製的圓形圖例](images/brushes-ovw-radials.png)

<span data-ttu-id="21a70-201">下列程式碼範例示範如何使用具有兩色色的 [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) 繪製此圓形：「黃色」在0.0 的位置，而「ForestGreen」在1.0。</span><span class="sxs-lookup"><span data-stu-id="21a70-201">The following code examples shows how to paint this circle with an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) that has two color stops: "Yellow" at a position of 0.0, and "ForestGreen" at a position of 1.0.</span></span> <span data-ttu-id="21a70-202">類似于建立 [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)，此範例會呼叫 [**CreateGradientStopCollection**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)) ，以從漸層停駐點的陣列建立 [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) 。</span><span class="sxs-lookup"><span data-stu-id="21a70-202">Similar to creating an [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), the example calls [**CreateGradientStopCollection**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)) to create an [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) from an array of gradient stops.</span></span>


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



<span data-ttu-id="21a70-203">若要建立 [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)，請使用 [**ID2D1RenderTarget：： CreateRadialGradientBrush**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createradialgradientbrush) 方法。</span><span class="sxs-lookup"><span data-stu-id="21a70-203">To create an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush), use the [**ID2D1RenderTarget::CreateRadialGradientBrush**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createradialgradientbrush) method.</span></span> <span data-ttu-id="21a70-204">**CreateRadialGradientBrush** 會採用三個參數。</span><span class="sxs-lookup"><span data-stu-id="21a70-204">The **CreateRadialGradientBrush** takes three parameters.</span></span> <span data-ttu-id="21a70-205">第一個參數是 D2D1 星形漸層 [**\_ \_ \_ 筆刷 \_ 屬性**](/windows/win32/api/d2d1/ns-d2d1-d2d1_radial_gradient_brush_properties) ，會指定漸層的中心、漸層原點位移和水準和垂直半徑。</span><span class="sxs-lookup"><span data-stu-id="21a70-205">The first parameter, a [**D2D1\_RADIAL\_GRADIENT\_BRUSH\_PROPERTIES**](/windows/win32/api/d2d1/ns-d2d1-d2d1_radial_gradient_brush_properties) specifies the center, gradient origin offset, and the horizontal and vertical radii of the gradient.</span></span> <span data-ttu-id="21a70-206">第二個參數是描述色彩及其在漸層中之位置的 [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) ，而第三個參數是接收新 **ID2D1RadialGradientBrush** 參考之指標的位址。</span><span class="sxs-lookup"><span data-stu-id="21a70-206">The second parameter is an [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) that describes the colors and their positions in the gradient, and the third parameter is the address of the pointer that receive the new **ID2D1RadialGradientBrush** reference.</span></span> <span data-ttu-id="21a70-207">某些多載會採用額外的參數，也就是 [**D2D1 \_ 筆刷 \_ 屬性**](/windows/win32/api/d2d1/ns-d2d1-d2d1_brush_properties) 結構，指定不透明度值和要套用至新筆刷的轉換。</span><span class="sxs-lookup"><span data-stu-id="21a70-207">Some overloads take an additional parameter, a [**D2D1\_BRUSH\_PROPERTIES**](/windows/win32/api/d2d1/ns-d2d1-d2d1_brush_properties) structure that specifies an opacity value and a transform to apply to the new brush.</span></span>

<span data-ttu-id="21a70-208">下一個範例會呼叫 [**CreateRadialGradientBrush**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createradialgradientbrush)，傳入漸層停駐的陣列，以及將 *中間* 值設定為 (75、75) 、將 *gradientOriginOffset* 設為 (0、0) 和 *radiusX* 和 *radiusY* 兩者都設為75的星形漸層筆刷屬性。</span><span class="sxs-lookup"><span data-stu-id="21a70-208">The next example calls [**CreateRadialGradientBrush**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createradialgradientbrush), passing in the array of gradient stops, and the radial gradient brush properties that have the *center* value set to (75, 75), the *gradientOriginOffset* set to (0, 0), and *radiusX* and *radiusY* both set to 75.</span></span>


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



<span data-ttu-id="21a70-209">最後一個範例會使用筆刷來填滿橢圓形。</span><span class="sxs-lookup"><span data-stu-id="21a70-209">The final example uses the brush to fill an ellipse.</span></span>


```C++
m_pRenderTarget->FillEllipse(ellipse, m_pRadialGradientBrush);
m_pRenderTarget->DrawEllipse(ellipse, m_pBlackBrush, 1, NULL);
```



### <a name="configuring-a-radial-gradient"></a><span data-ttu-id="21a70-210">設定放射狀漸層</span><span class="sxs-lookup"><span data-stu-id="21a70-210">Configuring a radial gradient</span></span>

<span data-ttu-id="21a70-211">*Center*、 *gradientOriginOffset*、 *radiusX* 和/或 *radiusY* 的不同值會產生不同的漸層。</span><span class="sxs-lookup"><span data-stu-id="21a70-211">Different values for *center*, *gradientOriginOffset*, *radiusX* and/or *radiusY* produce different gradients.</span></span> <span data-ttu-id="21a70-212">下圖顯示幾個具有不同漸層原點位移的放射狀漸層，並建立從不同角度照亮圓形的光線外觀。</span><span class="sxs-lookup"><span data-stu-id="21a70-212">The following illustration shows several radial gradients that have different gradient origin offsets, creating the appearance of the light illuminating the circles from different angles.</span></span>

![使用不同來源位移繪製放射狀漸層筆刷的相同圓形圖例](images/radialgradient.png)

## <a name="using-bitmap-brushes"></a><span data-ttu-id="21a70-214">使用點陣圖筆刷</span><span class="sxs-lookup"><span data-stu-id="21a70-214">Using bitmap brushes</span></span>

<span data-ttu-id="21a70-215">[**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush)繪製一個具有點陣圖 (的區域，) 由 [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap)物件表示。</span><span class="sxs-lookup"><span data-stu-id="21a70-215">An [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) paints an area with a bitmap (represented by an [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) object).</span></span>

<span data-ttu-id="21a70-216">下圖顯示以植物點陣圖繪製的正方形。</span><span class="sxs-lookup"><span data-stu-id="21a70-216">The following illustration shows a square painted with a bitmap of a plant.</span></span>

![以植物點陣圖繪製的正方形圖例](images/brushes-ovw-bitmap.png)

<span data-ttu-id="21a70-218">下列範例顯示如何使用 [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush)繪製此正方形。</span><span class="sxs-lookup"><span data-stu-id="21a70-218">The examples that follow shows how to paint this square with an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush).</span></span>

<span data-ttu-id="21a70-219">第一個範例會初始化與筆刷搭配使用的 [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) 。</span><span class="sxs-lookup"><span data-stu-id="21a70-219">The first example initializes an [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) for use with the brush.</span></span> <span data-ttu-id="21a70-220">**ID2D1Bitmap** 由範例中其他位置所定義的 Helper 方法 LoadResourceBitmap 提供。</span><span class="sxs-lookup"><span data-stu-id="21a70-220">The **ID2D1Bitmap** is provided by a helper method, LoadResourceBitmap, defined elsewhere in the sample.</span></span>


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



<span data-ttu-id="21a70-221">若要建立點陣圖筆刷，請呼叫 [**ID2D1RenderTarget：： CreateBitmapBrush**](id2d1rendertarget-createbitmapbrush.md) 方法，並指定要繪製的 [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) 。</span><span class="sxs-lookup"><span data-stu-id="21a70-221">To create the bitmap brush, call the [**ID2D1RenderTarget::CreateBitmapBrush**](id2d1rendertarget-createbitmapbrush.md) method and specify the [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) with which to paint.</span></span> <span data-ttu-id="21a70-222">方法會傳回 **HRESULT** 和 [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) 物件。</span><span class="sxs-lookup"><span data-stu-id="21a70-222">The method returns an **HRESULT** and an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) object.</span></span> <span data-ttu-id="21a70-223">某些 **CreateBitmapBrush** 多載可讓您藉由接受 [**D2D1 \_ 筆刷 \_ 屬性**](/windows/win32/api/d2d1/ns-d2d1-d2d1_brush_properties) 和 [**D2D1 \_ 點陣圖 \_ 筆刷 \_ 屬性**](/windows/win32/api/d2d1/ns-d2d1-d2d1_bitmap_brush_properties) 結構，來指定其他選項。</span><span class="sxs-lookup"><span data-stu-id="21a70-223">Some **CreateBitmapBrush** overloads enable you to specify additional options by accepting a [**D2D1\_BRUSH\_PROPERTIES**](/windows/win32/api/d2d1/ns-d2d1-d2d1_brush_properties) and a [**D2D1\_BITMAP\_BRUSH\_PROPERTIES**](/windows/win32/api/d2d1/ns-d2d1-d2d1_bitmap_brush_properties) structure.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = m_pRenderTarget->CreateBitmapBrush(
        m_pBitmap,
        &m_pBitmapBrush
        );
}
```



<span data-ttu-id="21a70-224">下一個範例會使用筆刷來填滿矩形。</span><span class="sxs-lookup"><span data-stu-id="21a70-224">The next example uses the brush to fill a rectangle.</span></span>


```C++
m_pRenderTarget->FillRectangle(&rcBrushRect, m_pBitmapBrush);
```



## <a name="configuring-extend-modes"></a><span data-ttu-id="21a70-225">設定延伸模式</span><span class="sxs-lookup"><span data-stu-id="21a70-225">Configuring extend modes</span></span>

<span data-ttu-id="21a70-226">有時候，漸層筆刷的漸層或點陣圖筆刷的點陣圖，並不會完全填滿正在繪製的區域。</span><span class="sxs-lookup"><span data-stu-id="21a70-226">Sometimes, the gradient of a gradient brush or the bitmap for a bitmap brush doesn't completely fill the area being painted.</span></span>

-   <span data-ttu-id="21a70-227">當 [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush)發生這種情況時，Direct2D 會使用筆刷的水準 ([**SetExtendModeX**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmapbrush-setextendmodex)) 和垂直 ([**SetExtendModeY**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmapbrush-setextendmodey)) 延伸模式設定，以決定如何填滿剩餘的區域。</span><span class="sxs-lookup"><span data-stu-id="21a70-227">When this happens for an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), Direct2D uses the brush's horizontal ([**SetExtendModeX**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmapbrush-setextendmodex)) and vertical ([**SetExtendModeY**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmapbrush-setextendmodey)) extend mode settings to determine how to fill the remaining area.</span></span>

-   <span data-ttu-id="21a70-228">當漸層筆刷發生這種情況時，Direct2D 會決定如何使用您在呼叫 [**CreateGradientStopCollection**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection))時所指定的 [**D2D1 \_ 延伸 \_ 模式**](/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode)參數值來填滿剩餘的區域，以建立漸層筆刷的 [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection)。</span><span class="sxs-lookup"><span data-stu-id="21a70-228">When this happens for a gradient brush, Direct2D determines how to fill the remaining area by using the value of the [**D2D1\_EXTEND\_MODE**](/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode) parameter that you specified when you called the [**CreateGradientStopCollection**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)) to create the gradient brush's [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection).</span></span>

<span data-ttu-id="21a70-229">下圖顯示 [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush)的擴充模式的每個可能組合的結果： [**D2D1 \_ 擴充 \_ 模式的 \_ 夾具**](/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode) (夾具) 、 **D2D1 \_ 延伸 \_ 模式 \_ 包裝** (換行) ，以及 **D2D1 \_ 擴充 \_ 鏡像** (鏡像) 。</span><span class="sxs-lookup"><span data-stu-id="21a70-229">The following illustration shows the results from every possible combination of the extend modes for an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush): [**D2D1\_EXTEND\_MODE\_CLAMP**](/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode) (CLAMP), **D2D1\_EXTEND\_MODE\_WRAP** (WRAP), and **D2D1\_EXTEND\_MIRROR** (MIRROR).</span></span>

![來自各種擴充模式的原始影像和產生影像的圖例](images/bitmapwrap-clamp-mirror.png)

<span data-ttu-id="21a70-231">下列範例顯示如何將點陣圖筆刷的 x 和 y 擴充模式設定為 [**D2D1 \_ 擴充 \_ 鏡像**](/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode)。</span><span class="sxs-lookup"><span data-stu-id="21a70-231">The following example shows how to set the bitmap brush's x- and y-extend modes to [**D2D1\_EXTEND\_MIRROR**](/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode).</span></span> <span data-ttu-id="21a70-232">然後使用 [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush)繪製矩形。</span><span class="sxs-lookup"><span data-stu-id="21a70-232">It then paints the rectangle with the [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush).</span></span>


```C++
m_pBitmapBrush->SetExtendModeX(D2D1_EXTEND_MODE_MIRROR);
m_pBitmapBrush->SetExtendModeY(D2D1_EXTEND_MODE_MIRROR);

m_pRenderTarget->FillRectangle(exampleRectangle, m_pBitmapBrush);
```



<span data-ttu-id="21a70-233">它會產生如下圖所示的輸出。</span><span class="sxs-lookup"><span data-stu-id="21a70-233">It produces output as shown in the following illustration.</span></span>

![鏡像 x 方向和 y 方向之後的原始影像和產生影像的圖例](images/brushes-ovw-bitmapmirrormirror.png)

## <a name="transforming-brushes"></a><span data-ttu-id="21a70-235">轉換筆刷</span><span class="sxs-lookup"><span data-stu-id="21a70-235">Transforming brushes</span></span>

<span data-ttu-id="21a70-236">當您使用筆刷繪製時，它會在呈現目標的座標空間中繪製。</span><span class="sxs-lookup"><span data-stu-id="21a70-236">When you paint with a brush, it paints in the coordinate space of the render target.</span></span> <span data-ttu-id="21a70-237">筆刷不會自動自行定位，以配合正在繪製的物件;根據預設，它們會在呈現目標的原點 (0、0) 開始繪製。</span><span class="sxs-lookup"><span data-stu-id="21a70-237">Brushes do not automatically position themselves to align with the object being painted; by default, they begin painting at the origin (0, 0) of the render target.</span></span>

<span data-ttu-id="21a70-238">您可以藉由設定起點和終點，將 [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) 所定義的漸層「移動」至目的地區域。</span><span class="sxs-lookup"><span data-stu-id="21a70-238">You can "move" the gradient defined by an [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) to a target area by setting its start point and end point.</span></span> <span data-ttu-id="21a70-239">同樣地，您可以藉由變更中央和半徑來移動 [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) 所定義的漸層。</span><span class="sxs-lookup"><span data-stu-id="21a70-239">Likewise, you can move the gradient defined by an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) by changing its center and radii.</span></span>

<span data-ttu-id="21a70-240">若要將 [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) 的內容對齊正在繪製的區域，您可以使用 [**SetTransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f)) 方法將點陣圖轉譯為所需的位置。</span><span class="sxs-lookup"><span data-stu-id="21a70-240">To align the content of an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) to the area being painted, you can use the [**SetTransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f)) method to translate the bitmap to the desired location.</span></span> <span data-ttu-id="21a70-241">此轉換只會影響筆刷;它不會影響呈現目標所繪製的任何其他內容。</span><span class="sxs-lookup"><span data-stu-id="21a70-241">This transform only affects the brush; it does not affect any other content drawn by the render target.</span></span>

<span data-ttu-id="21a70-242">下圖顯示使用 [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) 填滿位於 (100，100) 之矩形的效果。</span><span class="sxs-lookup"><span data-stu-id="21a70-242">The following illustrations shows the effect of using an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) to fill a rectangle located at (100, 100).</span></span> <span data-ttu-id="21a70-243">左圖上的圖例顯示填滿矩形的結果，而不會轉換筆刷：點陣圖是在轉譯目標的原點繪製。</span><span class="sxs-lookup"><span data-stu-id="21a70-243">The illustration on the left illustration shows the result of filling the rectangle without transforming the brush: the bitmap is drawn at the render target's origin.</span></span> <span data-ttu-id="21a70-244">如此一來，矩形中只會出現點陣圖的一部分。</span><span class="sxs-lookup"><span data-stu-id="21a70-244">As a result, only a portion of the bitmap appears in the rectangle.</span></span> <span data-ttu-id="21a70-245">右邊的圖例顯示轉換 **ID2D1BitmapBrush** 的結果，使其內容會向右移動50圖元，並向下移動50圖元。</span><span class="sxs-lookup"><span data-stu-id="21a70-245">The illustration on the right shows the result of transforming the **ID2D1BitmapBrush** so that its content is shifted 50 pixels to the right and 50 pixels down.</span></span> <span data-ttu-id="21a70-246">點陣圖現在會填滿矩形。</span><span class="sxs-lookup"><span data-stu-id="21a70-246">The bitmap now fills the rectangle.</span></span>

![以點陣圖筆刷繪製，而不轉換筆刷和轉換筆刷的正方形圖例](images/brushes-ovw-transform.png)

<span data-ttu-id="21a70-248">下列程式碼示範如何完成這項工作。</span><span class="sxs-lookup"><span data-stu-id="21a70-248">The following code shows how to accomplish this.</span></span> <span data-ttu-id="21a70-249">首先，將翻譯套用至 [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush)，並沿著 y 軸沿著 X 軸和50圖元向下移動筆刷50圖元。</span><span class="sxs-lookup"><span data-stu-id="21a70-249">First apply a translation to the [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), moving the brush 50 pixels right along the x-axis and 50 pixels down along the y-axis.</span></span> <span data-ttu-id="21a70-250">然後使用 **ID2D1BitmapBrush** 來填滿左上角的矩形，其位於 (100、100) ，而右下角的 (200，200) 。</span><span class="sxs-lookup"><span data-stu-id="21a70-250">Then use the **ID2D1BitmapBrush** to fill the rectangle that has the upper-left corner at (100, 100) and the lower-right corner at (200, 200).</span></span>


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

## <a name="related-topics"></a><span data-ttu-id="21a70-251">相關主題</span><span class="sxs-lookup"><span data-stu-id="21a70-251">Related topics</span></span>

* [<span data-ttu-id="21a70-252">Direct2D 參考</span><span class="sxs-lookup"><span data-stu-id="21a70-252">Direct2D reference</span></span>](reference.md)
* [<span data-ttu-id="21a70-253">如何建立純色筆刷</span><span class="sxs-lookup"><span data-stu-id="21a70-253">How to create a solid color brush</span></span>](how-to-create-a-solid-color-brush.md)
* [<span data-ttu-id="21a70-254">如何建立線性漸層筆刷</span><span class="sxs-lookup"><span data-stu-id="21a70-254">How to create a linear gradient brush</span></span>](how-to-create-a-linear-gradient-brush.md)
* [<span data-ttu-id="21a70-255">如何建立放射狀漸層筆刷</span><span class="sxs-lookup"><span data-stu-id="21a70-255">How to create a radial gradient brush</span></span>](how-to-create-a-radial-gradient-brush.md)
* [<span data-ttu-id="21a70-256">如何建立點陣圖筆刷</span><span class="sxs-lookup"><span data-stu-id="21a70-256">How to create a bitmap brush</span></span>](how-to-create-a-bitmap-brush.md)

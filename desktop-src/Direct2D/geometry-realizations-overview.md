---
title: 幾何實現概觀
description: 本主題說明如何使用 Direct2D geometry 實踐，在某些案例中改善應用程式的幾何呈現效能。
ms.assetid: E8C4C4E5-3102-4F53-847E-A4C2D12A6921
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b903e047ee58a803a7584aaca407281fc803e30
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106968287"
---
# <a name="geometry-realizations-overview"></a>幾何實現概觀

本主題說明如何使用 [Direct2D](direct2d-portal.md) geometry 實踐，在某些案例中改善應用程式的幾何呈現效能。

它包含下列區段：

-   [什麼是幾何實踐？](#what-are-geometry-realizations)
-   [為何要使用 geometry 實踐？](#why-use-geometry-realizations)
-   [使用 geometry 的時機實踐](#when-to-use-geometry-realizations)
-   [建立幾何實踐](#creating-geometry-realizations)
-   [繪製幾何實踐](#drawing-geometry-realizations)
-   [調整幾何實踐](#scaling-geometry-realizations)
    -   [在無法調整的應用程式中使用 geometry 實踐](#using-geometry-realizations-in-apps-that-do-not-scale)
    -   [在以小規模調整規模的應用程式中使用幾何實踐](#using-geometry-realizations-in-apps-that-scale-by-a-small-amount)
    -   [在以大量規模調整的應用程式中使用幾何實踐](#using-geometry-realizations-in-apps-that-scale-by-a-large-amount)
-   [相關主題](#related-topics)

## <a name="what-are-geometry-realizations"></a>什麼是幾何實踐？

幾何實踐（Windows 8.1 中引進）是一種新的繪圖基本類型，可讓 [Direct2D](direct2d-portal.md) 應用程式在某些情況下輕鬆地改善幾何轉譯效能。 幾何實踐是以 [**ID2D1GeometryRealization**](/windows/win32/api/d2d1_2/nn-d2d1_2-id2d1geometryrealization) 介面表示。

## <a name="why-use-geometry-realizations"></a>為何要使用 geometry 實踐？

當 [Direct2D](direct2d-portal.md) 轉譯 [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) 物件時，它必須將該幾何轉換成圖形硬體透過稱為鑲嵌的程式來理解的表單。 一般而言，Direct2D 必須 tessellate 繪圖的每個框架，即使幾何未變更也是一樣。 如果您的應用程式會在每個畫面格呈現相同的幾何，則重複的鑲嵌表示浪費的計算工作。 快取鑲嵌（甚至是完整的點陣化幾何），以及繪製該快取的標記法，而不是重複鑲嵌，會比較有效率。

開發人員解決此問題的常見方式是快取幾何的完整光柵。 尤其是建立新的點陣圖、將幾何柵格化至該點陣圖，然後視需要將該點陣圖繪製到場景的一般。  (這種方法會在改善 Direct2D 應用程式效能的 [幾何](improving-direct2d-performance.md) 轉譯區段中說明。 ) 雖然此方法的運算效率很高，但卻有一些缺點：

-   快取點陣圖對套用至場景的轉換變更很敏感。 例如，調整點陣化可能會導致明顯的調整構件。 使用高品質的調整演算法來緩和這些構件可能會耗用大量運算資源。
-   快取的點陣圖會耗用大量的記憶體，特別是在高解析度上進行柵格化時。

幾何實踐提供另一種方式來快取幾何，以避免發生上述缺點。 幾何實踐是以圖元為單位來表示 (，就像是完整的點陣化) ，而不是透過數學平面的點。 基於這個理由，它們的機密性與調整和其他操作的完整 rasterizations 較不敏感，而且會耗用明顯較少的記憶體。

## <a name="when-to-use-geometry-realizations"></a>使用 geometry 的時機實踐

當您的應用程式呈現不常變更但可能受限於變更轉換的複雜幾何時，請考慮使用幾何實踐。

例如，假設有一個對應應用程式會顯示靜態地圖，但是可讓使用者放大和縮小。此應用程式可受益于使用幾何實踐。 由於正在轉譯的幾何會保持靜態，因此快取這些幾何有助於節省鑲嵌式工作的目的。 但由於地圖是在使用者縮放時進行調整，因此因為調整成品，所以快取完整的點陣化並不理想。 快取幾何實踐可讓應用程式避免重新分割的工作，同時在調整期間維持高視覺品質。

另一方面，請考慮具有會持續變更之動畫幾何的 kaleidoscope 應用程式。 此應用程式可能不會受益于使用幾何實踐。 因為圖形本身會從框架變更為框架，所以快取其鑲嵌並不有用。 此應用程式的最佳方法是直接繪製 [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) 物件。

## <a name="creating-geometry-realizations"></a>建立幾何實踐

必須從現有的 [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry)物件建立 [**ID2D1GeometryRealization**](/windows/win32/api/d2d1_2/nn-d2d1_2-id2d1geometryrealization)物件。 若要建立幾何實現，請呼叫 [**CreateFilledGeometryRealization**](/windows/win32/api/d2d1_2/nf-d2d1_2-id2d1devicecontext1-createfilledgeometryrealization) 方法或 [**CreateStrokedGeometryRealization**](/windows/win32/api/d2d1_2/nf-d2d1_2-id2d1devicecontext1-createstrokedgeometryrealization) 方法，並傳入要實現的 **ID2D1Geometry** 。

-   [**CreateFilledGeometryRealization**](/windows/win32/api/d2d1_2/nf-d2d1_2-id2d1devicecontext1-createfilledgeometryrealization) 會建立圖形內部的實現：要藉由呼叫 [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry)繪製的區域。
-   [**CreateStrokedGeometryRealization**](/windows/win32/api/d2d1_2/nf-d2d1_2-id2d1devicecontext1-createstrokedgeometryrealization) 會建立圖形筆劃的實現：要藉由呼叫 [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry)繪製的區域。

這兩種類型的幾何實現都會以 [**ID2D1GeometryRealization**](/windows/win32/api/d2d1_2/nn-d2d1_2-id2d1geometryrealization) 介面表示。

建立幾何實現時， [Direct2D](direct2d-portal.md) 必須將所提供幾何中的任何曲線壓平合併成多邊形近似值。 您必須將簡維容錯參數提供給建立方法，這會指定幾何的真正曲線與其多邊形近似值之間的最大距離（以與裝置無關的圖元為單位） (Dip) 。 您提供的簡維容限越低，所產生之幾何實現物件的精確度就愈高。 同樣地，提供較高的簡維公差會產生較低精確度的幾何實現。 請注意，更高精確度幾何實踐的繪製成本比較低的精確度更高，但可以在引進可見成品之前進一步調整。 如需使用簡維容限的指引，請參閱下方的 [縮放幾何實踐](#scaling-geometry-realizations) 。

> [!Note]  
> 幾何實現物件與特定圖形裝置相關聯：它們是與裝置相關的資源。

 

## <a name="drawing-geometry-realizations"></a>繪製幾何實踐

繪製幾何實踐類似于繪製其他 [Direct2D](direct2d-portal.md) 基本專案，例如點陣圖。 若要這樣做，請呼叫 [**DrawGeometryRealization**](/windows/win32/api/d2d1_2/nf-d2d1_2-id2d1devicecontext1-drawgeometryrealization) 方法，並將要繪製的幾何實現物件和要使用的筆刷傳遞給它。 如同其他 Direct2D 繪圖方法，您必須在對 [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw)和 [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw)的呼叫之間呼叫 **DrawGeometryRealization** 。

## <a name="scaling-geometry-realizations"></a>調整幾何實踐

幾何實踐就像其他 [Direct2D](direct2d-portal.md) 基本專案一樣，會遵循裝置內容上的轉換集。 雖然平移和旋轉轉換對幾何實踐的視覺品質沒有任何影響，但調整規模轉換可以產生視覺構件。

尤其是，將夠大的小數位數套用至任何幾何實現可以顯示真正曲線的多邊形近似值。 此處的影像顯示一組橢圓形幾何實踐 (填滿和筆劃) 已相應放大。 曲線-簡維構件是可見的。

![一組橢圓形幾何實踐 (填滿和筆劃) ，已相應放大。 曲線-簡維構件是可見的。](images/zoomed-in.png)

區分視覺品質的應用程式應該採取措施來確保不會發生這種情況。 您處理調整的方式取決於您的應用程式需求。 以下是數種不同類型應用程式的幾個建議方法。

### <a name="using-geometry-realizations-in-apps-that-do-not-scale"></a>在無法調整的應用程式中使用 geometry 實踐

如果您的應用程式不會在幾何實踐上執行任何調整，則可以使用單一簡維容錯來安全地建立實踐一次。  (非縮放轉換並不會影響呈現幾何實踐的視覺品質。 ) 使用 [**ComputeFlatteningTolerance**](/previous-versions/windows/desktop/legacy/dn280327(v=vs.85)) 函式來計算 DPI 的適當簡維容限：


```C++
    float dpiX, dpiY;
    deviceContext->GetDpi(&dpiX, &dpiY);

    float flatteningTolerance = D2D1::ComputeFlatteningTolerance(
        D2D1::Matrix3x2F::Identity(),   // apply no additional scaling transform
        dpiX,                           // horizontal DPI
        dpiY                            // vertical DPI
        );
```



### <a name="using-geometry-realizations-in-apps-that-scale-by-a-small-amount"></a>在以小規模調整規模的應用程式中使用幾何實踐

如果您的應用程式只能以少量的 (（例如，最多2x 或 3) 倍）來調整幾何的實現，則最好只以比例較低的簡維容限來建立幾何實現一次，而不是預設值。 這會建立更高精確度的實現，可在產生調整構件之前大幅相應增加;權衡代價是，繪製更高精確度的實現需要更多工作。

例如，假設您知道您的應用程式永遠不會將幾何實現調整為超過2倍。 您的應用程式可以使用預設值一半的簡維容錯來建立幾何實現，並視需要調整實現，最多可達2倍。 使用 [**ComputeFlatteningTolerance**](/previous-versions/windows/desktop/legacy/dn280327(v=vs.85)) 函式來計算適當的簡維容限，方法是將2.0 傳遞為 *maxZoomFactor* 參數：


```C++
    float dpiX, dpiY;
    deviceContext->GetDpi(&dpiX, &dpiY);
    
    float flatteningTolerance = D2D1::ComputeFlatteningTolerance(
        D2D1::Matrix3x2F::Identity(),   // apply no additional scaling transform
        dpiX,                           // horizontal DPI
        dpiY,                           // vertical DPI
        2.0f                            // realization can be scaled by an additional 2x
        );
```



### <a name="using-geometry-realizations-in-apps-that-scale-by-a-large-amount"></a>在以大量規模調整的應用程式中使用幾何實踐

如果您的應用程式可以將幾何的數量調整為大量 (例如10倍以上的) ，則適當地處理調整會更複雜。

針對大部分的應用程式，建議的方法是在場景相應增加時，以逐漸較低的簡維公差重新建立幾何實現，以維持視覺效果的精確度，並避免調整成品。 同樣地，當場景縮小時，應用程式應該以逐漸較高的簡維公差重新建立幾何實踐，以避免 wastefully 無法顯示的呈現詳細資料。 應用程式不應該在每次調整規模時重新建立幾何實踐，因為這樣做會使您無法快取鑲嵌式工作的目的。 相反地，應用程式應該不常重新建立幾何實踐：例如，每隔2倍增加或減少尺規。

每次調整應用程式中的規模，以回應使用者互動時，應用程式可以將新的規模與上次建立幾何實踐的尺規做比較 (儲存，例如，在 **m \_ lastScale** 成員) 中。 如果兩個值都是 close (在此案例中，在 2) 的因數內，則不會採取進一步的動作。 但是，如果這兩個值不是關閉的，則會重新建立幾何實踐。 [**ComputeFlatteningTolerance**](/previous-versions/windows/desktop/legacy/dn280327(v=vs.85))函式可用來計算適用于新尺規的簡維容限，而 **m \_ lastScale** 會更新為新的尺規。

此外，應用程式一律會使用較小的容錯來建立實踐，其使用方式會比通常用於新的小數位數還要小，方法是將2的值當做 *maxZoomFactor* 參數傳遞至 [**ComputeFlatteningTolerance**](/previous-versions/windows/desktop/legacy/dn280327(v=vs.85))。 這可讓新的幾何實踐以額外的因數2來相應增加，而不會產生調整成品。

> [!Note]  
> 此處所述的方法可能不適合所有的應用程式。 比方說，如果您的應用程式允許以非常大的因素來調整場景 (例如，如果它包含可從100% 移至1000000% 的「縮放」滑杆（在幾個) 框架的範圍內），則這種方法可能會藉由重新建立每個畫面格的幾何實踐來產生過度的工作。 替代方法是在每次完成場景規模的操作之後，才重新建立幾何實踐，例如，在使用者完成縮小手勢) 之後 (。

 

## <a name="related-topics"></a>相關主題

[幾何概觀](direct2d-geometries-overview.md)

[改善 Direct2D 應用程式的效能](improving-direct2d-performance.md)

[呈現複雜靜態內容的一般指導方針](improving-direct2d-performance.md)

[**ID2D1DeviceCoNtext1**](/windows/win32/api/d2d1_2/nn-d2d1_2-id2d1devicecontext1)

[**ID2D1GeometryRealization**](/windows/win32/api/d2d1_2/nn-d2d1_2-id2d1geometryrealization)

[**ComputeFlatteningTolerance 函式**](/previous-versions/windows/desktop/legacy/dn280327(v=vs.85))
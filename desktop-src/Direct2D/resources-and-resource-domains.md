---
title: 資源總覽
description: 描述 Direct2D 資源，以及如何共用這些資源。
ms.assetid: afd308a7-9524-4436-9a0e-8575383d96fa
keywords:
- Direct2D，資源
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: bf4eb807a25b592e32a2d83436532af17462d70c
ms.sourcegitcommit: 7d0cc7eb398fee8f5be55cd654a12d29937d643c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/08/2021
ms.locfileid: "104321376"
---
# <a name="resources-overview"></a>資源總覽

Direct2D 資源是用來繪製和以 Direct2D 介面（例如 [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) 或 [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)）表示的物件。 本主題說明 Direct2D 資源的種類，以及如何共用這些資源。

本主題包含下列幾節：

-   [關於 Direct2D 資源](#about-direct2d-resources)
-   [與裝置無關的資源](#device-independent-resources)
-   [裝置相依的資源](#device-dependent-resources)
-   [共用 Factory 資源](#sharing-factory-resources)
-   [共用呈現目標資源](#sharing-render-target-resources)
    -   [硬體呈現目標](#hardware-render-targets)
    -   [DXGI 介面呈現目標](#dxgi-surface-render-targets)
    -   [相容的呈現目標和共用點陣圖](#compatible-render-targets-and-shared-bitmaps)

## <a name="about-direct2d-resources"></a>關於 Direct2D 資源

許多硬體加速 2D Api 都是針對 CPU 導向的資源模型，以及一組可在 Cpu 上運作正常的轉譯作業所設計。然後，API 的部分是硬體加速。 執行這些 Api 需要資源管理員，以將 CPU 資源對應至 GPU 上的資源。 由於 GPU 限制，某些作業可能無法在每種情況下加速。 在這些情況下，資源管理員必須在 CPU 與 GPU 之間來回進行通訊， (這種情況很昂貴) ，因此可以轉換為 CPU 轉譯。 在某些情況下，它可能會無法預期地強制轉譯為完全回復到 CPU。 此外，顯示簡單的轉譯作業可能需要暫時性的中繼轉譯步驟，這些步驟不會在 API 中公開，且需要額外的 GPU 資源。

Direct2D 可提供更直接的對應，以充分利用 GPU。 它提供兩種類別的資源：裝置獨立和裝置相依。

-   與裝置無關的資源（例如 [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry)）會保留在 CPU 上。
-   裝置相依的資源（例如 [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) 和 [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)）可在硬體加速可用時，直接對應至 GPU (上的資源) 。 轉譯呼叫的執行方式，是將幾何和涵蓋範圍資訊與裝置相依資源所產生的紋理資訊結合在一起。

當您建立裝置相依的資源時，系統資源 (可用的 GPU （如果有的話），或在裝置建立時配置的 CPU) ，而不會從某個轉譯作業變更為另一個。 這種情況下就不需要資源管理員。 除了排除資源管理員所提供的一般效能改進之外，此模型還可讓您直接控制任何中繼轉譯。

由於 Direct2D 可對資源提供太多控制權，因此您必須瞭解不同種類的資源，以及這些資源可以搭配使用的時機。

## <a name="device-independent-resources"></a>Device-Independent 資源

如上一節所述，與裝置無關的資源一律位於 CPU 上，而且永遠不會與硬體轉譯裝置產生關聯。 以下是與裝置無關的資源：

-   [**ID2D1DrawingStateBlock**](/windows/win32/api/d2d1/nn-d2d1-id2d1drawingstateblock)
-   [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)
-   [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) 和繼承自它的介面。
-   [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink)和 [ **ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink)
-   [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle)

使用 [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)本身是與裝置無關的資源，來建立與裝置無關的資源。  (若要建立 factory，請使用 [**CreateFactory**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory) 函數。 ) 

除了轉譯目標之外，處理站所建立的所有資源都與裝置無關。 轉譯目標是與裝置相關的資源。

## <a name="device-dependent-resources"></a>Device-Dependent 資源

未在前一個清單中命名的任何資源，都是與裝置相關的資源。 與裝置相關的資源會與特定的轉譯裝置相關聯。 當硬體加速可用時，該裝置就是 GPU。 在其他情況下，則是 CPU。

若要建立與裝置相關的大部分資源，請使用呈現目標。 在大多數情況下，請使用 factory 來建立轉譯目標。

以下是與裝置相關的資源範例：

-   [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush) 和繼承自它的介面。 使用呈現目標來建立筆刷。
-   [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer)。 使用呈現目標來建立圖層。
-   [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) 和繼承自它的介面。 若要建立轉譯目標，請使用 factory 或另一個呈現目標。

> [!Note]  
> 從 Windows 8 開始，有新的介面可建立裝置相依的資源。 如果從相同的 **ID2D1Device** 建立裝置內容和資源， [**ID2D1Device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device)和 [**ID2D1DeviceCoNtext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext)可以共用資源。

 

當相關聯的轉譯裝置變成無法使用時，裝置相依的資源就會變成無法使用。 這表示當您收到轉譯目標的 [**D2DERR \_ 重新建立 \_ 目標**](direct2d-error-codes.md) 錯誤時，必須重新建立轉譯目標及其所有資源。

## <a name="sharing-factory-resources"></a>共用 Factory 資源

您可以與所有其他資源分享所有與裝置無關的資源， (與裝置無關或由相同處理站建立的裝置相依) 。 例如，如果兩個 **ID2D1RenderTarget** 物件都是由相同的 factory 所建立，則您可以使用兩個 [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)物件來繪製相同的 [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) 。

接收介面 ([**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink)、 [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink)和 [**ID2D1TessellationSink**](/windows/win32/api/d2d1/nn-d2d1-id2d1tessellationsink)) 可與任何 factory 所建立的資源分享。 不同于 Direct2D 中的其他介面，可以使用任何接收介面的實作為。 例如，您可以使用自己的 **ID2D1SimplifiedGeometrySink** 執行。

## <a name="sharing-render-target-resources"></a>共用呈現目標資源

您共用轉譯目標所建立之資源的能力，取決於轉譯目標的種類。 當您建立型別 D2D1 轉譯目標 [**\_ \_ \_ 類型 \_ 預設值**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type)的轉譯目標時，該呈現目標所建立的資源只能由該轉譯目標 (使用，除非轉譯目標符合下列各節所述的其中一種類別) 。 發生這種情況是因為您不知道轉譯目標最後將使用的裝置，可能會導致轉譯至本機硬體、軟體或遠端用戶端的硬體。 例如，您可以撰寫一個程式，當它從遠端顯示時或轉譯目標的大小增加到轉譯硬體所支援的大小上限時，就會停止運作。

下列各節說明某個轉譯目標所建立的資源可與另一個轉譯目標共用的情況。

### <a name="hardware-render-targets"></a>硬體呈現目標

只要遠端模式相容，您就可以在任何明確使用硬體的轉譯目標之間共用資源。 只有當兩個轉譯目標使用 D2D1 轉譯目標使用方式 [**\_ \_ \_ \_ 強制 \_ 點陣圖 \_ 遠端處理**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_usage) 或 **D2D1 轉譯目標使用 \_ \_ \_ \_ GDI \_ 相容** 的使用旗標，或未指定任何旗標時，才保證遠端處理模式是相容的。 這些設定可保證資源一律會位於同一部電腦上。 若要指定使用模式，請使用一或多個 **D2D1 轉譯 \_ \_ 目標 \_ 使用** 方式旗標，設定用來建立轉譯目標之 [**D2D1 轉譯 \_ \_ 目標 \_ 屬性**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties)結構的 [**使用** 方式] 欄位。

若要建立明確使用硬體轉譯的呈現目標，請將您用來建立轉譯目標的 [**D2D1 轉譯 \_ \_ 目標 \_ 屬性**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties)結構的 [**類型**] 欄位設定為 [**D2D1 轉譯 \_ \_ 目標 \_ 類型 \_ 硬體**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type)。

### <a name="dxgi-surface-render-targets"></a>DXGI 介面呈現目標

您可以將 DXGI 介面轉譯目標所建立的資源，與使用相同基礎 Direct3D 裝置的任何其他 DXGI 介面呈現目標共用。

### <a name="compatible-render-targets-and-shared-bitmaps"></a>相容的呈現目標和共用點陣圖

您可以在轉譯目標和該呈現目標所建立的相容轉譯目標之間共用資源。 若要建立相容的呈現目標，請使用 [**ID2D1RenderTarget：： CreateCompatibleRenderTarget**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(id2d1bitmaprendertarget)) 方法。

您可以使用 [**ID2D1RenderTarget：： CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap) 方法建立可在方法呼叫所指定的兩個轉譯目標之間共用的 [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) （如果方法成功）。 只要兩個轉譯目標使用相同的基礎裝置來呈現，此方法就會成功。

 

 

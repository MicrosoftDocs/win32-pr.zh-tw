---
title: Direct2D Debug 圖層總覽
description: Direct2D Debug 圖層總覽
ms.assetid: 7c28e00b-ebb9-4b79-939c-64eade1351ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 833174e0d18b11e2384d838930d5508601cfceaf
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099986"
---
# <a name="direct2d-debug-layer-overview"></a>Direct2D Debug 圖層總覽

Direct2D debug 層提供設計階段的偵錯工具訊息，可讓您將執行時間應用程式失敗降至最低。 本總覽描述 Direct2D debug 層的基本概念。 它會假設您已熟悉如何建立基本 Direct2D 應用程式。

本總覽包含下列各節。

-   [什麼是 Direct2D Debug 層級](#what-is-the-direct2d-debug-layer)
-   [安裝 Direct2D Debug Layer](#installing-the-direct2d-debug-layer)
-   [啟用 Debug 圖層](#enabling-the-debug-layer)
-   [Debug 層級](#debug-levels)
-   [相關主題](#related-topics)

## <a name="what-is-the-direct2d-debug-layer"></a>什麼是 Direct2D Debug 層級

Direct2D debug 層會在其本身 DLL 中的 Direct2D （名為 d2d1debug.dll）分開執行，提供可讓您精確地使用 Direct2D 函式的調試訊息。 調試訊息通常是因為 API 合約違規所造成，例如不正確參數 (可能是 Direct3D 相關的) 、不正確資源、執行緒違規和效能問題，例如在剪輯足夠的情況下使用圖層。 若要指定 debug 層追蹤的資訊量，您可以指定下列三個調試層級的其中一個：資訊、警告和錯誤。和層級錯誤的訊息會觸發中斷點，以協助您進行調試。

## <a name="installing-the-direct2d-debug-layer"></a>安裝 Direct2D Debug Layer

如需有關安裝調試層的指示，請參閱 [安裝 Direct2D 調試層](installing-the-direct2d-debug-layer.md)。

## <a name="enabling-the-debug-layer"></a>啟用 Debug 圖層

若要在您的應用程式中啟用 debug 圖層，請在使用 [**D2D1CreateFactory**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory)函式建立處理站時，指定 **D2D1 \_ debug \_ level \_ NONE** 以外的 [**D2D1 \_ 調試層 \_ 級**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_debug_level)值。

> [!Note]  
> 如果已啟用 Direct2D debug 圖層，則在設定色彩內容時，Direct2D 色彩管理效果 (CLSID \_ D2D1ColorManagement) 可能會造成存取違規。 解決方法是在使用色彩管理效果時停用調試層

 

啟用 factory 的 debug 層也會啟用該處理站所建立之任何物件的偵錯工具資訊。

下列範例會在針對 DEBUG 組建設定編譯應用程式時，啟用 factory 的 debug 層。


```C++
        // If you set the options.debugLevel to D2D1_DEBUG_LEVEL_NONE,
        // the debug layer is not enabled.
#if defined(DEBUG) || defined(_DEBUG)
        D2D1_FACTORY_OPTIONS options;
        options.debugLevel = D2D1_DEBUG_LEVEL_INFORMATION;

        hr = D2D1CreateFactory(
            D2D1_FACTORY_TYPE_SINGLE_THREADED,
            options,
            &m_pD2DFactory
            );
#else
        hr = D2D1CreateFactory(
            D2D1_FACTORY_TYPE_SINGLE_THREADED,
            &m_pD2DFactory
            );
#endif
```



> [!Note]  
> 如果未指定任何 factory 選項，或指定了「無」的 debug 層級，則不會叫用 debug 層。 在應用程式的發行版本中，不應使用 debug 層。

 

下一節將說明 [**D2D1 \_ debug \_ 層級**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_debug_level) 列舉所定義的不同調試層級。

## <a name="debug-levels"></a>Debug 層級

[**D2D1 \_ debug \_ level**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_debug_level)列舉會指定三個 DEBUG 層級： D2D1 \_ debug \_ LEVEL \_ error (error) 、D2D1 \_ debug \_ level \_ warning (warning) 和 D2D1 \_ DEBUG \_ level \_ information (資訊) 。 這些層級的解讀方式如下：

-   **錯誤：** Direct2D 會將嚴重的錯誤訊息傳送至 debug 層。 例如，中斷線程條件約束將會產生嚴重的錯誤。

-   **警告：** Direct2D 會將錯誤訊息和警告傳送至 debug 圖層，以便您可以處理這些訊息。

-   **資訊：** Direct2D 會將錯誤訊息、警告和其他診斷資訊傳送至 debug 圖層。 例如，效能改進訊息將會在這個 debug 層級傳送。

值 D2D1 \_ DEBUG \_ LEVEL \_ none (None) 表示 Direct2D 不提供任何偵錯工具輸出。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Debug 訊息](direct2ddebuglayer-debugmessages.md)
</dt> </dl>

 

 





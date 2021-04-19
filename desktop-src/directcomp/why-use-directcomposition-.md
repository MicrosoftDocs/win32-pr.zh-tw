---
title: 為何要使用 DirectComposition
description: 本主題說明 Microsoft DirectComposition 的功能和優點。
ms.assetid: D597E737-24A1-49E9-8861-9DDD6D7FF2F8
keywords:
- 為何要使用 DirectComposition
- 使用 DirectComposition 的原因
- DirectComposition 功能和優點
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7ad68f779abc023b7645ed9e66f8af3bf63a140
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106965252"
---
# <a name="why-use-directcomposition"></a>為何要使用 DirectComposition？

> [!NOTE]
> 針對 Windows 10 上的應用程式，我們建議使用 DirectComposition，而不是使用。 如需詳細資訊，請參閱 [使用視覺分層將您的桌面應用程式現代化](/windows/uwp/composition/visual-layer-in-desktop-apps)。

本主題說明 Microsoft DirectComposition 的功能和優點。 它包含下列區段：

-   [建立視覺效果吸引人的使用者介面](#create-a-visually-engaging-user-interface)
-   [為您的應用程式啟用豐富且流暢的動畫](#enable-rich-smooth-animations-for-your-application)
-   [結合各種來源的點陣圖](#combine-bitmaps-from-a-variety-of-sources)
-   [透過與 DWM 整合來節省記憶體](#memory-savings-though-integration-with-dwm)
-   [保留您現有的內容](#keep-what-you-already-have)
-   [相關主題](#related-topics)

## <a name="create-a-visually-engaging-user-interface"></a>建立視覺效果吸引人的使用者介面

DirectComposition 可讓您結合和製作 [*視覺效果*](directcomposition-glossary.md) ，為您的 Windows 應用程式建立視覺互動的 UI。 它可協助讓您的應用程式具有獨特的外觀和風格，以建立與其他應用程式分開設定的身分識別。

DirectComposition 也可以讓您的應用程式更容易使用。 例如，您可使用視覺層來建立視覺提示和動畫螢幕轉換，而後者可顯示螢幕上項目之間的關聯性。

## <a name="enable-rich-smooth-animations-for-your-application"></a>為您的應用程式啟用豐富且流暢的動畫

DirectComposition 是一種高效能點陣圖組合引擎，其使用硬體加速圖形來達到高畫面播放速率，以平滑且一致地移動、滾動和複雜內容的動畫。 因為它的運作方式與用來呈現應用程式 UI 的執行緒不同，所以 DirectComposition 絕對不能「使」 UI 執行緒，也不會干擾應用程式繪製其 UI 元素的能力。

## <a name="combine-bitmaps-from-a-variety-of-sources"></a>結合各種來源的點陣圖

許多以 Windows 為基礎的應用程式都有一個由各種不同圖形架構所建立的元素所組成的 UI。 例如，應用程式可能會使用 Windows Forms 來建立狀態列、Windows 圖形裝置介面 (GDI) 來建立主視窗內容、Microsoft DirectX for Graphics 內容等等。 DirectComposition 可讓您結合各種圖形架構的內容，並將其轉譯為相同的最上層或子視窗，而不需要擔心來自不同 framework 的內容重迭時，會發生什麼事。

## <a name="memory-savings-though-integration-with-dwm"></a>透過與 DWM 整合來節省記憶體

DirectComposition 所建立的組合和動畫會傳遞至 Windows 的內建元件，稱為 [桌面視窗管理員 (DWM) ](/windows/desktop/dwm/dwm-overview) 以轉譯至螢幕。 因此，電腦上不需要任何特殊的呈現元件或 UI 架構。

## <a name="keep-what-you-already-have"></a>保留您現有的內容

以 Windows 為基礎的現有應用程式中的 UI 程式碼代表大量投資。 在大部分的情況下，DirectComposition 可讓您撰寫現有的 UI 內容，並製作其動畫。 這表示您可以使用 DirectComposition 對您的應用程式 UI 進行重大更新和增強，而不需要對現有的 UI 程式碼基底進行大量變更。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectComposition](directcomposition-portal.md)
</dt> </dl>

 

 
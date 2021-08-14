---
title: " (Windows 控制項的新功能) "
description: 本主題說明 Windows 8 與舊版 Windows 之間的主題和視覺化樣式的支援差異。
ms.assetid: 866C2E0B-D3AF-4DA0-8B45-D5FF1335C350
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d7801eea011aabb05663cc2e29f18e0dd58edc9fddc4f32014fcffb96c559cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957547"
---
# <a name="whats-new-windows-controls"></a> (Windows 控制項的新功能) 

本主題說明 Windows 8 與舊版 Windows 之間的主題和視覺化樣式的支援差異。

## <a name="through-windows-7"></a>到 Windows 7

透過 Windows 7，視覺效果樣式預設為開啟，但使用者可以選取 Windows 傳統主題或關閉主題服務，將其關閉。 當視覺化樣式關閉時，所有 UI 都會取得傳統外觀，且大部分的視覺效果樣式 Api 都無法使用。 已透過 Windows 7 保留視覺化樣式的模式，以支援各種高對比主題，以及 Windows 傳統主題。 如果您想要在相同的應用程式中同時支援視覺效果樣式和高對比主題，通常需要維護兩個不同的程式碼路徑來呈現控制項。

## <a name="windows-8-and-later"></a>Windows 8 和更新版本

在 Windows 8 中，無法透過 **PC 設定****的個人化頁面或** 關閉主題服務來關閉視覺效果樣式。 Windows傳統模式已不存在，而且已修改高對比模式來使用視覺化樣式。 因為這些變更，所以僅以 Windows 8 為目標的應用程式不再需要兩個不同的程式碼路徑來支援視覺效果樣式和高對比主題。

Windows 8 中的視覺化樣式包括 Windows 傳統主題模式的回溯相容性支援。 任何適用于舊版的 UI 轉譯程式碼將繼續在 Windows 8 上運作，而不需要修改。

在 Windows 8 中，如果您想要讓應用程式支援以視覺化樣式為基礎的高對比主題，您必須在應用程式資訊清單的 [相容性] 區段中包含 Windows 8 GUID。 否則，系統會假設應用程式是針對先前的版本所設計，並藉由模擬 Windows 傳統高對比主題來呈現工作區。 如需詳細資訊，請參閱 [支援高對比主題](supporting-high-contrast-themes.md)。

如同舊版，Windows 8 支援第5版和第6版的通用控制項，預設值為5。 因為只有第6版支援視覺化樣式，所以如果您想要將視覺化樣式套用至應用程式工作區中的通用控制項，則必須在應用程式資訊清單中指定第6版。 如需詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[啟用視覺化樣式](cookbook-overview.md)
</dt> <dt>

[支援高對比主題](supporting-high-contrast-themes.md)
</dt> <dt>

[視覺化樣式](themes-overview.md)
</dt> <dt>

[視覺化樣式總覽](visual-styles-overview.md)
</dt> </dl>

 

 





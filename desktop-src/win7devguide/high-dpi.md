---
title: 高 DPI
description: .
ms.assetid: 476fe65c-2acd-4a7a-8a76-72d9f010b772
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adad7c986c7083ab2327f0c8de0bd2cace5ef20a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023880"
---
# <a name="high-dpi"></a>高 DPI

隨著顯示器技術的進展，製造商增加了其顯示所支援的圖元數目。 雖然文字、影像和使用者介面專案在高解析度顯示器上看起來很清楚且更容易閱讀，但是作業系統必須擴大以支援視覺效果。否則，一切看起來都比較小。

Windows 7 支援高 *DPI* 顯示。 市場資料建議，高 *DPI* 畫面的部署 (120-144 點（每英寸） (DPI) ) 將在 Windows 7 時間範圍內增加。 在這些畫面上執行原生解析度時，許多應用程式會顯得非常小，除非它們使用 *高 DPI*。 某些應用程式 (例如 Windows Internet Explorer) 具有可讓使用者放大和縮小的字型調整功能，但許多應用程式都不提供。 Windows 7 中的 *高 DPI* 功能：

-   確保 Windows 和應用程式體驗在標準硬體上是最佳的， (*DPI* 設定已優化，可符合硬體) 的功能。
-   讓 Windows Shell 和其他以 Windows 為基礎的應用程式看起來更適合使用不同的 *DPI* 設定。
-   遵循預設 *DPI* 設定，以硬體規格和功能為基礎。
-   可讓使用者個人化 *DPI* 設定，而不需要重新開機。
-   確保畫面一律設為原生解析度。

Windows *DPI* 縮放比例功能可調整字型和使用者介面專案 (例如，依計算百分比) 的按鈕、圖示和輸入欄位，如 *DPI* 設定所指定。 這與顯示解析度降低時所發生的調整不同。 在 *DPI* 調整的情況下，Windows 會提供以更多圖元繪製的字型和使用者介面專案，從而產生更大、更高的精確度，以及更清晰的 Windows 體驗。 協力廠商 Windows 應用程式可以利用 *高 DPI* 設定，並據此調整使用者介面，方法是宣告自己的 *DPI* 感知。 應用程式開發人員應該不會再假設 96 DPI 是適用于所有應用程式的理想解決方案。

如需 *高 DPI* 及撰寫 *高 DPI* 感知應用程式的詳細資訊，請參閱 [高 DPI](../hidpi/high-dpi-desktop-application-development-on-windows.md)。

 

 
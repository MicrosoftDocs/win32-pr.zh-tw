---
title: 高 DPI
description: 高 DPI
ms.assetid: 476fe65c-2acd-4a7a-8a76-72d9f010b772
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5006d5bdf1c9e90745ef8e3571e64e729dbf5dff54338280789f39c6d0027e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118203959"
---
# <a name="high-dpi"></a>高 DPI

隨著顯示器技術的進展，製造商增加了其顯示所支援的圖元數目。 雖然文字、影像和使用者介面專案在高解析度顯示器上看起來很清楚且更容易閱讀，但是作業系統必須擴大以支援視覺效果。否則，一切看起來都比較小。

Windows 7 支援高 *DPI* 顯示。 市場資料建議，高 *DPI* 畫面的部署 (120-144 點（每英寸） (DPI) ) 將會在 Windows 7 個時間範圍內增加。 在這些畫面上執行原生解析度時，許多應用程式會顯得非常小，除非它們使用 *高 DPI*。 某些應用程式 (例如 Windows Internet Explorer) 具有可讓使用者放大和縮小的字型調整功能，但許多應用程式都沒有。 Windows 7 中的 *高 DPI* 功能：

-   確保 Windows 和應用程式體驗在標準硬體上是最佳的， (*DPI* 設定已優化，以符合硬體) 的功能。
-   讓 Windows Shell 和其他以 Windows 為基礎的應用程式在使用不同的 *DPI* 設定時更美觀。
-   遵循預設 *DPI* 設定，以硬體規格和功能為基礎。
-   可讓使用者個人化 *DPI* 設定，而不需要重新開機。
-   確保畫面一律設為原生解析度。

Windows *DPI* 縮放比例功能可調整字型和使用者介面元素 (例如，依計算百分比) 的按鈕、圖示和輸入欄位，如 *DPI* 設定所指定。 這與顯示解析度降低時所發生的調整不同。 在 *DPI* 縮放的情況下，Windows 提供以更多圖元繪製的字型和使用者介面專案，進而大幅提高精確度，並讓 Windows 體驗更清晰。 協力廠商 Windows 的應用程式可以利用 *高 DPI* 設定，並據此調整使用者介面，其方式是宣告自己的 *高 DPI* 感知。 應用程式開發人員應該不會再假設 96 DPI 是適用于所有應用程式的理想解決方案。

如需 *高 DPI* 及撰寫 *高 DPI* 感知應用程式的詳細資訊，請參閱 [高 DPI](../hidpi/high-dpi-desktop-application-development-on-windows.md)。

 

 

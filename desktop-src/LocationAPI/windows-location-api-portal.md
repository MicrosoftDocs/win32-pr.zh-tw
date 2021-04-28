---
description: 位置 API
ms.assetid: 0182461a-df06-46ea-a9c2-7aedbde5033b
title: 位置 API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3e9dccf5f88da1c608cfbc03898899f171a2627
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110886"
---
# <a name="location-api"></a>位置 API

\[Win32 位置 API，並可在 [需求] 區段中指定的作業系統中使用。 它在後續版本中可能會變更或無法使用。 相反地，請使用 [**Windows. 地理位置**](/uwp/api/Windows.Devices.Geolocation) API。 若要從網站存取位置，請使用 [W3C 地理位置 API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85))。 \]

## <a name="purpose"></a>目的

現今的電腦比以往更容易移動。 從小型膝上型電腦到 Tablet Pc，許多電腦都可以在使用者想要前往的任何地方進行。 利用電腦行動性的程式，可為人們的生活帶來顯著的價值。 例如，可以找到附近餐廳的程式，以及提供駕駛方向，似乎是可攜式電腦的自然擬合。 但是，雖然用來判斷使用者目前位置的技術是常見且經濟實惠的，但在這項技術上建立解決方案可能是一項艱巨的工作。

若要建立位置感知程式，您可能需要克服各種問題，包括：

-   全球定位系統 (GPS) 使用虛擬 COM 埠的裝置，這一次只提供一個程式的存取權。
-   瞭解和程式設計通訊協定，例如全國航海電子產品協會 (NMEA) 規格，以及專屬廠商延伸模組。
-   受限於已知、垂直硬體解決方案的程式設計。
-   執行邏輯以處理不同位置提供者之間的轉換，例如 GPS 接收器、連線的網路、行動電話通訊網路、網際網路和使用者設定。

本檔說明 (API) 的 Windows 位置應用程式設計介面。 位置 API 可提供一種標準方式來取得使用者位置的相關資料，並將位置資料包表的格式標準化，有助於簡化定位感知程式設計。 位置 API 會自動處理位置資料提供者之間的轉換，而且一律會為目前的情況選擇最準確的提供者。

## <a name="developer-audience"></a>開發人員對象

位置 API 會透過一組 COM 介面提供其功能。 您可以透過 c + + 程式設計語言，或在指令碼語言（如 Microsoft JScript）中使用 COM 物件的程式設計人員，使用位置 API 功能。

## <a name="in-this-section"></a>本節內容

-   [位置 API c + + 程式設計參考](windows-location-programming-reference.md)
-   [位置 API 物件模型參考](windows-location-script-programming-reference.md)

 

 

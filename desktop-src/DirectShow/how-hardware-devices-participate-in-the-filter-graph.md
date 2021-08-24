---
description: 硬體裝置如何參與篩選 Graph
ms.assetid: 27e1c097-9bb4-4f9c-b9f9-0d4225c0d290
title: 硬體裝置如何參與篩選 Graph
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b3b2940b6c434459d1213dd0f4265f4d9250e548ede7f2509f7f68c27166861
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119389158"
---
# <a name="how-hardware-devices-participate-in-the-filter-graph"></a>硬體裝置如何參與篩選 Graph

本文說明 DirectShow 如何與音訊和影片硬體互動。

**包裝函式篩選**

所有 DirectShow 濾波器都是使用者模式的軟體元件。 為了讓核心模式硬體裝置（例如，視頻捕捉卡）聯結 DirectShow 的篩選圖形，裝置必須以使用者模式篩選表示。 此函式是由 DirectShow 提供的特製化「包裝函式」篩選所執行。 這些篩選器包括 [音訊捕獲](audio-capture.md) 篩選器、 [VFW Capture](vfw-capture-filter.md) 篩選器、 [電視調諧器](tv-tuner-filter.md) 篩選器、 [電視音訊](tv-audio-filter.md) 篩選器，以及 [類比視頻縱橫](analog-video-crossbar-filter.md) 比對。 DirectShow 也會提供一個稱為 KsProxy 的篩選器，其可代表任何類型的 Windows Driver Model (WDM) 串流裝置。 硬體廠商可提供 *KsProxy 外掛程式*（由 KsProxy 匯總的 COM 物件），藉此擴充 KsProxy 以支援自訂功能。

包裝函式篩選會公開代表裝置功能的 COM 介面。 應用程式會使用這些介面，在篩選準則之間傳遞資訊。 篩選準則會將 COM 方法呼叫轉譯為設備磁碟機呼叫、以核心模式將該資訊傳遞至驅動程式，然後將結果轉譯回應用程式。 電視調諧器、電視音訊、類比視頻縱橫比對和 KsProxy 濾波器透過 [**IKsPropertySet**](ikspropertyset.md) 介面支援自訂驅動程式屬性。 VFW Capture 篩選器和音訊捕獲篩選器無法以這種方式擴充。

針對應用程式開發人員，包裝函式篩選器可讓應用程式控制裝置，就像控制任何其他 DirectShow 濾波器一樣。 不需要進行任何特殊的程式設計;與核心模式裝置通訊的詳細資料會封裝在篩選器中。

**Windows 裝置的影片**

VFW Capture 篩選器針對 Windows (VFW) Capture 卡支援較早的影片。 當目標系統上有 VfW 卡時，您可以使用 DirectShow[系統裝置列舉](system-device-enumerator.md)值，探索並將它新增至篩選圖形。 如需詳細資訊，請參閱 [列舉裝置和篩選器](enumerating-devices-and-filters.md)。

**音訊捕捉和混合裝置 (音效卡)**

較新的音效卡具有麥克風和其他類型裝置的輸入插孔。 這些卡片通常也有現成的混合功能，可控制每個個別輸入的音量、高音和低音。 在 DirectShow 中，音訊捕獲篩選器會包裝音效卡的輸入和混音器。 每張音效卡都可以使用系統裝置列舉值來探索。 若要查看系統中的音效卡，請執行 GraphEdit，然後從 [音訊捕獲來源] 類別中選取。 該類別中的每個篩選器都是音訊捕獲篩選準則的個別實例。  (參閱 [使用 GraphEdit](using-graphedit.md)。 ) 

**WDM 串流裝置**

較新的硬體解碼器和捕捉卡符合 Windows Driver Model (WDM) 規格。 這些裝置的功能比 VfW 裝置更大。 WDM 視頻捕捉卡可支援 VfW 下未提供的功能，包括取得格式的列舉、以程式設計方式控制影片參數，例如色調和亮度、程式設計輸入選擇，以及 TV 調諧器支援。

為了支援 WDM 串流裝置，DirectShow 提供 (ksproxy.ax) 的 KsProxy 篩選器。 KsProxy 已被稱為「瑞士軍隊刀篩選」，因為它有許多不同的專案。 篩選器上的釘選數目，以及篩選器所公開的 COM 介面數目，取決於基礎驅動程式的功能。 KsProxy 不會出現在篩選圖形的 "KsProxy" 名稱下方。 它一律會採用在登錄中找到之裝置的易記名稱。 若要查看您系統上的 WDM 裝置，請執行 GraphEdit，然後從 WDM 串流類別目錄中選取。 即使您的系統上只有一個 WDM 卡，該卡片可能包含多個裝置。 每個裝置都會以個別的篩選表示，而這些篩選器會實際 KsProxy。

應用程式會使用系統裝置列舉值，在系統上尋找 WDM 裝置的名字標記。 KsProxy 是藉由在標記上呼叫 **BindToObject** 來具現化。 由於 KsProxy 可代表所有種類的 WDM 裝置，因此它必須查詢驅動程式來判斷驅動程式支援的屬性集。 屬性集是由 WDM 驅動程式所使用的資料結構集合，也是由某些使用者模式篩選器所使用，例如 MPEG 2 軟體的解碼器。 KsProxy 會自行設定，以公開對應至這些屬性集的 COM 介面。 KsProxy 會將 COM 方法呼叫轉譯為屬性集，並將這些呼叫傳送至驅動程式。 硬體廠商可以藉由提供外掛程式來擴充 KsProxy，這是可公開裝置特殊功能的廠商特定介面。 這些詳細資料會在應用程式中隱藏。 應用程式會以 KsProxy 的方式來控制裝置，就像任何其他 DirectShow 濾波器一樣。

**核心串流**

WDM 裝置支援核心串流，其中的資料會完全以核心模式串流處理，而不會切換至使用者模式。 在核心模式和使用者模式之間切換需要耗費大量的計算成本;核心串流允許高位費率，而不會讓主機 CPU 負擔。 以 WDM 為基礎的篩選器可以使用核心串流，直接從一個硬體裝置將多媒體資料傳遞到另一個硬體裝置，不論是在相同的卡片或不同的卡片上，不需要將資料複製到系統的主要記憶體中。

從應用程式的觀點來看，它看起來就像是資料從某個使用者模式篩選移到下一個。 在現實情況下，資料可能永遠不會傳入使用者模式，而是會直接從某個核心模式裝置串流至另一個，直到它在視頻圖形配接器上轉譯為止。 某些案例（例如 capture 至檔案）要求資料在某個時間點從核心模式傳遞到使用者模式。 不過，此參數不一定需要將資料複製到記憶體中的新位置。

應用程式開發人員通常不需要擔心核心資料流程的詳細資料，但背景資訊除外。 如需有關 WDM、核心串流、KsProxy 和相關主題的詳細資訊，請參閱 Microsoft DDK。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[篩選 Graph 及其元件](the-filter-graph-and-its-components.md)
</dt> </dl>

 

 




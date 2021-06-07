---
description: Windows 映像取得 (WIA) 是 Windows 系列作業系統的靜止映射取得平臺，從 Windows Millennium Edition (Windows Me) 和 Windows XP 起。
ms.assetid: 8f32422e-25ec-48bc-9d79-57dbb3b53e93
title: Windows Image Acquisition (WIA)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 664b5accaa1312eae3baf6161e41c9c65e718c69
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443089"
---
# <a name="windows-image-acquisition-wia"></a>Windows Image Acquisition (WIA)

Windows 映像取得 (WIA) 是 Windows 系列作業系統的靜止映射取得平臺，從 Windows Millennium Edition (Windows Me) 和 Windows XP 起。

-   [簡介](#introduction)
-   [Windows 映像收購2.0 的優點](#benefits-of-windows-image-acquisition-20)
    -   [針對應用程式寫入器](#for-application-writers)
    -   [針對裝置製造商](#for-device-manufactures)
    -   [針對掃描器使用者](#for-scanner-users)
-   [開發 Windows 映像](#development-of-windows-image-acquisition)
-   [Windows 映像取得簡介](#overview-of-windows-image-acquisition)
-   [Windows 映像取得2.0 的相關事實](#facts-about-windows-image-acquisition-20)
-   [開發人員物件](#developer-audience)
-   [執行時間需求](#run-time-requirements)
-   [WIA 主題](#wia-topics)

## <a name="introduction"></a>簡介

WIA 平臺可讓影像處理/圖形應用程式與映射處理硬體互動，並將不同應用程式和掃描器之間的互動標準化。 這可讓那些不同的應用程式與這些不同的掃描器交談並進行互動，而不需要應用程式撰寫者和掃描器製造人員針對每個應用程式裝置組合自訂其應用程式或驅動程式。

![圖形顯示在影像處理應用程式和裝置之間，以雙向層呈現的 wia 基本架構。 ](images/wia-diagram1.png)

## <a name="benefits-of-windows-image-acquisition-20"></a>Windows 映像收購2.0 的優點

WIA 可提供應用程式開發人員、裝置製造商以及需要與映射處理硬體互動之掃描器使用者的優點。

### <a name="for-application-writers"></a>針對應用程式寫入器

-   Windows 會執行 WIA 驅動程式的認證程式，因此 WIA 應用程式保證會與所有以 WIA 為基礎的掃描程式相容。
-   Wia 驅動程式是在 WIA 服務進程中載入，因此可提供更穩定的驅動程式環境。
-   您可以透過 WIA 子系統所支援的推送事件，從掃描器掃描按鈕起始應用程式。
-   WIA 包含所有驅動程式都可利用的預設分割篩選;如此一來，應用程式就不需要撰寫程式碼來進行多重區域掃描，例如將大量相片分散到平台掃描器。

### <a name="for-device-manufactures"></a>針對裝置製造商

-   WIA 驅動程式認證程式可協助驅動程式開發人員建立其驅動程式符合 WIA 規範。
-   WIA 驅動程式可利用內建的分割篩選器、影像處理篩選和錯誤處理常式（如果選擇這樣做）。
-   以 WIA 為基礎的掃描器可以立即在 Windows 上使用 Windows 掃描應用程式（例如 Windows 傳真和掃描和油漆）來運作。
-   WIA 驅動程式提供更好的 Windows 整合，例如完整的裝置體驗。
-   Windows Vista 版本包含一個 WSD WIA 類別驅動程式，可讓所有與 Web Service for 掃描器相容的裝置 (WS-掃描) 通訊協定，以在沒有任何額外的驅動程式或軟體的情況下使用 WIA 應用程式。

### <a name="for-scanner-users"></a>針對掃描器使用者

-   您可以從 Windows 應用程式（例如 Windows 傳真和掃描和油漆）使用 WIA 型掃描器，而不需要任何額外的軟體。
-   以 WIA 為基礎的應用程式和掃描器也可以利用 WIA 附加元件（例如分割篩選器）來處理掃描器上的一些圖片，並在不需要使用者介入的情況下，將它們全部掃描到個別檔案。
-   WIA 型裝置提供與其他 Windows 功能（例如 Windows 7 的 Device Stage 功能）更好的整合。
-   WIA 藉由隔離驅動程式和應用程式，提供更強大、穩定且可靠的掃描體驗。

## <a name="development-of-windows-image-acquisition"></a>開發 Windows 映像

Windows 2000 和 Windows 95 或更新版本中的映射架構是由低層級的硬體抽象概念、映射架構 (STI) ，以及一組高階的 Api （稱為 TWAIN）所組成。 Windows XP 和 Windows Me 的 WIA 都是引進的。 WIA 是以 STI 為基礎的映射架構，但不需要 TWAIN，雖然您仍然支援 TWAIN 和 WIA。

WIA 1.0 是在 Windows Me 和 Windows XP 中引進，並支援掃描器、數位攝影機和數位視訊設備。 WIA 2.0 已與 Windows Vista 一起發行。 WIA 2.0 的目標物件是掃描器，但繼續透過 wia 1.0 至 wia 服務所提供的 WIA 2.0 相容性層，提供舊版 WIA 1.0 應用程式和裝置的支援。 不過，已從 Windows Vista 的 WIA 移除影片內容支援。 我們建議 Windows 可攜式裝置 (WPD) API 用於數位攝影機和數位視訊設備。 除了原生 WIA 2.0 設備磁碟機和映射應用程式，在 Windows Vista 和 Windows 7 上仍會直接支援 WIA 1.0 和 STI TWAIN 驅動程式。

## <a name="overview-of-windows-image-acquisition"></a>Windows 映像取得簡介

WIA 提供的架構可讓裝置為作業系統提供獨特的功能，並可讓映射應用程式叫用這些獨特的功能。

WIA 平臺包含資料取得通訊協定、設備磁碟機模型和介面 (的 DDI) 、API 和專用的 WIA 服務。 此平臺也包含一組內建的核心模式驅動程式，可支援在本機透過 USB、串列/平行、SCSI 和 FireWire 介面連線的映射裝置進行通訊。 WIA 子系統也包含透明相容性層，可讓 TWAIN 相容的應用程式採用並使用以 WIA 驅動程式為基礎的裝置。

您也可以透過隨附于 Windows Vista 的 WSD WIA 類別驅動程式，從 Windows Vista 和 Windows 7 上的 WIA 相容映射應用程式，使用支援裝置 (WSD) 通訊協定的網路連線映射裝置。 類別驅動程式會將 WIA 呼叫轉換為 WSD 呼叫，反之亦然，並讓現有的 WIA 應用程式能在沒有任何額外驅動程式的情況下，使用以 WSD 為基礎的掃描器。

WIA 驅動程式是由使用者介面所組成 (UI) 元件和核心驅動程式元件，載入至兩個不同的進程空間：應用程式空間中的 UI 和 WIA 服務空間中的驅動程式核心。 此服務會在 Windows XP 的本機系統內容中執行，並在從 Windows Server 2003 和 Windows Vista 開始的本機服務內容中執行，以增強安全性免于發生錯誤或惡意的驅動程式。

![圖形顯示 wia 的架構，以及它如何以服務的方式運作。](images/wia-arch.png)

WIA API 集會提供下列支援，藉此將影像應用程式公開給仍能取得映射的硬體功能：

-   列舉可用的映射取得裝置。
-   同時建立多個裝置的連接。
-   以標準且可擴充的方式查詢裝置屬性。
-   使用標準和高效能傳輸機制來取得裝置資料。
-   維護資料傳輸之間的影像屬性。
-   裝置狀態和掃描事件處理的通知。

Windows 將腳本支援新增至 WIA，方法是在2002中發行已併入 windows Vista 的 WIA Automation 程式庫做為 Windows 映像取得 (WIA) Automation 層，並繼續成為 Windows 7 的一部分。 WIA Automation 程式庫為啟用自動化的應用程式開發環境和程式設計語言（例如 Microsoft Visual Basic 6.0、Active Server Pages (ASP) 、VBScript 和 C）提供端對端映射取得功能 \# 。

針對 Windows 7，WIA Api 提供額外的支援來補充已存在的推播掃描支援。

-   自動設定裝置起始掃描裝置前端面板上掃描器設定的掃描參數。
-   自動來源選取裝置起始的掃描。

## <a name="facts-about-windows-image-acquisition-20"></a>Windows 映像取得2.0 的相關事實

-   WIA 2.0 中的資料傳輸機制是以資料流程為基礎。 資料流程抽象會移除不同傳輸類型之間的差異，也允許在裝置與應用程式之間交換相互同意的中繼資料。
-   WIA 2.0 子系統也包含基本的影像處理篩選器驅動程式附加元件，如果驅動程式選擇提供自訂的影像處理篩選器，則可選擇性地取代掃描器驅動程式。 內建篩選器可讓您處理透過掃描器取得的影像。 當調整亮度和對比等小型設定時，影像處理篩選也會啟用即時軟體預覽。
-   分割篩選是另一個方便使用的 WIA 元件，可由掃描器驅動程式以更自訂的篩選來取代。 分割篩選可以用於多重區域掃描。 例如，多重區域掃描可讓應用程式在不需要使用者介入的情況下，自動偵測不同的掃描區域，例如識別掃描器平板上隨機拍攝的大量相片。
-   WIA 2.0 提供可取代/可延伸的錯誤處理常式，可正常處理並可能從軟體、硬體和設定錯誤和延遲中復原。 錯誤處理常式是另一個 WIA 元件，可由掃描器驅動程式以更自訂的版本取代。 此延伸模組會在資料的取得期間提供狀態和錯誤訊息，例如「燈泡準備」、「說明開啟」、「紙紙」等等。 此延伸模組也可讓您更清楚支援「取消作業」。

## <a name="developer-audience"></a>開發人員讀者

WIA API 是設計來供 C/c + + 程式設計人員使用。 需要熟悉 Windows GUI 和元件物件模型 (COM) 介面。

針對熟悉 Microsoft Visual Basic 6.0、Active Server Pages (ASP) 或腳本處理的開發人員，WIA 提供適用于 Windows XP Service Pack 1 (SP1) 或更新版本的自動化層，其建立依據和簡化 C/c + + 所提供之基礎的存取。 如需自動化層的詳細資訊，請參閱 [Windows 映像取得自動化層](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage)。

> [!Note]  
> WIA 自動化層取代 Windows 映像取得 (WIA) 1.0 腳本。

 

## <a name="run-time-requirements"></a>執行階段需求

使用 WIA API 的應用程式需要 Windows XP 或更新版本。

## <a name="wia-topics"></a>WIA 主題

WIA 主題的組織方式如下表所示。



|  主題                                                                                                                            | 描述                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [關於 Windows 映像取得](-wia-about-windows-image-acquisition.md)                                                  | 關於 WIA 的一般資訊                                                                     |
| [Windows 映像取得驅動程式](/windows-hardware/drivers/image/windows-image-acquisition-drivers)                  | WIA 驅動程式開發                                                                            |
| [Windows 映像取得自動化層](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage) | WIA 自動化層                                                                              |
| [WIA 教學課程](-wia-wia-tutorial.md)                                                                                        | 軟體發展工具組中包含的程式碼逐步解說 (SDK) ，其著重于特定工作 |
| [參考](-wia-reference.md)                                                                                              | 有關在 C/c + + 和腳本中使用的 WIA 介面、方法、物件和資料類型的資訊。      |



 

 

 

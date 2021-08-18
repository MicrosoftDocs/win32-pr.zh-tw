---
description: Windows 7 作業系統提供感應器裝置的內建支援。
ms.assetid: 751ba2fc-fbff-4418-82ac-eebc8a145b14
title: Windows 感應器和位置平台的總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc4847d6d6137b91ce577cfce0dbc54cc8c6e19430e1318eaff145c24ce493af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118889725"
---
# <a name="overview-of-the-windows-sensor-and-location-platform"></a>Windows 感應器和位置平台的總覽

Windows 7 作業系統提供感應器裝置的內建支援。 這包括支援定位感應器，例如 GPS 裝置。 作為這項支援的一部分，Windows 感應器和位置平台提供了一種標準方式，讓裝置製造商向軟體發展人員和取用者公開感應器裝置。 同時，平臺會為開發人員提供標準化的 API 和設備磁碟機介面， (的 DDI) 來處理感應器和感應器資料。

## <a name="about-sensor-devices"></a>關於感應器裝置

感應器有許多設定，從某種觀點來看，幾乎任何提供實體現象相關資料的資訊都可以稱為感應器。 雖然我們通常會將感應器視為硬體裝置，但是邏輯感應器也可以透過模擬軟體或固件中的感應器功能來提供資訊。 此外，單一硬體裝置也可以包含多個感應器。

Windows 感應器和位置平台會將感應器組織成類別，其代表各種不同的感應器裝置 *類別*，而 *類型* 則代表特定類型的感應器。 例如，影片遊戲控制器中的感應器偵測播放程式手的位置和移動 (或許是保齡球遊戲的影片) 會分類為方向感應器，但其類型會是立體加速計。 在程式碼中，Windows 會使用全域唯一識別碼 (guid) 來表示分類和類型，其中許多都是預先定義的。 裝置製造商可以在必要時定義和發佈新的 Guid，藉以建立新的類別和類型。

位置裝置組成一個特別有趣的類別。 目前，大部分的人都熟悉全球定位系統 (GPS) 。 在 Windows 中，GPS 感應器是 Location 類別的一部分。 位置分類可能包含其他感應器類型。 其中有些感應器類型是以軟體為基礎，例如根據網際網路位址提供位置資訊的 IP 解析程式、根據附近的塔來決定位置的行動電話塔 triangulator，或從連線的無線網路中樞讀取位置資訊的 Wi-Fi 網路位置提供者。

## <a name="about-the-platform"></a>關於平臺

Windows 感應器和位置平台是由下列開發人員和使用者元件所組成：

-   DDI 可讓 Windows 為感應器裝置提供標準的方法，以連接到電腦並提供資料給其他子系統。
-   Windows 感應器 API 會提供一組方法、屬性和事件，以搭配連線的感應器和感應器資料使用。
-   Windows 位置 API （以 Windows 感應器 API 為基礎）會提供一組程式設計物件，包括腳本物件，以使用位置資訊。
-   定位和其他感應器主控台可讓電腦系統管理員設定每位使用者的感應器，包括定位感應器。

下列各節將說明每個元件。

## <a name="architecture-diagram"></a>架構圖

下圖顯示元件之間的關聯性。

![感應器和位置平臺圖表](images/platformarchitecture.png)

## <a name="device-driver-interface"></a>設備磁碟機介面

感應器製造商可以建立設備磁碟機以連接具有 Windows 7 的感應器。 感應器設備磁碟機是使用 Windows 的可攜式裝置 (WPD) 驅動程式模型來執行，這是以 Windows 使用者模式驅動程式架構 (的驅動程式模型為基礎。許多設備磁碟機都是使用這些架構來撰寫的。 因為已建立這些技術，所以有經驗的設備磁碟機程式設計人員會發現將感應器驅動程式寫成熟悉的工作。 感應器 DDI 會使用特定的 UMDF 和 WPD 資料類型和介面，也會定義需要的感應器特定 WPD 命令和參數。 如需有關建立感應器設備磁碟機的詳細資訊，請參閱 Windows 驅動程式套件。

## <a name="sensor-api"></a>感應器 API

感應器 API 可讓 c + + 開發人員使用一組 COM 介面建立以感應器為基礎的程式。 API 會定義介面來執行常見的感應器程式設計工作，包括依類別、類型或識別碼管理感應器、管理感應器事件、使用個別感應器和感應器集合，以及使用感應器資料。 Windows SDK 包括標頭檔、檔、範例和工具，協助引導軟體發展人員如何在 Windows 程式中使用感應器。 本檔說明感應器 API。

## <a name="location-api"></a>位置 API

位置 API 建基於感應器 API，可讓您輕鬆地取出地理位置的相關資料，同時保護使用者隱私權。 位置 API 會透過一組代表物件的 COM 介面提供其功能。 這些物件可供瞭解如何透過 c + + 程式設計語言或指令碼語言（例如 JScript）使用 COM 的程式設計人員使用。 腳本支援可讓您輕鬆存取在本機電腦區域（例如小工具）中執行之專案的位置資料。 Windows SDK 包括標頭檔、檔 (，包括腳本參考檔) 、範例和工具，可協助引導 Web 和軟體發展人員如何在其程式中使用位置資訊。

## <a name="location-and-other-sensors-control-panel"></a>定位和其他感應器主控台

Windows 7 包含一個控制台，可讓電腦系統管理員啟用或停用整個系統或每位使用者的感應器。 因為某些感應器可以公開機密資料，所以此使用者介面可讓系統管理員控制所有程式是否都能存取每個使用者的每個感應器。 使用者也可以查看感應器屬性，並變更使用者介面中顯示的感應器描述。

主控台也提供預設位置頁面，讓使用者能夠提供其位置。 如果沒有可用的感應器，平臺將會使用使用者提供的位置。 使用者可以提供市政位址欄位，其中包括街道位址、城市、州/省和國家或地區。

## <a name="related-topics"></a>相關主題

[關於感應器 API](about-the-sensor-api.md)

[Windows 硬體開發人員中心網站](https://www.microsoft.com/whdc/device/sensors/default.mspx)

[Windows 開發人員中心](https://msdn.microsoft.com/windows/default.aspx?wt.svl=client)

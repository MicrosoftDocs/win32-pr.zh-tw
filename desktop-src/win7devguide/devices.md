---
title: " (Windows 7 開發人員指南) 的裝置"
description: 裝置是 PC 體驗的基本部分，而 Windows 7 為與裝置互動的應用程式開發人員提供了新的可能性。
ms.assetid: faed8ec8-2f12-4090-a003-b14b3d26e02a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 775389f1a3548e2e94b8b2c25f9b46560cef5fc61a5e486f5dff28871da9f9e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119086731"
---
# <a name="devices-windows-7-developer-guide"></a> (Windows 7 開發人員指南) 的裝置

裝置是 PC 體驗的基本部分，而 Windows 7 為與裝置互動的應用程式開發人員提供了新的可能性。 裝置體驗平臺可讓應用程式和服務與特定裝置產生關聯，讓使用者可以在連線時立即取得其周邊的最大效益。 感應器平臺會提供一組 Api 來探索和通訊感應器裝置，以啟用新的應用程式來感知其環境。 位置平臺會提供新的 Api，以使用來自全球定位系統的位置資料 (GPS) 接收器或其他服務，以啟用行動使用者的位置特定應用程式行為。  (參閱 [裝置基本概念-總覽](https://www.microsoft.com/whdc/device/default.mspx). ) 

## <a name="device-experience-platform"></a>裝置體驗平臺

Windows 7 結合了軟體與服務，為行動電話、便攜媒體播放機、攝影機和印表機創造令人興奮的新體驗。 Windows 7 可讓您更輕鬆地直接從 Windows 桌面使用這些裝置。 它也提供在 Windows 桌面上具有顯著放置的裝置製作者，並供應商標機會和簡單介面，以呈現裝置所支援的功能和服務。

透過裝置體驗平臺，每個 Windows 會話都會變成一個入口網站，讓客戶從其裝置獲得更多價值。 裝置體驗平臺可讓使用者與裝置製造商連接、探索及使用相關服務，以及瞭解配件。 由於裝置體驗已連線到 Microsoft 的 web 服務，因此即使在裝置寄送給取用者之後，裝置公司也可以更新體驗。 裝置體驗平臺可以為 Windows *標誌* 的裝置產生類似應用程式的體驗，例如行動電話。

裝置體驗平臺可讓應用程式存取裝置，例如行動電話和媒體播放機，透過 *媒體傳輸通訊協定 (MTP)* 或 [Windows 可攜式裝置](https://www.bing.com/search?q=Windows+Portable+Devices)驅動程式模型來執行服務。

若要啟用電腦與裝置之間的個人資訊同步處理，裝置體驗平臺會為連接的裝置裝載新的同步處理平臺，並提供使用者介面來選取資料同步處理（例如 **連絡人**、行事 **曆** 和工作）的目標應用 **程式。**  (參閱[Windows 裝置體驗](https://www.microsoft.com/whdc/device/DeviceExperience/default.mspx)。 ) 

## <a name="windows-biometric-framework"></a>Windows 生物特徵辨識架構

Windows 生物特徵辨識架構 (WBF) 提供 API，可讓應用程式使用指紋裝置來註冊、識別及驗證使用者身分識別，而不需要直接存取任何生物特徵辨識指紋硬體或範例。 您可以使用 WBF 搭配具有 Windows 生物識別設備介面 (WBDI) 驅動程式的指紋裝置。 WBF 可透過管理感應器通訊、生物特徵辨識與範本儲存體的外掛程式介面卡進行擴充。 這可確保 WBF 可搭配各式各樣的指紋感應器使用。 在 Windows 7 中，指紋辨識器可以使用 WBF 在 *UAC* 和 Windows 登入期間進行驗證。  (參閱[Windows 生物特徵辨識架構 API](../secbiomet/biometric-service-api-portal.md)。 ) 

 

 

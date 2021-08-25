---
title: WindowsMedia 裝置管理員 11 SDK
description: WindowsMedia 裝置管理員 11 SDK
ms.assetid: 9c0c9a96-1335-4ae2-9393-bfab0dfe24c6
keywords:
- Windows媒體裝置管理員，關於
- 裝置管理員，關於
- '媒體傳輸通訊協定 (MTP) '
- 'MTP (媒體傳輸通訊協定) '
- '大量儲存體類別 (SERVICES.MSC) '
- 'SERVICES.MSC (大量儲存體類別) '
- Windows媒體裝置管理員，桌面應用程式
- 裝置管理員，桌面應用程式
- 桌面應用程式，關於
- Windows媒體裝置管理員、服務提供者
- 裝置管理員，服務提供者
- 服務提供者，關於
- Windows媒體裝置管理員、外掛程式
- 裝置管理員、外掛程式 insp
- 外掛程式，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57e8b19b035f0210b7928dcc42c19d9519a63fe4eac3e5adaeded780c9d4c729
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004808"
---
# <a name="windows-media-device-manager-11-sdk"></a>WindowsMedia 裝置管理員 11 SDK

> [!IMPORTANT]
> Windows 媒體裝置管理員 api 現在已包含在 Windows SDK 中。 不需要其他 SDK 下載。

 

Microsoft Windows Media 裝置管理員軟體發展工具組 (SDK) 可讓您建立可與連線可攜式裝置通訊的桌面應用程式和元件。 Windows媒體裝置管理員可讓您的應用程式或元件列舉、探索和交換具有裝置的檔案、查詢中繼資料，以及要求播放次數資訊。 Windows 媒體裝置管理員上建的應用程式或元件具有一致的 API，可與各種不同的裝置進行通訊，包括媒體傳輸通訊協定 (MTP) 、大型儲存體類別 (services.msc) 、RAPI，以及其他以最新版本和舊版 Windows 媒體技術為基礎的其他裝置。

您可以使用 Windows 媒體裝置管理員 SDK 來建立下列專案：

-   桌面應用程式，例如自訂媒體播放機。 應用程式和可攜式裝置之間的所有通訊都必須經過 Windows 媒體裝置管理員，其可作為應用程式、Microsoft 數位版權管理系統與服務提供者之間的訊息代理程式。
-   服務提供者，可作為自訂裝置和桌面應用程式之間的通訊連結。 雖然 Microsoft 提供數個服務提供者，可與大部分的裝置通訊，但您可以建立自訂服務提供者，以自訂裝置與桌面應用程式之間的通訊。
-   外掛程式，可執行工作，例如要求和記錄裝置上的播放次數。 這些外掛程式可以附加至其他桌面應用程式，例如 Windows Media Player，以將資訊傳送給內容提供者來處理對演出者的專利款項。

若要下載 Windows media 裝置管理員 SDK，請參閱 MSDN 網站上[的 Windows 媒體下載頁面](https://msdn.microsoft.com/windows/desktop/aa904949)。

此 SDK 是 Microsoft Windows 媒體軟體發展工具組的元件。 其他元件包含 Windows 媒體格式 SDK、Windows Media Services SDK、Windows 媒體編碼器 sdk、Windows media Rights Manager sdk 和 Windows Media Player SDK。

本檔包含下列各節。



| 區段                                            | 描述                                                                                                                                                                                                                                                     |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [快速入門](getting-started.md)             | 描述這一版 Windows 媒體裝置管理員的新功能、概述 Windows 媒體裝置管理員的運作方式、描述開發應用程式或服務提供者所需的功能，並說明 SDK 隨附的範例。 |
| [程式設計指南](programming-guide.md)         | 討論如何建立應用程式和服務提供者。                                                                                                                                                                                                      |
| [程式設計參考](programming-reference.md) | 針對 Windows 媒體裝置管理員 SDK 所支援的介面、方法、類別和結構，提供 c + + 參考資訊。                                                                                                                      |
| [*詞彙*](wmdm-glossary.md)                    | 定義本檔中使用的詞彙。                                                                                                                                                                                                                       |



 

 

 





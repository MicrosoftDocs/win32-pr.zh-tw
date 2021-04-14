---
title: Windows Media 裝置管理員 11 SDK
description: Windows Media 裝置管理員 11 SDK
ms.assetid: 9c0c9a96-1335-4ae2-9393-bfab0dfe24c6
keywords:
- Windows Media 裝置管理員，關於
- 裝置管理員，關於
- '媒體傳輸通訊協定 (MTP) '
- 'MTP (媒體傳輸通訊協定) '
- '大量儲存類別 (SERVICES.MSC) '
- 'SERVICES.MSC (大型儲存類別) '
- Windows Media 裝置管理員，桌面應用程式
- 裝置管理員，桌面應用程式
- 桌面應用程式，關於
- Windows Media 裝置管理員、服務提供者
- 裝置管理員，服務提供者
- 服務提供者，關於
- Windows Media 裝置管理員、外掛程式
- 裝置管理員、外掛程式 insp
- 外掛程式，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2b167e8244fb6f03a584dfb71255eabfa359c8e
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/09/2020
ms.locfileid: "104383125"
---
# <a name="windows-media-device-manager-11-sdk"></a>Windows Media 裝置管理員 11 SDK

> [!IMPORTANT]
> Windows Media 裝置管理員 Api 現在已包含在 Windows SDK 中。 不需要其他 SDK 下載。

 

Microsoft Windows Media 裝置管理員軟體發展工具組 (SDK) 可讓您建立可與連線可攜式裝置通訊的桌面應用程式和元件。 Windows Media 裝置管理員可讓您的應用程式或元件列舉、探索和交換具有裝置的檔案、查詢中繼資料，以及要求播放次數資訊。 Windows Media 裝置管理員上建的應用程式或元件具有一致的 API，可與各種不同的裝置進行通訊，包括媒體傳輸通訊協定 (MTP) 、大型儲存類別 (SERVICES.MSC) 、RAPI，以及其他以最新版本和舊版 Windows Media 技術為基礎的其他裝置。

您可以使用 Windows Media 裝置管理員 SDK 來建立下列專案：

-   桌面應用程式，例如自訂媒體播放機。 應用程式和可攜式裝置之間的所有通訊都必須經過 Windows Media 裝置管理員，以作為應用程式、Microsoft 數位版權管理系統和服務提供者之間的代理程式。
-   服務提供者，可作為自訂裝置和桌面應用程式之間的通訊連結。 雖然 Microsoft 提供數個服務提供者，可與大部分的裝置通訊，但您可以建立自訂服務提供者，以自訂裝置與桌面應用程式之間的通訊。
-   外掛程式，可執行工作，例如要求和記錄裝置上的播放次數。 這些外掛程式可以附加至其他桌面應用程式，例如 Windows Media Player，以將資訊傳送給內容提供者來處理對演出者的專利款項。

若要下載 Windows Media 裝置管理員 SDK，請參閱 MSDN 網站上 [的 Windows Media 下載頁面](https://msdn.microsoft.com/windows/desktop/aa904949) 。

此 SDK 是 Microsoft Windows Media 軟體發展工具組的元件。 其他元件包括 Windows Media Format SDK、Windows Media Services SDK、Windows Media 編碼器 SDK、Windows Media Rights Manager SDK 和 Windows Media Player SDK。

本檔包含下列各節。



| 區段                                            | 描述                                                                                                                                                                                                                                                     |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [快速入門](getting-started.md)             | 描述這一版 Windows Media 裝置管理員的新功能、概述 Windows Media 裝置管理員的運作方式、描述開發應用程式或服務提供者所需的功能，並說明 SDK 隨附的範例。 |
| [程式設計指南](programming-guide.md)         | 討論如何建立應用程式和服務提供者。                                                                                                                                                                                                      |
| [程式設計參考](programming-reference.md) | 提供 Windows Media 裝置管理員 SDK 所支援之介面、方法、類別和結構的 c + + 參考資訊。                                                                                                                      |
| [*詞彙*](wmdm-glossary.md)                    | 定義本檔中使用的詞彙。                                                                                                                                                                                                                       |



 

 

 





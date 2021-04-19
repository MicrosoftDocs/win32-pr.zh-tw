---
description: WPD 應用程式設計介面
ms.assetid: 3e2be15f-7af7-4e76-89b1-f9bc591c4f1b
title: WPD 應用程式設計介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c44dbcf731aa46941599b99766e52fa67a5c5a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975233"
---
# <a name="wpd-application-programming-interface"></a>WPD 應用程式設計介面

在 Windows 可攜式裝置上建立的應用程式可以探索裝置、傳送和接收內容，甚至控制裝置，例如拍攝圖片或傳送文字訊息。 系統設計為具有彈性，因此可以探索許多類型的裝置，並可進行擴充，讓驅動程式開發人員可以定義自訂裝置的自訂屬性和命令。

下表描述此檔的主要主題。



| 主題                                                                                                                  | 描述                                                                                                |
|------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [應用程式開發的一般需求](general-requirements-for-application-development.md)               | 使用 Windows 可攜式裝置開發驅動程式和應用程式的硬體和軟體需求。     |
| [Windows Media DRM-Enabled 應用程式的需求](requirements-for-windows-media-drm-enabled-applications.md) | 啟用 Windows Media 受 DRM 保護的內容傳輸所需的屬性。                      |
| [範例](sample.md)                                                                                                  | 此軟體發展工具組所提供的兩個命令列桌面應用程式的描述。 |
| [應用程式總覽](application-overview.md)                                                                       | Windows 可攜式裝置中使用的重要概念。                                                             |
| [程式設計指南](programming-guide.md)                                                                             | 應用程式將執行的主要工作，以及逐步指示和程式碼片段。              |
| [程式設計參考](programming-reference.md)                                                                     | Windows 可攜式裝置所定義之介面和資料類型的參考指南。                      |



 

以 Windows Media 裝置管理員或 Windows 映像取得建立的應用程式可以透過相容性層存取 Windows 可攜式裝置。

Microsoft 提供數個標準通訊協定和裝置的驅動程式，包括媒體傳輸通訊協定 (MTP) 裝置和大型儲存類別 (SERVICES.MSC) 裝置。 如果您熟悉 User-Mode 驅動程式架構，您可以為自訂裝置開發自己的驅動程式。

 

 




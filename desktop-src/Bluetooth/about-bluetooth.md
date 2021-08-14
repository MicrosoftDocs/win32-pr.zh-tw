---
title: 關於藍牙
description: 藍牙是一種業界標準的通訊協定，可為許多裝置（包括電腦、印表機、行動電話和掌上型裝置）啟用無線連線能力。
ms.assetid: 424168a1-e55c-4947-9a80-8594b4d83bbd
keywords:
- 藍牙藍牙，請參閱
- 藍牙藍牙，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51ed0f50b6fbe800960c7451bde4d7b43b744d1d2f2d8e398a7656a9f3261479
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118173179"
---
# <a name="about-bluetooth"></a>關於藍牙

藍牙是一種業界標準的通訊協定，可為許多裝置（包括電腦、印表機、行動電話和掌上型裝置）啟用無線連線能力。

主要藍牙功能包括：

-   低成本、低功率耗用量無線通訊協定，具有業界標準的支援和全球接受。
-   一種定義熟悉的程式設計介面，可讓開發人員用來快速開發或移植應用程式。
-   官方網站和業界合作的組織，可解釋、升級及標準化藍牙技術。 如需詳細資訊，請參閱 [www.bluetooth.com](https://www.bluetooth.com/)。

Windows 上的藍牙提供的核心服務，與傳輸控制通訊協定所公開的服務 (tcp/ip) 的 tcp 部分。 就像許多網路通訊協定和服務一樣，藍牙的連線能力和資料傳輸會透過 Windows 通訊端函式呼叫，使用常見的 Windows 通訊端程式設計技術和特定藍牙延伸模組進行程式設計。 不過，由於有線、固定網路和無線臨機網路之間有顯著的差異，藍牙提供服務/裝置探索和通知等擴充功能，讓應用程式在無線環境中正常運作。 這些延伸模組也 pave 了簡單移植到類似的技術（例如 IrDA 或未來的無線傳輸）的方式。

Microsoft 支援在 Windows xp service pack 1 (SP1) 和更新版本、Windows xp Embedded （含 service pack 2）和 Windows CE 上藍牙。 在 Windows xp 上執行的藍牙應用程式應該能夠在包含必要相依性的 Windows XP Embedded 執行時間映射上執行。 如需 Windows XP embedded 的詳細資訊，請參閱 MSDN 上的 Windows XP embedded 說明文件（英文）。 如需 Windows CE 程式設計的詳細資訊，請參閱 Windows CE SDK。

Microsoft 提供兩種方法，讓您在 Windows 上進行藍牙程式設計：

-   使用 Windows 通訊端介面
-   使用 nonsocket 藍牙介面直接管理裝置

本節提供下列主題中這兩種方法的總覽資訊。 如需有關使用 Windows 通訊端 API 元素來進行程式藍牙的詳細資訊，請參閱[藍牙使用 Windows 通訊端](bluetooth-programming-with-windows-sockets.md)進行程式設計。



| 區段                                                                                | Content                                                           |
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [適用於藍牙的 Windows 通訊端支援](windows-sockets-support-for-bluetooth.md)     | 描述藍牙與 Windows 通訊端之間的關聯性。 |
| [管理藍牙裝置和服務](managing-bluetooth-devices-and-services.md) | 說明如何管理藍牙的裝置和服務。           |



 

 

 





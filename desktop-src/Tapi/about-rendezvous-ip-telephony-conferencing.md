---
description: TAPI 3 會合控制項提供了用來通告及探索多方多媒體 IP 會議的機制。 以下描述一組元件物件模型 (COM) 元件和介面來執行會議。
ms.assetid: 0ca2edac-b507-497e-9e63-78a10466e2eb
title: 關於會合 IP 電話語音會議
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4bd06fb848088a42e34bd7b176358a7507e3d2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104554028"
---
# <a name="about-rendezvous-ip-telephony-conferencing"></a>關於會合 IP 電話語音會議

\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。 RTC 用戶端 API 提供類似的功能。\]

TAPI 3 會合控制項提供了用來通告及探索多方多媒體 IP 會議的機制。 以下描述一組元件物件模型 (COM) 元件和介面來執行會議。

COM 是適用于 TAPI 3 的基本程式碼模型，在本檔中，我們會假設您已熟悉。 如需 COM 的詳細資訊，請搜尋平臺軟體發展工具組 (SDK) 。

## <a name="features"></a>功能

-   提供會議目錄的摘要，以操作多媒體會議的公告
-   透過驗證、加密及每個公告存取控制層 (ACL 提供安全性) 
-   提供會議公告的一般架構，並依屬性值啟用搜尋
-   允許延伸模組透過提供者維護的屬性 (架構中的會議 blob) 
-   提供多播位址配置的 COM 包裝函式， (MADCAP) API

## <a name="architecture"></a>架構

下列說明和圖表說明系統架構的重要層面。

-   用戶端可以使用會合控制項來操作儲存在 ILS 動態目錄或 NTDS 伺服器上的會議。 輕量型目錄存取協定 (LDAP) 用來與 ILS 伺服器通訊。
-   會合控制項提供用於腳本和程式設計的雙重 COM 介面。
-   會話公告通訊協定 (可直接存取網際網路的 SAP) 伺服器會接聽網際網路上的會議公告，並以會議資訊填入 ILS 動態伺服器。 同樣地，它也會宣佈在本機建立的會議範圍包含網際網路。  (不會針對 Microsoft Windows 2000 規劃 SAP 伺服器。 ) 

![會合系統架構](images/rend1.png)

 

 




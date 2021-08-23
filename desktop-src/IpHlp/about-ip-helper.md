---
description: 網際網路通訊協定協助程式 (IP 協助程式) 可讓應用程式抓取本機電腦網路設定的相關資訊，以及修改該設定，以協助本機電腦的網路管理。
ms.assetid: 9eb8af78-612f-406c-ab92-4623b10a510e
title: 關於 IP Helper
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77445eb999b08bda038fbffc4de5d440b7a3e79c3fa921d50f6da4ccc1f42237
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014186"
---
# <a name="about-ip-helper"></a>關於 IP Helper

網際網路通訊協定協助程式 (IP 協助程式) 可讓應用程式抓取本機電腦網路設定的相關資訊，以及修改該設定，以協助本機電腦的網路管理。 IP 協助程式也提供通知機制，以確保應用程式會在本機電腦網路設定的特定層面變更時收到通知。

許多 IP Helper 函式都會傳遞結構參數，以代表與 [管理資訊基礎](/previous-versions/windows/desktop/mib/about-management-information-base) 技術相關聯的資料類型。 IP Helper 函式會使用這些結構來代表各種網路資訊，例如 ARP 快取專案。 由於 MIB API 也會使用這些結構，因此會在 [管理資訊基底參考](/previous-versions/windows/desktop/mib/management-information-base-reference)中說明這些結構。 雖然 IP 協助程式 API 使用這些結構，但 IP 協助程式與管理資訊基礎 (MIB) 和簡單的網路管理通訊協定 (SNMP) 不同。

IP 協助程式檔會廣泛地使用「介面卡」和「介面」詞彙。 「介面卡」是一種舊版的詞彙，它是一種網路介面卡的縮寫形式，最初指的是某種形式的網路硬體。 介面卡是一種交叉連結層級的抽象概念。

「介面」是在 IETF RFC 檔中使用的較新詞彙。 Rfc 將介面定義為抽象概念，以表示連結的節點附件。 介面是 IP 層級的抽象概念。

IP 協助程式檔中的介面卡和介面詞彙會稍微交替使用。 在 IP 協助程式檔中，介面卡清單可能包含軟體 WAN 介面以及回送介面 (這兩個都不是指硬體裝置) 。 在 IP 協助程式 Api 中，有一個介面卡與介面的一對一對應。

IP 協助程式提供下列方面的功能：

-   [正在抓取網路設定的相關資訊](retrieving-information-about-network-configuration.md)
-   [管理網路介面卡](managing-network-adapters.md)
-   [管理介面](managing-interfaces.md)
-   [管理 IP 位址](managing-ip-addresses.md)
-   [使用位址解析通訊協定](using-the-address-resolution-protocol.md)
-   [在網際網路通訊協定和網際網路控制訊息通訊協定上抓取資訊](retrieving-information-on-the-internet-protocol-and-the-internet-control-message-protocol.md)
-   [管理路由](managing-routing.md)
-   [接收網路事件的通知](receiving-notification-of-network-events.md)
-   [正在抓取傳輸控制通訊協定和使用者資料包協定的相關資訊](retrieving-information-about-the-transmission-control-protocol-and-the-user-datagram-protocol.md)

 

 

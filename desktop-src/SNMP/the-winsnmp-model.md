---
title: WinSNMP 模型
description: 符合 WinSNMP 規範的模型包含下列基本元件。
ms.assetid: 491df017-0b91-4fcf-97c3-4e296c3324bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8814786b6ae44527460930daf5a9e8164645ca0ecfce52824831b2dbc7e61e80
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127578"
---
# <a name="the-winsnmp-model"></a>WinSNMP 模型

符合 WinSNMP 規範的模型包含下列基本元件：

-   支援 WinSNMP 的 SNMP 網路管理應用程式，也就是與 WinSNMP 相容的 *應用程式*
-   WinSNMP 函數層級
-   支援 WinSNMP 的 SNMP 服務提供者，也就是符合 WinSNMP 規範的 *執行*

必須傳達 SNMP 訊息的網路管理應用程式，在事件驅動的環境中有效率地運作。 這是因為 SNMP 是在未建立虛擬電路的遠端實體之間，以資料包為基礎或不需連線的通訊協定。

由於 Microsoft Windows 的應用程式也是由事件驅動，因此，WinSNMP 會使用程式設計模型，在此模型中會接收和處理非同步 *訊息事件* 磁片磁碟機管理應用程式。 非同步訊息事件可以是由管理員應用程式發出的 SNMP 作業要求，或是由代理程式應用程式對要求的回應。

SNMP 會以 SNMP 訊息的形式傳送要求和回應。 SNMP 訊息是 SNMP 通訊協定資料單位 (PDU) 再加上相關 RFC 所定義的其他訊息標頭元素。 如需詳細資訊，請參閱 [關於 SNMP 訊息](about-snmp-messages.md)、使用變數系結 [清單](working-with-variable-binding-lists.md) 和 [使用通訊協定資料單位](working-with-protocol-data-units.md)。

 

 





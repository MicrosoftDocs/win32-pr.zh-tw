---
title: 關於 Microsoft WinSNMP 的執行
description: Microsoft WinSNMP 實行符合 WinSNMP 2.0 版。
ms.assetid: 99e11d30-d159-4d9b-94d0-baa6e49d82cf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 693a2fd5c6aa21d684d485f75b04160e72bfe1455c13ef8c320c863b61ab696b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009866"
---
# <a name="about-the-microsoft-winsnmp-implementation"></a>關於 Microsoft WinSNMP 的執行

Microsoft WinSNMP 實行符合 WinSNMP 2.0 版。 它支援在 WinSNMP 1.1 版規格和 WinSNMP 2.0 版附錄中定義的所有函式和作業。 此實為 WinSNMP 應用程式提供下列服務：

-   管理與管理實體之間的通訊。 實體可以位於本機電腦上，或透過本機或廣域網路或網際網路連接。 如需詳細資訊，請參閱 [SNMP 支援的層級](levels-of-snmp-support.md)。
-   隱藏 SNMP 通訊協定的詳細資料，抽象語法標記法 (一)  (asn.1) ，以及基本編碼規則 (BER) 來描述傳輸語法。
-   確認 Pdu 是否正確，並拒絕不正確 Pdu。 如需詳細資訊，請參閱 [使用通訊協定資料單位](working-with-protocol-data-units.md)。
-   在必要時，根據相關的 Rfc 轉換 SNMPv2C PDU 類型。
-   根據 RFC 1908 「在第1版與第2版的網際網路標準網路管理架構之間共存」，將 SNMPv1 陷阱從 SNMPv1 代理程式轉換為 SNMPv2C 陷阱。 如需詳細資訊，請參閱 [將陷阱從 SNMPv1 轉換為 SNMPv2C](translating-traps-from-snmpv1-to-snmpv2c.md)。
-   支援應用程式的重新傳輸原則，並提供重新傳輸執行支援。 如需詳細資訊，請參閱 [WinSNMP 資料庫](the-winsnmp-database.md) 和 [關於重新傳輸](about-retransmission.md)。
-   提供應用程式的實體和內容轉譯支援。 如需詳細資訊，請參閱 [WinSNMP 資料庫](the-winsnmp-database.md) 以及 [設定實體和內容轉譯模式](setting-the-entity-and-context-translation-mode.md)。

如需有關 WinSNMP 應用程式與執行之間關聯性的詳細資訊，請參閱 [winsnmp 資料管理概念](winsnmp-data-management-concepts.md) 和 [winsnmp 會話](winsnmp-sessions.md)。

 

 





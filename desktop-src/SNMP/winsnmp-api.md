---
title: WinSNMP API
description: Microsoft Windows SNMP 應用程式開發介面 () 1.1 a 和2.0 版的 WinSNMP API，可讓您開發以 SNMP 為基礎的網路管理應用程式，這些應用程式會在 Windows 環境中執行。
ms.assetid: 54d9b61a-815a-41c3-9365-ec4478acc3f2
keywords:
- WinSNMP API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c38f6205b8d5ad2315be877f62f0f81f17b5737e557d5db2683163ff26edf62c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142981"
---
# <a name="winsnmp-api"></a>WinSNMP API

\[SNMP 可用於 [需求] 區段中指定的作業系統。 它在後續版本中可能會變更或無法使用。 相反地，請使用[Windows 遠端管理](/windows/desktop/WinRM/portal)，也就是 Microsoft 對 ws-atomictransaction 的實。\]

Microsoft Windows SNMP 應用程式開發介面 () 1.1 a 和2.0 版的 WinSNMP API，可讓您開發以 SNMP 為基礎的網路管理應用程式，這些應用程式會在 Windows 環境中執行。 簡易網路管理通訊協定 (SNMP) 是一種要求-回應通訊協定，可在通訊協定實體之間傳輸管理資訊。

已透過數個公司、關聯和個人的合作、輸入和支援，共同開發了 WinSNMP。

本總覽的第一個部分提供有關 WinSNMP 2.0 增補、SNMP 版本的資訊，以及 (Rfc) 的相關要求清單。 它也會說明 WinSNMP 模型，以及 Microsoft WinSNMP 的元件和功能。 此外也提供您在 WinSNMP 環境中進行程式設計所需的資料管理和通訊概念的相關資訊。

第二節討論的是 WinSNMP 函數以及下列相關的 WinSNMP 程式設計工作：

-   [開啟和關閉 WinSNMP 應用程式](opening-and-closing-a-winsnmp-application.md)
-   [開啟和關閉 WinSNMP 會話](opening-and-closing-a-winsnmp-session.md)
-   [管理陷阱和通知](managing-traps-and-notifications.md)
-   [使用變數系結清單](working-with-variable-binding-lists.md)
-   [使用通訊協定資料單位](working-with-protocol-data-units.md)
-   [傳送 SNMP 訊息](sending-snmp-messages.md)
-   [接收 SNMP 訊息](receiving-snmp-messages.md)
-   [管理物件識別碼](managing-object-identifiers.md)
-   [釋放 WinSNMP 描述項](freeing-winsnmp-descriptors.md)
-   [設定實體和內容轉譯模式](setting-the-entity-and-context-translation-mode.md)
-   [管理重新傳輸原則](managing-the-retransmission-policy.md)
-   [使用多個執行緒撰寫的 WinSNMP 應用程式](writing-winsnmp-applications-with-multiple-threads.md)
-   [註冊 SNMP 代理程式應用程式](registering-an-snmp-agent-application.md)

閱讀此總覽之前，您應該先熟悉 SNMP 和 Windows 程式設計的基本概念。 如需 SNMP 的詳細資訊，請參閱「 [簡易網路管理通訊協定](simple-network-management-protocol-snmp-.md) 」和批註的相關要求 (rfc) 這些要求是由「網際網路工程任務推動力 (IETF) 所發行。

 

 
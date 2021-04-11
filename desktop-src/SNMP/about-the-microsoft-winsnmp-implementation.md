---
title: 關於 Microsoft WinSNMP 的執行
description: Microsoft WinSNMP 實行符合 WinSNMP 2.0 版。
ms.assetid: 99e11d30-d159-4d9b-94d0-baa6e49d82cf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cbf142ba85458374105af5b80ca5af30a6c5082
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103931807"
---
# <a name="about-the-microsoft-winsnmp-implementation"></a><span data-ttu-id="1670c-103">關於 Microsoft WinSNMP 的執行</span><span class="sxs-lookup"><span data-stu-id="1670c-103">About the Microsoft WinSNMP Implementation</span></span>

<span data-ttu-id="1670c-104">Microsoft WinSNMP 實行符合 WinSNMP 2.0 版。</span><span class="sxs-lookup"><span data-stu-id="1670c-104">The Microsoft WinSNMP implementation complies with WinSNMP version 2.0.</span></span> <span data-ttu-id="1670c-105">它支援在 WinSNMP 1.1 版規格和 WinSNMP 2.0 版附錄中定義的所有函式和作業。</span><span class="sxs-lookup"><span data-stu-id="1670c-105">It supports all the functions and operations defined in both the WinSNMP version 1.1a specification and the WinSNMP version 2.0 Addendum.</span></span> <span data-ttu-id="1670c-106">此實為 WinSNMP 應用程式提供下列服務：</span><span class="sxs-lookup"><span data-stu-id="1670c-106">The implementation provides the following services for WinSNMP applications:</span></span>

-   <span data-ttu-id="1670c-107">管理與管理實體之間的通訊。</span><span class="sxs-lookup"><span data-stu-id="1670c-107">Manages communications to and from management entities.</span></span> <span data-ttu-id="1670c-108">實體可以位於本機電腦上，或透過本機或廣域網路或網際網路連接。</span><span class="sxs-lookup"><span data-stu-id="1670c-108">The entity can reside on the local computer or be connected through a local or wide-area network, or the Internet.</span></span> <span data-ttu-id="1670c-109">如需詳細資訊，請參閱 [SNMP 支援的層級](levels-of-snmp-support.md)。</span><span class="sxs-lookup"><span data-stu-id="1670c-109">For more information, see [Levels of SNMP Support](levels-of-snmp-support.md).</span></span>
-   <span data-ttu-id="1670c-110">隱藏 SNMP 通訊協定的詳細資料，抽象語法標記法 (一)  (asn.1) ，以及基本編碼規則 (BER) 來描述傳輸語法。</span><span class="sxs-lookup"><span data-stu-id="1670c-110">Hides the details of SNMP protocol, Abstract Syntax Notation One (ASN.1), and the Basic Encoding Rules (BER) for describing transfer syntax.</span></span>
-   <span data-ttu-id="1670c-111">確認 Pdu 是否正確，並拒絕不正確 Pdu。</span><span class="sxs-lookup"><span data-stu-id="1670c-111">Verifies the correctness of PDUs and rejects invalid PDUs.</span></span> <span data-ttu-id="1670c-112">如需詳細資訊，請參閱 [使用通訊協定資料單位](working-with-protocol-data-units.md)。</span><span class="sxs-lookup"><span data-stu-id="1670c-112">For more information, see [Working with Protocol Data Units](working-with-protocol-data-units.md).</span></span>
-   <span data-ttu-id="1670c-113">在必要時，根據相關的 Rfc 轉換 SNMPv2C PDU 類型。</span><span class="sxs-lookup"><span data-stu-id="1670c-113">Transforms SNMPv2C PDU types when necessary in accordance with the relevant RFCs.</span></span>
-   <span data-ttu-id="1670c-114">根據 RFC 1908 「在第1版與第2版的網際網路標準網路管理架構之間共存」，將 SNMPv1 陷阱從 SNMPv1 代理程式轉換為 SNMPv2C 陷阱。</span><span class="sxs-lookup"><span data-stu-id="1670c-114">Converts SNMPv1 traps from an SNMPv1 agent to SNMPv2C traps in accordance with RFC 1908, "Coexistence between Version 1 and Version 2 of the Internet-standard Network Management Framework."</span></span> <span data-ttu-id="1670c-115">如需詳細資訊，請參閱 [將陷阱從 SNMPv1 轉換為 SNMPv2C](translating-traps-from-snmpv1-to-snmpv2c.md)。</span><span class="sxs-lookup"><span data-stu-id="1670c-115">For more information, see [Translating Traps from SNMPv1 to SNMPv2C](translating-traps-from-snmpv1-to-snmpv2c.md).</span></span>
-   <span data-ttu-id="1670c-116">支援應用程式的重新傳輸原則，並提供重新傳輸執行支援。</span><span class="sxs-lookup"><span data-stu-id="1670c-116">Supports the application's retransmission policy and provides retransmission execution support.</span></span> <span data-ttu-id="1670c-117">如需詳細資訊，請參閱 [WinSNMP 資料庫](the-winsnmp-database.md) 和 [關於重新傳輸](about-retransmission.md)。</span><span class="sxs-lookup"><span data-stu-id="1670c-117">For more information, see [The WinSNMP Database](the-winsnmp-database.md) and [About Retransmission](about-retransmission.md).</span></span>
-   <span data-ttu-id="1670c-118">提供應用程式的實體和內容轉譯支援。</span><span class="sxs-lookup"><span data-stu-id="1670c-118">Provides entity and context translation support for the application.</span></span> <span data-ttu-id="1670c-119">如需詳細資訊，請參閱 [WinSNMP 資料庫](the-winsnmp-database.md) 以及 [設定實體和內容轉譯模式](setting-the-entity-and-context-translation-mode.md)。</span><span class="sxs-lookup"><span data-stu-id="1670c-119">For more information, see [The WinSNMP Database](the-winsnmp-database.md) and [Setting the Entity and Context Translation Mode](setting-the-entity-and-context-translation-mode.md).</span></span>

<span data-ttu-id="1670c-120">如需有關 WinSNMP 應用程式與執行之間關聯性的詳細資訊，請參閱 [winsnmp 資料管理概念](winsnmp-data-management-concepts.md) 和 [winsnmp 會話](winsnmp-sessions.md)。</span><span class="sxs-lookup"><span data-stu-id="1670c-120">For additional information about the relationship between a WinSNMP application and the implementation, see [WinSNMP Data Management Concepts](winsnmp-data-management-concepts.md) and [WinSNMP Sessions](winsnmp-sessions.md).</span></span>

 

 





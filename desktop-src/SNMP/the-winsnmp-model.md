---
title: WinSNMP 模型
description: 符合 WinSNMP 規範的模型包含下列基本元件。
ms.assetid: 491df017-0b91-4fcf-97c3-4e296c3324bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff7ae4fa1c1ee56fc534e4aa4c9bffefb8d7f4d2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021104"
---
# <a name="the-winsnmp-model"></a><span data-ttu-id="b9122-103">WinSNMP 模型</span><span class="sxs-lookup"><span data-stu-id="b9122-103">The WinSNMP Model</span></span>

<span data-ttu-id="b9122-104">符合 WinSNMP 規範的模型包含下列基本元件：</span><span class="sxs-lookup"><span data-stu-id="b9122-104">The WinSNMP-compliant model includes the following basic components:</span></span>

-   <span data-ttu-id="b9122-105">支援 WinSNMP 的 SNMP 網路管理應用程式，也就是與 WinSNMP 相容的 *應用程式*</span><span class="sxs-lookup"><span data-stu-id="b9122-105">A WinSNMP-enabled SNMP network management application, that is, a WinSNMP-compliant *application*</span></span>
-   <span data-ttu-id="b9122-106">WinSNMP 函數層級</span><span class="sxs-lookup"><span data-stu-id="b9122-106">The WinSNMP function layer</span></span>
-   <span data-ttu-id="b9122-107">支援 WinSNMP 的 SNMP 服務提供者，也就是符合 WinSNMP 規範的 *執行*</span><span class="sxs-lookup"><span data-stu-id="b9122-107">A WinSNMP-enabled SNMP service provider, that is, a WinSNMP-compliant *implementation*</span></span>

<span data-ttu-id="b9122-108">必須傳達 SNMP 訊息的網路管理應用程式，在事件驅動的環境中有效率地運作。</span><span class="sxs-lookup"><span data-stu-id="b9122-108">Network management applications that must convey SNMP messages operate efficiently in an event-driven environment.</span></span> <span data-ttu-id="b9122-109">這是因為 SNMP 是在未建立虛擬電路的遠端實體之間，以資料包為基礎或不需連線的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="b9122-109">This is because SNMP is a datagram-based or connectionless protocol between remote entities that do not establish virtual circuits.</span></span>

<span data-ttu-id="b9122-110">由於 Microsoft Windows 應用程式也是事件驅動，因此，WinSNMP 會使用程式設計模型，在此模型中會接收和處理非同步 *訊息事件* 磁片磁碟機管理應用程式。</span><span class="sxs-lookup"><span data-stu-id="b9122-110">Since Microsoft Windows applications are also event-driven, WinSNMP uses a programming model in which the receipt and processing of asynchronous *message-events* drive management applications.</span></span> <span data-ttu-id="b9122-111">非同步訊息事件可以是由管理員應用程式發出的 SNMP 作業要求，或是由代理程式應用程式對要求的回應。</span><span class="sxs-lookup"><span data-stu-id="b9122-111">An asynchronous message-event can be an SNMP operation request by a manager application, or the response to a request by an agent application.</span></span>

<span data-ttu-id="b9122-112">SNMP 會以 SNMP 訊息的形式傳送要求和回應。</span><span class="sxs-lookup"><span data-stu-id="b9122-112">SNMP sends requests and responses as SNMP messages.</span></span> <span data-ttu-id="b9122-113">SNMP 訊息是 SNMP 通訊協定資料單位 (PDU) 再加上相關 RFC 所定義的其他訊息標頭元素。</span><span class="sxs-lookup"><span data-stu-id="b9122-113">An SNMP message is an SNMP protocol data unit (PDU) plus additional message header elements defined by the relevant RFC.</span></span> <span data-ttu-id="b9122-114">如需詳細資訊，請參閱 [關於 SNMP 訊息](about-snmp-messages.md)、使用變數系結 [清單](working-with-variable-binding-lists.md) 和 [使用通訊協定資料單位](working-with-protocol-data-units.md)。</span><span class="sxs-lookup"><span data-stu-id="b9122-114">For more information, see [About SNMP Messages](about-snmp-messages.md), [Working with Variable Binding Lists](working-with-variable-binding-lists.md) and [Working with Protocol Data Units](working-with-protocol-data-units.md).</span></span>

 

 





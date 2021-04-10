---
title: 補漏設格式
description: 陷阱 Pdu 的格式與其他 Pdu 的格式不同。 SNMPv1 陷阱和 SNMPv2C 陷阱的格式也不同。
ms.assetid: 2d2b4520-28b7-4a2e-8dee-456e17d9d6f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e87adc3222808fcc7e81904ade07c09afa13bc6d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021103"
---
# <a name="trap-formats"></a><span data-ttu-id="1490d-104">補漏設格式</span><span class="sxs-lookup"><span data-stu-id="1490d-104">Trap Formats</span></span>

<span data-ttu-id="1490d-105">陷阱 Pdu 的格式與其他 Pdu 的格式不同。</span><span class="sxs-lookup"><span data-stu-id="1490d-105">The format of trap PDUs is different than that of other PDUs.</span></span> <span data-ttu-id="1490d-106">SNMPv1 陷阱和 SNMPv2C 陷阱的格式也不同。</span><span class="sxs-lookup"><span data-stu-id="1490d-106">The format of SNMPv1 traps and SNMPv2C traps is also different.</span></span>

<span data-ttu-id="1490d-107">在 SNMPv2C 架構下，PDU 陷印格式是以下列方式組織的 *n* 個變數系結專案的變數系結清單：</span><span class="sxs-lookup"><span data-stu-id="1490d-107">Under the SNMPv2C framework, the PDU trap format is a variable binding list of *n* variable binding entries organized in the following manner:</span></span>

-   <span data-ttu-id="1490d-108">第一個變數系結專案包含時間戳記。</span><span class="sxs-lookup"><span data-stu-id="1490d-108">The first variable binding entry contains a time-stamp.</span></span>
-   <span data-ttu-id="1490d-109">第二個變數系結專案是識別陷阱的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="1490d-109">The second variable binding entry is an object identifier that identifies the trap.</span></span>
-   <span data-ttu-id="1490d-110">第三個到 *n* 個變數系結專案（如果有的話）會包含與該陷阱相關聯的其他資訊。</span><span class="sxs-lookup"><span data-stu-id="1490d-110">The third through *n* variable binding entries, if present, contain additional information associated with the trap.</span></span>

<span data-ttu-id="1490d-111">在 SNMPv1 架構下，PDU 陷印格式如下所示。</span><span class="sxs-lookup"><span data-stu-id="1490d-111">Under the SNMPv1 framework, the PDU trap format is as follows.</span></span>

| <span data-ttu-id="1490d-112">欄位</span><span class="sxs-lookup"><span data-stu-id="1490d-112">Field</span></span>                      | <span data-ttu-id="1490d-113">描述</span><span class="sxs-lookup"><span data-stu-id="1490d-113">Description</span></span>                                                      |
|----------------------------|------------------------------------------------------------------|
| <span data-ttu-id="1490d-114">企業</span><span class="sxs-lookup"><span data-stu-id="1490d-114">enterprise</span></span>                 | <span data-ttu-id="1490d-115">識別產生陷阱的裝置類型。</span><span class="sxs-lookup"><span data-stu-id="1490d-115">Identifies the type of device that generated the trap.</span></span>           |
| <span data-ttu-id="1490d-116">代理程式-addr</span><span class="sxs-lookup"><span data-stu-id="1490d-116">agent-addr</span></span>                 | <span data-ttu-id="1490d-117">識別產生陷阱的裝置 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="1490d-117">Identifies the IP address of the device that generated the trap.</span></span> |
| <span data-ttu-id="1490d-118">一般-陷阱/特定-陷阱</span><span class="sxs-lookup"><span data-stu-id="1490d-118">generic-trap/specific-trap</span></span> | <span data-ttu-id="1490d-119">識別預先定義的陷阱類型。</span><span class="sxs-lookup"><span data-stu-id="1490d-119">Identifies a predefined trap type.</span></span>                               |
| <span data-ttu-id="1490d-120">時間戳記</span><span class="sxs-lookup"><span data-stu-id="1490d-120">time-stamp</span></span>                 | <span data-ttu-id="1490d-121">識別產生陷阱的時間。</span><span class="sxs-lookup"><span data-stu-id="1490d-121">Identifies when the trap was generated.</span></span>                          |
| <span data-ttu-id="1490d-122">變數系結</span><span class="sxs-lookup"><span data-stu-id="1490d-122">variable-bindings</span></span>          | <span data-ttu-id="1490d-123">包含與陷阱相關聯的其他資訊。</span><span class="sxs-lookup"><span data-stu-id="1490d-123">Contains additional information associated with the trap.</span></span>        |



 

<span data-ttu-id="1490d-124">[**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg)函數一律會傳回 SNMPv2C 格式的訊息。</span><span class="sxs-lookup"><span data-stu-id="1490d-124">The [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) function always returns a message in the SNMPv2C format.</span></span> <span data-ttu-id="1490d-125">如果訊息包含「 **SNMP \_ PDU \_ 陷阱**」作業類型，應用程式可以讀取訊息的變數系結專案，並取得與該陷阱相關聯的資訊。</span><span class="sxs-lookup"><span data-stu-id="1490d-125">If the message contains the operation type **SNMP\_PDU\_TRAP**, the application can read the variable binding entries of the message and retrieve the information associated with the trap.</span></span>

 

 





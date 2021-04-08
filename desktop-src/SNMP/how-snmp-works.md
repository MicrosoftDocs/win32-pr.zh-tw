---
title: SNMP 的運作方式
description: 協力廠商 SNMP 管理主控台應用程式如何從 SNMP 服務傳回信息。
ms.assetid: 2edbf9ff-b9e3-4103-affc-a5c0f22b80a1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39d58943f0765b60f9c235094642d3fa759402db
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932073"
---
# <a name="how-snmp-works"></a><span data-ttu-id="c4684-103">SNMP 的運作方式</span><span class="sxs-lookup"><span data-stu-id="c4684-103">How SNMP Works</span></span>

<span data-ttu-id="c4684-104">下列步驟概述協力廠商 SNMP 管理主控台應用程式如何從 SNMP 服務傳回信息：</span><span class="sxs-lookup"><span data-stu-id="c4684-104">The following steps outline how a third-party SNMP management console application returns information from the SNMP service:</span></span>

1.  <span data-ttu-id="c4684-105">SNMP 管理主控台應用程式會根據使用者的輸入來會構成 SNMP 訊息。</span><span class="sxs-lookup"><span data-stu-id="c4684-105">The SNMP management console application formulates an SNMP message based on input from the user.</span></span> <span data-ttu-id="c4684-106">此訊息包含通訊協定資料單位 (PDU) 和驗證資訊。</span><span class="sxs-lookup"><span data-stu-id="c4684-106">The message includes a protocol data unit (PDU) and authentication information.</span></span> <span data-ttu-id="c4684-107">管理主控台應用程式可以使用 Microsoft SNMP 管理 API 程式庫 (MGMTAPI.DLL) 或 Microsoft [WINSNMP API](winsnmp-api.md) 程式庫 (WSNMP32.DLL) 來執行此步驟。</span><span class="sxs-lookup"><span data-stu-id="c4684-107">The management console application can use the Microsoft SNMP Management API library (MGMTAPI.DLL) or the Microsoft [WinSNMP API](winsnmp-api.md) library (WSNMP32.DLL) to perform this step.</span></span>
2.  <span data-ttu-id="c4684-108">SNMP 管理主控台應用程式會使用 SNMP 服務程式庫，將 SNMP 訊息傳送至 SNMP 服務。</span><span class="sxs-lookup"><span data-stu-id="c4684-108">The SNMP management console application sends the SNMP message to the SNMP service, using the SNMP service libraries.</span></span>
3.  <span data-ttu-id="c4684-109">SNMP 服務收到要求。</span><span class="sxs-lookup"><span data-stu-id="c4684-109">The SNMP service receives the request.</span></span> <span data-ttu-id="c4684-110">它會驗證驗證資訊和來源 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="c4684-110">It verifies the authentication information and the source IP address.</span></span>
4.  <span data-ttu-id="c4684-111">SNMP 服務會選取適當的擴充代理程式，並要求代理程式取得要求的資訊。</span><span class="sxs-lookup"><span data-stu-id="c4684-111">The SNMP service selects the appropriate extension agent and requests that the agent retrieve the requested information.</span></span>
5.  <span data-ttu-id="c4684-112">SNMP 服務會將回應傳送至 SNMP 管理主控台應用程式。</span><span class="sxs-lookup"><span data-stu-id="c4684-112">The SNMP service sends the response to the SNMP management console application.</span></span>

 

 





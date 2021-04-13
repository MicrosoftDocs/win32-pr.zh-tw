---
title: 訊息和訊息佇列屬性
description: 訊息具有屬性，可指定標籤、訊息主體和數個選項。
ms.assetid: d0c9126e-a2c6-4d70-b87a-154a570899fc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0139a588b52f1de1de43d8ec50aebdaf57b995ea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301355"
---
# <a name="message-and-message-queue-properties"></a><span data-ttu-id="49666-103">訊息和訊息佇列屬性</span><span class="sxs-lookup"><span data-stu-id="49666-103">Message and Message Queue Properties</span></span>

<span data-ttu-id="49666-104">訊息具有屬性，可指定標籤、訊息主體和數個選項。</span><span class="sxs-lookup"><span data-stu-id="49666-104">A message has properties, which specify a label, a message body, and a number of options.</span></span> <span data-ttu-id="49666-105">訊息屬性選項可以包含服務品質、優先順序、日誌、隱私權和驗證層級，以及訊息的存留期。</span><span class="sxs-lookup"><span data-stu-id="49666-105">Message property options can include quality of service, priority, journaling, privacy and authentication levels, and the lifetime of the message.</span></span> <span data-ttu-id="49666-106">在傳統 (非 RPC) 訊息佇列應用程式中，您可以藉由呼叫 MSMQ SDK 檔中所述的 MSMQ API 函數或 COM 物件方法來指定這些屬性。</span><span class="sxs-lookup"><span data-stu-id="49666-106">In conventional (non-RPC) message-queuing applications, you specify these properties by calling the MSMQ API functions or COM object methods, which are described in the MSMQ SDK documentation.</span></span> <span data-ttu-id="49666-107">RPC 用戶端應用程式可以藉由呼叫 [**RpcBindingSetOption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption) 和 [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo)，來設定遠端程序呼叫的特定屬性。</span><span class="sxs-lookup"><span data-stu-id="49666-107">RPC client applications can set certain properties for remote procedure calls by calling [**RpcBindingSetOption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption) and [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo).</span></span> <span data-ttu-id="49666-108">一旦設定之後，這些屬性會在用戶端應用程式重設之前，對每個訊息保持有效狀態。</span><span class="sxs-lookup"><span data-stu-id="49666-108">Once set, the properties remain in effect for each message until the client application resets them.</span></span>

<span data-ttu-id="49666-109">訊息佇列有自己的一組屬性，除了訊息之外。</span><span class="sxs-lookup"><span data-stu-id="49666-109">A message queue has its own set of properties, apart from those of the messages.</span></span> <span data-ttu-id="49666-110">這些屬性會唯一識別佇列，並定義佇列提供的服務類別、此佇列中訊息所需的隱私權和驗證層級，以及訊息是否為分散式交易的一部分。</span><span class="sxs-lookup"><span data-stu-id="49666-110">These properties uniquely identify a queue and define the class of service that the queue provides, the privacy and authentication levels required for messages in this queue, and whether the messages are to be part of a distributed transaction.</span></span> <span data-ttu-id="49666-111">如同訊息屬性，您可以藉由呼叫 MSMQ API 函數或 COM 物件方法（如 MSMQ 檔中所述）來指定訊息佇列的屬性。</span><span class="sxs-lookup"><span data-stu-id="49666-111">As with message properties, you specify the properties of a message queue by calling the MSMQ API functions or COM object methods, which are described in the MSMQ documentation.</span></span> <span data-ttu-id="49666-112">不過，RPC 伺服器應用程式在呼叫 [**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) 來建立系結時，可以指定其專屬接收佇列的屬性。</span><span class="sxs-lookup"><span data-stu-id="49666-112">However, an RPC server application can specify properties of its own receive queue when it calls [**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) to establish the binding.</span></span>

 

 





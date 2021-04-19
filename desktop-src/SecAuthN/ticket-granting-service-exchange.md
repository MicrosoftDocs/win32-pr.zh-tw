---
description: 在票證授與票證 (TGT) 和用戶端已建立工作階段金鑰之後，用戶端就可以要求個別的工作階段金鑰和服務的票證。
ms.assetid: b4f63642-9282-4e11-b40c-eec406b2dd2b
title: 票證授權服務交換
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3b227ee551d762abd145ca56c6cced110b6a2dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986844"
---
# <a name="ticket-granting-service-exchange"></a><span data-ttu-id="6a158-103">票證授權服務交換</span><span class="sxs-lookup"><span data-stu-id="6a158-103">Ticket-Granting Service Exchange</span></span>

<span data-ttu-id="6a158-104">在票證授與票證 (TGT) 和用戶端已建立 [*工作階段金鑰*](../secgloss/s-gly.md) 之後，用戶端就可以要求個別的工作階段金鑰和服務的票證。</span><span class="sxs-lookup"><span data-stu-id="6a158-104">After a ticket-granting ticket (TGT) and [*session key*](../secgloss/s-gly.md) have been established for the client, the client can request a separate session key and ticket for the service.</span></span>

<span data-ttu-id="6a158-105">**為另一個服務要求票證**</span><span class="sxs-lookup"><span data-stu-id="6a158-105">**To request a ticket for another service**</span></span>

1.  <span data-ttu-id="6a158-106">使用者工作站上的 Kerberos 用戶端會藉由傳送至 [*金鑰發佈中心*](../secgloss/k-gly.md) (KDC) 的訊息來要求服務的 [*認證*](../secgloss/c-gly.md)，該訊息類型為 KRB \_ TGS \_ 要求 (Kerberos Ticket-Granting 服務要求) 。</span><span class="sxs-lookup"><span data-stu-id="6a158-106">The Kerberos client on the user's workstation requests [*credentials*](../secgloss/c-gly.md) for the service by sending, to the [*Key Distribution Center*](../secgloss/k-gly.md) (KDC), a message of type KRB\_TGS\_REQ (Kerberos Ticket-Granting Service Request).</span></span> <span data-ttu-id="6a158-107">此訊息包含用戶端要求認證的服務身分識別、以使用者的新登入 [*工作階段金鑰*](../secgloss/s-gly.md)加密的驗證器訊息，以及從 [驗證服務交換](authentication-service-exchange.md)取得的 TGT。</span><span class="sxs-lookup"><span data-stu-id="6a158-107">This message consists of the identity of the service for which the client is requesting credentials, an authenticator message encrypted with the user's new logon [*session key*](../secgloss/s-gly.md), and the TGT obtained from the [Authentication Service Exchange](authentication-service-exchange.md).</span></span>
2.  <span data-ttu-id="6a158-108">當 KDC 收到 KRB 的 TGS 要求時 \_ \_ ，kdc 會使用其秘密金鑰來解密 TGT，並解壓縮使用者的登入工作階段金鑰。</span><span class="sxs-lookup"><span data-stu-id="6a158-108">When the KDC receives a KRB\_TGS\_REQ, the KDC decrypts the TGT with its secret key and extracts the user's logon session key.</span></span>
3.  <span data-ttu-id="6a158-109">KDC 會使用登入 [*工作階段金鑰*](../secgloss/s-gly.md) 來解密使用者的驗證器訊息，並進行評估。</span><span class="sxs-lookup"><span data-stu-id="6a158-109">The KDC uses the logon [*session key*](../secgloss/s-gly.md) to decrypt the user's authenticator message and evaluates it.</span></span> <span data-ttu-id="6a158-110">如果驗證器通過測試，KDC 會從 TGT 解壓縮使用者的授權資料，並 invents 工作階段金鑰，讓使用者與要求的伺服器共用。</span><span class="sxs-lookup"><span data-stu-id="6a158-110">If the authenticator passes the test, the KDC extracts the user's authorization data from the TGT and invents a session key for the user to share with the requested server.</span></span>
4.  <span data-ttu-id="6a158-111">KDC 會使用使用者的登入工作階段金鑰，加密一份服務工作階段金鑰。</span><span class="sxs-lookup"><span data-stu-id="6a158-111">The KDC encrypts one copy of the service session key with the user's logon session key.</span></span>
5.  <span data-ttu-id="6a158-112">KDC 會將服務工作階段金鑰的另一份複本內嵌在票證中，連同使用者的授權資料，並使用伺服器的 [*主要金鑰*](../secgloss/m-gly.md)來加密票證。</span><span class="sxs-lookup"><span data-stu-id="6a158-112">The KDC embeds another copy of the service session key in a ticket, along with the user's authorization data, and encrypts the ticket with the server's [*master key*](../secgloss/m-gly.md).</span></span>
6.  <span data-ttu-id="6a158-113">KDC 會以 KRB \_ TGS \_ 代表 (Kerberos Ticket-Granting 服務回復) 的訊息來回複，將這些認證傳送回用戶端。</span><span class="sxs-lookup"><span data-stu-id="6a158-113">The KDC sends these credentials back to the client by replying with a message of type KRB\_TGS\_REP (Kerberos Ticket-Granting Service Reply).</span></span>
7.  <span data-ttu-id="6a158-114">當用戶端收到回復時，它會使用使用者的登入工作階段金鑰來解密服務工作階段金鑰，並將服務工作階段金鑰儲存在其票證快取中。</span><span class="sxs-lookup"><span data-stu-id="6a158-114">When the client receives the reply, it decrypts the service session key with the user's logon session key and stores the service session key in its ticket cache.</span></span>
8.  <span data-ttu-id="6a158-115">用戶端會將票證解壓縮至伺服器，並將其儲存在其票證快取中。</span><span class="sxs-lookup"><span data-stu-id="6a158-115">The client extracts the ticket to the server and stores that in its ticket cache.</span></span>

 

 

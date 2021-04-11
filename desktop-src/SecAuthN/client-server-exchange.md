---
description: 用戶端/伺服器交換
ms.assetid: 2449c4b3-720d-4b84-b3cf-fcc4abd05d33
title: 用戶端/伺服器交換
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6274705ef6719c846f0551f90fca8790ba89f2e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114944"
---
# <a name="clientserver-exchange"></a><span data-ttu-id="5e48a-103">用戶端/伺服器交換</span><span class="sxs-lookup"><span data-stu-id="5e48a-103">Client/Server Exchange</span></span>

<span data-ttu-id="5e48a-104">當使用者對伺服器有票證之後，工作站用戶端就可以與該伺服器建立安全的通訊會話。</span><span class="sxs-lookup"><span data-stu-id="5e48a-104">After a user has a ticket to a server, the workstation client can establish a secure communications session with that server.</span></span>

<span data-ttu-id="5e48a-105">**若要建立與伺服器的安全通訊會話**</span><span class="sxs-lookup"><span data-stu-id="5e48a-105">**To establish a secure communications session with a server**</span></span>

1.  <span data-ttu-id="5e48a-106">用戶端會將 KRB AP 要求類型的訊息傳送給伺服器， \_ \_ (Kerberos 應用程式要求) 。</span><span class="sxs-lookup"><span data-stu-id="5e48a-106">The client sends the server a message of type KRB\_AP\_REQ (Kerberos Application Request).</span></span> <span data-ttu-id="5e48a-107">此訊息包含驗證器訊息，此訊息會使用 [*金鑰發佈中心*](/windows/desktop/SecGloss/k-gly) (KDC) 針對伺服器的會話、與伺服器會話的票證，以及指出用戶端是否要求相互驗證的旗標所傳送的金鑰進行加密。</span><span class="sxs-lookup"><span data-stu-id="5e48a-107">This message contains an authenticator message that is encrypted with the key sent by the [*Key Distribution Center*](/windows/desktop/SecGloss/k-gly) (KDC) for the session with the server, the ticket for sessions with the server, and a flag that indicates whether the client requests mutual authentication.</span></span> <span data-ttu-id="5e48a-108">設定要求相互驗證的旗標是設定 [*Kerberos*](/windows/desktop/SecGloss/k-gly)的其中一個選項。</span><span class="sxs-lookup"><span data-stu-id="5e48a-108">Setting the flag that requests mutual authentication is one of the options in configuring [*Kerberos*](/windows/desktop/SecGloss/k-gly).</span></span> <span data-ttu-id="5e48a-109">系統永遠不會詢問使用者是否應該使用相互驗證。</span><span class="sxs-lookup"><span data-stu-id="5e48a-109">The user is never asked whether mutual authentication should be used.</span></span>
2.  <span data-ttu-id="5e48a-110">伺服器會接收 KRB \_ 的 AP 要求 \_ 、解密票證，以及將使用者的授權資料和 [*工作階段金鑰*](/windows/desktop/SecGloss/s-gly)解壓縮。</span><span class="sxs-lookup"><span data-stu-id="5e48a-110">The server receives KRB\_AP\_REQ, decrypts the ticket, and extracts the user's authorization data and the [*session key*](/windows/desktop/SecGloss/s-gly).</span></span>
3.  <span data-ttu-id="5e48a-111">伺服器會使用票證中的工作階段金鑰，將使用者的驗證器訊息解密，並評估內的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="5e48a-111">The server uses the session key from the ticket to decrypt the user's authenticator message and evaluates the time stamp inside.</span></span>
4.  <span data-ttu-id="5e48a-112">如果驗證器訊息有效，伺服器會檢查用戶端要求中的相互驗證旗標。</span><span class="sxs-lookup"><span data-stu-id="5e48a-112">If the authenticator message is valid, the server checks the mutual authentication flag in the client's request.</span></span>
5.  <span data-ttu-id="5e48a-113">如果設定了相互驗證旗標，伺服器會使用工作階段金鑰來加密使用者驗證器訊息中的時間，並將結果傳回 KRB AP 代表類型的訊息， \_ \_ (Kerberos 應用程式回復) 。</span><span class="sxs-lookup"><span data-stu-id="5e48a-113">If the mutual authentication flag is set, the server uses the session key to encrypt the time from the user's authenticator message and returns the result in a message of type KRB\_AP\_REP (Kerberos Application Reply).</span></span>
6.  <span data-ttu-id="5e48a-114">當用戶端收到 KRB \_ AP \_ REP 時，它會使用與伺服器共用的工作階段金鑰將伺服器的驗證器訊息解密，並將服務傳回的時間與原始驗證器訊息中的時間進行比較。</span><span class="sxs-lookup"><span data-stu-id="5e48a-114">When the client receives KRB\_AP\_REP, it decrypts the server's authenticator message with the session key it shares with the server and compares the time sent back by the service with the time in its original authenticator message.</span></span> <span data-ttu-id="5e48a-115">如果兩者相符，用戶端就可以確保服務是正版的，且連接會繼續進行。</span><span class="sxs-lookup"><span data-stu-id="5e48a-115">If they match, the client is assured that the service is genuine, and the connection proceeds.</span></span>

 

 

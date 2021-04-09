---
title: 頻外信號
description: 使用目錄共用通用資料的共同應用程式，可以使用頻外信號來避免版本扭曲和部分更新。
ms.assetid: 82960273-5cda-44d2-bc17-d604f34f5a9b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bc630bfdf3a2700ab187cd24bbfc5a52def1103
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020837"
---
# <a name="out-of-band-signaling"></a><span data-ttu-id="57e3f-103">頻外信號</span><span class="sxs-lookup"><span data-stu-id="57e3f-103">Out-of-Band Signaling</span></span>

<span data-ttu-id="57e3f-104">使用目錄共用通用資料的共同應用程式，可以使用頻外信號來避免版本扭曲和部分更新。</span><span class="sxs-lookup"><span data-stu-id="57e3f-104">Cooperating applications that share common data using the directory can use out-of-band signaling to avoid both version skew and partial updates.</span></span> <span data-ttu-id="57e3f-105">簡單來說，共同的應用程式會使用與目錄複寫分開的機制，以通知彼此共用的一般資料變更。</span><span class="sxs-lookup"><span data-stu-id="57e3f-105">Put simply, the cooperating applications use a mechanism separate from directory replication to inform each other of changes in the shared common data.</span></span> <span data-ttu-id="57e3f-106">頻外信號與版本控制機制搭配使用時最有效-這可讓夥伴偵測變更，以通知遠端夥伴要等候的共用資料版本。</span><span class="sxs-lookup"><span data-stu-id="57e3f-106">Out-of-band signaling is most effective when used in combination with a versioning mechanism—this allows the partner detecting the change to notify remote partners what version of the shared data to wait for.</span></span>

<span data-ttu-id="57e3f-107">回到 Active Directory Domain Services 中複寫 [行為](replication-behavior-in-active-directory-domain-services.md)的「版本扭曲」一節所提供的 rpc 範例，RPC 伺服器可以回呼連線的用戶端，告知他們移至新的伺服器：「我即將移動。</span><span class="sxs-lookup"><span data-stu-id="57e3f-107">Returning to the RPC example given in the "Version Skew" section of [Replication Behavior in Active Directory Domain Services](replication-behavior-in-active-directory-domain-services.md), the RPC server could call back into connected clients to inform them of the move to a new server: "I am going to move.</span></span> <span data-ttu-id="57e3f-108">請稍候，複寫會立即為您帶來新的位址」，讓用戶端可以處理轉換期間。</span><span class="sxs-lookup"><span data-stu-id="57e3f-108">Please stand by, replication will bring you the new address shortly" so that the client can handle the transition period.</span></span>

<span data-ttu-id="57e3f-109">需要完全相同原則才能彼此通訊的應用程式，可以使用頻外信號來確保不會採用新的原則，直到所有相關的合作物件都收到為止。</span><span class="sxs-lookup"><span data-stu-id="57e3f-109">Applications that require identical policies to be in force in order to communicate with each other can use out-of-band signaling to ensure that a new policy is not employed until all involved parties have received it.</span></span> <span data-ttu-id="57e3f-110">例如，如果兩部電腦之間的網際網路通訊協定安全性 (IPsec) 原則變更，則來源機器上的代理程式可以聯繫目的地電腦上的代理程式，以協調已變更原則的應用程式，並讓來源電腦延遲應用程式，直到目的地電腦也收到新的原則為止。</span><span class="sxs-lookup"><span data-stu-id="57e3f-110">For example, if the Internet Protocol security (IPsec) policy between two machines is changed, an agent on the source machine could contact an agent on the destination machine to negotiate the application of the changed policy, with the source machine delaying application until the destination machine has received the new policy as well.</span></span>

 

 





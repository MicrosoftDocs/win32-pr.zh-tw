---
title: 關於使用 Kerberos 進行相互驗證
description: 在相互驗證中，用戶端和服務必須先驗證各自的身分識別，再執行應用程式功能。
ms.assetid: 5ce923d6-bede-4acb-b297-e93f2f506ea9
ms.tgt_platform: multiple
keywords:
- 關於使用 Kerberos AD 的相互驗證
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9685dad0bd20f233b8dcb0ecf12af338f318646f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020753"
---
# <a name="about-mutual-authentication-using-kerberos"></a><span data-ttu-id="7d25b-104">關於使用 Kerberos 進行相互驗證</span><span class="sxs-lookup"><span data-stu-id="7d25b-104">About Mutual Authentication Using Kerberos</span></span>

<span data-ttu-id="7d25b-105">在相互驗證中，用戶端和服務必須先驗證各自的身分識別，再執行應用程式功能。</span><span class="sxs-lookup"><span data-stu-id="7d25b-105">In mutual authentication, the client and service must verify their respective identities to each other before performing application functions.</span></span> <span data-ttu-id="7d25b-106">這兩個合作物件都不能執行其他作業，除非已驗證身分識別;也就是說，服務必須能夠驗證用戶端，而不需要查詢用戶端，而且用戶端必須能夠在不查詢服務的情況下驗證服務。</span><span class="sxs-lookup"><span data-stu-id="7d25b-106">Neither party can perform operations with the other until identity has been verified; that is, the service must be able to verify the client without querying the client and the client must be able to verify the service without querying the service.</span></span>

<span data-ttu-id="7d25b-107">可以驗證用戶端的服務值是知名的。</span><span class="sxs-lookup"><span data-stu-id="7d25b-107">The value of a service that can authenticate a client is well-known.</span></span> <span data-ttu-id="7d25b-108">例如，檔案服務會模擬用戶端，以判斷用戶端可以存取的檔案。</span><span class="sxs-lookup"><span data-stu-id="7d25b-108">For example, a file service impersonates a client to determine which files the client can access.</span></span>

<span data-ttu-id="7d25b-109">可以驗證服務的用戶端值比較不容易理解。</span><span class="sxs-lookup"><span data-stu-id="7d25b-109">The value of a client that can authenticate a service is less understood.</span></span> <span data-ttu-id="7d25b-110">驗證服務可讓用戶端信任從服務取得的資料，並且在將機密資料傳送至服務時安全。</span><span class="sxs-lookup"><span data-stu-id="7d25b-110">Authenticating a service enables the client to trust the data that it gets from the service and to be secure in sending sensitive data to the service.</span></span> <span data-ttu-id="7d25b-111">在支援用戶端安全性內容委派的用戶端/服務應用程式中，用戶端驗證服務的能力特別重要;也就是，用戶端會授權服務在存取其他服務或網路資源時作為其委派。</span><span class="sxs-lookup"><span data-stu-id="7d25b-111">The ability of a client to authenticate a service is particularly important in client/service applications that support delegation of the client's security context; that is, the client authorizes the service to act as its delegate in accessing additional services or network resources.</span></span>

<span data-ttu-id="7d25b-112">服務會驗證用戶端，如下所示：用戶端會在先前建立的內容中執行（例如，在已登入使用者的會話中執行），或明確向基礎安全性提供者出示認證，藉以建立本機安全性內容。</span><span class="sxs-lookup"><span data-stu-id="7d25b-112">A service authenticates a client as follows: The client establishes a local security context either by executing in a previously established context, for example, in the session of a logged-in user, or by explicitly presenting credentials to the underlying security provider.</span></span> <span data-ttu-id="7d25b-113">服務無法接受來自任何未經驗證之用戶端的連接。</span><span class="sxs-lookup"><span data-stu-id="7d25b-113">The service cannot accept connections from any unauthenticated client.</span></span>

<span data-ttu-id="7d25b-114">用戶端用來驗證服務的 Kerberos 機制如下所示：當安裝服務時，以系統管理員許可權執行的服務安裝程式會為每個服務實例註冊一或多個唯一的 Spn。</span><span class="sxs-lookup"><span data-stu-id="7d25b-114">The Kerberos mechanism by which a client authenticates a service works as follows: When a service is installed, a service installer, running with administrator privileges, registers one or more unique SPNs for each service instance.</span></span> <span data-ttu-id="7d25b-115">這些名稱會在服務實例將用來登入之使用者或電腦帳戶物件的 Active Directory 網網域控制站 (DC) 中註冊。</span><span class="sxs-lookup"><span data-stu-id="7d25b-115">The names are registered in the Active Directory Domain Controller (DC) on the user or computer account object that the service instance will use to log on.</span></span> <span data-ttu-id="7d25b-116">當用戶端要求服務的連接時，它會使用已知的資料或使用者提供的資料來撰寫服務實例的 SPN。</span><span class="sxs-lookup"><span data-stu-id="7d25b-116">When a client requests a connection to a service, it composes an SPN for a service instance, using known data or data provided by the user.</span></span> <span data-ttu-id="7d25b-117">接著，用戶端會使用 SSPI negotiate 套件，將 SPN 呈現給用戶端網域帳戶的金鑰發佈中心 (KDC) 。</span><span class="sxs-lookup"><span data-stu-id="7d25b-117">The client then uses the SSPI negotiate package to present the SPN to the Key Distribution Center (KDC) for the client domain account.</span></span> <span data-ttu-id="7d25b-118">KDC 會在樹系中搜尋已註冊 SPN 的使用者或電腦帳戶。</span><span class="sxs-lookup"><span data-stu-id="7d25b-118">The KDC searches the forest for a user or computer account on which that SPN is registered.</span></span> <span data-ttu-id="7d25b-119">如果 SPN 註冊在一個以上的帳戶上，驗證就會失敗。</span><span class="sxs-lookup"><span data-stu-id="7d25b-119">If the SPN is registered on more than one account, the authentication fails.</span></span> <span data-ttu-id="7d25b-120">否則，KDC 會使用註冊 SPN 之帳戶的密碼來加密訊息。</span><span class="sxs-lookup"><span data-stu-id="7d25b-120">Otherwise, the KDC encrypts a message using the password of the account on which the SPN was registered.</span></span> <span data-ttu-id="7d25b-121">KDC 會將這個加密的訊息傳遞給用戶端，然後再將它傳遞給服務實例。</span><span class="sxs-lookup"><span data-stu-id="7d25b-121">The KDC passes this encrypted message to the client, which in turn passes it to the service instance.</span></span> <span data-ttu-id="7d25b-122">服務會使用 SSPI 協商套件來解密訊息，然後將訊息傳回用戶端，並傳送給用戶端的 KDC。</span><span class="sxs-lookup"><span data-stu-id="7d25b-122">The service uses the SSPI negotiate package to decrypt the message, which it passes back to the client and on to the client's KDC.</span></span> <span data-ttu-id="7d25b-123">KDC 會在解密的訊息符合其原始訊息時驗證服務。</span><span class="sxs-lookup"><span data-stu-id="7d25b-123">The KDC authenticates the service if the decrypted message matches its original message.</span></span>

-   <span data-ttu-id="7d25b-124">如需撰寫和註冊 Spn 的詳細資訊，請參閱。[服務主體名稱](service-principal-names.md)</span><span class="sxs-lookup"><span data-stu-id="7d25b-124">For more information about composing and registering SPNs, see .[Service Principal Names](service-principal-names.md)</span></span>
-   <span data-ttu-id="7d25b-125">如需撰寫 Windows 通訊端服務之 SPN 的詳細資訊和程式碼範例，以服務連接點發佈本身，請參閱 [使用 SCP 撰寫服務的 spn](composing-the-spns-for-a-service-with-an-scp.md)。</span><span class="sxs-lookup"><span data-stu-id="7d25b-125">For more information and a code example that composes an SPN for a Windows Sockets service that publishes itself with a service connection point, see [Composing the SPNs for a Service with an SCP](composing-the-spns-for-a-service-with-an-scp.md).</span></span>
-   <span data-ttu-id="7d25b-126">如需撰寫 RPC 服務之 SPN 的詳細資訊和程式碼範例，請參閱 [撰寫 RpcNs 服務的 spn](composing-spns-for-an-rpcns-service.md)。</span><span class="sxs-lookup"><span data-stu-id="7d25b-126">For more information and a code example that composes an SPN for an RPC service, see [Composing SPNs for an RpcNs Service](composing-spns-for-an-rpcns-service.md).</span></span>

 

 





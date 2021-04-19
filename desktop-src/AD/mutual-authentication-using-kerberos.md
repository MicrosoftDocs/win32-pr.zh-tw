---
title: 使用 Kerberos 進行相互驗證
description: 相互驗證是一種安全性功能，其中用戶端程式必須向服務證明其身分識別，且服務必須向用戶端證明其身分識別，才能透過用戶端/服務連線傳輸任何應用程式流量。
ms.assetid: 775dd350-5c70-4d97-aa2f-d21e9aecc778
ms.tgt_platform: multiple
keywords:
- Active Directory，使用雙向驗證
- Active Directory，使用，安全性，相互驗證
- 安全性廣告
- 安全性 AD，相互驗證
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27cf2e68c1983dde9221cc3fa89866b5358ee6eb
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "106978574"
---
# <a name="mutual-authentication-using-kerberos"></a><span data-ttu-id="33e44-107">使用 Kerberos 進行相互驗證</span><span class="sxs-lookup"><span data-stu-id="33e44-107">Mutual Authentication Using Kerberos</span></span>

<span data-ttu-id="33e44-108">相互驗證是一種安全性功能，其中用戶端程式必須向服務證明其身分識別，且服務必須向用戶端證明其身分識別，才能透過用戶端/服務連線傳輸任何應用程式流量。</span><span class="sxs-lookup"><span data-stu-id="33e44-108">Mutual authentication is a security feature in which a client process must prove its identity to a service, and the service must prove its identity to the client, before any application traffic is transmitted over the client/service connection.</span></span>

<span data-ttu-id="33e44-109">Active Directory Domain Services 和 Windows 提供服務主體名稱 (SPN) 的支援，這是 Kerberos 機制中的重要元件，可供用戶端用來驗證服務。</span><span class="sxs-lookup"><span data-stu-id="33e44-109">Active Directory Domain Services and Windows provide support for service principal names (SPN), which are a key component in the Kerberos mechanism by which a client authenticates a service.</span></span> <span data-ttu-id="33e44-110">SPN 是唯一的名稱，用來識別服務的實例，並與服務實例執行所在的登入帳戶相關聯。</span><span class="sxs-lookup"><span data-stu-id="33e44-110">An SPN is a unique name that identifies an instance of a service and is associated with the logon account under which the service instance runs.</span></span> <span data-ttu-id="33e44-111">SPN 的元件可讓用戶端在沒有服務登入帳戶的情況下撰寫服務的 SPN。</span><span class="sxs-lookup"><span data-stu-id="33e44-111">The components of an SPN are such that a client can compose an SPN for a service without the service logon account.</span></span> <span data-ttu-id="33e44-112">這可讓用戶端要求服務驗證其帳戶，即使用戶端沒有帳戶名稱也一樣。</span><span class="sxs-lookup"><span data-stu-id="33e44-112">This enables the client to request the service to authenticate its account even though the client does not have the account name.</span></span>

<span data-ttu-id="33e44-113">本節包含下列主題的總覽：</span><span class="sxs-lookup"><span data-stu-id="33e44-113">This section includes an overview of:</span></span>

-   <span data-ttu-id="33e44-114">使用 Kerberos 進行相互驗證。</span><span class="sxs-lookup"><span data-stu-id="33e44-114">Mutual authentication using Kerberos.</span></span>
-   <span data-ttu-id="33e44-115">撰寫唯一的 SPN。</span><span class="sxs-lookup"><span data-stu-id="33e44-115">Composing a unique SPN.</span></span>
-   <span data-ttu-id="33e44-116">服務安裝程式如何在與服務實例相關聯的帳戶物件上註冊 Spn。</span><span class="sxs-lookup"><span data-stu-id="33e44-116">How a service installer registers SPNs on the account object associated with a service instance.</span></span>
-   <span data-ttu-id="33e44-117">用戶端應用程式如何在 Active Directory Domain Services 中使用服務實例的服務連接點 (SCP) 物件，來取出用來撰寫服務 SPN 的資料。</span><span class="sxs-lookup"><span data-stu-id="33e44-117">How a client application uses a service instance's service connection point (SCP) object in Active Directory Domain Services to retrieve data from which to compose an SPN for the service.</span></span>
-   <span data-ttu-id="33e44-118">用戶端應用程式如何搭配安全性支援提供者介面使用服務 SPN (SSPI) 來驗證服務。</span><span class="sxs-lookup"><span data-stu-id="33e44-118">How a client application uses a service SPN in conjunction with the Security Support Provider Interface (SSPI) to authenticate the service.</span></span>
-   <span data-ttu-id="33e44-119">Windows 通訊端用戶端/服務應用程式的程式碼範例，該應用程式會使用 SCP 和 SSPI 來執行相互驗證。</span><span class="sxs-lookup"><span data-stu-id="33e44-119">A code example for a Windows Sockets client/service application that uses an SCP and SSPI to perform mutual authentication.</span></span>
-   <span data-ttu-id="33e44-120">RPC 用戶端/服務的程式碼範例，此範例會使用 RPC 名稱服務和 RPC 驗證來執行相互驗證。</span><span class="sxs-lookup"><span data-stu-id="33e44-120">A code example for an RPC client/service that performs mutual authentication using the RPC name service and RPC authentication.</span></span>
-   <span data-ttu-id="33e44-121">Windows 通訊端註冊和解析 (RnR) 服務如何使用 Spn 來執行相互驗證。</span><span class="sxs-lookup"><span data-stu-id="33e44-121">How a Windows Sockets Registration and Resolution (RnR) service uses SPNs to perform mutual authentication.</span></span>

<span data-ttu-id="33e44-122">本節討論如何使用 Active Directory 網域服務進行相互驗證，特別是在相互驗證中，服務連接點和服務主體名稱的用途。</span><span class="sxs-lookup"><span data-stu-id="33e44-122">This section discusses using Active Directory Domain Service for mutual authentication, in particular, the purpose of service connection points and service principal names in mutual authentication.</span></span> <span data-ttu-id="33e44-123">這並不是有關如何使用 SSPI 進行相互驗證或適用于 RPC 和 Windows 通訊端應用程式的驗證和安全性支援的完整討論。</span><span class="sxs-lookup"><span data-stu-id="33e44-123">It is not a complete discussion of how to use SSPI for mutual authentication or the authentication and security support available for RPC and Windows Sockets applications.</span></span>

<span data-ttu-id="33e44-124">如需詳細資訊，請參閱</span><span class="sxs-lookup"><span data-stu-id="33e44-124">For more information, see:</span></span>

-   [<span data-ttu-id="33e44-125">使用服務連接點發佈</span><span class="sxs-lookup"><span data-stu-id="33e44-125">Publishing with service connection points</span></span>](publishing-with-service-connection-points.md)
-   [<span data-ttu-id="33e44-126">SSPI</span><span class="sxs-lookup"><span data-stu-id="33e44-126">SSPI</span></span>](/windows/desktop/SecAuthN/sspi)
-   [<span data-ttu-id="33e44-127">Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="33e44-127">Windows Sockets</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
-   [<span data-ttu-id="33e44-128">RPC</span><span class="sxs-lookup"><span data-stu-id="33e44-128">RPC</span></span>](/windows/desktop/Rpc/rpc-start-page)

 

 
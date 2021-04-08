---
title: 服務發行
description: 服務會使用儲存在 Active Directory Domain Services 中的物件來通告本身。
ms.assetid: 69e9256f-40ee-4aed-8213-1bbda0e508af
ms.tgt_platform: multiple
keywords:
- 服務發行集廣告
- Active Directory，使用服務發行集
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9437d9f4aa5184c53f2962d7b2640e933107501f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020826"
---
# <a name="service-publication"></a><span data-ttu-id="2b829-105">服務發行</span><span class="sxs-lookup"><span data-stu-id="2b829-105">Service Publication</span></span>

<span data-ttu-id="2b829-106">服務會使用儲存在 Active Directory Domain Services 中的物件來通告本身。</span><span class="sxs-lookup"><span data-stu-id="2b829-106">Services advertise themselves using objects stored in Active Directory Domain Services.</span></span> <span data-ttu-id="2b829-107">這就是所謂的 *服務發行*。</span><span class="sxs-lookup"><span data-stu-id="2b829-107">This is known as *service publication*.</span></span> <span data-ttu-id="2b829-108">用戶端會查詢目錄以找出服務。</span><span class="sxs-lookup"><span data-stu-id="2b829-108">Clients query the directory to locate services.</span></span> <span data-ttu-id="2b829-109">這稱為 *用戶端服務* 會合。</span><span class="sxs-lookup"><span data-stu-id="2b829-109">This is called *client-service rendezvous*.</span></span> <span data-ttu-id="2b829-110">本節將討論用於服務發行的目錄物件類型，並說明如何將它們用於用戶端服務會合。</span><span class="sxs-lookup"><span data-stu-id="2b829-110">This section discusses the types of directory objects used for service publication and explains how they are used for client-service rendezvous.</span></span>

<span data-ttu-id="2b829-111">本節將討論下列主題：</span><span class="sxs-lookup"><span data-stu-id="2b829-111">This section discusses the following topics:</span></span>

-   [<span data-ttu-id="2b829-112">服務發行的總覽</span><span class="sxs-lookup"><span data-stu-id="2b829-112">An overview of service publication</span></span>](about-service-publication.md)
-   [<span data-ttu-id="2b829-113">服務發行的安全性問題</span><span class="sxs-lookup"><span data-stu-id="2b829-113">Security issues for service publication</span></span>](security-issues-for-service-publication.md)
-   [<span data-ttu-id="2b829-114">連接點物件</span><span class="sxs-lookup"><span data-stu-id="2b829-114">Connection point objects</span></span>](connection-points.md)
-   [<span data-ttu-id="2b829-115">使用服務連接點發行 (Scp) </span><span class="sxs-lookup"><span data-stu-id="2b829-115">Publishing with service connection points (SCPs)</span></span>](publishing-with-service-connection-points.md)
-   [<span data-ttu-id="2b829-116">要在服務連接點中儲存的資訊</span><span class="sxs-lookup"><span data-stu-id="2b829-116">What information to store in a service connection point</span></span>](service-connection-point-properties.md)
-   [<span data-ttu-id="2b829-117">建立服務連接點的位置</span><span class="sxs-lookup"><span data-stu-id="2b829-117">Where to create a service connection point</span></span>](where-to-create-a-service-connection-point.md)
-   [<span data-ttu-id="2b829-118">如何使用服務連接點發佈可複寫、主機式和資料庫服務</span><span class="sxs-lookup"><span data-stu-id="2b829-118">How to publish replicable, host-based, and database services using service connection points</span></span>](service-connection-points-for-replicated-host-based-and-database-services.md)
-   [<span data-ttu-id="2b829-119">建立和維護服務連接點</span><span class="sxs-lookup"><span data-stu-id="2b829-119">Creating and maintaining a service connection point</span></span>](creating-and-maintaining-a-service-connection-point.md)
-   [<span data-ttu-id="2b829-120">用戶端如何查詢 SCP 並使用它來系結至服務實例</span><span class="sxs-lookup"><span data-stu-id="2b829-120">How a client queries for an SCP and uses it to bind to a service instance</span></span>](how-clients-find-and-use-a-service-connection-point.md)
-   [<span data-ttu-id="2b829-121">使用 RPC 名稱服務 (RpcNs) Api 來發佈 RPC 服務</span><span class="sxs-lookup"><span data-stu-id="2b829-121">Using the RPC name service (RpcNs) APIs to publish an RPC service</span></span>](publishing-with-the-rpc-name-service-rpcns.md)
-   [<span data-ttu-id="2b829-122">Windows 通訊端註冊和解析 (RnR) 發佈 Windows 通訊端服務</span><span class="sxs-lookup"><span data-stu-id="2b829-122">Windows Sockets registration and resolution (RnR) to publish a Windows Sockets service</span></span>](publishing-with-windows-sockets-registration-and-resolution.md)
-   [<span data-ttu-id="2b829-123">Com + 類別存放區中以 COM 為基礎的服務發行</span><span class="sxs-lookup"><span data-stu-id="2b829-123">Publication of COM-based services in the COM+ class store</span></span>](publishing-com-services.md)

<span data-ttu-id="2b829-124">如需服務和用戶端彼此驗證方式的詳細資訊，請參閱 [使用 Kerberos 的相互驗證](mutual-authentication-using-kerberos.md)。</span><span class="sxs-lookup"><span data-stu-id="2b829-124">For more information about how services and clients authenticate each other, see [Mutual Authentication Using Kerberos](mutual-authentication-using-kerberos.md).</span></span> <span data-ttu-id="2b829-125">如需有關服務安全性內容和登入帳戶的詳細資訊，請參閱 [服務登入帳戶](service-logon-accounts.md)。</span><span class="sxs-lookup"><span data-stu-id="2b829-125">For more information about service security contexts and logon accounts, see [Service Logon Accounts](service-logon-accounts.md).</span></span>

 

 





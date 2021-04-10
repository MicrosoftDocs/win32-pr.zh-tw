---
title: 服務主要名稱
description: 服務主體名稱 (SPN) 是服務實例的唯一識別碼。
ms.assetid: 54b02853-4097-4e37-b7a2-6b5cfd168ece
ms.tgt_platform: multiple
keywords:
- 服務主要名稱
- SPN 請參閱服務主體名稱
- 服務主體名稱 AD
- 服務主體名稱 AD、關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aaa34b7d90803a324faced7d67b56c0b6a1f13af
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "103842023"
---
# <a name="service-principal-names"></a><span data-ttu-id="bd469-107">服務主要名稱</span><span class="sxs-lookup"><span data-stu-id="bd469-107">Service Principal Names</span></span>

<span data-ttu-id="bd469-108">服務主體名稱 (SPN) 是服務實例的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="bd469-108">A service principal name (SPN) is a unique identifier of a service instance.</span></span> <span data-ttu-id="bd469-109">[Kerberos 驗證](mutual-authentication-using-kerberos.md)會使用 spn，將服務實例與服務登入帳戶建立關聯。</span><span class="sxs-lookup"><span data-stu-id="bd469-109">SPNs are used by [Kerberos authentication](mutual-authentication-using-kerberos.md) to associate a service instance with a service logon account.</span></span> <span data-ttu-id="bd469-110">這可讓用戶端應用程式要求服務驗證帳戶，即使用戶端沒有帳戶名稱也一樣。</span><span class="sxs-lookup"><span data-stu-id="bd469-110">This allows a client application to request that the service authenticate an account even if the client does not have the account name.</span></span>

<span data-ttu-id="bd469-111">若您透過樹系在電腦上安裝多個服務執行個體，則每個執行個體都須有自己的 SPN。</span><span class="sxs-lookup"><span data-stu-id="bd469-111">If you install multiple instances of a service on computers throughout a forest, each instance must have its own SPN.</span></span> <span data-ttu-id="bd469-112">若用戶端需使用多個名稱進行驗證，則指定的服務執行個體可擁有多個 SPN。</span><span class="sxs-lookup"><span data-stu-id="bd469-112">A given service instance can have multiple SPNs if there are multiple names that clients might use for authentication.</span></span> <span data-ttu-id="bd469-113">例如，SPN 一律會包含執行服務實例之主機電腦的名稱，因此服務實例可能會為其主機的每個名稱或別名註冊 SPN。</span><span class="sxs-lookup"><span data-stu-id="bd469-113">For example, an SPN always includes the name of the host computer on which the service instance is running, so a service instance might register an SPN for each name or alias of its host.</span></span> <span data-ttu-id="bd469-114">如需 SPN 格式和撰寫唯一 SPN 的詳細資訊，請參閱 [唯一 spn 的名稱格式](name-formats-for-unique-spns.md)。</span><span class="sxs-lookup"><span data-stu-id="bd469-114">For more information about SPN format and composing a unique SPN, see [Name Formats for Unique SPNs](name-formats-for-unique-spns.md).</span></span>

<span data-ttu-id="bd469-115">在 Kerberos 驗證服務可以使用 SPN 來驗證服務之前，必須先在服務實例用來登入的帳戶物件上註冊 SPN。</span><span class="sxs-lookup"><span data-stu-id="bd469-115">Before the Kerberos authentication service can use an SPN to authenticate a service, the SPN must be registered on the account object that the service instance uses to log on.</span></span> <span data-ttu-id="bd469-116">指定的 SPN 只能在一個帳戶上註冊。</span><span class="sxs-lookup"><span data-stu-id="bd469-116">A given SPN can be registered on only one account.</span></span> <span data-ttu-id="bd469-117">針對 Win32 服務，服務安裝程式會在安裝服務的實例時，指定登入帳戶。</span><span class="sxs-lookup"><span data-stu-id="bd469-117">For Win32 services, a service installer specifies the logon account when an instance of the service is installed.</span></span> <span data-ttu-id="bd469-118">然後，安裝程式會撰寫 Spn，並在 Active Directory Domain Services 中將其寫入為 account 物件的屬性。</span><span class="sxs-lookup"><span data-stu-id="bd469-118">The installer then composes the SPNs and writes them as a property of the account object in Active Directory Domain Services.</span></span> <span data-ttu-id="bd469-119">如果服務實例的登入帳戶變更，必須在新帳戶下重新註冊 Spn。</span><span class="sxs-lookup"><span data-stu-id="bd469-119">If the logon account of a service instance changes, the SPNs must be re-registered under the new account.</span></span> <span data-ttu-id="bd469-120">如需詳細資訊，請參閱 [服務如何註冊其 spn](how-a-service-registers-its-spns.md)。</span><span class="sxs-lookup"><span data-stu-id="bd469-120">For more information, see [How a Service Registers its SPNs](how-a-service-registers-its-spns.md).</span></span>

<span data-ttu-id="bd469-121">當用戶端想要連接到服務時，它會尋找服務的執行個體、撰寫該執行個體的 SPN、連接到服務，然後呈現服務的 SPN 以進行驗證。</span><span class="sxs-lookup"><span data-stu-id="bd469-121">When a client wants to connect to a service, it locates an instance of the service, composes an SPN for that instance, connects to the service, and presents the SPN for the service to authenticate.</span></span> <span data-ttu-id="bd469-122">如需詳細資訊，請參閱 [用戶端如何撰寫服務的 SPN](how-clients-compose-a-serviceampaposs-spn.md)。</span><span class="sxs-lookup"><span data-stu-id="bd469-122">For more information, see [How Clients Compose a Service's SPN](how-clients-compose-a-serviceampaposs-spn.md).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="bd469-123">本章節內容</span><span class="sxs-lookup"><span data-stu-id="bd469-123">In this Section</span></span>

## <a name="in-this-section"></a><span data-ttu-id="bd469-124">本節內容</span><span class="sxs-lookup"><span data-stu-id="bd469-124">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="bd469-125">唯一 Spn 的名稱格式</span><span class="sxs-lookup"><span data-stu-id="bd469-125">Name Formats for Unique SPNs</span></span>](name-formats-for-unique-spns.md)
</dt> <dt>

[<span data-ttu-id="bd469-126">服務如何撰寫其 Spn</span><span class="sxs-lookup"><span data-stu-id="bd469-126">How a Service Composes its SPNs</span></span>](how-a-service-composes-its-spns.md)
</dt> <dt>

[<span data-ttu-id="bd469-127">服務如何註冊其 Spn</span><span class="sxs-lookup"><span data-stu-id="bd469-127">How a Service Registers its SPNs</span></span>](how-a-service-registers-its-spns.md)
</dt> <dt>

[<span data-ttu-id="bd469-128">用戶端如何撰寫服務的 SPN</span><span class="sxs-lookup"><span data-stu-id="bd469-128">How Clients Compose a Service's SPN</span></span>](how-clients-compose-a-serviceampaposs-spn.md)
</dt> </dl>

## <a name="related-topics"></a><span data-ttu-id="bd469-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="bd469-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bd469-130">什麼是 SPN，為什麼您應該在意？</span><span class="sxs-lookup"><span data-stu-id="bd469-130">What is an SPN and why should you care?</span></span>](/archive/blogs/autz_auth_stuff/what-is-a-spn-and-why-should-you-care)
</dt> <dt>

[<span data-ttu-id="bd469-131">使用 Kerberos 進行相互驗證</span><span class="sxs-lookup"><span data-stu-id="bd469-131">Mutual Authentication Using Kerberos</span></span>](mutual-authentication-using-kerberos.md)
</dt> </dl>

 

 
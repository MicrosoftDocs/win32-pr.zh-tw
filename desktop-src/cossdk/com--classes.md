---
description: 以下是 COM + 類別。
ms.assetid: 236725f6-16a3-4209-a9e3-a127c1d7243a
title: COM + 類別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 626c3dfdae542b602cf27a8d8be5cb69dde5910f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111685"
---
# <a name="com-classes"></a><span data-ttu-id="87d12-103">COM + 類別</span><span class="sxs-lookup"><span data-stu-id="87d12-103">COM+ Classes</span></span>

<span data-ttu-id="87d12-104">以下是 COM + 類別。</span><span class="sxs-lookup"><span data-stu-id="87d12-104">The following are the COM+ classes.</span></span>



| <span data-ttu-id="87d12-105">類別</span><span class="sxs-lookup"><span data-stu-id="87d12-105">Class</span></span>                                                            | <span data-ttu-id="87d12-106">描述</span><span class="sxs-lookup"><span data-stu-id="87d12-106">Description</span></span>                                                                                                                                                                                                                             |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="87d12-107">**AppDomainHelper**</span><span class="sxs-lookup"><span data-stu-id="87d12-107">**AppDomainHelper**</span></span>](appdomainhelper.md)                       | <span data-ttu-id="87d12-108">將 managed 物件系結至應用程式域，也就是應用程式執行所在的隔離環境。</span><span class="sxs-lookup"><span data-stu-id="87d12-108">Binds a managed object to an application domain, which is an isolated environment where applications execute.</span></span>                                                                                                                           |
| [<span data-ttu-id="87d12-109">**ClrAssemblyLocator**</span><span class="sxs-lookup"><span data-stu-id="87d12-109">**ClrAssemblyLocator**</span></span>](clrassemblylocator.md)                 | <span data-ttu-id="87d12-110">使用 .NET Framework common language runtime 中的 managed 程式碼時，捕獲元件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="87d12-110">Retrieves information about an assembly when using managed code in the .NET Framework common language runtime.</span></span>                                                                                                                          |
| [<span data-ttu-id="87d12-111">**CServiceConfig**</span><span class="sxs-lookup"><span data-stu-id="87d12-111">**CServiceConfig**</span></span>](cserviceconfig.md)                         | <span data-ttu-id="87d12-112">指定和設定在呼叫 [**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) 或 [**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain)時所輸入的服務網域中要使用的服務。</span><span class="sxs-lookup"><span data-stu-id="87d12-112">Specifies and configures the services that are to be active in the service domain entered when calling either [**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) or [**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain).</span></span>                     |
| [<span data-ttu-id="87d12-113">**SecurityCallCoNtext**</span><span class="sxs-lookup"><span data-stu-id="87d12-113">**SecurityCallContext**</span></span>](securitycallcontext.md)               | <span data-ttu-id="87d12-114">提供存取目前呼叫的安全性內容，其中包含物件呼叫端的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="87d12-114">Provides access to the current call's security context, which contains information about an object's callers.</span></span>                                                                                                                           |
| [<span data-ttu-id="87d12-115">**SecurityCallers**</span><span class="sxs-lookup"><span data-stu-id="87d12-115">**SecurityCallers**</span></span>](securitycallers.md)                       | <span data-ttu-id="87d12-116">提供呼叫端集合中個別呼叫端的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="87d12-116">Provides access to information about individual callers in a collection of callers.</span></span> <span data-ttu-id="87d12-117">集合代表以目前呼叫結尾的呼叫鏈，而集合中的每個呼叫端都代表一個呼叫端的身分識別。</span><span class="sxs-lookup"><span data-stu-id="87d12-117">The collection represents the chain of calls ending with the current call, and each caller in the collection represents the identity of one caller.</span></span> |
| [<span data-ttu-id="87d12-118">**SecurityIdentity**</span><span class="sxs-lookup"><span data-stu-id="87d12-118">**SecurityIdentity**</span></span>](securityidentity.md)                     | <span data-ttu-id="87d12-119">提供安全性資訊集合的存取，代表呼叫者的身分識別。</span><span class="sxs-lookup"><span data-stu-id="87d12-119">Provides access to a collection of security information representing a caller's identity.</span></span> <span data-ttu-id="87d12-120">使用這個類別，您可以在屬於安全性呼叫內容一部分的呼叫端中找出特定的呼叫端。</span><span class="sxs-lookup"><span data-stu-id="87d12-120">Using this class, you can find out about a particular caller in a chain of callers that is part of the security call context.</span></span>                 |
| [<span data-ttu-id="87d12-121">**SharedProperty**</span><span class="sxs-lookup"><span data-stu-id="87d12-121">**SharedProperty**</span></span>](sharedproperty.md)                         | <span data-ttu-id="87d12-122">設定或抓取共用屬性的值。</span><span class="sxs-lookup"><span data-stu-id="87d12-122">Sets or retrieves the value of a shared property.</span></span>                                                                                                                                                                                       |
| [<span data-ttu-id="87d12-123">**SharedPropertyGroup**</span><span class="sxs-lookup"><span data-stu-id="87d12-123">**SharedPropertyGroup**</span></span>](sharedpropertygroup.md)               | <span data-ttu-id="87d12-124">建立並存取共用屬性群組中的共用屬性。</span><span class="sxs-lookup"><span data-stu-id="87d12-124">Creates and accesses the shared properties in a shared property group.</span></span>                                                                                                                                                                  |
| [<span data-ttu-id="87d12-125">**SharedPropertyGroupManager**</span><span class="sxs-lookup"><span data-stu-id="87d12-125">**SharedPropertyGroupManager**</span></span>](sharedpropertygroupmanager.md) | <span data-ttu-id="87d12-126">建立共用屬性群組，並取得現有共用屬性群組的存取權。</span><span class="sxs-lookup"><span data-stu-id="87d12-126">Creates shared property groups and to obtain access to existing shared property groups.</span></span>                                                                                                                                                 |
| [<span data-ttu-id="87d12-127">**TransactionCoNtext**</span><span class="sxs-lookup"><span data-stu-id="87d12-127">**TransactionContext**</span></span>](transactioncontext.md)                 | <span data-ttu-id="87d12-128">建立可開始交易的泛型交易式物件。</span><span class="sxs-lookup"><span data-stu-id="87d12-128">Creates a generic transactional object that begins a transaction.</span></span>                                                                                                                                                                       |
| [<span data-ttu-id="87d12-129">**TransactionCoNtextEx**</span><span class="sxs-lookup"><span data-stu-id="87d12-129">**TransactionContextEx**</span></span>](transactioncontextex.md)             | <span data-ttu-id="87d12-130">建立可開始交易的泛型交易式物件。</span><span class="sxs-lookup"><span data-stu-id="87d12-130">Creates a generic transactional object that begins a transaction.</span></span> <span data-ttu-id="87d12-131">藉由呼叫這個類別的方法，您可以在單一交易中撰寫多個 COM 物件的工作，並明確地認可或中止交易。</span><span class="sxs-lookup"><span data-stu-id="87d12-131">By calling the methods of this class, you can compose the work of multiple COM objects in a single transaction and explicitly commit or abort the transaction.</span></span>        |



 

 

 




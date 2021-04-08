---
title: 使用服務連接點發佈
description: Active Directory 架構會定義 serviceConnectionPoint (SCP) 物件類別，讓服務能夠輕鬆地將服務特定的資料發佈到目錄中。
ms.assetid: 3544aa64-ecb0-48a1-ae49-05247a983842
ms.tgt_platform: multiple
keywords:
- 使用服務連接點發佈 AD
- 服務連接點廣告
- 服務連接點廣告，發佈方式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a458822f6c5e4d764b2e330c7ba084021b586548
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671251"
---
# <a name="publishing-with-service-connection-points"></a><span data-ttu-id="c43ab-106">使用服務連接點發佈</span><span class="sxs-lookup"><span data-stu-id="c43ab-106">Publishing with Service Connection Points</span></span>

<span data-ttu-id="c43ab-107">Active Directory 架構會定義 **serviceConnectionPoint** (SCP) 物件類別，讓服務能夠輕鬆地將服務特定的資料發佈到目錄中。</span><span class="sxs-lookup"><span data-stu-id="c43ab-107">The Active Directory Schema defines a **serviceConnectionPoint** (SCP) object class to make it easy for a service to publish service-specific data in the directory.</span></span> <span data-ttu-id="c43ab-108">服務的用戶端會使用 SCP 中的資料來尋找、連接及驗證您的服務實例。</span><span class="sxs-lookup"><span data-stu-id="c43ab-108">Clients of the service use the data in an SCP to locate, connect to, and authenticate an instance of your service.</span></span>

<span data-ttu-id="c43ab-109">本節提供服務連接點和程式碼範例的總覽，說明用戶端/服務應用程式如何使用 Scp。</span><span class="sxs-lookup"><span data-stu-id="c43ab-109">This section provides an overview of service connection points and code examples that show how a client/service application uses SCPs.</span></span>

<span data-ttu-id="c43ab-110">程式碼範例會遵循下列步驟來使用 Scp 來執行服務發行。</span><span class="sxs-lookup"><span data-stu-id="c43ab-110">The code example follows these steps to implement service publication with SCPs.</span></span>

<span data-ttu-id="c43ab-111">如需執行這些步驟的詳細資訊和程式碼範例，請參閱 [建立服務連接點](creating-a-service-connection-point.md)。</span><span class="sxs-lookup"><span data-stu-id="c43ab-111">For more information and a code example that performs these steps, see [Creating a Service Connection Point](creating-a-service-connection-point.md).</span></span>

<span data-ttu-id="c43ab-112">**在服務安裝的目錄中建立 Scp**</span><span class="sxs-lookup"><span data-stu-id="c43ab-112">**To create SCPs in the directory at service installation**</span></span>

1.  <span data-ttu-id="c43ab-113">系結至已安裝服務實例之主機電腦的電腦物件。</span><span class="sxs-lookup"><span data-stu-id="c43ab-113">Bind to the computer object for the host computer on which the service instance is installed.</span></span>
2.  <span data-ttu-id="c43ab-114">建立 SCP 物件做為電腦物件的子系，並指定 SCP 屬性的初始值。</span><span class="sxs-lookup"><span data-stu-id="c43ab-114">Create an SCP object as a child of the computer object, specifying the initial values for the attributes of the SCP.</span></span>
3.  <span data-ttu-id="c43ab-115">在 SCP 物件的安全描述項中，將存取控制專案設定 (Ace) ，讓服務在執行時間修改 SCP 屬性。</span><span class="sxs-lookup"><span data-stu-id="c43ab-115">Set access control entries (ACEs) in the security descriptor of the SCP object to enable the service to modify SCP properties at run time.</span></span>
4.  <span data-ttu-id="c43ab-116">在服務主機電腦上的登錄中快取 SCP 的 **objectGUID** 。</span><span class="sxs-lookup"><span data-stu-id="c43ab-116">Cache the **objectGUID** of the SCP in the registry on the service's host computer.</span></span>

<span data-ttu-id="c43ab-117">如需執行這些步驟的詳細資訊和程式碼範例，請參閱 [更新服務連接點](updating-a-service-connection-point.md)。</span><span class="sxs-lookup"><span data-stu-id="c43ab-117">For more information and a code example that performs these steps, see [Updating a Service Connection Point](updating-a-service-connection-point.md).</span></span>

<span data-ttu-id="c43ab-118">**在服務啟動時更新 SCP 屬性**</span><span class="sxs-lookup"><span data-stu-id="c43ab-118">**To update the SCP attributes at service startup**</span></span>

1.  <span data-ttu-id="c43ab-119">從登錄取出 **objectGUID** ，並用它來系結至 SCP。</span><span class="sxs-lookup"><span data-stu-id="c43ab-119">Retrieve the **objectGUID** from the registry and use it to bind to the SCP.</span></span>
2.  <span data-ttu-id="c43ab-120">從 SCP 取出屬性，例如 **serviceDNSName** 和 **serviceBindingInformation**。</span><span class="sxs-lookup"><span data-stu-id="c43ab-120">Retrieve attributes, such as **serviceDNSName** and **serviceBindingInformation**, from the SCP.</span></span> <span data-ttu-id="c43ab-121">將這些值與目前的值相比較，並視需要更新 SCP。</span><span class="sxs-lookup"><span data-stu-id="c43ab-121">Compare these values to the current values and update the SCP if necessary.</span></span>

<span data-ttu-id="c43ab-122">如需執行這些步驟的詳細資訊和程式碼範例，請參閱 [用戶端如何尋找和使用服務連接點](how-clients-find-and-use-a-service-connection-point.md)。</span><span class="sxs-lookup"><span data-stu-id="c43ab-122">For more information and a code example that performs these steps, see [How Clients Find and Use a Service Connection Point](how-clients-find-and-use-a-service-connection-point.md).</span></span>

<span data-ttu-id="c43ab-123">**若要透過用戶端應用程式尋找並使用 SCP**</span><span class="sxs-lookup"><span data-stu-id="c43ab-123">**To find and use an SCP by a client application**</span></span>

1.  <span data-ttu-id="c43ab-124">系結至通用類別目錄，並搜尋具有符合服務產品 GUID 之 **關鍵字** 屬性的物件。</span><span class="sxs-lookup"><span data-stu-id="c43ab-124">Bind to the Global Catalog and search for objects with a **keywords** attribute that matches the service's product GUID.</span></span> <span data-ttu-id="c43ab-125">每個找到的物件都是服務的實例。</span><span class="sxs-lookup"><span data-stu-id="c43ab-125">Each object found is an instance of the service.</span></span> <span data-ttu-id="c43ab-126">選取實例並取出 SCP 的分辨名稱。</span><span class="sxs-lookup"><span data-stu-id="c43ab-126">Select an instance and retrieve the distinguished name of the SCP.</span></span>
2.  <span data-ttu-id="c43ab-127">使用該辨別名稱來繫結到 SCP。</span><span class="sxs-lookup"><span data-stu-id="c43ab-127">Use the distinguished name to bind to the SCP.</span></span>
3.  <span data-ttu-id="c43ab-128">從 SCP 取出各種屬性的值，例如 **serviceDNSName** 和 **serviceBindingInformation**。</span><span class="sxs-lookup"><span data-stu-id="c43ab-128">Retrieve the values of various attributes from the SCP, such as **serviceDNSName** and **serviceBindingInformation**.</span></span> <span data-ttu-id="c43ab-129">使用這些值連線到服務執行個體並向其驗證。</span><span class="sxs-lookup"><span data-stu-id="c43ab-129">Use these values to connect to and authenticate the service instance.</span></span>

<span data-ttu-id="c43ab-130">如需有關哪些角色可以建立及更新 SCP 的詳細資訊，請參閱 [服務發行的安全性問題](security-issues-for-service-publication.md)。</span><span class="sxs-lookup"><span data-stu-id="c43ab-130">For more information about what roles can create and update an SCP, see [Security Issues for Service Publication](security-issues-for-service-publication.md).</span></span>

<span data-ttu-id="c43ab-131">如需有關如何建立 SCP 的詳細資訊，請參閱 [建立服務連接點的位置](where-to-create-a-service-connection-point.md)。</span><span class="sxs-lookup"><span data-stu-id="c43ab-131">For more information about where to create an SCP, see [Where to Create a Service Connection Point](where-to-create-a-service-connection-point.md).</span></span>

<span data-ttu-id="c43ab-132">如需在 SCP 中儲存之資料類型的詳細資訊，請參閱 [服務連接點屬性](service-connection-point-properties.md)。</span><span class="sxs-lookup"><span data-stu-id="c43ab-132">For more information about the kind of data to store in an SCP, see [Service Connection Point Properties](service-connection-point-properties.md).</span></span>

<span data-ttu-id="c43ab-133">如需有關服務安裝程式和服務如何一起運作以維護 SCP 中目前資料的詳細資訊，請參閱 [建立和維護服務連接點](creating-and-maintaining-a-service-connection-point.md)。</span><span class="sxs-lookup"><span data-stu-id="c43ab-133">For more information about how a service installer and the service work together to maintain current data in an SCP, see [Creating and Maintaining a Service Connection Point](creating-and-maintaining-a-service-connection-point.md).</span></span>

 

 





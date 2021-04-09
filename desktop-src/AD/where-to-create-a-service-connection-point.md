---
title: 建立服務連接點的位置
description: 當安裝 Active Directory Domain Services 的實例時，服務安裝程式會在 Active Directory Domain Services 中 (SCP) 建立服務連接點物件。
ms.assetid: a90566d9-dd68-43e2-be9e-300d57a7fbf4
ms.tgt_platform: multiple
keywords:
- 何處可以建立服務連接點 AD
- active directory，在何處建立服務連接點
- 何處可以建立服務連接點 AD
- 建立服務連接點 AD
- 服務連接點 AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf122ebabcfd8085ebad46314ffd1c09f827e783
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020819"
---
# <a name="where-to-create-a-service-connection-point"></a><span data-ttu-id="588ff-108">建立服務連接點的位置</span><span class="sxs-lookup"><span data-stu-id="588ff-108">Where to Create a Service Connection Point</span></span>

<span data-ttu-id="588ff-109">當安裝 Active Directory Domain Services 的實例時，服務安裝程式會在 Active Directory Domain Services 中 (SCP) 建立服務連接點物件。</span><span class="sxs-lookup"><span data-stu-id="588ff-109">When an instance of Active Directory Domain Services is installed, the service installer creates service connection point objects (SCP) in Active Directory Domain Services.</span></span> <span data-ttu-id="588ff-110">主要目標應該是將複寫流量降到最低，並啟用物件的有效率管理和維護。</span><span class="sxs-lookup"><span data-stu-id="588ff-110">The primary objective should be to minimize replication traffic and to enable efficient administration and maintenance of objects.</span></span>

<span data-ttu-id="588ff-111">請注意，用戶端應用程式會搜尋 SCP 中關鍵字的目錄來尋找 Scp。</span><span class="sxs-lookup"><span data-stu-id="588ff-111">Be aware that client applications find SCPs by searching the directory for keywords in the SCP.</span></span> <span data-ttu-id="588ff-112">SCP 的 **關鍵字** 屬性包含在通用類別目錄中;用戶端可以搜尋通用類別目錄，以在樹系中尋找 Scp。</span><span class="sxs-lookup"><span data-stu-id="588ff-112">The **keywords** attribute of an SCP is included in the Global Catalog; clients can search the Global Catalog to find SCPs in the forest.</span></span> <span data-ttu-id="588ff-113">基於這個理由，用戶端並不會影響發佈 Scp 的位置。</span><span class="sxs-lookup"><span data-stu-id="588ff-113">For this reason, the client does not influence where to publish SCPs.</span></span>

## <a name="minimize-replication-traffic"></a><span data-ttu-id="588ff-114">最小化複寫流量</span><span class="sxs-lookup"><span data-stu-id="588ff-114">Minimize Replication Traffic</span></span>

<span data-ttu-id="588ff-115">若要將複寫流量降到最低，請在服務主機電腦之網域的網域分割區中建立 Scp。</span><span class="sxs-lookup"><span data-stu-id="588ff-115">To minimize replication traffic, create SCPs in the domain partition of the domain of the service host computer.</span></span> <span data-ttu-id="588ff-116">例如，您可以將 Scp 建立為安裝服務之電腦物件的子物件。</span><span class="sxs-lookup"><span data-stu-id="588ff-116">For example, you can create SCPs as child objects of the computer object on which the service is installed.</span></span> <span data-ttu-id="588ff-117">Active Directory Domain Services 的網域分割（有時也稱為網域命名內容）包含網域特定物件，例如網域的使用者和電腦的物件。</span><span class="sxs-lookup"><span data-stu-id="588ff-117">A domain partition of Active Directory Domain Services, sometimes called a domain naming context, contains domain-specific objects such as the objects for the users and computers of the domain.</span></span> <span data-ttu-id="588ff-118">網域分割區中所有物件的完整複本會複寫到網域的每個網域控制站 (DC) ，但不會複寫到其他網域的 Dc。</span><span class="sxs-lookup"><span data-stu-id="588ff-118">A full replica of all objects in the domain partition is replicated to every domain controller (DC) for the domain, but it is not replicated to DCs of other domains.</span></span>

<span data-ttu-id="588ff-119">請勿在設定磁碟分割（也稱為設定命名內容）中建立 Scp，因為設定磁碟分割的變更會複寫到樹系中的每個 DC。</span><span class="sxs-lookup"><span data-stu-id="588ff-119">Do not create SCPs in the Configuration partition, also known as the configuration naming context, because changes to the Configuration partition are replicated to every DC in the forest.</span></span> <span data-ttu-id="588ff-120">如上所述，整個樹系中的用戶端都可以查詢通用類別目錄來尋找樹系中任何位置的 Scp，因此在設定分割區中建立 Scp 並不會讓用戶端看見它們。它只會產生更多的複寫流量。</span><span class="sxs-lookup"><span data-stu-id="588ff-120">As noted above, clients throughout the forest can query the Global Catalog to find SCPs anywhere in the forest, so creating SCPs in the Configuration partition does not make them more visible to clients; it only generates more replication traffic.</span></span>

## <a name="ease-of-administration"></a><span data-ttu-id="588ff-121">易於管理</span><span class="sxs-lookup"><span data-stu-id="588ff-121">Ease of Administration</span></span>

<span data-ttu-id="588ff-122">針對物件管理，請考慮下列指導方針：</span><span class="sxs-lookup"><span data-stu-id="588ff-122">Consider the following guidelines for object administration:</span></span>

-   <span data-ttu-id="588ff-123">使用原則和繼承存取權限，來放置系統管理員可以控制其存取權的特定服務物件。</span><span class="sxs-lookup"><span data-stu-id="588ff-123">Place service-specific objects where administrators can control access to them using policy and inherited access permissions.</span></span>
-   <span data-ttu-id="588ff-124">將物件放在系統管理員可以輕鬆找到這些物件的位置。</span><span class="sxs-lookup"><span data-stu-id="588ff-124">Place the objects in where an administrator can easily find them.</span></span>

<span data-ttu-id="588ff-125">符合這兩個目標的良好預設位置是在每個服務實例主機電腦的電腦物件下建立 SCP 和其他服務特定物件。</span><span class="sxs-lookup"><span data-stu-id="588ff-125">A good default location that satisfies both goals is to create SCP and other service-specific objects under the computer object of the host computer of each service instance.</span></span> <span data-ttu-id="588ff-126">如需詳細資訊，請參閱 [在電腦物件下發行](publishing-under-a-computer-object.md)。</span><span class="sxs-lookup"><span data-stu-id="588ff-126">For more information, see [Publishing Under a Computer Object](publishing-under-a-computer-object.md).</span></span>

<span data-ttu-id="588ff-127">針對未系結至單一主機的服務，最好的替代方法是在網域分割區的系統容器底下建立服務物件的容器。</span><span class="sxs-lookup"><span data-stu-id="588ff-127">A good alternative for services not tied to a single host is to create a container for the service objects under the System container in a domain partition.</span></span> <span data-ttu-id="588ff-128">如需詳細資訊，請參閱 [在網域系統容器中發行](publishing-in-a-domain-system-container.md)。</span><span class="sxs-lookup"><span data-stu-id="588ff-128">For more information, see [Publishing in a Domain System Container](publishing-in-a-domain-system-container.md).</span></span>

<span data-ttu-id="588ff-129">下圖顯示網域分割的部分預設容器階層。</span><span class="sxs-lookup"><span data-stu-id="588ff-129">The following diagram shows part of the default container hierarchy for a domain partition.</span></span>

![預設網域分割容器階層](images/domain-container-heirarchy.png)

<span data-ttu-id="588ff-131">下圖顯示 Active Directory Domain Services 包含的預設網域階層。</span><span class="sxs-lookup"><span data-stu-id="588ff-131">The diagram shows the default domain hierarchy included with Active Directory Domain Services.</span></span> <span data-ttu-id="588ff-132">不過，許多企業會建立組織單位的階層， (OU) 容器來將物件類別（例如使用者和電腦）組成群組，以供管理之用。</span><span class="sxs-lookup"><span data-stu-id="588ff-132">However, many enterprises create a hierarchy of organizational unit (OU) containers to group object classes, such as users and computers, together for purposes of administration.</span></span> <span data-ttu-id="588ff-133">然後，系統管理員可以將原則和可繼承的存取控制專案 (Ace) 套用至 OU，以委派 OU 中物件的系統管理授權。</span><span class="sxs-lookup"><span data-stu-id="588ff-133">Administrators can then apply policy and inheritable access-control entries (ACEs) to an OU to delegate administrative authority for objects in the OU.</span></span> <span data-ttu-id="588ff-134">這可讓系統管理員有效率地管理企業，但對於服務程式設計人員有一些結果：</span><span class="sxs-lookup"><span data-stu-id="588ff-134">This enables administrators to efficiently manage an enterprise, but it has a few consequences for service programmers:</span></span>

-   <span data-ttu-id="588ff-135">服務主機的電腦物件可能不在 [電腦] 容器底下，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="588ff-135">The computer object for a service host might not be under the Computers container as shown in the diagram.</span></span> <span data-ttu-id="588ff-136">如需有關如何尋找本機電腦之電腦物件的詳細資訊，請參閱 [在電腦物件下發布](publishing-under-a-computer-object.md)。</span><span class="sxs-lookup"><span data-stu-id="588ff-136">For more information about how to find the computer object for the local computer, see [Publishing Under a Computer Object](publishing-under-a-computer-object.md).</span></span>
-   <span data-ttu-id="588ff-137">系統管理員可以在組織需要變更時移動物件。</span><span class="sxs-lookup"><span data-stu-id="588ff-137">Administrators may move objects as their organizational needs change.</span></span> <span data-ttu-id="588ff-138">這表示您無法依賴固定位置中剩餘的物件;也就是說，您的服務無法依賴剩餘的物件辨別名稱。</span><span class="sxs-lookup"><span data-stu-id="588ff-138">This means that you cannot depend on your objects remaining in a fixed location; that is, your service cannot depend on an object distinguished name remaining the same.</span></span> <span data-ttu-id="588ff-139">相反地，請使用物件的 **objectGUID** 屬性，如果物件已移動或重新命名，則不會變更。</span><span class="sxs-lookup"><span data-stu-id="588ff-139">Instead, use an object's **objectGUID** attribute, which does not change if the object is moved or renamed.</span></span> <span data-ttu-id="588ff-140">如需詳細資訊，以及建立 SCP 的程式碼範例，請儲存其 **objectguid**，並于稍後抓取要系結至 SCP 的 **objectguid** ，請參閱 [建立和維護服務連接點](creating-and-maintaining-a-service-connection-point.md)。</span><span class="sxs-lookup"><span data-stu-id="588ff-140">For more information, and a code example that creates an SCP, stores its **objectGUID**, and later retrieves the **objectGUID** to bind to the SCP, see [Creating and Maintaining a Service Connection Point](creating-and-maintaining-a-service-connection-point.md).</span></span>
-   <span data-ttu-id="588ff-141">所有標準服務相關的物件類別以及這些類別的任何子類別，都是 **電腦** 和 **organizationalUnit** 類別的有效子系。</span><span class="sxs-lookup"><span data-stu-id="588ff-141">All of the standard service-related object classes, as well as any subclasses of these classes, are valid children of the **computer** and **organizationalUnit** classes.</span></span> <span data-ttu-id="588ff-142">如果您延伸架構來定義您自己的服務專屬類別，請確定 **電腦** 和 **organizationalUnit** 類別都包含在可能的 superiors 中。</span><span class="sxs-lookup"><span data-stu-id="588ff-142">If you extend the schema to define your own service-specific class, be sure that the **computer** and **organizationalUnit** classes are included in the possible superiors.</span></span>
-   <span data-ttu-id="588ff-143">服務安裝程式會決定用來建立 Scp 的預設位置。</span><span class="sxs-lookup"><span data-stu-id="588ff-143">The service installer determines the default location for creating SCPs.</span></span> <span data-ttu-id="588ff-144">您可能會想要允許安裝服務的系統管理員指定替代的安裝路徑。</span><span class="sxs-lookup"><span data-stu-id="588ff-144">You may want to allow the administrator installing the service to specify an alternate install path.</span></span>

<span data-ttu-id="588ff-145">不應該在下欄區域中建立服務特定物件：</span><span class="sxs-lookup"><span data-stu-id="588ff-145">Service-specific objects should not be created in the following areas:</span></span>

-   <span data-ttu-id="588ff-146">服務不應該直接在網域分割區的 [使用者] 或 [電腦] 容器中發佈物件，也不應該在這些容器中建立新的容器。</span><span class="sxs-lookup"><span data-stu-id="588ff-146">Services should not publish objects directly in the Users or Computers containers of a domain partition, nor should they create new containers in these containers.</span></span> <span data-ttu-id="588ff-147">不過，無論電腦物件是否儲存在 [電腦] 容器中，服務都可以將物件發佈為電腦物件的子物件。</span><span class="sxs-lookup"><span data-stu-id="588ff-147">However, services can publish objects as child objects of a computer object, whether or not the computer object is stored in the Computers container.</span></span>
-   <span data-ttu-id="588ff-148">使用 Windows 通訊端註冊和解析 (RnR) 或 RPC 名稱服務的服務， (RpcNs) Api 來通告本身，請在 WinsockServices 和 RpcServices 容器的網域分割區系統容器底下建立適當的物件。</span><span class="sxs-lookup"><span data-stu-id="588ff-148">Services, that use Windows Sockets registration and resolution (RnR) or the RPC name service (RpcNs) APIs to advertise themselves, create the proper objects in the WinsockServices and RpcServices containers under a domain partition's System container.</span></span> <span data-ttu-id="588ff-149">請勿在這些容器中明確建立物件。</span><span class="sxs-lookup"><span data-stu-id="588ff-149">Do not explicitly create objects in these containers.</span></span> <span data-ttu-id="588ff-150">這樣做並不會造成直接損害，但對系統管理員來說可能會造成混淆。</span><span class="sxs-lookup"><span data-stu-id="588ff-150">Doing so does not cause direct harm, but may be confusing for administrators.</span></span>

 

 





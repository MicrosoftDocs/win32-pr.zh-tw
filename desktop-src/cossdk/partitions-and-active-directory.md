---
description: 除了包含一或多個應用程式的資料分割之外，COM + 也包含資料分割集，其中包含一或多個資料分割。
ms.assetid: 0b1a6daa-55e1-4a74-be01-e39473e3c0cc
title: 磁碟分割和 Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b08e7b70c4b474e7b7bd949f530fb73973d39c6a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973967"
---
# <a name="partitions-and-active-directory"></a><span data-ttu-id="b4d00-103">磁碟分割和 Active Directory</span><span class="sxs-lookup"><span data-stu-id="b4d00-103">Partitions and Active Directory</span></span>

<span data-ttu-id="b4d00-104">除了包含一或多個應用程式的資料分割之外，COM + 也包含資料 *分割集*，其中包含一或多個資料分割。</span><span class="sxs-lookup"><span data-stu-id="b4d00-104">In addition to partitions, which contain one or more applications, COM+ also includes *partition sets*, which contain one or more partitions.</span></span> <span data-ttu-id="b4d00-105">在 Active Directory 中建立的資料分割集會讓網域中的使用者存取整個網域的 COM + 應用程式。</span><span class="sxs-lookup"><span data-stu-id="b4d00-105">Created in Active Directory, partition sets allow users in a domain to access COM+ applications throughout the domain.</span></span> <span data-ttu-id="b4d00-106">在建立期間，會將每個特定的使用者或組織單位 (OU) 指派或對應至資料分割集。</span><span class="sxs-lookup"><span data-stu-id="b4d00-106">During creation, each specific user or organizational unit (OU) is assigned, or mapped, to a partition set.</span></span>

<span data-ttu-id="b4d00-107">單一使用者或 OU 可以存取多個分割區和其應用程式，因為使用者身分識別或 OU 與分割集之間有一對一的相互關聯。</span><span class="sxs-lookup"><span data-stu-id="b4d00-107">A single user or OU can access multiple partitions and their applications because there is a one-to-one correlation between a user identity or OU and a partition set.</span></span> <span data-ttu-id="b4d00-108">如果沒有分割集，使用者或 OU 就需要多個使用者身分識別，才能存取不同分割區中的應用程式。</span><span class="sxs-lookup"><span data-stu-id="b4d00-108">Without a partition set, a user or OU would need multiple user identities to access applications in different partitions.</span></span>

<span data-ttu-id="b4d00-109">若要讓網域使用者可以使用 COM + 應用程式，系統管理員必須在 Active Directory 所在的網域控制站上，以及已安裝 COM + 應用程式的伺服器上執行工作。</span><span class="sxs-lookup"><span data-stu-id="b4d00-109">To make COM+ applications available to domain users, an administrator must perform tasks both on the domain controller where Active Directory resides and on the server where the COM+ application is installed.</span></span>

## <a name="on-the-domain-controller"></a><span data-ttu-id="b4d00-110">在網域控制站上</span><span class="sxs-lookup"><span data-stu-id="b4d00-110">On the Domain Controller</span></span>

<span data-ttu-id="b4d00-111">系統管理員會先在 Active Directory 中建立磁碟分割。</span><span class="sxs-lookup"><span data-stu-id="b4d00-111">The administrator first creates a partition within Active Directory.</span></span> <span data-ttu-id="b4d00-112">您可以透過使用 Active Directory 消費者和電腦系統管理工具，或使用 Active Directory Services 介面 (ADSI) ，以程式設計方式來建立 COM + 分割。</span><span class="sxs-lookup"><span data-stu-id="b4d00-112">Creating a COM+ partition is done either through the use of the Active Directory Users and Computers administrative tool or programmatically by using the Active Directory Services Interface (ADSI).</span></span>

<span data-ttu-id="b4d00-113">在 Active Directory 中建立分割區之後，系統管理員會建立分割集。</span><span class="sxs-lookup"><span data-stu-id="b4d00-113">After the partition has been created within Active Directory, the administrator then creates a partition set.</span></span> <span data-ttu-id="b4d00-114">在建立資料分割集時，系統管理員會定義該集合中包含的資料分割。</span><span class="sxs-lookup"><span data-stu-id="b4d00-114">In creating a partition set, the administrator defines the partitions that are included in that set.</span></span> <span data-ttu-id="b4d00-115">建立 COM + 分割集的方法是透過使用 Active Directory 消費者和電腦系統管理工具，或使用 (ADSI) 的 Active Directory Services 介面以程式設計方式進行。</span><span class="sxs-lookup"><span data-stu-id="b4d00-115">Creating a COM+ partition set is done either through the use of the Active Directory Users and Computers administrative tool or programmatically by using the Active Directory Services Interface (ADSI).</span></span>

<span data-ttu-id="b4d00-116">最後，系統管理員會將網域使用者或組織單位 (Ou) 對應到新建立的資料分割集。</span><span class="sxs-lookup"><span data-stu-id="b4d00-116">Finally, the administrator maps domain users or organizational units (OUs) to the newly created partition set.</span></span> <span data-ttu-id="b4d00-117">這是藉由顯示使用者的 [ **屬性** ] 頁面、存取 [ **Com + 資料分割集** ] 索引標籤，然後從清單方塊中選取資料分割集來完成。</span><span class="sxs-lookup"><span data-stu-id="b4d00-117">This is done by displaying a user's **Properties** page, accessing the **COM+ Partition Sets** tab, and selecting a partition set from the list box.</span></span>

## <a name="on-the-com-application-server"></a><span data-ttu-id="b4d00-118">在 COM + 應用程式伺服器上</span><span class="sxs-lookup"><span data-stu-id="b4d00-118">On the COM+ Application Server</span></span>

<span data-ttu-id="b4d00-119">系統管理員會建立新的磁碟分割，並指定相同的分割區名稱和資料分割識別碼 (GUID) 與在網域控制站 Active Directory 內建立的分割區識別碼相同。</span><span class="sxs-lookup"><span data-stu-id="b4d00-119">The administrator creates a new partition, specifying the same partition name and partition ID (GUID) as that of the partition that was created within Active Directory on the domain controller.</span></span> <span data-ttu-id="b4d00-120">這是使用 [元件服務] 系統管理工具內的 [ **Com + 磁碟分割** ] 資料夾來完成的。</span><span class="sxs-lookup"><span data-stu-id="b4d00-120">This is done using the **COM+ Partitions** folder within the Component Services administrative tool.</span></span> <span data-ttu-id="b4d00-121">為了簡化這項工作，[元件服務] 工具可讓系統管理員流覽 Active Directory，以選取所需的磁碟分割和其 GUID。</span><span class="sxs-lookup"><span data-stu-id="b4d00-121">To simplify this task, the Component Services tool allows the administrator to browse Active Directory to select the desired partition and its GUID.</span></span>

<span data-ttu-id="b4d00-122">在應用程式伺服器上建立網域分割區時，使用者的預設分割區會成為 Active Directory 中分割集的預設資料分割。</span><span class="sxs-lookup"><span data-stu-id="b4d00-122">When the domain partition has been created on the application server, a user's default partition becomes the default partition of the partition set in the Active Directory.</span></span> <span data-ttu-id="b4d00-123">最後，系統管理員可以將 COM + 應用程式安裝到應用程式伺服器上新建立的磁碟分割。</span><span class="sxs-lookup"><span data-stu-id="b4d00-123">Finally, the administrator can install the COM+ application into the newly created partition on the application server.</span></span>

<span data-ttu-id="b4d00-124">如需管理資料分割以供網域使用者存取的詳細資訊，請參閱與 Active Directory 消費者和電腦系統管理工具相關聯的說明。</span><span class="sxs-lookup"><span data-stu-id="b4d00-124">For more information about administering partitions for access by domain users, see the help associated with the Active Directory Users and Computers administrative tool.</span></span>

## <a name="mapping-user-identities-and-ous-to-partition-sets"></a><span data-ttu-id="b4d00-125">將使用者身分識別和 Ou 對應到資料分割集</span><span class="sxs-lookup"><span data-stu-id="b4d00-125">Mapping User Identities and OUs to Partition Sets</span></span>

<span data-ttu-id="b4d00-126">使用者和 Ou 可以對應到資料分割集。</span><span class="sxs-lookup"><span data-stu-id="b4d00-126">Users and OUs can be mapped to a partition sets.</span></span> <span data-ttu-id="b4d00-127">藉由將 Ou 對應到資料分割集，系統管理員可以將多個使用者與一次資料分割集建立關聯，而不需要對應多個使用者識別。</span><span class="sxs-lookup"><span data-stu-id="b4d00-127">By mapping OUs to partition sets, an administrator can associate multiple users with a partition set at one time instead of having to map multiple user identities.</span></span> <span data-ttu-id="b4d00-128">單一使用者識別或 OU 只能對應到一個資料分割集。</span><span class="sxs-lookup"><span data-stu-id="b4d00-128">A single user identity or OU can be mapped to one partition set only.</span></span> <span data-ttu-id="b4d00-129">一般情況下，將使用者身分識別或 Ou 對應到資料分割集，會執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="b4d00-129">In general, mapping user identities or OUs to partition sets does the following:</span></span>

-   <span data-ttu-id="b4d00-130">確保應用程式可供網域中的適當使用者使用</span><span class="sxs-lookup"><span data-stu-id="b4d00-130">Ensures that applications are available to the appropriate users in the domain</span></span>
-   <span data-ttu-id="b4d00-131">協助 COM + 判斷應用程式所在的磁碟分割</span><span class="sxs-lookup"><span data-stu-id="b4d00-131">Helps COM+ in determining the partition in which an application is located</span></span>
-   <span data-ttu-id="b4d00-132">建立使用者存取特定應用程式的許可權</span><span class="sxs-lookup"><span data-stu-id="b4d00-132">Establishes a user's right to access a particular application</span></span>

<span data-ttu-id="b4d00-133">若要將資料分割與 Active Directory 內的資料分割集建立關聯，並將使用者和 Ou 對應到這些分割集，系統管理員可以使用 Active Directory 消費者和電腦和元件服務系統管理工具。</span><span class="sxs-lookup"><span data-stu-id="b4d00-133">To associate partitions with partition sets within Active Directory and to map users and OUs to those partition sets, administrators use the Active Directory Users and Computers and Component Services administrative tools.</span></span> <span data-ttu-id="b4d00-134">在 Active Directory 中建立分割區時，系統管理員必須在要安裝相關 COM + 應用程式的電腦上，于本機設定該分割區。</span><span class="sxs-lookup"><span data-stu-id="b4d00-134">When a partition is created within Active Directory, an administrator needs to locally configure that partition on the computer where the relevant COM+ application is to be installed.</span></span> <span data-ttu-id="b4d00-135">在 Active Directory 中建立之分割區的本機設定是透過 [元件服務] 系統管理工具來完成。</span><span class="sxs-lookup"><span data-stu-id="b4d00-135">This local configuration of partitions created within Active Directory is done through the Component Services administrative tool.</span></span>

<span data-ttu-id="b4d00-136">如果網域使用者身分識別未對應到資料分割集，則會將使用者的 OU 存取權授與使用者，而該 OU 會對應到資料分割。</span><span class="sxs-lookup"><span data-stu-id="b4d00-136">If a domain user identity is not mapped to a partition set, the user is granted access by the user's OU, which is mapped to the partition.</span></span> <span data-ttu-id="b4d00-137">如果使用者的 OU 未對應到資料分割集，但階層中的下一個最高 OU 對應到該分割集，則使用者可以存取該資料分割。</span><span class="sxs-lookup"><span data-stu-id="b4d00-137">If the user's OU is not mapped to a partition set but the next highest OU in the hierarchy is mapped to that partition set, the user can access the partition.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b4d00-138">相關主題</span><span class="sxs-lookup"><span data-stu-id="b4d00-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b4d00-139">預設分割區</span><span class="sxs-lookup"><span data-stu-id="b4d00-139">Default Partitions</span></span>](default-partitions.md)
</dt> <dt>

[<span data-ttu-id="b4d00-140">本機分割區</span><span class="sxs-lookup"><span data-stu-id="b4d00-140">Local Partitions</span></span>](local-partitions.md)
</dt> <dt>

[<span data-ttu-id="b4d00-141">分割區屬性</span><span class="sxs-lookup"><span data-stu-id="b4d00-141">Partition Properties</span></span>](partition-properties.md)
</dt> <dt>

[<span data-ttu-id="b4d00-142">全域分割區</span><span class="sxs-lookup"><span data-stu-id="b4d00-142">The Global Partition</span></span>](the-global-partition.md)
</dt> </dl>

 

 




---
title: 新增保留
description: 路由資料庫包含保留清單。
ms.assetid: c36e731c-6a0b-42a8-bc92-106a8e017b0d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 358181cbe57a046f5af54f7adf17bdadb24c3ddc
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/20/2020
ms.locfileid: "104508191"
---
# <a name="adding-a-reservation"></a><span data-ttu-id="40d89-103">新增保留</span><span class="sxs-lookup"><span data-stu-id="40d89-103">Adding a Reservation</span></span>

<span data-ttu-id="40d89-104">路由資料庫包含保留清單。</span><span class="sxs-lookup"><span data-stu-id="40d89-104">The routing database contains the reservation list.</span></span> <span data-ttu-id="40d89-105">保留清單包含允許存取命名空間的使用者，以及保留下所列每位使用者的存取層級。</span><span class="sxs-lookup"><span data-stu-id="40d89-105">The reservation list consists of the users that are allowed access to the namespace, as well as the level of access for each user listed under the reservation.</span></span> <span data-ttu-id="40d89-106">新增或刪除保留時，會搜尋路由資料庫來決定存取權限。</span><span class="sxs-lookup"><span data-stu-id="40d89-106">When reservations are added or deleted, the routing database is searched to determine access privileges.</span></span>

<span data-ttu-id="40d89-107">除了檢查使用者識別碼之外，HTTP 伺服器 API 也會在安裝新的保留專案之前，先檢查現有保留中的衝突。</span><span class="sxs-lookup"><span data-stu-id="40d89-107">In addition to checking the users ID, the HTTP Server API also checks for conflicts in existing reservations before installing a new reservation.</span></span>

<span data-ttu-id="40d89-108">**若要加入新的保留**</span><span class="sxs-lookup"><span data-stu-id="40d89-108">**To add a new reservation**</span></span>

1.  <span data-ttu-id="40d89-109">如果 UrlPrefix 中的埠號碼具有與 UrlPrefix 中配置不同的配置保留或註冊，則註冊會失敗。</span><span class="sxs-lookup"><span data-stu-id="40d89-109">If the port number in the UrlPrefix has reservations or registrations for a scheme different from the scheme in the UrlPrefix, the registration fails.</span></span> <span data-ttu-id="40d89-110">在相同的埠上無法支援 HTTP 和 HTTPS。</span><span class="sxs-lookup"><span data-stu-id="40d89-110">HTTP and HTTPS cannot be supported on the same port.</span></span>
2.  <span data-ttu-id="40d89-111">找出適當的註冊值區， (查看 [路由傳入要求](routing-incoming-requests.md) ] 區段) ，根據主機類型。</span><span class="sxs-lookup"><span data-stu-id="40d89-111">Locate the appropriate bucket for the registration (see the [Routing Incoming Requests](routing-incoming-requests.md) section), based on the host type.</span></span> <span data-ttu-id="40d89-112">其餘步驟則相對於此值區。</span><span class="sxs-lookup"><span data-stu-id="40d89-112">The remaining steps are relative to this bucket.</span></span>
3.  <span data-ttu-id="40d89-113">選取具有配置、主機和埠元件的保留專案，以符合保留的 UrlPrefix。</span><span class="sxs-lookup"><span data-stu-id="40d89-113">Select reservation entries with scheme, host and port components that match the UrlPrefix being reserved.</span></span> <span data-ttu-id="40d89-114">從這些專案中找出具有最長相符 *relativeUri* 的專案，該專案不等於保留 (中的 relativeUri，也就是 *父節點*) 。</span><span class="sxs-lookup"><span data-stu-id="40d89-114">From these, locate the entry with the longest matching *relativeUri* that is not equal to the relativeUri in the reservation (that is, the *parent node*).</span></span> <span data-ttu-id="40d89-115">如果專案存在，則根據指派給該專案的 ACL 來評估存取權限。</span><span class="sxs-lookup"><span data-stu-id="40d89-115">If the entry exists, then evaluate access rights based on the ACL assigned to that entry.</span></span>
4.  <span data-ttu-id="40d89-116">如果找不到父節點，這是具有空白 relativeUri 或 *根保留* 的保留。</span><span class="sxs-lookup"><span data-stu-id="40d89-116">If a parent node was not found, this is a reservation with an empty relativeUri, or *root reservation*.</span></span> <span data-ttu-id="40d89-117">只有在以 LocalSystem 或系統管理員帳戶註冊呼叫端時，才授與存取權限。</span><span class="sxs-lookup"><span data-stu-id="40d89-117">Grant access rights only if the caller is registered under the LocalSystem or Administrator accounts.</span></span>
5.  <span data-ttu-id="40d89-118">如果授與存取權限，請檢查是否有重複的保留。</span><span class="sxs-lookup"><span data-stu-id="40d89-118">If access rights are granted, check for duplicate reservations.</span></span> <span data-ttu-id="40d89-119">如果存在具有相同配置、埠、主機和 relativeUri 的保留專案， \_ \_ 則會傳回錯誤已存在的程式碼。</span><span class="sxs-lookup"><span data-stu-id="40d89-119">If a reservation entry exists with the same scheme, port, host and relativeUri, an ERROR\_ALREADY\_EXISTS code is returned.</span></span>
    > [!Note]  
    > <span data-ttu-id="40d89-120">若要更新現有的專案，請執行下列兩個步驟：刪除專案，並新增一個新專案。</span><span class="sxs-lookup"><span data-stu-id="40d89-120">Updating an existing entry should be performed in two steps: delete the entry and add a new one.</span></span>

     

<span data-ttu-id="40d89-121">如果上述步驟成功，則會在保留資料庫中輸入新的保留專案。</span><span class="sxs-lookup"><span data-stu-id="40d89-121">If the above steps succeed, a new reservation entry is entered into the reservation database.</span></span>

> [!Note]  
> <span data-ttu-id="40d89-122">新的專案會以指定的 ACL 建立，且不會從 *父* 專案繼承 acl。</span><span class="sxs-lookup"><span data-stu-id="40d89-122">The new entry is created with the specified ACL and does not inherit ACLs from the *parent* entry.</span></span>

 

<span data-ttu-id="40d89-123">下列範例說明保留流程。</span><span class="sxs-lookup"><span data-stu-id="40d89-123">The following examples illustrate the reservation process.</span></span>

-   <span data-ttu-id="40d89-124">保留1： `https://+:80/vroot/subdir/` 使用者 A 和使用者 C 的系統管理員成功，並輸入 "+" bucket。</span><span class="sxs-lookup"><span data-stu-id="40d89-124">Reservation 1: `https://+:80/vroot/subdir/` by Admin for User A and User C succeeds and is entered into the "+" bucket.</span></span>
-   <span data-ttu-id="40d89-125">保留2： `https://adatum.com:80/vroot/` 使用者 B 的系統管理員成功，並輸入「明確主機」 bucket。</span><span class="sxs-lookup"><span data-stu-id="40d89-125">Reservation 2: `https://adatum.com:80/vroot/` by Admin for User B succeeds and is entered into the "Explicit host" bucket.</span></span>
-   <span data-ttu-id="40d89-126">保留3：使用者 `https://adatum.com:80/vroot/subdir/otherdir/` C 的使用者 B 成功，因為保留2。</span><span class="sxs-lookup"><span data-stu-id="40d89-126">Reservation 3: `https://adatum.com:80/vroot/subdir/otherdir/` by User B for User C succeeds due to reservation 2.</span></span>
-   <span data-ttu-id="40d89-127">保留4： `https://+:80/vroot/subdir/otherdir/` 使用者 E 的使用者 A 成功，因為保留1。</span><span class="sxs-lookup"><span data-stu-id="40d89-127">Reservation 4: `https://+:80/vroot/subdir/otherdir/` by User A for User E succeeds due to reservation 1.</span></span>
-   <span data-ttu-id="40d89-128">保留5： `https://adatum.com:80/vroot/subdir/otherdir/` 使用者 E 的使用者 A 失敗。</span><span class="sxs-lookup"><span data-stu-id="40d89-128">Reservation 5: `https://adatum.com:80/vroot/subdir/otherdir/` by User A for User E fails.</span></span> <span data-ttu-id="40d89-129">因保留2而拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="40d89-129">Access denied due to reservation 2.</span></span>
-   <span data-ttu-id="40d89-130">保留6： `https://+:80/vroot/subdir/` 使用者 A 的管理員失敗。</span><span class="sxs-lookup"><span data-stu-id="40d89-130">Reservation 6: `https://+:80/vroot/subdir/` by Admin for User A fails.</span></span> <span data-ttu-id="40d89-131">保留與保留1衝突。</span><span class="sxs-lookup"><span data-stu-id="40d89-131">The reservation conflicts with reservation 1.</span></span>
-   <span data-ttu-id="40d89-132">保留7：使用者 a 的 `https://adatum.com:80/newroot/` 使用者 a 失敗。</span><span class="sxs-lookup"><span data-stu-id="40d89-132">Reservation 7: `https://adatum.com:80/newroot/` by User A for User A fails.</span></span> <span data-ttu-id="40d89-133">因為 LocalSystem 或系統管理員的隱含根保留，所以拒絕存取 `https://adatum.com:80/` 。</span><span class="sxs-lookup"><span data-stu-id="40d89-133">Access denied due to implicit root reservation of `https://adatum.com:80/` for LocalSystem or Administrator.</span></span>

<span data-ttu-id="40d89-134">保留可能會影響傳遞至先前註冊 UrlPrefix 之進程的要求中的一組 Url。</span><span class="sxs-lookup"><span data-stu-id="40d89-134">Reservations can affect the set of URLs in requests delivered to a process that has previously registered a UrlPrefix.</span></span> <span data-ttu-id="40d89-135">例如，請設想下列情況。</span><span class="sxs-lookup"><span data-stu-id="40d89-135">For example, consider the following scenario.</span></span>

-   <span data-ttu-id="40d89-136">註冊： `https://adatum.com:80/vroot/` 使用者 A 的應用程式1。</span><span class="sxs-lookup"><span data-stu-id="40d89-136">Registration: `https://adatum.com:80/vroot/` by application 1 for User A.</span></span>
-   <span data-ttu-id="40d89-137">的要求 `https://adatum.com:80/vroot/subdir/file.htm` 會傳遞至應用程式1。</span><span class="sxs-lookup"><span data-stu-id="40d89-137">A request for `https://adatum.com:80/vroot/subdir/file.htm` is delivered to application 1.</span></span>
-   <span data-ttu-id="40d89-138">保留： `https://+:80/vroot/subdir/` 適用于使用者 B。</span><span class="sxs-lookup"><span data-stu-id="40d89-138">Reservation: `https://+:80/vroot/subdir/` for User B.</span></span>
-   <span data-ttu-id="40d89-139">的要求 `https://adatum.com:80/vroot/subdir/file.htm` 現在已遭到拒絕。</span><span class="sxs-lookup"><span data-stu-id="40d89-139">A request for `https://adatum.com:80/vroot/subdir/file.htm` is now rejected.</span></span>
-   <span data-ttu-id="40d89-140">註冊： `https://adatum.com:80/vroot/subdir/` 依應用程式2為使用者 B。</span><span class="sxs-lookup"><span data-stu-id="40d89-140">Registration: `https://adatum.com:80/vroot/subdir/` by application 2 for User B.</span></span>
-   <span data-ttu-id="40d89-141">的要求 `https://adatum.com:80/vroot/subdir/file.htm` 會傳遞至應用程式2。</span><span class="sxs-lookup"><span data-stu-id="40d89-141">A request for `https://adatum.com:80/vroot/subdir/file.htm` is delivered to application 2.</span></span>

 

 





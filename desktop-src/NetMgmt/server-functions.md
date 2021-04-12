---
title: " (網路管理) 的伺服器功能"
description: Network management server 函式會在本機或遠端伺服器上執行管理工作。 伺服器函數如下所示。
ms.assetid: 43e1285b-8c86-4af4-9834-fcd5ee8aceb8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43758fa822ce60d484418431941a386681bb77d1
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104024496"
---
# <a name="server-functions-network-management"></a><span data-ttu-id="2b9ff-104"> (網路管理) 的伺服器功能</span><span class="sxs-lookup"><span data-stu-id="2b9ff-104">Server Functions (Network Management)</span></span>

<span data-ttu-id="2b9ff-105">Network management server 函式會在本機或遠端伺服器上執行管理工作。</span><span class="sxs-lookup"><span data-stu-id="2b9ff-105">The network management server functions perform administrative tasks on a local or remote server.</span></span> <span data-ttu-id="2b9ff-106">伺服器函數如下所示。</span><span class="sxs-lookup"><span data-stu-id="2b9ff-106">The server functions are listed following.</span></span>



| <span data-ttu-id="2b9ff-107">函式</span><span class="sxs-lookup"><span data-stu-id="2b9ff-107">Function</span></span>                                       | <span data-ttu-id="2b9ff-108">描述</span><span class="sxs-lookup"><span data-stu-id="2b9ff-108">Description</span></span>                                                                        |
|------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="2b9ff-109">**NetServerDiskEnum**</span><span class="sxs-lookup"><span data-stu-id="2b9ff-109">**NetServerDiskEnum**</span></span>](/windows/desktop/api/Lmserver/nf-lmserver-netserverdiskenum) | <span data-ttu-id="2b9ff-110">傳回伺服器上的本機磁片磁碟機清單。</span><span class="sxs-lookup"><span data-stu-id="2b9ff-110">Returns a list of local disk drives on a server.</span></span>                                   |
| [<span data-ttu-id="2b9ff-111">**NetServerEnum**</span><span class="sxs-lookup"><span data-stu-id="2b9ff-111">**NetServerEnum**</span></span>](/windows/desktop/api/Lmserver/nf-lmserver-netserverenum)         | <span data-ttu-id="2b9ff-112">列出特定類型的所有可見伺服器 (或指定網域中) 的類型。</span><span class="sxs-lookup"><span data-stu-id="2b9ff-112">Lists all visible servers of a particular type (or types) in the specified domain.</span></span> |
| [<span data-ttu-id="2b9ff-113">**NetServerGetInfo**</span><span class="sxs-lookup"><span data-stu-id="2b9ff-113">**NetServerGetInfo**</span></span>](/windows/desktop/api/Lmserver/nf-lmserver-netservergetinfo)   | <span data-ttu-id="2b9ff-114">傳回指定伺服器的設定資訊。</span><span class="sxs-lookup"><span data-stu-id="2b9ff-114">Returns configuration information about a specified server.</span></span>                        |
| [<span data-ttu-id="2b9ff-115">**NetServerSetInfo**</span><span class="sxs-lookup"><span data-stu-id="2b9ff-115">**NetServerSetInfo**</span></span>](/windows/desktop/api/Lmserver/nf-lmserver-netserversetinfo)   | <span data-ttu-id="2b9ff-116">設定伺服器的指令引數。</span><span class="sxs-lookup"><span data-stu-id="2b9ff-116">Sets the operating parameters for a server.</span></span>                                        |



 

<span data-ttu-id="2b9ff-117">只有在本機或遠端伺服器上具有系統管理員群組成員資格的使用者或應用程式，才能在該伺服器上執行系統管理工作，以控制伺服器的作業、使用者存取和資源分享。</span><span class="sxs-lookup"><span data-stu-id="2b9ff-117">Only a user or application with admin group membership on a local or remote server can perform administrative tasks on that server to control the server's operation, user access, and resource sharing.</span></span> <span data-ttu-id="2b9ff-118">您可以藉由呼叫 [**NetServerGetInfo**](/windows/desktop/api/Lmserver/nf-lmserver-netservergetinfo) 和 [**NetServerSetInfo**](/windows/desktop/api/Lmserver/nf-lmserver-netserversetinfo) 函數來檢查和修改影響伺服器作業的低層級參數。</span><span class="sxs-lookup"><span data-stu-id="2b9ff-118">The low-level parameters that affect a server's operation can be examined and modified by calling the [**NetServerGetInfo**](/windows/desktop/api/Lmserver/nf-lmserver-netservergetinfo) and [**NetServerSetInfo**](/windows/desktop/api/Lmserver/nf-lmserver-netserversetinfo) functions.</span></span> <span data-ttu-id="2b9ff-119">這些參數是在伺服器的 LANMAN.INI 檔案中定義。</span><span class="sxs-lookup"><span data-stu-id="2b9ff-119">These parameters are defined in the server's LANMAN.INI file.</span></span>

<span data-ttu-id="2b9ff-120">大部分的網路管理伺服器功能只會在遠端伺服器上執行。</span><span class="sxs-lookup"><span data-stu-id="2b9ff-120">Most network management server functions execute only on a remote server.</span></span> <span data-ttu-id="2b9ff-121">[**NetServerEnum**](/windows/desktop/api/Lmserver/nf-lmserver-netserverenum)函式是在本機工作站或遠端伺服器上執行。</span><span class="sxs-lookup"><span data-stu-id="2b9ff-121">The [**NetServerEnum**](/windows/desktop/api/Lmserver/nf-lmserver-netserverenum) function executes on either a local workstation or a remote server.</span></span> <span data-ttu-id="2b9ff-122">如果您嘗試在本機工作站上執行其他伺服器函式，這些函式會傳回錯誤 NERR \_ RemoteOnly。</span><span class="sxs-lookup"><span data-stu-id="2b9ff-122">If you attempt to execute other server functions on a local workstation, the functions return the error NERR\_RemoteOnly.</span></span>

<span data-ttu-id="2b9ff-123">您可以在下列層級取得伺服器特定的資訊：</span><span class="sxs-lookup"><span data-stu-id="2b9ff-123">Server-specific information is available at the following levels:</span></span>

-   [<span data-ttu-id="2b9ff-124">**伺服器 \_ 資訊 \_ 100**</span><span class="sxs-lookup"><span data-stu-id="2b9ff-124">**SERVER\_INFO\_100**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_100)
-   [<span data-ttu-id="2b9ff-125">**伺服器 \_ 資訊 \_ 101**</span><span class="sxs-lookup"><span data-stu-id="2b9ff-125">**SERVER\_INFO\_101**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_101)
-   [<span data-ttu-id="2b9ff-126">**伺服器 \_ 資訊 \_ 102**</span><span class="sxs-lookup"><span data-stu-id="2b9ff-126">**SERVER\_INFO\_102**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_102)
-   [<span data-ttu-id="2b9ff-127">**伺服器 \_ 資訊 \_ 402**</span><span class="sxs-lookup"><span data-stu-id="2b9ff-127">**SERVER\_INFO\_402**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_402)
-   [<span data-ttu-id="2b9ff-128">**伺服器 \_ 資訊 \_ 403**</span><span class="sxs-lookup"><span data-stu-id="2b9ff-128">**SERVER\_INFO\_403**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_403)
-   [<span data-ttu-id="2b9ff-129">**伺服器 \_ 資訊 \_ 1501**</span><span class="sxs-lookup"><span data-stu-id="2b9ff-129">**SERVER\_INFO\_1501**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1501)
-   [<span data-ttu-id="2b9ff-130">**伺服器 \_ 資訊 \_ 1502**</span><span class="sxs-lookup"><span data-stu-id="2b9ff-130">**SERVER\_INFO\_1502**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1502)
-   [<span data-ttu-id="2b9ff-131">**伺服器 \_ 資訊 \_ 1503**</span><span class="sxs-lookup"><span data-stu-id="2b9ff-131">**SERVER\_INFO\_1503**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1503)
-   [<span data-ttu-id="2b9ff-132">**伺服器 \_ 資訊 \_ 1506**</span><span class="sxs-lookup"><span data-stu-id="2b9ff-132">**SERVER\_INFO\_1506**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1506)
-   [<span data-ttu-id="2b9ff-133">**伺服器 \_ 資訊 \_ 1509**</span><span class="sxs-lookup"><span data-stu-id="2b9ff-133">**SERVER\_INFO\_1509**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1509)
-   [<span data-ttu-id="2b9ff-134">**伺服器 \_ 資訊 \_ 1510**</span><span class="sxs-lookup"><span data-stu-id="2b9ff-134">**SERVER\_INFO\_1510**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1510)
-   [<span data-ttu-id="2b9ff-135">**伺服器 \_ 資訊 \_ 1511**</span><span class="sxs-lookup"><span data-stu-id="2b9ff-135">**SERVER\_INFO\_1511**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1511)
-   [<span data-ttu-id="2b9ff-136">**伺服器 \_ 資訊 \_ 1512**</span><span class="sxs-lookup"><span data-stu-id="2b9ff-136">**SERVER\_INFO\_1512**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1512)
-   [<span data-ttu-id="2b9ff-137">**伺服器 \_ 資訊 \_ 1513**</span><span class="sxs-lookup"><span data-stu-id="2b9ff-137">**SERVER\_INFO\_1513**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1513)
-   [<span data-ttu-id="2b9ff-138">**伺服器 \_ 資訊 \_ 1515**</span><span class="sxs-lookup"><span data-stu-id="2b9ff-138">**SERVER\_INFO\_1515**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1515)
-   [<span data-ttu-id="2b9ff-139">**伺服器 \_ 資訊 \_ 1516**</span><span class="sxs-lookup"><span data-stu-id="2b9ff-139">**SERVER\_INFO\_1516**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1516)
-   [<span data-ttu-id="2b9ff-140">**伺服器 \_ 資訊 \_ 1518**</span><span class="sxs-lookup"><span data-stu-id="2b9ff-140">**SERVER\_INFO\_1518**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1518)
-   [<span data-ttu-id="2b9ff-141">**伺服器 \_ 資訊 \_ 1523**</span><span class="sxs-lookup"><span data-stu-id="2b9ff-141">**SERVER\_INFO\_1523**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1523)
-   [<span data-ttu-id="2b9ff-142">**伺服器 \_ 資訊 \_ 1528**</span><span class="sxs-lookup"><span data-stu-id="2b9ff-142">**SERVER\_INFO\_1528**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1528)
-   [<span data-ttu-id="2b9ff-143">**伺服器 \_ 資訊 \_ 1529**</span><span class="sxs-lookup"><span data-stu-id="2b9ff-143">**SERVER\_INFO\_1529**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1529)
-   [<span data-ttu-id="2b9ff-144">**伺服器 \_ 資訊 \_ 1530**</span><span class="sxs-lookup"><span data-stu-id="2b9ff-144">**SERVER\_INFO\_1530**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1530)
-   [<span data-ttu-id="2b9ff-145">**伺服器 \_ 資訊 \_ 1533**</span><span class="sxs-lookup"><span data-stu-id="2b9ff-145">**SERVER\_INFO\_1533**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1533)
-   [<span data-ttu-id="2b9ff-146">**伺服器 \_ 資訊 \_ 1536**</span><span class="sxs-lookup"><span data-stu-id="2b9ff-146">**SERVER\_INFO\_1536**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1536)
-   [<span data-ttu-id="2b9ff-147">**伺服器 \_ 資訊 \_ 1538**</span><span class="sxs-lookup"><span data-stu-id="2b9ff-147">**SERVER\_INFO\_1538**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1538)
-   [<span data-ttu-id="2b9ff-148">**伺服器 \_ 資訊 \_ 1539**</span><span class="sxs-lookup"><span data-stu-id="2b9ff-148">**SERVER\_INFO\_1539**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1539)
-   [<span data-ttu-id="2b9ff-149">**伺服器 \_ 資訊 \_ 1540**</span><span class="sxs-lookup"><span data-stu-id="2b9ff-149">**SERVER\_INFO\_1540**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1540)
-   [<span data-ttu-id="2b9ff-150">**伺服器 \_ 資訊 \_ 1541**</span><span class="sxs-lookup"><span data-stu-id="2b9ff-150">**SERVER\_INFO\_1541**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1541)
-   [<span data-ttu-id="2b9ff-151">**伺服器 \_ 資訊 \_ 1542**</span><span class="sxs-lookup"><span data-stu-id="2b9ff-151">**SERVER\_INFO\_1542**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1542)
-   [<span data-ttu-id="2b9ff-152">**伺服器 \_ 資訊 \_ 1544**</span><span class="sxs-lookup"><span data-stu-id="2b9ff-152">**SERVER\_INFO\_1544**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1544)
-   [<span data-ttu-id="2b9ff-153">**伺服器 \_ 資訊 \_ 1550**</span><span class="sxs-lookup"><span data-stu-id="2b9ff-153">**SERVER\_INFO\_1550**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1550)
-   [<span data-ttu-id="2b9ff-154">**伺服器 \_ 資訊 \_ 1552**</span><span class="sxs-lookup"><span data-stu-id="2b9ff-154">**SERVER\_INFO\_1552**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1552)

<span data-ttu-id="2b9ff-155">如果您正在針對 Active Directory 進行程式設計，您可以呼叫特定 Active Directory 服務介面 (ADSI) 方法，以取得您可以藉由呼叫網路管理伺服器功能達成的相同功能。</span><span class="sxs-lookup"><span data-stu-id="2b9ff-155">If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same functionality you can achieve by calling the network management server functions.</span></span> <span data-ttu-id="2b9ff-156">如需詳細資訊，請參閱 [**IADsComputer**](/windows/desktop/api/iads/nn-iads-iadscomputer)。</span><span class="sxs-lookup"><span data-stu-id="2b9ff-156">For more information, see [**IADsComputer**](/windows/desktop/api/iads/nn-iads-iadscomputer).</span></span>

<span data-ttu-id="2b9ff-157">如需詳細資訊，請參閱 [伺服器和工作站傳輸功能](server-and-workstation-transport-functions.md)。</span><span class="sxs-lookup"><span data-stu-id="2b9ff-157">For more information, see the [Server and Workstation Transport Functions](server-and-workstation-transport-functions.md).</span></span>

 

 

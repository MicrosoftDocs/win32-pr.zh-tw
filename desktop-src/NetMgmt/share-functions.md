---
title: 共用函式
description: 網路管理共用功能會控制共用資源。 共用資源是伺服器上的本機資源 (例如，磁碟目錄、列印裝置或具名管道) ，可供使用者和網路上的應用程式存取。
ms.assetid: 3764c667-2290-48e6-ba3a-c74eee2c27f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5034d46e233ebb7ed4de691bd79942a3ecdf5263
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382573"
---
# <a name="share-functions"></a><span data-ttu-id="1c151-104">共用函式</span><span class="sxs-lookup"><span data-stu-id="1c151-104">Share Functions</span></span>

<span data-ttu-id="1c151-105">網路管理共用功能會控制共用資源。</span><span class="sxs-lookup"><span data-stu-id="1c151-105">The network management share functions control shared resources.</span></span> <span data-ttu-id="1c151-106">共用資源是伺服器上的本機資源 (例如，磁碟目錄、列印裝置或具名管道) ，可供使用者和網路上的應用程式存取。</span><span class="sxs-lookup"><span data-stu-id="1c151-106">A shared resource is a local resource on a server (for example, a disk directory, print device, or named pipe) that can be accessed by users and applications on the network.</span></span>

<span data-ttu-id="1c151-107">共用函數如下所示。</span><span class="sxs-lookup"><span data-stu-id="1c151-107">The share functions are listed following.</span></span>



| <span data-ttu-id="1c151-108">函式</span><span class="sxs-lookup"><span data-stu-id="1c151-108">Function</span></span>                                  | <span data-ttu-id="1c151-109">描述</span><span class="sxs-lookup"><span data-stu-id="1c151-109">Description</span></span>                                                          |
|-------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="1c151-110">**NetShareAdd**</span><span class="sxs-lookup"><span data-stu-id="1c151-110">**NetShareAdd**</span></span>](/windows/desktop/api/lmshare/nf-lmshare-netshareadd)         | <span data-ttu-id="1c151-111">共用伺服器上的資源。</span><span class="sxs-lookup"><span data-stu-id="1c151-111">Shares a resource on a server.</span></span>                                       |
| [<span data-ttu-id="1c151-112">**NetShareCheck**</span><span class="sxs-lookup"><span data-stu-id="1c151-112">**NetShareCheck**</span></span>](/windows/desktop/api/lmshare/nf-lmshare-netsharecheck)     | <span data-ttu-id="1c151-113">查詢伺服器是否正在共用裝置。</span><span class="sxs-lookup"><span data-stu-id="1c151-113">Queries whether a server is sharing a device.</span></span>                        |
| [<span data-ttu-id="1c151-114">**NetShareDel**</span><span class="sxs-lookup"><span data-stu-id="1c151-114">**NetShareDel**</span></span>](/windows/desktop/api/lmshare/nf-lmshare-netsharedel)         | <span data-ttu-id="1c151-115">從伺服器的共用資源清單中刪除共用名稱。</span><span class="sxs-lookup"><span data-stu-id="1c151-115">Deletes a share name from a server's list of shared resources.</span></span>       |
| [<span data-ttu-id="1c151-116">**NetShareEnum**</span><span class="sxs-lookup"><span data-stu-id="1c151-116">**NetShareEnum**</span></span>](/windows/desktop/api/lmshare/nf-lmshare-netshareenum)       | <span data-ttu-id="1c151-117">抓取伺服器上每個共用資源的共用資訊。</span><span class="sxs-lookup"><span data-stu-id="1c151-117">Retrieves share information about each shared resource on a server.</span></span>  |
| [<span data-ttu-id="1c151-118">**NetShareGetInfo**</span><span class="sxs-lookup"><span data-stu-id="1c151-118">**NetShareGetInfo**</span></span>](/windows/desktop/api/lmshare/nf-lmshare-netsharegetinfo) | <span data-ttu-id="1c151-119">抓取伺服器上指定之共用資源的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="1c151-119">Retrieves information about a specified shared resource on a server.</span></span> |
| [<span data-ttu-id="1c151-120">**NetShareSetInfo**</span><span class="sxs-lookup"><span data-stu-id="1c151-120">**NetShareSetInfo**</span></span>](/windows/desktop/api/lmshare/nf-lmshare-netsharesetinfo) | <span data-ttu-id="1c151-121">設定共用資源的參數。</span><span class="sxs-lookup"><span data-stu-id="1c151-121">Sets a shared resource's parameters.</span></span>                                 |



 

<span data-ttu-id="1c151-122">這些共用函式僅適用于伺服器訊息區上的共用， (LAN Manager) Server。</span><span class="sxs-lookup"><span data-stu-id="1c151-122">These share function apply only to shares on a Server Message Block (LAN Manager) server.</span></span> <span data-ttu-id="1c151-123">這些共用功能不支援 (DFS) 共用分散式檔案系統。</span><span class="sxs-lookup"><span data-stu-id="1c151-123">These share functions do not support Distributed File System (DFS) shares.</span></span> <span data-ttu-id="1c151-124">例如， [**NetShareGetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netsharegetinfo) 函式只能取得 SMB 伺服器上指定之共用資源的資訊。</span><span class="sxs-lookup"><span data-stu-id="1c151-124">For example, the [**NetShareGetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netsharegetinfo) function can only retrieve information for a specified share resource on an SMB Server.</span></span> <span data-ttu-id="1c151-125">若要使用不同的網路提供者取出共用的資訊 (WebDAV 或 DFS 共用（例如) ），請使用 [**WNetGetConnection**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetgetconnectiona) 函式。</span><span class="sxs-lookup"><span data-stu-id="1c151-125">To retrieve information for a share using a different network provider (WebDAV or a DFS share, for example), use the [**WNetGetConnection**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetgetconnectiona) function.</span></span>

<span data-ttu-id="1c151-126">[**NetShareAdd**](/windows/desktop/api/lmshare/nf-lmshare-netshareadd)函式可讓使用者或應用程式使用指定的共用名稱來共用特定類型的資源。</span><span class="sxs-lookup"><span data-stu-id="1c151-126">The [**NetShareAdd**](/windows/desktop/api/lmshare/nf-lmshare-netshareadd) function allows a user or application to share a resource of a specific type using the specified share name.</span></span> <span data-ttu-id="1c151-127">**NetShareAdd** 函式需要共用名稱和本機裝置名稱，才能共用資源。</span><span class="sxs-lookup"><span data-stu-id="1c151-127">The **NetShareAdd** function requires the share name and local device name to share the resource.</span></span> <span data-ttu-id="1c151-128">使用者或應用程式必須具有伺服器上的帳戶，才能存取資源。</span><span class="sxs-lookup"><span data-stu-id="1c151-128">A user or application must have an account on the server to access the resource.</span></span>

<span data-ttu-id="1c151-129">您也可以指定要與共享相關聯的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="1c151-129">You can also specify a security descriptor to be associated with a share.</span></span> <span data-ttu-id="1c151-130">安全描述項會指定允許哪些使用者透過共用存取檔案，以及使用何種類型的存取權。</span><span class="sxs-lookup"><span data-stu-id="1c151-130">Security descriptors specify which users are allowed to access files through the share, and with what type of access.</span></span> <span data-ttu-id="1c151-131">呼叫 **NetShareAdd** 或 [**NetShareSetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netsharesetinfo)時，請指定具有 [**共用 \_ 資訊 \_ 502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502)資訊層級的 [**安全 \_ 描述項**](/windows/desktop/api/winnt/ns-winnt-security_descriptor)。</span><span class="sxs-lookup"><span data-stu-id="1c151-131">Specify a [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) with the [**SHARE\_INFO\_502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502) information level when calling **NetShareAdd** or [**NetShareSetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netsharesetinfo).</span></span> <span data-ttu-id="1c151-132">**NetShareSetInfo** 支援 [**共用 \_ 資訊 \_ 1501**](/windows/desktop/api/lmshare/ns-lmshare-share_info_1501) 資訊層級。</span><span class="sxs-lookup"><span data-stu-id="1c151-132">**NetShareSetInfo** supports the [**SHARE\_INFO\_1501**](/windows/desktop/api/lmshare/ns-lmshare-share_info_1501) information level.</span></span> <span data-ttu-id="1c151-133">如需安全描述項的詳細資訊，請參閱 [存取控制](/windows/desktop/SecAuthZ/access-control)。</span><span class="sxs-lookup"><span data-stu-id="1c151-133">For more information about security descriptors, see [Access Control](/windows/desktop/SecAuthZ/access-control).</span></span>

<span data-ttu-id="1c151-134">網路管理功能會使用下列特殊的共用名稱來進行處理序間通訊 (IPC) 和伺服器的遠端系統管理：</span><span class="sxs-lookup"><span data-stu-id="1c151-134">The network management functions use the following special share names for interprocess communication (IPC) and remote administration of the server:</span></span>

-   <span data-ttu-id="1c151-135">IPC $，保留給處理序間通訊</span><span class="sxs-lookup"><span data-stu-id="1c151-135">IPC$, reserved for interprocess communication</span></span>
-   <span data-ttu-id="1c151-136">ADMIN $，保留給遠端系統管理</span><span class="sxs-lookup"><span data-stu-id="1c151-136">ADMIN$, reserved for remote administration</span></span>
-   <span data-ttu-id="1c151-137">$、B $、C $ (和其他本機磁片名稱，後面接著貨幣符號) ，指派給本機磁片裝置</span><span class="sxs-lookup"><span data-stu-id="1c151-137">A$, B$, C$ (and other local disk names followed by a dollar sign), assigned to local disk devices</span></span>

<span data-ttu-id="1c151-138">若要列出伺服器上共用資源的所有連線，或列出從特定電腦建立的所有連接，請呼叫 [**NetConnectionEnum**](/windows/desktop/api/lmshare/nf-lmshare-netconnectionenum) 函數。</span><span class="sxs-lookup"><span data-stu-id="1c151-138">To list all connections made to a shared resource on a server, or to list all connections established from a particular computer, call the [**NetConnectionEnum**](/windows/desktop/api/lmshare/nf-lmshare-netconnectionenum) function.</span></span> <span data-ttu-id="1c151-139">您可以在 [**連接 \_ 資訊 \_ 0**](/windows/desktop/api/lmshare/ns-lmshare-connection_info_0)和 [**連接 \_ 資訊 \_ 1**](/windows/desktop/api/lmshare/ns-lmshare-connection_info_1)資訊層級呼叫 **NetConnectionEnum** 。</span><span class="sxs-lookup"><span data-stu-id="1c151-139">You can call **NetConnectionEnum** at the [**CONNECTION\_INFO\_0**](/windows/desktop/api/lmshare/ns-lmshare-connection_info_0) and [**CONNECTION\_INFO\_1**](/windows/desktop/api/lmshare/ns-lmshare-connection_info_1) information levels.</span></span>

<span data-ttu-id="1c151-140">您可以在下列資訊層級取得共用函式，不過某些共用層級只適用于某些共用功能：</span><span class="sxs-lookup"><span data-stu-id="1c151-140">Share functions are available at the following information levels although some share levels are only applicable to some of the share functions:</span></span>

-   [<span data-ttu-id="1c151-141">**共用 \_ 資訊 \_ 0**</span><span class="sxs-lookup"><span data-stu-id="1c151-141">**SHARE\_INFO\_0**</span></span>](/windows/desktop/api/lmshare/ns-lmshare-share_info_0)
-   [<span data-ttu-id="1c151-142">**共用 \_ 資訊 \_ 1**</span><span class="sxs-lookup"><span data-stu-id="1c151-142">**SHARE\_INFO\_1**</span></span>](/windows/desktop/api/lmshare/ns-lmshare-share_info_1)
-   [<span data-ttu-id="1c151-143">**共用 \_ 資訊 \_ 2**</span><span class="sxs-lookup"><span data-stu-id="1c151-143">**SHARE\_INFO\_2**</span></span>](/windows/desktop/api/lmshare/ns-lmshare-share_info_2)
-   [<span data-ttu-id="1c151-144">**共用 \_ 資訊 \_ 501**</span><span class="sxs-lookup"><span data-stu-id="1c151-144">**SHARE\_INFO\_501**</span></span>](/windows/desktop/api/lmshare/ns-lmshare-share_info_501)
-   [<span data-ttu-id="1c151-145">**共用 \_ 資訊 \_ 502**</span><span class="sxs-lookup"><span data-stu-id="1c151-145">**SHARE\_INFO\_502**</span></span>](/windows/desktop/api/lmshare/ns-lmshare-share_info_502)
-   [<span data-ttu-id="1c151-146">**共用 \_ 資訊 \_ 503**</span><span class="sxs-lookup"><span data-stu-id="1c151-146">**SHARE\_INFO\_503**</span></span>](/windows/desktop/api/lmshare/ns-lmshare-share_info_503)
-   [<span data-ttu-id="1c151-147">**共用 \_ 資訊 \_ 1004**</span><span class="sxs-lookup"><span data-stu-id="1c151-147">**SHARE\_INFO\_1004**</span></span>](/windows/desktop/api/lmshare/ns-lmshare-share_info_1004)
-   [<span data-ttu-id="1c151-148">**共用 \_ 資訊 \_ 1005**</span><span class="sxs-lookup"><span data-stu-id="1c151-148">**SHARE\_INFO\_1005**</span></span>](/windows/desktop/api/lmshare/ns-lmshare-share_info_1005)
-   [<span data-ttu-id="1c151-149">**共用 \_ 資訊 \_ 1006**</span><span class="sxs-lookup"><span data-stu-id="1c151-149">**SHARE\_INFO\_1006**</span></span>](/windows/desktop/api/lmshare/ns-lmshare-share_info_1006)
-   [<span data-ttu-id="1c151-150">**共用 \_ 資訊 \_ 1501**</span><span class="sxs-lookup"><span data-stu-id="1c151-150">**SHARE\_INFO\_1501**</span></span>](/windows/desktop/api/lmshare/ns-lmshare-share_info_1501)

<span data-ttu-id="1c151-151">如需詳細資料，請參閱特定共用功能的檔。</span><span class="sxs-lookup"><span data-stu-id="1c151-151">Please review to documentation for a specific share function for details.</span></span>

<span data-ttu-id="1c151-152">如果您正在針對 Active Directory 進行程式設計，您可以呼叫特定 Active Directory 服務介面 (ADSI) 方法，以取得您可以藉由呼叫網路管理共用功能來達成的相同功能。</span><span class="sxs-lookup"><span data-stu-id="1c151-152">If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same functionality you can achieve by calling the network management share functions.</span></span> <span data-ttu-id="1c151-153">如需詳細資訊，請參閱 [**IADsFileShare**](/windows/desktop/api/iads/nn-iads-iadsfileshare)。</span><span class="sxs-lookup"><span data-stu-id="1c151-153">For more information, see [**IADsFileShare**](/windows/desktop/api/iads/nn-iads-iadsfileshare).</span></span>

 

 
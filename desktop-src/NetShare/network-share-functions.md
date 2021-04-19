---
description: 網路共用功能會控制共用資源。 共用資源是伺服器上的本機資源 (例如，磁碟目錄、列印裝置或具名管道) ，可供使用者和網路上的應用程式存取。
ms.assetid: 14886bb0-e597-4728-a64f-bc16e82874da
title: 網路共用功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 640dc877c9b482cb8ebdcef0d36e6dff562fcd8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106981531"
---
# <a name="network-share-functions"></a><span data-ttu-id="e54d4-104">網路共用功能</span><span class="sxs-lookup"><span data-stu-id="e54d4-104">Network Share Functions</span></span>

<span data-ttu-id="e54d4-105">網路共用功能會控制共用資源。</span><span class="sxs-lookup"><span data-stu-id="e54d4-105">The network share functions control shared resources.</span></span> <span data-ttu-id="e54d4-106">共用資源是伺服器上的本機資源 (例如，磁碟目錄、列印裝置或具名管道) ，可供使用者和網路上的應用程式存取。</span><span class="sxs-lookup"><span data-stu-id="e54d4-106">A shared resource is a local resource on a server (for example, a disk directory, print device, or named pipe) that can be accessed by users and applications on the network.</span></span>

<span data-ttu-id="e54d4-107">共用函數如下所示。</span><span class="sxs-lookup"><span data-stu-id="e54d4-107">The share functions are listed following.</span></span>



| <span data-ttu-id="e54d4-108">函式</span><span class="sxs-lookup"><span data-stu-id="e54d4-108">Function</span></span>                                   | <span data-ttu-id="e54d4-109">描述</span><span class="sxs-lookup"><span data-stu-id="e54d4-109">Description</span></span>                                                          |
|--------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="e54d4-110">**NetShareAdd**</span><span class="sxs-lookup"><span data-stu-id="e54d4-110">**NetShareAdd**</span></span>](/windows/desktop/api/Lmshare/nf-lmshare-netshareadd)         | <span data-ttu-id="e54d4-111">共用伺服器上的資源。</span><span class="sxs-lookup"><span data-stu-id="e54d4-111">Shares a resource on a server.</span></span>                                       |
| [<span data-ttu-id="e54d4-112">**NetShareCheck**</span><span class="sxs-lookup"><span data-stu-id="e54d4-112">**NetShareCheck**</span></span>](/windows/desktop/api/Lmshare/nf-lmshare-netsharecheck)     | <span data-ttu-id="e54d4-113">查詢伺服器是否正在共用裝置。</span><span class="sxs-lookup"><span data-stu-id="e54d4-113">Queries whether a server is sharing a device.</span></span>                        |
| [<span data-ttu-id="e54d4-114">**NetShareDel**</span><span class="sxs-lookup"><span data-stu-id="e54d4-114">**NetShareDel**</span></span>](/windows/desktop/api/Lmshare/nf-lmshare-netsharedel)         | <span data-ttu-id="e54d4-115">從伺服器的共用資源清單中刪除共用名稱。</span><span class="sxs-lookup"><span data-stu-id="e54d4-115">Deletes a share name from a server's list of shared resources.</span></span>       |
| [<span data-ttu-id="e54d4-116">**NetShareEnum**</span><span class="sxs-lookup"><span data-stu-id="e54d4-116">**NetShareEnum**</span></span>](/windows/desktop/api/Lmshare/nf-lmshare-netshareenum)       | <span data-ttu-id="e54d4-117">抓取伺服器上每個共用資源的共用資訊。</span><span class="sxs-lookup"><span data-stu-id="e54d4-117">Retrieves share information about each shared resource on a server.</span></span>  |
| [<span data-ttu-id="e54d4-118">**NetShareGetInfo**</span><span class="sxs-lookup"><span data-stu-id="e54d4-118">**NetShareGetInfo**</span></span>](/windows/desktop/api/Lmshare/nf-lmshare-netsharegetinfo) | <span data-ttu-id="e54d4-119">抓取伺服器上指定之共用資源的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="e54d4-119">Retrieves information about a specified shared resource on a server.</span></span> |
| [<span data-ttu-id="e54d4-120">**NetShareSetInfo**</span><span class="sxs-lookup"><span data-stu-id="e54d4-120">**NetShareSetInfo**</span></span>](/windows/desktop/api/Lmshare/nf-lmshare-netsharesetinfo) | <span data-ttu-id="e54d4-121">設定共用資源的參數。</span><span class="sxs-lookup"><span data-stu-id="e54d4-121">Sets a shared resource's parameters.</span></span>                                 |



 

<span data-ttu-id="e54d4-122">[**NetShareAdd**](/windows/desktop/api/Lmshare/nf-lmshare-netshareadd)函式可讓使用者或應用程式使用指定的共用名稱來共用特定類型的資源。</span><span class="sxs-lookup"><span data-stu-id="e54d4-122">The [**NetShareAdd**](/windows/desktop/api/Lmshare/nf-lmshare-netshareadd) function allows a user or application to share a resource of a specific type using the specified share name.</span></span> <span data-ttu-id="e54d4-123">**NetShareAdd** 函式需要共用名稱和本機裝置名稱，才能共用資源。</span><span class="sxs-lookup"><span data-stu-id="e54d4-123">The **NetShareAdd** function requires the share name and local device name to share the resource.</span></span> <span data-ttu-id="e54d4-124">使用者或應用程式必須具有伺服器上的帳戶，才能存取資源。</span><span class="sxs-lookup"><span data-stu-id="e54d4-124">A user or application must have an account on the server to access the resource.</span></span>

<span data-ttu-id="e54d4-125">您也可以指定要與共享相關聯的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="e54d4-125">You can also specify a security descriptor to be associated with a share.</span></span> <span data-ttu-id="e54d4-126">安全描述項會指定允許哪些使用者透過共用存取檔案，以及使用何種類型的存取權。</span><span class="sxs-lookup"><span data-stu-id="e54d4-126">Security descriptors specify which users are allowed to access files through the share, and with what type of access.</span></span> <span data-ttu-id="e54d4-127">呼叫 [**NetShareAdd**](/windows/desktop/api/Lmshare/nf-lmshare-netshareadd)或 [**NetShareSetInfo**](/windows/desktop/api/Lmshare/nf-lmshare-netsharesetinfo)時，請指定具有 [**共用 \_ 資訊 \_ 502**](/windows/desktop/api/Lmshare/ns-lmshare-share_info_502)資訊層級的 [**安全 \_ 描述項**](/windows/desktop/api/winnt/ns-winnt-security_descriptor)。</span><span class="sxs-lookup"><span data-stu-id="e54d4-127">Specify a [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) with the [**SHARE\_INFO\_502**](/windows/desktop/api/Lmshare/ns-lmshare-share_info_502) information level when calling [**NetShareAdd**](/windows/desktop/api/Lmshare/nf-lmshare-netshareadd) or [**NetShareSetInfo**](/windows/desktop/api/Lmshare/nf-lmshare-netsharesetinfo).</span></span> <span data-ttu-id="e54d4-128">**NetShareSetInfo** 支援 [**共用 \_ 資訊 \_ 1501**](/windows/desktop/api/Lmshare/ns-lmshare-share_info_1501) 資訊層級。</span><span class="sxs-lookup"><span data-stu-id="e54d4-128">**NetShareSetInfo** supports the [**SHARE\_INFO\_1501**](/windows/desktop/api/Lmshare/ns-lmshare-share_info_1501) information level.</span></span> <span data-ttu-id="e54d4-129">如需安全描述項的詳細資訊，請參閱 [存取控制](/windows/desktop/SecAuthZ/access-control)。</span><span class="sxs-lookup"><span data-stu-id="e54d4-129">For more information about security descriptors, see [Access Control](/windows/desktop/SecAuthZ/access-control).</span></span>

<span data-ttu-id="e54d4-130">網路管理功能會使用下列特殊的共用名稱來進行處理序間通訊 (IPC) 和伺服器的遠端系統管理：</span><span class="sxs-lookup"><span data-stu-id="e54d4-130">The network management functions use the following special share names for interprocess communication (IPC) and remote administration of the server:</span></span>

-   <span data-ttu-id="e54d4-131">IPC $，保留給處理序間通訊</span><span class="sxs-lookup"><span data-stu-id="e54d4-131">IPC$, reserved for interprocess communication</span></span>
-   <span data-ttu-id="e54d4-132">ADMIN $，保留給遠端系統管理</span><span class="sxs-lookup"><span data-stu-id="e54d4-132">ADMIN$, reserved for remote administration</span></span>
-   <span data-ttu-id="e54d4-133">$、B $、C $ (和其他本機磁片名稱，後面接著貨幣符號) ，指派給本機磁片裝置</span><span class="sxs-lookup"><span data-stu-id="e54d4-133">A$, B$, C$ (and other local disk names followed by a dollar sign), assigned to local disk devices</span></span>

<span data-ttu-id="e54d4-134">若要列出伺服器上共用資源的所有連線，或列出從特定電腦建立的所有連接，請呼叫 [**NetConnectionEnum**](/windows/desktop/api/Lmshare/nf-lmshare-netconnectionenum) 函數。</span><span class="sxs-lookup"><span data-stu-id="e54d4-134">To list all connections made to a shared resource on a server, or to list all connections established from a particular computer, call the [**NetConnectionEnum**](/windows/desktop/api/Lmshare/nf-lmshare-netconnectionenum) function.</span></span> <span data-ttu-id="e54d4-135">您可以在 [**連接 \_ 資訊 \_ 0**](/windows/desktop/api/Lmshare/ns-lmshare-connection_info_0)和 [**連接 \_ 資訊 \_ 1**](/windows/desktop/api/Lmshare/ns-lmshare-connection_info_1)資訊層級呼叫 **NetConnectionEnum** 。</span><span class="sxs-lookup"><span data-stu-id="e54d4-135">You can call **NetConnectionEnum** at the [**CONNECTION\_INFO\_0**](/windows/desktop/api/Lmshare/ns-lmshare-connection_info_0) and [**CONNECTION\_INFO\_1**](/windows/desktop/api/Lmshare/ns-lmshare-connection_info_1) information levels.</span></span>

<span data-ttu-id="e54d4-136">共用功能可在下列資訊層級取得：</span><span class="sxs-lookup"><span data-stu-id="e54d4-136">Share functions are available at the following information levels:</span></span>

<dl>

[<span data-ttu-id="e54d4-137">**共用 \_ 資訊 \_ 0**</span><span class="sxs-lookup"><span data-stu-id="e54d4-137">**SHARE\_INFO\_0**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-share_info_0)  
[<span data-ttu-id="e54d4-138">**共用 \_ 資訊 \_ 1**</span><span class="sxs-lookup"><span data-stu-id="e54d4-138">**SHARE\_INFO\_1**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-share_info_1)  
[<span data-ttu-id="e54d4-139">**共用 \_ 資訊 \_ 2**</span><span class="sxs-lookup"><span data-stu-id="e54d4-139">**SHARE\_INFO\_2**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-share_info_2)  
[<span data-ttu-id="e54d4-140">**共用 \_ 資訊 \_ 501**</span><span class="sxs-lookup"><span data-stu-id="e54d4-140">**SHARE\_INFO\_501**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-share_info_501)  
[<span data-ttu-id="e54d4-141">**共用 \_ 資訊 \_ 502**</span><span class="sxs-lookup"><span data-stu-id="e54d4-141">**SHARE\_INFO\_502**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-share_info_502)  
[<span data-ttu-id="e54d4-142">**共用 \_ 資訊 \_ 1005**</span><span class="sxs-lookup"><span data-stu-id="e54d4-142">**SHARE\_INFO\_1005**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-share_info_1005)  
</dl>

<span data-ttu-id="e54d4-143">下列資訊層級只對 [**NetShareSetInfo**](/windows/desktop/api/Lmshare/nf-lmshare-netsharesetinfo)有效：</span><span class="sxs-lookup"><span data-stu-id="e54d4-143">The following information levels are valid only for [**NetShareSetInfo**](/windows/desktop/api/Lmshare/nf-lmshare-netsharesetinfo):</span></span>

<dl>

[<span data-ttu-id="e54d4-144">**共用 \_ 資訊 \_ 1004**</span><span class="sxs-lookup"><span data-stu-id="e54d4-144">**SHARE\_INFO\_1004**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-share_info_1004)  
[<span data-ttu-id="e54d4-145">**共用 \_ 資訊 \_ 1006**</span><span class="sxs-lookup"><span data-stu-id="e54d4-145">**SHARE\_INFO\_1006**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-share_info_1006)  
[<span data-ttu-id="e54d4-146">**共用 \_ 資訊 \_ 1501**</span><span class="sxs-lookup"><span data-stu-id="e54d4-146">**SHARE\_INFO\_1501**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-share_info_1501)  
</dl>

<span data-ttu-id="e54d4-147">如果您正在針對 Active Directory 進行程式設計，您可以呼叫特定 Active Directory 服務介面 (ADSI) 方法，以取得您可以藉由呼叫網路管理共用功能來達成的相同功能。</span><span class="sxs-lookup"><span data-stu-id="e54d4-147">If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same functionality you can achieve by calling the network management share functions.</span></span> <span data-ttu-id="e54d4-148">如需詳細資訊，請參閱 [**IADsFileShare**](/windows/desktop/api/iads/nn-iads-iadsfileshare)。</span><span class="sxs-lookup"><span data-stu-id="e54d4-148">For more information, see [**IADsFileShare**](/windows/desktop/api/iads/nn-iads-iadsfileshare).</span></span>

 

 

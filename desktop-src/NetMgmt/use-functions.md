---
title: 使用函式
description: 網路管理使用功能檢查和管理連線 (在工作站和伺服器之間使用) 。 使用函數如下所示。
ms.assetid: ddf1b8dc-f13b-402a-9e4e-e4944a29ac31
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbd2660b911fd87c39b9db10b0dbfea0e47c484c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842639"
---
# <a name="use-functions"></a><span data-ttu-id="d9d2b-104">使用函式</span><span class="sxs-lookup"><span data-stu-id="d9d2b-104">Use Functions</span></span>

<span data-ttu-id="d9d2b-105">網路管理使用功能檢查和管理連線 (在工作站和伺服器之間使用) 。</span><span class="sxs-lookup"><span data-stu-id="d9d2b-105">The network management use functions examine and manage connections (uses) between workstations and servers.</span></span> <span data-ttu-id="d9d2b-106">使用函數如下所示。</span><span class="sxs-lookup"><span data-stu-id="d9d2b-106">The use functions are listed following.</span></span>



| <span data-ttu-id="d9d2b-107">函式</span><span class="sxs-lookup"><span data-stu-id="d9d2b-107">Function</span></span>                               | <span data-ttu-id="d9d2b-108">描述</span><span class="sxs-lookup"><span data-stu-id="d9d2b-108">Description</span></span>                                                                               |
|----------------------------------------|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d9d2b-109">**NetUseAdd**</span><span class="sxs-lookup"><span data-stu-id="d9d2b-109">**NetUseAdd**</span></span>](/windows/desktop/api/Lmuse/nf-lmuse-netuseadd)         | <span data-ttu-id="d9d2b-110">在本機電腦與伺服器之間建立連線。</span><span class="sxs-lookup"><span data-stu-id="d9d2b-110">Creates a connection between a local computer and a server.</span></span>                               |
| [<span data-ttu-id="d9d2b-111">**NetUseDel**</span><span class="sxs-lookup"><span data-stu-id="d9d2b-111">**NetUseDel**</span></span>](/windows/desktop/api/Lmuse/nf-lmuse-netusedel)         | <span data-ttu-id="d9d2b-112">結束共用資源的連接。</span><span class="sxs-lookup"><span data-stu-id="d9d2b-112">Ends a connection to a shared resource.</span></span>                                                   |
| [<span data-ttu-id="d9d2b-113">**NetUseEnum**</span><span class="sxs-lookup"><span data-stu-id="d9d2b-113">**NetUseEnum**</span></span>](/windows/desktop/api/Lmuse/nf-lmuse-netuseenum)       | <span data-ttu-id="d9d2b-114">列出本機電腦與遠端伺服器上的資源之間的所有目前連接。</span><span class="sxs-lookup"><span data-stu-id="d9d2b-114">Lists all current connections between the local computer and resources on remote servers.</span></span> |
| [<span data-ttu-id="d9d2b-115">**NetUseGetInfo**</span><span class="sxs-lookup"><span data-stu-id="d9d2b-115">**NetUseGetInfo**</span></span>](/windows/desktop/api/Lmuse/nf-lmuse-netusegetinfo) | <span data-ttu-id="d9d2b-116">傳回共用資源連接的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d9d2b-116">Returns information about a connection to a shared resource.</span></span>                              |



 

<span data-ttu-id="d9d2b-117">這些函式只適用于 (LAN Manager 工作站) 用戶端的伺服器訊息區。</span><span class="sxs-lookup"><span data-stu-id="d9d2b-117">These function applies only to the Server Message Block (LAN Manager Workstation) client.</span></span> <span data-ttu-id="d9d2b-118">**NetUseGetInfo** 函數不支援 (DFS) 共用分散式檔案系統。</span><span class="sxs-lookup"><span data-stu-id="d9d2b-118">The **NetUseGetInfo** function does not support Distributed File System (DFS) shares.</span></span> <span data-ttu-id="d9d2b-119">若要使用不同的網路提供者來抓取共用資源的連接資訊 (WebDAV 或 DFS 共用（例如) ），請使用 [**WNetGetConnection**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetgetconnectiona) 函式。</span><span class="sxs-lookup"><span data-stu-id="d9d2b-119">To retrieve connection information for a shared resource using a different network provider (WebDAV or a DFS share, for example), use the [**WNetGetConnection**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetgetconnectiona) function.</span></span>

<span data-ttu-id="d9d2b-120">連接會從會話辨別：當工作站第一次建立與伺服器上共用資源的連接時，就會建立 *會話* 。</span><span class="sxs-lookup"><span data-stu-id="d9d2b-120">Connections are distinguished from sessions: a *session* is established the first time a workstation makes a connection to a shared resource on the server.</span></span> <span data-ttu-id="d9d2b-121">在會話結束之前，工作站和伺服器之間的所有其他連線都是此相同會話的一部分。</span><span class="sxs-lookup"><span data-stu-id="d9d2b-121">All additional connections between the workstation and the server are part of this same session until the session ends.</span></span> <span data-ttu-id="d9d2b-122">您可以建立兩種類型的連線：裝置名稱連接 (只能是明確的) 和通用命名慣例 (UNC) 連接 (可以是明確或隱含的) 。</span><span class="sxs-lookup"><span data-stu-id="d9d2b-122">Two types of connections can be made: device-name connections (which can only be explicit) and universal-naming convention (UNC) connections (which can be explicit or implicit).</span></span>

<span data-ttu-id="d9d2b-123">*連接* 是以每個使用者為基礎進行。</span><span class="sxs-lookup"><span data-stu-id="d9d2b-123">*Connections* are made on a per-user basis.</span></span> <span data-ttu-id="d9d2b-124">當使用者登出時，就會刪除使用者所建立的連接。</span><span class="sxs-lookup"><span data-stu-id="d9d2b-124">A connection made by a user is deleted when that user logs off.</span></span> <span data-ttu-id="d9d2b-125">基於這個理由，網路管理使用的功能只在本機，因為任何其他使用者都無法存取由遠端使用者設定的連線，即使是以互動方式登入該電腦的使用者也是如此。</span><span class="sxs-lookup"><span data-stu-id="d9d2b-125">For this reason the network management use functions are local only, because a connection set up by a remote user would not be accessible to any other users, even the user that was interactively logged on to that computer.</span></span>

<span data-ttu-id="d9d2b-126">[**NetUseAdd**](/windows/desktop/api/Lmuse/nf-lmuse-netuseadd)函式會將本機裝置名稱重新導向至遠端伺服器資源的共用名稱（ (\\ \\ *servername* \\ *共用*) ），藉此在本機電腦和伺服器上共用的資源之間建立明確的連接。</span><span class="sxs-lookup"><span data-stu-id="d9d2b-126">The [**NetUseAdd**](/windows/desktop/api/Lmuse/nf-lmuse-netuseadd) function establishes an explicit connection between the local computer and a resource shared on a server by redirecting a local device name to the share name of a remote server resource (\\\\*servername*\\*sharename*).</span></span> <span data-ttu-id="d9d2b-127">建立裝置名稱連接之後，使用者或應用程式可以藉由指定本機裝置名稱，來使用遠端資源。</span><span class="sxs-lookup"><span data-stu-id="d9d2b-127">Once a device-name connection is made, users or applications can use the remote resource by specifying the local device name.</span></span>

<span data-ttu-id="d9d2b-128">隱含 UNC 連接是由負責連接的函式所組成。</span><span class="sxs-lookup"><span data-stu-id="d9d2b-128">Implicit UNC connections are made by the function responsible for the connection.</span></span> <span data-ttu-id="d9d2b-129">若要建立隱含的 UNC 連接，應用程式會將資源的共用名稱傳遞給接受 UNC 路徑的任何函式。</span><span class="sxs-lookup"><span data-stu-id="d9d2b-129">To establish an implicit UNC connection, an application passes the share name of a resource to any function that accepts UNC paths.</span></span> <span data-ttu-id="d9d2b-130">此函式會接受 UNC 名稱，並連接到指定的共用名稱。</span><span class="sxs-lookup"><span data-stu-id="d9d2b-130">The function accepts the UNC name and makes a connection to the specified share name.</span></span> <span data-ttu-id="d9d2b-131">此連接上的所有進一步要求都需要完整的共用名稱。</span><span class="sxs-lookup"><span data-stu-id="d9d2b-131">All further requests on this connection require the full share name.</span></span>

<span data-ttu-id="d9d2b-132">使用函式適用于下列資訊層級：</span><span class="sxs-lookup"><span data-stu-id="d9d2b-132">The use functions are available at the following information levels:</span></span>

-   [<span data-ttu-id="d9d2b-133">**使用 \_ 資訊 \_ 0**</span><span class="sxs-lookup"><span data-stu-id="d9d2b-133">**USE\_INFO\_0**</span></span>](/windows/desktop/api/Lmuse/ns-lmuse-use_info_0)
-   [<span data-ttu-id="d9d2b-134">**使用 \_ 資訊 \_ 1**</span><span class="sxs-lookup"><span data-stu-id="d9d2b-134">**USE\_INFO\_1**</span></span>](/windows/desktop/api/Lmuse/ns-lmuse-use_info_1)
-   [<span data-ttu-id="d9d2b-135">**使用 \_ 資訊 \_ 2**</span><span class="sxs-lookup"><span data-stu-id="d9d2b-135">**USE\_INFO\_2**</span></span>](/windows/desktop/api/Lmuse/ns-lmuse-use_info_2)

 

 
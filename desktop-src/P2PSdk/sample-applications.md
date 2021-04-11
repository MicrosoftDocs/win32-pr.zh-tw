---
title: " (對等基礎結構) 的範例應用程式"
description: 下列範例應用程式包含在 Windows XP 對等 SDK 中。
ms.assetid: 26c45360-f232-4e29-90b5-44ccacb5a9c3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c15e2bf3162151a4cbf18547fdfe482c7ea77fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944276"
---
# <a name="sample-applications-peer-infrastructure"></a><span data-ttu-id="83d6b-103"> (對等基礎結構) 的範例應用程式</span><span class="sxs-lookup"><span data-stu-id="83d6b-103">Sample applications (Peer Infrastructure)</span></span>

<span data-ttu-id="83d6b-104">下列範例應用程式包含在 Windows XP 對等 SDK 中。</span><span class="sxs-lookup"><span data-stu-id="83d6b-104">The following sample applications are included in the Windows XP Peer SDK.</span></span> <span data-ttu-id="83d6b-105">當您使用對等基礎結構開發自己的對等應用程式時，這些範例可協助您。</span><span class="sxs-lookup"><span data-stu-id="83d6b-105">The samples can help you when you develop your own peer applications using the Peer Infrastructure.</span></span>

-   [<span data-ttu-id="83d6b-106">圖形聊天</span><span class="sxs-lookup"><span data-stu-id="83d6b-106">Graph Chat</span></span>](#graph-chat)
-   [<span data-ttu-id="83d6b-107">群組聊天</span><span class="sxs-lookup"><span data-stu-id="83d6b-107">Group Chat</span></span>](#group-chat)
-   [<span data-ttu-id="83d6b-108">群組瀏覽器</span><span class="sxs-lookup"><span data-stu-id="83d6b-108">Group Browser</span></span>](#group-browser)

## <a name="graph-chat"></a><span data-ttu-id="83d6b-109">圖形聊天</span><span class="sxs-lookup"><span data-stu-id="83d6b-109">Graph Chat</span></span>

<span data-ttu-id="83d6b-110">圖形聊天範例應用程式是簡單的聊天應用程式，示範如何使用對等圖形 Api 和對等名稱解析通訊協定 (PNRP) 命名空間提供者搭配 Winsock 2 API。</span><span class="sxs-lookup"><span data-stu-id="83d6b-110">The Graph Chat sample application is a simple chat application that demonstrates how to use the Peer Graphing APIs and the Peer Name Resolution Protocol (PNRP) Namespace Provider with the Winsock 2 API.</span></span> <span data-ttu-id="83d6b-111">應用程式會示範下列工作：</span><span class="sxs-lookup"><span data-stu-id="83d6b-111">The application demonstrates the following tasks:</span></span>

-   <span data-ttu-id="83d6b-112">建立圖形</span><span class="sxs-lookup"><span data-stu-id="83d6b-112">Creating a graph</span></span>
-   <span data-ttu-id="83d6b-113">連接至現有的圖形</span><span class="sxs-lookup"><span data-stu-id="83d6b-113">Connecting to an existing graph</span></span>
-   <span data-ttu-id="83d6b-114">中斷與現有圖形的連線</span><span class="sxs-lookup"><span data-stu-id="83d6b-114">Disconnecting from an existing graph</span></span>
-   <span data-ttu-id="83d6b-115">列舉對等實體</span><span class="sxs-lookup"><span data-stu-id="83d6b-115">Enumerating peer entities</span></span>
-   <span data-ttu-id="83d6b-116">將記錄新增至圖形</span><span class="sxs-lookup"><span data-stu-id="83d6b-116">Adding records to the graph</span></span>
-   <span data-ttu-id="83d6b-117">使用圖表的直接連接</span><span class="sxs-lookup"><span data-stu-id="83d6b-117">Using direct connections with a graph</span></span>
-   <span data-ttu-id="83d6b-118">使用通知和事件基礎結構與圖形</span><span class="sxs-lookup"><span data-stu-id="83d6b-118">Using the notification and event infrastructure with graphs</span></span>
-   <span data-ttu-id="83d6b-119">使用 PNRP 註冊名稱</span><span class="sxs-lookup"><span data-stu-id="83d6b-119">Registering names with PNRP</span></span>
-   <span data-ttu-id="83d6b-120">使用 PNRP 解析名稱</span><span class="sxs-lookup"><span data-stu-id="83d6b-120">Resolving names with PNRP</span></span>
-   <span data-ttu-id="83d6b-121">使用 PNRP 取消註冊名稱</span><span class="sxs-lookup"><span data-stu-id="83d6b-121">Unregistering names with PNRP</span></span>

## <a name="group-chat"></a><span data-ttu-id="83d6b-122">群組聊天</span><span class="sxs-lookup"><span data-stu-id="83d6b-122">Group Chat</span></span>

<span data-ttu-id="83d6b-123">群組聊天範例應用程式是簡單的聊天應用程式，示範如何使用對等群組和 Identity Manager Api。</span><span class="sxs-lookup"><span data-stu-id="83d6b-123">The Group Chat sample application is a simple chat application that demonstrates how to use the Peer Grouping and Identity Manager APIs.</span></span> <span data-ttu-id="83d6b-124">應用程式會示範下列工作：</span><span class="sxs-lookup"><span data-stu-id="83d6b-124">The application demonstrates the following tasks:</span></span>

-   <span data-ttu-id="83d6b-125">建立身分識別</span><span class="sxs-lookup"><span data-stu-id="83d6b-125">Creating an identity</span></span>
-   <span data-ttu-id="83d6b-126">建立和取得身分識別資訊</span><span class="sxs-lookup"><span data-stu-id="83d6b-126">Creating and obtaining identity information</span></span>
-   <span data-ttu-id="83d6b-127">列舉身分識別</span><span class="sxs-lookup"><span data-stu-id="83d6b-127">Enumerating identities</span></span>
-   <span data-ttu-id="83d6b-128">列舉與身分識別相關聯的群組</span><span class="sxs-lookup"><span data-stu-id="83d6b-128">Enumerating groups associated with an identity</span></span>
-   <span data-ttu-id="83d6b-129">建立群組</span><span class="sxs-lookup"><span data-stu-id="83d6b-129">Creating a group</span></span>
-   <span data-ttu-id="83d6b-130">建立群組的邀請</span><span class="sxs-lookup"><span data-stu-id="83d6b-130">Creating invitations for a group</span></span>
-   <span data-ttu-id="83d6b-131">連接至現有的群組</span><span class="sxs-lookup"><span data-stu-id="83d6b-131">Connecting to an existing group</span></span>
-   <span data-ttu-id="83d6b-132">中斷與現有群組的連接</span><span class="sxs-lookup"><span data-stu-id="83d6b-132">Disconnecting from an existing group</span></span>
-   <span data-ttu-id="83d6b-133">從群組屬性中解壓縮資訊</span><span class="sxs-lookup"><span data-stu-id="83d6b-133">Extracting information from the group properties</span></span>
-   <span data-ttu-id="83d6b-134">使用直接連接與群組</span><span class="sxs-lookup"><span data-stu-id="83d6b-134">Using direct connections with a group</span></span>
-   <span data-ttu-id="83d6b-135">使用群組中的列舉函數</span><span class="sxs-lookup"><span data-stu-id="83d6b-135">Using the enumeration functions within a group</span></span>
-   <span data-ttu-id="83d6b-136">列舉群組成員</span><span class="sxs-lookup"><span data-stu-id="83d6b-136">Enumerating group members</span></span>
-   <span data-ttu-id="83d6b-137">將記錄新增至群組</span><span class="sxs-lookup"><span data-stu-id="83d6b-137">Adding records to a group</span></span>
-   <span data-ttu-id="83d6b-138">使用通知和事件基礎結構與群組</span><span class="sxs-lookup"><span data-stu-id="83d6b-138">Using the notification and event infrastructure with groups</span></span>

## <a name="group-browser"></a><span data-ttu-id="83d6b-139">群組瀏覽器</span><span class="sxs-lookup"><span data-stu-id="83d6b-139">Group Browser</span></span>

<span data-ttu-id="83d6b-140">群組瀏覽器範例應用程式是簡單的對等群組管理工具，示範如何使用對等群組和 Identity Manager Api。</span><span class="sxs-lookup"><span data-stu-id="83d6b-140">The Group Browser sample application is a simple peer group management tool that demonstrates how to use the Peer Grouping and Identity Manager APIs.</span></span> <span data-ttu-id="83d6b-141">應用程式會示範下列工作：</span><span class="sxs-lookup"><span data-stu-id="83d6b-141">The application demonstrates the following tasks:</span></span>

-   <span data-ttu-id="83d6b-142">列舉 PNRP 雲端</span><span class="sxs-lookup"><span data-stu-id="83d6b-142">Enumerating PNRP clouds</span></span>
-   <span data-ttu-id="83d6b-143">列舉身分識別</span><span class="sxs-lookup"><span data-stu-id="83d6b-143">Enumerating identities</span></span>
-   <span data-ttu-id="83d6b-144">列舉與身分識別相關聯的群組</span><span class="sxs-lookup"><span data-stu-id="83d6b-144">Enumerating groups associated with an identity</span></span>
-   <span data-ttu-id="83d6b-145">建立和刪除身分識別</span><span class="sxs-lookup"><span data-stu-id="83d6b-145">Creating and deleting identities</span></span>
-   <span data-ttu-id="83d6b-146">建立群組，並將其與身分識別建立關聯</span><span class="sxs-lookup"><span data-stu-id="83d6b-146">Creating a group and associating it with an identity</span></span>
-   <span data-ttu-id="83d6b-147">建立並儲存邀請</span><span class="sxs-lookup"><span data-stu-id="83d6b-147">Creating an invitation and saving it</span></span>
-   <span data-ttu-id="83d6b-148">開啟邀請並使用它來加入群組</span><span class="sxs-lookup"><span data-stu-id="83d6b-148">Opening an invitation and using it to join a group</span></span>
-   <span data-ttu-id="83d6b-149">刪除身分識別和群組成員資格</span><span class="sxs-lookup"><span data-stu-id="83d6b-149">Deleting an identity and group membership</span></span>
-   <span data-ttu-id="83d6b-150">連接至現有的群組</span><span class="sxs-lookup"><span data-stu-id="83d6b-150">Connecting to an existing group</span></span>
-   <span data-ttu-id="83d6b-151">中斷與現有群組的連接</span><span class="sxs-lookup"><span data-stu-id="83d6b-151">Disconnecting from an existing group</span></span>
-   <span data-ttu-id="83d6b-152">從群組屬性解壓縮資訊</span><span class="sxs-lookup"><span data-stu-id="83d6b-152">Extracting information from group properties</span></span>
-   <span data-ttu-id="83d6b-153">使用群組中的列舉函數</span><span class="sxs-lookup"><span data-stu-id="83d6b-153">Using the enumeration functions within a group</span></span>
-   <span data-ttu-id="83d6b-154">列舉群組成員</span><span class="sxs-lookup"><span data-stu-id="83d6b-154">Enumerating group members</span></span>
-   <span data-ttu-id="83d6b-155">使用通知和事件基礎結構與群組</span><span class="sxs-lookup"><span data-stu-id="83d6b-155">Using the notification and event infrastructure with groups</span></span>

 

 




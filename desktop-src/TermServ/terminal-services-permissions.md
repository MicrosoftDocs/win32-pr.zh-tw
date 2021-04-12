---
title: 遠端桌面服務許可權
description: 您可以使用提供給遠端桌面服務的許可權，來控制使用者和群組存取伺服器的方式。
ms.assetid: 448a7f9b-bf12-48eb-a3e7-4512ec288d95
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f1358a4360889bc013beefcee4e029f3572c9c0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375549"
---
# <a name="remote-desktop-services-permissions"></a><span data-ttu-id="df54b-103">遠端桌面服務許可權</span><span class="sxs-lookup"><span data-stu-id="df54b-103">Remote Desktop Services permissions</span></span>

<span data-ttu-id="df54b-104">您可以使用提供給遠端桌面服務的許可權，來控制使用者和群組存取伺服器的方式。</span><span class="sxs-lookup"><span data-stu-id="df54b-104">You can use the permissions provided for Remote Desktop Services to control how users and groups access the server.</span></span> <span data-ttu-id="df54b-105">如需預設許可權類型的描述，以及一般遠端桌面服務許可權的詳細資訊，請參閱遠端桌面服務設定系統管理工具隨附的檔。</span><span class="sxs-lookup"><span data-stu-id="df54b-105">For a description of the default permission types and more detailed information about Remote Desktop Services permissions in general, see the documentation that accompanies the Remote Desktop Services Configuration administrative tool.</span></span> <span data-ttu-id="df54b-106">如需有關為 Windows Server 2008 設定這些許可權的詳細資訊，請參閱 [設定遠端桌面服務連接的許可權](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc753032(v=ws.11))。</span><span class="sxs-lookup"><span data-stu-id="df54b-106">For information about configuring these permissions for Windows Server 2008, see [Configure Permissions for Remote Desktop Services Connections](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc753032(v=ws.11)).</span></span>

<span data-ttu-id="df54b-107">以下是您可以設定的許可權清單，以及許可權允許的工作。</span><span class="sxs-lookup"><span data-stu-id="df54b-107">Following is a list of the permissions that you can set and the tasks the permissions allow.</span></span>



| <span data-ttu-id="df54b-108">值</span><span class="sxs-lookup"><span data-stu-id="df54b-108">Value</span></span>                        | <span data-ttu-id="df54b-109">意義</span><span class="sxs-lookup"><span data-stu-id="df54b-109">Meaning</span></span>                                                                                                                                                               |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df54b-110">查詢資訊</span><span class="sxs-lookup"><span data-stu-id="df54b-110">Query Information</span></span><br/> | <span data-ttu-id="df54b-111">查詢會話和伺服器以取得資訊。</span><span class="sxs-lookup"><span data-stu-id="df54b-111">Query sessions and servers for information.</span></span><br/>                                                                                                                |
| <span data-ttu-id="df54b-112">設定資訊</span><span class="sxs-lookup"><span data-stu-id="df54b-112">Set Information</span></span><br/>   | <span data-ttu-id="df54b-113">設定連接屬性。</span><span class="sxs-lookup"><span data-stu-id="df54b-113">Configure connection properties.</span></span><br/>                                                                                                                           |
| <span data-ttu-id="df54b-114">遠端控制</span><span class="sxs-lookup"><span data-stu-id="df54b-114">Remote Control</span></span><br/>    | <span data-ttu-id="df54b-115">查看或主動控制其他使用者的會話。</span><span class="sxs-lookup"><span data-stu-id="df54b-115">View or actively control another user's session.</span></span><br/>                                                                                                           |
| <span data-ttu-id="df54b-116">登入</span><span class="sxs-lookup"><span data-stu-id="df54b-116">Logon</span></span><br/>             | <span data-ttu-id="df54b-117">登入伺服器上的會話。</span><span class="sxs-lookup"><span data-stu-id="df54b-117">Log on to a session on the server.</span></span><br/>                                                                                                                         |
| <span data-ttu-id="df54b-118">Logoff</span><span class="sxs-lookup"><span data-stu-id="df54b-118">Logoff</span></span><br/>            | <span data-ttu-id="df54b-119">將使用者登出會話。</span><span class="sxs-lookup"><span data-stu-id="df54b-119">Log off a user from a session.</span></span> <span data-ttu-id="df54b-120">請注意，在沒有警告的情況下登出使用者可能會導致用戶端的資料遺失。</span><span class="sxs-lookup"><span data-stu-id="df54b-120">Be aware that logging off a user without warning can result in loss of data at the client.</span></span><br/>                                  |
| <span data-ttu-id="df54b-121">訊息</span><span class="sxs-lookup"><span data-stu-id="df54b-121">Message</span></span><br/>           | <span data-ttu-id="df54b-122">傳送訊息給其他使用者的會話。</span><span class="sxs-lookup"><span data-stu-id="df54b-122">Send a message to another user's sessions.</span></span><br/>                                                                                                                 |
| <span data-ttu-id="df54b-123">連線</span><span class="sxs-lookup"><span data-stu-id="df54b-123">Connect</span></span><br/>           | <span data-ttu-id="df54b-124">連接到另一個會話。</span><span class="sxs-lookup"><span data-stu-id="df54b-124">Connect to another session.</span></span><br/>                                                                                                                                |
| <span data-ttu-id="df54b-125">中斷連線</span><span class="sxs-lookup"><span data-stu-id="df54b-125">Disconnect</span></span><br/>        | <span data-ttu-id="df54b-126">中斷會話的連線。</span><span class="sxs-lookup"><span data-stu-id="df54b-126">Disconnect a session.</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="df54b-127">虛擬通道</span><span class="sxs-lookup"><span data-stu-id="df54b-127">Virtual Channels</span></span><br/>  | <span data-ttu-id="df54b-128">使用虛擬通道。</span><span class="sxs-lookup"><span data-stu-id="df54b-128">Use virtual channels.</span></span> <span data-ttu-id="df54b-129">請注意，關閉虛擬通道會停用某些遠端桌面服務功能，例如剪貼簿和印表機重新導向。</span><span class="sxs-lookup"><span data-stu-id="df54b-129">Be aware that turning off virtual channels disables some Remote Desktop Services features such as clipboard and printer redirection.</span></span><br/> |
| <span data-ttu-id="df54b-130">重設</span><span class="sxs-lookup"><span data-stu-id="df54b-130">Reset</span></span><br/>             | <span data-ttu-id="df54b-131">結束會話。</span><span class="sxs-lookup"><span data-stu-id="df54b-131">End a session.</span></span> <span data-ttu-id="df54b-132">請注意，在沒有警告的情況下結束會話可能會導致用戶端的資料遺失。</span><span class="sxs-lookup"><span data-stu-id="df54b-132">Be aware that ending a session without warning can result in loss of data at the client.</span></span><br/>                                                    |



 

<span data-ttu-id="df54b-133">需要登入許可權，使用者才能登入新的遠端桌面服務會話。</span><span class="sxs-lookup"><span data-stu-id="df54b-133">The Logon permission is required for a user to log on to a new Remote Desktop Services session.</span></span> <span data-ttu-id="df54b-134">所有其他遠端桌面服務許可權都適用于控制其他使用者的遠端桌面服務會話。</span><span class="sxs-lookup"><span data-stu-id="df54b-134">All other Remote Desktop Services permissions apply to controlling another user's Remote Desktop Services session.</span></span>

<span data-ttu-id="df54b-135">您可以針對個別使用者或群組授與或設定遠端桌面服務許可權。</span><span class="sxs-lookup"><span data-stu-id="df54b-135">Remote Desktop Services permissions can be granted, or set, for individual users or groups.</span></span> <span data-ttu-id="df54b-136">使用者也可以由於成為群組成員而繼承許可權。</span><span class="sxs-lookup"><span data-stu-id="df54b-136">Users can also inherit permissions as a result of being a group member.</span></span> <span data-ttu-id="df54b-137">不過，拒絕許可權會覆寫繼承的許可權。</span><span class="sxs-lookup"><span data-stu-id="df54b-137">The denial of a permission, however, overrides an inherited permission.</span></span> <span data-ttu-id="df54b-138">例如，遠端桌面使用者 (RDU) 群組的成員預設會獲得查詢許可權。</span><span class="sxs-lookup"><span data-stu-id="df54b-138">For example, members of the Remote Desktop Users (RDU) group are granted the Query permission by default.</span></span> <span data-ttu-id="df54b-139">如果系統管理員將該使用者的查詢許可權設定為 [拒絕]，使用者將無法查詢另一個使用者的會話。</span><span class="sxs-lookup"><span data-stu-id="df54b-139">If an Administrator sets the Query permission to "Deny" for that user, the user will not be able to query another user's session.</span></span> <span data-ttu-id="df54b-140">使用者登入會話之後，就會授與使用者會話的所有其他遠端桌面服務許可權。</span><span class="sxs-lookup"><span data-stu-id="df54b-140">After a user logs on to a session, the user is granted all other Remote Desktop Services permissions for his or her session.</span></span>

## <a name="related-topics"></a><span data-ttu-id="df54b-141">相關主題</span><span class="sxs-lookup"><span data-stu-id="df54b-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df54b-142">遠端桌面服務管理應用程式</span><span class="sxs-lookup"><span data-stu-id="df54b-142">Remote Desktop Services management applications</span></span>](terminal-services-management-applications.md)
</dt> <dt>

[<span data-ttu-id="df54b-143">**Win32 \_ TSAccount**</span><span class="sxs-lookup"><span data-stu-id="df54b-143">**Win32\_TSAccount**</span></span>](win32-tsaccount.md)
</dt> </dl>

 


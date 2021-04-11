---
description: 當使用者或群組的成員不應再獲得指派給角色的應用程式資源存取權時，您可以從角色中移除使用者帳戶或群組。
ms.assetid: d2cfa5cb-a143-41de-9aa2-7af7fce10ed7
title: 將使用者帳戶或群組移至不同的角色
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2401d792066212269d4eaa4eb11eadfef6e2d73e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111289"
---
# <a name="moving-a-user-account-or-group-to-a-different-role"></a><span data-ttu-id="042c7-103">將使用者帳戶或群組移至不同的角色</span><span class="sxs-lookup"><span data-stu-id="042c7-103">Moving a User Account or Group to a Different Role</span></span>

<span data-ttu-id="042c7-104">當使用者或群組的成員不應再獲得指派給角色的應用程式資源存取權時，您可以從角色中移除使用者帳戶或群組。</span><span class="sxs-lookup"><span data-stu-id="042c7-104">You can remove user accounts or groups from a role when the users or members of the groups should no longer be given access to the application resources to which the role is assigned.</span></span>

<span data-ttu-id="042c7-105">**若要從角色移除使用者帳戶或群組**</span><span class="sxs-lookup"><span data-stu-id="042c7-105">**To remove a user account or group from a role**</span></span>

1.  <span data-ttu-id="042c7-106">在 [元件服務] 系統管理工具的主控台樹中，找出包含您感興趣之角色的 COM + 應用程式。</span><span class="sxs-lookup"><span data-stu-id="042c7-106">In the console tree of the Component Services administrative tool, locate the COM+ application that contains the role you are interested in.</span></span> <span data-ttu-id="042c7-107">在主控台樹中展開視圖，直到角色的使用者可以看見為止。</span><span class="sxs-lookup"><span data-stu-id="042c7-107">Expand the view in the console tree until the users for the role are visible.</span></span>

2.  <span data-ttu-id="042c7-108">以滑鼠右鍵按一下您要移除的使用者帳戶或群組，然後按一下 [ **刪除**]。</span><span class="sxs-lookup"><span data-stu-id="042c7-108">Right-click the user account or group you want to remove, and then click **Delete**.</span></span>

3.  <span data-ttu-id="042c7-109">當 [ **確認專案刪除** ] 對話方塊出現提示時，請按一下 [ **是]** 以刪除使用者帳戶或群組。</span><span class="sxs-lookup"><span data-stu-id="042c7-109">When prompted by the **Confirm Item Delete** dialog box, click **Yes** to delete the user account or group.</span></span>

<span data-ttu-id="042c7-110">您從角色移除的使用者帳戶或群組不會再出現在 [ **使用者** ] 資料夾中。</span><span class="sxs-lookup"><span data-stu-id="042c7-110">The user account or group that you have removed from the role no longer appears in the **Users** folder.</span></span> <span data-ttu-id="042c7-111">新的角色成員資格會在應用程式下次啟動時生效。</span><span class="sxs-lookup"><span data-stu-id="042c7-111">The new role membership takes effect the next time the application is started.</span></span> <span data-ttu-id="042c7-112">如果您已對 **系統應用程式** 進行變更，您必須重新開機電腦，變更才會生效。</span><span class="sxs-lookup"><span data-stu-id="042c7-112">If you have made changes to the **System Application**, you must restart the computer for the changes to take effect.</span></span>

 

 




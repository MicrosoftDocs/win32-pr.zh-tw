---
description: 如果使用者的許可權變更或角色已新增至應用程式，您可以將帳戶從一個角色移至另一個角色。
ms.assetid: 2d81a45a-9762-48b9-8395-3c3a4dcd5e8c
title: 從角色中移除使用者帳戶或群組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 176272aef16af0d0a65d90f6a1d7628a5af232fc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970116"
---
# <a name="removing-a-user-account-or-group-from-a-role"></a><span data-ttu-id="b2eca-103">從角色中移除使用者帳戶或群組</span><span class="sxs-lookup"><span data-stu-id="b2eca-103">Removing a User Account or Group from a Role</span></span>

<span data-ttu-id="b2eca-104">如果使用者的許可權變更或角色已新增至應用程式，您可以將帳戶從一個角色移至另一個角色。</span><span class="sxs-lookup"><span data-stu-id="b2eca-104">If a user's privileges change or if roles are added to an application, you can move an account from one role to another role.</span></span> <span data-ttu-id="b2eca-105">若要將使用者帳戶或使用者群組從某個角色移至另一個角色，您必須從其目前的角色中移除使用者帳戶或群組，然後將其指派給新的角色。</span><span class="sxs-lookup"><span data-stu-id="b2eca-105">To move a user account or group of users from one role to another, you must remove the user account or group from its current role and then assign it to the new role.</span></span>

<span data-ttu-id="b2eca-106">**若要將使用者帳戶或群組從某個角色移至另一個角色**</span><span class="sxs-lookup"><span data-stu-id="b2eca-106">**To move a user account or group from one role to another**</span></span>

1.  <span data-ttu-id="b2eca-107">將使用者帳戶或群組從它不再屬於的角色中移除，如下所示：</span><span class="sxs-lookup"><span data-stu-id="b2eca-107">Remove the user account or group from the role that it should no longer belong to, as follows:</span></span>

    1.  <span data-ttu-id="b2eca-108">在 [元件服務] 系統管理工具的主控台樹中，找出包含您感興趣之角色的 COM + 應用程式。</span><span class="sxs-lookup"><span data-stu-id="b2eca-108">In the console tree of the Component Services administrative tool, locate the COM+ application that contains the role you are interested in.</span></span> <span data-ttu-id="b2eca-109">在主控台樹中展開視圖，直到角色的使用者可以看見為止。</span><span class="sxs-lookup"><span data-stu-id="b2eca-109">Expand the view in the console tree until the users for the role are visible.</span></span>

    2.  <span data-ttu-id="b2eca-110">以滑鼠右鍵按一下您要移除的使用者帳戶或群組，然後按一下 [ **刪除**]。</span><span class="sxs-lookup"><span data-stu-id="b2eca-110">Right-click the user account or group you want to remove, and then click **Delete**.</span></span>

    3.  <span data-ttu-id="b2eca-111">當 [ **確認專案刪除** ] 對話方塊出現提示時，請按一下 [ **是]** 以刪除使用者帳戶或群組。</span><span class="sxs-lookup"><span data-stu-id="b2eca-111">When prompted by the **Confirm Item Delete** dialog box, click **Yes** to delete the user account or group.</span></span>

    <span data-ttu-id="b2eca-112">您從角色移除的使用者帳戶或群組不會再出現在 [ **使用者** ] 資料夾中。</span><span class="sxs-lookup"><span data-stu-id="b2eca-112">The user account or group that you have removed from the role no longer appears in the **Users** folder.</span></span>

2.  <span data-ttu-id="b2eca-113">將您已移除的使用者帳戶或群組指派給指派給使用者或群組的角色，如下所示：</span><span class="sxs-lookup"><span data-stu-id="b2eca-113">Assign the user account or group you have removed to the roles that the user or group should be assigned to, as follows:</span></span>

    1.  <span data-ttu-id="b2eca-114">在 [元件服務] 系統管理工具的主控台樹中，找出包含您要新增使用者帳戶或群組之角色的 COM + 應用程式。</span><span class="sxs-lookup"><span data-stu-id="b2eca-114">In the console tree of the Component Services administrative tool, locate the COM+ application that contains the role to which you want to add the user account or group.</span></span> <span data-ttu-id="b2eca-115">在主控台樹中展開視圖，直到應用程式的角色可見為止。</span><span class="sxs-lookup"><span data-stu-id="b2eca-115">Expand the view in the console tree until the application's roles are visible.</span></span>

    2.  <span data-ttu-id="b2eca-116">找出您要新增使用者帳戶或群組的角色。</span><span class="sxs-lookup"><span data-stu-id="b2eca-116">Locate the role to which you want to add the user account or group.</span></span>

        > [!Note]  
        > <span data-ttu-id="b2eca-117">如果您要尋找的角色不在 [ **角色** ] 資料夾中，表示該角色尚未新增至應用程式。</span><span class="sxs-lookup"><span data-stu-id="b2eca-117">If the role you are looking for is not in the **Roles** folder, the role has not been added to the application.</span></span> <span data-ttu-id="b2eca-118">開發人員必須先將它新增至應用程式，您才能將使用者帳戶指派給角色。</span><span class="sxs-lookup"><span data-stu-id="b2eca-118">It must be added to the application by the developer before you can assign user accounts to the role.</span></span>

         

    3.  <span data-ttu-id="b2eca-119">在角色中的 [ **使用者** ] 資料夾上按一下滑鼠右鍵，指向 [ **新增**]，然後按一下 [ **使用者**]。</span><span class="sxs-lookup"><span data-stu-id="b2eca-119">Right-click the **Users** folder in the role, point to **New**, and then click **User**.</span></span>

    4.  <span data-ttu-id="b2eca-120">在 [ **選取使用者或群組** ] 視窗的下方窗格中，輸入您要新增之使用者或群組的完整名稱。</span><span class="sxs-lookup"><span data-stu-id="b2eca-120">In the **Select Users or Groups** window, in the bottom pane, type the fully qualified name of the user or group you want to add.</span></span> <span data-ttu-id="b2eca-121">如果您不知道名稱，請按一下 [ **Advanced** ] 按鈕，然後按一下 [ **立即尋找** ]，以查看所選網域中的使用者和群組清單。</span><span class="sxs-lookup"><span data-stu-id="b2eca-121">If you do not know the name, click the **Advanced** button and then click **Find Now** to view a list of users and groups in the selected domain.</span></span> <span data-ttu-id="b2eca-122">從 **名稱 (RDN)** 清單中選取使用者或群組，然後按一下 **[確定]**。</span><span class="sxs-lookup"><span data-stu-id="b2eca-122">Select a user or group from the **Name (RDN)** list and click **OK**.</span></span>

    5.  <span data-ttu-id="b2eca-123">當您完成將使用者帳戶或群組新增至角色時，請按一下 **[確定]**。</span><span class="sxs-lookup"><span data-stu-id="b2eca-123">When you have finished adding the user account or group to the role, click **OK**.</span></span>

    <span data-ttu-id="b2eca-124">針對您已指派給角色的每個使用者帳戶或群組，[ **使用者** ] 資料夾中會出現一個圖示。</span><span class="sxs-lookup"><span data-stu-id="b2eca-124">For each user account or group you have assigned to the role, an icon appears in the **Users** folder.</span></span>

<span data-ttu-id="b2eca-125">使用者帳戶或群組的已變更角色成員資格會在應用程式下次啟動時生效。</span><span class="sxs-lookup"><span data-stu-id="b2eca-125">The changed role membership for the user account or group takes effect the next time the application is started.</span></span>

 

 




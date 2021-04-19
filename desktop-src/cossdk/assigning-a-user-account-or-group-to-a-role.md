---
description: 您可以使用 [元件服務] 系統管理工具，以使用者帳戶或群組填入角色。
ms.assetid: 1cf7dc38-185a-4cc4-8f4c-44b6af4c5f4a
title: 將使用者帳戶或群組指派給角色
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d53b37c9f0265e02c7abdf74eeaf81bd0b12e3d8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972564"
---
# <a name="assigning-a-user-account-or-group-to-a-role"></a><span data-ttu-id="08e5a-103">將使用者帳戶或群組指派給角色</span><span class="sxs-lookup"><span data-stu-id="08e5a-103">Assigning a User Account or Group to a Role</span></span>

<span data-ttu-id="08e5a-104">您可以使用 [元件服務] 系統管理工具，以使用者帳戶或群組填入角色。</span><span class="sxs-lookup"><span data-stu-id="08e5a-104">You can use the Component Services administrative tool to populate a role with user accounts or groups.</span></span> <span data-ttu-id="08e5a-105">將使用者帳戶指派給角色的慣用方式是將使用者帳戶指派給群組，然後將該群組指派給該角色。</span><span class="sxs-lookup"><span data-stu-id="08e5a-105">The preferred way to assign a user account to a role is to assign the user account to a group and then assign the group to the role.</span></span> <span data-ttu-id="08e5a-106">使用群組來填入角色，可讓您更輕鬆地管理大量使用者。</span><span class="sxs-lookup"><span data-stu-id="08e5a-106">Using groups to populate roles makes it easier for you to manage large numbers of users.</span></span> <span data-ttu-id="08e5a-107">在 [電腦管理] 系統管理工具的線上說明中，如需有關建立群組或將使用者帳戶指派給群組的詳細資訊，請參閱「本機使用者和群組」主題。</span><span class="sxs-lookup"><span data-stu-id="08e5a-107">In the online help for the Computer Management administrative tool, see the topic "Local Users and Groups" for more information about creating groups or assigning a user account to a group.</span></span>

> [!Note]  
> <span data-ttu-id="08e5a-108">若要允許未驗證的網路使用者執行 COM + 應用程式，應用程式角色必須包含匿名使用者。</span><span class="sxs-lookup"><span data-stu-id="08e5a-108">To allow unauthenticated network users to run a COM+ application, the application roles must include the Anonymous user.</span></span> <span data-ttu-id="08e5a-109">從 Windows Server 2003 開始，根據預設，匿名使用者不會包含在 Everyone 群組中。</span><span class="sxs-lookup"><span data-stu-id="08e5a-109">Starting with Windows Server 2003, by default, the Anonymous user is not included in the Everyone group.</span></span>

 

<span data-ttu-id="08e5a-110">將使用者帳戶指派給適當的 Windows 群組之後，請遵循下列步驟，將 Windows 群組指派給角色。</span><span class="sxs-lookup"><span data-stu-id="08e5a-110">After you have assigned the user account to the appropriate Windows group, follow these steps to assign the Windows group to the role.</span></span>

<span data-ttu-id="08e5a-111">**將 Windows 群組指派給安全性角色**</span><span class="sxs-lookup"><span data-stu-id="08e5a-111">**To assign a Windows group to a security role**</span></span>

1.  <span data-ttu-id="08e5a-112">在 [元件服務] 系統管理工具的主控台樹中，找出包含您要新增使用者帳戶或群組之角色的 COM + 應用程式。</span><span class="sxs-lookup"><span data-stu-id="08e5a-112">In the console tree of the Component Services administrative tool, locate the COM+ application that contains the role to which you want to add the user account or group.</span></span> <span data-ttu-id="08e5a-113">在主控台樹中展開視圖，直到應用程式的角色可見為止。</span><span class="sxs-lookup"><span data-stu-id="08e5a-113">Expand the view in the console tree until the application's roles are visible.</span></span>

2.  <span data-ttu-id="08e5a-114">找出您要新增使用者帳戶或群組的角色。</span><span class="sxs-lookup"><span data-stu-id="08e5a-114">Locate the role to which you want to add the user account or group.</span></span>

    > [!Note]  
    > <span data-ttu-id="08e5a-115">如果您要尋找的角色不在 [ **角色** ] 資料夾中，表示該角色尚未新增至應用程式。</span><span class="sxs-lookup"><span data-stu-id="08e5a-115">If the role you are looking for is not in the **Roles** folder, the role has not been added to the application.</span></span> <span data-ttu-id="08e5a-116">開發人員必須先將它新增至應用程式，您才能將使用者帳戶指派給角色。</span><span class="sxs-lookup"><span data-stu-id="08e5a-116">It must be added to the application by the developer before you can assign user accounts to the role.</span></span>

     

3.  <span data-ttu-id="08e5a-117">在角色中的 [ **使用者** ] 資料夾上按一下滑鼠右鍵，指向 [ **新增**]，然後按一下 [ **使用者**]。</span><span class="sxs-lookup"><span data-stu-id="08e5a-117">Right-click the **Users** folder in the role, point to **New**, and then click **User**.</span></span>

4.  <span data-ttu-id="08e5a-118">在 [ **選取使用者或群組** ] 視窗的下方窗格中，輸入您要新增之使用者或群組的完整名稱。</span><span class="sxs-lookup"><span data-stu-id="08e5a-118">In the **Select Users or Groups** window, in the bottom pane, type the fully qualified name of the user or group you want to add.</span></span> <span data-ttu-id="08e5a-119">如果您不知道名稱，請按一下 [ **Advanced** ] 按鈕，然後按一下 [ **立即尋找** ]，以查看所選網域中的使用者和群組清單。</span><span class="sxs-lookup"><span data-stu-id="08e5a-119">If you do not know the name, click the **Advanced** button and then click **Find Now** to view a list of users and groups in the selected domain.</span></span> <span data-ttu-id="08e5a-120">從 **名稱 (RDN)** 清單中選取使用者或群組，然後按一下 **[確定]**。</span><span class="sxs-lookup"><span data-stu-id="08e5a-120">Select a user or group from the **Name (RDN)** list, and click **OK**.</span></span>

5.  <span data-ttu-id="08e5a-121">若要新增更多使用者帳戶或群組，請重複步驟4。</span><span class="sxs-lookup"><span data-stu-id="08e5a-121">To add more user accounts or groups, repeat step 4.</span></span>

6.  <span data-ttu-id="08e5a-122">當您完成將使用者帳戶和群組新增至角色時，請按一下 **[確定]**。</span><span class="sxs-lookup"><span data-stu-id="08e5a-122">When you have finished adding user accounts and groups to the role, click **OK**.</span></span>

<span data-ttu-id="08e5a-123">針對您已指派給角色的每個使用者帳戶或群組，[ **使用者** ] 資料夾中會出現一個圖示。</span><span class="sxs-lookup"><span data-stu-id="08e5a-123">For each user account or group you have assigned to the role, an icon appears in the **Users** folder.</span></span> <span data-ttu-id="08e5a-124">新的角色成員資格會在應用程式下次啟動時生效。</span><span class="sxs-lookup"><span data-stu-id="08e5a-124">The new role membership takes effect the next time the application is started.</span></span>

 

 




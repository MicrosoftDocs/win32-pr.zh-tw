---
description: 您可以定義應用程式所需的安全性許可權，以判斷該應用程式的安全性原則。
ms.assetid: 0348684f-aebd-4d2d-a69b-85fea551c0cd
title: 定義應用程式的角色
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f8e46eb2cb857a2b2dee2aabe41cb571e12ed98
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991632"
---
# <a name="defining-roles-for-an-application"></a><span data-ttu-id="1e7c8-103">定義應用程式的角色</span><span class="sxs-lookup"><span data-stu-id="1e7c8-103">Defining Roles for an Application</span></span>

<span data-ttu-id="1e7c8-104">您可以定義應用程式所需的安全性許可權，以判斷該應用程式的安全性原則。</span><span class="sxs-lookup"><span data-stu-id="1e7c8-104">You determine a security policy for an application by defining the security privileges that it requires.</span></span> <span data-ttu-id="1e7c8-105">若要這樣做，請將特殊許可權的符號層級宣告為角色，也就是定義應用程式的角色，然後 [將角色指派](assigning-roles-to-components--interfaces--or-methods.md) 給應用程式內的特定資源。</span><span class="sxs-lookup"><span data-stu-id="1e7c8-105">To do this you declare a symbolic level of privilege as a role—that is, define the role for the application—and then [assign the role](assigning-roles-to-components--interfaces--or-methods.md) to specific resources within the application.</span></span> <span data-ttu-id="1e7c8-106">這項設計是在部署應用程式時完成的，而系統管理員則會將實際的使用者和使用者群組填入角色。</span><span class="sxs-lookup"><span data-stu-id="1e7c8-106">This design is fulfilled when the application is deployed and system administrators populate the role with actual users and user groups.</span></span> <span data-ttu-id="1e7c8-107">如需更詳細的資訊，請參閱以 [角色為基礎的安全性管理](role-based-security-administration.md)。</span><span class="sxs-lookup"><span data-stu-id="1e7c8-107">For greater detail, see [Role-Based Security Administration](role-based-security-administration.md).</span></span>

<span data-ttu-id="1e7c8-108">**將角色加入至應用程式**</span><span class="sxs-lookup"><span data-stu-id="1e7c8-108">**To add a role to an application**</span></span>

1.  <span data-ttu-id="1e7c8-109">在 [元件服務] 系統管理工具的主控台樹中，找出您要新增角色的 COM + 應用程式。</span><span class="sxs-lookup"><span data-stu-id="1e7c8-109">In the console tree of the Component Services administrative tool, locate the COM+ application to which you want to add the role.</span></span> <span data-ttu-id="1e7c8-110">展開樹狀結構，以查看應用程式的資料夾。</span><span class="sxs-lookup"><span data-stu-id="1e7c8-110">Expand the tree to view the folders for the application.</span></span>

2.  <span data-ttu-id="1e7c8-111">以滑鼠右鍵按一下應用程式的 [ **角色** ] 資料夾，指向 [ **新增**]，然後按一下 [ **角色**]。</span><span class="sxs-lookup"><span data-stu-id="1e7c8-111">Right-click the **Roles** folder for the application, point to **New**, and then click **Role**.</span></span>

3.  <span data-ttu-id="1e7c8-112">在 [ **角色**] 對話方塊中，于提供的方塊中輸入新角色的名稱。</span><span class="sxs-lookup"><span data-stu-id="1e7c8-112">In the **Role** dialog box, type the name of the new role in the box provided.</span></span>

4.  <span data-ttu-id="1e7c8-113">按一下 [確定]  。</span><span class="sxs-lookup"><span data-stu-id="1e7c8-113">Click **OK**.</span></span>

> [!Note]  
> <span data-ttu-id="1e7c8-114">將角色新增至應用程式之後，您必須確定將角色指派給適當的元件、介面和方法。</span><span class="sxs-lookup"><span data-stu-id="1e7c8-114">After adding roles to the application, you must be sure to assign the roles to the appropriate components, interfaces, and methods.</span></span> <span data-ttu-id="1e7c8-115">否則，如果已選擇並啟用以角色為基礎的安全性，而且已新增但未指派角色，則對應用程式的所有呼叫都會失敗。</span><span class="sxs-lookup"><span data-stu-id="1e7c8-115">Otherwise, if role-based security has been chosen and enabled and if roles have been added but not assigned, all calls to the application will fail.</span></span> <span data-ttu-id="1e7c8-116">如需詳細資訊，請參閱 [將角色指派給元件、介面或方法](assigning-roles-to-components--interfaces--or-methods.md)。</span><span class="sxs-lookup"><span data-stu-id="1e7c8-116">For more information, see [Assigning Roles to Components, Interfaces, or Methods](assigning-roles-to-components--interfaces--or-methods.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="1e7c8-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="1e7c8-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1e7c8-118">將角色指派給元件、介面或方法</span><span class="sxs-lookup"><span data-stu-id="1e7c8-118">Assigning Roles to Components, Interfaces, or Methods</span></span>](assigning-roles-to-components--interfaces--or-methods.md)
</dt> <dt>

[<span data-ttu-id="1e7c8-119">設定 Role-Based 安全性</span><span class="sxs-lookup"><span data-stu-id="1e7c8-119">Configuring Role-Based Security</span></span>](configuring-role-based-security.md)
</dt> <dt>

[<span data-ttu-id="1e7c8-120">啟用應用程式的存取檢查</span><span class="sxs-lookup"><span data-stu-id="1e7c8-120">Enabling Access Checks for an Application</span></span>](enabling-access-checks-for-an-application.md)
</dt> <dt>

[<span data-ttu-id="1e7c8-121">在元件層級啟用存取檢查</span><span class="sxs-lookup"><span data-stu-id="1e7c8-121">Enabling Access Checks at the Component Level</span></span>](enabling-access-checks-at-the-component-level.md)
</dt> <dt>

[<span data-ttu-id="1e7c8-122">設定存取檢查的安全性等級</span><span class="sxs-lookup"><span data-stu-id="1e7c8-122">Setting a Security Level for Access Checks</span></span>](setting-a-security-level-for-access-checks.md)
</dt> </dl>

 

 




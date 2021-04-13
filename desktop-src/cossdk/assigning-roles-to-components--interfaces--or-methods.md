---
description: 將角色指派給元件、介面或方法
ms.assetid: 687d5692-4a83-4de8-b99d-859aaaddd16d
title: 將角色指派給元件、介面或方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5efb66c9de865cbfcdc6e9cb047af92c95f6bc0a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104385966"
---
# <a name="assigning-roles-to-components-interfaces-or-methods"></a><span data-ttu-id="76b6c-103">將角色指派給元件、介面或方法</span><span class="sxs-lookup"><span data-stu-id="76b6c-103">Assigning Roles to Components, Interfaces, or Methods</span></span>

<span data-ttu-id="76b6c-104">您可以透過 [元件服務] 系統管理工具，將角色明確指派給 COM + 應用程式中可看見的任何專案。</span><span class="sxs-lookup"><span data-stu-id="76b6c-104">You can explicitly assign a role to any item within a COM+ application that is visible through the Component Services administrative tool.</span></span> <span data-ttu-id="76b6c-105">這麼做可確保屬於該角色成員的任何使用者都可以存取該專案及其包含的任何其他專案。</span><span class="sxs-lookup"><span data-stu-id="76b6c-105">Doing so ensures that any users that are members of the role will be permitted access to that item and any other items that it contains.</span></span> <span data-ttu-id="76b6c-106">例如，如果您將「讀取者」角色指派給某個元件，「讀取器」的任何成員都可以存取該元件，以及它所公開的任何介面和方法。</span><span class="sxs-lookup"><span data-stu-id="76b6c-106">For example, if you assign the role "Readers" to a component, any member of "Readers" is allowed access to that component and any interfaces and methods it exposes.</span></span> <span data-ttu-id="76b6c-107">「讀取器」會顯示為任何這些介面和方法的繼承角色。</span><span class="sxs-lookup"><span data-stu-id="76b6c-107">"Readers" will show up as an Inherited role for any of those interfaces and methods.</span></span>

<span data-ttu-id="76b6c-108">只有當您將角色指派給呼叫端，或是將角色指派給方法的介面或方法的元件時，呼叫端才可以存取方法，在此情況下，此方法會繼承角色。</span><span class="sxs-lookup"><span data-stu-id="76b6c-108">A method is accessible to callers only if you assign a role to it, either by explicitly assigning the role directly to the method or by assigning a role to the method's interface or the method's component, in which case the role will be inherited by the method.</span></span> <span data-ttu-id="76b6c-109">如果未指派任何角色，而且已啟用存取檢查，則對方法的所有呼叫都將會失敗。</span><span class="sxs-lookup"><span data-stu-id="76b6c-109">If no role is assigned and if access checks are enabled, all calls to the method will fail.</span></span>

<span data-ttu-id="76b6c-110">您必須先為應用程式 [定義](defining-roles-for-an-application.md) 角色，才能指派角色。</span><span class="sxs-lookup"><span data-stu-id="76b6c-110">Before you can assign a role, you must [define](defining-roles-for-an-application.md) it for the application.</span></span> <span data-ttu-id="76b6c-111">針對應用程式定義的所有角色，都會出現在應用程式內任何元件、方法和介面的 [**安全性**] 索引標籤上，針對 **選取的專案 (s 明確設定的角色)** 視窗中。</span><span class="sxs-lookup"><span data-stu-id="76b6c-111">All roles defined for the application will appear in the **Roles explicitly set for selected item(s)** window on the **Security** tab for any components, methods, and interfaces within the application.</span></span>

<span data-ttu-id="76b6c-112">**將角色指派給元件、方法或介面**</span><span class="sxs-lookup"><span data-stu-id="76b6c-112">**To assign roles to a component, method, or interface**</span></span>

1.  <span data-ttu-id="76b6c-113">在 [元件服務] 系統管理工具的主控台樹中，找出已定義角色的 COM + 應用程式。</span><span class="sxs-lookup"><span data-stu-id="76b6c-113">In the console tree of the Component Services administrative tool, locate the COM+ application for which the role has been defined.</span></span> <span data-ttu-id="76b6c-114">展開樹狀結構，以根據您指派角色的目標來查看應用程式的元件、介面或方法。</span><span class="sxs-lookup"><span data-stu-id="76b6c-114">Expand the tree to view the application's components, interfaces, or methods, depending on what you are assigning the role to.</span></span>

2.  <span data-ttu-id="76b6c-115">以滑鼠右鍵按一下您要指派角色的專案，然後按一下 [ **屬性**]。</span><span class="sxs-lookup"><span data-stu-id="76b6c-115">Right-click the item to which you want to assign the role, and then click **Properties**.</span></span>

3.  <span data-ttu-id="76b6c-116">在 [屬性] 對話方塊中，按一下 [ **安全性** ] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="76b6c-116">In the properties dialog box, click the **Security** tab.</span></span>

4.  <span data-ttu-id="76b6c-117">在 [ **為選取的專案明確設定的角色 (s)** ] 方塊中，選取您要指派給專案的角色。</span><span class="sxs-lookup"><span data-stu-id="76b6c-117">In the **Roles explicitly set for selected item(s)** box, select the roles that you want to assign to the item.</span></span>

5.  <span data-ttu-id="76b6c-118">按一下 [確定]  。</span><span class="sxs-lookup"><span data-stu-id="76b6c-118">Click **OK**.</span></span>

<span data-ttu-id="76b6c-119">任何您已為專案明確設定的角色，都會由它所包含的任何較低層級專案繼承，並顯示在這些專案 **(s) 視窗中所選取專案繼承的角色** 中。</span><span class="sxs-lookup"><span data-stu-id="76b6c-119">Any roles that you have explicitly set for an item will be inherited by any lower-level items it contains and will show up in the **Roles inherited by selected item(s)** window for those items.</span></span>

## <a name="related-topics"></a><span data-ttu-id="76b6c-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="76b6c-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="76b6c-121">設定 Role-Based 安全性</span><span class="sxs-lookup"><span data-stu-id="76b6c-121">Configuring Role-Based Security</span></span>](configuring-role-based-security.md)
</dt> <dt>

[<span data-ttu-id="76b6c-122">定義應用程式的角色</span><span class="sxs-lookup"><span data-stu-id="76b6c-122">Defining Roles for an Application</span></span>](defining-roles-for-an-application.md)
</dt> <dt>

[<span data-ttu-id="76b6c-123">啟用應用程式的存取檢查</span><span class="sxs-lookup"><span data-stu-id="76b6c-123">Enabling Access Checks for an Application</span></span>](enabling-access-checks-for-an-application.md)
</dt> <dt>

[<span data-ttu-id="76b6c-124">在元件層級啟用存取檢查</span><span class="sxs-lookup"><span data-stu-id="76b6c-124">Enabling Access Checks at the Component Level</span></span>](enabling-access-checks-at-the-component-level.md)
</dt> <dt>

[<span data-ttu-id="76b6c-125">設定存取檢查的安全性等級</span><span class="sxs-lookup"><span data-stu-id="76b6c-125">Setting a Security Level for Access Checks</span></span>](setting-a-security-level-for-access-checks.md)
</dt> </dl>

 

 




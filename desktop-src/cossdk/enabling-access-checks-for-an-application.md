---
description: 執行此步驟會根據您選取的安全性層級以及是否啟用個別元件的存取檢查，來啟用程式存取檢查或完整的角色型安全性。
ms.assetid: 266bdac1-41be-45a5-a8c7-f9c6fe08445c
title: 啟用應用程式的存取檢查
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3d64a32b23467f85c368e088a870ebe5e4d683e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972333"
---
# <a name="enabling-access-checks-for-an-application"></a><span data-ttu-id="bc525-103">啟用應用程式的存取檢查</span><span class="sxs-lookup"><span data-stu-id="bc525-103">Enabling Access Checks for an Application</span></span>

<span data-ttu-id="bc525-104">執行此步驟會根據您選取的安全性層級以及是否啟用個別元件的存取檢查，來啟用程式存取檢查或完整的角色型安全性。</span><span class="sxs-lookup"><span data-stu-id="bc525-104">Performing this step enables either process access checks or full role-based security, depending on what security level you select and whether you enable access checking for individual components.</span></span>

<span data-ttu-id="bc525-105">**若要啟用應用程式的存取檢查**</span><span class="sxs-lookup"><span data-stu-id="bc525-105">**To enable access checks for an application**</span></span>

1.  <span data-ttu-id="bc525-106">在 [元件服務] 系統管理工具的主控台樹中，以滑鼠 **按右鍵您** 要啟用存取檢查的 com + 應用程式，然後按一下 [內容]。</span><span class="sxs-lookup"><span data-stu-id="bc525-106">In the console tree of the Component Services administrative tool, right-click the COM+ application for which you want to enable access checks, and then click **Properties**.</span></span>

2.  <span data-ttu-id="bc525-107">在 [應用程式屬性] 對話方塊中，按一下 [ **安全性** ] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="bc525-107">In the application properties dialog box, click the **Security** tab.</span></span>

3.  <span data-ttu-id="bc525-108">選取 [ **強制執行此應用程式的存取檢查** ] 核取方塊。</span><span class="sxs-lookup"><span data-stu-id="bc525-108">Select the **Enforce access checks for this application** check box.</span></span>

4.  <span data-ttu-id="bc525-109">按一下 [確定]  。</span><span class="sxs-lookup"><span data-stu-id="bc525-109">Click **OK**.</span></span>

> [!Note]  
> <span data-ttu-id="bc525-110">從 Windows Server 2003，建立 COM + 應用程式時，預設會啟用存取檢查。</span><span class="sxs-lookup"><span data-stu-id="bc525-110">As of Windows Server 2003, access checks are enabled by default when creating a COM+ application.</span></span> <span data-ttu-id="bc525-111">預設會在應用層級啟用存取檢查，並且在元件層級預設為停用。</span><span class="sxs-lookup"><span data-stu-id="bc525-111">Access checks are enabled by default at the application level and disabled by default at the component level.</span></span> <span data-ttu-id="bc525-112">先前，在應用層級依預設會停用存取檢查，而且在元件層級預設為啟用。</span><span class="sxs-lookup"><span data-stu-id="bc525-112">Previously, access checks were disabled by default at the application level and enabled by default at the component level.</span></span>

 

<span data-ttu-id="bc525-113">啟用存取檢查之後，您應該選取適當的安全性層級。</span><span class="sxs-lookup"><span data-stu-id="bc525-113">After enabling access checks, you should select the appropriate security level.</span></span> <span data-ttu-id="bc525-114">請參閱 [設定存取檢查的安全性層級](setting-a-security-level-for-access-checks.md)。</span><span class="sxs-lookup"><span data-stu-id="bc525-114">See [Setting a Security Level for Access Checks](setting-a-security-level-for-access-checks.md).</span></span> <span data-ttu-id="bc525-115">此外，您必須務必定義角色，並將它們新增至應用程式。</span><span class="sxs-lookup"><span data-stu-id="bc525-115">Also, you must be sure to define roles and add them to the application.</span></span> <span data-ttu-id="bc525-116">如果啟用存取檢查但未新增任何角色，對應用程式的所有呼叫都將會失敗。</span><span class="sxs-lookup"><span data-stu-id="bc525-116">If access checks are enabled but no roles have been added, all calls to the application will fail.</span></span> <span data-ttu-id="bc525-117">請參閱 [定義應用程式的角色](defining-roles-for-an-application.md)。</span><span class="sxs-lookup"><span data-stu-id="bc525-117">See [Defining Roles for an Application](defining-roles-for-an-application.md).</span></span>

> [!Note]  
> <span data-ttu-id="bc525-118">當您對應用程式進行偵錯工具時，停用安全性可能會很有説明，讓您能夠專注于程式列為和設計的其他層面。</span><span class="sxs-lookup"><span data-stu-id="bc525-118">When debugging your application, it might be helpful to disable security so that you can concentrate on other aspects of your program's behavior and design.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="bc525-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="bc525-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc525-120">將角色指派給元件、介面或方法</span><span class="sxs-lookup"><span data-stu-id="bc525-120">Assigning Roles to Components, Interfaces, or Methods</span></span>](assigning-roles-to-components--interfaces--or-methods.md)
</dt> <dt>

[<span data-ttu-id="bc525-121">設定 Role-Based 安全性</span><span class="sxs-lookup"><span data-stu-id="bc525-121">Configuring Role-Based Security</span></span>](configuring-role-based-security.md)
</dt> <dt>

[<span data-ttu-id="bc525-122">定義應用程式的角色</span><span class="sxs-lookup"><span data-stu-id="bc525-122">Defining Roles for an Application</span></span>](defining-roles-for-an-application.md)
</dt> <dt>

[<span data-ttu-id="bc525-123">在元件層級啟用存取檢查</span><span class="sxs-lookup"><span data-stu-id="bc525-123">Enabling Access Checks at the Component Level</span></span>](enabling-access-checks-at-the-component-level.md)
</dt> <dt>

[<span data-ttu-id="bc525-124">設定存取檢查的安全性等級</span><span class="sxs-lookup"><span data-stu-id="bc525-124">Setting a Security Level for Access Checks</span></span>](setting-a-security-level-for-access-checks.md)
</dt> </dl>

 

 




---
title: 擴充目錄物件的消費者介面
description: 使用 Microsoft Windows 2000 和更新版本時，可以使用 Microsoft Management Console (MMC) 嵌入式管理單元（例如 Active Directory 消費者和電腦嵌入式管理單元）來管理 Active Directory Domain Services。
ms.assetid: 758ec25d-42ab-46ba-aa58-416d7ac8fd68
ms.tgt_platform: multiple
keywords:
- Active Directory，使用擴充使用者介面
- 物件 AD，擴充目錄物件的使用者介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b8d635132a26e80a63fddb35f779211308779f9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671280"
---
# <a name="extending-the-user-interface-for-directory-objects"></a><span data-ttu-id="7ab3b-105">擴充目錄物件的消費者介面</span><span class="sxs-lookup"><span data-stu-id="7ab3b-105">Extending the User Interface for Directory Objects</span></span>

<span data-ttu-id="7ab3b-106">使用 Microsoft Windows 2000 和更新版本時，可以使用 Microsoft Management Console (MMC) 嵌入式管理單元（例如 Active Directory 消費者和電腦嵌入式管理單元）來管理 Active Directory Domain Services。</span><span class="sxs-lookup"><span data-stu-id="7ab3b-106">With Microsoft Windows 2000 and later, Microsoft Management Console (MMC) snap-ins, such as the Active Directory Users and Computers snap-in, for administration of Active Directory Domain Services, are available.</span></span> <span data-ttu-id="7ab3b-107">此外，Windows 2000 shell 還包含使用者介面， (Ui) 尋找位於目錄中的物件，以及讀取和寫入屬性。</span><span class="sxs-lookup"><span data-stu-id="7ab3b-107">In addition, the Windows 2000 shell includes user interfaces (UIs) for finding objects that reside in the directory and reading and writing properties.</span></span> <span data-ttu-id="7ab3b-108">本節說明如何在 Windows shell 中擴充用來查看和管理 Active Directory Domain Services 物件的 UI，並 Active Directory 系統管理嵌入式管理單元。本節也涵蓋將 UI 延伸模組部署到使用者的桌面時所需的內容。</span><span class="sxs-lookup"><span data-stu-id="7ab3b-108">This section explains how to extend the UI for viewing and managing Active Directory Domain Services objects in the Windows shell and Active Directory administrative snap-ins. This section also covers what is required to deploy the UI extensions to the user's desktops.</span></span>

<span data-ttu-id="7ab3b-109">具體而言，本節將討論下列各項：</span><span class="sxs-lookup"><span data-stu-id="7ab3b-109">Specifically, this section discusses the following:</span></span>

-   [<span data-ttu-id="7ab3b-110">關於 Active Directory 使用者介面</span><span class="sxs-lookup"><span data-stu-id="7ab3b-110">About Active Directory User Interfaces</span></span>](about-the-user-interfaces-of-active-directory-domain-services.md)
-   [<span data-ttu-id="7ab3b-111">顯示規範</span><span class="sxs-lookup"><span data-stu-id="7ab3b-111">Display Specifiers</span></span>](display-specifiers.md)
-   [<span data-ttu-id="7ab3b-112">類別和屬性顯示名稱</span><span class="sxs-lookup"><span data-stu-id="7ab3b-112">Class and Attribute Display Names</span></span>](class-and-attribute-display-names.md)
-   [<span data-ttu-id="7ab3b-113">類別圖示</span><span class="sxs-lookup"><span data-stu-id="7ab3b-113">Class Icons</span></span>](class-icons.md)
-   [<span data-ttu-id="7ab3b-114">以分葉節點形式來查看容器</span><span class="sxs-lookup"><span data-stu-id="7ab3b-114">Viewing Containers as Leaf Nodes</span></span>](viewing-containers-as-leaf-nodes.md)
-   [<span data-ttu-id="7ab3b-115">修改現有的使用者介面</span><span class="sxs-lookup"><span data-stu-id="7ab3b-115">Modifying Existing User Interfaces</span></span>](modifying-existing-user-interfaces.md)
-   [<span data-ttu-id="7ab3b-116">新物件類別的消費者介面延伸模組</span><span class="sxs-lookup"><span data-stu-id="7ab3b-116">User Interface Extension for New Object Classes</span></span>](user-interface-extension-for-new-object-classes.md)
-   [<span data-ttu-id="7ab3b-117">搭配顯示規範使用的屬性頁</span><span class="sxs-lookup"><span data-stu-id="7ab3b-117">Property Pages for Use with Display Specifiers</span></span>](property-pages-for-use-with-display-specifiers.md)
-   [<span data-ttu-id="7ab3b-118">用於顯示規範的內容功能表</span><span class="sxs-lookup"><span data-stu-id="7ab3b-118">Context Menus for Use with Display Specifiers</span></span>](context-menus-for-use-with-display-specifiers.md)
-   [<span data-ttu-id="7ab3b-119">物件建立的嚮導</span><span class="sxs-lookup"><span data-stu-id="7ab3b-119">Object Creation Wizards</span></span>](object-creation-wizards.md)
-   [<span data-ttu-id="7ab3b-120">使用標準對話方塊來處理 Active Directory Domain Services 中的物件</span><span class="sxs-lookup"><span data-stu-id="7ab3b-120">Using Standard Dialog Boxes for Handling Objects in Active Directory Domain Services</span></span>](using-standard-dialog-boxes-to-handle-objects-in-active-directory-domain-services.md)
-   [<span data-ttu-id="7ab3b-121">系統管理通知處理常式</span><span class="sxs-lookup"><span data-stu-id="7ab3b-121">Administrative Notification Handlers</span></span>](administrative-notification-handlers.md)
-   [<span data-ttu-id="7ab3b-122">散發消費者介面元件</span><span class="sxs-lookup"><span data-stu-id="7ab3b-122">Distributing User Interface Components</span></span>](distributing-user-interface-components.md)
-   [<span data-ttu-id="7ab3b-123">應用程式應該如何使用顯示規範</span><span class="sxs-lookup"><span data-stu-id="7ab3b-123">How Applications Should Use Display Specifiers</span></span>](how-applications-should-use-display-specifiers.md)
-   [<span data-ttu-id="7ab3b-124">Active Directory 擴充功能的偵錯工具</span><span class="sxs-lookup"><span data-stu-id="7ab3b-124">Debugging an Active Directory Extension</span></span>](debugging-an-active-directory-extension.md)

 

 





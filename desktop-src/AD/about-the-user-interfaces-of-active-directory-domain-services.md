---
title: 關於 Active Directory Domain Services 的使用者介面
description: 系統管理員和使用者必須能夠從使用者介面查看和修改 Microsoft Active Directory Domain Services 中的目錄服務物件。
ms.assetid: b6eec599-ebb3-40af-a4a2-059755285854
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c451a44660aaadbf0021ff57e675736b797d8f3e
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104023207"
---
# <a name="about-the-user-interfaces-of-active-directory-domain-services"></a><span data-ttu-id="7dfcf-103">關於 Active Directory Domain Services 的使用者介面</span><span class="sxs-lookup"><span data-stu-id="7dfcf-103">About the User Interfaces of Active Directory Domain Services</span></span>

<span data-ttu-id="7dfcf-104">系統管理員和使用者必須能夠從使用者介面查看和修改 Microsoft Active Directory Domain Services 中的目錄服務物件。</span><span class="sxs-lookup"><span data-stu-id="7dfcf-104">Administrators and users must be able to view and modify directory service objects in Microsoft Active Directory Domain Services from a user interface.</span></span> <span data-ttu-id="7dfcf-105">系統管理員會使用不同的 Microsoft Management Console (MMC) 嵌入式管理單元來管理 Active Directory 伺服器，具體來說，Active Directory Domain Services 的使用者和電腦、Active Directory Domain Services 的網站和服務、Active Directory Domain Services 的網域和信任，以及 Active Directory Domain Services 的架構管理員嵌入式管理單元。如果授與適當許可權，使用者也可以使用 Active Directory MMC 嵌入式管理單元來查看目錄物件。</span><span class="sxs-lookup"><span data-stu-id="7dfcf-105">Administrators manage the Active Directory server using different Microsoft Management Console (MMC) snap-ins, specifically, the Active Directory Domain Services Users and Computers, Active Directory Domain Services Sites and Services, Active Directory Domain Services Domains and Trusts, and Active Directory Domain Services Schema Manager snap-ins. The end user, if granted appropriate permissions, can also use the Active Directory MMC snap-ins to view directory objects.</span></span> <span data-ttu-id="7dfcf-106">Windows shell 也可以用來查看目錄物件。</span><span class="sxs-lookup"><span data-stu-id="7dfcf-106">The Windows shell can also be used to view directory objects.</span></span> <span data-ttu-id="7dfcf-107">Windows shell 可讓使用者從 [我的網路位置] 中的目錄專案，或透過 [開始] 功能表中提供的 [搜尋] 對話方塊，流覽儲存在目錄中的物件。</span><span class="sxs-lookup"><span data-stu-id="7dfcf-107">The Windows shell enables users to browse objects stored in the directory from either the directory item in My Network Places on the desktop or through the search dialogs available in the Start menu.</span></span>

<span data-ttu-id="7dfcf-108">Active Directory Domain Services 支援可適應的使用者介面，以符合系統管理員和終端使用者的需求。</span><span class="sxs-lookup"><span data-stu-id="7dfcf-108">Active Directory Domain Services support a user interface that adapts to meet the needs of administrators and end users.</span></span> <span data-ttu-id="7dfcf-109">Active Directory Domain Services 可讓您擴充代表現有物件類別的使用者介面，以及新增至架構的新類別。</span><span class="sxs-lookup"><span data-stu-id="7dfcf-109">Active Directory Domain Services enable you to extend the user interface that represents existing object classes as well as new classes added to the schema.</span></span> <span data-ttu-id="7dfcf-110">下列元素可以用來控制或擴充架構中所定義之每個類別的 UI：</span><span class="sxs-lookup"><span data-stu-id="7dfcf-110">The following elements can be used to control or extend the UI for each class defined in the schema:</span></span>

-   [<span data-ttu-id="7dfcf-111">搭配顯示規範使用的屬性頁</span><span class="sxs-lookup"><span data-stu-id="7dfcf-111">Property Pages for Use with Display Specifiers</span></span>](property-pages-for-use-with-display-specifiers.md)
-   [<span data-ttu-id="7dfcf-112">用於顯示規範的內容功能表</span><span class="sxs-lookup"><span data-stu-id="7dfcf-112">Context Menus for Use with Display Specifiers</span></span>](context-menus-for-use-with-display-specifiers.md)
-   [<span data-ttu-id="7dfcf-113">類別和屬性顯示名稱</span><span class="sxs-lookup"><span data-stu-id="7dfcf-113">Class and Attribute Display Names</span></span>](class-and-attribute-display-names.md)
-   [<span data-ttu-id="7dfcf-114">物件建立的嚮導</span><span class="sxs-lookup"><span data-stu-id="7dfcf-114">Object Creation Wizards</span></span>](object-creation-wizards.md)
-   [<span data-ttu-id="7dfcf-115">類別圖示</span><span class="sxs-lookup"><span data-stu-id="7dfcf-115">Class Icons</span></span>](class-icons.md)
-   [<span data-ttu-id="7dfcf-116">以分葉節點形式來查看容器</span><span class="sxs-lookup"><span data-stu-id="7dfcf-116">Viewing Containers as Leaf Nodes</span></span>](viewing-containers-as-leaf-nodes.md)

<span data-ttu-id="7dfcf-117">從 Windows 2000 開始，系統會提供 COM 物件，以執行使用目錄物件的通用對話方塊。</span><span class="sxs-lookup"><span data-stu-id="7dfcf-117">Beginning with Windows 2000, the system provides COM objects that implement common dialog boxes for working with directory objects.</span></span> <span data-ttu-id="7dfcf-118">這些對話方塊會提供通用 UI，而不需要重新產生這些對話方塊。</span><span class="sxs-lookup"><span data-stu-id="7dfcf-118">These dialog boxes provide a common UI without having to reimplement these dialog boxes.</span></span>

-   [<span data-ttu-id="7dfcf-119">目錄物件選擇器</span><span class="sxs-lookup"><span data-stu-id="7dfcf-119">Directory Object Picker</span></span>](directory-object-picker.md)
-   [<span data-ttu-id="7dfcf-120">網域瀏覽器</span><span class="sxs-lookup"><span data-stu-id="7dfcf-120">Domain Browser</span></span>](domain-browser.md)
-   [<span data-ttu-id="7dfcf-121">容器瀏覽器</span><span class="sxs-lookup"><span data-stu-id="7dfcf-121">Container Browser</span></span>](container-browser.md)

<span data-ttu-id="7dfcf-122">您可以使用 MMC 延伸嵌入式管理單元擴充 Active Directory 的系統管理嵌入式管理單元、內容功能表和屬性頁。其他 MMC 延伸模組（例如，任務板、命名空間專案、控制列和工具列）也可以執行。</span><span class="sxs-lookup"><span data-stu-id="7dfcf-122">Active Directory administrative snap-ins, context menus, and property pages can be extended using MMC extension snap-ins. Other MMC extensions, such as taskpads, namespace items, control bars, and toolbars can also be implemented.</span></span> <span data-ttu-id="7dfcf-123">如需詳細資訊，請參閱 [擴充 Active Directory 系統管理嵌入式管理單元](/previous-versions/windows/desktop/mmc/extending-the-active-directory-administrative-snap-ins)。</span><span class="sxs-lookup"><span data-stu-id="7dfcf-123">For more information, see [Extending the Active Directory Administrative Snap-ins](/previous-versions/windows/desktop/mmc/extending-the-active-directory-administrative-snap-ins).</span></span>

 

 
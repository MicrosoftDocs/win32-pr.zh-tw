---
description: 這個範例示範如何在安裝元件時，使用自訂動作在本機電腦上建立使用者帳戶。
ms.assetid: fc06dd7b-46d7-45a0-85b3-26f808c64f89
title: 使用自訂動作在本機電腦上建立使用者帳戶
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfd3bf002c0fa1d661c6bfebb6d1a18cbc4b0652
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319607"
---
# <a name="using-a-custom-action-to-create-user-accounts-on-a-local-computer"></a><span data-ttu-id="dc789-103">使用自訂動作在本機電腦上建立使用者帳戶</span><span class="sxs-lookup"><span data-stu-id="dc789-103">Using a Custom Action to Create User Accounts on a Local Computer</span></span>

<span data-ttu-id="dc789-104">這個範例示範如何在安裝元件時，使用自訂動作在本機電腦上建立使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="dc789-104">This sample demonstrates how to use custom actions to create user accounts on a local computer when installing a component.</span></span> <span data-ttu-id="dc789-105">移除元件會移除自訂動作所建立的本機使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="dc789-105">Removal of a component removes the local user accounts created by the custom action.</span></span> <span data-ttu-id="dc789-106">示範數個自訂動作，包括 [延後執行自訂動作](deferred-execution-custom-actions.md) 和 [復原自訂動作](rollback-custom-actions.md)。</span><span class="sxs-lookup"><span data-stu-id="dc789-106">Several custom actions are demonstrated including [Deferred Execution Custom Actions](deferred-execution-custom-actions.md) and [Rollback Custom Actions](rollback-custom-actions.md).</span></span>

<span data-ttu-id="dc789-107">此範例符合下列規格。</span><span class="sxs-lookup"><span data-stu-id="dc789-107">The sample meets the following specifications.</span></span>

-   <span data-ttu-id="dc789-108">安裝只會在執行 Windows 2000 時建立使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="dc789-108">The installation creates user accounts only if running Windows 2000.</span></span>
-   <span data-ttu-id="dc789-109">只有在安裝元件以在本機執行時，安裝才會建立使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="dc789-109">The installation creates user accounts only if the component is being installed to run locally.</span></span> <span data-ttu-id="dc789-110">這無法在元件修復或重新安裝期間建立使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="dc789-110">This precludes creating user accounts during the repair or reinstallation of the component.</span></span>
-   <span data-ttu-id="dc789-111">移除元件時，安裝程式會移除這些帳戶。</span><span class="sxs-lookup"><span data-stu-id="dc789-111">The Installer removes the accounts when the component is removed.</span></span>
-   <span data-ttu-id="dc789-112">系統會從安裝資料庫中的自訂資料表讀取使用者帳戶資訊，而不是硬式編碼的自訂動作程式碼。</span><span class="sxs-lookup"><span data-stu-id="dc789-112">User account information is read from a custom table in the installation database and is not hard-coded into the custom action code.</span></span>
-   <span data-ttu-id="dc789-113">由於建立或移除使用者帳戶需要較高的許可權，因此某些自訂動作必須能夠對需要較高許可權的系統進行變更。</span><span class="sxs-lookup"><span data-stu-id="dc789-113">Because the creation or removal of user accounts requires elevated privileges, some of the custom actions must be capable of making changes to the system that require elevated privileges.</span></span> <span data-ttu-id="dc789-114">這些自訂動作必須是執行腳本時執行的延後自訂動作。</span><span class="sxs-lookup"><span data-stu-id="dc789-114">These custom actions must be deferred custom actions that run when in the execution script.</span></span>
-   <span data-ttu-id="dc789-115">每個帳戶都有復原自訂動作，以確保帳戶會在元件安裝復原時移除。</span><span class="sxs-lookup"><span data-stu-id="dc789-115">Each account has a rollback custom action to ensure the account is removed on rollback of the component installation.</span></span> <span data-ttu-id="dc789-116">這不包括在移除元件期間復原刪除帳戶。</span><span class="sxs-lookup"><span data-stu-id="dc789-116">This does not include the rollback of an account deletion during the removal of a component.</span></span>
-   <span data-ttu-id="dc789-117">自訂動作會傳送每個建立或移除的帳戶的 ActionData 訊息。</span><span class="sxs-lookup"><span data-stu-id="dc789-117">Custom actions send ActionData messages for each account that is created or removed.</span></span> <span data-ttu-id="dc789-118">這不包括提供 ProgressBar 的進度訊息。</span><span class="sxs-lookup"><span data-stu-id="dc789-118">This does not include providing progress messages for the ProgressBar.</span></span>
-   <span data-ttu-id="dc789-119">如果無法建立帳戶，自訂動作會報告錯誤。</span><span class="sxs-lookup"><span data-stu-id="dc789-119">Custom actions report an error if an account cannot be created.</span></span>
-   <span data-ttu-id="dc789-120">帳戶的密碼是透過使用者與使用者介面互動，或在基本 UI 或無 [消費者介面層級](user-interface-levels.md)進行安裝的情況下取得，作為在命令列上傳遞的屬性。</span><span class="sxs-lookup"><span data-stu-id="dc789-120">The password for the account is obtained through the user interaction with the user interface, or in the case of an installation at the Basic UI or None [User Interface Levels](user-interface-levels.md), as a property passed on the command line.</span></span>
-   <span data-ttu-id="dc789-121">記錄檔中會隱藏敏感性資料。</span><span class="sxs-lookup"><span data-stu-id="dc789-121">Sensitive data is hidden from the log file.</span></span>

<span data-ttu-id="dc789-122">此範例包含名為 TestAccount 的假想元件。</span><span class="sxs-lookup"><span data-stu-id="dc789-122">The sample includes a hypothetical component named TestAccount.</span></span> <span data-ttu-id="dc789-123">下列各節中的討論會假設您已建立 TestAccount 所需的資源，並在安裝此元件所需的範例資料庫中撰寫了 [Feature](feature-table.md)、 [Component](component-table.md)、 [File](file-table.md)、 [Directory](directory-table.md)和 [FeatureComponents](featurecomponents-table.md) 資料表。</span><span class="sxs-lookup"><span data-stu-id="dc789-123">The discussion in the following sections assumes that you have already created the resources required by TestAccount and have authored the [Feature](feature-table.md), [Component](component-table.md), [File](file-table.md), [Directory](directory-table.md), and [FeatureComponents](featurecomponents-table.md) tables in the sample database required to install this component.</span></span> <span data-ttu-id="dc789-124">如需詳細資訊，請參閱 [安裝範例](an-installation-example.md)。</span><span class="sxs-lookup"><span data-stu-id="dc789-124">For more information, see [An Installation Example](an-installation-example.md).</span></span>

<span data-ttu-id="dc789-125">下列主題包含有關如何建立必要的自訂動作，並將其新增至安裝套件的資訊。</span><span class="sxs-lookup"><span data-stu-id="dc789-125">The following topics contain information about how to create required custom actions and add them to an installation package.</span></span>

-   [<span data-ttu-id="dc789-126">撰寫自訂動作</span><span class="sxs-lookup"><span data-stu-id="dc789-126">Authoring the Custom Actions</span></span>](authoring-the-custom-actions.md)
-   [<span data-ttu-id="dc789-127">新增自訂 CustomUserAccounts 資料表</span><span class="sxs-lookup"><span data-stu-id="dc789-127">Adding a Custom CustomUserAccounts Table</span></span>](adding-a-custom-customuseraccounts-table.md)
-   [<span data-ttu-id="dc789-128">撰寫 CustomAction 資料表</span><span class="sxs-lookup"><span data-stu-id="dc789-128">Authoring the CustomAction Table</span></span>](authoring-the-customaction-table.md)
-   [<span data-ttu-id="dc789-129">撰寫 ActionText 和錯誤資料表</span><span class="sxs-lookup"><span data-stu-id="dc789-129">Authoring the ActionText and Error Tables</span></span>](authoring-the-actiontext-and-error-tables.md)
-   [<span data-ttu-id="dc789-130">撰寫 InstallExecuteSequence 資料表</span><span class="sxs-lookup"><span data-stu-id="dc789-130">Authoring the InstallExecuteSequence Table</span></span>](authoring-the-installexecutesequence-table.md)
-   [<span data-ttu-id="dc789-131">撰寫密碼輸入的消費者介面</span><span class="sxs-lookup"><span data-stu-id="dc789-131">Authoring the User Interface for Password Input</span></span>](authoring-the-user-interface-for-password-input.md)
-   [<span data-ttu-id="dc789-132">保護安裝的安全</span><span class="sxs-lookup"><span data-stu-id="dc789-132">Securing the installation</span></span>](securing-the-installation.md)

 

 




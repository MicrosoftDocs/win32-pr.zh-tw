---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ms.assetid: 541fd08c-c21a-4a51-aa1c-d65cc0f5da75
title: " (Windows Installer) "
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46677d8823c5298307db922f2d61285564add437
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115397"
---
# <a name="a-windows-installer"></a><span data-ttu-id="7829f-103"> (Windows Installer) </span><span class="sxs-lookup"><span data-stu-id="7829f-103">A (Windows Installer)</span></span>

<span data-ttu-id="7829f-104">[B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [](u-gly.md) [W X](v-gly.md) Y Z</span><span class="sxs-lookup"><span data-stu-id="7829f-104">A [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="7829f-105"><span id="_msi_accessibility_using_windows_installer_gly"></span><span id="_MSI_ACCESSIBILITY_USING_WINDOWS_INSTALLER_GLY"></span>**工具**</span><span class="sxs-lookup"><span data-stu-id="7829f-105"><span id="_msi_accessibility_using_windows_installer_gly"></span><span id="_MSI_ACCESSIBILITY_USING_WINDOWS_INSTALLER_GLY"></span>**accessibility**</span></span>
</dt> <dd>

<span data-ttu-id="7829f-106">讓所有使用者都能存取安裝程式之使用者介面的設計實行。</span><span class="sxs-lookup"><span data-stu-id="7829f-106">Design implementation for making the installer's user interface accessible to all users.</span></span> <span data-ttu-id="7829f-107">如需協助工具的詳細資訊，請參閱總覽主題： [協助工具](accessibility.md)。</span><span class="sxs-lookup"><span data-stu-id="7829f-107">For more information about accessibility, see the overview topic: [Accessibility](accessibility.md).</span></span>

</dd> <dt>

<span data-ttu-id="7829f-108"><span id="_msi_acquisition_phase_gly"></span><span id="_MSI_ACQUISITION_PHASE_GLY"></span>**取得階段**</span><span class="sxs-lookup"><span data-stu-id="7829f-108"><span id="_msi_acquisition_phase_gly"></span><span id="_MSI_ACQUISITION_PHASE_GLY"></span>**acquisition phase**</span></span>
</dt> <dd>

<span data-ttu-id="7829f-109">安裝程式用來決定程式的安裝階段。</span><span class="sxs-lookup"><span data-stu-id="7829f-109">Phase of installation during which the installer determines procedure.</span></span> <span data-ttu-id="7829f-110">取得階段會在應用程式或使用者指示 [*Windows Installer*](m-gly.md) 安裝應用程式或功能時開始。</span><span class="sxs-lookup"><span data-stu-id="7829f-110">Acquisition phase begins when an application or user instructs [*Windows Installer*](m-gly.md) to install an application or feature.</span></span> <span data-ttu-id="7829f-111">然後，安裝程式會在資料庫產生安裝的 [*執行腳本*](e-gly.md)時，查詢 [*資料庫*](i-gly.md)中的資訊。</span><span class="sxs-lookup"><span data-stu-id="7829f-111">The installer then queries the [*database*](i-gly.md) for information as it generates the [*execution script*](e-gly.md) for the installation.</span></span> <span data-ttu-id="7829f-112">如需有關安裝階段的詳細資訊，請參閱 [安裝機制](installation-mechanism.md)。</span><span class="sxs-lookup"><span data-stu-id="7829f-112">For more information about the phases of an installation, see [Installation Mechanism](installation-mechanism.md).</span></span>

</dd> <dt>

<span data-ttu-id="7829f-113"><span id="_msi_action_gly"></span><span id="_MSI_ACTION_GLY"></span>**行動**</span><span class="sxs-lookup"><span data-stu-id="7829f-113"><span id="_msi_action_gly"></span><span id="_MSI_ACTION_GLY"></span>**action**</span></span>
</dt> <dd>

<span data-ttu-id="7829f-114">Windows Installer 所執行的許多函數都會封裝至動作中。</span><span class="sxs-lookup"><span data-stu-id="7829f-114">Many of the functions performed by Windows Installer are encapsulated into actions.</span></span> <span data-ttu-id="7829f-115">每個動作都會指定特定函式的執行，而安裝程式的總程式流程則是依 [*順序資料表*](s-gly.md)中的動作順序來指定。</span><span class="sxs-lookup"><span data-stu-id="7829f-115">Each action specifies the execution of a particular function and the total procedural flow of the installation is prescribed by the sequence of actions in the [*Sequence tables*](s-gly.md).</span></span> <span data-ttu-id="7829f-116">Windows Installer 中內建 [*標準動作*](s-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="7829f-116">[*Standard actions*](s-gly.md) are built into Windows Installer.</span></span> <span data-ttu-id="7829f-117">[*自訂動作*](c-gly.md) 是由安裝 [*套件*](p-gly.md)的作者所撰寫。</span><span class="sxs-lookup"><span data-stu-id="7829f-117">[*Custom actions*](c-gly.md) are written by the author of the installation [*package*](p-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="7829f-118"><span id="_msi_admin_approval_mode_gly"></span><span id="_MSI_ADMIN_APPROVAL_MODE_GLY"></span>**管理核准模式**</span><span class="sxs-lookup"><span data-stu-id="7829f-118"><span id="_msi_admin_approval_mode_gly"></span><span id="_MSI_ADMIN_APPROVAL_MODE_GLY"></span>**Admin Approval Mode**</span></span>
</dt> <dd>

<span data-ttu-id="7829f-119">使用者帳戶保護所啟用的核准狀態 (UAC) ，以最小許可權（包括系統管理員）執行所有使用者。</span><span class="sxs-lookup"><span data-stu-id="7829f-119">The approval state enabled by User Account Protection (UAC) that runs all users with least privilege, including administrators.</span></span> <span data-ttu-id="7829f-120">使用者必須提供同意，才能提升需要系統管理員許可權的安裝。</span><span class="sxs-lookup"><span data-stu-id="7829f-120">Users are required to provide consent to elevate installations that require administrator privileges.</span></span>

</dd> <dt>

<span data-ttu-id="7829f-121"><span id="_msi_advertising_gly"></span><span id="_MSI_ADVERTISING_GLY"></span>**廣告**</span><span class="sxs-lookup"><span data-stu-id="7829f-121"><span id="_msi_advertising_gly"></span><span id="_MSI_ADVERTISING_GLY"></span>**advertising**</span></span>
</dt> <dd>

<span data-ttu-id="7829f-122">能夠讓載入所需的介面，並讓應用程式可供使用，而不需要安裝應用程式。</span><span class="sxs-lookup"><span data-stu-id="7829f-122">Capability to make the interfaces required for loading and to make an application available without installing the application.</span></span> <span data-ttu-id="7829f-123">當使用者或應用程式啟動已公告的介面時，安裝程式就會繼續安裝必要的元件。</span><span class="sxs-lookup"><span data-stu-id="7829f-123">When a user or application activates an advertised interface, the installer then proceeds to install the necessary components.</span></span> <span data-ttu-id="7829f-124">這兩種類型的廣告是 [*指派*](/windows) 和 [*發佈*](p-gly.md)的。</span><span class="sxs-lookup"><span data-stu-id="7829f-124">The two types of advertising are [*assigning*](/windows) and [*publishing*](p-gly.md).</span></span> <span data-ttu-id="7829f-125">如需詳細資訊，請參閱 [*隨選安裝*](i-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="7829f-125">For more information, see also [*install-on-demand*](i-gly.md).</span></span> <span data-ttu-id="7829f-126">如需安裝程式如何通告應用程式的詳細資訊，請參閱 [公告](advertisement.md)。</span><span class="sxs-lookup"><span data-stu-id="7829f-126">For more information about how the installer advertises applications, see [Advertisement](advertisement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7829f-127"><span id="_msi_application_information_service_gly"></span><span id="_MSI_APPLICATION_INFORMATION_SERVICE_GLY"></span>**應用程式資訊服務 (AIS)**</span><span class="sxs-lookup"><span data-stu-id="7829f-127"><span id="_msi_application_information_service_gly"></span><span id="_MSI_APPLICATION_INFORMATION_SERVICE_GLY"></span>**Application Information Service (AIS)**</span></span>
</dt> <dd>

<span data-ttu-id="7829f-128">Windows Vista 的系統服務，可協助您開始執行需要提高許可權才能執行的安裝。</span><span class="sxs-lookup"><span data-stu-id="7829f-128">A system service of Windows Vista that facilitates starting installations that require elevated privileges to run.</span></span> <span data-ttu-id="7829f-129">提供使用者帳戶控制用來提示使用者提供系統管理員授權的同意 UI。</span><span class="sxs-lookup"><span data-stu-id="7829f-129">Provides the Consent UI used by User Account Control to prompt a user for administrator authorization.</span></span>

</dd> <dt>

<span data-ttu-id="7829f-130"><span id="_msi_assigning_gly"></span><span id="_MSI_ASSIGNING_GLY"></span>**分配**</span><span class="sxs-lookup"><span data-stu-id="7829f-130"><span id="_msi_assigning_gly"></span><span id="_MSI_ASSIGNING_GLY"></span>**assigning**</span></span>
</dt> <dd>

<span data-ttu-id="7829f-131">讓應用程式可供使用，並讓它看起來好像已安裝給使用者，而不需要實際安裝。</span><span class="sxs-lookup"><span data-stu-id="7829f-131">Makes an application available, and makes it appear as if it has been installed to a user, without actually installing it.</span></span> <span data-ttu-id="7829f-132">指派會在 [ **開始** ] 功能表中加入快捷方式和圖示、關聯適當的檔案，以及寫入應用程式的登錄專案。</span><span class="sxs-lookup"><span data-stu-id="7829f-132">Assigning adds shortcuts and icons to the **Start** menu, associates appropriate files, and writes registry entries for the application.</span></span> <span data-ttu-id="7829f-133">當使用者嘗試開啟指派的應用程式時，安裝程式會安裝應用程式。</span><span class="sxs-lookup"><span data-stu-id="7829f-133">When a user tries to open an assigned application, then the installer installs the application.</span></span> <span data-ttu-id="7829f-134">指派和 [*發佈*](p-gly.md) 是兩種 [*廣告*](/windows)方法。</span><span class="sxs-lookup"><span data-stu-id="7829f-134">Assigning and [*publishing*](p-gly.md) are two methods of [*advertising*](/windows).</span></span> <span data-ttu-id="7829f-135">如需詳細資訊，請參閱 [公告](advertisement.md)。</span><span class="sxs-lookup"><span data-stu-id="7829f-135">For more information, see [Advertisement](advertisement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7829f-136"><span id="_msi_asynchronous_execution_using_windows_installer_gly"></span><span id="_MSI_ASYNCHRONOUS_EXECUTION_USING_WINDOWS_INSTALLER_GLY"></span>**非同步執行**</span><span class="sxs-lookup"><span data-stu-id="7829f-136"><span id="_msi_asynchronous_execution_using_windows_installer_gly"></span><span id="_MSI_ASYNCHRONOUS_EXECUTION_USING_WINDOWS_INSTALLER_GLY"></span>**asynchronous execution**</span></span>
</dt> <dd>

<span data-ttu-id="7829f-137">[*自訂動作*](c-gly.md) ，在此期間，安裝程式會同時執行自訂動作的個別執行緒和目前的安裝。</span><span class="sxs-lookup"><span data-stu-id="7829f-137">[*Custom action*](c-gly.md) during which the installer runs separate threads of the custom action and the current installation simultaneously.</span></span> <span data-ttu-id="7829f-138">如需詳細資訊，請參閱 [同步和非同步自訂動作](synchronous-and-asynchronous-custom-actions.md)。</span><span class="sxs-lookup"><span data-stu-id="7829f-138">For more information, see [Synchronous and Asynchronous Custom Actions](synchronous-and-asynchronous-custom-actions.md).</span></span>

</dd> </dl>

 

 

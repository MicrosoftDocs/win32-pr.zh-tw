---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ms.assetid: b8e0a14f-ebdc-4b8f-a884-f6276dccda49
title: '我 (Windows Installer) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca95a473f648ca9e1a08773d93f47bd198df11e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850191"
---
# <a name="i-windows-installer"></a><span data-ttu-id="28a8d-103">我 (Windows Installer) </span><span class="sxs-lookup"><span data-stu-id="28a8d-103">I (Windows Installer)</span></span>

<span data-ttu-id="28a8d-104">[](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H I J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [](u-gly.md) [W X](v-gly.md) Y Z</span><span class="sxs-lookup"><span data-stu-id="28a8d-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H I J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="28a8d-105"><span id="_msi_.idt_file_gly"></span><span id="_MSI_.IDT_FILE_GLY"></span>**idt 檔案**</span><span class="sxs-lookup"><span data-stu-id="28a8d-105"><span id="_msi_.idt_file_gly"></span><span id="_MSI_.IDT_FILE_GLY"></span>**.idt file**</span></span>
</dt> <dd>

<span data-ttu-id="28a8d-106">匯出的安裝程式資料庫資料表。</span><span class="sxs-lookup"><span data-stu-id="28a8d-106">Exported installer database table.</span></span> <span data-ttu-id="28a8d-107">如需詳細資訊，請參閱匯 [入和匯出](importing-and-exporting.md) 和 [Windows Installer 副檔名](windows-installer-file-extensions.md)。</span><span class="sxs-lookup"><span data-stu-id="28a8d-107">For more information, see [Importing and Exporting](importing-and-exporting.md) and [Windows Installer File Extensions](windows-installer-file-extensions.md).</span></span>

</dd> <dt>

<span data-ttu-id="28a8d-108"><span id="_msi_import_address_table_gly"></span><span id="_MSI_IMPORT_ADDRESS_TABLE_GLY"></span>**匯入位址表 (IAT)**</span><span class="sxs-lookup"><span data-stu-id="28a8d-108"><span id="_msi_import_address_table_gly"></span><span id="_MSI_IMPORT_ADDRESS_TABLE_GLY"></span>**Import Address table (IAT)**</span></span>
</dt> <dd>

<span data-ttu-id="28a8d-109">從所有 Dll 匯入的每個函式都會儲存計算的虛擬位址。</span><span class="sxs-lookup"><span data-stu-id="28a8d-109">Where the computed virtual address is saved from each function imported from all DLLs.</span></span>

</dd> <dt>

<span data-ttu-id="28a8d-110"><span id="_msi_internal_user_interface_gly"></span><span id="_MSI_INTERNAL_USER_INTERFACE_GLY"></span>**內部使用者介面**</span><span class="sxs-lookup"><span data-stu-id="28a8d-110"><span id="_msi_internal_user_interface_gly"></span><span id="_MSI_INTERNAL_USER_INTERFACE_GLY"></span>**internal user interface**</span></span>
</dt> <dd>

<span data-ttu-id="28a8d-111">安裝程式的內建功能，可以用來撰寫圖形化 UI 以進行安裝。</span><span class="sxs-lookup"><span data-stu-id="28a8d-111">Built-in capabilities of the installer that can be used to author a graphical UI for installation.</span></span> <span data-ttu-id="28a8d-112">作者可以選擇 [*外部使用者介面*](e-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="28a8d-112">An author may choose an [*external user interface*](e-gly.md).</span></span> <span data-ttu-id="28a8d-113">如需詳細資訊，請參閱 [關於消費者介面](about-the-user-interface.md)。</span><span class="sxs-lookup"><span data-stu-id="28a8d-113">For more information, see [About the User Interface](about-the-user-interface.md).</span></span>

</dd> <dt>

<span data-ttu-id="28a8d-114"><span id="_msi_install_level_gly"></span><span id="_MSI_INSTALL_LEVEL_GLY"></span>**安裝層級**</span><span class="sxs-lookup"><span data-stu-id="28a8d-114"><span id="_msi_install_level_gly"></span><span id="_MSI_INSTALL_LEVEL_GLY"></span>**install level**</span></span>
</dt> <dd>

<span data-ttu-id="28a8d-115">指定的安裝值。</span><span class="sxs-lookup"><span data-stu-id="28a8d-115">Specified installation value.</span></span> <span data-ttu-id="28a8d-116">只有當應用程式的層級小於或等於安裝層級時，才會安裝應用程式。</span><span class="sxs-lookup"><span data-stu-id="28a8d-116">An application is installed only if its own level is less than or equal to the install level.</span></span> <span data-ttu-id="28a8d-117">因此，您可以藉由改變安裝層級來變更安裝所選擇的應用程式集。</span><span class="sxs-lookup"><span data-stu-id="28a8d-117">The set of applications chosen for installation can therefore be changed by altering the install level.</span></span> <span data-ttu-id="28a8d-118">如需詳細資訊，請參閱 [功能表](feature-table.md)。</span><span class="sxs-lookup"><span data-stu-id="28a8d-118">For more information, see [Feature Table](feature-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="28a8d-119"><span id="_msi_install_on_demand_gly"></span><span id="_MSI_INSTALL_ON_DEMAND_GLY"></span>**隨選安裝**</span><span class="sxs-lookup"><span data-stu-id="28a8d-119"><span id="_msi_install_on_demand_gly"></span><span id="_MSI_INSTALL_ON_DEMAND_GLY"></span>**installation-on-demand**</span></span>
</dt> <dd>

<span data-ttu-id="28a8d-120">依使用者或其他應用程式的要求安裝應用程式或功能的服務。</span><span class="sxs-lookup"><span data-stu-id="28a8d-120">Service that installs applications or features as requested by the user or another application.</span></span> <span data-ttu-id="28a8d-121">[*廣告*](a-gly.md) 讓功能或應用程式可用於隨選安裝。</span><span class="sxs-lookup"><span data-stu-id="28a8d-121">[*Advertising*](a-gly.md) makes a feature or application available for install-on-demand installation.</span></span> <span data-ttu-id="28a8d-122">如需詳細資訊，請參閱： [隨選安裝](installation-on-demand.md)。</span><span class="sxs-lookup"><span data-stu-id="28a8d-122">For more information, see: [Installation-on-Demand](installation-on-demand.md).</span></span>

</dd> <dt>

<span data-ttu-id="28a8d-123"><span id="_msi_installation_context_gly"></span><span id="_MSI_INSTALLATION_CONTEXT_GLY"></span>**安裝內容**</span><span class="sxs-lookup"><span data-stu-id="28a8d-123"><span id="_msi_installation_context_gly"></span><span id="_MSI_INSTALLATION_CONTEXT_GLY"></span>**installation context**</span></span>
</dt> <dd>

<span data-ttu-id="28a8d-124">安裝許可權與安裝類型的組合會產生三個不同的安裝內容：每位使用者的非受控、每位使用者管理，以及每部電腦管理的內容。</span><span class="sxs-lookup"><span data-stu-id="28a8d-124">The combination of installation rights and installation types produces three different installation contexts: per-user non-managed, per-user managed, and per-machine managed.</span></span> <span data-ttu-id="28a8d-125">每一部電腦都沒有這類的非受控功能。</span><span class="sxs-lookup"><span data-stu-id="28a8d-125">There is no such thing as per-machine non-managed.</span></span>

</dd> <dt>

<span data-ttu-id="28a8d-126"><span id="_msi_installer_gly"></span><span id="_MSI_INSTALLER_GLY"></span>**安裝**</span><span class="sxs-lookup"><span data-stu-id="28a8d-126"><span id="_msi_installer_gly"></span><span id="_MSI_INSTALLER_GLY"></span>**installer**</span></span>
</dt> <dd>

<span data-ttu-id="28a8d-127">[*Windows Installer*](m-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="28a8d-127">The [*Windows Installer*](m-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="28a8d-128"><span id="_msi_installer_database_gly"></span><span id="_MSI_INSTALLER_DATABASE_GLY"></span>**安裝程式資料庫**</span><span class="sxs-lookup"><span data-stu-id="28a8d-128"><span id="_msi_installer_database_gly"></span><span id="_MSI_INSTALLER_DATABASE_GLY"></span>**installer database**</span></span>
</dt> <dd>

<span data-ttu-id="28a8d-129">關係資料庫，其中包含安裝的安裝指示。</span><span class="sxs-lookup"><span data-stu-id="28a8d-129">Relational database containing setup instructions for an installation.</span></span> <span data-ttu-id="28a8d-130">安裝程式資料庫會儲存在 [*.msi*](m-gly.md)檔案中。</span><span class="sxs-lookup"><span data-stu-id="28a8d-130">The installer database is stored in the [*.msi file*](m-gly.md).</span></span> <span data-ttu-id="28a8d-131">如需詳細資訊，請參閱 [安裝程式資料庫](installer-database.md)。</span><span class="sxs-lookup"><span data-stu-id="28a8d-131">For more information, see [Installer Database](installer-database.md).</span></span>

</dd> <dt>

<span data-ttu-id="28a8d-132"><span id="_msi_installer_function_gly"></span><span id="_MSI_INSTALLER_FUNCTION_GLY"></span>**安裝程式函數**</span><span class="sxs-lookup"><span data-stu-id="28a8d-132"><span id="_msi_installer_function_gly"></span><span id="_MSI_INSTALLER_FUNCTION_GLY"></span>**installer function**</span></span>
</dt> <dd>

<span data-ttu-id="28a8d-133">由使用者或應用程式呼叫，以取得安裝程式服務和功能。</span><span class="sxs-lookup"><span data-stu-id="28a8d-133">Called by a user or application to obtain installer services and functionality.</span></span> <span data-ttu-id="28a8d-134">這是安裝程式的應用程式開發介面。</span><span class="sxs-lookup"><span data-stu-id="28a8d-134">This is the application programming interface of the installer.</span></span> <span data-ttu-id="28a8d-135">如需詳細資訊，請參閱 [安裝程式函數參考](installer-function-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="28a8d-135">For information, see [Installer Function Reference](installer-function-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="28a8d-136"><span id="_msi_installer_package_authoring_tool_gly"></span><span id="_MSI_INSTALLER_PACKAGE_AUTHORING_TOOL_GLY"></span>**安裝程式套件 authoring tool**</span><span class="sxs-lookup"><span data-stu-id="28a8d-136"><span id="_msi_installer_package_authoring_tool_gly"></span><span id="_MSI_INSTALLER_PACKAGE_AUTHORING_TOOL_GLY"></span>**installer package authoring tool**</span></span>
</dt> <dd>

<span data-ttu-id="28a8d-137">可讓開發人員建立和編輯 [*.msi*](m-gly.md)檔案的軟體。</span><span class="sxs-lookup"><span data-stu-id="28a8d-137">Software that enables a developer to create and edit an [*.msi file*](m-gly.md).</span></span> <span data-ttu-id="28a8d-138">這與任何 [*外部來源*](e-gly.md) 檔案都包含一個 [*套件*](p-gly.md) ，其中包含安裝所需的所有資訊。</span><span class="sxs-lookup"><span data-stu-id="28a8d-138">This together with any [*external source files*](e-gly.md) comprise a [*package*](p-gly.md) containing all the information required for an installation.</span></span>

</dd> <dt>

<span data-ttu-id="28a8d-139"><span id="_msi_internal_source_files_gly"></span><span id="_MSI_INTERNAL_SOURCE_FILES_GLY"></span>**內部來源檔案**</span><span class="sxs-lookup"><span data-stu-id="28a8d-139"><span id="_msi_internal_source_files_gly"></span><span id="_MSI_INTERNAL_SOURCE_FILES_GLY"></span>**internal source files**</span></span>
</dt> <dd>

<span data-ttu-id="28a8d-140">儲存在 [*.msi*](m-gly.md)檔案中。</span><span class="sxs-lookup"><span data-stu-id="28a8d-140">Stored in the [*.msi file*](m-gly.md).</span></span> <span data-ttu-id="28a8d-141">您可以將多個內部來源檔案壓縮並儲存在 .msi 檔案中儲存的封 [*包*](c-gly.md) 檔中。</span><span class="sxs-lookup"><span data-stu-id="28a8d-141">Multiple internal source files can be compressed and stored together in a [*cabinet file*](c-gly.md) that is stored within an .msi file.</span></span>

</dd> </dl>

 

 




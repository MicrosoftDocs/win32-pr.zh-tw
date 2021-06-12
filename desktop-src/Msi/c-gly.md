---
description: 瞭解以字母 C 為開頭的 Windows Installer 概念，例如封包檔和總和檢查碼。
ms.assetid: f98d19c5-5187-4718-b241-3ec69454c2d6
title: 'C (Windows Installer) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47e7af99ad32d8dff7f4e8509976b0004045477b
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010921"
---
# <a name="c-windows-installer"></a><span data-ttu-id="65a21-103">C (Windows Installer) </span><span class="sxs-lookup"><span data-stu-id="65a21-103">C (Windows Installer)</span></span>

<span data-ttu-id="65a21-104">[](a-gly.md) [B](b-gly.md) C [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [](u-gly.md) [W X](v-gly.md) Y Z</span><span class="sxs-lookup"><span data-stu-id="65a21-104">[A](a-gly.md) [B](b-gly.md) C [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="65a21-105"><span id="_msi_cabinet_file_using_windows_installer_gly"></span><span id="_MSI_CABINET_FILE_USING_WINDOWS_INSTALLER_GLY"></span>**封包檔**</span><span class="sxs-lookup"><span data-stu-id="65a21-105"><span id="_msi_cabinet_file_using_windows_installer_gly"></span><span id="_MSI_CABINET_FILE_USING_WINDOWS_INSTALLER_GLY"></span>**cabinet file**</span></span>
</dt> <dd>

<span data-ttu-id="65a21-106">單一檔案，通常會有 .cab 副檔名，可將壓縮檔案儲存在檔案庫中。</span><span class="sxs-lookup"><span data-stu-id="65a21-106">Single file, usually with a .cab extension, that stores compressed files in a file library.</span></span> <span data-ttu-id="65a21-107">封包格式是封裝多個檔案的有效方式，因為壓縮會跨檔案界限執行，大幅改善壓縮率。</span><span class="sxs-lookup"><span data-stu-id="65a21-107">The cabinet format is an efficient way to package multiple files because compression is performed across file boundaries, significantly improving compression ratio.</span></span> <span data-ttu-id="65a21-108">如需建立封包的相關資訊，請參閱封 [包](cabinet-files.md)檔。</span><span class="sxs-lookup"><span data-stu-id="65a21-108">For information about creating cabinets, see [Cabinet Files](cabinet-files.md).</span></span>

</dd> <dt>

<span data-ttu-id="65a21-109"><span id="_msi_checksum_gly"></span><span id="_MSI_CHECKSUM_GLY"></span>**校驗**</span><span class="sxs-lookup"><span data-stu-id="65a21-109"><span id="_msi_checksum_gly"></span><span id="_MSI_CHECKSUM_GLY"></span>**checksum**</span></span>
</dt> <dd>

<span data-ttu-id="65a21-110">相依于檔案內容的計算值。</span><span class="sxs-lookup"><span data-stu-id="65a21-110">Computed value that depends on the contents of a file.</span></span> <span data-ttu-id="65a21-111">它會與資料一起儲存，以偵測檔案損毀。</span><span class="sxs-lookup"><span data-stu-id="65a21-111">It is stored with data to detect file corruption.</span></span> <span data-ttu-id="65a21-112">系統會檢查此值，以確保資料不會被損壞。</span><span class="sxs-lookup"><span data-stu-id="65a21-112">The system checks this value to ensure that the data is uncorrupted.</span></span>

</dd> <dt>

<span data-ttu-id="65a21-113"><span id="_msi_component_using_windows_installer_gly"></span><span id="_MSI_COMPONENT_USING_WINDOWS_INSTALLER_GLY"></span>**元件**</span><span class="sxs-lookup"><span data-stu-id="65a21-113"><span id="_msi_component_using_windows_installer_gly"></span><span id="_MSI_COMPONENT_USING_WINDOWS_INSTALLER_GLY"></span>**component**</span></span>
</dt> <dd>

<span data-ttu-id="65a21-114">安裝程式所處理的最小部分安裝，也是來自程式設計人員觀點的應用程式或功能的組建區塊。</span><span class="sxs-lookup"><span data-stu-id="65a21-114">Smallest piece of an installation handled by the installer, also a building-block of an application or feature from the programmer's perspective.</span></span> <span data-ttu-id="65a21-115">元件的範例包括一組相關的檔案、COM 物件或程式庫。</span><span class="sxs-lookup"><span data-stu-id="65a21-115">Examples of components are a group of related files, a COM object, or a library.</span></span> <span data-ttu-id="65a21-116">如需詳細資訊，請參閱 [元件和功能](components-and-features.md)。</span><span class="sxs-lookup"><span data-stu-id="65a21-116">For more information, see [Components and Features](components-and-features.md).</span></span>

</dd> <dt>

<span data-ttu-id="65a21-117"><span id="_msi_committing_databases_using_windows_installer_gly"></span><span id="_MSI_COMMITTING_DATABASES_USING_WINDOWS_INSTALLER_GLY"></span>**認可資料庫**</span><span class="sxs-lookup"><span data-stu-id="65a21-117"><span id="_msi_committing_databases_using_windows_installer_gly"></span><span id="_MSI_COMMITTING_DATABASES_USING_WINDOWS_INSTALLER_GLY"></span>**committing databases**</span></span>
</dt> <dd>

<span data-ttu-id="65a21-118">在資料庫中進行的累積變更。</span><span class="sxs-lookup"><span data-stu-id="65a21-118">Accumulated changes made in a database.</span></span> <span data-ttu-id="65a21-119">在資料庫認可之前，這些變更不會反映在實際的資料庫中。</span><span class="sxs-lookup"><span data-stu-id="65a21-119">The changes are not reflected in the actual database until the database is committed.</span></span> <span data-ttu-id="65a21-120">如需詳細資訊，請參閱認可 [資料庫](committing-databases.md)。</span><span class="sxs-lookup"><span data-stu-id="65a21-120">For more information, see [Committing Databases](committing-databases.md).</span></span>

</dd> <dt>

<span data-ttu-id="65a21-121"><span id="_msi_controlevent_gly"></span><span id="_MSI_CONTROLEVENT_GLY"></span>**ControlEvent**</span><span class="sxs-lookup"><span data-stu-id="65a21-121"><span id="_msi_controlevent_gly"></span><span id="_MSI_CONTROLEVENT_GLY"></span>**ControlEvent**</span></span>
</dt> <dd>

<span data-ttu-id="65a21-122">安裝程式使用者介面的功能層面。</span><span class="sxs-lookup"><span data-stu-id="65a21-122">Aspect of functionality of the installer's user interface.</span></span> <span data-ttu-id="65a21-123">一般的 ControlEvent 會在啟動對話方塊控制項或其他事件時，觸發安裝程式的一些動作。</span><span class="sxs-lookup"><span data-stu-id="65a21-123">A typical ControlEvent triggers some action by the installer upon the activation of a dialog box control or other event.</span></span> <span data-ttu-id="65a21-124">如需詳細資訊，請參閱 [ControlEvent 總覽](controlevent-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="65a21-124">For more information, see [ControlEvent Overview](controlevent-overview.md).</span></span>

</dd> <dt>

<span data-ttu-id="65a21-125"><span id="_msi_costing_gly"></span><span id="_MSI_COSTING_GLY"></span>**成本**</span><span class="sxs-lookup"><span data-stu-id="65a21-125"><span id="_msi_costing_gly"></span><span id="_MSI_COSTING_GLY"></span>**costing**</span></span>
</dt> <dd>

<span data-ttu-id="65a21-126">安裝程式用來判斷安裝磁碟空間需求的方法。</span><span class="sxs-lookup"><span data-stu-id="65a21-126">Method used by the installer to determine disk space requirements for installation.</span></span> <span data-ttu-id="65a21-127">成本考慮會考慮是否需要覆寫現有的檔案。</span><span class="sxs-lookup"><span data-stu-id="65a21-127">Costing takes into account factors such as whether existing files need to be overwritten.</span></span> <span data-ttu-id="65a21-128">如需詳細資訊，請參閱檔案 [成本](file-costing.md)。</span><span class="sxs-lookup"><span data-stu-id="65a21-128">For more information, see [File Costing](file-costing.md).</span></span>

</dd> <dt>

<span data-ttu-id="65a21-129"><span id="_msi_.cub_file_gly"></span><span id="_MSI_.CUB_FILE_GLY"></span>**.cub 檔案**</span><span class="sxs-lookup"><span data-stu-id="65a21-129"><span id="_msi_.cub_file_gly"></span><span id="_MSI_.CUB_FILE_GLY"></span>**.cub file**</span></span>
</dt> <dd>

<span data-ttu-id="65a21-130">儲存和提供 ICE 自訂動作存取權的驗證模組。</span><span class="sxs-lookup"><span data-stu-id="65a21-130">Validation module that stores and provides access to ICE custom actions.</span></span> <span data-ttu-id="65a21-131">如需詳細資訊，請參閱 [範例 .cub](sample--cub-file.md)檔。</span><span class="sxs-lookup"><span data-stu-id="65a21-131">For more information, see [Sample .cub File](sample--cub-file.md).</span></span> <span data-ttu-id="65a21-132">如需詳細資訊，請參閱也 [Windows Installer 的副檔名](windows-installer-file-extensions.md)。</span><span class="sxs-lookup"><span data-stu-id="65a21-132">For more information, see also [Windows Installer File Extensions](windows-installer-file-extensions.md).</span></span>

</dd> <dt>

<span data-ttu-id="65a21-133"><span id="_msi_custom_action_using_windows_installer_gly"></span><span id="_MSI_CUSTOM_ACTION_USING_WINDOWS_INSTALLER_GLY"></span>**自訂動作**</span><span class="sxs-lookup"><span data-stu-id="65a21-133"><span id="_msi_custom_action_using_windows_installer_gly"></span><span id="_MSI_CUSTOM_ACTION_USING_WINDOWS_INSTALLER_GLY"></span>**custom action**</span></span>
</dt> <dd>

<span data-ttu-id="65a21-134">由 [*封裝*](p-gly.md) 的作者所撰寫，但不是以標準動作的形式內建在安裝程式中。</span><span class="sxs-lookup"><span data-stu-id="65a21-134">Written by the author of the [*package*](p-gly.md) but not built into the installer as a standard action.</span></span> <span data-ttu-id="65a21-135">如需詳細資訊，請參閱 [自訂動作](custom-actions.md)。</span><span class="sxs-lookup"><span data-stu-id="65a21-135">For more information, see [Custom Actions](custom-actions.md).</span></span>

</dd> </dl>

 

 




---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ms.assetid: 868f5ed3-b179-404b-9462-1d3a179103f8
title: 'P (Windows Installer) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a4e6b8f1343fdd68f4a6ce042852cff1e28e05c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115360"
---
# <a name="p-windows-installer"></a><span data-ttu-id="a436e-103">P (Windows Installer) </span><span class="sxs-lookup"><span data-stu-id="a436e-103">P (Windows Installer)</span></span>

<span data-ttu-id="a436e-104">[](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) P [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [](u-gly.md) [W X](v-gly.md) Y Z</span><span class="sxs-lookup"><span data-stu-id="a436e-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) P [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="a436e-105"><span id="_msi_package_using_windows_installer_gly"></span><span id="_MSI_PACKAGE_USING_WINDOWS_INSTALLER_GLY"></span>**包**</span><span class="sxs-lookup"><span data-stu-id="a436e-105"><span id="_msi_package_using_windows_installer_gly"></span><span id="_MSI_PACKAGE_USING_WINDOWS_INSTALLER_GLY"></span>**package**</span></span>
</dt> <dd>

<span data-ttu-id="a436e-106">[*.msi*](m-gly.md) 檔案，以及此檔案可能指向的任何 [*外部原始*](e-gly.md) 程式檔。</span><span class="sxs-lookup"><span data-stu-id="a436e-106">[*.msi file*](m-gly.md) and any [*external source files*](e-gly.md) that may be pointed to by this file.</span></span> <span data-ttu-id="a436e-107">因此，套件包含 Windows Installer 執行 UI 以及安裝或卸載應用程式所需的所有資訊。</span><span class="sxs-lookup"><span data-stu-id="a436e-107">A package therefore contains all the information the Windows Installer needs to run the UI and to install or uninstall the application.</span></span> <span data-ttu-id="a436e-108">如需詳細資訊，請參閱 [*安裝程式資料庫*](i-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="a436e-108">For more information, see also [*installer database*](i-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="a436e-109"><span id="_msi_package_code_gly"></span><span id="_MSI_PACKAGE_CODE_GLY"></span>**封裝程式碼**</span><span class="sxs-lookup"><span data-stu-id="a436e-109"><span id="_msi_package_code_gly"></span><span id="_MSI_PACKAGE_CODE_GLY"></span>**package code**</span></span>
</dt> <dd>

<span data-ttu-id="a436e-110">識別特定封裝的 GUID。</span><span class="sxs-lookup"><span data-stu-id="a436e-110">GUID that identifies a particular package.</span></span> <span data-ttu-id="a436e-111">需要唯一的封裝程式碼，因為某些轉換或修補套件可以套用至多個應用程式，或者可以將應用程式升級到另一個應用程式或版本。</span><span class="sxs-lookup"><span data-stu-id="a436e-111">A unique package code is required because some transforms or patch packages can be applied to more than one application or can upgrade an application into another application or version.</span></span> <span data-ttu-id="a436e-112">如需詳細資訊，請參閱 [封裝程式碼](package-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="a436e-112">For more information, see [Package Codes](package-codes.md).</span></span>

</dd> <dt>

<span data-ttu-id="a436e-113"><span id="_msi_patching_gly"></span><span id="_MSI_PATCHING_GLY"></span>**修補**</span><span class="sxs-lookup"><span data-stu-id="a436e-113"><span id="_msi_patching_gly"></span><span id="_MSI_PATCHING_GLY"></span>**patching**</span></span>
</dt> <dd>

<span data-ttu-id="a436e-114">更新檔案的方法，該檔案只會取代變更的位，而不是整個檔案。</span><span class="sxs-lookup"><span data-stu-id="a436e-114">Method of updating a file that replaces only the bits being changed, rather than the entire file.</span></span> <span data-ttu-id="a436e-115">這表示使用者可以下載產品的升級修補程式，而此產品遠小於整個產品。</span><span class="sxs-lookup"><span data-stu-id="a436e-115">This means that users can download an upgrade patch for a product that is much smaller than the entire product.</span></span> <span data-ttu-id="a436e-116">如需詳細資訊，請參閱 [修補套件](patch-packages.md)。</span><span class="sxs-lookup"><span data-stu-id="a436e-116">For more information, see [Patch Packages](patch-packages.md).</span></span>

</dd> <dt>

<span data-ttu-id="a436e-117"><span id="_msi_patch_file_gly"></span><span id="_MSI_PATCH_FILE_GLY"></span>**修補檔案**</span><span class="sxs-lookup"><span data-stu-id="a436e-117"><span id="_msi_patch_file_gly"></span><span id="_MSI_PATCH_FILE_GLY"></span>**patch file**</span></span>
</dt> <dd>

<span data-ttu-id="a436e-118">用於修補的 P [atch 套件](patch-packages.md) 。</span><span class="sxs-lookup"><span data-stu-id="a436e-118">P [atch package](patch-packages.md) used for patching.</span></span> <span data-ttu-id="a436e-119">如需詳細資訊，請參閱 [修補和升級](patching-and-upgrades.md)。</span><span class="sxs-lookup"><span data-stu-id="a436e-119">For more information, see [Patching and Upgrades](patching-and-upgrades.md).</span></span>

</dd> <dt>

<span data-ttu-id="a436e-120"><span id="_msi_preview_mode_using_windows_installer_gly"></span><span id="_MSI_PREVIEW_MODE_USING_WINDOWS_INSTALLER_GLY"></span>**預覽模式**</span><span class="sxs-lookup"><span data-stu-id="a436e-120"><span id="_msi_preview_mode_using_windows_installer_gly"></span><span id="_MSI_PREVIEW_MODE_USING_WINDOWS_INSTALLER_GLY"></span>**preview mode**</span></span>
</dt> <dd>

<span data-ttu-id="a436e-121">用來查看 UI 設計的模式。</span><span class="sxs-lookup"><span data-stu-id="a436e-121">Mode for viewing the design of the UI.</span></span> <span data-ttu-id="a436e-122">如需詳細資訊，請參閱 [預覽消費者介面](previewing-the-user-interface.md)。</span><span class="sxs-lookup"><span data-stu-id="a436e-122">For more information, see [Previewing the User Interface](previewing-the-user-interface.md).</span></span>

</dd> <dt>

<span data-ttu-id="a436e-123"><span id="_msi_progress_bar_gly"></span><span id="_MSI_PROGRESS_BAR_GLY"></span>**進度列**</span><span class="sxs-lookup"><span data-stu-id="a436e-123"><span id="_msi_progress_bar_gly"></span><span id="_MSI_PROGRESS_BAR_GLY"></span>**progress bar**</span></span>
</dt> <dd>

<span data-ttu-id="a436e-124">控制安裝程式可以在腳本執行時間顯示，以代表安裝進度。</span><span class="sxs-lookup"><span data-stu-id="a436e-124">Control the installer can display during script execution time representing the progress of the installation.</span></span> <span data-ttu-id="a436e-125">如需詳細資訊，請參閱 [撰寫 ProgressBar 控制項](authoring-a-progressbar-control.md)。</span><span class="sxs-lookup"><span data-stu-id="a436e-125">For more information, see [Authoring a ProgressBar Control](authoring-a-progressbar-control.md).</span></span>

</dd> <dt>

<span data-ttu-id="a436e-126"><span id="_msi_property_gly"></span><span id="_MSI_PROPERTY_GLY"></span>**財產**</span><span class="sxs-lookup"><span data-stu-id="a436e-126"><span id="_msi_property_gly"></span><span id="_MSI_PROPERTY_GLY"></span>**property**</span></span>
</dt> <dd>

<span data-ttu-id="a436e-127">在安裝期間使用的全域變數。</span><span class="sxs-lookup"><span data-stu-id="a436e-127">Global variables used during an installation.</span></span> <span data-ttu-id="a436e-128"> (查看 [屬性](about-properties.md)。 ) </span><span class="sxs-lookup"><span data-stu-id="a436e-128">(See [About Properties](about-properties.md).)</span></span>

<span data-ttu-id="a436e-129">「屬性」一詞也指的是 automation 物件的屬性。</span><span class="sxs-lookup"><span data-stu-id="a436e-129">The term "property" also refers to an attribute of an automation object.</span></span> <span data-ttu-id="a436e-130"> (請參閱 [Automation 介面](automation-interface.md)。 ) </span><span class="sxs-lookup"><span data-stu-id="a436e-130">(See [Automation Interface](automation-interface.md).)</span></span>

</dd> <dt>

<span data-ttu-id="a436e-131"><span id="_msi_publishing_gly"></span><span id="_MSI_PUBLISHING_GLY"></span>**出版**</span><span class="sxs-lookup"><span data-stu-id="a436e-131"><span id="_msi_publishing_gly"></span><span id="_MSI_PUBLISHING_GLY"></span>**publishing**</span></span>
</dt> <dd>

<span data-ttu-id="a436e-132">[*廣告*](a-gly.md)功能或應用程式的方法。</span><span class="sxs-lookup"><span data-stu-id="a436e-132">Method of [*advertising*](a-gly.md) a feature or application.</span></span> <span data-ttu-id="a436e-133">發佈不會填入 UI。</span><span class="sxs-lookup"><span data-stu-id="a436e-133">Publishing does not populate the UI.</span></span> <span data-ttu-id="a436e-134">但是，如果另一個應用程式嘗試開啟已發佈的應用程式，則安裝程式會有足夠的資訊來指派已發行的應用程式。</span><span class="sxs-lookup"><span data-stu-id="a436e-134">However, if another application attempts to open a published application, there is enough information present for the installer to assign the published application.</span></span> <span data-ttu-id="a436e-135">如需詳細資訊，請參閱 [*指派*](a-gly.md) 和 [元件和功能](components-and-features.md)。</span><span class="sxs-lookup"><span data-stu-id="a436e-135">For more information, see [*assigning*](a-gly.md) and [Components and Features](components-and-features.md).</span></span>

</dd> </dl>

 

 




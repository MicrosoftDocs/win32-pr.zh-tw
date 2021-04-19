---
description: Windows Installer 可以使用交易處理來安裝多個封裝。
ms.assetid: c4a0f4d8-818d-4e60-908b-adaa2a54de95
title: Multiple-Package 安裝
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65fa30893f353d6661a7f77fe23fe55b4c9b22c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977264"
---
# <a name="multiple-package-installations"></a><span data-ttu-id="93d21-103">Multiple-Package 安裝</span><span class="sxs-lookup"><span data-stu-id="93d21-103">Multiple-Package Installations</span></span>

<span data-ttu-id="93d21-104">Windows Installer 可以使用 [*交易處理*](t-gly.md)來安裝多個封裝。</span><span class="sxs-lookup"><span data-stu-id="93d21-104">Windows Installer can install multiple packages using [*transaction processing*](t-gly.md).</span></span> <span data-ttu-id="93d21-105">從 Windows Installer 4.5 開始，可以使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="93d21-105">This capability is available beginning with Windows Installer 4.5.</span></span> <span data-ttu-id="93d21-106">安裝程式將會安裝屬於多封裝交易的所有封裝，或不安裝任何套件。</span><span class="sxs-lookup"><span data-stu-id="93d21-106">The installer will install all the packages belonging to a multiple-package transaction or none of the packages.</span></span> <span data-ttu-id="93d21-107">如果無法順利安裝交易中的所有封裝，或如果使用者取消安裝，Windows Installer 可以復原變更，並將電腦還原為其原始狀態。</span><span class="sxs-lookup"><span data-stu-id="93d21-107">If all the packages in the transaction cannot be installed successfully, or if the user cancels the installation, the Windows Installer can roll back changes and restore the computer to its original state.</span></span>

<span data-ttu-id="93d21-108">多套件安裝封裝可以包含 [MsiEmbeddedChainer 資料表](msiembeddedchainer-table.md) ，該資料表會參考使用 [**MsiBeginTransaction**](/windows/desktop/api/Msi/nf-msi-msibegintransactiona)、 [**MsiJoinTransaction**](/windows/desktop/api/Msi/nf-msi-msijointransaction)和 [**MsiEndTransaction**](/windows/desktop/api/Msi/nf-msi-msiendtransaction) 函數的使用者定義函數。</span><span class="sxs-lookup"><span data-stu-id="93d21-108">A multiple-package installation package can contain a [MsiEmbeddedChainer table](msiembeddedchainer-table.md) that references a user-defined function that uses the [**MsiBeginTransaction**](/windows/desktop/api/Msi/nf-msi-msibegintransactiona), [**MsiJoinTransaction**](/windows/desktop/api/Msi/nf-msi-msijointransaction), and [**MsiEndTransaction**](/windows/desktop/api/Msi/nf-msi-msiendtransaction) functions.</span></span>

<span data-ttu-id="93d21-109">[MsiPackageCertificate 資料表](msipackagecertificate-table.md)會列出數位簽章憑證，用來驗證進行多套件安裝之安裝套件的身分識別。</span><span class="sxs-lookup"><span data-stu-id="93d21-109">The [MsiPackageCertificate Table](msipackagecertificate-table.md) lists digital signature certificates used to verify the identity of the installation packages that make a multiple-package installation.</span></span> <span data-ttu-id="93d21-110">您可以使用此表格來減少多套件安裝在需要系統管理員回應的 (UAC) 提示字元中，顯示 [*使用者帳戶控制*](u-gly.md) 的次數。</span><span class="sxs-lookup"><span data-stu-id="93d21-110">You can use this table to reduce the number of times your multiple-package installation displays a [*User Account Control*](u-gly.md) (UAC) prompt that requires a response by an administrator.</span></span>

<span data-ttu-id="93d21-111">下列 Windows Installer 功能可在 Windows Installer 安裝、修復、更新或移除應用程式時，對使用者的電腦進行變更。</span><span class="sxs-lookup"><span data-stu-id="93d21-111">The following Windows Installer functions can make changes to the user's computer when the Windows Installer installs, repairs, updates, or removes applications.</span></span> <span data-ttu-id="93d21-112">從 Windows Installer 4.5 開始，安裝程式可以在多套件安裝的 [*交易處理*](t-gly.md) 期間復原這些函數所做的變更：</span><span class="sxs-lookup"><span data-stu-id="93d21-112">Beginning with Windows Installer 4.5, the installer can roll back changes made by these functions during the [*transaction processing*](t-gly.md) of a multiple-package installation:</span></span>

<dl>

[<span data-ttu-id="93d21-113">**MsiAdvertiseProduct**</span><span class="sxs-lookup"><span data-stu-id="93d21-113">**MsiAdvertiseProduct**</span></span>](/windows/desktop/api/Msi/nf-msi-msiadvertiseproducta)  
[<span data-ttu-id="93d21-114">**MsiAdvertiseProductEx**</span><span class="sxs-lookup"><span data-stu-id="93d21-114">**MsiAdvertiseProductEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa)  
[<span data-ttu-id="93d21-115">**MsiApplyMultiplePatches**</span><span class="sxs-lookup"><span data-stu-id="93d21-115">**MsiApplyMultiplePatches**</span></span>](/windows/desktop/api/Msi/nf-msi-msiapplymultiplepatchesa)  
[<span data-ttu-id="93d21-116">**MsiApplyPatch**</span><span class="sxs-lookup"><span data-stu-id="93d21-116">**MsiApplyPatch**</span></span>](/windows/desktop/api/Msi/nf-msi-msiapplypatcha)  
[<span data-ttu-id="93d21-117">**MsiConfigureFeature**</span><span class="sxs-lookup"><span data-stu-id="93d21-117">**MsiConfigureFeature**</span></span>](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea)  
[<span data-ttu-id="93d21-118">**MsiConfigureProduct**</span><span class="sxs-lookup"><span data-stu-id="93d21-118">**MsiConfigureProduct**</span></span>](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta)  
[<span data-ttu-id="93d21-119">**MsiConfigureProductEx**</span><span class="sxs-lookup"><span data-stu-id="93d21-119">**MsiConfigureProductEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msiconfigureproductexa)  
[<span data-ttu-id="93d21-120">**MsiInstallMissingComponent**</span><span class="sxs-lookup"><span data-stu-id="93d21-120">**MsiInstallMissingComponent**</span></span>](/windows/desktop/api/Msi/nf-msi-msiinstallmissingcomponenta)  
[<span data-ttu-id="93d21-121">**MsiInstallMissingFile**</span><span class="sxs-lookup"><span data-stu-id="93d21-121">**MsiInstallMissingFile**</span></span>](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea)  
[<span data-ttu-id="93d21-122">**MsiInstallProduct**</span><span class="sxs-lookup"><span data-stu-id="93d21-122">**MsiInstallProduct**</span></span>](/windows/desktop/api/Msi/nf-msi-msiinstallproducta)  
[<span data-ttu-id="93d21-123">**MsiProvideAssembly**</span><span class="sxs-lookup"><span data-stu-id="93d21-123">**MsiProvideAssembly**</span></span>](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya)  
[<span data-ttu-id="93d21-124">**MsiProvideComponent**</span><span class="sxs-lookup"><span data-stu-id="93d21-124">**MsiProvideComponent**</span></span>](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta)  
[<span data-ttu-id="93d21-125">**MsiProvideQualifiedComponent**</span><span class="sxs-lookup"><span data-stu-id="93d21-125">**MsiProvideQualifiedComponent**</span></span>](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta)  
[<span data-ttu-id="93d21-126">**MsiProvideQualifiedComponentEx**</span><span class="sxs-lookup"><span data-stu-id="93d21-126">**MsiProvideQualifiedComponentEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponentexa)  
[<span data-ttu-id="93d21-127">**MsiReinstallFeature**</span><span class="sxs-lookup"><span data-stu-id="93d21-127">**MsiReinstallFeature**</span></span>](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea)  
[<span data-ttu-id="93d21-128">**MsiReinstallProduct**</span><span class="sxs-lookup"><span data-stu-id="93d21-128">**MsiReinstallProduct**</span></span>](/windows/desktop/api/Msi/nf-msi-msireinstallproducta)  
[<span data-ttu-id="93d21-129">**MsiRemovePatches**</span><span class="sxs-lookup"><span data-stu-id="93d21-129">**MsiRemovePatches**</span></span>](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)  
</dl>

<span data-ttu-id="93d21-130">如果 Windows Installer 遇到屬於包含 [ForceReboot](forcereboot-action.md) 或 [ScheduleReboot](schedulereboot-action.md) 動作之多套件安裝的封裝，就會發生例外狀況。</span><span class="sxs-lookup"><span data-stu-id="93d21-130">There is an exception if the Windows Installer encounters a package belonging to a multiple-package installation that contains a [ForceReboot](forcereboot-action.md) or [ScheduleReboot](schedulereboot-action.md) action.</span></span> <span data-ttu-id="93d21-131">在此情況下，Windows Installer 不會安裝該套件。</span><span class="sxs-lookup"><span data-stu-id="93d21-131">In this case, Windows Installer does not install only that package.</span></span> <span data-ttu-id="93d21-132">您可以安裝屬於多套件安裝的其他套件，而這些套件不包含 ForceReboot 或 ScheduleReboot 動作。</span><span class="sxs-lookup"><span data-stu-id="93d21-132">Other packages belonging to the multiple-package installation, that do not contain a ForceReboot or ScheduleReboot action, can be installed.</span></span>

<span data-ttu-id="93d21-133">\*\*[Windows Installer 4.0 及更早版本](not-supported-in-windows-installer-4-0.md)：不支援多個封裝 Windows Installer 安裝的 [*交易處理*](t-gly.md) 。</span><span class="sxs-lookup"><span data-stu-id="93d21-133">\*\*[Windows Installer 4.0 and earlier](not-supported-in-windows-installer-4-0.md):  \*\*[*Transaction processing*](t-gly.md) of multiple-package Windows Installer installations is not supported.</span></span> <span data-ttu-id="93d21-134">這些版本的 Windows Installer 無法將多個封裝的安裝復原成單一交易。</span><span class="sxs-lookup"><span data-stu-id="93d21-134">These versions of the Windows Installer are unable to roll back the installation of multiple packages as a single transaction.</span></span>

<span data-ttu-id="93d21-135">**啟用 [遠端桌面服務](../termserv/terminal-services-portal.md) 角色的 Windows Server 2008 R2：** 不支援。</span><span class="sxs-lookup"><span data-stu-id="93d21-135">**Windows Server 2008 R2 with the [Remote Desktop Services](../termserv/terminal-services-portal.md) role enabled:** Not supported.</span></span> <span data-ttu-id="93d21-136">如果啟用[遠端桌面服務](../termserv/terminal-services-portal.md)角色，使用[MsiEmbeddedChainer 資料表](msiembeddedchainer-table.md)的多個套件安裝將會失敗。</span><span class="sxs-lookup"><span data-stu-id="93d21-136">A multiple package installation using the [MsiEmbeddedChainer table](msiembeddedchainer-table.md) fails if the [Remote Desktop Services](../termserv/terminal-services-portal.md) role is enabled.</span></span>

 

 

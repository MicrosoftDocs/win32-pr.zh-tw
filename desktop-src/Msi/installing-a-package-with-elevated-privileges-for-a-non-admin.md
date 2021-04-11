---
description: 系統管理員可以使用下列方法，讓非系統管理員使用者以提高的系統許可權安裝應用程式。
ms.assetid: 61b9297e-f45e-4f50-9001-9bae580e1bf4
title: 以較高的許可權安裝非系統管理員的封裝
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec81de333d6ca388017e03c96f739d7bd258a7c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852111"
---
# <a name="installing-a-package-with-elevated-privileges-for-a-non-admin"></a><span data-ttu-id="91c81-103">以較高的許可權安裝非系統管理員的封裝</span><span class="sxs-lookup"><span data-stu-id="91c81-103">Installing a Package with Elevated Privileges for a Non-Admin</span></span>

<span data-ttu-id="91c81-104">系統管理員可以使用下列方法，讓非系統管理員使用者以提高的系統許可權安裝應用程式。</span><span class="sxs-lookup"><span data-stu-id="91c81-104">An administrator can use the following methods to enable a non-administrator user to install an application with elevated system privileges.</span></span>

-   <span data-ttu-id="91c81-105">在具有 Windows Installer 的 Windows Vista 中，系統管理員群組的成員可以提供授權給非系統管理員，以透過 [*使用者帳戶控制*](u-gly.md) (uac) 來提高安裝的許可權，如 [使用 Windows Installer 與 uac](using-windows-installer-with-uac.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="91c81-105">In Windows Vista with Windows Installer, a member of the Administrators group can provide authorization for a non-administrator to elevate the installation through [*User Account Control*](u-gly.md) (UAC) as described in [Using Windows Installer with UAC](using-windows-installer-with-uac.md).</span></span>

    <span data-ttu-id="91c81-106">**Windows Vista：** 必填。</span><span class="sxs-lookup"><span data-stu-id="91c81-106">**Windows Vista:** Required.</span></span>

<span data-ttu-id="91c81-107">您也可以使用下列方法，以較高的系統許可權安裝應用程式。</span><span class="sxs-lookup"><span data-stu-id="91c81-107">The following methods can also be used to install an application with elevated system privileges.</span></span>

-   <span data-ttu-id="91c81-108">系統管理員可以使用應用程式部署和 [群組原則](/previous-versions/windows/desktop/Policy/group-policy-start-page)來指派或發佈 Windows Installer 套件，以公告使用者電腦上的應用程式。</span><span class="sxs-lookup"><span data-stu-id="91c81-108">An administrator can advertise an application on a user's computer by assigning or publishing the Windows Installer package using application deployment and [Group Policy](/previous-versions/windows/desktop/Policy/group-policy-start-page).</span></span> <span data-ttu-id="91c81-109">系統管理員會針對每部電腦安裝通告套件。</span><span class="sxs-lookup"><span data-stu-id="91c81-109">The administrator advertises the package for per-machine installation.</span></span> <span data-ttu-id="91c81-110">如果非系統管理員使用者接著安裝應用程式，則可以使用較高的許可權來執行安裝。</span><span class="sxs-lookup"><span data-stu-id="91c81-110">If a non-administrator user then installs the application, the installation can run with elevated privileges.</span></span> <span data-ttu-id="91c81-111">非系統管理員的使用者無法安裝需要較高系統許可權的 unadvertised 套件。</span><span class="sxs-lookup"><span data-stu-id="91c81-111">Non-administrator users cannot install unadvertised packages that require elevated system privileges.</span></span>
-   <span data-ttu-id="91c81-112">系統管理員可以移至使用者的電腦，並針對個別電腦的安裝 [公告](advertisement.md) 應用程式。</span><span class="sxs-lookup"><span data-stu-id="91c81-112">An administrator can go to the user's computer and [advertise](advertisement.md) the application for per-machine installation.</span></span> <span data-ttu-id="91c81-113">由於 Windows Installer 一律具有更高的許可權，而且在個別電腦 [安裝內容](installation-context.md)中執行安裝時，如果非系統管理員使用者接著安裝已公告的應用程式，則可以使用較高的許可權來執行安裝。</span><span class="sxs-lookup"><span data-stu-id="91c81-113">Because the Windows Installer always has elevated privileges while doing installs in the per-machine [installation context](installation-context.md), if a non-administrator user then installs the advertised application, the installation can run with elevated privileges.</span></span> <span data-ttu-id="91c81-114">非系統管理員的使用者仍然無法安裝需要較高許可權的 unadvertised 套件。</span><span class="sxs-lookup"><span data-stu-id="91c81-114">Non-administrator users still cannot install unadvertised packages that require elevated privileges.</span></span>
-   <span data-ttu-id="91c81-115">如果本機系統代理程式通告應用程式，則沒有許可權的使用者可以安裝需要較高許可權的已公告應用程式。</span><span class="sxs-lookup"><span data-stu-id="91c81-115">A non-privileged user can install an advertised application that requires elevated privileges if a local system agent advertises the application.</span></span> <span data-ttu-id="91c81-116">您可以針對每個使用者或個別電腦的安裝來公告應用程式。</span><span class="sxs-lookup"><span data-stu-id="91c81-116">The application can be advertised for a per-user or per-machine installation.</span></span> <span data-ttu-id="91c81-117">使用此方法安裝的應用程式會被視為受管理。</span><span class="sxs-lookup"><span data-stu-id="91c81-117">An application installed using this method is considered managed.</span></span> <span data-ttu-id="91c81-118">如需詳細資訊，請參閱 [廣告以較高的許可權安裝的 Per-User 應用程式](advertising-a-per-user-application-to-be-installed-with-elevated-privileges.md)。</span><span class="sxs-lookup"><span data-stu-id="91c81-118">For more information, see [Advertising a Per-User Application To Be Installed with Elevated Privileges](advertising-a-per-user-application-to-be-installed-with-elevated-privileges.md).</span></span>
-   <span data-ttu-id="91c81-119">系統管理員可以針對每位使用者和每部電腦的安裝設定 [AlwaysInstallElevated](alwaysinstallelevated.md) 原則。</span><span class="sxs-lookup"><span data-stu-id="91c81-119">An administrator can set the [AlwaysInstallElevated](alwaysinstallelevated.md) policy for both per-user and per-machine installations.</span></span> <span data-ttu-id="91c81-120">這個方法可以開啟電腦的安全性風險，因為當設定此原則時，非系統管理員的使用者可以使用較高的許可權執行安裝，並存取電腦上的安全位置，例如 SystemFolder 或 **HKLM** 登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="91c81-120">This method can open a computer to a security risk, because when this policy is set, a non-administrator user can run installations with elevated privileges and access secure locations on the computer, such as the SystemFolder or the **HKLM** registry key.</span></span>

    <span data-ttu-id="91c81-121">如果在設定 [AlwaysInstallElevated](alwaysinstallelevated.md) 原則的情況下，每一部電腦都已安裝應用程式，則會將產品視為受管理。</span><span class="sxs-lookup"><span data-stu-id="91c81-121">If the application is installed per-machine while the [AlwaysInstallElevated](alwaysinstallelevated.md) policy is set, the product is treated as managed.</span></span> <span data-ttu-id="91c81-122">在此情況下，如果移除原則，應用程式仍然可以使用較高的許可權來執行修復。</span><span class="sxs-lookup"><span data-stu-id="91c81-122">In this case, the application can still perform a repair with elevated privileges if the policy is removed.</span></span> <span data-ttu-id="91c81-123">此外，如果在設定 AlwaysInstallElevated 原則的情況下，每位使用者都安裝應用程式，則應用程式在移除原則時將無法執行修復。</span><span class="sxs-lookup"><span data-stu-id="91c81-123">Also, if the application is installed per-user while the AlwaysInstallElevated policy is set, the application is unable to perform a repair if the policy is removed.</span></span>

-   <span data-ttu-id="91c81-124">系統管理員可以移至使用者的電腦，並執行應用程式的每一電腦安裝。</span><span class="sxs-lookup"><span data-stu-id="91c81-124">An administrator can go to a user's computer and do a per-machine installation of the application.</span></span> <span data-ttu-id="91c81-125">由於需要許可權才能執行這種類型的安裝，因此一律會管理每部電腦安裝。</span><span class="sxs-lookup"><span data-stu-id="91c81-125">Because privileges are required to perform this type of installation, per-machine installations are always managed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="91c81-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="91c81-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="91c81-127">安裝內容</span><span class="sxs-lookup"><span data-stu-id="91c81-127">Installation Context</span></span>](installation-context.md)
</dt> </dl>

 

 

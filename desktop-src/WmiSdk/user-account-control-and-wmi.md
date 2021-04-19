---
description: " (UAC) 的使用者帳戶控制會影響命令列工具所傳回的 WMI 資料、遠端存取，以及腳本必須如何執行。 如需 UAC 的詳細資訊，請參閱使用使用者帳戶控制開始使用。"
ms.assetid: f6840aaa-834b-42c8-b641-01c570078fcb
ms.tgt_platform: multiple
title: 使用者帳戶控制和 WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 39d48abcffa537d886397092c6d4a7b558825021
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984990"
---
# <a name="user-account-control-and-wmi"></a><span data-ttu-id="0ccf1-104">使用者帳戶控制和 WMI</span><span class="sxs-lookup"><span data-stu-id="0ccf1-104">User Account Control and WMI</span></span>

<span data-ttu-id="0ccf1-105"> (UAC) 的使用者帳戶控制會影響命令列工具所傳回的 WMI 資料、遠端存取，以及腳本必須如何執行。</span><span class="sxs-lookup"><span data-stu-id="0ccf1-105">User Account Control (UAC) affects the WMI data that is returned from a command-line tool, remote access, and how scripts must run.</span></span> <span data-ttu-id="0ccf1-106">如需 UAC 的詳細資訊，請參閱 [使用使用者帳戶控制開始使用](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista)。</span><span class="sxs-lookup"><span data-stu-id="0ccf1-106">For more information about UAC, see [Getting Started with User Account Control](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista).</span></span>

<span data-ttu-id="0ccf1-107">下列各節說明 UAC 功能：</span><span class="sxs-lookup"><span data-stu-id="0ccf1-107">The following sections describe UAC functionality:</span></span>

-   [<span data-ttu-id="0ccf1-108">使用者帳戶控制</span><span class="sxs-lookup"><span data-stu-id="0ccf1-108">User Account Control</span></span>](#user-account-control-and-wmi)
-   [<span data-ttu-id="0ccf1-109">執行 WMI Command-Line 工具所需的帳戶</span><span class="sxs-lookup"><span data-stu-id="0ccf1-109">Account Needed to Run WMI Command-Line Tools</span></span>](#account-needed-to-run-wmi-command-line-tools)
-   [<span data-ttu-id="0ccf1-110">處理 UAC 下的遠端連線</span><span class="sxs-lookup"><span data-stu-id="0ccf1-110">Handling Remote Connections Under UAC</span></span>](#handling-remote-connections-under-uac)
-   [<span data-ttu-id="0ccf1-111">UAC 對傳回給腳本或應用程式的 WMI 資料有何影響</span><span class="sxs-lookup"><span data-stu-id="0ccf1-111">UAC Effect on WMI Data Returned to Scripts or Applications</span></span>](#uac-effect-on-wmi-data-returned-to-scripts-or-applications)
-   [<span data-ttu-id="0ccf1-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="0ccf1-112">Related topics</span></span>](#related-topics)

## <a name="user-account-control"></a><span data-ttu-id="0ccf1-113">使用者帳戶控制</span><span class="sxs-lookup"><span data-stu-id="0ccf1-113">User Account Control</span></span>

<span data-ttu-id="0ccf1-114">在 UAC 下，本機 Administrators 群組中的帳戶有兩個 [*存取權杖*](/windows/desktop/SecGloss/a-gly)，一個具有標準使用者權限，另一個具有系統管理員許可權。</span><span class="sxs-lookup"><span data-stu-id="0ccf1-114">Under UAC, accounts in the local Administrators group have two [*access tokens*](/windows/desktop/SecGloss/a-gly), one with standard user privileges and one with administrator privileges.</span></span> <span data-ttu-id="0ccf1-115">由於 UAC 存取權杖篩選，腳本通常會在標準使用者 token 下執行，除非它在更高的許可權模式下以系統管理員身分執行。</span><span class="sxs-lookup"><span data-stu-id="0ccf1-115">Because of UAC access token filtering, a script is normally run under the standard user token, unless it is run "as an Administrator" in elevated privilege mode.</span></span> <span data-ttu-id="0ccf1-116">並非所有腳本都需要系統管理許可權。</span><span class="sxs-lookup"><span data-stu-id="0ccf1-116">Not all scripts required administrative privileges.</span></span>

<span data-ttu-id="0ccf1-117">腳本無法以程式設計方式判斷它們是以標準使用者安全性權杖還是系統管理員權杖來執行。</span><span class="sxs-lookup"><span data-stu-id="0ccf1-117">Scripts cannot determine programmatically whether they are running under a standard user security token or an Administrator token.</span></span> <span data-ttu-id="0ccf1-118">腳本可能會因為拒絕存取錯誤而失敗。</span><span class="sxs-lookup"><span data-stu-id="0ccf1-118">The script may fail with an access denied error.</span></span> <span data-ttu-id="0ccf1-119">如果腳本需要系統管理員許可權，則必須在提高許可權的模式下執行。</span><span class="sxs-lookup"><span data-stu-id="0ccf1-119">If the script requires administrator privileges, then it must be run in the elevated mode.</span></span> <span data-ttu-id="0ccf1-120">WMI 命名空間的存取權會因腳本是否在提高許可權的模式中執行而有所不同。</span><span class="sxs-lookup"><span data-stu-id="0ccf1-120">Access to WMI namespaces differs depending on whether the script is run in elevated mode.</span></span> <span data-ttu-id="0ccf1-121">某些 WMI 作業（例如取得資料或執行大部分的方法）不需要以系統管理員身分執行該帳戶。</span><span class="sxs-lookup"><span data-stu-id="0ccf1-121">Some WMI operations, such as getting data or executing most methods, do not require that the account run as an administrator.</span></span> <span data-ttu-id="0ccf1-122">如需預設存取權限的詳細資訊，請參閱 [存取 WMI 命名空間](access-to-wmi-namespaces.md) 和執行特殊許可權 [作業](executing-privileged-operations.md)。</span><span class="sxs-lookup"><span data-stu-id="0ccf1-122">For more information about default access permissions, see [Access to WMI Namespaces](access-to-wmi-namespaces.md) and [Executing Privileged Operations](executing-privileged-operations.md).</span></span>

<span data-ttu-id="0ccf1-123">由於使用者帳戶控制，執行腳本的帳戶必須在本機電腦的 Administrators 群組中，才能以較高的許可權執行。</span><span class="sxs-lookup"><span data-stu-id="0ccf1-123">Because of User Account Control, the account running the script must be in the Administrators group on the local computer to have the ability to run with elevated rights.</span></span>

<span data-ttu-id="0ccf1-124">您可以藉由執行下列其中一種方法，以較高的許可權執行腳本或應用程式：</span><span class="sxs-lookup"><span data-stu-id="0ccf1-124">You can run a script or an application with elevated rights by performing one of the following methods:</span></span>

<span data-ttu-id="0ccf1-125">**在提高許可權的模式中執行腳本**</span><span class="sxs-lookup"><span data-stu-id="0ccf1-125">**To Run a Script In Elevated Mode**</span></span>

1.  <span data-ttu-id="0ccf1-126">以滑鼠右鍵按一下 [開始] 功能表中的 [命令提示字元]，然後按一下 [以 **系統管理員身分執行**]，開啟 [命令提示字元] 視窗。</span><span class="sxs-lookup"><span data-stu-id="0ccf1-126">Open a Command Prompt window by right-clicking Command Prompt in the Start menu and then clicking **Run as administrator**.</span></span>
2.  <span data-ttu-id="0ccf1-127">使用工作排程器將腳本排程為提高許可權執行。</span><span class="sxs-lookup"><span data-stu-id="0ccf1-127">Schedule the script to run elevated using Task Scheduler.</span></span> <span data-ttu-id="0ccf1-128">如需詳細資訊，請參閱 [執行工作的安全性](/windows/desktop/TaskSchd/security-contexts-for-running-tasks)內容。</span><span class="sxs-lookup"><span data-stu-id="0ccf1-128">For more information, see [Security Contexts for Running Tasks](/windows/desktop/TaskSchd/security-contexts-for-running-tasks).</span></span>
3.  <span data-ttu-id="0ccf1-129">使用內建的系統管理員帳戶來執行腳本。</span><span class="sxs-lookup"><span data-stu-id="0ccf1-129">Run the script using the built-in Administrator account.</span></span>

## <a name="account-needed-to-run-wmi-command-line-tools"></a><span data-ttu-id="0ccf1-130">執行 WMI Command-Line 工具所需的帳戶</span><span class="sxs-lookup"><span data-stu-id="0ccf1-130">Account Needed to Run WMI Command-Line Tools</span></span>

<span data-ttu-id="0ccf1-131">若要執行下列 [WMI Command-Line 工具](wmi-command-line-tools.md)，您的帳戶必須在 Administrators 群組中，而且必須從提升許可權的命令提示字元執行此工具。</span><span class="sxs-lookup"><span data-stu-id="0ccf1-131">To run the following [WMI Command-Line Tools](wmi-command-line-tools.md), your account must be in the Administrators group and the tool must be run from an elevated command prompt.</span></span> <span data-ttu-id="0ccf1-132">內建的系統管理員帳戶也可以執行這些工具。</span><span class="sxs-lookup"><span data-stu-id="0ccf1-132">The built-in administrator account can also run these tools.</span></span>

-   [<span data-ttu-id="0ccf1-133">**mofcomp.exe**</span><span class="sxs-lookup"><span data-stu-id="0ccf1-133">**mofcomp**</span></span>](mofcomp.md)

-   [<span data-ttu-id="0ccf1-134">**wmic**</span><span class="sxs-lookup"><span data-stu-id="0ccf1-134">**wmic**</span></span>](wmic.md)

    <span data-ttu-id="0ccf1-135">當您第一次在系統安裝之後執行 Wmic 時，必須從已提升許可權的命令提示字元執行。</span><span class="sxs-lookup"><span data-stu-id="0ccf1-135">The first time you run Wmic after system installation, it must be run from an elevated command prompt.</span></span> <span data-ttu-id="0ccf1-136">除非 WMI 作業需要系統管理員許可權，否則，後續執行的 Wmic 可能不需要提高許可權模式。</span><span class="sxs-lookup"><span data-stu-id="0ccf1-136">The elevated mode may not be required for subsequent executions of Wmic unless the WMI operations require administrator privilege.</span></span>

-   [<span data-ttu-id="0ccf1-137">**winmgmt**</span><span class="sxs-lookup"><span data-stu-id="0ccf1-137">**winmgmt**</span></span>](winmgmt.md)

-   [<span data-ttu-id="0ccf1-138">**wmiadap**</span><span class="sxs-lookup"><span data-stu-id="0ccf1-138">**wmiadap**</span></span>](wmiadap.md)

<span data-ttu-id="0ccf1-139">若要 (Wmimgmt.msc) 執行 [*Wmi 控制項*](gloss-w.md) ，並變更 wmi 命名空間安全性或審核設定，您的帳戶必須明確授與或在本機 Administrators 群組中的編輯安全性許可權。</span><span class="sxs-lookup"><span data-stu-id="0ccf1-139">To run the [*WMI Control*](gloss-w.md) (Wmimgmt.msc) and make changes to WMI namespace security or auditing settings, your account must have the Edit Security right explicitly granted or be in the local Administrators group.</span></span> <span data-ttu-id="0ccf1-140">內建的系統管理員帳戶也可以變更命名空間的安全性或審核。</span><span class="sxs-lookup"><span data-stu-id="0ccf1-140">The built-in Administrator account can also change the security or auditing for a namespace.</span></span>

<span data-ttu-id="0ccf1-141">Wbemtest.exe，Microsoft 客戶支援服務不支援的命令列工具，可以由不在本機 Administrators 群組中的帳戶執行，除非特定的作業需要通常授與系統管理員帳戶的許可權。</span><span class="sxs-lookup"><span data-stu-id="0ccf1-141">Wbemtest.exe, a command-line tool that is not supported by Microsoft Customer Support services, can be run by accounts that are not in the local Administrators group, unless a specific operation requires privileges that are normally granted to Administrator accounts.</span></span>

## <a name="handling-remote-connections-under-uac"></a><span data-ttu-id="0ccf1-142">處理 UAC 下的遠端連線</span><span class="sxs-lookup"><span data-stu-id="0ccf1-142">Handling Remote Connections Under UAC</span></span>

<span data-ttu-id="0ccf1-143">無論您是連接到網域中或工作組中的遠端電腦，都會決定是否發生 UAC 篩選。</span><span class="sxs-lookup"><span data-stu-id="0ccf1-143">Whether you are connecting to a remote computer in a domain or in a workgroup determines whether UAC filtering occurs.</span></span>

<span data-ttu-id="0ccf1-144">如果您的電腦是網域的一部分，請使用遠端電腦的本機 Administrators 群組中的網域帳戶來連接到目的電腦。</span><span class="sxs-lookup"><span data-stu-id="0ccf1-144">If your computer is part of a domain, connect to the target computer using a domain account that is in the local Administrators group of the remote computer.</span></span> <span data-ttu-id="0ccf1-145">然後 UAC 存取權杖篩選不會影響本機 Administrators 群組中的網域帳戶。</span><span class="sxs-lookup"><span data-stu-id="0ccf1-145">Then UAC access token filtering will not affect the domain accounts in the local Administrators group.</span></span> <span data-ttu-id="0ccf1-146">請勿在遠端電腦上使用本機的非網域帳戶，即使帳戶是在 Administrators 群組中也一樣。</span><span class="sxs-lookup"><span data-stu-id="0ccf1-146">Do not use a local, nondomain account on the remote computer, even if the account is in the Administrators group.</span></span>

<span data-ttu-id="0ccf1-147">在工作組中，連接至遠端電腦的帳戶是該電腦上的本機使用者。</span><span class="sxs-lookup"><span data-stu-id="0ccf1-147">In a workgroup, the account connecting to the remote computer is a local user on that computer.</span></span> <span data-ttu-id="0ccf1-148">即使帳戶是在 Administrators 群組中，UAC 篩選也表示腳本會以標準使用者的身分執行。</span><span class="sxs-lookup"><span data-stu-id="0ccf1-148">Even if the account is in the Administrators group, UAC filtering means that a script runs as a standard user.</span></span> <span data-ttu-id="0ccf1-149">最佳做法是在目的電腦上建立專用的本機使用者群組或使用者帳戶，特別是用於遠端連線。</span><span class="sxs-lookup"><span data-stu-id="0ccf1-149">A best practice is to create a dedicated local user group or user account on the target computer specifically for remote connections.</span></span>

<span data-ttu-id="0ccf1-150">因為帳戶從未具有系統管理許可權，所以必須調整安全性才能使用此帳戶。</span><span class="sxs-lookup"><span data-stu-id="0ccf1-150">The security must be adjusted to be able to use this account because the account never has had administrative privileges.</span></span> <span data-ttu-id="0ccf1-151">授與本機使用者：</span><span class="sxs-lookup"><span data-stu-id="0ccf1-151">Give the local user:</span></span>

-   <span data-ttu-id="0ccf1-152">遠端啟動和啟動存取 DCOM 的許可權。</span><span class="sxs-lookup"><span data-stu-id="0ccf1-152">Remote launch and activate rights to access DCOM.</span></span> <span data-ttu-id="0ccf1-153">如需詳細資訊，請參閱 [連接到遠端電腦上的 WMI](connecting-to-wmi-on-a-remote-computer.md)。</span><span class="sxs-lookup"><span data-stu-id="0ccf1-153">For more information, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>
-   <span data-ttu-id="0ccf1-154">從遠端存取 WMI 命名空間 (遠端啟用) 的許可權。</span><span class="sxs-lookup"><span data-stu-id="0ccf1-154">Rights to access the WMI namespace remotely (Remote Enable).</span></span> <span data-ttu-id="0ccf1-155">如需詳細資訊，請參閱 [WMI 命名空間的存取](access-to-wmi-namespaces.md)。</span><span class="sxs-lookup"><span data-stu-id="0ccf1-155">For more information, see [Access to WMI Namespaces](access-to-wmi-namespaces.md).</span></span>
-   <span data-ttu-id="0ccf1-156">存取特定安全物件的許可權，視物件所需的安全性而定。</span><span class="sxs-lookup"><span data-stu-id="0ccf1-156">Right to access the specific securable object, depending on the security required by the object.</span></span>

<span data-ttu-id="0ccf1-157">如果您使用本機帳戶，可能是因為您是在工作組中，或是本機電腦帳戶，則可能會強制將特定工作提供給本機使用者。</span><span class="sxs-lookup"><span data-stu-id="0ccf1-157">If you use a local account, either because you are in a workgroup or it is a local computer account, you may be forced to give specific tasks to a local user.</span></span> <span data-ttu-id="0ccf1-158">例如，您可以授與使用者透過 SC.exe 命令、 [**Win32 \_ 服務**](/windows/desktop/CIMWin32Prov/win32-service)的 [**GetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/getsecuritydescriptor-method-in-class-win32-service)和 [**SetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/setsecuritydescriptor-method-in-class-win32-service)方法，或透過使用 gpedit.msc 的群組原則來停止或啟動特定服務的許可權。</span><span class="sxs-lookup"><span data-stu-id="0ccf1-158">For example, you can grant the user the right to stop or start a specific service through the SC.exe command, the [**GetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/getsecuritydescriptor-method-in-class-win32-service) and [**SetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/setsecuritydescriptor-method-in-class-win32-service) methods of [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service), or through Group Policy using Gpedit.msc.</span></span> <span data-ttu-id="0ccf1-159">某些安全物件可能不允許標準使用者執行工作，也不能提供改變預設安全性的方法。</span><span class="sxs-lookup"><span data-stu-id="0ccf1-159">Some securable objects may not allow a standard user to perform tasks and offer no means to alter the default security.</span></span> <span data-ttu-id="0ccf1-160">在此情況下，您可能需要停用 UAC，讓本機使用者帳戶不會經過篩選，而是會成為完整的系統管理員。</span><span class="sxs-lookup"><span data-stu-id="0ccf1-160">In this case, you may need to disable UAC so that the local user account is not filtered and instead becomes a full administrator.</span></span> <span data-ttu-id="0ccf1-161">請注意，基於安全性理由，停用 UAC 應該是最後的手段。</span><span class="sxs-lookup"><span data-stu-id="0ccf1-161">Be aware that for security reasons, disabling UAC should be a last resort.</span></span>

<span data-ttu-id="0ccf1-162">不建議藉由變更控制遠端 UAC 的登錄專案來停用遠端 UAC，但在工作組中可能是必要的。</span><span class="sxs-lookup"><span data-stu-id="0ccf1-162">Disabling Remote UAC by changing the registry entry that controls Remote UAC is not recommended, but may be necessary in a workgroup.</span></span> <span data-ttu-id="0ccf1-163">登錄專案是 **HKEY \_ 本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **原則** \\ **系統** \\ **LocalAccountTokenFilterPolicy**。</span><span class="sxs-lookup"><span data-stu-id="0ccf1-163">The registry entry is **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**Policies**\\**system**\\**LocalAccountTokenFilterPolicy**.</span></span> <span data-ttu-id="0ccf1-164">當這個專案的值為零 (0) 時，會啟用遠端 UAC 存取權杖篩選。</span><span class="sxs-lookup"><span data-stu-id="0ccf1-164">When the value of this entry is zero (0), Remote UAC access token filtering is enabled.</span></span> <span data-ttu-id="0ccf1-165">當值為1時，會停用遠端 UAC。</span><span class="sxs-lookup"><span data-stu-id="0ccf1-165">When the value is 1, remote UAC is disabled.</span></span>

## <a name="uac-effect-on-wmi-data-returned-to-scripts-or-applications"></a><span data-ttu-id="0ccf1-166">UAC 對傳回給腳本或應用程式的 WMI 資料有何影響</span><span class="sxs-lookup"><span data-stu-id="0ccf1-166">UAC Effect on WMI Data Returned to Scripts or Applications</span></span>

<span data-ttu-id="0ccf1-167">如果腳本或應用程式是在 Administrators 群組中的帳戶下執行，但未以較高的許可權執行，則您可能無法取得傳回的所有資料，因為此帳戶是以標準使用者身分執行。</span><span class="sxs-lookup"><span data-stu-id="0ccf1-167">If a script or application is running under an account in the Administrators group, but not running with an elevated privilege, then you may not get all the data returned because this account is running as a standard user.</span></span> <span data-ttu-id="0ccf1-168">某些類別的 WMI [*提供者*](gloss-p.md) 不會將所有實例都傳回給標準使用者帳戶，或由於 UAC 篩選而未以完整系統管理員身分執行的系統管理員帳戶。</span><span class="sxs-lookup"><span data-stu-id="0ccf1-168">The WMI [*providers*](gloss-p.md) for some classes do not return all instances to a standard user account or an Administrator account that is not running as a full administrator because of UAC filtering.</span></span>

<span data-ttu-id="0ccf1-169">當 UAC 篩選帳戶時，下列類別不會傳回某些實例：</span><span class="sxs-lookup"><span data-stu-id="0ccf1-169">The following classes do not return some instances when the account is filtered by UAC:</span></span>

-   [<span data-ttu-id="0ccf1-170">**Win32 \_ 匯流排**</span><span class="sxs-lookup"><span data-stu-id="0ccf1-170">**Win32\_Bus**</span></span>](/windows/desktop/CIMWin32Prov/win32-bus)
-   [<span data-ttu-id="0ccf1-171">**Win32 \_ 印表機**</span><span class="sxs-lookup"><span data-stu-id="0ccf1-171">**Win32\_Printer**</span></span>](/windows/desktop/CIMWin32Prov/win32-printer)
-   [<span data-ttu-id="0ccf1-172">**Win32 \_ ComponentCategory**</span><span class="sxs-lookup"><span data-stu-id="0ccf1-172">**Win32\_ComponentCategory**</span></span>](/windows/desktop/CIMWin32Prov/win32-componentcategory)
-   [<span data-ttu-id="0ccf1-173">**Win32 \_ LogicalProgramGroupItem**</span><span class="sxs-lookup"><span data-stu-id="0ccf1-173">**Win32\_LogicalProgramGroupItem**</span></span>](/windows/desktop/CIMWin32Prov/win32-logicalprogramgroupitem)
-   [<span data-ttu-id="0ccf1-174">**Win32 \_ LogicalProgramGroup**</span><span class="sxs-lookup"><span data-stu-id="0ccf1-174">**Win32\_LogicalProgramGroup**</span></span>](/windows/desktop/CIMWin32Prov/win32-logicalprogramgroup)
-   [<span data-ttu-id="0ccf1-175">**Win32 \_ NetworkConnection**</span><span class="sxs-lookup"><span data-stu-id="0ccf1-175">**Win32\_NetworkConnection**</span></span>](/windows/desktop/CIMWin32Prov/win32-networkconnection)
-   [<span data-ttu-id="0ccf1-176">**Win32 \_ UserAccount**</span><span class="sxs-lookup"><span data-stu-id="0ccf1-176">**Win32\_UserAccount**</span></span>](/windows/desktop/CIMWin32Prov/win32-useraccount)
-   [<span data-ttu-id="0ccf1-177">**Win32 \_ PrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="0ccf1-177">**Win32\_PrinterDriver**</span></span>](/windows/desktop/CIMWin32Prov/win32-printerdriver)
-   [<span data-ttu-id="0ccf1-178">**Win32 \_ PortResource**</span><span class="sxs-lookup"><span data-stu-id="0ccf1-178">**Win32\_PortResource**</span></span>](/windows/desktop/CIMWin32Prov/win32-portresource)
-   [<span data-ttu-id="0ccf1-179">**Win32 \_ DeviceMemoryAddress**</span><span class="sxs-lookup"><span data-stu-id="0ccf1-179">**Win32\_DeviceMemoryAddress**</span></span>](/windows/desktop/CIMWin32Prov/win32-devicememoryaddress)

<span data-ttu-id="0ccf1-180">當 UAC 篩選帳戶時，下列類別不會傳回某些屬性：</span><span class="sxs-lookup"><span data-stu-id="0ccf1-180">The following classes do not return some properties when the account is filtered by UAC:</span></span>

-   [<span data-ttu-id="0ccf1-181">**Win32 \_ >networkadapterconfiguration**</span><span class="sxs-lookup"><span data-stu-id="0ccf1-181">**Win32\_NetworkAdapterConfiguration**</span></span>](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration)
-   [<span data-ttu-id="0ccf1-182">**Win32 \_ DCOMApplicationSetting**</span><span class="sxs-lookup"><span data-stu-id="0ccf1-182">**Win32\_DCOMApplicationSetting**</span></span>](/windows/desktop/CIMWin32Prov/win32-dcomapplicationsetting)
-   [<span data-ttu-id="0ccf1-183">**Win32 \_ DCOMApplication**</span><span class="sxs-lookup"><span data-stu-id="0ccf1-183">**Win32\_DCOMApplication**</span></span>](/windows/desktop/CIMWin32Prov/win32-dcomapplication)
-   [<span data-ttu-id="0ccf1-184">**Win32 \_ 基礎板**</span><span class="sxs-lookup"><span data-stu-id="0ccf1-184">**Win32\_Baseboard**</span></span>](/windows/desktop/CIMWin32Prov/win32-baseboard)
-   [<span data-ttu-id="0ccf1-185">**Win32 \_ 未進行**</span><span class="sxs-lookup"><span data-stu-id="0ccf1-185">**Win32\_ComputerSystem**</span></span>](/windows/desktop/CIMWin32Prov/win32-computersystem)
-   [<span data-ttu-id="0ccf1-186">**Win32 \_ NetworkAdapter**</span><span class="sxs-lookup"><span data-stu-id="0ccf1-186">**Win32\_NetworkAdapter**</span></span>](/windows/desktop/CIMWin32Prov/win32-networkadapter)
-   [<span data-ttu-id="0ccf1-187">**Win32 \_ MotherboardDevice**</span><span class="sxs-lookup"><span data-stu-id="0ccf1-187">**Win32\_MotherboardDevice**</span></span>](/windows/desktop/CIMWin32Prov/win32-motherboarddevice)
-   [<span data-ttu-id="0ccf1-188">**Win32 \_ DiskDrive**</span><span class="sxs-lookup"><span data-stu-id="0ccf1-188">**Win32\_DiskDrive**</span></span>](/windows/desktop/CIMWin32Prov/win32-diskdrive)
-   [<span data-ttu-id="0ccf1-189">**Win32 \_ PnPEntity**</span><span class="sxs-lookup"><span data-stu-id="0ccf1-189">**Win32\_PnPEntity**</span></span>](/windows/desktop/CIMWin32Prov/win32-pnpentity)
-   [<span data-ttu-id="0ccf1-190">**Win32 \_ VideoController**</span><span class="sxs-lookup"><span data-stu-id="0ccf1-190">**Win32\_VideoController**</span></span>](/windows/desktop/CIMWin32Prov/win32-videocontroller)
-   [<span data-ttu-id="0ccf1-191">**Win32 \_ ParallelPort**</span><span class="sxs-lookup"><span data-stu-id="0ccf1-191">**Win32\_ParallelPort**</span></span>](/windows/desktop/CIMWin32Prov/win32-parallelport)
-   [<span data-ttu-id="0ccf1-192">**Win32 \_ LogicalDisk**</span><span class="sxs-lookup"><span data-stu-id="0ccf1-192">**Win32\_LogicalDisk**</span></span>](/windows/desktop/CIMWin32Prov/win32-logicaldisk)
-   [<span data-ttu-id="0ccf1-193">**Win32 \_ >systemdriver**</span><span class="sxs-lookup"><span data-stu-id="0ccf1-193">**Win32\_SystemDriver**</span></span>](/windows/desktop/CIMWin32Prov/win32-systemdriver)
-   [<span data-ttu-id="0ccf1-194">**Win32 \_ IRQResource**</span><span class="sxs-lookup"><span data-stu-id="0ccf1-194">**Win32\_IRQResource**</span></span>](/windows/desktop/CIMWin32Prov/win32-irqresource)
-   [<span data-ttu-id="0ccf1-195">**Win32 \_ NetworkProtocol**</span><span class="sxs-lookup"><span data-stu-id="0ccf1-195">**Win32\_NetworkProtocol**</span></span>](/windows/desktop/CIMWin32Prov/win32-networkprotocol)

## <a name="related-topics"></a><span data-ttu-id="0ccf1-196">相關主題</span><span class="sxs-lookup"><span data-stu-id="0ccf1-196">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0ccf1-197">關於 WMI</span><span class="sxs-lookup"><span data-stu-id="0ccf1-197">About WMI</span></span>](about-wmi.md)
</dt> <dt>

[<span data-ttu-id="0ccf1-198">存取 WMI 安全物件</span><span class="sxs-lookup"><span data-stu-id="0ccf1-198">Access to WMI Securable Objects</span></span>](access-to-wmi-securable-objects.md)
</dt> <dt>

[<span data-ttu-id="0ccf1-199">變更安全物件的存取安全性</span><span class="sxs-lookup"><span data-stu-id="0ccf1-199">Changing Access Security on Securable Objects</span></span>](changing-access-security-on-securable-objects.md)
</dt> </dl>

 

 

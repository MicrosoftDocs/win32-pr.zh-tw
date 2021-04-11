---
description: 您可以撰寫 [MsiRMFilesInUse] 對話方塊，以顯示目前執行的檔案必須由安裝覆寫或刪除的進程清單。
ms.assetid: e8d93310-388e-4a08-9bce-04c31c33a665
title: MsiRMFilesInUse 對話方塊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72bba73cab51f4b3d8321b15001dbb72c638176b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945257"
---
# <a name="msirmfilesinuse-dialog"></a><span data-ttu-id="894d5-103">MsiRMFilesInUse 對話方塊</span><span class="sxs-lookup"><span data-stu-id="894d5-103">MsiRMFilesInUse Dialog</span></span>

<span data-ttu-id="894d5-104">您可以撰寫 [MsiRMFilesInUse] 對話方塊，以顯示目前執行的檔案必須由安裝覆寫或刪除的進程清單。</span><span class="sxs-lookup"><span data-stu-id="894d5-104">The MsiRMFilesInUse Dialog box can be authored to display a list of processes that are currently running files that need to be overwritten or deleted by the installation.</span></span> <span data-ttu-id="894d5-105">使用者可以選取 [自動關閉應用程式並重新啟動應用程式] 或 [不要關閉應用程式] 選項。</span><span class="sxs-lookup"><span data-stu-id="894d5-105">The user can select between options to "Automatically close applications and restart them" or "Do not close applications.</span></span> <span data-ttu-id="894d5-106"> (將需要重新開機。 ) 」如果使用者選取 [自動關閉應用程式並重新啟動應用程式] 選項，就可以撰寫此對話方塊上的 [推送] 按鈕控制項來發佈 RMShutdownAndRestart 控制項事件，然後 [重新開機管理員](../rstmgr/restart-manager-portal.md) 可以關閉應用程式，並在安裝結束時重新開機應用程式。</span><span class="sxs-lookup"><span data-stu-id="894d5-106">(A reboot will be required.)" If the user selects the "Automatically close applications and restart them" option, a push button control on this dialog box can be authored to publish the RMShutdownAndRestart control event and the [Restart Manager](../rstmgr/restart-manager-portal.md) can close the applications and restart them at the end of the installation.</span></span> <span data-ttu-id="894d5-107">這可以消除或減少重新開機電腦的需求。</span><span class="sxs-lookup"><span data-stu-id="894d5-107">This can eliminate or reduce the need to restart the computer.</span></span> <span data-ttu-id="894d5-108">如需詳細資訊，請參閱 [系統重新開機](system-reboots.md)。</span><span class="sxs-lookup"><span data-stu-id="894d5-108">For more information, see [System Reboots](system-reboots.md).</span></span>

<span data-ttu-id="894d5-109">只有在下列所有條件都成立時，才會在安裝期間顯示 [ **MsiRMFilesInUse** ] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="894d5-109">The **MsiRMFilesInUse** dialog box is displayed during an installation only if all the following are true.</span></span> <span data-ttu-id="894d5-110">當這些是 false 時，Windows Installer 會忽略 [ **MsiRMFilesInUse** ] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="894d5-110">When any of these are false, the Windows Installer ignores the **MsiRMFilesInUse** dialog box.</span></span>

-   <span data-ttu-id="894d5-111">不早于4.0 版的 Windows Installer 版本，以及早于 Windows Vista 或 Windows Server 2008 的作業系統正在執行安裝。</span><span class="sxs-lookup"><span data-stu-id="894d5-111">A Windows Installer version that is not earlier than version 4.0 and an operating system that is not earlier than Windows Vista or Windows Server 2008 is running the installation.</span></span>
-   <span data-ttu-id="894d5-112">使用完整的 UI [使用者介面層級](user-interface-levels.md) 。</span><span class="sxs-lookup"><span data-stu-id="894d5-112">The Full UI [user interface level](user-interface-levels.md) is used.</span></span>
-   <span data-ttu-id="894d5-113">[**MSIRESTARTMANAGERCONTROL**](msirestartmanagercontrol.md)屬性或 [DisableAutomaticApplicationShutdown](disableautomaticapplicationshutdown.md)原則尚未停用與 [重新開機管理員](../rstmgr/restart-manager-portal.md)的互動。</span><span class="sxs-lookup"><span data-stu-id="894d5-113">Interactions with the [Restart Manager](../rstmgr/restart-manager-portal.md) have not been disabled by the [**MSIRESTARTMANAGERCONTROL**](msirestartmanagercontrol.md) property or the [DisableAutomaticApplicationShutdown](disableautomaticapplicationshutdown.md) policy.</span></span>
-   <span data-ttu-id="894d5-114">[ **MsiRMFilesInUse** ] 對話方塊存在於安裝套件中。</span><span class="sxs-lookup"><span data-stu-id="894d5-114">The **MsiRMFilesInUse** dialog box is present in the installation package.</span></span>
-   <span data-ttu-id="894d5-115">從 Windows Installer 到 [重新開機管理員](../rstmgr/restart-manager-portal.md) 的所有呼叫都會成功。</span><span class="sxs-lookup"><span data-stu-id="894d5-115">All calls from the Windows Installer to the [Restart Manager](../rstmgr/restart-manager-portal.md) are successful.</span></span>

<span data-ttu-id="894d5-116">此對話方塊將會依 [InstallValidate 動作](installvalidate-action.md)的要求建立。</span><span class="sxs-lookup"><span data-stu-id="894d5-116">This dialog box will be created as required by the [InstallValidate action](installvalidate-action.md).</span></span>

 

 

---
description: 通知 Windows Installer 使用重新開機管理員來關閉所有具有檔案使用中的應用程式，並在安裝結束時重新開機這些應用程式。
ms.assetid: bfa19cc8-4cf7-42ed-9e94-acaeca8d707a
title: RmShutdownAndRestart ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc91d1de52f516c0728e8d6469fb8cddc2e50cfb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106982317"
---
# <a name="rmshutdownandrestart-controlevent"></a><span data-ttu-id="6c9d4-103">RmShutdownAndRestart ControlEvent</span><span class="sxs-lookup"><span data-stu-id="6c9d4-103">RmShutdownAndRestart ControlEvent</span></span>

<span data-ttu-id="6c9d4-104">此事件會通知 Windows Installer 使用 [重新開機管理員](../rstmgr/restart-manager-portal.md) 來關閉所有具有檔案使用中的應用程式，並在安裝結束時重新開機這些應用程式。</span><span class="sxs-lookup"><span data-stu-id="6c9d4-104">This event notifies the Windows Installer to use the [Restart Manager](../rstmgr/restart-manager-portal.md) to shutdown all applications that have files in use and to restart them at the end of the installation.</span></span>

<span data-ttu-id="6c9d4-105">如果下列任一條件成立，此 ControlEvent 就沒有任何作用。</span><span class="sxs-lookup"><span data-stu-id="6c9d4-105">This ControlEvent has no effect if any of the following are true.</span></span>

-   <span data-ttu-id="6c9d4-106">執行安裝的作業系統不是 Windows Vista 或 Windows Server 2008。</span><span class="sxs-lookup"><span data-stu-id="6c9d4-106">The operating system running the installation is not Windows Vista or Windows Server 2008.</span></span>
-   <span data-ttu-id="6c9d4-107">[**MSIRESTARTMANAGERCONTROL**](msirestartmanagercontrol.md)屬性或 [DisableAutomaticApplicationShutdown](disableautomaticapplicationshutdown.md)原則已停用與 [重新開機管理員](../rstmgr/restart-manager-portal.md)的互動。</span><span class="sxs-lookup"><span data-stu-id="6c9d4-107">Interactions with the [Restart Manager](../rstmgr/restart-manager-portal.md) have been disabled by the [**MSIRESTARTMANAGERCONTROL**](msirestartmanagercontrol.md) property or the [DisableAutomaticApplicationShutdown](disableautomaticapplicationshutdown.md) policy.</span></span>
-   <span data-ttu-id="6c9d4-108">目前沒有任何開啟的 [重新開機管理員](../rstmgr/restart-manager-portal.md) 會話。</span><span class="sxs-lookup"><span data-stu-id="6c9d4-108">There is currently no open [Restart Manager](../rstmgr/restart-manager-portal.md) session.</span></span>
-   <span data-ttu-id="6c9d4-109">從 Windows Installer 到 [重新開機管理員](../rstmgr/restart-manager-portal.md) 的任何呼叫都會傳回失敗。</span><span class="sxs-lookup"><span data-stu-id="6c9d4-109">Any calls from the Windows Installer to the [Restart Manager](../rstmgr/restart-manager-portal.md) returns a failure.</span></span>

## <a name="typical-use"></a><span data-ttu-id="6c9d4-110">一般用法</span><span class="sxs-lookup"><span data-stu-id="6c9d4-110">Typical Use</span></span>

<span data-ttu-id="6c9d4-111">RMShutdownAndRestart 控制項事件只會透過 [ [MsiRMFilesInUse] 對話方塊](msirmfilesinuse-dialog.md)上的[按鈕](pushbutton-control.md)控制項來發行。</span><span class="sxs-lookup"><span data-stu-id="6c9d4-111">The RMShutdownAndRestart control event is published only by a [PushButton](pushbutton-control.md) control on the [MsiRMFilesInUse Dialog](msirmfilesinuse-dialog.md) box.</span></span>

 

 

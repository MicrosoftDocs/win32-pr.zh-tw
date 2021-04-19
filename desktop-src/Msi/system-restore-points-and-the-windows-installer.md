---
description: 系統還原會自動監視並記錄使用者電腦上的重要系統變更。 如需詳細資訊，請參閱系統還原。
ms.assetid: 5fc345ff-8a47-4372-806f-64b8c271fd2d
title: 系統還原點和 Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7fe9bd4b8e22f5aee7e49d3e4c452378f402e7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107000084"
---
# <a name="system-restore-points-and-the-windows-installer"></a><span data-ttu-id="ce4c3-104">系統還原點和 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="ce4c3-104">System Restore Points and the Windows Installer</span></span>

<span data-ttu-id="ce4c3-105">系統還原會自動監視並記錄使用者電腦上的重要系統變更。</span><span class="sxs-lookup"><span data-stu-id="ce4c3-105">System Restore automatically monitors and records key system changes on a user's computer.</span></span> <span data-ttu-id="ce4c3-106">如需詳細資訊，請參閱 [系統還原](../sr/system-restore-portal.md)。</span><span class="sxs-lookup"><span data-stu-id="ce4c3-106">For more information, see [System Restore](../sr/system-restore-portal.md).</span></span>

<span data-ttu-id="ce4c3-107">系統還原點是由系統建立的，而且也會在安裝或移除軟體時 Windows Installer 建立。</span><span class="sxs-lookup"><span data-stu-id="ce4c3-107">System restore points are created by the system and are also created by Windows Installer when software is installed or removed.</span></span>

<span data-ttu-id="ce4c3-108">在 Windows XP 中，安裝程式可能會在第一次安裝應用程式期間，以及在移除時建立檢查點。</span><span class="sxs-lookup"><span data-stu-id="ce4c3-108">On Windows XP, the installer may create checkpoints during the first installation of an application, and during its removal.</span></span> <span data-ttu-id="ce4c3-109">只有在使用 [*基本 UI*](b-gly.md)執行變更時，安裝程式才會在這些情況下建立檢查點。</span><span class="sxs-lookup"><span data-stu-id="ce4c3-109">The installer only creates checkpoints in these cases when the change is run with at least a [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="ce4c3-110">[使用者介面層級](user-interface-levels.md)設定為 [無] 的安裝通常是由系統或應該處理建立檢查點的應用程式所起始。</span><span class="sxs-lookup"><span data-stu-id="ce4c3-110">Installations having the [user interface level](user-interface-levels.md) set to None are usually initiated by the system or an application that should handle creating a checkpoint.</span></span> <span data-ttu-id="ce4c3-111">如需詳細資訊，請參閱 [系統還原](../sr/system-restore-portal.md)。</span><span class="sxs-lookup"><span data-stu-id="ce4c3-111">For more information, see [System Restore](../sr/system-restore-portal.md).</span></span>

<span data-ttu-id="ce4c3-112">在具有許多小型應用程式的公司中，系統管理員可能會決定停用安裝程式內的檢查點，以改善效能。</span><span class="sxs-lookup"><span data-stu-id="ce4c3-112">In corporations with many small applications, administrators may decide to disable checkpointing from within the installer to improve performance.</span></span> <span data-ttu-id="ce4c3-113">如需詳細資訊，請參閱 [LimitSystemRestoreCheckpointing](limitsystemrestorecheckpointing.md) 或 [設定自訂動作的還原點](setting-a-restore-point-from-a-custom-action.md)。</span><span class="sxs-lookup"><span data-stu-id="ce4c3-113">For more information, see [LimitSystemRestoreCheckpointing](limitsystemrestorecheckpointing.md) or [Setting a Restore Point from a Custom Action](setting-a-restore-point-from-a-custom-action.md).</span></span>

<span data-ttu-id="ce4c3-114">從 Windows Installer 5.0 開始，可以設定 [**MSIFASTINSTALL**](msifastinstall.md) 屬性，以防止安裝產生系統還原點。</span><span class="sxs-lookup"><span data-stu-id="ce4c3-114">Beginning with Windows Installer 5.0, the [**MSIFASTINSTALL**](msifastinstall.md) property can be set to prevent an installation from generating a system restore point.</span></span>

 

 

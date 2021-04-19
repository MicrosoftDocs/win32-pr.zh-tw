---
description: 每一電腦的系統原則會依 Windows Installer 關閉檢查點的建立。
ms.assetid: 706d6c85-3876-4205-b7da-b0fd709e65dd
title: LimitSystemRestoreCheckpointing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7606d266b4e9e42f6287669df9b3ab33a3ad9f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106989916"
---
# <a name="limitsystemrestorecheckpointing"></a><span data-ttu-id="efab8-103">LimitSystemRestoreCheckpointing</span><span class="sxs-lookup"><span data-stu-id="efab8-103">LimitSystemRestoreCheckpointing</span></span>

<span data-ttu-id="efab8-104">每一電腦的 [系統原則](system-policy.md) 會依 Windows Installer 關閉檢查點的建立。</span><span class="sxs-lookup"><span data-stu-id="efab8-104">This per-machine [system policy](system-policy.md) turns off the creation of checkpoints by Windows Installer.</span></span>

<span data-ttu-id="efab8-105">設定為0或不存在，安裝程式會進行安裝或卸載的一般檢查點檢查。</span><span class="sxs-lookup"><span data-stu-id="efab8-105">Set to 0 or absent, the installer does normal checkpointing for install or uninstall.</span></span> <span data-ttu-id="efab8-106">設定為1時，安裝程式不會建立檢查點。</span><span class="sxs-lookup"><span data-stu-id="efab8-106">Set to 1, the installer creates no checkpoints.</span></span>

<span data-ttu-id="efab8-107">此原則只會影響 Windows Installer 所設定的檢查點。</span><span class="sxs-lookup"><span data-stu-id="efab8-107">This policy affects only checkpoints set by Windows Installer.</span></span> <span data-ttu-id="efab8-108">在 Windows XP 電腦上，系統管理員可能會決定停用 Windows Installer 內的檢查點，以改善效能。</span><span class="sxs-lookup"><span data-stu-id="efab8-108">On Windows XP computers, administrators may decide to disable checkpointing from within Windows Installer to improve performance.</span></span> <span data-ttu-id="efab8-109">[**系統還原**](../sr/system-restore-portal.md) 也會建立額外的檢查點。</span><span class="sxs-lookup"><span data-stu-id="efab8-109">[**System Restore**](../sr/system-restore-portal.md) also creates additional checkpoints.</span></span> <span data-ttu-id="efab8-110">如需詳細資訊，請參閱 [系統還原點和 Windows Installer](system-restore-points-and-the-windows-installer.md) ，以及 [設定自訂動作的還原點](setting-a-restore-point-from-a-custom-action.md)。</span><span class="sxs-lookup"><span data-stu-id="efab8-110">For more information, see [System Restore Points and the Windows Installer](system-restore-points-and-the-windows-installer.md) and [Setting a Restore Point from a Custom Action](setting-a-restore-point-from-a-custom-action.md).</span></span>

## <a name="registry-key"></a><span data-ttu-id="efab8-111">登錄金鑰</span><span class="sxs-lookup"><span data-stu-id="efab8-111">Registry Key</span></span>

<span data-ttu-id="efab8-112">在下列登錄機碼底下，設定名為 LimitSystemRestoreCheckpointing 的值。</span><span class="sxs-lookup"><span data-stu-id="efab8-112">Set the value named LimitSystemRestoreCheckpointing under the following registry key.</span></span>

<span data-ttu-id="efab8-113">**HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ 原則 \\ Microsoft \\ Windows \\ Installer**</span><span class="sxs-lookup"><span data-stu-id="efab8-113">**HKEY\_LOCAL\_MACHINE\\Software\\Policies\\Microsoft\\Windows\\Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="efab8-114">資料類型</span><span class="sxs-lookup"><span data-stu-id="efab8-114">Data Type</span></span>

<span data-ttu-id="efab8-115">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="efab8-115">**REG\_DWORD**</span></span>

 

 

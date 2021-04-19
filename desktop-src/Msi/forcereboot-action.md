---
description: ForceReboot 動作會在安裝期間提示使用者重新開機系統。
ms.assetid: e1bcdd59-8cbc-46f7-b908-c8cbc2ea0539
title: ForceReboot 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 807bab474f1faacfbc7684797b7a0b7b74f354d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975162"
---
# <a name="forcereboot-action"></a><span data-ttu-id="40b2c-103">ForceReboot 動作</span><span class="sxs-lookup"><span data-stu-id="40b2c-103">ForceReboot Action</span></span>

<span data-ttu-id="40b2c-104">ForceReboot 動作會在安裝期間提示使用者重新開機系統。</span><span class="sxs-lookup"><span data-stu-id="40b2c-104">The ForceReboot action prompts the user for a restart of the system during the installation.</span></span> <span data-ttu-id="40b2c-105">ForceReboot 動作與 [ScheduleReboot 動作](schedulereboot-action.md) 不同，因為 ScheduleReboot 動作是用來排定在安裝結束時重新開機的提示。</span><span class="sxs-lookup"><span data-stu-id="40b2c-105">The ForceReboot action is different from the [ScheduleReboot action](schedulereboot-action.md) in that the ScheduleReboot action is used to schedule a prompt to restart at the end of the installation.</span></span>

<span data-ttu-id="40b2c-106">如果安裝具有使用者介面，安裝程式會在每個 ForceReboot 動作顯示對話方塊，提示使用者重新開機系統。</span><span class="sxs-lookup"><span data-stu-id="40b2c-106">If the installation has a user interface, the installer displays a dialog box at each ForceReboot action which prompts the user to restart the system.</span></span> <span data-ttu-id="40b2c-107">使用者必須在繼續安裝之前回應此提示。</span><span class="sxs-lookup"><span data-stu-id="40b2c-107">The user must respond to this prompt before continuing with the installation.</span></span> <span data-ttu-id="40b2c-108">如果安裝沒有使用者介面，系統會自動重新開機 ForceReboot 動作。</span><span class="sxs-lookup"><span data-stu-id="40b2c-108">If the installation has no user interface, the system automatically restarts at the ForceReboot action.</span></span>

<span data-ttu-id="40b2c-109">如果安裝程式判斷是否需要重新開機，它會在安裝結束時自動提示使用者重新開機，不論順序中是否有任何 ForceReboot 或 ScheduleReboot 動作。</span><span class="sxs-lookup"><span data-stu-id="40b2c-109">If the installer determines that a restart is necessary, it automatically prompts the user to restart at the end of the installation, whether or not there are any ForceReboot or ScheduleReboot actions in the sequence.</span></span> <span data-ttu-id="40b2c-110">例如，安裝程式會在需要取代安裝期間所使用的任何檔案時，自動提示重新開機。</span><span class="sxs-lookup"><span data-stu-id="40b2c-110">For example, the installer automatically prompts for a restart if it needs to replace any files used during the installation.</span></span>

<span data-ttu-id="40b2c-111">藉由設定 [ [**重新開機**](reboot.md) ] 屬性來抑制特定的重新開機提示。</span><span class="sxs-lookup"><span data-stu-id="40b2c-111">Suppress certain restart prompts by setting the [**REBOOT**](reboot.md) property.</span></span>

<span data-ttu-id="40b2c-112">如果 Windows Installer 在[多套件安裝](multiple-package-installations.md)期間遇到 ForceReboot 或[ScheduleReboot](schedulereboot-action.md)動作，安裝程式將會停止並復原安裝。</span><span class="sxs-lookup"><span data-stu-id="40b2c-112">If the Windows Installer encounters the ForceReboot or [ScheduleReboot](schedulereboot-action.md) action during a [multiple-package installation](multiple-package-installations.md), the installer will stop and roll back the installation.</span></span> <span data-ttu-id="40b2c-113">您可以安裝屬於多套件安裝的其他套件，而這些套件不包含 ForceReboot 或 ScheduleReboot 動作。</span><span class="sxs-lookup"><span data-stu-id="40b2c-113">Other packages belonging to the multiple-package installation, that do not contain a ForceReboot or ScheduleReboot action, can be installed.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="40b2c-114">順序限制</span><span class="sxs-lookup"><span data-stu-id="40b2c-114">Sequence Restrictions</span></span>

<span data-ttu-id="40b2c-115">下列動作通常會一起作為動作順序中的群組。</span><span class="sxs-lookup"><span data-stu-id="40b2c-115">The following actions commonly occur together as a group in the action sequence.</span></span> <span data-ttu-id="40b2c-116">建議您將 ForceReboot 動作排定在此群組之後。</span><span class="sxs-lookup"><span data-stu-id="40b2c-116">It is recommended that the ForceReboot action be scheduled to come after this group.</span></span> <span data-ttu-id="40b2c-117">如果 ForceReboot 動作是在 [RegisterProduct 動作](registerproduct-action.md)之前排程，則安裝程式會在重新開機後再次要求安裝套件的來源。</span><span class="sxs-lookup"><span data-stu-id="40b2c-117">If the ForceReboot action is scheduled before the [RegisterProduct action](registerproduct-action.md), the installer again requires the source of the installation package after the restart.</span></span> <span data-ttu-id="40b2c-118">因此，ForceReboot 的慣用順序會緊接在此動作序列之後。</span><span class="sxs-lookup"><span data-stu-id="40b2c-118">Therefore, the preferred sequence for ForceReboot is immediately following this action sequence.</span></span>

-   [<span data-ttu-id="40b2c-119">RegisterProduct</span><span class="sxs-lookup"><span data-stu-id="40b2c-119">RegisterProduct</span></span>](registerproduct-action.md)
-   [<span data-ttu-id="40b2c-120">RegisterUser</span><span class="sxs-lookup"><span data-stu-id="40b2c-120">RegisterUser</span></span>](registeruser-action.md)
-   [<span data-ttu-id="40b2c-121">PublishProduct</span><span class="sxs-lookup"><span data-stu-id="40b2c-121">PublishProduct</span></span>](publishproduct-action.md)
-   [<span data-ttu-id="40b2c-122">PublishFeatures</span><span class="sxs-lookup"><span data-stu-id="40b2c-122">PublishFeatures</span></span>](publishfeatures-action.md)
-   [<span data-ttu-id="40b2c-123">CreateShortcuts</span><span class="sxs-lookup"><span data-stu-id="40b2c-123">CreateShortcuts</span></span>](createshortcuts-action.md)
-   [<span data-ttu-id="40b2c-124">RegisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="40b2c-124">RegisterMIMEInfo</span></span>](registermimeinfo-action.md)
-   [<span data-ttu-id="40b2c-125">RegisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="40b2c-125">RegisterExtensionInfo</span></span>](registerextensioninfo-action.md)
-   [<span data-ttu-id="40b2c-126">RegisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="40b2c-126">RegisterClassInfo</span></span>](registerclassinfo-action.md)
-   [<span data-ttu-id="40b2c-127">RegisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="40b2c-127">RegisterProgIdInfo</span></span>](registerprogidinfo-action.md)

<span data-ttu-id="40b2c-128">ForceReboot 動作必須位於[InstallExecuteSequence 資料表](installexecutesequence-table.md)的動作順序中的[InstallInitialize](installinitialize-action.md)和[InstallFinalize](installfinalize-action.md)之間。</span><span class="sxs-lookup"><span data-stu-id="40b2c-128">The ForceReboot action must come between [InstallInitialize](installinitialize-action.md) and [InstallFinalize](installfinalize-action.md) in the action sequence of the [InstallExecuteSequence table](installexecutesequence-table.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="40b2c-129">ActionData 訊息</span><span class="sxs-lookup"><span data-stu-id="40b2c-129">ActionData Messages</span></span>

<span data-ttu-id="40b2c-130">沒有任何 ActionData 訊息。</span><span class="sxs-lookup"><span data-stu-id="40b2c-130">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="40b2c-131">備註</span><span class="sxs-lookup"><span data-stu-id="40b2c-131">Remarks</span></span>

<span data-ttu-id="40b2c-132">ForceReboot 動作必須一律搭配條件陳述式使用，讓安裝程式只在必要時才觸發重新開機。</span><span class="sxs-lookup"><span data-stu-id="40b2c-132">The ForceReboot action must always be used with a conditional statement such that the installer triggers a restart only when necessary.</span></span> <span data-ttu-id="40b2c-133">例如，只有在已取代特定檔案或安裝特定元件時，才可能需要重新開機。</span><span class="sxs-lookup"><span data-stu-id="40b2c-133">For example, a restart may only be required if a particular file is replaced or a particular component is installed.</span></span> <span data-ttu-id="40b2c-134">每個產品安裝都是唯一的，而且可能需要進行自訂動作，以判斷是否需要重新開機。</span><span class="sxs-lookup"><span data-stu-id="40b2c-134">Each product installation is unique and a custom action may be required to determine whether a restart is needed.</span></span> <span data-ttu-id="40b2c-135">ForceReboot 動作的條件通常會使用 [**AFTERREBOOT**](afterreboot.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="40b2c-135">The condition on the ForceReboot action commonly makes use of the [**AFTERREBOOT**](afterreboot.md) property.</span></span>

<span data-ttu-id="40b2c-136">ForceReboot 會在提示重新開機或重新開機之前，執行任何先前動作所產生的系統作業。</span><span class="sxs-lookup"><span data-stu-id="40b2c-136">ForceReboot runs system operations generated by any previous actions before prompting for a restart or restarting.</span></span> <span data-ttu-id="40b2c-137">例如， [InstallFiles](installfiles-action.md) 和 [WriteRegistryValues](writeregistryvalues-action.md) 所產生的系統作業會在重新開機之前執行。</span><span class="sxs-lookup"><span data-stu-id="40b2c-137">For example, the system operations generated by [InstallFiles](installfiles-action.md) and [WriteRegistryValues](writeregistryvalues-action.md) are run before a restart.</span></span>

<span data-ttu-id="40b2c-138">ForceReboot 動作會寫入登錄機碼，以便在重新開機後啟動安裝程式。</span><span class="sxs-lookup"><span data-stu-id="40b2c-138">The ForceReboot action writes a registry key that causes the installer to start after restarting.</span></span> <span data-ttu-id="40b2c-139">此機碼的位置是 **HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ Windows \\ CurrentVersion \\ RunOnce**。</span><span class="sxs-lookup"><span data-stu-id="40b2c-139">The location of this key is **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\RunOnce**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="40b2c-140">相關主題</span><span class="sxs-lookup"><span data-stu-id="40b2c-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40b2c-141">系統重新開機</span><span class="sxs-lookup"><span data-stu-id="40b2c-141">System Reboots</span></span>](system-reboots.md)
</dt> </dl>

 

 




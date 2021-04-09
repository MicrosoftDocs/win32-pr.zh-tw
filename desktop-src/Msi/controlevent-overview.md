---
description: 事件事件與 Win32 架構應用程式中的 Microsoft Windows 訊息類似。
ms.assetid: ac62bb94-0605-4145-996a-e91fb1a42a77
title: ControlEvent 總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b92f8662a87bf9040b6a811fc170c25a5cf62ad7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852348"
---
# <a name="controlevent-overview"></a><span data-ttu-id="9041e-103">ControlEvent 總覽</span><span class="sxs-lookup"><span data-stu-id="9041e-103">ControlEvent Overview</span></span>

<span data-ttu-id="9041e-104">事件事件與 Win32 架構應用程式中的 Microsoft Windows 訊息類似。</span><span class="sxs-lookup"><span data-stu-id="9041e-104">ControlEvents are analogous to Microsoft Windows messages in Win32-based applications.</span></span> <span data-ttu-id="9041e-105">但是，不是使用 [SendMessage](/windows/win32/api/winuser/nf-winuser-sendmessage) 函式來建立回呼函式，而是使用函式來接收 windows 訊息和傳送 windows 訊息，而是使用使用者介面 (UI) 安裝程式和 [控制項發行控制項](control-events.md)。</span><span class="sxs-lookup"><span data-stu-id="9041e-105">However, rather than creating a callback function to receive Windows messages and sending Windows messages with the [SendMessage](/windows/win32/api/winuser/nf-winuser-sendmessage) function, the user interface (UI) installer and controls publish [ControlEvents](control-events.md).</span></span> <span data-ttu-id="9041e-106">您可以指定其他控制項和安裝程式來訂閱特定的控制項，然後變更訂閱控制項的屬性。</span><span class="sxs-lookup"><span data-stu-id="9041e-106">Other controls and the installer can be specified to subscribe to particular ControlEvents that will then change attributes of the subscribing control.</span></span> <span data-ttu-id="9041e-107">若要將工作控制項新增至對話方塊，UI 的作者會指定在 [ControlEvent 資料表](controlevent-table.md) 中進行事件的發行，並訂閱控制項以在 [EventMapping 資料表](eventmapping-table.md)中進行事件處理。</span><span class="sxs-lookup"><span data-stu-id="9041e-107">To add working controls to dialog boxes, the author of the UI specifies the publication of ControlEvents in the [ControlEvent table](controlevent-table.md) and subscribes controls to ControlEvents in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="9041e-108">安裝程式會將下列事件發行至 [EventMapping 資料表](eventmapping-table.md)中所列的訂閱控制項。</span><span class="sxs-lookup"><span data-stu-id="9041e-108">The installer will publish the following events to subscribing controls listed in the [EventMapping table](eventmapping-table.md).</span></span> <span data-ttu-id="9041e-109">[ProgressBar 控制項](progressbar-control.md)或[佈告欄控制項](billboard-control.md)通常會訂閱 SetProgress，其餘部分則由[文字控制項](text-control.md)訂閱。</span><span class="sxs-lookup"><span data-stu-id="9041e-109">A [ProgressBar control](progressbar-control.md) or [Billboard control](billboard-control.md) typically subscribes to SetProgress, the rest are subscribed to by [Text controls](text-control.md).</span></span>

[<span data-ttu-id="9041e-110">ActionData ControlEvent</span><span class="sxs-lookup"><span data-stu-id="9041e-110">ActionData ControlEvent</span></span>](actiondata-controlevent.md)

[<span data-ttu-id="9041e-111">ActionText ControlEvent</span><span class="sxs-lookup"><span data-stu-id="9041e-111">ActionText ControlEvent</span></span>](actiontext-controlevent.md)

[<span data-ttu-id="9041e-112">SetProgress ControlEvent</span><span class="sxs-lookup"><span data-stu-id="9041e-112">SetProgress ControlEvent</span></span>](setprogress-controlevent.md)

[<span data-ttu-id="9041e-113">TimeRemaining ControlEvent</span><span class="sxs-lookup"><span data-stu-id="9041e-113">TimeRemaining ControlEvent</span></span>](timeremaining-controlevent.md)

[<span data-ttu-id="9041e-114">ScriptInProgress ControlEvent</span><span class="sxs-lookup"><span data-stu-id="9041e-114">ScriptInProgress ControlEvent</span></span>](scriptinprogress-controlevent.md)

<span data-ttu-id="9041e-115">當專案選取範圍移至 [SelectionTree 控制項](selectiontree-control.md) 或 [DirectoryList 控制項](directorylist-control.md)時，控制項就會發佈下列事件。</span><span class="sxs-lookup"><span data-stu-id="9041e-115">The following events are published by the control when the item selection is moved in a [SelectionTree control](selectiontree-control.md) or [DirectoryList Control](directorylist-control.md).</span></span> <span data-ttu-id="9041e-116">訂閱控制項必須位於相同的對話方塊上，並且列在 EventMapping 資料表中。</span><span class="sxs-lookup"><span data-stu-id="9041e-116">Subscribing controls must be located on the same dialog box and listed in the EventMapping table.</span></span>

[<span data-ttu-id="9041e-117">IgnoreChange ControlEvent</span><span class="sxs-lookup"><span data-stu-id="9041e-117">IgnoreChange ControlEvent</span></span>](ignorechange-controlevent.md)

[<span data-ttu-id="9041e-118">SelectionDescription ControlEvent</span><span class="sxs-lookup"><span data-stu-id="9041e-118">SelectionDescription ControlEvent</span></span>](selectiondescription-controlevent.md)

[<span data-ttu-id="9041e-119">SelectionSize ControlEvent</span><span class="sxs-lookup"><span data-stu-id="9041e-119">SelectionSize ControlEvent</span></span>](selectionsize-controlevent.md)

[<span data-ttu-id="9041e-120">SelectionPath ControlEvent</span><span class="sxs-lookup"><span data-stu-id="9041e-120">SelectionPath ControlEvent</span></span>](selectionpath-controlevent.md)

[<span data-ttu-id="9041e-121">SelectionAction ControlEvent</span><span class="sxs-lookup"><span data-stu-id="9041e-121">SelectionAction ControlEvent</span></span>](selectionaction-controlevent.md)

[<span data-ttu-id="9041e-122">SelectionNoItems ControlEvent</span><span class="sxs-lookup"><span data-stu-id="9041e-122">SelectionNoItems ControlEvent</span></span>](selectionnoitems-controlevent.md)

<span data-ttu-id="9041e-123">您可以藉由在對話方塊中與 [按鈕控制項](pushbutton-control.md) 或 [核取方塊控制項](checkbox-control.md) 互動，以使用者的意願來發行下列事件。</span><span class="sxs-lookup"><span data-stu-id="9041e-123">The following ControlEvents can be published at the discretion of a user by interacting with a [PushButton control](pushbutton-control.md) or [CheckBox control](checkbox-control.md) on a dialog box.</span></span> <span data-ttu-id="9041e-124">Checkbox 控制項只能發行 AddLocal、AddSource、Remove、Dataadapter.doaction 和 SetProperty 事件。</span><span class="sxs-lookup"><span data-stu-id="9041e-124">The Checkbox control can only publish the AddLocal, AddSource, Remove, DoAction, and SetProperty events.</span></span> <span data-ttu-id="9041e-125">有了 Windows Server 2003 和更新版本隨附的 Windows Installer 版本， [SelectionTree 控制項](selectiontree-control.md) 可以發佈 Dataadapter.doaction、ControlEvent 和 SetProperty 事件。</span><span class="sxs-lookup"><span data-stu-id="9041e-125">With Windows Installer versions that shipped with Windows Server 2003 and later, the [SelectionTree control](selectiontree-control.md) can publish the DoAction, ControlEvent and SetProperty ControlEvents.</span></span> <span data-ttu-id="9041e-126">UI 的作者應該會列出 [ControlEvent 資料表](controlevent-table.md)中的 ControlEvent。</span><span class="sxs-lookup"><span data-stu-id="9041e-126">The author of the UI should list the ControlEvent in the [ControlEvent table](controlevent-table.md).</span></span> <span data-ttu-id="9041e-127">安裝程式的 UI 處理常式是這些事件的訂閱者。</span><span class="sxs-lookup"><span data-stu-id="9041e-127">The UI handler of the installer is the subscriber to these events.</span></span>

[<span data-ttu-id="9041e-128">AddLocal ControlEvent</span><span class="sxs-lookup"><span data-stu-id="9041e-128">AddLocal ControlEvent</span></span>](addlocal-controlevent.md)

[<span data-ttu-id="9041e-129">AddSource ControlEvent</span><span class="sxs-lookup"><span data-stu-id="9041e-129">AddSource ControlEvent</span></span>](addsource-controlevent.md)

[<span data-ttu-id="9041e-130">CheckExistingTargetPath ControlEvent</span><span class="sxs-lookup"><span data-stu-id="9041e-130">CheckExistingTargetPath ControlEvent</span></span>](checkexistingtargetpath-controlevent.md)

[<span data-ttu-id="9041e-131">CheckTargetPath ControlEvent</span><span class="sxs-lookup"><span data-stu-id="9041e-131">CheckTargetPath ControlEvent</span></span>](checktargetpath-controlevent.md)

[<span data-ttu-id="9041e-132">Dataadapter.doaction ControlEvent</span><span class="sxs-lookup"><span data-stu-id="9041e-132">DoAction ControlEvent</span></span>](doaction-controlevent.md)

[<span data-ttu-id="9041e-133">EnableRollback ControlEvent</span><span class="sxs-lookup"><span data-stu-id="9041e-133">EnableRollback ControlEvent</span></span>](enablerollback-controlevent.md)

[<span data-ttu-id="9041e-134">EndDialog ControlEvent</span><span class="sxs-lookup"><span data-stu-id="9041e-134">EndDialog ControlEvent</span></span>](enddialog-controlevent.md)

[<span data-ttu-id="9041e-135">NewDialog ControlEvent</span><span class="sxs-lookup"><span data-stu-id="9041e-135">NewDialog ControlEvent</span></span>](newdialog-controlevent.md)

[<span data-ttu-id="9041e-136">重新安裝 ControlEvent</span><span class="sxs-lookup"><span data-stu-id="9041e-136">Reinstall ControlEvent</span></span>](reinstall-controlevent.md)

[<span data-ttu-id="9041e-137">ReinstallMode ControlEvent</span><span class="sxs-lookup"><span data-stu-id="9041e-137">ReinstallMode ControlEvent</span></span>](reinstallmode-controlevent.md)

[<span data-ttu-id="9041e-138">移除 ControlEvent</span><span class="sxs-lookup"><span data-stu-id="9041e-138">Remove ControlEvent</span></span>](remove-controlevent.md)

[<span data-ttu-id="9041e-139">重設 ControlEvent</span><span class="sxs-lookup"><span data-stu-id="9041e-139">Reset ControlEvent</span></span>](reset-controlevent.md)

[<span data-ttu-id="9041e-140">SetInstallLevel ControlEvent</span><span class="sxs-lookup"><span data-stu-id="9041e-140">SetInstallLevel ControlEvent</span></span>](setinstalllevel-controlevent.md)

[<span data-ttu-id="9041e-141">SetProperty ControlEvent</span><span class="sxs-lookup"><span data-stu-id="9041e-141">SetProperty ControlEvent</span></span>](setproperty-controlevent.md)

[<span data-ttu-id="9041e-142">SetTargetPath ControlEvent</span><span class="sxs-lookup"><span data-stu-id="9041e-142">SetTargetPath ControlEvent</span></span>](settargetpath-controlevent.md)

[<span data-ttu-id="9041e-143">SpawnDialog ControlEvent</span><span class="sxs-lookup"><span data-stu-id="9041e-143">SpawnDialog ControlEvent</span></span>](spawndialog-controlevent.md)

[<span data-ttu-id="9041e-144">SpawnWaitDialog ControlEvent</span><span class="sxs-lookup"><span data-stu-id="9041e-144">SpawnWaitDialog ControlEvent</span></span>](spawnwaitdialog-controlevent.md)

[<span data-ttu-id="9041e-145">ValidateProductID ControlEvent</span><span class="sxs-lookup"><span data-stu-id="9041e-145">ValidateProductID ControlEvent</span></span>](validateproductid-controlevent.md)

<span data-ttu-id="9041e-146">[按鈕控制項](pushbutton-control.md)可以將下列事件發行至位於相同對話方塊中的訂閱[SelectionTree 控制項](selectiontree-control.md)或[DirectoryList 控制項](directorylist-control.md)。</span><span class="sxs-lookup"><span data-stu-id="9041e-146">A [PushButton control](pushbutton-control.md) can publish the following events to a subscribing [SelectionTree control](selectiontree-control.md) or [DirectoryList control](directorylist-control.md) located in the same dialog box.</span></span> <span data-ttu-id="9041e-147">[按鈕] 控制項應列在 ControlEvent 資料表中，而且訂閱控制項應列在 [EventMapping] 資料表中。</span><span class="sxs-lookup"><span data-stu-id="9041e-147">The PushButton Control should be listed in the ControlEvent table and the subscribing controls should be listed in the EventMapping table.</span></span>

[<span data-ttu-id="9041e-148">SelectionBrowse ControlEvent</span><span class="sxs-lookup"><span data-stu-id="9041e-148">SelectionBrowse ControlEvent</span></span>](selectionbrowse-controlevent.md)

[<span data-ttu-id="9041e-149">DirectoryListUp ControlEvent</span><span class="sxs-lookup"><span data-stu-id="9041e-149">DirectoryListUp ControlEvent</span></span>](directorylistup-controlevent.md)

[<span data-ttu-id="9041e-150">DirectoryListNew ControlEvent</span><span class="sxs-lookup"><span data-stu-id="9041e-150">DirectoryListNew ControlEvent</span></span>](directorylistnew-controlevent.md)

[<span data-ttu-id="9041e-151">DirectoryListOpen ControlEvent</span><span class="sxs-lookup"><span data-stu-id="9041e-151">DirectoryListOpen ControlEvent</span></span>](directorylistopen-controlevent.md)

<span data-ttu-id="9041e-152">控制事件通常需要在 [*完整的 ui*](f-gly.md) 層級上執行 ui。</span><span class="sxs-lookup"><span data-stu-id="9041e-152">Control events generally require that the UI be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="9041e-153">大部分的事件處理都不會使用 [*精簡的 ui*](r-gly.md) 或 [*基本 ui*](b-gly.md) ，因為這些層級只會顯示非強制回應對話方塊。</span><span class="sxs-lookup"><span data-stu-id="9041e-153">Most ControlEvents will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md) because these levels only display modeless dialog boxes.</span></span> <span data-ttu-id="9041e-154">ActionText、AddSource、SetProgress、TimeRemaining 和 ScriptInProgress 事件都是例外狀況，並可在精簡或基本的 UI 中運作。</span><span class="sxs-lookup"><span data-stu-id="9041e-154">The ActionText, AddSource, SetProgress, TimeRemaining, and ScriptInProgress events are exceptions and will work in reduced or basic UI.</span></span> <span data-ttu-id="9041e-155">如需 UI 層級的詳細資訊，請參閱 [消費者介面層級](user-interface-levels.md)。</span><span class="sxs-lookup"><span data-stu-id="9041e-155">For more information about UI levels, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="9041e-156">您可以從[按鈕控制項](pushbutton-control.md)或[核取方塊控制項](checkbox-control.md)發佈 ControlEvent，以執行[自訂動作](custom-actions.md)。</span><span class="sxs-lookup"><span data-stu-id="9041e-156">You can run [custom actions](custom-actions.md) by publishing a ControlEvent from a [PushButton control](pushbutton-control.md) or [Checkbox control](checkbox-control.md).</span></span> <span data-ttu-id="9041e-157">將記錄加入至 [ControlEvent 資料表](controlevent-table.md) ，其中包含對話方塊的名稱和發行 ControlEvent 的控制項。</span><span class="sxs-lookup"><span data-stu-id="9041e-157">Add a record to the [ControlEvent table](controlevent-table.md) with the names of the dialog and the control publishing the ControlEvent.</span></span> <span data-ttu-id="9041e-158">此控制項應發佈 [Dataadapter.doaction ControlEvent](doaction-controlevent.md) ，通知安裝程式執行自訂動作。</span><span class="sxs-lookup"><span data-stu-id="9041e-158">This control should publish a [DoAction ControlEvent](doaction-controlevent.md) notifying the installer to run the custom action.</span></span> <span data-ttu-id="9041e-159">在 Windows XP 或舊版系統上，您無法從 [SelectionTree 控制項](selectiontree-control.md)發佈 ControlEvent 來執行自訂動作。</span><span class="sxs-lookup"><span data-stu-id="9041e-159">On Windows XP or earlier systems, you cannot run a custom action by publishing a ControlEvent from a [SelectionTree control](selectiontree-control.md).</span></span>

<span data-ttu-id="9041e-160">如需有關特定事件的詳細資訊，請參閱[消費者介面參考](user-interface-reference.md)中的標準[事件](control-events.md)清單。</span><span class="sxs-lookup"><span data-stu-id="9041e-160">For a more information about particular ControlEvents, see the list of standard [ControlEvents](control-events.md) in [User Interface Reference](user-interface-reference.md).</span></span>

 

 

---
description: EventMapping 資料表會列出訂閱某些控制項事件的控制項，並列出當其他控制項或 Windows Installer 發佈事件時要變更的屬性。
ms.assetid: 63c9ba3e-aa8a-475b-8360-4aec78ed19db
title: EventMapping 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6e9a7b5b4283b5d70102123dcb11e3e9e844221
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848851"
---
# <a name="eventmapping-table"></a><span data-ttu-id="1af2d-103">EventMapping 資料表</span><span class="sxs-lookup"><span data-stu-id="1af2d-103">EventMapping Table</span></span>

<span data-ttu-id="1af2d-104">EventMapping 資料表會列出訂閱某些控制項事件的控制項，並列出當其他控制項或 Windows Installer 發佈事件時要變更的屬性。</span><span class="sxs-lookup"><span data-stu-id="1af2d-104">The EventMapping Table lists the controls that subscribe to some control events, and lists the attribute to be changed when the event is published by another control or the Windows Installer.</span></span>

<span data-ttu-id="1af2d-105">EventMapping 資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="1af2d-105">The EventMapping Table has the following columns.</span></span>



| <span data-ttu-id="1af2d-106">Column</span><span class="sxs-lookup"><span data-stu-id="1af2d-106">Column</span></span>    | <span data-ttu-id="1af2d-107">類型</span><span class="sxs-lookup"><span data-stu-id="1af2d-107">Type</span></span>                         | <span data-ttu-id="1af2d-108">答案</span><span class="sxs-lookup"><span data-stu-id="1af2d-108">Key</span></span> | <span data-ttu-id="1af2d-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="1af2d-109">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="1af2d-110">對話\_</span><span class="sxs-lookup"><span data-stu-id="1af2d-110">Dialog\_</span></span>  | [<span data-ttu-id="1af2d-111">識別碼</span><span class="sxs-lookup"><span data-stu-id="1af2d-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="1af2d-112">Y</span><span class="sxs-lookup"><span data-stu-id="1af2d-112">Y</span></span>   | <span data-ttu-id="1af2d-113">N</span><span class="sxs-lookup"><span data-stu-id="1af2d-113">N</span></span>        |
| <span data-ttu-id="1af2d-114">控制項\_</span><span class="sxs-lookup"><span data-stu-id="1af2d-114">Control\_</span></span> | [<span data-ttu-id="1af2d-115">識別碼</span><span class="sxs-lookup"><span data-stu-id="1af2d-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="1af2d-116">Y</span><span class="sxs-lookup"><span data-stu-id="1af2d-116">Y</span></span>   | <span data-ttu-id="1af2d-117">N</span><span class="sxs-lookup"><span data-stu-id="1af2d-117">N</span></span>        |
| <span data-ttu-id="1af2d-118">事件</span><span class="sxs-lookup"><span data-stu-id="1af2d-118">Event</span></span>     | [<span data-ttu-id="1af2d-119">識別碼</span><span class="sxs-lookup"><span data-stu-id="1af2d-119">Identifier</span></span>](identifier.md) | <span data-ttu-id="1af2d-120">Y</span><span class="sxs-lookup"><span data-stu-id="1af2d-120">Y</span></span>   | <span data-ttu-id="1af2d-121">N</span><span class="sxs-lookup"><span data-stu-id="1af2d-121">N</span></span>        |
| <span data-ttu-id="1af2d-122">屬性</span><span class="sxs-lookup"><span data-stu-id="1af2d-122">Attribute</span></span> | [<span data-ttu-id="1af2d-123">識別碼</span><span class="sxs-lookup"><span data-stu-id="1af2d-123">Identifier</span></span>](identifier.md) | <span data-ttu-id="1af2d-124">N</span><span class="sxs-lookup"><span data-stu-id="1af2d-124">N</span></span>   | <span data-ttu-id="1af2d-125">N</span><span class="sxs-lookup"><span data-stu-id="1af2d-125">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="1af2d-126">資料行</span><span class="sxs-lookup"><span data-stu-id="1af2d-126">Columns</span></span>

<dl> <dt>

<span data-ttu-id="1af2d-127"><span id="Dialog_"></span><span id="dialog_"></span><span id="DIALOG_"></span>對話 框\_</span><span class="sxs-lookup"><span data-stu-id="1af2d-127"><span id="Dialog_"></span><span id="dialog_"></span><span id="DIALOG_"></span>Dialog\_</span></span>
</dt> <dd>

<span data-ttu-id="1af2d-128">[對話方塊資料表](dialog-table.md)第一個資料行的外部索引鍵。</span><span class="sxs-lookup"><span data-stu-id="1af2d-128">An external key to the first column of the [Dialog Table](dialog-table.md).</span></span> <span data-ttu-id="1af2d-129">這個欄位和控制項 \_ 欄位會一起識別控制項。</span><span class="sxs-lookup"><span data-stu-id="1af2d-129">This field and the Control\_ field together identify a control.</span></span>

</dd> <dt>

<span data-ttu-id="1af2d-130"><span id="Control_"></span><span id="control_"></span><span id="CONTROL_"></span>控制\_</span><span class="sxs-lookup"><span data-stu-id="1af2d-130"><span id="Control_"></span><span id="control_"></span><span id="CONTROL_"></span>Control\_</span></span>
</dt> <dd>

<span data-ttu-id="1af2d-131">[控制資料表](control-table.md)第二個數據行的外部索引鍵。</span><span class="sxs-lookup"><span data-stu-id="1af2d-131">An external key to the second column of the [Control Table](control-table.md).</span></span> <span data-ttu-id="1af2d-132">這個欄位和對話 \_ 欄位會一起識別控制項。</span><span class="sxs-lookup"><span data-stu-id="1af2d-132">This field and the Dialog\_ field together identify a control.</span></span>

</dd> <dt>

<span data-ttu-id="1af2d-133"><span id="Event"></span><span id="event"></span><span id="EVENT"></span>事件</span><span class="sxs-lookup"><span data-stu-id="1af2d-133"><span id="Event"></span><span id="event"></span><span id="EVENT"></span>Event</span></span>
</dt> <dd>

<span data-ttu-id="1af2d-134">此欄位是指定控制項所訂閱之事件種類的識別碼。</span><span class="sxs-lookup"><span data-stu-id="1af2d-134">This field is an identifier that specifies the type of event that is subscribed to by the control.</span></span> <span data-ttu-id="1af2d-135">如需詳細資訊，請參閱 [ControlEvent 總覽](controlevent-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="1af2d-135">For more information, see [ControlEvent Overview](controlevent-overview.md).</span></span>

</dd> <dt>

<span data-ttu-id="1af2d-136"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>屬性</span><span class="sxs-lookup"><span data-stu-id="1af2d-136"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>Attribute</span></span>
</dt> <dd>

<span data-ttu-id="1af2d-137">\_當收到事件資料行中的事件時，所設定的控制項屬性名稱。</span><span class="sxs-lookup"><span data-stu-id="1af2d-137">The name of the Control\_ attribute that is set when the event in the Event column is received.</span></span> <span data-ttu-id="1af2d-138">事件的引數會以屬性呼叫的引數形式傳遞，以變更控制項的這個屬性。</span><span class="sxs-lookup"><span data-stu-id="1af2d-138">The Argument of the event is passed as the argument of the attribute call to change this attribute of the control.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1af2d-139">備註</span><span class="sxs-lookup"><span data-stu-id="1af2d-139">Remarks</span></span>

<span data-ttu-id="1af2d-140">[ControlEvent 資料表](controlevent-table.md)會指定使用者與[按鈕控制項](pushbutton-control.md)、 [CheckBox 控制項](checkbox-control.md)或[SelectionTree 控制項](selectiontree-control.md)互動時，所啟動的控制項事件。</span><span class="sxs-lookup"><span data-stu-id="1af2d-140">The [ControlEvent Table](controlevent-table.md) specifies the control events that are started when a user interacts with a [PushButton Control](pushbutton-control.md), [CheckBox Control](checkbox-control.md), or [SelectionTree Control](selectiontree-control.md).</span></span> <span data-ttu-id="1af2d-141">這些是使用者唯一可用來起始控制項事件的控制項。</span><span class="sxs-lookup"><span data-stu-id="1af2d-141">These are the only controls that a user can use to initiate control events.</span></span>

<span data-ttu-id="1af2d-142">對話方塊上有一個以上的控制項可以訂閱相同的事件。</span><span class="sxs-lookup"><span data-stu-id="1af2d-142">More than one control on a dialog box can subscribe to the same event.</span></span>

<span data-ttu-id="1af2d-143">下列清單會識別 EventMapping 資料表的一般用途：</span><span class="sxs-lookup"><span data-stu-id="1af2d-143">The following list identifies the typical uses for the EventMapping Table:</span></span>

-   <span data-ttu-id="1af2d-144">若要將[文字控制項](text-control.md)訂閱至[ActionText ControlEvent](actiontext-controlevent.md)、 [ActionData ControlEvent](actiondata-controlevent.md)、 [ScriptInProgress ControlEvent](scriptinprogress-controlevent.md)或 Windows Installer 所發佈的[TimeRemaining ControlEvent。](timeremaining-controlevent.md)</span><span class="sxs-lookup"><span data-stu-id="1af2d-144">To subscribe a [Text Control](text-control.md) to an [ActionText ControlEvent](actiontext-controlevent.md), [ActionData ControlEvent](actiondata-controlevent.md), [ScriptInProgress ControlEvent](scriptinprogress-controlevent.md) or [TimeRemaining ControlEvent](timeremaining-controlevent.md) published by the Windows Installer.</span></span>
-   <span data-ttu-id="1af2d-145">將 [ProgressBar 控制項](progressbar-control.md) 或 [佈告欄控制項](billboard-control.md) 訂閱至 [SetProgress ControlEvent](setprogress-controlevent.md)。</span><span class="sxs-lookup"><span data-stu-id="1af2d-145">To subscribe a [ProgressBar Control](progressbar-control.md) or [Billboard Control](billboard-control.md) to a [SetProgress ControlEvent](setprogress-controlevent.md).</span></span>
-   <span data-ttu-id="1af2d-146">將 [DirectoryCombo 控制項](directorycombo-control.md) 訂閱至 [IgnoreChange ControlEvent](ignorechange-controlevent.md)。</span><span class="sxs-lookup"><span data-stu-id="1af2d-146">To subscribe a [DirectoryCombo Control](directorycombo-control.md) to an [IgnoreChange ControlEvent](ignorechange-controlevent.md).</span></span>
-   <span data-ttu-id="1af2d-147">使用[SelectionTree 控制項](selectiontree-control.md)自動停用位於相同對話方塊上的[按鈕控制項](pushbutton-control.md)。</span><span class="sxs-lookup"><span data-stu-id="1af2d-147">To automatically disable a [PushButton Control](pushbutton-control.md) located on the same dialog with a [SelectionTree Control](selectiontree-control.md).</span></span> <span data-ttu-id="1af2d-148">若要在 [SelectionTree 控制項](selectiontree-control.md)中未列出任何功能時停用推播按鈕，請使用 EventMapping 資料表來訂閱 [SelectionNoItems ControlEvent](selectionnoitems-controlevent.md)的按鈕控制項。</span><span class="sxs-lookup"><span data-stu-id="1af2d-148">To disable the push button when no features are listed in the [SelectionTree Control](selectiontree-control.md), use the EventMapping Table to subscribe the PushButton control to a [SelectionNoItems ControlEvent](selectionnoitems-controlevent.md).</span></span> <span data-ttu-id="1af2d-149">在 EventMapping 資料表的 [屬性] 欄位中輸入 **Enable** 。</span><span class="sxs-lookup"><span data-stu-id="1af2d-149">Enter **Enable** in the Attributes field of the EventMapping Table.</span></span>
-   <span data-ttu-id="1af2d-150">顯示 [文字控制項](text-control.md) ，顯示在相同對話方塊上， [SelectionTree 控制項](selectiontree-control.md) 中所選取之功能的安裝位置路徑。</span><span class="sxs-lookup"><span data-stu-id="1af2d-150">To display a [Text Control](text-control.md) that shows the path to the installation location for the feature that is selected in a [SelectionTree Control](selectiontree-control.md) on the same dialog.</span></span> <span data-ttu-id="1af2d-151">您可以使用 EventMapping 資料表，將[文字控制項](text-control.md)訂閱至[ControlEvent 控制項](selectiontree-control.md)所發佈的[SelectionPathOn ControlEvent](selectionpathon-controlevent.md)和[SelectionPath SelectionTree](selectionpath-controlevent.md) 。</span><span class="sxs-lookup"><span data-stu-id="1af2d-151">Use the EventMapping Table to subscribe the [Text Control](text-control.md) to both a [SelectionPathOn ControlEvent](selectionpathon-controlevent.md) and [SelectionPath ControlEvent](selectionpath-controlevent.md) published by the [SelectionTree Control](selectiontree-control.md).</span></span>
-   <span data-ttu-id="1af2d-152">若要顯示 [文字控制項](text-control.md) ，以顯示在相同對話方塊上 [SelectionTree 控制項](selectiontree-control.md) 中醒目提示的專案描述，請使用 EventMapping 資料表將 [文字控制項](text-control.md) 訂閱至 [SelectionDescription ControlEvent](selectiondescription-controlevent.md)、 [SelectionSize ControlEvent](selectionsize-controlevent.md) 或 [SelectionAction ControlEvent](selectionaction-controlevent.md)。</span><span class="sxs-lookup"><span data-stu-id="1af2d-152">To display a [Text Control](text-control.md) that shows a description of the item highlighted in a [SelectionTree Control](selectiontree-control.md) located on the same dialog, use the EventMapping Table to subscribe the [Text Control](text-control.md) to a [SelectionDescription ControlEvent](selectiondescription-controlevent.md), [SelectionSize ControlEvent](selectionsize-controlevent.md) or [SelectionAction ControlEvent](selectionaction-controlevent.md).</span></span> <span data-ttu-id="1af2d-153">在 [EventMapping] 資料表的 [屬性] 欄位中輸入 **文字** 。</span><span class="sxs-lookup"><span data-stu-id="1af2d-153">Enter **Text** in the Attribute field of the EventMapping Table.</span></span>

## <a name="validation"></a><span data-ttu-id="1af2d-154">驗證</span><span class="sxs-lookup"><span data-stu-id="1af2d-154">Validation</span></span>

<dl>

[<span data-ttu-id="1af2d-155">ICE03</span><span class="sxs-lookup"><span data-stu-id="1af2d-155">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="1af2d-156">ICE06</span><span class="sxs-lookup"><span data-stu-id="1af2d-156">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="1af2d-157">ICE32</span><span class="sxs-lookup"><span data-stu-id="1af2d-157">ICE32</span></span>](ice32.md)  
</dl>

 

 




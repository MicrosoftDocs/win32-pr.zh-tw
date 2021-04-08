---
description: ControlEvent 資料表可讓作者指定當使用者與按鈕控制項、CheckBox 控制項或 SelectionTree 控制項互動時，所啟動的控制項事件。
ms.assetid: e34d17e9-cd6b-4a21-9abc-9562ee648c59
title: ControlEvent 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 721dc7ac9a729b8df0623a2958a4d0fe32851307
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852347"
---
# <a name="controlevent-table"></a><span data-ttu-id="16074-103">ControlEvent 資料表</span><span class="sxs-lookup"><span data-stu-id="16074-103">ControlEvent Table</span></span>

<span data-ttu-id="16074-104">ControlEvent 資料表可讓作者指定當使用者與[按鈕控制項](pushbutton-control.md)、 [CheckBox 控制項](checkbox-control.md)或[SelectionTree 控制項](selectiontree-control.md)互動時，所啟動的[控制項事件](control-events.md)。</span><span class="sxs-lookup"><span data-stu-id="16074-104">The ControlEvent table allows the author to specify the [Control Events](control-events.md) started when a user interacts with a [PushButton Control](pushbutton-control.md), [CheckBox Control](checkbox-control.md), or [SelectionTree Control](selectiontree-control.md).</span></span> <span data-ttu-id="16074-105">這些是使用者唯一可用來起始控制項事件的控制項。</span><span class="sxs-lookup"><span data-stu-id="16074-105">These are the only controls users can use to initiate control events.</span></span> <span data-ttu-id="16074-106">每個控制項都可以發行多個控制項事件。</span><span class="sxs-lookup"><span data-stu-id="16074-106">Each control can publish multiple control events.</span></span> <span data-ttu-id="16074-107">安裝程式會依 [排序] 資料行中指定的順序啟動每個事件。</span><span class="sxs-lookup"><span data-stu-id="16074-107">The installer starts each event in the order specified in the Ordering column.</span></span> <span data-ttu-id="16074-108">例如，按鈕控制項可以發行事件，以起始轉換至另一個對話方塊、結束對話方塊序列，以及開始安裝檔案。</span><span class="sxs-lookup"><span data-stu-id="16074-108">For example, a push button control can publish events to initiate a transition to another dialog box, exit the dialog box sequence, and begin file installation.</span></span>

<span data-ttu-id="16074-109">要注意的例外狀況是每個控制項都可以發行最多一個 [NewDialog](newdialog-controlevent.md) 或一個 [SpawnDialog](spawndialog-controlevent.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="16074-109">The exception to note is that each control can publish a most one [NewDialog](newdialog-controlevent.md) or one [SpawnDialog](spawndialog-controlevent.md) event.</span></span> <span data-ttu-id="16074-110">如果您需要在此資料表中撰寫多個 NewDialog 和 SpawnDialog 控制項事件，也請在 [條件] 欄位中包含條件陳述式，以確保最多可發佈一個事件。</span><span class="sxs-lookup"><span data-stu-id="16074-110">If you need to author multiple NewDialog and SpawnDialog control events in this table, also include conditional statements in the Condition fields that ensure at most one event is published.</span></span> <span data-ttu-id="16074-111">如果針對相同的控制項選取了多個 NewDialog 和 SpawnDialog 控制項事件，則在啟用控制項時，只會發佈 [排序] 資料行中具有最大值的事件。</span><span class="sxs-lookup"><span data-stu-id="16074-111">If multiple NewDialog and SpawnDialog control events are selected for the same control, only the event with the largest value in the Ordering column gets published when the control is activated.</span></span>

<span data-ttu-id="16074-112">ControlEvent 資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="16074-112">The ControlEvent table has the following columns.</span></span>



| <span data-ttu-id="16074-113">Column</span><span class="sxs-lookup"><span data-stu-id="16074-113">Column</span></span>    | <span data-ttu-id="16074-114">類型</span><span class="sxs-lookup"><span data-stu-id="16074-114">Type</span></span>                         | <span data-ttu-id="16074-115">答案</span><span class="sxs-lookup"><span data-stu-id="16074-115">Key</span></span> | <span data-ttu-id="16074-116">Nullable</span><span class="sxs-lookup"><span data-stu-id="16074-116">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="16074-117">對話\_</span><span class="sxs-lookup"><span data-stu-id="16074-117">Dialog\_</span></span>  | [<span data-ttu-id="16074-118">識別碼</span><span class="sxs-lookup"><span data-stu-id="16074-118">Identifier</span></span>](identifier.md) | <span data-ttu-id="16074-119">Y</span><span class="sxs-lookup"><span data-stu-id="16074-119">Y</span></span>   | <span data-ttu-id="16074-120">N</span><span class="sxs-lookup"><span data-stu-id="16074-120">N</span></span>        |
| <span data-ttu-id="16074-121">控制項\_</span><span class="sxs-lookup"><span data-stu-id="16074-121">Control\_</span></span> | [<span data-ttu-id="16074-122">識別碼</span><span class="sxs-lookup"><span data-stu-id="16074-122">Identifier</span></span>](identifier.md) | <span data-ttu-id="16074-123">Y</span><span class="sxs-lookup"><span data-stu-id="16074-123">Y</span></span>   | <span data-ttu-id="16074-124">N</span><span class="sxs-lookup"><span data-stu-id="16074-124">N</span></span>        |
| <span data-ttu-id="16074-125">事件</span><span class="sxs-lookup"><span data-stu-id="16074-125">Event</span></span>     | [<span data-ttu-id="16074-126">格式 化</span><span class="sxs-lookup"><span data-stu-id="16074-126">Formatted</span></span>](formatted.md)   | <span data-ttu-id="16074-127">Y</span><span class="sxs-lookup"><span data-stu-id="16074-127">Y</span></span>   | <span data-ttu-id="16074-128">N</span><span class="sxs-lookup"><span data-stu-id="16074-128">N</span></span>        |
| <span data-ttu-id="16074-129">引數</span><span class="sxs-lookup"><span data-stu-id="16074-129">Argument</span></span>  | [<span data-ttu-id="16074-130">格式 化</span><span class="sxs-lookup"><span data-stu-id="16074-130">Formatted</span></span>](formatted.md)   | <span data-ttu-id="16074-131">Y</span><span class="sxs-lookup"><span data-stu-id="16074-131">Y</span></span>   | <span data-ttu-id="16074-132">N</span><span class="sxs-lookup"><span data-stu-id="16074-132">N</span></span>        |
| <span data-ttu-id="16074-133">條件</span><span class="sxs-lookup"><span data-stu-id="16074-133">Condition</span></span> | [<span data-ttu-id="16074-134">Condition</span><span class="sxs-lookup"><span data-stu-id="16074-134">Condition</span></span>](condition.md)   | <span data-ttu-id="16074-135">Y</span><span class="sxs-lookup"><span data-stu-id="16074-135">Y</span></span>   | <span data-ttu-id="16074-136">Y</span><span class="sxs-lookup"><span data-stu-id="16074-136">Y</span></span>        |
| <span data-ttu-id="16074-137">排序</span><span class="sxs-lookup"><span data-stu-id="16074-137">Ordering</span></span>  | [<span data-ttu-id="16074-138">整數</span><span class="sxs-lookup"><span data-stu-id="16074-138">Integer</span></span>](integer.md)       | <span data-ttu-id="16074-139">N</span><span class="sxs-lookup"><span data-stu-id="16074-139">N</span></span>   | <span data-ttu-id="16074-140">Y</span><span class="sxs-lookup"><span data-stu-id="16074-140">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="16074-141">資料行</span><span class="sxs-lookup"><span data-stu-id="16074-141">Columns</span></span>

<dl> <dt>

<span data-ttu-id="16074-142"><span id="Dialog_"></span><span id="dialog_"></span><span id="DIALOG_"></span>對話 框\_</span><span class="sxs-lookup"><span data-stu-id="16074-142"><span id="Dialog_"></span><span id="dialog_"></span><span id="DIALOG_"></span>Dialog\_</span></span>
</dt> <dd>

<span data-ttu-id="16074-143">[對話方塊資料表](dialog-table.md)第一個資料行的外部索引鍵。</span><span class="sxs-lookup"><span data-stu-id="16074-143">An external key to the first column of the [Dialog table](dialog-table.md).</span></span> <span data-ttu-id="16074-144">結合此欄位與控制項欄位，即可 \_ 識別唯一的控制項。</span><span class="sxs-lookup"><span data-stu-id="16074-144">Combining this field with the Control\_ field identifies a unique control.</span></span>

</dd> <dt>

<span data-ttu-id="16074-145"><span id="Control_"></span><span id="control_"></span><span id="CONTROL_"></span>控制\_</span><span class="sxs-lookup"><span data-stu-id="16074-145"><span id="Control_"></span><span id="control_"></span><span id="CONTROL_"></span>Control\_</span></span>
</dt> <dd>

<span data-ttu-id="16074-146">[控制資料表](control-table.md)第二個數據行的外部索引鍵。</span><span class="sxs-lookup"><span data-stu-id="16074-146">An external key to the second column of the [Control table](control-table.md).</span></span> <span data-ttu-id="16074-147">將此欄位與對話方塊欄位合併會 \_ 識別唯一的控制項。</span><span class="sxs-lookup"><span data-stu-id="16074-147">Combining this field with the Dialog\_ field identifies a unique control.</span></span>

</dd> <dt>

<span data-ttu-id="16074-148"><span id="Event"></span><span id="event"></span><span id="EVENT"></span>事件</span><span class="sxs-lookup"><span data-stu-id="16074-148"><span id="Event"></span><span id="event"></span><span id="EVENT"></span>Event</span></span>
</dt> <dd>

<span data-ttu-id="16074-149">識別碼，指定當使用者與對話方塊和控制項所指定的控制項互動時應該發生的事件種類 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="16074-149">An identifier that specifies the type of event that should take place when the user interacts with the control specified by Dialog\_ and Control\_.</span></span> <span data-ttu-id="16074-150">如需可能值的清單，請參閱 [ControlEvent 總覽](controlevent-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="16074-150">For a list of possible values see [ControlEvent Overview](controlevent-overview.md).</span></span>

<span data-ttu-id="16074-151">若要設定具有控制項的屬性，請將 \[ 屬性 \_ 名稱放 \] 在此欄位中，並在 [引數] 欄位中輸入新值。</span><span class="sxs-lookup"><span data-stu-id="16074-151">To set a property with a control, put \[Property\_Name\] in this field and the new value in the argument field.</span></span> <span data-ttu-id="16074-152">將 {} 放入引數欄位以輸入 null 值。</span><span class="sxs-lookup"><span data-stu-id="16074-152">Put { } into the argument field to enter the null value.</span></span>

</dd> <dt>

<span data-ttu-id="16074-153"><span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>參數</span><span class="sxs-lookup"><span data-stu-id="16074-153"><span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>Argument</span></span>
</dt> <dd>

<span data-ttu-id="16074-154">當觸發特定事件時，用來做為修飾詞的值。</span><span class="sxs-lookup"><span data-stu-id="16074-154">A value used as a modifier when triggering a particular event.</span></span>

<span data-ttu-id="16074-155">例如， [NewDialog ControlEvent](newdialog-controlevent.md) 或 [SpawnDialog ControlEvent](spawndialog-controlevent.md) 的引數是對話方塊的名稱，而 [安裝動作](install-action.md) 的引數則是定義安裝層級的數位。</span><span class="sxs-lookup"><span data-stu-id="16074-155">For example, the argument of the [NewDialog ControlEvent](newdialog-controlevent.md) or the [SpawnDialog ControlEvent](spawndialog-controlevent.md) is the name of the dialog box and the argument of the [Install action](install-action.md) is a number defining the install level.</span></span>

</dd> <dt>

<span data-ttu-id="16074-156"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>條件</span><span class="sxs-lookup"><span data-stu-id="16074-156"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condition</span></span>
</dt> <dd>

<span data-ttu-id="16074-157">條件陳述式，可判斷安裝程式是否在事件資料行中啟用事件。</span><span class="sxs-lookup"><span data-stu-id="16074-157">A conditional statement that determines whether the installer activates the event in the Event column.</span></span> <span data-ttu-id="16074-158">如果條件欄位中的條件陳述式評估為 True，則安裝程式會觸發事件。</span><span class="sxs-lookup"><span data-stu-id="16074-158">The installer triggers the event if the conditional statement in the Condition field evaluates to True.</span></span> <span data-ttu-id="16074-159">因此，請在此資料行中放入1，以確保安裝程式會觸發事件。</span><span class="sxs-lookup"><span data-stu-id="16074-159">Therefore put a 1 in this column to ensure that the installer triggers the event.</span></span> <span data-ttu-id="16074-160">如果條件欄位包含評估為 False 的語句，安裝程式就不會觸發事件。</span><span class="sxs-lookup"><span data-stu-id="16074-160">The installer does not trigger the event if the Condition field contains a statement that evaluates to False.</span></span> <span data-ttu-id="16074-161">除非控制項的其他事件未評估為 True，否則安裝程式不會在條件欄位中觸發具有空白的事件。</span><span class="sxs-lookup"><span data-stu-id="16074-161">The installer does not trigger an event with a blank in the Condition field unless no other events of the control evaluate to True.</span></span> <span data-ttu-id="16074-162">如果在控制項欄位中指定之控制項的條件欄位都未 \_ 評估為 True，則安裝程式會觸發一個具有空白條件欄位的事件，如果有一個以上的條件欄位為空白，則會使用 [排序] 欄位中的最大值來觸發其中一個事件。</span><span class="sxs-lookup"><span data-stu-id="16074-162">If none of the Condition fields for the control named in the Control\_ field evaluate to True, the installer triggers the one event having a blank Condition field, and if more than one Condition field is blank it triggers the one event of these with the largest value in the Ordering field.</span></span> <span data-ttu-id="16074-163">請參閱 [條件陳述式語法](conditional-statement-syntax.md)。</span><span class="sxs-lookup"><span data-stu-id="16074-163">See [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

</dd> <dt>

<span data-ttu-id="16074-164"><span id="Ordering"></span><span id="ordering"></span><span id="ORDERING"></span>訂購</span><span class="sxs-lookup"><span data-stu-id="16074-164"><span id="Ordering"></span><span id="ordering"></span><span id="ORDERING"></span>Ordering</span></span>
</dt> <dd>

<span data-ttu-id="16074-165">用來排序多個與相同控制項系結之事件的整數。</span><span class="sxs-lookup"><span data-stu-id="16074-165">An integer used to order several events tied to the same control.</span></span> <span data-ttu-id="16074-166">此值必須是非負數。</span><span class="sxs-lookup"><span data-stu-id="16074-166">This must be a non-negative number.</span></span> <span data-ttu-id="16074-167">這個欄位可以保留空白。</span><span class="sxs-lookup"><span data-stu-id="16074-167">This field may be left blank.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="16074-168">備註</span><span class="sxs-lookup"><span data-stu-id="16074-168">Remarks</span></span>

<span data-ttu-id="16074-169">[EventMapping 資料表](eventmapping-table.md)會列出訂閱某些控制項事件的控制項，並列出當另一個控制項或安裝程式發行該事件時，要變更的控制項屬性。</span><span class="sxs-lookup"><span data-stu-id="16074-169">The [EventMapping table](eventmapping-table.md) lists the controls that subscribe to some control event and lists the control attribute to be changed when that event is published by the another control or the installer.</span></span>

<span data-ttu-id="16074-170">在 Windows XP 或更早版本的作業系統上，使用者只能透過與 [Checkbox 控制項](checkbox-control.md) 或 [按鈕控制項](pushbutton-control.md)互動來發佈控制項事件。</span><span class="sxs-lookup"><span data-stu-id="16074-170">On Windows XP or earlier operating systems, users can publish a control event only by interacting with a [Checkbox Control](checkbox-control.md) or [Pushbutton Control](pushbutton-control.md).</span></span> <span data-ttu-id="16074-171">使用 Windows Server 2003 時，使用者只能透過與 [Checkbox 控制項](checkbox-control.md)、 [SelectionTree 控制項](selectiontree-control.md)和 [按鈕控制項](pushbutton-control.md)互動，來發佈控制項事件。</span><span class="sxs-lookup"><span data-stu-id="16074-171">With Windows Server 2003, users can publish a control event only by interacting with a [Checkbox Control](checkbox-control.md), [SelectionTree Control](selectiontree-control.md), and [Pushbutton Control](pushbutton-control.md).</span></span> <span data-ttu-id="16074-172">列出控制項欄位中的其他控制項 \_ 不會有任何作用。</span><span class="sxs-lookup"><span data-stu-id="16074-172">Listing other controls in the Control\_ field has no effect.</span></span>

## <a name="validation"></a><span data-ttu-id="16074-173">驗證</span><span class="sxs-lookup"><span data-stu-id="16074-173">Validation</span></span>

<dl>

[<span data-ttu-id="16074-174">ICE03</span><span class="sxs-lookup"><span data-stu-id="16074-174">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="16074-175">ICE06</span><span class="sxs-lookup"><span data-stu-id="16074-175">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="16074-176">ICE17</span><span class="sxs-lookup"><span data-stu-id="16074-176">ICE17</span></span>](ice17.md)  
[<span data-ttu-id="16074-177">ICE20</span><span class="sxs-lookup"><span data-stu-id="16074-177">ICE20</span></span>](ice20.md)  
[<span data-ttu-id="16074-178">ICE32</span><span class="sxs-lookup"><span data-stu-id="16074-178">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="16074-179">ICE44</span><span class="sxs-lookup"><span data-stu-id="16074-179">ICE44</span></span>](ice44.md)  
[<span data-ttu-id="16074-180">ICE46</span><span class="sxs-lookup"><span data-stu-id="16074-180">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="16074-181">ICE79</span><span class="sxs-lookup"><span data-stu-id="16074-181">ICE79</span></span>](ice79.md)  
[<span data-ttu-id="16074-182">ICE86</span><span class="sxs-lookup"><span data-stu-id="16074-182">ICE86</span></span>](ice86.md)  
</dl>

 

 




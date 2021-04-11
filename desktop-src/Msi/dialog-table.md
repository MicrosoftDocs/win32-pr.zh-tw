---
description: 對話方塊資料表包含使用者介面中顯示的所有對話方塊， (UI) 全部和縮減模式。
ms.assetid: 981386dd-4fee-4003-8c62-16933cc5bd14
title: 對話方塊資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09a210ad051eec950dcff8f8f940a1df11bf74c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850224"
---
# <a name="dialog-table"></a><span data-ttu-id="551b4-103">對話方塊資料表</span><span class="sxs-lookup"><span data-stu-id="551b4-103">Dialog Table</span></span>

<span data-ttu-id="551b4-104">對話方塊資料表包含使用者介面中顯示的所有對話方塊， (UI) 全部和縮減模式。</span><span class="sxs-lookup"><span data-stu-id="551b4-104">The Dialog Table contains all the dialogs that appear in the user interface (UI) in both the full and reduced modes.</span></span>

<span data-ttu-id="551b4-105">對話方塊資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="551b4-105">The Dialog Table has the following columns.</span></span>



| <span data-ttu-id="551b4-106">Column</span><span class="sxs-lookup"><span data-stu-id="551b4-106">Column</span></span>           | <span data-ttu-id="551b4-107">類型</span><span class="sxs-lookup"><span data-stu-id="551b4-107">Type</span></span>                               | <span data-ttu-id="551b4-108">答案</span><span class="sxs-lookup"><span data-stu-id="551b4-108">Key</span></span> | <span data-ttu-id="551b4-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="551b4-109">Nullable</span></span> |
|------------------|------------------------------------|-----|----------|
| <span data-ttu-id="551b4-110">對話</span><span class="sxs-lookup"><span data-stu-id="551b4-110">Dialog</span></span>           | [<span data-ttu-id="551b4-111">識別碼</span><span class="sxs-lookup"><span data-stu-id="551b4-111">Identifier</span></span>](identifier.md)       | <span data-ttu-id="551b4-112">Y</span><span class="sxs-lookup"><span data-stu-id="551b4-112">Y</span></span>   | <span data-ttu-id="551b4-113">N</span><span class="sxs-lookup"><span data-stu-id="551b4-113">N</span></span>        |
| <span data-ttu-id="551b4-114">HCentering</span><span class="sxs-lookup"><span data-stu-id="551b4-114">HCentering</span></span>       | [<span data-ttu-id="551b4-115">整數</span><span class="sxs-lookup"><span data-stu-id="551b4-115">Integer</span></span>](integer.md)             | <span data-ttu-id="551b4-116">N</span><span class="sxs-lookup"><span data-stu-id="551b4-116">N</span></span>   | <span data-ttu-id="551b4-117">N</span><span class="sxs-lookup"><span data-stu-id="551b4-117">N</span></span>        |
| <span data-ttu-id="551b4-118">VCentering</span><span class="sxs-lookup"><span data-stu-id="551b4-118">VCentering</span></span>       | [<span data-ttu-id="551b4-119">整數</span><span class="sxs-lookup"><span data-stu-id="551b4-119">Integer</span></span>](integer.md)             | <span data-ttu-id="551b4-120">N</span><span class="sxs-lookup"><span data-stu-id="551b4-120">N</span></span>   | <span data-ttu-id="551b4-121">N</span><span class="sxs-lookup"><span data-stu-id="551b4-121">N</span></span>        |
| <span data-ttu-id="551b4-122">寬度</span><span class="sxs-lookup"><span data-stu-id="551b4-122">Width</span></span>            | [<span data-ttu-id="551b4-123">整數</span><span class="sxs-lookup"><span data-stu-id="551b4-123">Integer</span></span>](integer.md)             | <span data-ttu-id="551b4-124">N</span><span class="sxs-lookup"><span data-stu-id="551b4-124">N</span></span>   | <span data-ttu-id="551b4-125">N</span><span class="sxs-lookup"><span data-stu-id="551b4-125">N</span></span>        |
| <span data-ttu-id="551b4-126">高度</span><span class="sxs-lookup"><span data-stu-id="551b4-126">Height</span></span>           | [<span data-ttu-id="551b4-127">整數</span><span class="sxs-lookup"><span data-stu-id="551b4-127">Integer</span></span>](integer.md)             | <span data-ttu-id="551b4-128">N</span><span class="sxs-lookup"><span data-stu-id="551b4-128">N</span></span>   | <span data-ttu-id="551b4-129">N</span><span class="sxs-lookup"><span data-stu-id="551b4-129">N</span></span>        |
| <span data-ttu-id="551b4-130">屬性</span><span class="sxs-lookup"><span data-stu-id="551b4-130">Attributes</span></span>       | [<span data-ttu-id="551b4-131">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="551b4-131">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="551b4-132">N</span><span class="sxs-lookup"><span data-stu-id="551b4-132">N</span></span>   | <span data-ttu-id="551b4-133">Y</span><span class="sxs-lookup"><span data-stu-id="551b4-133">Y</span></span>        |
| <span data-ttu-id="551b4-134">標題</span><span class="sxs-lookup"><span data-stu-id="551b4-134">Title</span></span>            | [<span data-ttu-id="551b4-135">格式 化</span><span class="sxs-lookup"><span data-stu-id="551b4-135">Formatted</span></span>](formatted.md)         | <span data-ttu-id="551b4-136">N</span><span class="sxs-lookup"><span data-stu-id="551b4-136">N</span></span>   | <span data-ttu-id="551b4-137">Y</span><span class="sxs-lookup"><span data-stu-id="551b4-137">Y</span></span>        |
| <span data-ttu-id="551b4-138">\_先控制項</span><span class="sxs-lookup"><span data-stu-id="551b4-138">Control\_First</span></span>   | [<span data-ttu-id="551b4-139">識別碼</span><span class="sxs-lookup"><span data-stu-id="551b4-139">Identifier</span></span>](identifier.md)       | <span data-ttu-id="551b4-140">N</span><span class="sxs-lookup"><span data-stu-id="551b4-140">N</span></span>   | <span data-ttu-id="551b4-141">N</span><span class="sxs-lookup"><span data-stu-id="551b4-141">N</span></span>        |
| <span data-ttu-id="551b4-142">控制項 \_ 預設值</span><span class="sxs-lookup"><span data-stu-id="551b4-142">Control\_Default</span></span> | [<span data-ttu-id="551b4-143">識別碼</span><span class="sxs-lookup"><span data-stu-id="551b4-143">Identifier</span></span>](identifier.md)       | <span data-ttu-id="551b4-144">N</span><span class="sxs-lookup"><span data-stu-id="551b4-144">N</span></span>   | <span data-ttu-id="551b4-145">Y</span><span class="sxs-lookup"><span data-stu-id="551b4-145">Y</span></span>        |
| <span data-ttu-id="551b4-146">控制 \_ 取消</span><span class="sxs-lookup"><span data-stu-id="551b4-146">Control\_Cancel</span></span>  | [<span data-ttu-id="551b4-147">識別碼</span><span class="sxs-lookup"><span data-stu-id="551b4-147">Identifier</span></span>](identifier.md)       | <span data-ttu-id="551b4-148">N</span><span class="sxs-lookup"><span data-stu-id="551b4-148">N</span></span>   | <span data-ttu-id="551b4-149">Y</span><span class="sxs-lookup"><span data-stu-id="551b4-149">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="551b4-150">資料行</span><span class="sxs-lookup"><span data-stu-id="551b4-150">Columns</span></span>

<dl> <dt>

<span data-ttu-id="551b4-151"><span id="Dialog"></span><span id="dialog"></span><span id="DIALOG"></span>對話 框</span><span class="sxs-lookup"><span data-stu-id="551b4-151"><span id="Dialog"></span><span id="dialog"></span><span id="DIALOG"></span>Dialog</span></span>
</dt> <dd>

<span data-ttu-id="551b4-152">對話方塊的主要索引鍵和名稱。</span><span class="sxs-lookup"><span data-stu-id="551b4-152">The primary key and name of the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="551b4-153"><span id="HCentering"></span><span id="hcentering"></span><span id="HCENTERING"></span>HCentering</span><span class="sxs-lookup"><span data-stu-id="551b4-153"><span id="HCentering"></span><span id="hcentering"></span><span id="HCENTERING"></span>HCentering</span></span>
</dt> <dd>

<span data-ttu-id="551b4-154">對話方塊的水準位置。</span><span class="sxs-lookup"><span data-stu-id="551b4-154">The horizontal position of the dialog box.</span></span>

<span data-ttu-id="551b4-155">範圍是0到100，螢幕左邊緣有0，右邊緣100。</span><span class="sxs-lookup"><span data-stu-id="551b4-155">The range is 0 to 100, with 0 at the left edge of the screen and 100 at the right edge.</span></span>

</dd> <dt>

<span data-ttu-id="551b4-156"><span id="VCentering"></span><span id="vcentering"></span><span id="VCENTERING"></span>VCentering</span><span class="sxs-lookup"><span data-stu-id="551b4-156"><span id="VCentering"></span><span id="vcentering"></span><span id="VCENTERING"></span>VCentering</span></span>
</dt> <dd>

<span data-ttu-id="551b4-157">對話方塊的垂直位置。</span><span class="sxs-lookup"><span data-stu-id="551b4-157">The vertical position of the dialog box.</span></span>

<span data-ttu-id="551b4-158">範圍是0到100，在畫面的上邊緣為0，而在下邊緣是100。</span><span class="sxs-lookup"><span data-stu-id="551b4-158">The range is 0 to 100, with 0 at the top edge of the screen and 100 at the bottom edge.</span></span>

</dd> <dt>

<span data-ttu-id="551b4-159"><span id="Width"></span><span id="width"></span><span id="WIDTH"></span>寬度</span><span class="sxs-lookup"><span data-stu-id="551b4-159"><span id="Width"></span><span id="width"></span><span id="WIDTH"></span>Width</span></span>
</dt> <dd>

<span data-ttu-id="551b4-160">對話方塊矩形邊界的寬度。</span><span class="sxs-lookup"><span data-stu-id="551b4-160">The width of the rectangular boundary of the dialog box.</span></span>

<span data-ttu-id="551b4-161">此數位必須為非負數。</span><span class="sxs-lookup"><span data-stu-id="551b4-161">This number must be non-negative.</span></span>

</dd> <dt>

<span data-ttu-id="551b4-162"><span id="Height"></span><span id="height"></span><span id="HEIGHT"></span>高度</span><span class="sxs-lookup"><span data-stu-id="551b4-162"><span id="Height"></span><span id="height"></span><span id="HEIGHT"></span>Height</span></span>
</dt> <dd>

<span data-ttu-id="551b4-163">對話方塊矩形邊界的高度。</span><span class="sxs-lookup"><span data-stu-id="551b4-163">The height of the rectangular boundary of the dialog box.</span></span>

<span data-ttu-id="551b4-164">此數位必須為非負數。</span><span class="sxs-lookup"><span data-stu-id="551b4-164">This number must be non-negative.</span></span>

</dd> <dt>

<span data-ttu-id="551b4-165"><span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>屬性</span><span class="sxs-lookup"><span data-stu-id="551b4-165"><span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>
</dt> <dd>

<span data-ttu-id="551b4-166">指定要套用至這個對話方塊之屬性旗標的32位字。</span><span class="sxs-lookup"><span data-stu-id="551b4-166">A 32-bit word that specifies the attribute flags to be applied to this dialog box.</span></span>

<span data-ttu-id="551b4-167">此數位必須為非負數。</span><span class="sxs-lookup"><span data-stu-id="551b4-167">This number must be non-negative.</span></span> <span data-ttu-id="551b4-168">如需詳細資訊，請參閱 [對話方塊樣式位](dialog-style-bits.md)。</span><span class="sxs-lookup"><span data-stu-id="551b4-168">For more information, see [Dialog Style Bits](dialog-style-bits.md).</span></span>

</dd> <dt>

<span data-ttu-id="551b4-169"><span id="Title"></span><span id="title"></span><span id="TITLE"></span>標題</span><span class="sxs-lookup"><span data-stu-id="551b4-169"><span id="Title"></span><span id="title"></span><span id="TITLE"></span>Title</span></span>
</dt> <dd>

<span data-ttu-id="551b4-170">可當地語系化的文字字串，指定要顯示在對話方塊標題列中的標題。</span><span class="sxs-lookup"><span data-stu-id="551b4-170">A localizable text string specifying the title to be displayed in the title bar of the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="551b4-171"><span id="Control_First"></span><span id="control_first"></span><span id="CONTROL_FIRST"></span>\_先控制項</span><span class="sxs-lookup"><span data-stu-id="551b4-171"><span id="Control_First"></span><span id="control_first"></span><span id="CONTROL_FIRST"></span>Control\_First</span></span>
</dt> <dd>

<span data-ttu-id="551b4-172">[控制資料表](control-table.md)第二個數據行的外部索引鍵。</span><span class="sxs-lookup"><span data-stu-id="551b4-172">An external key to the second column of the [Control Table](control-table.md).</span></span>

<span data-ttu-id="551b4-173">將此欄位與對話方塊欄位合併時，會指定在開啟對話方塊時取得焦點的 [控制資料表](control-table.md) 中的唯一控制項。</span><span class="sxs-lookup"><span data-stu-id="551b4-173">Combining this field with the Dialog field specifies a unique control in the [Control Table](control-table.md) that takes the focus when the dialog box is opened.</span></span> <span data-ttu-id="551b4-174">一般而言，這可以是 [編輯控制項](edit-control.md)、 [SelectionTree 控制項](selectiontree-control.md)，或可取得焦點的任何其他控制項。</span><span class="sxs-lookup"><span data-stu-id="551b4-174">Typically, this can be an [Edit Control](edit-control.md), [SelectionTree Control](selectiontree-control.md), or any other control that can take the focus.</span></span> <span data-ttu-id="551b4-175">如果 [按鈕控制項](pushbutton-control.md) 是可取得焦點之對話方塊中唯一的控制項，則在 [ControlDefault] 欄位中輸入的按鈕也必須輸入到 [控制項] 的第一個欄位中。</span><span class="sxs-lookup"><span data-stu-id="551b4-175">If the [PushButton Control](pushbutton-control.md) is the only control present on the dialog box that can take the focus, the PushButton entered in the ControlDefault field must also be entered into the Control First field.</span></span> <span data-ttu-id="551b4-176">[錯誤對話方塊](error-dialog.md)中會忽略此資料行。</span><span class="sxs-lookup"><span data-stu-id="551b4-176">This column is ignored in an [Error Dialog](error-dialog.md) box.</span></span>

<span data-ttu-id="551b4-177">因為靜態文字無法取得焦點，所以描述[編輯控制項](edit-control.md)、 [PathEdit 控制項](pathedit-control.md)、 [ListView 控制項](listview-control.md)、 [ComboBox 控制項](combobox-control.md)或[VolumeSelectCombo 控制項](volumeselectcombo-control.md)的[文字控制項](text-control.md)必須成為對話方塊中的第一個控制項，以確保與螢幕讀取器的相容性。</span><span class="sxs-lookup"><span data-stu-id="551b4-177">Because static text cannot take the focus, a [Text Control](text-control.md) that describes an [Edit Control](edit-control.md), [PathEdit Control](pathedit-control.md), [ListView Control](listview-control.md), [ComboBox Control](combobox-control.md) or [VolumeSelectCombo Control](volumeselectcombo-control.md) must be made the first control in the dialog box to ensure compatibility with screen readers.</span></span>

</dd> <dt>

<span data-ttu-id="551b4-178"><span id="Control_Default"></span><span id="control_default"></span><span id="CONTROL_DEFAULT"></span>控制項 \_ 預設值</span><span class="sxs-lookup"><span data-stu-id="551b4-178"><span id="Control_Default"></span><span id="control_default"></span><span id="CONTROL_DEFAULT"></span>Control\_Default</span></span>
</dt> <dd>

<span data-ttu-id="551b4-179">[控制資料表](control-table.md)第二個數據行的外部索引鍵。</span><span class="sxs-lookup"><span data-stu-id="551b4-179">An external key to the second column of the [Control Table](control-table.md).</span></span>

<span data-ttu-id="551b4-180">結合此欄位與對話方塊欄位，可指定在開啟對話方塊時取得焦點的預設控制項。</span><span class="sxs-lookup"><span data-stu-id="551b4-180">Combining this field with the Dialog field specifies the default control that takes focus when the dialog box is opened.</span></span> <span data-ttu-id="551b4-181">一般而言，這可以是 [按鈕控制項](pushbutton-control.md)。</span><span class="sxs-lookup"><span data-stu-id="551b4-181">Typically, this can be a [PushButton Control](pushbutton-control.md).</span></span> <span data-ttu-id="551b4-182">如果對話方塊上沒有任何按鈕控制項具有焦點，則傳回索引鍵相當於按一下預設控制項。</span><span class="sxs-lookup"><span data-stu-id="551b4-182">If no PushButton Control on the dialog box has the focus, the Return key is equivalent to clicking on the default control.</span></span> <span data-ttu-id="551b4-183">如果此資料行保留空白，則沒有預設控制項。</span><span class="sxs-lookup"><span data-stu-id="551b4-183">If this column is left blank, then there is no default control.</span></span> <span data-ttu-id="551b4-184">[錯誤對話方塊](error-dialog.md)中會忽略此資料行。</span><span class="sxs-lookup"><span data-stu-id="551b4-184">This column is ignored in an [Error Dialog](error-dialog.md) box.</span></span>

</dd> <dt>

<span data-ttu-id="551b4-185"><span id="Control_Cancel"></span><span id="control_cancel"></span><span id="CONTROL_CANCEL"></span>控制 \_ 取消</span><span class="sxs-lookup"><span data-stu-id="551b4-185"><span id="Control_Cancel"></span><span id="control_cancel"></span><span id="CONTROL_CANCEL"></span>Control\_Cancel</span></span>
</dt> <dd>

<span data-ttu-id="551b4-186">[控制資料表](control-table.md)第二個數據行的外部索引鍵。</span><span class="sxs-lookup"><span data-stu-id="551b4-186">An external key to the second column of the [Control Table](control-table.md).</span></span>

<span data-ttu-id="551b4-187">將此欄位與對話方塊欄位結合，可指定取消安裝的控制項。</span><span class="sxs-lookup"><span data-stu-id="551b4-187">Combining this field with the Dialog field specifies a control that cancels the installation.</span></span> <span data-ttu-id="551b4-188">此控制項會與用來取消安裝的 [ControlEvent 資料表](controlevent-table.md) 中的事件結合。</span><span class="sxs-lookup"><span data-stu-id="551b4-188">This control is coupled to events in the [ControlEvent Table](controlevent-table.md) used to cancel the installation.</span></span> <span data-ttu-id="551b4-189">按下 ESC 鍵或按一下 [關閉] 按鈕，相當於按一下 [取消] 控制項。</span><span class="sxs-lookup"><span data-stu-id="551b4-189">Hitting the ESC key or clicking the Close button is equivalent to clicking on the cancel control.</span></span> <span data-ttu-id="551b4-190">[錯誤對話方塊](error-dialog.md)中會忽略此資料行</span><span class="sxs-lookup"><span data-stu-id="551b4-190">This column is ignored in an [Error Dialog](error-dialog.md)</span></span>

<span data-ttu-id="551b4-191">方塊。</span><span class="sxs-lookup"><span data-stu-id="551b4-191">box.</span></span>

<span data-ttu-id="551b4-192">在復原或移除備份檔案時，會隱藏取消控制項。</span><span class="sxs-lookup"><span data-stu-id="551b4-192">The cancel control is hidden during rollback or the removal of backed up files.</span></span> <span data-ttu-id="551b4-193">內部 UI 處理常式會在收到 INSTALLMESSAGE COMMONDATA 訊息時隱藏控制項 \_ 。</span><span class="sxs-lookup"><span data-stu-id="551b4-193">The internal UI handler hides the control upon receiving a INSTALLMESSAGE\_COMMONDATA message.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="551b4-194">備註</span><span class="sxs-lookup"><span data-stu-id="551b4-194">Remarks</span></span>

<span data-ttu-id="551b4-195">寬度和高度的整數值是在 [安裝程式單位](installer-units.md)中，而不是對話方塊單位。</span><span class="sxs-lookup"><span data-stu-id="551b4-195">The integer values for width and height are in the [Installer Units](installer-units.md), not dialog units.</span></span>

<span data-ttu-id="551b4-196">在嚮導序列中的後續對話方塊中，會忽略兩個置中值。</span><span class="sxs-lookup"><span data-stu-id="551b4-196">The two centering values are ignored for subsequent dialog boxes in a wizard sequence.</span></span> <span data-ttu-id="551b4-197">對話方塊位置是由使用者設定，或與上一個對話方塊相同。</span><span class="sxs-lookup"><span data-stu-id="551b4-197">Dialog box positions are set by the user or as for the previous dialog box.</span></span> <span data-ttu-id="551b4-198">這些對話方塊順序是由 [NewDialog ControlEvent](newdialog-controlevent.md)所建立。</span><span class="sxs-lookup"><span data-stu-id="551b4-198">These dialog box sequences are created by a [NewDialog ControlEvent](newdialog-controlevent.md).</span></span>

## <a name="validation"></a><span data-ttu-id="551b4-199">驗證</span><span class="sxs-lookup"><span data-stu-id="551b4-199">Validation</span></span>

<dl>

[<span data-ttu-id="551b4-200">ICE03</span><span class="sxs-lookup"><span data-stu-id="551b4-200">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="551b4-201">ICE06</span><span class="sxs-lookup"><span data-stu-id="551b4-201">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="551b4-202">ICE13</span><span class="sxs-lookup"><span data-stu-id="551b4-202">ICE13</span></span>](ice13.md)  
[<span data-ttu-id="551b4-203">ICE20</span><span class="sxs-lookup"><span data-stu-id="551b4-203">ICE20</span></span>](ice20.md)  
[<span data-ttu-id="551b4-204">ICE23</span><span class="sxs-lookup"><span data-stu-id="551b4-204">ICE23</span></span>](ice23.md)  
[<span data-ttu-id="551b4-205">ICE27</span><span class="sxs-lookup"><span data-stu-id="551b4-205">ICE27</span></span>](ice27.md)  
[<span data-ttu-id="551b4-206">ICE32</span><span class="sxs-lookup"><span data-stu-id="551b4-206">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="551b4-207">ICE44</span><span class="sxs-lookup"><span data-stu-id="551b4-207">ICE44</span></span>](ice44.md)  
[<span data-ttu-id="551b4-208">ICE45</span><span class="sxs-lookup"><span data-stu-id="551b4-208">ICE45</span></span>](ice45.md)  
[<span data-ttu-id="551b4-209">ICE46</span><span class="sxs-lookup"><span data-stu-id="551b4-209">ICE46</span></span>](ice46.md)  
</dl>

 

 




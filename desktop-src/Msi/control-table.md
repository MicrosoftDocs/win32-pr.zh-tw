---
description: 控制資料表會定義出現在每個對話方塊上的控制項。
ms.assetid: cbe7acd6-b916-45f3-b694-d2345c5a892a
title: 控制資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ced41fcaf020a043962b16cf12d9c339901b415
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194102"
---
# <a name="control-table"></a><span data-ttu-id="3b099-103">控制資料表</span><span class="sxs-lookup"><span data-stu-id="3b099-103">Control Table</span></span>

<span data-ttu-id="3b099-104">控制資料表會定義出現在每個對話方塊上的控制項。</span><span class="sxs-lookup"><span data-stu-id="3b099-104">The Control table defines the controls that appear on each dialog box.</span></span>

<span data-ttu-id="3b099-105">控制資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="3b099-105">The Control table has the following columns.</span></span>



| <span data-ttu-id="3b099-106">Column</span><span class="sxs-lookup"><span data-stu-id="3b099-106">Column</span></span>        | <span data-ttu-id="3b099-107">類型</span><span class="sxs-lookup"><span data-stu-id="3b099-107">Type</span></span>                               | <span data-ttu-id="3b099-108">答案</span><span class="sxs-lookup"><span data-stu-id="3b099-108">Key</span></span> | <span data-ttu-id="3b099-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="3b099-109">Nullable</span></span> |
|---------------|------------------------------------|-----|----------|
| <span data-ttu-id="3b099-110">對話\_</span><span class="sxs-lookup"><span data-stu-id="3b099-110">Dialog\_</span></span>      | [<span data-ttu-id="3b099-111">識別碼</span><span class="sxs-lookup"><span data-stu-id="3b099-111">Identifier</span></span>](identifier.md)       | <span data-ttu-id="3b099-112">Y</span><span class="sxs-lookup"><span data-stu-id="3b099-112">Y</span></span>   | <span data-ttu-id="3b099-113">N</span><span class="sxs-lookup"><span data-stu-id="3b099-113">N</span></span>        |
| <span data-ttu-id="3b099-114">控制</span><span class="sxs-lookup"><span data-stu-id="3b099-114">Control</span></span>       | [<span data-ttu-id="3b099-115">識別碼</span><span class="sxs-lookup"><span data-stu-id="3b099-115">Identifier</span></span>](identifier.md)       | <span data-ttu-id="3b099-116">Y</span><span class="sxs-lookup"><span data-stu-id="3b099-116">Y</span></span>   | <span data-ttu-id="3b099-117">N</span><span class="sxs-lookup"><span data-stu-id="3b099-117">N</span></span>        |
| <span data-ttu-id="3b099-118">類型</span><span class="sxs-lookup"><span data-stu-id="3b099-118">Type</span></span>          | [<span data-ttu-id="3b099-119">識別碼</span><span class="sxs-lookup"><span data-stu-id="3b099-119">Identifier</span></span>](identifier.md)       | <span data-ttu-id="3b099-120">N</span><span class="sxs-lookup"><span data-stu-id="3b099-120">N</span></span>   | <span data-ttu-id="3b099-121">N</span><span class="sxs-lookup"><span data-stu-id="3b099-121">N</span></span>        |
| <span data-ttu-id="3b099-122">X</span><span class="sxs-lookup"><span data-stu-id="3b099-122">X</span></span>             | [<span data-ttu-id="3b099-123">整數</span><span class="sxs-lookup"><span data-stu-id="3b099-123">Integer</span></span>](integer.md)             | <span data-ttu-id="3b099-124">N</span><span class="sxs-lookup"><span data-stu-id="3b099-124">N</span></span>   | <span data-ttu-id="3b099-125">N</span><span class="sxs-lookup"><span data-stu-id="3b099-125">N</span></span>        |
| <span data-ttu-id="3b099-126">Y</span><span class="sxs-lookup"><span data-stu-id="3b099-126">Y</span></span>             | [<span data-ttu-id="3b099-127">整數</span><span class="sxs-lookup"><span data-stu-id="3b099-127">Integer</span></span>](integer.md)             | <span data-ttu-id="3b099-128">N</span><span class="sxs-lookup"><span data-stu-id="3b099-128">N</span></span>   | <span data-ttu-id="3b099-129">N</span><span class="sxs-lookup"><span data-stu-id="3b099-129">N</span></span>        |
| <span data-ttu-id="3b099-130">寬度</span><span class="sxs-lookup"><span data-stu-id="3b099-130">Width</span></span>         | [<span data-ttu-id="3b099-131">整數</span><span class="sxs-lookup"><span data-stu-id="3b099-131">Integer</span></span>](integer.md)             | <span data-ttu-id="3b099-132">N</span><span class="sxs-lookup"><span data-stu-id="3b099-132">N</span></span>   | <span data-ttu-id="3b099-133">N</span><span class="sxs-lookup"><span data-stu-id="3b099-133">N</span></span>        |
| <span data-ttu-id="3b099-134">高度</span><span class="sxs-lookup"><span data-stu-id="3b099-134">Height</span></span>        | [<span data-ttu-id="3b099-135">整數</span><span class="sxs-lookup"><span data-stu-id="3b099-135">Integer</span></span>](integer.md)             | <span data-ttu-id="3b099-136">N</span><span class="sxs-lookup"><span data-stu-id="3b099-136">N</span></span>   | <span data-ttu-id="3b099-137">N</span><span class="sxs-lookup"><span data-stu-id="3b099-137">N</span></span>        |
| <span data-ttu-id="3b099-138">屬性</span><span class="sxs-lookup"><span data-stu-id="3b099-138">Attributes</span></span>    | [<span data-ttu-id="3b099-139">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="3b099-139">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="3b099-140">N</span><span class="sxs-lookup"><span data-stu-id="3b099-140">N</span></span>   | <span data-ttu-id="3b099-141">Y</span><span class="sxs-lookup"><span data-stu-id="3b099-141">Y</span></span>        |
| <span data-ttu-id="3b099-142">屬性</span><span class="sxs-lookup"><span data-stu-id="3b099-142">Property</span></span>      | [<span data-ttu-id="3b099-143">識別碼</span><span class="sxs-lookup"><span data-stu-id="3b099-143">Identifier</span></span>](identifier.md)       | <span data-ttu-id="3b099-144">N</span><span class="sxs-lookup"><span data-stu-id="3b099-144">N</span></span>   | <span data-ttu-id="3b099-145">Y</span><span class="sxs-lookup"><span data-stu-id="3b099-145">Y</span></span>        |
| <span data-ttu-id="3b099-146">Text</span><span class="sxs-lookup"><span data-stu-id="3b099-146">Text</span></span>          | [<span data-ttu-id="3b099-147">格式 化</span><span class="sxs-lookup"><span data-stu-id="3b099-147">Formatted</span></span>](formatted.md)         | <span data-ttu-id="3b099-148">N</span><span class="sxs-lookup"><span data-stu-id="3b099-148">N</span></span>   | <span data-ttu-id="3b099-149">Y</span><span class="sxs-lookup"><span data-stu-id="3b099-149">Y</span></span>        |
| <span data-ttu-id="3b099-150">控制 \_ 下一步</span><span class="sxs-lookup"><span data-stu-id="3b099-150">Control\_Next</span></span> | [<span data-ttu-id="3b099-151">識別碼</span><span class="sxs-lookup"><span data-stu-id="3b099-151">Identifier</span></span>](identifier.md)       | <span data-ttu-id="3b099-152">N</span><span class="sxs-lookup"><span data-stu-id="3b099-152">N</span></span>   | <span data-ttu-id="3b099-153">Y</span><span class="sxs-lookup"><span data-stu-id="3b099-153">Y</span></span>        |
| <span data-ttu-id="3b099-154">Help</span><span class="sxs-lookup"><span data-stu-id="3b099-154">Help</span></span>          | [<span data-ttu-id="3b099-155">Text</span><span class="sxs-lookup"><span data-stu-id="3b099-155">Text</span></span>](text.md)                   | <span data-ttu-id="3b099-156">N</span><span class="sxs-lookup"><span data-stu-id="3b099-156">N</span></span>   | <span data-ttu-id="3b099-157">Y</span><span class="sxs-lookup"><span data-stu-id="3b099-157">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="3b099-158">資料行</span><span class="sxs-lookup"><span data-stu-id="3b099-158">Columns</span></span>

<dl> <dt>

<span data-ttu-id="3b099-159"><span id="Dialog_"></span><span id="dialog_"></span><span id="DIALOG_"></span>對話 框\_</span><span class="sxs-lookup"><span data-stu-id="3b099-159"><span id="Dialog_"></span><span id="dialog_"></span><span id="DIALOG_"></span>Dialog\_</span></span>
</dt> <dd>

<span data-ttu-id="3b099-160">對話方塊 [資料表](dialog-table.md)的第一個資料行的外部索引鍵，也就是對話方塊的名稱。</span><span class="sxs-lookup"><span data-stu-id="3b099-160">External key to the first column of the [Dialog table](dialog-table.md), the name of the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="3b099-161"><span id="Control"></span><span id="control"></span><span id="CONTROL"></span>控制</span><span class="sxs-lookup"><span data-stu-id="3b099-161"><span id="Control"></span><span id="control"></span><span id="CONTROL"></span>Control</span></span>
</dt> <dd>

<span data-ttu-id="3b099-162">控制項的名稱。</span><span class="sxs-lookup"><span data-stu-id="3b099-162">Name of the control.</span></span> <span data-ttu-id="3b099-163">這個名稱在對話方塊內必須是唯一的，但可以在不同的對話方塊上重複。</span><span class="sxs-lookup"><span data-stu-id="3b099-163">This name must be unique within a dialog box but can be repeated on different dialog boxes.</span></span> <span data-ttu-id="3b099-164">結合對話方塊資料行的控制項資料行會 \_ 形成此資料表的主要索引鍵。</span><span class="sxs-lookup"><span data-stu-id="3b099-164">The Control column combined with the Dialog\_ column form the primary key to this table.</span></span>

</dd> <dt>

<span data-ttu-id="3b099-165"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>類型</span><span class="sxs-lookup"><span data-stu-id="3b099-165"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>Type</span></span>
</dt> <dd>

<span data-ttu-id="3b099-166">控制項的類型。</span><span class="sxs-lookup"><span data-stu-id="3b099-166">The type of the control.</span></span> <span data-ttu-id="3b099-167">如需控制項類型的清單，請參閱 [控制項](controls.md)。</span><span class="sxs-lookup"><span data-stu-id="3b099-167">For a list of control types, see [Controls](controls.md).</span></span>

</dd> <dt>

<span data-ttu-id="3b099-168"><span id="X"></span><span id="x"></span>X</span><span class="sxs-lookup"><span data-stu-id="3b099-168"><span id="X"></span><span id="x"></span>X</span></span>
</dt> <dd>

<span data-ttu-id="3b099-169">控制項矩形界限左上角的水準座標。</span><span class="sxs-lookup"><span data-stu-id="3b099-169">Horizontal coordinate of the upper-left corner of the rectangular boundary of the control.</span></span> <span data-ttu-id="3b099-170">此值必須是非負數。</span><span class="sxs-lookup"><span data-stu-id="3b099-170">This must be a non-negative number.</span></span> <span data-ttu-id="3b099-171">請參閱 [Position 控制項屬性](position-control-attribute.md)。</span><span class="sxs-lookup"><span data-stu-id="3b099-171">See [Position Control Attribute](position-control-attribute.md).</span></span>

</dd> <dt>

<span data-ttu-id="3b099-172"><span id="Y"></span><span id="y"></span>Y</span><span class="sxs-lookup"><span data-stu-id="3b099-172"><span id="Y"></span><span id="y"></span>Y</span></span>
</dt> <dd>

<span data-ttu-id="3b099-173">控制項矩形界限左上角的垂直座標。</span><span class="sxs-lookup"><span data-stu-id="3b099-173">Vertical coordinate of the upper-left corner of the rectangular boundary of the control.</span></span> <span data-ttu-id="3b099-174">此值必須是非負數。</span><span class="sxs-lookup"><span data-stu-id="3b099-174">This must be a non-negative number.</span></span> <span data-ttu-id="3b099-175">請參閱 [Position 控制項屬性](position-control-attribute.md)。</span><span class="sxs-lookup"><span data-stu-id="3b099-175">See [Position Control Attribute](position-control-attribute.md).</span></span>

</dd> <dt>

<span data-ttu-id="3b099-176"><span id="Width"></span><span id="width"></span><span id="WIDTH"></span>寬度</span><span class="sxs-lookup"><span data-stu-id="3b099-176"><span id="Width"></span><span id="width"></span><span id="WIDTH"></span>Width</span></span>
</dt> <dd>

<span data-ttu-id="3b099-177">控制項矩形邊界的寬度。</span><span class="sxs-lookup"><span data-stu-id="3b099-177">Width of the rectangular boundary of the control.</span></span> <span data-ttu-id="3b099-178">此值必須是非負數。</span><span class="sxs-lookup"><span data-stu-id="3b099-178">This must be a non-negative number.</span></span> <span data-ttu-id="3b099-179">請參閱 [Position 控制項屬性](position-control-attribute.md)。</span><span class="sxs-lookup"><span data-stu-id="3b099-179">See [Position Control Attribute](position-control-attribute.md).</span></span>

</dd> <dt>

<span data-ttu-id="3b099-180"><span id="Height"></span><span id="height"></span><span id="HEIGHT"></span>高度</span><span class="sxs-lookup"><span data-stu-id="3b099-180"><span id="Height"></span><span id="height"></span><span id="HEIGHT"></span>Height</span></span>
</dt> <dd>

<span data-ttu-id="3b099-181">控制項矩形界限的高度。</span><span class="sxs-lookup"><span data-stu-id="3b099-181">Height of the rectangular boundary of the control.</span></span> <span data-ttu-id="3b099-182">此值必須是非負數。</span><span class="sxs-lookup"><span data-stu-id="3b099-182">This must be a non-negative number.</span></span> <span data-ttu-id="3b099-183">請參閱 [Position 控制項屬性](position-control-attribute.md)。</span><span class="sxs-lookup"><span data-stu-id="3b099-183">See [Position Control Attribute](position-control-attribute.md).</span></span>

</dd> <dt>

<span data-ttu-id="3b099-184"><span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>屬性</span><span class="sxs-lookup"><span data-stu-id="3b099-184"><span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>
</dt> <dd>

<span data-ttu-id="3b099-185">指定要套用至這個控制項之位旗標的32位字。</span><span class="sxs-lookup"><span data-stu-id="3b099-185">A 32-bit word that specifies the bit flags to be applied to this control.</span></span> <span data-ttu-id="3b099-186">這必須是非負數，且允許的值取決於控制項的類型。</span><span class="sxs-lookup"><span data-stu-id="3b099-186">This must be a non-negative number, and the allowed values depend upon the type of control.</span></span> <span data-ttu-id="3b099-187">如需所有控制項屬性的清單，以及此欄位中要輸入的值，請參閱 [控制項屬性](control-attributes.md)。</span><span class="sxs-lookup"><span data-stu-id="3b099-187">For a list of all control attributes, and the value to enter in this field, see [Control Attributes](control-attributes.md).</span></span>

</dd> <dt>

<span data-ttu-id="3b099-188"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>財產</span><span class="sxs-lookup"><span data-stu-id="3b099-188"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Property</span></span>
</dt> <dd>

<span data-ttu-id="3b099-189">要連結至此控制項之已定義屬性的名稱。</span><span class="sxs-lookup"><span data-stu-id="3b099-189">The name of a defined property to be linked to this control.</span></span> <span data-ttu-id="3b099-190">選項按鈕、清單方塊和下拉式方塊值會連結至相同的屬性，以系結至群組。</span><span class="sxs-lookup"><span data-stu-id="3b099-190">Radio button, list box, and combo box values are tied into a group by being linked to the same property.</span></span> <span data-ttu-id="3b099-191">現用控制項需要此資料行。</span><span class="sxs-lookup"><span data-stu-id="3b099-191">This column is required for active controls.</span></span>

</dd> <dt>

<span data-ttu-id="3b099-192"><span id="Text"></span><span id="text"></span><span id="TEXT"></span>文本</span><span class="sxs-lookup"><span data-stu-id="3b099-192"><span id="Text"></span><span id="text"></span><span id="TEXT"></span>Text</span></span>
</dt> <dd>

<span data-ttu-id="3b099-193">可當地語系化的字串，用來設定控制項中包含的初始文字。</span><span class="sxs-lookup"><span data-stu-id="3b099-193">A localizable string used to set the initial text contained in a control.</span></span> <span data-ttu-id="3b099-194">字串也可以包含內嵌屬性。</span><span class="sxs-lookup"><span data-stu-id="3b099-194">The string can also contain embedded properties.</span></span> <span data-ttu-id="3b099-195">如需包含屬性之格式化字串的語法，請參閱 [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) 函數。</span><span class="sxs-lookup"><span data-stu-id="3b099-195">For the syntax of a formatted string containing properties see the [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) function.</span></span> <span data-ttu-id="3b099-196">藉由在文字字串前面加上 {style} 來指定文字的大小、字型和色彩 \\ ，其中 style 是在文字樣式 [表](textstyle-table.md)的文字樣式中撰寫的文字樣式。</span><span class="sxs-lookup"><span data-stu-id="3b099-196">Specify the size, font, and color of the text by prefixing the text string with {\\style}, where style is a text style authored into the TextStyle column of the [TextStyle table](textstyle-table.md).</span></span> <span data-ttu-id="3b099-197">如果文字字串太長而無法放入控制項，則會被截斷。</span><span class="sxs-lookup"><span data-stu-id="3b099-197">The text string is truncated if it is too long to fit on to the control.</span></span> <span data-ttu-id="3b099-198">文字字串可能是空白的。</span><span class="sxs-lookup"><span data-stu-id="3b099-198">The text string may be blank.</span></span>

<span data-ttu-id="3b099-199">如果文字是顯示在具有 TrackDiskpace 屬性之對話方塊的[文字控制項](text-control.md)中，就必須在此欄位中特別撰寫[格式化](formatted.md)的文字字串。</span><span class="sxs-lookup"><span data-stu-id="3b099-199">Special authoring of the [Formatted](formatted.md) text string in this field is required if the text is to be displayed by a [Text Control](text-control.md) located on a dialog box having the TrackDiskpace attribute.</span></span> <span data-ttu-id="3b099-200">這是在[對話方塊資料表](dialog-table.md)的屬性中顯示的[TrackDiskSpace 對話方塊樣式位](trackdiskspace-dialog-style-bit.md)所指定的情況。</span><span class="sxs-lookup"><span data-stu-id="3b099-200">This is the case specified by the [TrackDiskSpace Dialog Style Bit](trackdiskspace-dialog-style-bit.md) appearing in the Attributes of the [Dialog table](dialog-table.md).</span></span> <span data-ttu-id="3b099-201">在此情況下，如果控制資料表的文字資料行中的格式化字串開頭為 " \[ "，且結尾為 " \] "，則您必須在字串的結尾加上空格。</span><span class="sxs-lookup"><span data-stu-id="3b099-201">In this case, if the Formatted string in the Text column of the Control table begins with "\[" and ends with "\]" then you must add a space at the end of the string.</span></span> <span data-ttu-id="3b099-202">例如，如果 DlgTextFont 是將設定為 "{ \\ DlgFontBold}" 的屬性，則格式化的字串 " \[ DlgTextFont \] MyText \[ ProductName \] " 需要右括弧之後結尾的空格。</span><span class="sxs-lookup"><span data-stu-id="3b099-202">For example, if DlgTextFont is a property that will be set to "{\\DlgFontBold}" the formatted string "\[DlgTextFont\]MyText\[ProductName\] " requires the space at the end after the closing bracket.</span></span> <span data-ttu-id="3b099-203">安裝程式需要這個額外的空間，才能正確地在文字控制項中顯示文字。</span><span class="sxs-lookup"><span data-stu-id="3b099-203">This extra space is required by the installer to correctly display the text in the Text control.</span></span>

<span data-ttu-id="3b099-204">您可以針對 [VolumeCostList](volumecostlist-control.md)、 [ListView](listview-control.md)、 [DirectoryList](directorylist-control.md)和 [SelectionTree 控制項](selectiontree-control.md)輸入簡短的描述性文字字串。</span><span class="sxs-lookup"><span data-stu-id="3b099-204">You can enter a short descriptive text string for the [VolumeCostList](volumecostlist-control.md), [ListView](listview-control.md), [DirectoryList](directorylist-control.md), and the [SelectionTree controls](selectiontree-control.md).</span></span> <span data-ttu-id="3b099-205">使用者看不到此文字，但螢幕讀取器可以讀取此文字作為控制項的描述。</span><span class="sxs-lookup"><span data-stu-id="3b099-205">This text is not seen by the user but it can be read by screen readers as the description of the control.</span></span>

<span data-ttu-id="3b099-206">另請參閱 [協助工具](accessibility.md)。</span><span class="sxs-lookup"><span data-stu-id="3b099-206">See also [Accessibility](accessibility.md).</span></span>

</dd> <dt>

<span data-ttu-id="3b099-207"><span id="Control_Next"></span><span id="control_next"></span><span id="CONTROL_NEXT"></span>控制 \_ 下一步</span><span class="sxs-lookup"><span data-stu-id="3b099-207"><span id="Control_Next"></span><span id="control_next"></span><span id="CONTROL_NEXT"></span>Control\_Next</span></span>
</dt> <dd>

<span data-ttu-id="3b099-208">相同對話方塊上另一個控制項的名稱，以及控制資料表第二個數據行的外部索引鍵。</span><span class="sxs-lookup"><span data-stu-id="3b099-208">The name of another control on the same dialog box and an external key to the second column of the Control table.</span></span> <span data-ttu-id="3b099-209">如果對話方塊中的焦點是在控制項資料行中的控制項上，則按下 tab 鍵會將焦點移至控制項下一個資料行中所列的控制項 \_ 。</span><span class="sxs-lookup"><span data-stu-id="3b099-209">If the focus in the dialog box is on the control in the Control column, hitting the tab key moves the focus to the control listed in the Control\_Next column.</span></span> <span data-ttu-id="3b099-210">因此，這個資料行是用來指定對話方塊上控制項的定位順序。</span><span class="sxs-lookup"><span data-stu-id="3b099-210">Therefore this column is used to specify the tab order of the controls on the dialog box.</span></span> <span data-ttu-id="3b099-211">控制項之間的連結必須形成封閉的迴圈。</span><span class="sxs-lookup"><span data-stu-id="3b099-211">The links between the controls must form a closed cycle.</span></span> <span data-ttu-id="3b099-212">某些控制項（例如靜態文字控制項）可以離開迴圈。</span><span class="sxs-lookup"><span data-stu-id="3b099-212">Some controls, such as static text controls, can be left out of the cycle.</span></span> <span data-ttu-id="3b099-213">在此情況下，此欄位可能會保留空白。</span><span class="sxs-lookup"><span data-stu-id="3b099-213">In this case, this field may be left blank.</span></span>

<span data-ttu-id="3b099-214">另請參閱 [協助工具](accessibility.md)。</span><span class="sxs-lookup"><span data-stu-id="3b099-214">See also [Accessibility](accessibility.md).</span></span>

</dd> <dt>

<span data-ttu-id="3b099-215"><span id="Help"></span><span id="help"></span><span id="HELP"></span>説明</span><span class="sxs-lookup"><span data-stu-id="3b099-215"><span id="Help"></span><span id="help"></span><span id="HELP"></span>Help</span></span>
</dt> <dd>

<span data-ttu-id="3b099-216">選用的可當地語系化文字字串，與 [說明] 按鈕一起使用。</span><span class="sxs-lookup"><span data-stu-id="3b099-216">Optional, localizable text strings that are used with the Help button.</span></span> <span data-ttu-id="3b099-217">字串會依分隔符號 () 分割成兩個部分 \| 。</span><span class="sxs-lookup"><span data-stu-id="3b099-217">The string is divided into two parts by a separator character (\|).</span></span> <span data-ttu-id="3b099-218">字串的第一個部分是用來做為工具提示文字。</span><span class="sxs-lookup"><span data-stu-id="3b099-218">The first part of the string is used as ToolTip text.</span></span> <span data-ttu-id="3b099-219">螢幕讀取器會為包含圖片的控制項使用此文字。</span><span class="sxs-lookup"><span data-stu-id="3b099-219">This text is used by screen readers for controls that contain a picture.</span></span> <span data-ttu-id="3b099-220">字串的第二個部分保留供日後使用。</span><span class="sxs-lookup"><span data-stu-id="3b099-220">The second part of the string is reserved for future use.</span></span> <span data-ttu-id="3b099-221">即使只有兩種類型的文字中有一種，也需要分隔符號。</span><span class="sxs-lookup"><span data-stu-id="3b099-221">The separator character is required even if only one of the two kinds of text is present.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3b099-222">備註</span><span class="sxs-lookup"><span data-stu-id="3b099-222">Remarks</span></span>

<span data-ttu-id="3b099-223">X、y、寬度和高度的整數值是在 [安裝程式單位](installer-units.md)中，而不是對話方塊單位。</span><span class="sxs-lookup"><span data-stu-id="3b099-223">The integer values for x, y, width, and height are in the [installer units](installer-units.md), not dialog units.</span></span> <span data-ttu-id="3b099-224">安裝程式單位等於10點 MS sans-serif 字型大小的一到第十二個高度。</span><span class="sxs-lookup"><span data-stu-id="3b099-224">An installer unit is equal to one-twelfth the height of the 10-point MS Sans Serif font size.</span></span> <span data-ttu-id="3b099-225">控制項的座標相對於佈告欄。</span><span class="sxs-lookup"><span data-stu-id="3b099-225">Coordinates for the controls are relative to the billboard.</span></span>

## <a name="validation"></a><span data-ttu-id="3b099-226">驗證</span><span class="sxs-lookup"><span data-stu-id="3b099-226">Validation</span></span>

<dl>

[<span data-ttu-id="3b099-227">ICE03</span><span class="sxs-lookup"><span data-stu-id="3b099-227">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="3b099-228">ICE06</span><span class="sxs-lookup"><span data-stu-id="3b099-228">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="3b099-229">ICE17</span><span class="sxs-lookup"><span data-stu-id="3b099-229">ICE17</span></span>](ice17.md)  
[<span data-ttu-id="3b099-230">ICE20</span><span class="sxs-lookup"><span data-stu-id="3b099-230">ICE20</span></span>](ice20.md)  
[<span data-ttu-id="3b099-231">ICE23</span><span class="sxs-lookup"><span data-stu-id="3b099-231">ICE23</span></span>](ice23.md)  
[<span data-ttu-id="3b099-232">ICE31</span><span class="sxs-lookup"><span data-stu-id="3b099-232">ICE31</span></span>](ice31.md)  
[<span data-ttu-id="3b099-233">ICE32</span><span class="sxs-lookup"><span data-stu-id="3b099-233">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="3b099-234">ICE34</span><span class="sxs-lookup"><span data-stu-id="3b099-234">ICE34</span></span>](ice34.md)  
[<span data-ttu-id="3b099-235">ICE45</span><span class="sxs-lookup"><span data-stu-id="3b099-235">ICE45</span></span>](ice45.md)  
[<span data-ttu-id="3b099-236">ICE46</span><span class="sxs-lookup"><span data-stu-id="3b099-236">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="3b099-237">ICE95</span><span class="sxs-lookup"><span data-stu-id="3b099-237">ICE95</span></span>](ice95.md)  
</dl>

 

 




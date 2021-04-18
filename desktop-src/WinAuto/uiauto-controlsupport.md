---
title: 標準控制項的 UI 自動化支援
description: 本主題將識別 Microsoft 消費者介面自動化支援的標準 Windows 控制項。 只有 (Windows XP 及更新版本) 提供的 ComCtrl32.dll 版本6的控制項才會提供完整的支援。
ms.assetid: 4821684c-8a90-413c-8ddc-699926e3bb09
keywords:
- 用戶端，消費者介面自動化標準控制項的支援
- 用戶端，標準控制項支援
- 用戶端、Win32 控制項
- 消費者介面自動化，標準控制項的支援
- 消費者介面自動化，標準控制項支援
- 消費者介面自動化，Win32 控制項
- 標準控制項的支援
- 標準控制項支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae6e384b9ee0fd72fd8a41aa3f791a5c996fe6d6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507080"
---
# <a name="ui-automation-support-for-standard-controls"></a><span data-ttu-id="bd750-112">標準控制項的 UI 自動化支援</span><span class="sxs-lookup"><span data-stu-id="bd750-112">UI Automation Support for Standard Controls</span></span>

<span data-ttu-id="bd750-113">本主題將識別 Microsoft 消費者介面自動化支援的標準 Windows 控制項。</span><span class="sxs-lookup"><span data-stu-id="bd750-113">This topic identifies the standard Windows controls that are supported by Microsoft UI Automation.</span></span> <span data-ttu-id="bd750-114">只有 (Windows XP 及更新版本) 提供的 ComCtrl32.dll 版本6的控制項才會提供完整的支援。</span><span class="sxs-lookup"><span data-stu-id="bd750-114">Full support is provided only for controls from version 6 of ComCtrl32.dll (available with Windows XP and later).</span></span>

> [!Note]  
> <span data-ttu-id="bd750-115">RichEdit 控制項僅支援 Windows Vista (RichEd20.dll 3.1 版和更新版本中隨附的版本，以及 MsftEdit.dll 4.1 版和更新版本的) 。</span><span class="sxs-lookup"><span data-stu-id="bd750-115">The RichEdit control is supported only for versions shipped with Windows Vista (in RichEd20.dll version 3.1 and later, and MsftEdit.dll version 4.1 and later).</span></span>

 

<span data-ttu-id="bd750-116">下表列出支援的標準控制項的類別名稱，以及對應的消費者介面自動化控制項類型。</span><span class="sxs-lookup"><span data-stu-id="bd750-116">The following table lists the class names of the supported standard controls, along with the corresponding UI Automation control types.</span></span>



| <span data-ttu-id="bd750-117">類別名稱</span><span class="sxs-lookup"><span data-stu-id="bd750-117">Class Name</span></span>          | <span data-ttu-id="bd750-118">控制項類型</span><span class="sxs-lookup"><span data-stu-id="bd750-118">Control Type</span></span>        |
|---------------------|---------------------|
| <span data-ttu-id="bd750-119">Button</span><span class="sxs-lookup"><span data-stu-id="bd750-119">Button</span></span>              | <span data-ttu-id="bd750-120">Button</span><span class="sxs-lookup"><span data-stu-id="bd750-120">Button</span></span>              |
| <span data-ttu-id="bd750-121">Button</span><span class="sxs-lookup"><span data-stu-id="bd750-121">Button</span></span>              | <span data-ttu-id="bd750-122">RadioButton</span><span class="sxs-lookup"><span data-stu-id="bd750-122">RadioButton</span></span>         |
| <span data-ttu-id="bd750-123">按鈕</span><span class="sxs-lookup"><span data-stu-id="bd750-123">Button</span></span>              | <span data-ttu-id="bd750-124">Group</span><span class="sxs-lookup"><span data-stu-id="bd750-124">Group</span></span>               |
| <span data-ttu-id="bd750-125">按鈕</span><span class="sxs-lookup"><span data-stu-id="bd750-125">Button</span></span>              | <span data-ttu-id="bd750-126">核取方塊</span><span class="sxs-lookup"><span data-stu-id="bd750-126">CheckBox</span></span>            |
| <span data-ttu-id="bd750-127">按鈕</span><span class="sxs-lookup"><span data-stu-id="bd750-127">Button</span></span>              | <span data-ttu-id="bd750-128">Hyperlink</span><span class="sxs-lookup"><span data-stu-id="bd750-128">Hyperlink</span></span>           |
| <span data-ttu-id="bd750-129">按鈕</span><span class="sxs-lookup"><span data-stu-id="bd750-129">Button</span></span>              | <span data-ttu-id="bd750-130">SplitButton</span><span class="sxs-lookup"><span data-stu-id="bd750-130">SplitButton</span></span>         |
| <span data-ttu-id="bd750-131">按鈕</span><span class="sxs-lookup"><span data-stu-id="bd750-131">Button</span></span>              | <span data-ttu-id="bd750-132">核取方塊</span><span class="sxs-lookup"><span data-stu-id="bd750-132">CheckBox</span></span>            |
| <span data-ttu-id="bd750-133">ComboBoxEx32</span><span class="sxs-lookup"><span data-stu-id="bd750-133">ComboBoxEx32</span></span>        | <span data-ttu-id="bd750-134">ComboBox</span><span class="sxs-lookup"><span data-stu-id="bd750-134">ComboBox</span></span>            |
| <span data-ttu-id="bd750-135">ComboBox</span><span class="sxs-lookup"><span data-stu-id="bd750-135">ComboBox</span></span>            | <span data-ttu-id="bd750-136">ComboBox</span><span class="sxs-lookup"><span data-stu-id="bd750-136">ComboBox</span></span>            |
| <span data-ttu-id="bd750-137">編輯</span><span class="sxs-lookup"><span data-stu-id="bd750-137">Edit</span></span>                | <span data-ttu-id="bd750-138">文件</span><span class="sxs-lookup"><span data-stu-id="bd750-138">Document</span></span>            |
| <span data-ttu-id="bd750-139">編輯</span><span class="sxs-lookup"><span data-stu-id="bd750-139">Edit</span></span>                | <span data-ttu-id="bd750-140">編輯</span><span class="sxs-lookup"><span data-stu-id="bd750-140">Edit</span></span>                |
| <span data-ttu-id="bd750-141">SysLink</span><span class="sxs-lookup"><span data-stu-id="bd750-141">SysLink</span></span>             | <span data-ttu-id="bd750-142">Hyperlink</span><span class="sxs-lookup"><span data-stu-id="bd750-142">Hyperlink</span></span>           |
| <span data-ttu-id="bd750-143">Static</span><span class="sxs-lookup"><span data-stu-id="bd750-143">Static</span></span>              | <span data-ttu-id="bd750-144">Text</span><span class="sxs-lookup"><span data-stu-id="bd750-144">Text</span></span>                |
| <span data-ttu-id="bd750-145">Static</span><span class="sxs-lookup"><span data-stu-id="bd750-145">Static</span></span>              | <span data-ttu-id="bd750-146">Image</span><span class="sxs-lookup"><span data-stu-id="bd750-146">Image</span></span>               |
| <span data-ttu-id="bd750-147">SysIPAddress32</span><span class="sxs-lookup"><span data-stu-id="bd750-147">SysIPAddress32</span></span>      | <span data-ttu-id="bd750-148">自訂</span><span class="sxs-lookup"><span data-stu-id="bd750-148">Custom</span></span>              |
| <span data-ttu-id="bd750-149">SysHeader32</span><span class="sxs-lookup"><span data-stu-id="bd750-149">SysHeader32</span></span>         | <span data-ttu-id="bd750-150">Header/HeaderItem</span><span class="sxs-lookup"><span data-stu-id="bd750-150">Header/HeaderItem</span></span>   |
| <span data-ttu-id="bd750-151">SysListView32</span><span class="sxs-lookup"><span data-stu-id="bd750-151">SysListView32</span></span>       | <span data-ttu-id="bd750-152">DataGrid</span><span class="sxs-lookup"><span data-stu-id="bd750-152">DataGrid</span></span>            |
| <span data-ttu-id="bd750-153">SysListView32</span><span class="sxs-lookup"><span data-stu-id="bd750-153">SysListView32</span></span>       | <span data-ttu-id="bd750-154">List</span><span class="sxs-lookup"><span data-stu-id="bd750-154">List</span></span>                |
| <span data-ttu-id="bd750-155">ListBox</span><span class="sxs-lookup"><span data-stu-id="bd750-155">ListBox</span></span>             | <span data-ttu-id="bd750-156">List</span><span class="sxs-lookup"><span data-stu-id="bd750-156">List</span></span>                |
| <span data-ttu-id="bd750-157">ListBox</span><span class="sxs-lookup"><span data-stu-id="bd750-157">ListBox</span></span>             | <span data-ttu-id="bd750-158">ListItem</span><span class="sxs-lookup"><span data-stu-id="bd750-158">ListItem</span></span>            |
| <span data-ttu-id="bd750-159">\#32768</span><span class="sxs-lookup"><span data-stu-id="bd750-159">\#32768</span></span>             | <span data-ttu-id="bd750-160">功能表</span><span class="sxs-lookup"><span data-stu-id="bd750-160">Menu</span></span>                |
| <span data-ttu-id="bd750-161">\#32768</span><span class="sxs-lookup"><span data-stu-id="bd750-161">\#32768</span></span>             | <span data-ttu-id="bd750-162">MenuItem</span><span class="sxs-lookup"><span data-stu-id="bd750-162">MenuItem</span></span>            |
| <span data-ttu-id="bd750-163">msctls \_ progress32</span><span class="sxs-lookup"><span data-stu-id="bd750-163">msctls\_progress32</span></span>  | <span data-ttu-id="bd750-164">進度列</span><span class="sxs-lookup"><span data-stu-id="bd750-164">ProgressBar</span></span>         |
| <span data-ttu-id="bd750-165">RichEdit</span><span class="sxs-lookup"><span data-stu-id="bd750-165">RichEdit</span></span>            | <span data-ttu-id="bd750-166">文件。</span><span class="sxs-lookup"><span data-stu-id="bd750-166">Document.</span></span> <span data-ttu-id="bd750-167">請參閱附註。</span><span class="sxs-lookup"><span data-stu-id="bd750-167">See note.</span></span> |
| <span data-ttu-id="bd750-168">RichEdit20A</span><span class="sxs-lookup"><span data-stu-id="bd750-168">RichEdit20A</span></span>         | <span data-ttu-id="bd750-169">文件</span><span class="sxs-lookup"><span data-stu-id="bd750-169">Document</span></span>            |
| <span data-ttu-id="bd750-170">RichEdit20W</span><span class="sxs-lookup"><span data-stu-id="bd750-170">RichEdit20W</span></span>         | <span data-ttu-id="bd750-171">文件</span><span class="sxs-lookup"><span data-stu-id="bd750-171">Document</span></span>            |
| <span data-ttu-id="bd750-172">RichEdit50W</span><span class="sxs-lookup"><span data-stu-id="bd750-172">RichEdit50W</span></span>         | <span data-ttu-id="bd750-173">文件</span><span class="sxs-lookup"><span data-stu-id="bd750-173">Document</span></span>            |
| <span data-ttu-id="bd750-174">ScrollBar</span><span class="sxs-lookup"><span data-stu-id="bd750-174">ScrollBar</span></span>           | <span data-ttu-id="bd750-175">滑桿</span><span class="sxs-lookup"><span data-stu-id="bd750-175">Slider</span></span>              |
| <span data-ttu-id="bd750-176">msctls \_ trackbar32</span><span class="sxs-lookup"><span data-stu-id="bd750-176">msctls\_trackbar32</span></span>  | <span data-ttu-id="bd750-177">滑桿</span><span class="sxs-lookup"><span data-stu-id="bd750-177">Slider</span></span>              |
| <span data-ttu-id="bd750-178">msctls \_ updown32</span><span class="sxs-lookup"><span data-stu-id="bd750-178">msctls\_updown32</span></span>    | <span data-ttu-id="bd750-179">Spinner</span><span class="sxs-lookup"><span data-stu-id="bd750-179">Spinner</span></span>             |
| <span data-ttu-id="bd750-180">msctls \_ statusbar32</span><span class="sxs-lookup"><span data-stu-id="bd750-180">msctls\_statusbar32</span></span> | <span data-ttu-id="bd750-181">StatusBar</span><span class="sxs-lookup"><span data-stu-id="bd750-181">StatusBar</span></span>           |
| <span data-ttu-id="bd750-182">SysTabControl32</span><span class="sxs-lookup"><span data-stu-id="bd750-182">SysTabControl32</span></span>     | <span data-ttu-id="bd750-183">索引標籤</span><span class="sxs-lookup"><span data-stu-id="bd750-183">Tab</span></span>                 |
| <span data-ttu-id="bd750-184">SysTabControl32</span><span class="sxs-lookup"><span data-stu-id="bd750-184">SysTabControl32</span></span>     | <span data-ttu-id="bd750-185">TabItem</span><span class="sxs-lookup"><span data-stu-id="bd750-185">TabItem</span></span>             |
| <span data-ttu-id="bd750-186">ToolbarWindow32</span><span class="sxs-lookup"><span data-stu-id="bd750-186">ToolbarWindow32</span></span>     | <span data-ttu-id="bd750-187">ToolBar</span><span class="sxs-lookup"><span data-stu-id="bd750-187">ToolBar</span></span>             |
| <span data-ttu-id="bd750-188">ToolbarWindow32</span><span class="sxs-lookup"><span data-stu-id="bd750-188">ToolbarWindow32</span></span>     | <span data-ttu-id="bd750-189">MenuItem</span><span class="sxs-lookup"><span data-stu-id="bd750-189">MenuItem</span></span>            |
| <span data-ttu-id="bd750-190">ToolbarWindow32</span><span class="sxs-lookup"><span data-stu-id="bd750-190">ToolbarWindow32</span></span>     | <span data-ttu-id="bd750-191">按鈕</span><span class="sxs-lookup"><span data-stu-id="bd750-191">Button</span></span>              |
| <span data-ttu-id="bd750-192">ToolbarWindow32</span><span class="sxs-lookup"><span data-stu-id="bd750-192">ToolbarWindow32</span></span>     | <span data-ttu-id="bd750-193">核取方塊</span><span class="sxs-lookup"><span data-stu-id="bd750-193">CheckBox</span></span>            |
| <span data-ttu-id="bd750-194">ToolbarWindow32</span><span class="sxs-lookup"><span data-stu-id="bd750-194">ToolbarWindow32</span></span>     | <span data-ttu-id="bd750-195">RadioButton</span><span class="sxs-lookup"><span data-stu-id="bd750-195">RadioButton</span></span>         |
| <span data-ttu-id="bd750-196">ToolbarWindow32</span><span class="sxs-lookup"><span data-stu-id="bd750-196">ToolbarWindow32</span></span>     | <span data-ttu-id="bd750-197">Separator</span><span class="sxs-lookup"><span data-stu-id="bd750-197">Separator</span></span>           |
| <span data-ttu-id="bd750-198">工具提示 \_ class32</span><span class="sxs-lookup"><span data-stu-id="bd750-198">tooltips\_class32</span></span>   | <span data-ttu-id="bd750-199">ToolTip</span><span class="sxs-lookup"><span data-stu-id="bd750-199">ToolTip</span></span>             |
| <span data-ttu-id="bd750-200">\#32774</span><span class="sxs-lookup"><span data-stu-id="bd750-200">\#32774</span></span>             | <span data-ttu-id="bd750-201">ToolTip</span><span class="sxs-lookup"><span data-stu-id="bd750-201">ToolTip</span></span>             |
| <span data-ttu-id="bd750-202">ReBarWindow32</span><span class="sxs-lookup"><span data-stu-id="bd750-202">ReBarWindow32</span></span>       | <span data-ttu-id="bd750-203">工具列</span><span class="sxs-lookup"><span data-stu-id="bd750-203">Toolbar</span></span>             |
| <span data-ttu-id="bd750-204">SysTreeView32</span><span class="sxs-lookup"><span data-stu-id="bd750-204">SysTreeView32</span></span>       | <span data-ttu-id="bd750-205">樹狀結構</span><span class="sxs-lookup"><span data-stu-id="bd750-205">Tree</span></span>                |
| <span data-ttu-id="bd750-206">SysTreeView32</span><span class="sxs-lookup"><span data-stu-id="bd750-206">SysTreeView32</span></span>       | <span data-ttu-id="bd750-207">TreeItem</span><span class="sxs-lookup"><span data-stu-id="bd750-207">TreeItem</span></span>            |



 

<span data-ttu-id="bd750-208">下表所列的控制項不受支援。</span><span class="sxs-lookup"><span data-stu-id="bd750-208">The controls listed in the following table are not supported.</span></span>



| <span data-ttu-id="bd750-209">類別名稱</span><span class="sxs-lookup"><span data-stu-id="bd750-209">Class Name</span></span>                                    | <span data-ttu-id="bd750-210">控制項類型</span><span class="sxs-lookup"><span data-stu-id="bd750-210">Control Type</span></span> |
|-----------------------------------------------|--------------|
| <span data-ttu-id="bd750-211">SysAnimate32</span><span class="sxs-lookup"><span data-stu-id="bd750-211">SysAnimate32</span></span>                                  | <span data-ttu-id="bd750-212">Image</span><span class="sxs-lookup"><span data-stu-id="bd750-212">Image</span></span>        |
| <span data-ttu-id="bd750-213">SysPager</span><span class="sxs-lookup"><span data-stu-id="bd750-213">SysPager</span></span>                                      | <span data-ttu-id="bd750-214">Spinner</span><span class="sxs-lookup"><span data-stu-id="bd750-214">Spinner</span></span>      |
| <span data-ttu-id="bd750-215">SysDateTimePick32</span><span class="sxs-lookup"><span data-stu-id="bd750-215">SysDateTimePick32</span></span>                             | <span data-ttu-id="bd750-216">自訂</span><span class="sxs-lookup"><span data-stu-id="bd750-216">Custom</span></span>       |
| <span data-ttu-id="bd750-217">SysMonthCal32</span><span class="sxs-lookup"><span data-stu-id="bd750-217">SysMonthCal32</span></span>                                 | <span data-ttu-id="bd750-218">Calendar</span><span class="sxs-lookup"><span data-stu-id="bd750-218">Calendar</span></span>     |
| <span data-ttu-id="bd750-219">MS \_ WINNOTE</span><span class="sxs-lookup"><span data-stu-id="bd750-219">MS\_WINNOTE</span></span>                                   | <span data-ttu-id="bd750-220">工具提示</span><span class="sxs-lookup"><span data-stu-id="bd750-220">Tooltip</span></span>      |
| <span data-ttu-id="bd750-221">VBBubble</span><span class="sxs-lookup"><span data-stu-id="bd750-221">VBBubble</span></span>                                      | <span data-ttu-id="bd750-222">工具提示</span><span class="sxs-lookup"><span data-stu-id="bd750-222">Tooltip</span></span>      |
| <span data-ttu-id="bd750-223">ScrollBar (當做獨立控制項使用時)</span><span class="sxs-lookup"><span data-stu-id="bd750-223">ScrollBar (when used as a standalone control)</span></span> | <span data-ttu-id="bd750-224">滑桿</span><span class="sxs-lookup"><span data-stu-id="bd750-224">Slider</span></span>       |
| <span data-ttu-id="bd750-225">SuperGrid</span><span class="sxs-lookup"><span data-stu-id="bd750-225">SuperGrid</span></span>                                     | <span data-ttu-id="bd750-226">自訂</span><span class="sxs-lookup"><span data-stu-id="bd750-226">Custom</span></span>       |



 

## <a name="related-topics"></a><span data-ttu-id="bd750-227">相關主題</span><span class="sxs-lookup"><span data-stu-id="bd750-227">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bd750-228">UI 自動化控制項類型概觀</span><span class="sxs-lookup"><span data-stu-id="bd750-228">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> </dl>

 

 





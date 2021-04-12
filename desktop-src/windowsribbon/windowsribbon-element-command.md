---
title: Command 元素
description: 表示命令定義。
ms.assetid: f332423d-d258-488d-9233-71687288b462
keywords:
- 命令元素視窗功能區
topic_type:
- apiref
api_name:
- Command
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b684b361927180a4bb87d2d7814d2f26d4fdcd91
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316138"
---
# <a name="command-element"></a><span data-ttu-id="1e290-104">Command 元素</span><span class="sxs-lookup"><span data-stu-id="1e290-104">Command element</span></span>

<span data-ttu-id="1e290-105">表示命令定義。</span><span class="sxs-lookup"><span data-stu-id="1e290-105">Represents a Command definition.</span></span>

## <a name="usage"></a><span data-ttu-id="1e290-106">使用方式</span><span class="sxs-lookup"><span data-stu-id="1e290-106">Usage</span></span>

``` syntax
<Command
  Name = "xs:string"
  Symbol = "xs:string"
  Id = "xs:positiveInteger union xs:string"
  Comment = "xs:string"
  LabelTitle = "xs:string"
  LabelDescription = "xs:string"
  TooltipTitle = "xs:string"
  TooltipDescription = "xs:string"
  Keytip = "xs:string">
  child elements
</Command>
```

## <a name="attributes"></a><span data-ttu-id="1e290-107">屬性</span><span class="sxs-lookup"><span data-stu-id="1e290-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1e290-108">屬性</span><span class="sxs-lookup"><span data-stu-id="1e290-108">Attribute</span></span></th>
<th><span data-ttu-id="1e290-109">類型</span><span class="sxs-lookup"><span data-stu-id="1e290-109">Type</span></span></th>
<th><span data-ttu-id="1e290-110">必要</span><span class="sxs-lookup"><span data-stu-id="1e290-110">Required</span></span></th>
<th><span data-ttu-id="1e290-111">描述</span><span class="sxs-lookup"><span data-stu-id="1e290-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1e290-112"><strong>註解</strong></span><span class="sxs-lookup"><span data-stu-id="1e290-112"><strong>Comment</strong></span></span><br/></td>
<td><span data-ttu-id="1e290-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="1e290-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="1e290-114">No</span><span class="sxs-lookup"><span data-stu-id="1e290-114">No</span></span><br/></td>
<td><span data-ttu-id="1e290-115">用來批註命令元素。</span><span class="sxs-lookup"><span data-stu-id="1e290-115">Used to annotate the command element.</span></span><br/> <br/><span data-ttu-id="1e290-116">
<dt><span></span><span></span><strong></strong> (xs： string) </span><span class="sxs-lookup"><span data-stu-id="1e290-116">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="1e290-117">由任何字元序列組成的字串，包括空白字元和分行符號字元。</span><span class="sxs-lookup"><span data-stu-id="1e290-117">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> <span data-ttu-id="1e290-118">最大長度：250個字元。</span><span class="sxs-lookup"><span data-stu-id="1e290-118">Maximum length: 250 characters.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1e290-119"><strong>識別碼</strong></span><span class="sxs-lookup"><span data-stu-id="1e290-119"><strong>Id</strong></span></span><br/></td>
<td><span data-ttu-id="1e290-120">xs： positiveInteger union xs： string</span><span class="sxs-lookup"><span data-stu-id="1e290-120">xs:positiveInteger union xs:string</span></span><br/></td>
<td><span data-ttu-id="1e290-121">No</span><span class="sxs-lookup"><span data-stu-id="1e290-121">No</span></span><br/></td>
<td><span data-ttu-id="1e290-122">唯一的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="1e290-122">The unique resource ID.</span></span> <br/> <br/><span data-ttu-id="1e290-123">
<dt><span></span><span></span><strong></strong> (xs： positiveInteger 和 xs： string 的聯集) </span><span class="sxs-lookup"><span data-stu-id="1e290-123">
<dt><span></span><span></span><strong></strong> (The union of xs:positiveInteger and xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="1e290-124">介於2和59999（含）之間的整數值，或以十六進位（含）表示的0xea5f。</span><span class="sxs-lookup"><span data-stu-id="1e290-124">An integer value between 2 and 59999, inclusive, or 0x2 and 0xea5f in hexadecimal, inclusive.</span></span> <br/> <span data-ttu-id="1e290-125">最大長度為10個字元，包括選擇性前置零。</span><span class="sxs-lookup"><span data-stu-id="1e290-125">Maximum length is 10 characters, including optional leading zeros.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1e290-126"><strong>Keytip</strong></span><span class="sxs-lookup"><span data-stu-id="1e290-126"><strong>Keytip</strong></span></span><br/></td>
<td><span data-ttu-id="1e290-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="1e290-127">xs:string</span></span><br/></td>
<td><span data-ttu-id="1e290-128">No</span><span class="sxs-lookup"><span data-stu-id="1e290-128">No</span></span><br/></td>
<td><span data-ttu-id="1e290-129">字串，表示 command 元素的鍵盤快速鍵。</span><span class="sxs-lookup"><span data-stu-id="1e290-129">A string that represents the keyboard shortcut of a command element.</span></span><br/> <br/><span data-ttu-id="1e290-130">
<dt><span></span><span></span><strong></strong> (xs： string) </span><span class="sxs-lookup"><span data-stu-id="1e290-130">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="1e290-131">由任何字元序列組成的字串，包含空白字元。</span><span class="sxs-lookup"><span data-stu-id="1e290-131">A string composed of any sequence of characters, including white space.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1e290-132"><strong>LabelDescription</strong></span><span class="sxs-lookup"><span data-stu-id="1e290-132"><strong>LabelDescription</strong></span></span><br/></td>
<td><span data-ttu-id="1e290-133">xs:string</span><span class="sxs-lookup"><span data-stu-id="1e290-133">xs:string</span></span><br/></td>
<td><span data-ttu-id="1e290-134">No</span><span class="sxs-lookup"><span data-stu-id="1e290-134">No</span></span><br/></td>
<td><span data-ttu-id="1e290-135">字串，表示命令元素上顯示的文字。</span><span class="sxs-lookup"><span data-stu-id="1e290-135">A string that represents the text displayed on a command element.</span></span><br/> <br/><span data-ttu-id="1e290-136">
<dt><span></span><span></span><strong></strong> (xs： string) </span><span class="sxs-lookup"><span data-stu-id="1e290-136">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="1e290-137">由任何字元序列組成的字串，包括空白字元和分行符號字元。</span><span class="sxs-lookup"><span data-stu-id="1e290-137">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1e290-138"><strong>LabelTitle</strong></span><span class="sxs-lookup"><span data-stu-id="1e290-138"><strong>LabelTitle</strong></span></span><br/></td>
<td><span data-ttu-id="1e290-139">xs:string</span><span class="sxs-lookup"><span data-stu-id="1e290-139">xs:string</span></span><br/></td>
<td><span data-ttu-id="1e290-140">No</span><span class="sxs-lookup"><span data-stu-id="1e290-140">No</span></span><br/></td>
<td><span data-ttu-id="1e290-141">字串，表示命令元素上顯示的文字。</span><span class="sxs-lookup"><span data-stu-id="1e290-141">A string that represents the text displayed on a command element.</span></span><br/> <br/><span data-ttu-id="1e290-142">
<dt><span></span><span></span><strong></strong> (xs： string) </span><span class="sxs-lookup"><span data-stu-id="1e290-142">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="1e290-143">由任何字元序列組成的字串，包括空白字元和分行符號字元。</span><span class="sxs-lookup"><span data-stu-id="1e290-143">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1e290-144"><strong>名稱</strong></span><span class="sxs-lookup"><span data-stu-id="1e290-144"><strong>Name</strong></span></span><br/></td>
<td><span data-ttu-id="1e290-145">xs:string</span><span class="sxs-lookup"><span data-stu-id="1e290-145">xs:string</span></span><br/></td>
<td><span data-ttu-id="1e290-146">No</span><span class="sxs-lookup"><span data-stu-id="1e290-146">No</span></span><br/></td>
<td><span data-ttu-id="1e290-147"><dt><span></span><span></span><strong></strong> (xs： string) </span><span class="sxs-lookup"><span data-stu-id="1e290-147"><dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="1e290-148">包含字母或底線的字串，後面接著任何數位、字母或底線序列。</span><span class="sxs-lookup"><span data-stu-id="1e290-148">A string that consists of a letter or underscore followed by any sequence of digits, letters, or underscores.</span></span><br/> <span data-ttu-id="1e290-149">最大長度：100個字元。</span><span class="sxs-lookup"><span data-stu-id="1e290-149">Maximum length: 100 characters.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1e290-150"><strong>符號</strong></span><span class="sxs-lookup"><span data-stu-id="1e290-150"><strong>Symbol</strong></span></span><br/></td>
<td><span data-ttu-id="1e290-151">xs:string</span><span class="sxs-lookup"><span data-stu-id="1e290-151">xs:string</span></span><br/></td>
<td><span data-ttu-id="1e290-152">No</span><span class="sxs-lookup"><span data-stu-id="1e290-152">No</span></span><br/></td>
<td><span data-ttu-id="1e290-153"><dt><span></span><span></span><strong></strong> (xs： string) </span><span class="sxs-lookup"><span data-stu-id="1e290-153"><dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="1e290-154">包含字母或底線的字串，後面接著任何數位、字母或底線序列。</span><span class="sxs-lookup"><span data-stu-id="1e290-154">A string that consists of a letter or underscore followed by any sequence of digits, letters, or underscores.</span></span><br/> <span data-ttu-id="1e290-155">最大長度：100個字元。</span><span class="sxs-lookup"><span data-stu-id="1e290-155">Maximum length: 100 characters.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1e290-156"><strong>TooltipDescription</strong></span><span class="sxs-lookup"><span data-stu-id="1e290-156"><strong>TooltipDescription</strong></span></span><br/></td>
<td><span data-ttu-id="1e290-157">xs:string</span><span class="sxs-lookup"><span data-stu-id="1e290-157">xs:string</span></span><br/></td>
<td><span data-ttu-id="1e290-158">No</span><span class="sxs-lookup"><span data-stu-id="1e290-158">No</span></span><br/></td>
<td><span data-ttu-id="1e290-159">字串，表示命令元素上顯示的文字。</span><span class="sxs-lookup"><span data-stu-id="1e290-159">A string that represents the text displayed on a command element.</span></span><br/> <br/><span data-ttu-id="1e290-160">
<dt><span></span><span></span><strong></strong> (xs： string) </span><span class="sxs-lookup"><span data-stu-id="1e290-160">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="1e290-161">由任何字元序列組成的字串，包括空白字元和分行符號字元。</span><span class="sxs-lookup"><span data-stu-id="1e290-161">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1e290-162"><strong>TooltipTitle</strong></span><span class="sxs-lookup"><span data-stu-id="1e290-162"><strong>TooltipTitle</strong></span></span><br/></td>
<td><span data-ttu-id="1e290-163">xs:string</span><span class="sxs-lookup"><span data-stu-id="1e290-163">xs:string</span></span><br/></td>
<td><span data-ttu-id="1e290-164">No</span><span class="sxs-lookup"><span data-stu-id="1e290-164">No</span></span><br/></td>
<td><span data-ttu-id="1e290-165">字串，表示命令元素上顯示的文字。</span><span class="sxs-lookup"><span data-stu-id="1e290-165">A string that represents the text displayed on a command element.</span></span><br/> <br/><span data-ttu-id="1e290-166">
<dt><span></span><span></span><strong></strong> (xs： string) </span><span class="sxs-lookup"><span data-stu-id="1e290-166">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="1e290-167">由任何字元序列組成的字串，包括空白字元和分行符號字元。</span><span class="sxs-lookup"><span data-stu-id="1e290-167">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="1e290-168">子元素</span><span class="sxs-lookup"><span data-stu-id="1e290-168">Child elements</span></span>



| <span data-ttu-id="1e290-169">元素</span><span class="sxs-lookup"><span data-stu-id="1e290-169">Element</span></span>                                                                                                     | <span data-ttu-id="1e290-170">描述</span><span class="sxs-lookup"><span data-stu-id="1e290-170">Description</span></span>                                   |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="1e290-171">**命令。批註**</span><span class="sxs-lookup"><span data-stu-id="1e290-171">**Command.Comment**</span></span>](windowsribbon-element-command-comment.md)<br/>                                 | <span data-ttu-id="1e290-172">最多可能發生一次</span><span class="sxs-lookup"><span data-stu-id="1e290-172">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="1e290-173">**Command.Id**</span><span class="sxs-lookup"><span data-stu-id="1e290-173">**Command.Id**</span></span>](windowsribbon-element-command-id.md)<br/>                                           | <span data-ttu-id="1e290-174">最多可能發生一次</span><span class="sxs-lookup"><span data-stu-id="1e290-174">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="1e290-175">**命令。快速鍵**</span><span class="sxs-lookup"><span data-stu-id="1e290-175">**Command.Keytip**</span></span>](windowsribbon-element-command-keytip.md)<br/>                                   | <span data-ttu-id="1e290-176">最多可能發生一次</span><span class="sxs-lookup"><span data-stu-id="1e290-176">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="1e290-177">**LabelDescription**</span><span class="sxs-lookup"><span data-stu-id="1e290-177">**Command.LabelDescription**</span></span>](windowsribbon-element-command-labeldescription.md)<br/>               | <span data-ttu-id="1e290-178">最多可能發生一次</span><span class="sxs-lookup"><span data-stu-id="1e290-178">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="1e290-179">**LabelTitle**</span><span class="sxs-lookup"><span data-stu-id="1e290-179">**Command.LabelTitle**</span></span>](windowsribbon-element-command-labeltitle.md)<br/>                           | <span data-ttu-id="1e290-180">最多可能發生一次</span><span class="sxs-lookup"><span data-stu-id="1e290-180">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="1e290-181">**LargeHighContrastImages**</span><span class="sxs-lookup"><span data-stu-id="1e290-181">**Command.LargeHighContrastImages**</span></span>](windowsribbon-element-command-largehighcontrastimages.md)<br/> | <span data-ttu-id="1e290-182">最多可能發生一次</span><span class="sxs-lookup"><span data-stu-id="1e290-182">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="1e290-183">**LargeImages**</span><span class="sxs-lookup"><span data-stu-id="1e290-183">**Command.LargeImages**</span></span>](windowsribbon-element-command-largeimages.md)<br/>                         | <span data-ttu-id="1e290-184">最多可能發生一次</span><span class="sxs-lookup"><span data-stu-id="1e290-184">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="1e290-185">**Command.Name**</span><span class="sxs-lookup"><span data-stu-id="1e290-185">**Command.Name**</span></span>](windowsribbon-element-command-name.md)<br/>                                       | <span data-ttu-id="1e290-186">最多可能發生一次</span><span class="sxs-lookup"><span data-stu-id="1e290-186">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="1e290-187">**SmallHighContrastImages**</span><span class="sxs-lookup"><span data-stu-id="1e290-187">**Command.SmallHighContrastImages**</span></span>](windowsribbon-element-command-smallhighcontrastimages.md)<br/> | <span data-ttu-id="1e290-188">最多可能發生一次</span><span class="sxs-lookup"><span data-stu-id="1e290-188">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="1e290-189">**SmallImages**</span><span class="sxs-lookup"><span data-stu-id="1e290-189">**Command.SmallImages**</span></span>](windowsribbon-element-command-smallimages.md)<br/>                         | <span data-ttu-id="1e290-190">最多可能發生一次</span><span class="sxs-lookup"><span data-stu-id="1e290-190">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="1e290-191">**命令。符號**</span><span class="sxs-lookup"><span data-stu-id="1e290-191">**Command.Symbol**</span></span>](windowsribbon-element-command-symbol.md)<br/>                                   | <span data-ttu-id="1e290-192">最多可能發生一次</span><span class="sxs-lookup"><span data-stu-id="1e290-192">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="1e290-193">**TooltipDescription**</span><span class="sxs-lookup"><span data-stu-id="1e290-193">**Command.TooltipDescription**</span></span>](windowsribbon-element-command-tooltipdescription.md)<br/>           | <span data-ttu-id="1e290-194">最多可能發生一次</span><span class="sxs-lookup"><span data-stu-id="1e290-194">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="1e290-195">**TooltipTitle**</span><span class="sxs-lookup"><span data-stu-id="1e290-195">**Command.TooltipTitle**</span></span>](windowsribbon-element-command-tooltiptitle.md)<br/>                       | <span data-ttu-id="1e290-196">最多可能發生一次</span><span class="sxs-lookup"><span data-stu-id="1e290-196">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="1e290-197">父元素</span><span class="sxs-lookup"><span data-stu-id="1e290-197">Parent elements</span></span>



| <span data-ttu-id="1e290-198">元素</span><span class="sxs-lookup"><span data-stu-id="1e290-198">Element</span></span>                                                                               |
|---------------------------------------------------------------------------------------|
| [<span data-ttu-id="1e290-199">**應用程式。命令**</span><span class="sxs-lookup"><span data-stu-id="1e290-199">**Application.Commands**</span></span>](windowsribbon-element-application-commands.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="1e290-200">備註</span><span class="sxs-lookup"><span data-stu-id="1e290-200">Remarks</span></span>

<span data-ttu-id="1e290-201">必要。</span><span class="sxs-lookup"><span data-stu-id="1e290-201">Required.</span></span>

<span data-ttu-id="1e290-202">每個應用程式都可能會發生一次或多次 [**。命令**](windowsribbon-element-application-commands.md) 元素。</span><span class="sxs-lookup"><span data-stu-id="1e290-202">May occur one or more times for each [**Application.Commands**](windowsribbon-element-application-commands.md) element.</span></span>

<span data-ttu-id="1e290-203">**Command** 元素的子項目可能會以任何順序出現。</span><span class="sxs-lookup"><span data-stu-id="1e290-203">The child elements of the **Command** element may occur in any order.</span></span>

<span data-ttu-id="1e290-204">通常，命令資源是在功能區標記中宣告，但也可以在執行時間透過呼叫 [**SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty)來設定。</span><span class="sxs-lookup"><span data-stu-id="1e290-204">Typically, Command resources are declared in Ribbon markup, but they can also be set at run time with a call to [**SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).</span></span> <span data-ttu-id="1e290-205">例如，您可以設定命令的 [UI \_ PKEY \_ Keytip](windowsribbon-reference-properties-uipkey-keytip.md) 屬性，而不是使用 [**命令提示**](windowsribbon-element-command-keytip.md) 專案專案在標記中宣告值。</span><span class="sxs-lookup"><span data-stu-id="1e290-205">For example, it is possible to set the [UI\_PKEY\_Keytip](windowsribbon-reference-properties-uipkey-keytip.md) property for a Command instead of declaring a value in markup with the [**Command.Keytip**](windowsribbon-element-command-keytip.md) element.</span></span>

<span data-ttu-id="1e290-206">如果無法使用 [**SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) 設定命令屬性，例如標籤和影像，它們可能會在呼叫 [**InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand)時失效。</span><span class="sxs-lookup"><span data-stu-id="1e290-206">In cases where Command properties, such as labels and images, cannot be set with [**SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) they can be invalidated with a call to [**InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand).</span></span> <span data-ttu-id="1e290-207">在失效之後，架構會查詢主機應用程式中的資源詳細資料。</span><span class="sxs-lookup"><span data-stu-id="1e290-207">After invalidation, the framework queries the host application for the resource details.</span></span>

> [!Note]  
> <span data-ttu-id="1e290-208">無法從標記資源資料表復原資源，之後便無法復原。</span><span class="sxs-lookup"><span data-stu-id="1e290-208">A resource cannot be reinstated from the markup resource table after it has been invalidated.</span></span>

 

<span data-ttu-id="1e290-209">在標記中宣告的每個 **命令** 的功能區標記標頭檔中，都會加入一個命令定義。</span><span class="sxs-lookup"><span data-stu-id="1e290-209">A Command definition is added to the Ribbon markup header file for each **Command** declared in markup.</span></span>

<span data-ttu-id="1e290-210">*快速鍵* 的值會作為命令的鍵盤快速鍵，除非該命令是透過功能表項目公開。</span><span class="sxs-lookup"><span data-stu-id="1e290-210">The value of *Keytip* acts as the keyboard accelerator for a Command unless that Command is exposed through a menu item.</span></span> <span data-ttu-id="1e290-211">在這種情況下，架構會忽略 *Keytip* 值，並改為使用 *LabelTitle* 或 [UI \_ PKEY \_ 標籤](windowsribbon-reference-properties-uipkey-label.md)所指定的符號前面加上連字號。</span><span class="sxs-lookup"><span data-stu-id="1e290-211">In this case, the framework ignores the *Keytip* value and instead uses a character preceded by an ampersand as specified by *LabelTitle* or [UI\_PKEY\_Label](windowsribbon-reference-properties-uipkey-label.md).</span></span> <span data-ttu-id="1e290-212">如果 *LabelTitle* 或 UI PKEY 標籤未指定任何 & 符號 \_ \_ ，則不會公開任何快捷方式或鍵盤快速鍵。</span><span class="sxs-lookup"><span data-stu-id="1e290-212">If no ampersand is specified by *LabelTitle* or UI\_PKEY\_Label, no keytip or keyboard accelerator is exposed.</span></span>

## <a name="examples"></a><span data-ttu-id="1e290-213">範例</span><span class="sxs-lookup"><span data-stu-id="1e290-213">Examples</span></span>

<span data-ttu-id="1e290-214">下列範例顯示 [**首頁**] 索引標籤的 **命令** 專案資訊清單。</span><span class="sxs-lookup"><span data-stu-id="1e290-214">The following example shows a manifest of **Command** elements for a **Home** tab.</span></span>


```XML
<Application.Commands>
```




```XML
<Command Name="cmdHomeTab"
         LabelTitle="Home"
         Keytip="H" />
<Command Name="cmdClipboardGroup"
         Symbol="IDR_CMD_CLIPBOARD"
         Id="10000"
         Comment="Command definition for clipboard group"
         LabelTitle="Clipboard"
         Keytip="CB" />
<Command Name="cmdCopy"
         Symbol="IDR_CMD_COPY"
         LabelTitle="Copy"
         LabelDescription="Copy"
         Keytip="C"
         TooltipTitle="Copy"
         TooltipDescription="Click to copy">
  <Command.SmallImages>
    <Image>res/copyS_16.bmp</Image>
  </Command.SmallImages>
  <Command.LargeImages>
    <Image>res/copyL_32.bmp</Image>
  </Command.LargeImages>
</Command>
<Command Name="cmdPaste"
         Symbol="IDR_CMD_PASTE" >
  <Command.LabelTitle>Paste</Command.LabelTitle>
  <Command.LabelDescription>
    <String Content="Paste contents of clipboard"
            Id="10001"
            Symbol="IDR_RES_LABELDESC_PASTE" />
  </Command.LabelDescription>
  <Command.Keytip>P</Command.Keytip>
  <Command.TooltipTitle>
    <String Content="Paste contents of clipboard"
            Id="10002"
            Symbol="IDR_RES_TOOLTIP_PASTE"/>
  </Command.TooltipTitle>
  <Command.TooltipDescription>
    <String Content="Click to paste contents of clipboard"/>
  </Command.TooltipDescription>
  <Command.SmallImages>
    <Image
      Id="10010"
      MinDPI="96"
      Symbol="IDR_RES_SMALL_IMAGE96">
      <Image.Source>res/pasteS_96bpp.bmp</Image.Source>
    </Image>
    <Image Source="res/pasteS_120bpp.bmp"
           Id="10011"
           MinDPI="120"
           Symbol="IDR_RES_SMALL_IMAGE120" />
  </Command.SmallImages>
  <Command.LargeImages>
    <Image>res/pasteL_32.bmp</Image>
  </Command.LargeImages>
</Command>
<Command Name="cmdMinimize"
         Symbol="IDR_CMD_MINIMIZE"
         Id="10001"
         LabelTitle="Minimize" />
```




```XML
</Application.Commands>
```



## <a name="element-information"></a><span data-ttu-id="1e290-215">項目資訊</span><span class="sxs-lookup"><span data-stu-id="1e290-215">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="1e290-216">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="1e290-216">Minimum supported system</span></span><br/> | <span data-ttu-id="1e290-217">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1e290-217">Windows 7</span></span> |
| <span data-ttu-id="1e290-218">可以是空的</span><span class="sxs-lookup"><span data-stu-id="1e290-218">Can be empty</span></span>                        | <span data-ttu-id="1e290-219">否</span><span class="sxs-lookup"><span data-stu-id="1e290-219">No</span></span>        |



 


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
ms.openlocfilehash: 1e1df5b62c7b2d7c55345ba8d6da366d04697054
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443479"
---
# <a name="command-element"></a><span data-ttu-id="eda30-104">Command 元素</span><span class="sxs-lookup"><span data-stu-id="eda30-104">Command element</span></span>

<span data-ttu-id="eda30-105">表示命令定義。</span><span class="sxs-lookup"><span data-stu-id="eda30-105">Represents a Command definition.</span></span>

## <a name="usage"></a><span data-ttu-id="eda30-106">使用方式</span><span class="sxs-lookup"><span data-stu-id="eda30-106">Usage</span></span>

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

## <a name="attributes"></a><span data-ttu-id="eda30-107">屬性</span><span class="sxs-lookup"><span data-stu-id="eda30-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="eda30-108">屬性</span><span class="sxs-lookup"><span data-stu-id="eda30-108">Attribute</span></span></th>
<th><span data-ttu-id="eda30-109">類型</span><span class="sxs-lookup"><span data-stu-id="eda30-109">Type</span></span></th>
<th><span data-ttu-id="eda30-110">必要</span><span class="sxs-lookup"><span data-stu-id="eda30-110">Required</span></span></th>
<th><span data-ttu-id="eda30-111">描述</span><span class="sxs-lookup"><span data-stu-id="eda30-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="eda30-112"><strong>註解</strong></span><span class="sxs-lookup"><span data-stu-id="eda30-112"><strong>Comment</strong></span></span><br/></td>
<td><span data-ttu-id="eda30-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="eda30-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="eda30-114">否</span><span class="sxs-lookup"><span data-stu-id="eda30-114">No</span></span><br/></td>
<td><span data-ttu-id="eda30-115">用來批註命令元素。</span><span class="sxs-lookup"><span data-stu-id="eda30-115">Used to annotate the command element.</span></span><br/> <br/><span data-ttu-id="eda30-116">
<dt><span></span><span></span><strong></strong> (xs： string) </span><span class="sxs-lookup"><span data-stu-id="eda30-116">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="eda30-117">由任何字元序列組成的字串，包括空白字元和分行符號字元。</span><span class="sxs-lookup"><span data-stu-id="eda30-117">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> <span data-ttu-id="eda30-118">最大長度：250個字元。</span><span class="sxs-lookup"><span data-stu-id="eda30-118">Maximum length: 250 characters.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eda30-119"><strong>識別碼</strong></span><span class="sxs-lookup"><span data-stu-id="eda30-119"><strong>Id</strong></span></span><br/></td>
<td><span data-ttu-id="eda30-120">xs： positiveInteger union xs： string</span><span class="sxs-lookup"><span data-stu-id="eda30-120">xs:positiveInteger union xs:string</span></span><br/></td>
<td><span data-ttu-id="eda30-121">否</span><span class="sxs-lookup"><span data-stu-id="eda30-121">No</span></span><br/></td>
<td><span data-ttu-id="eda30-122">唯一的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="eda30-122">The unique resource ID.</span></span> <br/> <br/><span data-ttu-id="eda30-123">
<dt><span></span><span></span><strong></strong> (xs： positiveInteger 和 xs： string 的聯集) </span><span class="sxs-lookup"><span data-stu-id="eda30-123">
<dt><span></span><span></span><strong></strong> (The union of xs:positiveInteger and xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="eda30-124">介於2和59999（含）之間的整數值，或以十六進位（含）表示的0xea5f。</span><span class="sxs-lookup"><span data-stu-id="eda30-124">An integer value between 2 and 59999, inclusive, or 0x2 and 0xea5f in hexadecimal, inclusive.</span></span> <br/> <span data-ttu-id="eda30-125">最大長度為10個字元，包括選擇性前置零。</span><span class="sxs-lookup"><span data-stu-id="eda30-125">Maximum length is 10 characters, including optional leading zeros.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eda30-126"><strong>Keytip</strong></span><span class="sxs-lookup"><span data-stu-id="eda30-126"><strong>Keytip</strong></span></span><br/></td>
<td><span data-ttu-id="eda30-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="eda30-127">xs:string</span></span><br/></td>
<td><span data-ttu-id="eda30-128">否</span><span class="sxs-lookup"><span data-stu-id="eda30-128">No</span></span><br/></td>
<td><span data-ttu-id="eda30-129">字串，表示 command 元素的鍵盤快速鍵。</span><span class="sxs-lookup"><span data-stu-id="eda30-129">A string that represents the keyboard shortcut of a command element.</span></span><br/> <br/><span data-ttu-id="eda30-130">
<dt><span></span><span></span><strong></strong> (xs： string) </span><span class="sxs-lookup"><span data-stu-id="eda30-130">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="eda30-131">由任何字元序列組成的字串，包含空白字元。</span><span class="sxs-lookup"><span data-stu-id="eda30-131">A string composed of any sequence of characters, including white space.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eda30-132"><strong>LabelDescription</strong></span><span class="sxs-lookup"><span data-stu-id="eda30-132"><strong>LabelDescription</strong></span></span><br/></td>
<td><span data-ttu-id="eda30-133">xs:string</span><span class="sxs-lookup"><span data-stu-id="eda30-133">xs:string</span></span><br/></td>
<td><span data-ttu-id="eda30-134">否</span><span class="sxs-lookup"><span data-stu-id="eda30-134">No</span></span><br/></td>
<td><span data-ttu-id="eda30-135">字串，表示命令元素上顯示的文字。</span><span class="sxs-lookup"><span data-stu-id="eda30-135">A string that represents the text displayed on a command element.</span></span><br/> <br/><span data-ttu-id="eda30-136">
<dt><span></span><span></span><strong></strong> (xs： string) </span><span class="sxs-lookup"><span data-stu-id="eda30-136">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="eda30-137">由任何字元序列組成的字串，包括空白字元和分行符號字元。</span><span class="sxs-lookup"><span data-stu-id="eda30-137">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eda30-138"><strong>LabelTitle</strong></span><span class="sxs-lookup"><span data-stu-id="eda30-138"><strong>LabelTitle</strong></span></span><br/></td>
<td><span data-ttu-id="eda30-139">xs:string</span><span class="sxs-lookup"><span data-stu-id="eda30-139">xs:string</span></span><br/></td>
<td><span data-ttu-id="eda30-140">否</span><span class="sxs-lookup"><span data-stu-id="eda30-140">No</span></span><br/></td>
<td><span data-ttu-id="eda30-141">字串，表示命令元素上顯示的文字。</span><span class="sxs-lookup"><span data-stu-id="eda30-141">A string that represents the text displayed on a command element.</span></span><br/> <br/><span data-ttu-id="eda30-142">
<dt><span></span><span></span><strong></strong> (xs： string) </span><span class="sxs-lookup"><span data-stu-id="eda30-142">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="eda30-143">由任何字元序列組成的字串，包括空白字元和分行符號字元。</span><span class="sxs-lookup"><span data-stu-id="eda30-143">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eda30-144"><strong>名稱</strong></span><span class="sxs-lookup"><span data-stu-id="eda30-144"><strong>Name</strong></span></span><br/></td>
<td><span data-ttu-id="eda30-145">xs:string</span><span class="sxs-lookup"><span data-stu-id="eda30-145">xs:string</span></span><br/></td>
<td><span data-ttu-id="eda30-146">否</span><span class="sxs-lookup"><span data-stu-id="eda30-146">No</span></span><br/></td>
<td><span data-ttu-id="eda30-147"><dt><span></span><span></span><strong></strong> (xs： string) </span><span class="sxs-lookup"><span data-stu-id="eda30-147"><dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="eda30-148">包含字母或底線的字串，後面接著任何數位、字母或底線序列。</span><span class="sxs-lookup"><span data-stu-id="eda30-148">A string that consists of a letter or underscore followed by any sequence of digits, letters, or underscores.</span></span><br/> <span data-ttu-id="eda30-149">最大長度：100個字元。</span><span class="sxs-lookup"><span data-stu-id="eda30-149">Maximum length: 100 characters.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eda30-150"><strong>符號</strong></span><span class="sxs-lookup"><span data-stu-id="eda30-150"><strong>Symbol</strong></span></span><br/></td>
<td><span data-ttu-id="eda30-151">xs:string</span><span class="sxs-lookup"><span data-stu-id="eda30-151">xs:string</span></span><br/></td>
<td><span data-ttu-id="eda30-152">否</span><span class="sxs-lookup"><span data-stu-id="eda30-152">No</span></span><br/></td>
<td><span data-ttu-id="eda30-153"><dt><span></span><span></span><strong></strong> (xs： string) </span><span class="sxs-lookup"><span data-stu-id="eda30-153"><dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="eda30-154">包含字母或底線的字串，後面接著任何數位、字母或底線序列。</span><span class="sxs-lookup"><span data-stu-id="eda30-154">A string that consists of a letter or underscore followed by any sequence of digits, letters, or underscores.</span></span><br/> <span data-ttu-id="eda30-155">最大長度：100個字元。</span><span class="sxs-lookup"><span data-stu-id="eda30-155">Maximum length: 100 characters.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eda30-156"><strong>TooltipDescription</strong></span><span class="sxs-lookup"><span data-stu-id="eda30-156"><strong>TooltipDescription</strong></span></span><br/></td>
<td><span data-ttu-id="eda30-157">xs:string</span><span class="sxs-lookup"><span data-stu-id="eda30-157">xs:string</span></span><br/></td>
<td><span data-ttu-id="eda30-158">否</span><span class="sxs-lookup"><span data-stu-id="eda30-158">No</span></span><br/></td>
<td><span data-ttu-id="eda30-159">字串，表示命令元素上顯示的文字。</span><span class="sxs-lookup"><span data-stu-id="eda30-159">A string that represents the text displayed on a command element.</span></span><br/> <br/><span data-ttu-id="eda30-160">
<dt><span></span><span></span><strong></strong> (xs： string) </span><span class="sxs-lookup"><span data-stu-id="eda30-160">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="eda30-161">由任何字元序列組成的字串，包括空白字元和分行符號字元。</span><span class="sxs-lookup"><span data-stu-id="eda30-161">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eda30-162"><strong>TooltipTitle</strong></span><span class="sxs-lookup"><span data-stu-id="eda30-162"><strong>TooltipTitle</strong></span></span><br/></td>
<td><span data-ttu-id="eda30-163">xs:string</span><span class="sxs-lookup"><span data-stu-id="eda30-163">xs:string</span></span><br/></td>
<td><span data-ttu-id="eda30-164">否</span><span class="sxs-lookup"><span data-stu-id="eda30-164">No</span></span><br/></td>
<td><span data-ttu-id="eda30-165">字串，表示命令元素上顯示的文字。</span><span class="sxs-lookup"><span data-stu-id="eda30-165">A string that represents the text displayed on a command element.</span></span><br/> <br/><span data-ttu-id="eda30-166">
<dt><span></span><span></span><strong></strong> (xs： string) </span><span class="sxs-lookup"><span data-stu-id="eda30-166">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="eda30-167">由任何字元序列組成的字串，包括空白字元和分行符號字元。</span><span class="sxs-lookup"><span data-stu-id="eda30-167">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="eda30-168">子元素</span><span class="sxs-lookup"><span data-stu-id="eda30-168">Child elements</span></span>



| <span data-ttu-id="eda30-169">元素</span><span class="sxs-lookup"><span data-stu-id="eda30-169">Element</span></span>                                                                                                     | <span data-ttu-id="eda30-170">描述</span><span class="sxs-lookup"><span data-stu-id="eda30-170">Description</span></span>                                   |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="eda30-171">**命令。批註**</span><span class="sxs-lookup"><span data-stu-id="eda30-171">**Command.Comment**</span></span>](windowsribbon-element-command-comment.md)<br/>                                 | <span data-ttu-id="eda30-172">最多可能發生一次</span><span class="sxs-lookup"><span data-stu-id="eda30-172">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="eda30-173">**Command.Id**</span><span class="sxs-lookup"><span data-stu-id="eda30-173">**Command.Id**</span></span>](windowsribbon-element-command-id.md)<br/>                                           | <span data-ttu-id="eda30-174">最多可能發生一次</span><span class="sxs-lookup"><span data-stu-id="eda30-174">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="eda30-175">**命令。快速鍵**</span><span class="sxs-lookup"><span data-stu-id="eda30-175">**Command.Keytip**</span></span>](windowsribbon-element-command-keytip.md)<br/>                                   | <span data-ttu-id="eda30-176">最多可能發生一次</span><span class="sxs-lookup"><span data-stu-id="eda30-176">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="eda30-177">**LabelDescription**</span><span class="sxs-lookup"><span data-stu-id="eda30-177">**Command.LabelDescription**</span></span>](windowsribbon-element-command-labeldescription.md)<br/>               | <span data-ttu-id="eda30-178">最多可能發生一次</span><span class="sxs-lookup"><span data-stu-id="eda30-178">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="eda30-179">**LabelTitle**</span><span class="sxs-lookup"><span data-stu-id="eda30-179">**Command.LabelTitle**</span></span>](windowsribbon-element-command-labeltitle.md)<br/>                           | <span data-ttu-id="eda30-180">最多可能發生一次</span><span class="sxs-lookup"><span data-stu-id="eda30-180">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="eda30-181">**LargeHighContrastImages**</span><span class="sxs-lookup"><span data-stu-id="eda30-181">**Command.LargeHighContrastImages**</span></span>](windowsribbon-element-command-largehighcontrastimages.md)<br/> | <span data-ttu-id="eda30-182">最多可能發生一次</span><span class="sxs-lookup"><span data-stu-id="eda30-182">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="eda30-183">**LargeImages**</span><span class="sxs-lookup"><span data-stu-id="eda30-183">**Command.LargeImages**</span></span>](windowsribbon-element-command-largeimages.md)<br/>                         | <span data-ttu-id="eda30-184">最多可能發生一次</span><span class="sxs-lookup"><span data-stu-id="eda30-184">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="eda30-185">**Command.Name**</span><span class="sxs-lookup"><span data-stu-id="eda30-185">**Command.Name**</span></span>](windowsribbon-element-command-name.md)<br/>                                       | <span data-ttu-id="eda30-186">最多可能發生一次</span><span class="sxs-lookup"><span data-stu-id="eda30-186">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="eda30-187">**SmallHighContrastImages**</span><span class="sxs-lookup"><span data-stu-id="eda30-187">**Command.SmallHighContrastImages**</span></span>](windowsribbon-element-command-smallhighcontrastimages.md)<br/> | <span data-ttu-id="eda30-188">最多可能發生一次</span><span class="sxs-lookup"><span data-stu-id="eda30-188">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="eda30-189">**SmallImages**</span><span class="sxs-lookup"><span data-stu-id="eda30-189">**Command.SmallImages**</span></span>](windowsribbon-element-command-smallimages.md)<br/>                         | <span data-ttu-id="eda30-190">最多可能發生一次</span><span class="sxs-lookup"><span data-stu-id="eda30-190">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="eda30-191">**命令。符號**</span><span class="sxs-lookup"><span data-stu-id="eda30-191">**Command.Symbol**</span></span>](windowsribbon-element-command-symbol.md)<br/>                                   | <span data-ttu-id="eda30-192">最多可能發生一次</span><span class="sxs-lookup"><span data-stu-id="eda30-192">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="eda30-193">**TooltipDescription**</span><span class="sxs-lookup"><span data-stu-id="eda30-193">**Command.TooltipDescription**</span></span>](windowsribbon-element-command-tooltipdescription.md)<br/>           | <span data-ttu-id="eda30-194">最多可能發生一次</span><span class="sxs-lookup"><span data-stu-id="eda30-194">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="eda30-195">**TooltipTitle**</span><span class="sxs-lookup"><span data-stu-id="eda30-195">**Command.TooltipTitle**</span></span>](windowsribbon-element-command-tooltiptitle.md)<br/>                       | <span data-ttu-id="eda30-196">最多可能發生一次</span><span class="sxs-lookup"><span data-stu-id="eda30-196">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="eda30-197">父元素</span><span class="sxs-lookup"><span data-stu-id="eda30-197">Parent elements</span></span>



| <span data-ttu-id="eda30-198">元素</span><span class="sxs-lookup"><span data-stu-id="eda30-198">Element</span></span>                                                                               |
|---------------------------------------------------------------------------------------|
| [<span data-ttu-id="eda30-199">**應用程式。命令**</span><span class="sxs-lookup"><span data-stu-id="eda30-199">**Application.Commands**</span></span>](windowsribbon-element-application-commands.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="eda30-200">備註</span><span class="sxs-lookup"><span data-stu-id="eda30-200">Remarks</span></span>

<span data-ttu-id="eda30-201">必要。</span><span class="sxs-lookup"><span data-stu-id="eda30-201">Required.</span></span>

<span data-ttu-id="eda30-202">每個應用程式都可能會發生一次或多次 [**。命令**](windowsribbon-element-application-commands.md) 元素。</span><span class="sxs-lookup"><span data-stu-id="eda30-202">May occur one or more times for each [**Application.Commands**](windowsribbon-element-application-commands.md) element.</span></span>

<span data-ttu-id="eda30-203">**Command** 元素的子項目可能會以任何順序出現。</span><span class="sxs-lookup"><span data-stu-id="eda30-203">The child elements of the **Command** element may occur in any order.</span></span>

<span data-ttu-id="eda30-204">通常，命令資源是在功能區標記中宣告，但也可以在執行時間透過呼叫 [**SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty)來設定。</span><span class="sxs-lookup"><span data-stu-id="eda30-204">Typically, Command resources are declared in Ribbon markup, but they can also be set at run time with a call to [**SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).</span></span> <span data-ttu-id="eda30-205">例如，您可以設定命令的 [UI \_ PKEY \_ Keytip](windowsribbon-reference-properties-uipkey-keytip.md) 屬性，而不是使用 [**命令提示**](windowsribbon-element-command-keytip.md) 專案專案在標記中宣告值。</span><span class="sxs-lookup"><span data-stu-id="eda30-205">For example, it is possible to set the [UI\_PKEY\_Keytip](windowsribbon-reference-properties-uipkey-keytip.md) property for a Command instead of declaring a value in markup with the [**Command.Keytip**](windowsribbon-element-command-keytip.md) element.</span></span>

<span data-ttu-id="eda30-206">如果無法使用 [**SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) 設定命令屬性，例如標籤和影像，它們可能會在呼叫 [**InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand)時失效。</span><span class="sxs-lookup"><span data-stu-id="eda30-206">In cases where Command properties, such as labels and images, cannot be set with [**SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) they can be invalidated with a call to [**InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand).</span></span> <span data-ttu-id="eda30-207">在失效之後，架構會查詢主機應用程式中的資源詳細資料。</span><span class="sxs-lookup"><span data-stu-id="eda30-207">After invalidation, the framework queries the host application for the resource details.</span></span>

> [!Note]  
> <span data-ttu-id="eda30-208">無法從標記資源資料表復原資源，之後便無法復原。</span><span class="sxs-lookup"><span data-stu-id="eda30-208">A resource cannot be reinstated from the markup resource table after it has been invalidated.</span></span>

 

<span data-ttu-id="eda30-209">在標記中宣告的每個 **命令** 的功能區標記標頭檔中，都會加入一個命令定義。</span><span class="sxs-lookup"><span data-stu-id="eda30-209">A Command definition is added to the Ribbon markup header file for each **Command** declared in markup.</span></span>

<span data-ttu-id="eda30-210">*快速鍵* 的值會作為命令的鍵盤快速鍵，除非該命令是透過功能表項目公開。</span><span class="sxs-lookup"><span data-stu-id="eda30-210">The value of *Keytip* acts as the keyboard accelerator for a Command unless that Command is exposed through a menu item.</span></span> <span data-ttu-id="eda30-211">在這種情況下，架構會忽略 *Keytip* 值，並改為使用 *LabelTitle* 或 [UI \_ PKEY \_ 標籤](windowsribbon-reference-properties-uipkey-label.md)所指定的符號前面加上連字號。</span><span class="sxs-lookup"><span data-stu-id="eda30-211">In this case, the framework ignores the *Keytip* value and instead uses a character preceded by an ampersand as specified by *LabelTitle* or [UI\_PKEY\_Label](windowsribbon-reference-properties-uipkey-label.md).</span></span> <span data-ttu-id="eda30-212">如果 *LabelTitle* 或 UI PKEY 標籤未指定任何 & 符號 \_ \_ ，則不會公開任何快捷方式或鍵盤快速鍵。</span><span class="sxs-lookup"><span data-stu-id="eda30-212">If no ampersand is specified by *LabelTitle* or UI\_PKEY\_Label, no keytip or keyboard accelerator is exposed.</span></span>

## <a name="examples"></a><span data-ttu-id="eda30-213">範例</span><span class="sxs-lookup"><span data-stu-id="eda30-213">Examples</span></span>

<span data-ttu-id="eda30-214">下列範例顯示 [**首頁**] 索引標籤的 **命令** 專案資訊清單。</span><span class="sxs-lookup"><span data-stu-id="eda30-214">The following example shows a manifest of **Command** elements for a **Home** tab.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="eda30-215">項目資訊</span><span class="sxs-lookup"><span data-stu-id="eda30-215">Element information</span></span>

* <span data-ttu-id="eda30-216">**最低支援系統**： Windows 7</span><span class="sxs-lookup"><span data-stu-id="eda30-216">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="eda30-217">**可以是空** 的：否</span><span class="sxs-lookup"><span data-stu-id="eda30-217">**Can be empty**: No</span></span>



 


---
title: String 元素
description: 表示字串資源。
ms.assetid: 83e5bdbb-ef86-4942-af40-2e327360ee67
keywords:
- 字串元素視窗功能區
topic_type:
- apiref
api_name:
- String
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 577d318292081dddf4e2839967642c6115a474d6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104022534"
---
# <a name="string-element"></a><span data-ttu-id="9ca34-104">String 元素</span><span class="sxs-lookup"><span data-stu-id="9ca34-104">String element</span></span>

<span data-ttu-id="9ca34-105">表示字串資源。</span><span class="sxs-lookup"><span data-stu-id="9ca34-105">Represents a string resource.</span></span>

## <a name="usage"></a><span data-ttu-id="9ca34-106">使用方式</span><span class="sxs-lookup"><span data-stu-id="9ca34-106">Usage</span></span>

``` syntax
<String
  Content = "xs:string"
  Id = "xs:positiveInteger or xs:string"
  Symbol = "xs:string">
  child elements
</String>
```

## <a name="attributes"></a><span data-ttu-id="9ca34-107">屬性</span><span class="sxs-lookup"><span data-stu-id="9ca34-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9ca34-108">屬性</span><span class="sxs-lookup"><span data-stu-id="9ca34-108">Attribute</span></span></th>
<th><span data-ttu-id="9ca34-109">類型</span><span class="sxs-lookup"><span data-stu-id="9ca34-109">Type</span></span></th>
<th><span data-ttu-id="9ca34-110">必要</span><span class="sxs-lookup"><span data-stu-id="9ca34-110">Required</span></span></th>
<th><span data-ttu-id="9ca34-111">描述</span><span class="sxs-lookup"><span data-stu-id="9ca34-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9ca34-112"><strong>內容</strong></span><span class="sxs-lookup"><span data-stu-id="9ca34-112"><strong>Content</strong></span></span><br/></td>
<td><span data-ttu-id="9ca34-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="9ca34-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="9ca34-114">No</span><span class="sxs-lookup"><span data-stu-id="9ca34-114">No</span></span><br/></td>
<td><span data-ttu-id="9ca34-115"><dt><span></span><span></span><strong></strong> (xs： string) </span><span class="sxs-lookup"><span data-stu-id="9ca34-115"><dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="9ca34-116">由任何字元序列組成的字串，包括空白字元和分行符號字元。</span><span class="sxs-lookup"><span data-stu-id="9ca34-116">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ca34-117"><strong>識別碼</strong></span><span class="sxs-lookup"><span data-stu-id="9ca34-117"><strong>Id</strong></span></span><br/></td>
<td><span data-ttu-id="9ca34-118">xs： positiveInteger 或 xs： string</span><span class="sxs-lookup"><span data-stu-id="9ca34-118">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="9ca34-119">No</span><span class="sxs-lookup"><span data-stu-id="9ca34-119">No</span></span><br/></td>
<td><span data-ttu-id="9ca34-120">唯一的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="9ca34-120">The unique resource ID.</span></span> <br/> <br/><span data-ttu-id="9ca34-121">
<dt><span></span><span></span><strong></strong> (xs： positiveInteger 或 xs： string) </span><span class="sxs-lookup"><span data-stu-id="9ca34-121">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="9ca34-122">介於2和59999（含）之間的整數值，或以十六進位（含）表示的0xea5f。</span><span class="sxs-lookup"><span data-stu-id="9ca34-122">An integer value between 2 and 59999, inclusive, or 0x2 and 0xea5f in hexadecimal, inclusive.</span></span> <br/> <span data-ttu-id="9ca34-123">最大長度為10個字元，包括選擇性前置零。</span><span class="sxs-lookup"><span data-stu-id="9ca34-123">The maximum length is 10 characters including optional leading zeros.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ca34-124"><strong>符號</strong></span><span class="sxs-lookup"><span data-stu-id="9ca34-124"><strong>Symbol</strong></span></span><br/></td>
<td><span data-ttu-id="9ca34-125">xs:string</span><span class="sxs-lookup"><span data-stu-id="9ca34-125">xs:string</span></span><br/></td>
<td><span data-ttu-id="9ca34-126">No</span><span class="sxs-lookup"><span data-stu-id="9ca34-126">No</span></span><br/></td>
<td><span data-ttu-id="9ca34-127">字串的資源符號。</span><span class="sxs-lookup"><span data-stu-id="9ca34-127">The resource symbol for the string.</span></span><br/> <br/><span data-ttu-id="9ca34-128">
<dt><span></span><span></span><strong></strong> (xs： string) </span><span class="sxs-lookup"><span data-stu-id="9ca34-128">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="9ca34-129">字母或底線，後面接著任何一連串的字母、數位或底線。</span><span class="sxs-lookup"><span data-stu-id="9ca34-129">A letter or underscore followed by any sequence of letters, digits, or underscores.</span></span><br/> <span data-ttu-id="9ca34-130">長度上限為100個字元。</span><span class="sxs-lookup"><span data-stu-id="9ca34-130">The maximum length is 100 characters.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="9ca34-131">子元素</span><span class="sxs-lookup"><span data-stu-id="9ca34-131">Child elements</span></span>



| <span data-ttu-id="9ca34-132">元素</span><span class="sxs-lookup"><span data-stu-id="9ca34-132">Element</span></span>                                                                   | <span data-ttu-id="9ca34-133">描述</span><span class="sxs-lookup"><span data-stu-id="9ca34-133">Description</span></span>                                   |
|---------------------------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="9ca34-134">**字串。內容**</span><span class="sxs-lookup"><span data-stu-id="9ca34-134">**String.Content**</span></span>](windowsribbon-element-string-content.md)<br/> | <span data-ttu-id="9ca34-135">最多可能發生一次</span><span class="sxs-lookup"><span data-stu-id="9ca34-135">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="9ca34-136">**String.Id**</span><span class="sxs-lookup"><span data-stu-id="9ca34-136">**String.Id**</span></span>](windowsribbon-element-string-id.md)<br/>           | <span data-ttu-id="9ca34-137">最多可能發生一次</span><span class="sxs-lookup"><span data-stu-id="9ca34-137">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="9ca34-138">**字串. 符號**</span><span class="sxs-lookup"><span data-stu-id="9ca34-138">**String.Symbol**</span></span>](windowsribbon-element-string-symbol.md)<br/>   | <span data-ttu-id="9ca34-139">最多可能發生一次</span><span class="sxs-lookup"><span data-stu-id="9ca34-139">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="9ca34-140">父元素</span><span class="sxs-lookup"><span data-stu-id="9ca34-140">Parent elements</span></span>



| <span data-ttu-id="9ca34-141">元素</span><span class="sxs-lookup"><span data-stu-id="9ca34-141">Element</span></span>                                                                                           |
|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9ca34-142">**命令。快速鍵**</span><span class="sxs-lookup"><span data-stu-id="9ca34-142">**Command.Keytip**</span></span>](windowsribbon-element-command-keytip.md)<br/>                         |
| [<span data-ttu-id="9ca34-143">**LabelDescription**</span><span class="sxs-lookup"><span data-stu-id="9ca34-143">**Command.LabelDescription**</span></span>](windowsribbon-element-command-labeldescription.md)<br/>     |
| [<span data-ttu-id="9ca34-144">**LabelTitle**</span><span class="sxs-lookup"><span data-stu-id="9ca34-144">**Command.LabelTitle**</span></span>](windowsribbon-element-command-labeltitle.md)<br/>                 |
| [<span data-ttu-id="9ca34-145">**TooltipDescription**</span><span class="sxs-lookup"><span data-stu-id="9ca34-145">**Command.TooltipDescription**</span></span>](windowsribbon-element-command-tooltipdescription.md)<br/> |
| [<span data-ttu-id="9ca34-146">**TooltipTitle**</span><span class="sxs-lookup"><span data-stu-id="9ca34-146">**Command.TooltipTitle**</span></span>](windowsribbon-element-command-tooltiptitle.md)<br/>             |



## <a name="remarks"></a><span data-ttu-id="9ca34-147">備註</span><span class="sxs-lookup"><span data-stu-id="9ca34-147">Remarks</span></span>

<span data-ttu-id="9ca34-148">選擇性。</span><span class="sxs-lookup"><span data-stu-id="9ca34-148">Optional.</span></span>

<span data-ttu-id="9ca34-149">每個命令最多隻能出現一次 [**。 LabelTitle**](windowsribbon-element-command-labeltitle.md)、 [**LabelDescription**](windowsribbon-element-command-labeldescription.md)、 [**命令提示**](windowsribbon-element-command-keytip.md)、 [**命令 TooltipTitle**](windowsribbon-element-command-tooltiptitle.md)或 [**TooltipDescription**](windowsribbon-element-command-tooltipdescription.md) 元素。</span><span class="sxs-lookup"><span data-stu-id="9ca34-149">May occur at most once for each [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md), [**Command.LabelDescription**](windowsribbon-element-command-labeldescription.md), [**Command.Keytip**](windowsribbon-element-command-keytip.md), [**Command.TooltipTitle**](windowsribbon-element-command-tooltiptitle.md), or [**Command.TooltipDescription**](windowsribbon-element-command-tooltipdescription.md) element.</span></span>

<span data-ttu-id="9ca34-150">字串定義會加入至功能區標頭檔中，例如 `#define strSave 59999` 。</span><span class="sxs-lookup"><span data-stu-id="9ca34-150">The string definition is added to the Ribbon header file, for example, `#define strSave 59999`.</span></span>

<span data-ttu-id="9ca34-151">如果未宣告任何宣告，則會將字串加入功能區資源檔中的字串資料表，其中的名稱和識別碼是由功能區架構產生的。</span><span class="sxs-lookup"><span data-stu-id="9ca34-151">The string is added to a string table in the Ribbon resource file where a name and ID are generated by the Ribbon framework if none are declared.</span></span>

## <a name="examples"></a><span data-ttu-id="9ca34-152">範例</span><span class="sxs-lookup"><span data-stu-id="9ca34-152">Examples</span></span>

<span data-ttu-id="9ca34-153">下列範例示範 [**LabelTitle**](windowsribbon-element-command-labeltitle.md) 專案的標記與 **字串** 宣告。</span><span class="sxs-lookup"><span data-stu-id="9ca34-153">The following example demonstrates the markup for a [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) element with a **String** declaration.</span></span>


```XML
<Command.LabelTitle>
  <String>
    <String.Content>Label for Save</String.Content>
    <String.Id>59999</String.Id>
    <String.Symbol>strSave</String.Symbol>
  </String>
</Command.LabelTitle>
```



## <a name="element-information"></a><span data-ttu-id="9ca34-154">項目資訊</span><span class="sxs-lookup"><span data-stu-id="9ca34-154">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="9ca34-155">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="9ca34-155">Minimum supported system</span></span><br/> | <span data-ttu-id="9ca34-156">Windows 7</span><span class="sxs-lookup"><span data-stu-id="9ca34-156">Windows 7</span></span> |
| <span data-ttu-id="9ca34-157">可以是空的</span><span class="sxs-lookup"><span data-stu-id="9ca34-157">Can be empty</span></span>                        | <span data-ttu-id="9ca34-158">否</span><span class="sxs-lookup"><span data-stu-id="9ca34-158">No</span></span>        |



 

 






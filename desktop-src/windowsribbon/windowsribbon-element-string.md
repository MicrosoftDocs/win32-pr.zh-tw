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
ms.openlocfilehash: 0b0dab5d7ce1485aad5fe1e15442069c488933aa
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443899"
---
# <a name="string-element"></a><span data-ttu-id="1da49-104">String 元素</span><span class="sxs-lookup"><span data-stu-id="1da49-104">String element</span></span>

<span data-ttu-id="1da49-105">表示字串資源。</span><span class="sxs-lookup"><span data-stu-id="1da49-105">Represents a string resource.</span></span>

## <a name="usage"></a><span data-ttu-id="1da49-106">使用方式</span><span class="sxs-lookup"><span data-stu-id="1da49-106">Usage</span></span>

``` syntax
<String
  Content = "xs:string"
  Id = "xs:positiveInteger or xs:string"
  Symbol = "xs:string">
  child elements
</String>
```

## <a name="attributes"></a><span data-ttu-id="1da49-107">屬性</span><span class="sxs-lookup"><span data-stu-id="1da49-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1da49-108">屬性</span><span class="sxs-lookup"><span data-stu-id="1da49-108">Attribute</span></span></th>
<th><span data-ttu-id="1da49-109">類型</span><span class="sxs-lookup"><span data-stu-id="1da49-109">Type</span></span></th>
<th><span data-ttu-id="1da49-110">必要</span><span class="sxs-lookup"><span data-stu-id="1da49-110">Required</span></span></th>
<th><span data-ttu-id="1da49-111">描述</span><span class="sxs-lookup"><span data-stu-id="1da49-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1da49-112"><strong>內容</strong></span><span class="sxs-lookup"><span data-stu-id="1da49-112"><strong>Content</strong></span></span><br/></td>
<td><span data-ttu-id="1da49-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="1da49-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="1da49-114">否</span><span class="sxs-lookup"><span data-stu-id="1da49-114">No</span></span><br/></td>
<td><span data-ttu-id="1da49-115"><dt><span></span><span></span><strong></strong> (xs： string) </span><span class="sxs-lookup"><span data-stu-id="1da49-115"><dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="1da49-116">由任何字元序列組成的字串，包括空白字元和分行符號字元。</span><span class="sxs-lookup"><span data-stu-id="1da49-116">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1da49-117"><strong>識別碼</strong></span><span class="sxs-lookup"><span data-stu-id="1da49-117"><strong>Id</strong></span></span><br/></td>
<td><span data-ttu-id="1da49-118">xs： positiveInteger 或 xs： string</span><span class="sxs-lookup"><span data-stu-id="1da49-118">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="1da49-119">否</span><span class="sxs-lookup"><span data-stu-id="1da49-119">No</span></span><br/></td>
<td><span data-ttu-id="1da49-120">唯一的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="1da49-120">The unique resource ID.</span></span> <br/> <br/><span data-ttu-id="1da49-121">
<dt><span></span><span></span><strong></strong> (xs： positiveInteger 或 xs： string) </span><span class="sxs-lookup"><span data-stu-id="1da49-121">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="1da49-122">介於2和59999（含）之間的整數值，或以十六進位（含）表示的0xea5f。</span><span class="sxs-lookup"><span data-stu-id="1da49-122">An integer value between 2 and 59999, inclusive, or 0x2 and 0xea5f in hexadecimal, inclusive.</span></span> <br/> <span data-ttu-id="1da49-123">最大長度為10個字元，包括選擇性前置零。</span><span class="sxs-lookup"><span data-stu-id="1da49-123">The maximum length is 10 characters including optional leading zeros.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1da49-124"><strong>符號</strong></span><span class="sxs-lookup"><span data-stu-id="1da49-124"><strong>Symbol</strong></span></span><br/></td>
<td><span data-ttu-id="1da49-125">xs:string</span><span class="sxs-lookup"><span data-stu-id="1da49-125">xs:string</span></span><br/></td>
<td><span data-ttu-id="1da49-126">否</span><span class="sxs-lookup"><span data-stu-id="1da49-126">No</span></span><br/></td>
<td><span data-ttu-id="1da49-127">字串的資源符號。</span><span class="sxs-lookup"><span data-stu-id="1da49-127">The resource symbol for the string.</span></span><br/> <br/><span data-ttu-id="1da49-128">
<dt><span></span><span></span><strong></strong> (xs： string) </span><span class="sxs-lookup"><span data-stu-id="1da49-128">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="1da49-129">字母或底線，後面接著任何一連串的字母、數位或底線。</span><span class="sxs-lookup"><span data-stu-id="1da49-129">A letter or underscore followed by any sequence of letters, digits, or underscores.</span></span><br/> <span data-ttu-id="1da49-130">長度上限為100個字元。</span><span class="sxs-lookup"><span data-stu-id="1da49-130">The maximum length is 100 characters.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="1da49-131">子元素</span><span class="sxs-lookup"><span data-stu-id="1da49-131">Child elements</span></span>



| <span data-ttu-id="1da49-132">元素</span><span class="sxs-lookup"><span data-stu-id="1da49-132">Element</span></span>                                                                   | <span data-ttu-id="1da49-133">描述</span><span class="sxs-lookup"><span data-stu-id="1da49-133">Description</span></span>                                   |
|---------------------------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="1da49-134">**字串。內容**</span><span class="sxs-lookup"><span data-stu-id="1da49-134">**String.Content**</span></span>](windowsribbon-element-string-content.md)<br/> | <span data-ttu-id="1da49-135">最多可能發生一次</span><span class="sxs-lookup"><span data-stu-id="1da49-135">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="1da49-136">**String.Id**</span><span class="sxs-lookup"><span data-stu-id="1da49-136">**String.Id**</span></span>](windowsribbon-element-string-id.md)<br/>           | <span data-ttu-id="1da49-137">最多可能發生一次</span><span class="sxs-lookup"><span data-stu-id="1da49-137">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="1da49-138">**字串. 符號**</span><span class="sxs-lookup"><span data-stu-id="1da49-138">**String.Symbol**</span></span>](windowsribbon-element-string-symbol.md)<br/>   | <span data-ttu-id="1da49-139">最多可能發生一次</span><span class="sxs-lookup"><span data-stu-id="1da49-139">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="1da49-140">父元素</span><span class="sxs-lookup"><span data-stu-id="1da49-140">Parent elements</span></span>



| <span data-ttu-id="1da49-141">元素</span><span class="sxs-lookup"><span data-stu-id="1da49-141">Element</span></span>                                                                                           |
|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1da49-142">**命令。快速鍵**</span><span class="sxs-lookup"><span data-stu-id="1da49-142">**Command.Keytip**</span></span>](windowsribbon-element-command-keytip.md)<br/>                         |
| [<span data-ttu-id="1da49-143">**LabelDescription**</span><span class="sxs-lookup"><span data-stu-id="1da49-143">**Command.LabelDescription**</span></span>](windowsribbon-element-command-labeldescription.md)<br/>     |
| [<span data-ttu-id="1da49-144">**LabelTitle**</span><span class="sxs-lookup"><span data-stu-id="1da49-144">**Command.LabelTitle**</span></span>](windowsribbon-element-command-labeltitle.md)<br/>                 |
| [<span data-ttu-id="1da49-145">**TooltipDescription**</span><span class="sxs-lookup"><span data-stu-id="1da49-145">**Command.TooltipDescription**</span></span>](windowsribbon-element-command-tooltipdescription.md)<br/> |
| [<span data-ttu-id="1da49-146">**TooltipTitle**</span><span class="sxs-lookup"><span data-stu-id="1da49-146">**Command.TooltipTitle**</span></span>](windowsribbon-element-command-tooltiptitle.md)<br/>             |



## <a name="remarks"></a><span data-ttu-id="1da49-147">備註</span><span class="sxs-lookup"><span data-stu-id="1da49-147">Remarks</span></span>

<span data-ttu-id="1da49-148">選擇性。</span><span class="sxs-lookup"><span data-stu-id="1da49-148">Optional.</span></span>

<span data-ttu-id="1da49-149">每個命令最多隻能出現一次 [**。 LabelTitle**](windowsribbon-element-command-labeltitle.md)、 [**LabelDescription**](windowsribbon-element-command-labeldescription.md)、 [**命令提示**](windowsribbon-element-command-keytip.md)、 [**命令 TooltipTitle**](windowsribbon-element-command-tooltiptitle.md)或 [**TooltipDescription**](windowsribbon-element-command-tooltipdescription.md) 元素。</span><span class="sxs-lookup"><span data-stu-id="1da49-149">May occur at most once for each [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md), [**Command.LabelDescription**](windowsribbon-element-command-labeldescription.md), [**Command.Keytip**](windowsribbon-element-command-keytip.md), [**Command.TooltipTitle**](windowsribbon-element-command-tooltiptitle.md), or [**Command.TooltipDescription**](windowsribbon-element-command-tooltipdescription.md) element.</span></span>

<span data-ttu-id="1da49-150">字串定義會加入至功能區標頭檔中，例如 `#define strSave 59999` 。</span><span class="sxs-lookup"><span data-stu-id="1da49-150">The string definition is added to the Ribbon header file, for example, `#define strSave 59999`.</span></span>

<span data-ttu-id="1da49-151">如果未宣告任何宣告，則會將字串加入功能區資源檔中的字串資料表，其中的名稱和識別碼是由功能區架構產生的。</span><span class="sxs-lookup"><span data-stu-id="1da49-151">The string is added to a string table in the Ribbon resource file where a name and ID are generated by the Ribbon framework if none are declared.</span></span>

## <a name="examples"></a><span data-ttu-id="1da49-152">範例</span><span class="sxs-lookup"><span data-stu-id="1da49-152">Examples</span></span>

<span data-ttu-id="1da49-153">下列範例示範 [**LabelTitle**](windowsribbon-element-command-labeltitle.md) 專案的標記與 **字串** 宣告。</span><span class="sxs-lookup"><span data-stu-id="1da49-153">The following example demonstrates the markup for a [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) element with a **String** declaration.</span></span>


```XML
<Command.LabelTitle>
  <String>
    <String.Content>Label for Save</String.Content>
    <String.Id>59999</String.Id>
    <String.Symbol>strSave</String.Symbol>
  </String>
</Command.LabelTitle>
```



## <a name="element-information"></a><span data-ttu-id="1da49-154">項目資訊</span><span class="sxs-lookup"><span data-stu-id="1da49-154">Element information</span></span>

- <span data-ttu-id="1da49-155">**最低支援系統**： Windows 7</span><span class="sxs-lookup"><span data-stu-id="1da49-155">**Minimum supported system**: Windows 7</span></span> 
- <span data-ttu-id="1da49-156">**可以是空** 的：否</span><span class="sxs-lookup"><span data-stu-id="1da49-156">**Can be empty**: No</span></span>



 

 






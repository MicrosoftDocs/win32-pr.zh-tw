---
title: ApplicationMenu 元素
description: 表示應用程式功能表。 |ApplicationMenu 元素
ms.assetid: 815e0462-ea45-44b1-81bf-f5797b22e920
keywords:
- ApplicationMenu 元素視窗功能區
topic_type:
- apiref
api_name:
- ApplicationMenu
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a02193b4c3e61b4b8cf2f129619969f6a82a84ac
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104196022"
---
# <a name="applicationmenu-element"></a><span data-ttu-id="774a8-105">ApplicationMenu 元素</span><span class="sxs-lookup"><span data-stu-id="774a8-105">ApplicationMenu element</span></span>

<span data-ttu-id="774a8-106">表示 [應用程式功能表](windowsribbon-controls-applicationmenu.md)。</span><span class="sxs-lookup"><span data-stu-id="774a8-106">Represents the [Application Menu](windowsribbon-controls-applicationmenu.md).</span></span>

## <a name="usage"></a><span data-ttu-id="774a8-107">使用方式</span><span class="sxs-lookup"><span data-stu-id="774a8-107">Usage</span></span>

``` syntax
<ApplicationMenu
  CommandName = "xs:positiveInteger or xs:string"
>
  child elements
</ApplicationMenu>
```

## <a name="attributes"></a><span data-ttu-id="774a8-108">屬性</span><span class="sxs-lookup"><span data-stu-id="774a8-108">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="774a8-109">屬性</span><span class="sxs-lookup"><span data-stu-id="774a8-109">Attribute</span></span></th>
<th><span data-ttu-id="774a8-110">類型</span><span class="sxs-lookup"><span data-stu-id="774a8-110">Type</span></span></th>
<th><span data-ttu-id="774a8-111">必要</span><span class="sxs-lookup"><span data-stu-id="774a8-111">Required</span></span></th>
<th><span data-ttu-id="774a8-112">描述</span><span class="sxs-lookup"><span data-stu-id="774a8-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="774a8-113"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="774a8-113"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="774a8-114">xs： positiveInteger 或 xs： string</span><span class="sxs-lookup"><span data-stu-id="774a8-114">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="774a8-115">No</span><span class="sxs-lookup"><span data-stu-id="774a8-115">No</span></span><br/></td>
<td><span data-ttu-id="774a8-116">將元素與 <a href="windowsribbon-element-command.md"><strong>命令</strong></a>產生關聯。</span><span class="sxs-lookup"><span data-stu-id="774a8-116">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="774a8-117">
<dt><span></span><span></span><strong></strong> (xs： positiveInteger 或 xs： string) </span><span class="sxs-lookup"><span data-stu-id="774a8-117">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="774a8-118">字串、介於2與59999（含）之間的整數值，或介於0x2 與0xea5f （含）之間的十六進位值。</span><span class="sxs-lookup"><span data-stu-id="774a8-118">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="774a8-119">值在功能區 XML 檔中必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="774a8-119">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="774a8-120">最大長度：100個字元。</span><span class="sxs-lookup"><span data-stu-id="774a8-120">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="774a8-121">子元素</span><span class="sxs-lookup"><span data-stu-id="774a8-121">Child elements</span></span>



| <span data-ttu-id="774a8-122">元素</span><span class="sxs-lookup"><span data-stu-id="774a8-122">Element</span></span>                                                                                             | <span data-ttu-id="774a8-123">描述</span><span class="sxs-lookup"><span data-stu-id="774a8-123">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="774a8-124">**ApplicationMenu.RecentItems**</span><span class="sxs-lookup"><span data-stu-id="774a8-124">**ApplicationMenu.RecentItems**</span></span>](windowsribbon-element-applicationmenu-recentitems.md)<br/> | <span data-ttu-id="774a8-125">最多可能發生一次</span><span class="sxs-lookup"><span data-stu-id="774a8-125">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="774a8-126">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="774a8-126">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>                                     | <span data-ttu-id="774a8-127">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="774a8-127">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="774a8-128">父元素</span><span class="sxs-lookup"><span data-stu-id="774a8-128">Parent elements</span></span>



| <span data-ttu-id="774a8-129">元素</span><span class="sxs-lookup"><span data-stu-id="774a8-129">Element</span></span>                                                                                   |
|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="774a8-130">**功能區. ApplicationMenu**</span><span class="sxs-lookup"><span data-stu-id="774a8-130">**Ribbon.ApplicationMenu**</span></span>](windowsribbon-element-ribbon-applicationmenu.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="774a8-131">備註</span><span class="sxs-lookup"><span data-stu-id="774a8-131">Remarks</span></span>

<span data-ttu-id="774a8-132">必要。</span><span class="sxs-lookup"><span data-stu-id="774a8-132">Required.</span></span>

<span data-ttu-id="774a8-133">每個 [**ApplicationMenu**](windowsribbon-element-ribbon-applicationmenu.md)都必須剛好發生一次。</span><span class="sxs-lookup"><span data-stu-id="774a8-133">Must occur exactly once for each [**Ribbon.ApplicationMenu**](windowsribbon-element-ribbon-applicationmenu.md).</span></span>

<span data-ttu-id="774a8-134">**ApplicationMenu** 元素的子項目必須以指定的順序發生：</span><span class="sxs-lookup"><span data-stu-id="774a8-134">The child elements of the **ApplicationMenu** element must occur in the specified order:</span></span>

1.  [<span data-ttu-id="774a8-135">**ApplicationMenu.RecentItems**</span><span class="sxs-lookup"><span data-stu-id="774a8-135">**ApplicationMenu.RecentItems**</span></span>](windowsribbon-element-applicationmenu-recentitems.md)
2.  [<span data-ttu-id="774a8-136">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="774a8-136">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)

## <a name="examples"></a><span data-ttu-id="774a8-137">範例</span><span class="sxs-lookup"><span data-stu-id="774a8-137">Examples</span></span>

<span data-ttu-id="774a8-138">下列範例示範 [應用程式功能表](windowsribbon-controls-applicationmenu.md)的基本標記。</span><span class="sxs-lookup"><span data-stu-id="774a8-138">The following example demonstrates the basic markup for the [Application Menu](windowsribbon-controls-applicationmenu.md).</span></span>

<span data-ttu-id="774a8-139">這段程式碼會顯示 **ApplicationMenu** 命令宣告。</span><span class="sxs-lookup"><span data-stu-id="774a8-139">This section of code shows the **ApplicationMenu** Command declarations.</span></span>


```XML
<!-- Command declarations for the Application Menu. -->
<Command Name="cmdFileMenu"
         Symbol="ID_FILE_MENU"
         Id="25000" />
<!-- Command declaration for most recently used items. -->
<Command Name="cmdMRUItems"
         Symbol="ID_FILE_MRUITEMS"
         Id="25050"/>
<!-- Command declarations for Application Menu items. -->
<Command Name="cmdNew"
         Symbol="ID_FILE_NEW"
         Comment="New"
         Id="25001"
         LabelTitle="&amp;New"/>
<Command Name="cmdOpen"
         Symbol="ID_FILE_OPEN"
         Comment="Open"
         Id="25002"
         LabelTitle="&amp;&amp;Open"/>
<Command>
  <Command.Name>cmdSave</Command.Name>
  <Command.Symbol>ID_FILE_SAVE</Command.Symbol>
  <Command.Comment>Save</Command.Comment>
  <Command.Id>25003</Command.Id>
  <Command.LabelTitle>
    <String>
      <String.Content>Label for Save</String.Content>
      <String.Id>59999</String.Id>
      <String.Symbol>strSave</String.Symbol>
    </String>
  </Command.LabelTitle>
  <Command.TooltipTitle>Tooltip title with &amp;&amp; for Save Command</Command.TooltipTitle>
  <Command.TooltipDescription>Tooltip description for Save Command.</Command.TooltipDescription>
  <Command.Keytip>s1</Command.Keytip>
</Command>
<Command Name="cmdPrint"
         Symbol="ID_FILE_PRINT"
         Comment="Save"
         Id="25004"
         LabelTitle="Print" />
<Command Name="cmdExit"
         Symbol="ID_FILE_EXIT"
         Comment="Exit"
         Id="25005"
         LabelTitle="Exit" />
```



<span data-ttu-id="774a8-140">這段程式碼會顯示 **ApplicationMenu** 控制項宣告。</span><span class="sxs-lookup"><span data-stu-id="774a8-140">This section of code shows the **ApplicationMenu** control declarations.</span></span>


```XML
<!-- Control declarations for Application Menu items. -->
<Ribbon.ApplicationMenu>
  <ApplicationMenu CommandName="cmdFileMenu">
    <!-- Most recently used items collection. -->
    <ApplicationMenu.RecentItems>
      <RecentItems CommandName="cmdMRUItems"/>
    </ApplicationMenu.RecentItems>
    <!-- Menu items collection. -->
    <MenuGroup>
      <Button CommandName="cmdNew" />
      <Button CommandName="cmdOpen" />
      <Button CommandName="cmdSave" />
    </MenuGroup>
    <MenuGroup>
      <Button CommandName="cmdPrint" />
      <Button CommandName="cmdExit" />
    </MenuGroup>
  </ApplicationMenu>
</Ribbon.ApplicationMenu>
```



## <a name="element-information"></a><span data-ttu-id="774a8-141">項目資訊</span><span class="sxs-lookup"><span data-stu-id="774a8-141">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="774a8-142">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="774a8-142">Minimum supported system</span></span><br/> | <span data-ttu-id="774a8-143">Windows 7</span><span class="sxs-lookup"><span data-stu-id="774a8-143">Windows 7</span></span> |
| <span data-ttu-id="774a8-144">可以是空的</span><span class="sxs-lookup"><span data-stu-id="774a8-144">Can be empty</span></span>                        | <span data-ttu-id="774a8-145">否</span><span class="sxs-lookup"><span data-stu-id="774a8-145">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="774a8-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="774a8-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="774a8-147">應用程式功能表控制項</span><span class="sxs-lookup"><span data-stu-id="774a8-147">Application Menu control</span></span>](windowsribbon-controls-applicationmenu.md)
</dt> </dl>

 

 






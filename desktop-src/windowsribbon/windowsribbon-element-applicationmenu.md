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
ms.openlocfilehash: e535fbcc09a404ad7dd5a4019438f4513f5c77c6
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443049"
---
# <a name="applicationmenu-element"></a><span data-ttu-id="b9275-105">ApplicationMenu 元素</span><span class="sxs-lookup"><span data-stu-id="b9275-105">ApplicationMenu element</span></span>

<span data-ttu-id="b9275-106">表示 [應用程式功能表](windowsribbon-controls-applicationmenu.md)。</span><span class="sxs-lookup"><span data-stu-id="b9275-106">Represents the [Application Menu](windowsribbon-controls-applicationmenu.md).</span></span>

## <a name="usage"></a><span data-ttu-id="b9275-107">使用方式</span><span class="sxs-lookup"><span data-stu-id="b9275-107">Usage</span></span>

``` syntax
<ApplicationMenu
  CommandName = "xs:positiveInteger or xs:string"
>
  child elements
</ApplicationMenu>
```

## <a name="attributes"></a><span data-ttu-id="b9275-108">屬性</span><span class="sxs-lookup"><span data-stu-id="b9275-108">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b9275-109">屬性</span><span class="sxs-lookup"><span data-stu-id="b9275-109">Attribute</span></span></th>
<th><span data-ttu-id="b9275-110">類型</span><span class="sxs-lookup"><span data-stu-id="b9275-110">Type</span></span></th>
<th><span data-ttu-id="b9275-111">必要</span><span class="sxs-lookup"><span data-stu-id="b9275-111">Required</span></span></th>
<th><span data-ttu-id="b9275-112">描述</span><span class="sxs-lookup"><span data-stu-id="b9275-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b9275-113"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="b9275-113"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="b9275-114">xs： positiveInteger 或 xs： string</span><span class="sxs-lookup"><span data-stu-id="b9275-114">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="b9275-115">否</span><span class="sxs-lookup"><span data-stu-id="b9275-115">No</span></span><br/></td>
<td><span data-ttu-id="b9275-116">將元素與 <a href="windowsribbon-element-command.md"><strong>命令</strong></a>產生關聯。</span><span class="sxs-lookup"><span data-stu-id="b9275-116">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="b9275-117">
<dt><span></span><span></span><strong></strong> (xs： positiveInteger 或 xs： string) </span><span class="sxs-lookup"><span data-stu-id="b9275-117">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="b9275-118">字串、介於2與59999（含）之間的整數值，或介於0x2 與0xea5f （含）之間的十六進位值。</span><span class="sxs-lookup"><span data-stu-id="b9275-118">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="b9275-119">值在功能區 XML 檔中必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="b9275-119">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="b9275-120">最大長度：100個字元。</span><span class="sxs-lookup"><span data-stu-id="b9275-120">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="b9275-121">子元素</span><span class="sxs-lookup"><span data-stu-id="b9275-121">Child elements</span></span>



| <span data-ttu-id="b9275-122">元素</span><span class="sxs-lookup"><span data-stu-id="b9275-122">Element</span></span>                                                                                             | <span data-ttu-id="b9275-123">描述</span><span class="sxs-lookup"><span data-stu-id="b9275-123">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="b9275-124">**ApplicationMenu.RecentItems**</span><span class="sxs-lookup"><span data-stu-id="b9275-124">**ApplicationMenu.RecentItems**</span></span>](windowsribbon-element-applicationmenu-recentitems.md)<br/> | <span data-ttu-id="b9275-125">最多可能發生一次</span><span class="sxs-lookup"><span data-stu-id="b9275-125">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="b9275-126">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="b9275-126">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>                                     | <span data-ttu-id="b9275-127">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="b9275-127">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="b9275-128">父元素</span><span class="sxs-lookup"><span data-stu-id="b9275-128">Parent elements</span></span>



| <span data-ttu-id="b9275-129">元素</span><span class="sxs-lookup"><span data-stu-id="b9275-129">Element</span></span>                                                                                   |
|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b9275-130">**功能區. ApplicationMenu**</span><span class="sxs-lookup"><span data-stu-id="b9275-130">**Ribbon.ApplicationMenu**</span></span>](windowsribbon-element-ribbon-applicationmenu.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="b9275-131">備註</span><span class="sxs-lookup"><span data-stu-id="b9275-131">Remarks</span></span>

<span data-ttu-id="b9275-132">必要。</span><span class="sxs-lookup"><span data-stu-id="b9275-132">Required.</span></span>

<span data-ttu-id="b9275-133">每個 [**ApplicationMenu**](windowsribbon-element-ribbon-applicationmenu.md)都必須剛好發生一次。</span><span class="sxs-lookup"><span data-stu-id="b9275-133">Must occur exactly once for each [**Ribbon.ApplicationMenu**](windowsribbon-element-ribbon-applicationmenu.md).</span></span>

<span data-ttu-id="b9275-134">**ApplicationMenu** 元素的子項目必須以指定的順序發生：</span><span class="sxs-lookup"><span data-stu-id="b9275-134">The child elements of the **ApplicationMenu** element must occur in the specified order:</span></span>

1.  [<span data-ttu-id="b9275-135">**ApplicationMenu.RecentItems**</span><span class="sxs-lookup"><span data-stu-id="b9275-135">**ApplicationMenu.RecentItems**</span></span>](windowsribbon-element-applicationmenu-recentitems.md)
2.  [<span data-ttu-id="b9275-136">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="b9275-136">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)

## <a name="examples"></a><span data-ttu-id="b9275-137">範例</span><span class="sxs-lookup"><span data-stu-id="b9275-137">Examples</span></span>

<span data-ttu-id="b9275-138">下列範例示範 [應用程式功能表](windowsribbon-controls-applicationmenu.md)的基本標記。</span><span class="sxs-lookup"><span data-stu-id="b9275-138">The following example demonstrates the basic markup for the [Application Menu](windowsribbon-controls-applicationmenu.md).</span></span>

<span data-ttu-id="b9275-139">這段程式碼會顯示 **ApplicationMenu** 命令宣告。</span><span class="sxs-lookup"><span data-stu-id="b9275-139">This section of code shows the **ApplicationMenu** Command declarations.</span></span>


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



<span data-ttu-id="b9275-140">這段程式碼會顯示 **ApplicationMenu** 控制項宣告。</span><span class="sxs-lookup"><span data-stu-id="b9275-140">This section of code shows the **ApplicationMenu** control declarations.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="b9275-141">項目資訊</span><span class="sxs-lookup"><span data-stu-id="b9275-141">Element information</span></span>

* <span data-ttu-id="b9275-142">**最低支援系統**： Windows 7</span><span class="sxs-lookup"><span data-stu-id="b9275-142">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="b9275-143">**可以是空** 的：否</span><span class="sxs-lookup"><span data-stu-id="b9275-143">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="b9275-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b9275-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9275-145">應用程式功能表控制項</span><span class="sxs-lookup"><span data-stu-id="b9275-145">Application Menu control</span></span>](windowsribbon-controls-applicationmenu.md)
</dt> </dl>

 

 






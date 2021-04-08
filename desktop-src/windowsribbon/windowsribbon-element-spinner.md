---
title: 微調元素
description: 表示微調控制項。
ms.assetid: 6a174ec9-0fde-4171-a363-0e330ac31a8b
keywords:
- 微調元素視窗功能區
topic_type:
- apiref
api_name:
- Spinner
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5b1f9727dc7fbad8be24c15f0b1f551b021294dd
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/11/2020
ms.locfileid: "104022979"
---
# <a name="spinner-element"></a><span data-ttu-id="f3680-104">微調元素</span><span class="sxs-lookup"><span data-stu-id="f3680-104">Spinner element</span></span>

<span data-ttu-id="f3680-105">表示 [微調](windowsribbon-controls-spinner.md) 控制項。</span><span class="sxs-lookup"><span data-stu-id="f3680-105">Represents a [Spinner](windowsribbon-controls-spinner.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="f3680-106">使用方式</span><span class="sxs-lookup"><span data-stu-id="f3680-106">Usage</span></span>

``` syntax
<Spinner
  CommandName = "xs:positiveInteger or xs:string"/>
```

## <a name="attributes"></a><span data-ttu-id="f3680-107">屬性</span><span class="sxs-lookup"><span data-stu-id="f3680-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f3680-108">屬性</span><span class="sxs-lookup"><span data-stu-id="f3680-108">Attribute</span></span></th>
<th><span data-ttu-id="f3680-109">類型</span><span class="sxs-lookup"><span data-stu-id="f3680-109">Type</span></span></th>
<th><span data-ttu-id="f3680-110">必要</span><span class="sxs-lookup"><span data-stu-id="f3680-110">Required</span></span></th>
<th><span data-ttu-id="f3680-111">描述</span><span class="sxs-lookup"><span data-stu-id="f3680-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f3680-112"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="f3680-112"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="f3680-113">xs： positiveInteger 或 xs： string</span><span class="sxs-lookup"><span data-stu-id="f3680-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="f3680-114">No</span><span class="sxs-lookup"><span data-stu-id="f3680-114">No</span></span><br/></td>
<td><span data-ttu-id="f3680-115">將元素與 <a href="windowsribbon-element-command.md"><strong>命令</strong></a>產生關聯。</span><span class="sxs-lookup"><span data-stu-id="f3680-115">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="f3680-116">
<dt><span></span><span></span><strong></strong> (xs： positiveInteger 或 xs： string) </span><span class="sxs-lookup"><span data-stu-id="f3680-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="f3680-117">字串、介於2與59999（含）之間的整數值，或介於0x2 與0xea5f （含）之間的十六進位值。</span><span class="sxs-lookup"><span data-stu-id="f3680-117">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="f3680-118">值在功能區 XML 檔中必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="f3680-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="f3680-119">最大長度：100個字元。</span><span class="sxs-lookup"><span data-stu-id="f3680-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="f3680-120">子元素</span><span class="sxs-lookup"><span data-stu-id="f3680-120">Child elements</span></span>

<span data-ttu-id="f3680-121">沒有任何子項目。</span><span class="sxs-lookup"><span data-stu-id="f3680-121">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="f3680-122">父元素</span><span class="sxs-lookup"><span data-stu-id="f3680-122">Parent elements</span></span>



| <span data-ttu-id="f3680-123">元素</span><span class="sxs-lookup"><span data-stu-id="f3680-123">Element</span></span>                                                                           |
|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="f3680-124">**ControlGroup**</span><span class="sxs-lookup"><span data-stu-id="f3680-124">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>             |
| [<span data-ttu-id="f3680-125">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="f3680-125">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>       |
| [<span data-ttu-id="f3680-126">**Group**</span><span class="sxs-lookup"><span data-stu-id="f3680-126">**Group**</span></span>](windowsribbon-element-group.md)<br/>                           |
| [<span data-ttu-id="f3680-127">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="f3680-127">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>                   |
| [<span data-ttu-id="f3680-128">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="f3680-128">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="f3680-129">備註</span><span class="sxs-lookup"><span data-stu-id="f3680-129">Remarks</span></span>

<span data-ttu-id="f3680-130">選擇性。</span><span class="sxs-lookup"><span data-stu-id="f3680-130">Optional.</span></span>

<span data-ttu-id="f3680-131">可能會針對每個 [**ControlGroup**](windowsribbon-element-controlgroup.md) 或 [**Group**](windowsribbon-element-group.md) 元素髮生一次或多次。</span><span class="sxs-lookup"><span data-stu-id="f3680-131">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md) or [**Group**](windowsribbon-element-group.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="f3680-132">範例</span><span class="sxs-lookup"><span data-stu-id="f3680-132">Examples</span></span>

<span data-ttu-id="f3680-133">下列範例示範 [微調](windowsribbon-controls-spinner.md)項的基本標記。</span><span class="sxs-lookup"><span data-stu-id="f3680-133">The following example demonstrates the basic markup for the [Spinner](windowsribbon-controls-spinner.md).</span></span>

<span data-ttu-id="f3680-134">這一節的程式碼會顯示 **微調** 命令宣告，以及做為 **微調** 專案父容器的 [**Group**](windowsribbon-element-group.md)元素。</span><span class="sxs-lookup"><span data-stu-id="f3680-134">This section of code shows the **Spinner** Command declarations, with a [**Group**](windowsribbon-element-group.md) element that functions as the parent container for the **Spinner** element.</span></span>


```XML
<Command Name="GroupSpinner1" Symbol="IDR_CMD_GROUPSPINNER1" Id="30010">
  <Command.LabelTitle>
    <String Id="210">Resize</String>
  </Command.LabelTitle>
</Command>
<Command Name="Spinner_Size" Symbol="IDR_CMD_SPINNER_RESIZE" Id="30015">
  <Command.LabelTitle>
    <String Id="215">Resize by:</String>
  </Command.LabelTitle>
</Command>
```



<span data-ttu-id="f3680-135">這段程式碼會顯示 **微調** 控制項宣告。</span><span class="sxs-lookup"><span data-stu-id="f3680-135">This section of code shows the **Spinner** control declarations.</span></span>


```XML
<Group CommandName="GroupSpinner1">
  <Spinner CommandName="Spinner_Size" />
</Group>
```



## <a name="element-information"></a><span data-ttu-id="f3680-136">項目資訊</span><span class="sxs-lookup"><span data-stu-id="f3680-136">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="f3680-137">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="f3680-137">Minimum supported system</span></span><br/> | <span data-ttu-id="f3680-138">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f3680-138">Windows 7</span></span> |
| <span data-ttu-id="f3680-139">可以是空的</span><span class="sxs-lookup"><span data-stu-id="f3680-139">Can be empty</span></span>                        | <span data-ttu-id="f3680-140">Yes</span><span class="sxs-lookup"><span data-stu-id="f3680-140">Yes</span></span>       |



## <a name="see-also"></a><span data-ttu-id="f3680-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f3680-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3680-142">微調控制項</span><span class="sxs-lookup"><span data-stu-id="f3680-142">Spinner control</span></span>](windowsribbon-controls-spinner.md)
</dt> </dl>

 

 






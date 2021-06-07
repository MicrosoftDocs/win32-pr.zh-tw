---
title: GroupSizeDefinition 元素
description: 表示自訂範本中控制項群組的版面配置大小。
ms.assetid: c0e20c80-16af-41d5-81e1-0dc32e92e3fa
keywords:
- GroupSizeDefinition 元素視窗功能區
topic_type:
- apiref
api_name:
- GroupSizeDefinition
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 650301a29ace2c6df9316a315d4cdbad448e5573
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443379"
---
# <a name="groupsizedefinition-element"></a><span data-ttu-id="ab483-104">GroupSizeDefinition 元素</span><span class="sxs-lookup"><span data-stu-id="ab483-104">GroupSizeDefinition element</span></span>

<span data-ttu-id="ab483-105">表示自訂範本中控制項群組的版面配置大小。</span><span class="sxs-lookup"><span data-stu-id="ab483-105">Represents a layout size for a group of controls in a custom template.</span></span>

## <a name="usage"></a><span data-ttu-id="ab483-106">使用方式</span><span class="sxs-lookup"><span data-stu-id="ab483-106">Usage</span></span>

``` syntax
<GroupSizeDefinition
  Size = "xs:string">
  child elements
</GroupSizeDefinition>
```

## <a name="attributes"></a><span data-ttu-id="ab483-107">屬性</span><span class="sxs-lookup"><span data-stu-id="ab483-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ab483-108">屬性</span><span class="sxs-lookup"><span data-stu-id="ab483-108">Attribute</span></span></th>
<th><span data-ttu-id="ab483-109">類型</span><span class="sxs-lookup"><span data-stu-id="ab483-109">Type</span></span></th>
<th><span data-ttu-id="ab483-110">必要</span><span class="sxs-lookup"><span data-stu-id="ab483-110">Required</span></span></th>
<th><span data-ttu-id="ab483-111">描述</span><span class="sxs-lookup"><span data-stu-id="ab483-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ab483-112"><strong>大小</strong></span><span class="sxs-lookup"><span data-stu-id="ab483-112"><strong>Size</strong></span></span><br/></td>
<td><span data-ttu-id="ab483-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="ab483-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="ab483-114">否</span><span class="sxs-lookup"><span data-stu-id="ab483-114">No</span></span><br/></td>
<td><span data-ttu-id="ab483-115">限制為下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="ab483-115">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="ab483-116">
<dt><span></span><span></span><strong></strong> (大型) </span><span class="sxs-lookup"><span data-stu-id="ab483-116">
<dt><span></span><span></span><strong></strong> (Large)</span></span><br/> </dt> <dd> <span data-ttu-id="ab483-117">預設值。</span><span class="sxs-lookup"><span data-stu-id="ab483-117">Default.</span></span> <br/> </dd> <span data-ttu-id="ab483-118"><dt><span></span><span></span><strong></strong> (中) </span><span class="sxs-lookup"><span data-stu-id="ab483-118"><dt><span></span><span></span><strong></strong> (Medium)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="ab483-119"><dt><span></span><span></span><strong></strong> (Small) </span><span class="sxs-lookup"><span data-stu-id="ab483-119"><dt><span></span><span></span><strong></strong> (Small)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="ab483-120">子元素</span><span class="sxs-lookup"><span data-stu-id="ab483-120">Child elements</span></span>



| <span data-ttu-id="ab483-121">元素</span><span class="sxs-lookup"><span data-stu-id="ab483-121">Element</span></span>                                                                                 | <span data-ttu-id="ab483-122">描述</span><span class="sxs-lookup"><span data-stu-id="ab483-122">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="ab483-123">**ColumnBreak**</span><span class="sxs-lookup"><span data-stu-id="ab483-123">**ColumnBreak**</span></span>](windowsribbon-element-columnbreak.md)<br/>                     | <span data-ttu-id="ab483-124">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="ab483-124">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="ab483-125">**ControlGroup**</span><span class="sxs-lookup"><span data-stu-id="ab483-125">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>                   | <span data-ttu-id="ab483-126">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="ab483-126">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="ab483-127">**ControlSizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="ab483-127">**ControlSizeDefinition**</span></span>](windowsribbon-element-controlsizedefinition.md)<br/> | <span data-ttu-id="ab483-128">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="ab483-128">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="ab483-129">**資料列**</span><span class="sxs-lookup"><span data-stu-id="ab483-129">**Row**</span></span>](windowsribbon-element-row.md)<br/>                                     | <span data-ttu-id="ab483-130">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="ab483-130">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="ab483-131">父元素</span><span class="sxs-lookup"><span data-stu-id="ab483-131">Parent elements</span></span>



| <span data-ttu-id="ab483-132">元素</span><span class="sxs-lookup"><span data-stu-id="ab483-132">Element</span></span>                                                                   |
|---------------------------------------------------------------------------|
| [<span data-ttu-id="ab483-133">**SizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="ab483-133">**SizeDefinition**</span></span>](windowsribbon-element-sizedefinition.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="ab483-134">備註</span><span class="sxs-lookup"><span data-stu-id="ab483-134">Remarks</span></span>

<span data-ttu-id="ab483-135">選擇性。</span><span class="sxs-lookup"><span data-stu-id="ab483-135">Optional.</span></span>

<span data-ttu-id="ab483-136">每個 [**SizeDefinition**](windowsribbon-element-sizedefinition.md) 元素最多可能會有三次， (每個 *大小*) 一次。</span><span class="sxs-lookup"><span data-stu-id="ab483-136">May occur up to three times for each [**SizeDefinition**](windowsribbon-element-sizedefinition.md) element (one time for each *Size*).</span></span>

## <a name="examples"></a><span data-ttu-id="ab483-137">範例</span><span class="sxs-lookup"><span data-stu-id="ab483-137">Examples</span></span>

<span data-ttu-id="ab483-138">下列程式碼範例說明基本自訂範本，其中包含在建立自訂範本時，必須以 **GroupSizeDefinition** 元素定義的三個群組配置大小。</span><span class="sxs-lookup"><span data-stu-id="ab483-138">The following code example illustrates a basic custom template that includes the three group layout sizes that must be defined with the **GroupSizeDefinition** element when creating a custom template.</span></span>


```XML
<Group CommandName="cmdButtonGroup2">
  <SizeDefinition>
    <ControlNameMap>
      <ControlNameDefinition Name="button1"/>
      <ControlNameDefinition Name="button2"/>
      <ControlNameDefinition Name="button3"/>
      <ControlNameDefinition Name="button4"/>
    </ControlNameMap>
    <GroupSizeDefinition Size="Large">
      <ControlGroup>
        <ControlSizeDefinition ControlName="button1"
                               ImageSize="Large"
                               IsLabelVisible="true" />
        <ControlSizeDefinition ControlName="button2"
                               ImageSize="Large"
                               IsLabelVisible="true" />
      </ControlGroup>
      <ColumnBreak ShowSeparator="true"/>
      <ControlGroup>
        <ControlSizeDefinition ControlName="button3"
                               ImageSize="Large"
                              IsLabelVisible="true" />
        <ControlSizeDefinition ControlName="button4"
                              ImageSize="Large"
                              IsLabelVisible="true" />
      </ControlGroup>
    </GroupSizeDefinition>
    <GroupSizeDefinition Size="Medium">
      <Row>
        <ControlSizeDefinition ControlName="button1"
                               ImageSize="Small"
                               IsLabelVisible="true" />
        <ControlSizeDefinition ControlName="button3"
                               ImageSize="Small"
                               IsLabelVisible="true" />
      </Row>
      <Row>
        <ControlSizeDefinition ControlName="button2"
                               ImageSize="Small"
                               IsLabelVisible="true" />
        <ControlSizeDefinition ControlName="button4"
                               ImageSize="Small"
                               IsLabelVisible="true" />
      </Row>
    </GroupSizeDefinition>
    <GroupSizeDefinition Size="Small">
      <Row>
        <ControlSizeDefinition ControlName="button1"
                               ImageSize="Small"
                               IsLabelVisible="true" />
        <ControlSizeDefinition ControlName="button3"
                               ImageSize="Small"
                               IsLabelVisible="false" />
      </Row>
      <Row>
        <ControlSizeDefinition ControlName="button2"
                               ImageSize="Small"
                               IsLabelVisible="true" />
        <ControlSizeDefinition ControlName="button4"
                               ImageSize="Small"
                               IsLabelVisible="false" />
      </Row>
    </GroupSizeDefinition>
  </SizeDefinition>
  <Button CommandName="cmdButtonG21"></Button>
  <Button CommandName="cmdButtonG22"></Button>
  <Button CommandName="cmdButtonG23"></Button>
  <Button CommandName="cmdButtonG24"></Button>
</Group>
<Group CommandName="cmdCheckBoxGroup">
  <CheckBox CommandName="cmdCheckBox"></CheckBox>
</Group>
<Group CommandName="cmdToggleButtonGroup"
       SizeDefinition="OneButton">
  <ToggleButton CommandName="cmdToggleButton"></ToggleButton>
</Group>
<Group CommandName="cmdButtonGroup"
       SizeDefinition="ThreeButtons">
  <Button CommandName="cmdButton1"></Button>
  <Button CommandName="cmdButton2"></Button>
  <Button CommandName="cmdButton3"></Button>
</Group>
```



## <a name="element-information"></a><span data-ttu-id="ab483-139">項目資訊</span><span class="sxs-lookup"><span data-stu-id="ab483-139">Element information</span></span>

* <span data-ttu-id="ab483-140">**最低支援系統**： Windows 7</span><span class="sxs-lookup"><span data-stu-id="ab483-140">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="ab483-141">**可以是空** 的：否</span><span class="sxs-lookup"><span data-stu-id="ab483-141">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="ab483-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ab483-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab483-143">透過大小定義和調整原則自訂功能區</span><span class="sxs-lookup"><span data-stu-id="ab483-143">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 






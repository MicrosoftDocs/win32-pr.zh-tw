---
title: ColumnBreak 元素
description: 表示自訂 SizeDefinition 版面配置範本中 (可見或隱藏) 的垂直分隔符號。
ms.assetid: 5979d3e6-366b-4c47-810f-90fb8039af8d
keywords:
- ColumnBreak 元素視窗功能區
topic_type:
- apiref
api_name:
- ColumnBreak
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 00257783c0c8a7919251004a4b1996ab4d994c3c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "106969085"
---
# <a name="columnbreak-element"></a><span data-ttu-id="d86bf-104">ColumnBreak 元素</span><span class="sxs-lookup"><span data-stu-id="d86bf-104">ColumnBreak element</span></span>

<span data-ttu-id="d86bf-105">表示自訂 [**SizeDefinition**](windowsribbon-element-sizedefinition.md) 版面配置範本中 (可見或隱藏) 的垂直分隔符號。</span><span class="sxs-lookup"><span data-stu-id="d86bf-105">Represents a vertical separator (visible or hidden) in custom [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layout templates.</span></span>

## <a name="usage"></a><span data-ttu-id="d86bf-106">使用方式</span><span class="sxs-lookup"><span data-stu-id="d86bf-106">Usage</span></span>

``` syntax
<ColumnBreak
  ShowSeparator = "Boolean"/>
```

## <a name="attributes"></a><span data-ttu-id="d86bf-107">屬性</span><span class="sxs-lookup"><span data-stu-id="d86bf-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d86bf-108">屬性</span><span class="sxs-lookup"><span data-stu-id="d86bf-108">Attribute</span></span></th>
<th><span data-ttu-id="d86bf-109">類型</span><span class="sxs-lookup"><span data-stu-id="d86bf-109">Type</span></span></th>
<th><span data-ttu-id="d86bf-110">必要</span><span class="sxs-lookup"><span data-stu-id="d86bf-110">Required</span></span></th>
<th><span data-ttu-id="d86bf-111">描述</span><span class="sxs-lookup"><span data-stu-id="d86bf-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d86bf-112"><strong>ShowSeparator</strong></span><span class="sxs-lookup"><span data-stu-id="d86bf-112"><strong>ShowSeparator</strong></span></span><br/></td>
<td><span data-ttu-id="d86bf-113">Boolean</span><span class="sxs-lookup"><span data-stu-id="d86bf-113">Boolean</span></span><br/></td>
<td><span data-ttu-id="d86bf-114">No</span><span class="sxs-lookup"><span data-stu-id="d86bf-114">No</span></span><br/></td>
<td><span data-ttu-id="d86bf-115">限制為下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="d86bf-115">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="d86bf-116">
<dt><span></span><span></span><strong></strong> (true) </span><span class="sxs-lookup"><span data-stu-id="d86bf-116">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="d86bf-117">預設值。</span><span class="sxs-lookup"><span data-stu-id="d86bf-117">Default.</span></span> <br/> </dd> <span data-ttu-id="d86bf-118"><dt><span></span><span></span><strong></strong> (false) </span><span class="sxs-lookup"><span data-stu-id="d86bf-118"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="d86bf-119">子元素</span><span class="sxs-lookup"><span data-stu-id="d86bf-119">Child elements</span></span>

<span data-ttu-id="d86bf-120">沒有任何子項目。</span><span class="sxs-lookup"><span data-stu-id="d86bf-120">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="d86bf-121">父元素</span><span class="sxs-lookup"><span data-stu-id="d86bf-121">Parent elements</span></span>



| <span data-ttu-id="d86bf-122">元素</span><span class="sxs-lookup"><span data-stu-id="d86bf-122">Element</span></span>                                                                             |
|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="d86bf-123">**GroupSizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="d86bf-123">**GroupSizeDefinition**</span></span>](windowsribbon-element-groupsizedefinition.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="d86bf-124">備註</span><span class="sxs-lookup"><span data-stu-id="d86bf-124">Remarks</span></span>

<span data-ttu-id="d86bf-125">選擇性。</span><span class="sxs-lookup"><span data-stu-id="d86bf-125">Optional.</span></span>

<span data-ttu-id="d86bf-126">每個 [**GroupSizeDefinition**](windowsribbon-element-groupsizedefinition.md) 專案可能會發生一次或多次。</span><span class="sxs-lookup"><span data-stu-id="d86bf-126">May occur one or more times for each [**GroupSizeDefinition**](windowsribbon-element-groupsizedefinition.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="d86bf-127">範例</span><span class="sxs-lookup"><span data-stu-id="d86bf-127">Examples</span></span>

<span data-ttu-id="d86bf-128">下列範例示範自訂四按鈕 [**SizeDefinition**](windowsribbon-element-sizedefinition.md)版面配置範本中 **ColumnBreak** 元素的基本標記。</span><span class="sxs-lookup"><span data-stu-id="d86bf-128">The following example demonstrates the basic markup for a **ColumnBreak** element in a custom four-button [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layout template.</span></span> <span data-ttu-id="d86bf-129">**ColumnBreak** 只會針對 `Large` 範本指定。</span><span class="sxs-lookup"><span data-stu-id="d86bf-129">The **ColumnBreak** is only specified for the `Large` template.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="d86bf-130">項目資訊</span><span class="sxs-lookup"><span data-stu-id="d86bf-130">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="d86bf-131">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="d86bf-131">Minimum supported system</span></span><br/> | <span data-ttu-id="d86bf-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d86bf-132">Windows 7</span></span> |
| <span data-ttu-id="d86bf-133">可以是空的</span><span class="sxs-lookup"><span data-stu-id="d86bf-133">Can be empty</span></span>                        | <span data-ttu-id="d86bf-134">Yes</span><span class="sxs-lookup"><span data-stu-id="d86bf-134">Yes</span></span>       |



## <a name="see-also"></a><span data-ttu-id="d86bf-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d86bf-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d86bf-136">透過大小定義和調整原則自訂功能區</span><span class="sxs-lookup"><span data-stu-id="d86bf-136">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 






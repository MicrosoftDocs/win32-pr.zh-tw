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
ms.openlocfilehash: b5bff1682cdf55b44092a176abd6dc7e935220a7
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444839"
---
# <a name="columnbreak-element"></a><span data-ttu-id="e9dac-104">ColumnBreak 元素</span><span class="sxs-lookup"><span data-stu-id="e9dac-104">ColumnBreak element</span></span>

<span data-ttu-id="e9dac-105">表示自訂 [**SizeDefinition**](windowsribbon-element-sizedefinition.md) 版面配置範本中 (可見或隱藏) 的垂直分隔符號。</span><span class="sxs-lookup"><span data-stu-id="e9dac-105">Represents a vertical separator (visible or hidden) in custom [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layout templates.</span></span>

## <a name="usage"></a><span data-ttu-id="e9dac-106">使用方式</span><span class="sxs-lookup"><span data-stu-id="e9dac-106">Usage</span></span>

``` syntax
<ColumnBreak
  ShowSeparator = "Boolean"/>
```

## <a name="attributes"></a><span data-ttu-id="e9dac-107">屬性</span><span class="sxs-lookup"><span data-stu-id="e9dac-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e9dac-108">屬性</span><span class="sxs-lookup"><span data-stu-id="e9dac-108">Attribute</span></span></th>
<th><span data-ttu-id="e9dac-109">類型</span><span class="sxs-lookup"><span data-stu-id="e9dac-109">Type</span></span></th>
<th><span data-ttu-id="e9dac-110">必要</span><span class="sxs-lookup"><span data-stu-id="e9dac-110">Required</span></span></th>
<th><span data-ttu-id="e9dac-111">描述</span><span class="sxs-lookup"><span data-stu-id="e9dac-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e9dac-112"><strong>ShowSeparator</strong></span><span class="sxs-lookup"><span data-stu-id="e9dac-112"><strong>ShowSeparator</strong></span></span><br/></td>
<td><span data-ttu-id="e9dac-113">Boolean</span><span class="sxs-lookup"><span data-stu-id="e9dac-113">Boolean</span></span><br/></td>
<td><span data-ttu-id="e9dac-114">否</span><span class="sxs-lookup"><span data-stu-id="e9dac-114">No</span></span><br/></td>
<td><span data-ttu-id="e9dac-115">限制為下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="e9dac-115">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="e9dac-116">
<dt><span></span><span></span><strong></strong> (true) </span><span class="sxs-lookup"><span data-stu-id="e9dac-116">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="e9dac-117">預設值。</span><span class="sxs-lookup"><span data-stu-id="e9dac-117">Default.</span></span> <br/> </dd> <span data-ttu-id="e9dac-118"><dt><span></span><span></span><strong></strong> (false) </span><span class="sxs-lookup"><span data-stu-id="e9dac-118"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="e9dac-119">子元素</span><span class="sxs-lookup"><span data-stu-id="e9dac-119">Child elements</span></span>

<span data-ttu-id="e9dac-120">沒有任何子項目。</span><span class="sxs-lookup"><span data-stu-id="e9dac-120">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="e9dac-121">父元素</span><span class="sxs-lookup"><span data-stu-id="e9dac-121">Parent elements</span></span>



| <span data-ttu-id="e9dac-122">元素</span><span class="sxs-lookup"><span data-stu-id="e9dac-122">Element</span></span>                                                                             |
|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="e9dac-123">**GroupSizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="e9dac-123">**GroupSizeDefinition**</span></span>](windowsribbon-element-groupsizedefinition.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="e9dac-124">備註</span><span class="sxs-lookup"><span data-stu-id="e9dac-124">Remarks</span></span>

<span data-ttu-id="e9dac-125">選擇性。</span><span class="sxs-lookup"><span data-stu-id="e9dac-125">Optional.</span></span>

<span data-ttu-id="e9dac-126">每個 [**GroupSizeDefinition**](windowsribbon-element-groupsizedefinition.md) 專案可能會發生一次或多次。</span><span class="sxs-lookup"><span data-stu-id="e9dac-126">May occur one or more times for each [**GroupSizeDefinition**](windowsribbon-element-groupsizedefinition.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="e9dac-127">範例</span><span class="sxs-lookup"><span data-stu-id="e9dac-127">Examples</span></span>

<span data-ttu-id="e9dac-128">下列範例示範自訂四按鈕 [**SizeDefinition**](windowsribbon-element-sizedefinition.md)版面配置範本中 **ColumnBreak** 元素的基本標記。</span><span class="sxs-lookup"><span data-stu-id="e9dac-128">The following example demonstrates the basic markup for a **ColumnBreak** element in a custom four-button [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layout template.</span></span> <span data-ttu-id="e9dac-129">**ColumnBreak** 只會針對 `Large` 範本指定。</span><span class="sxs-lookup"><span data-stu-id="e9dac-129">The **ColumnBreak** is only specified for the `Large` template.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="e9dac-130">項目資訊</span><span class="sxs-lookup"><span data-stu-id="e9dac-130">Element information</span></span>

* <span data-ttu-id="e9dac-131">**最低支援系統**： Windows 7</span><span class="sxs-lookup"><span data-stu-id="e9dac-131">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="e9dac-132">**可以是空** 的：是</span><span class="sxs-lookup"><span data-stu-id="e9dac-132">**Can be empty**: Yes</span></span>



## <a name="see-also"></a><span data-ttu-id="e9dac-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e9dac-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9dac-134">透過大小定義和調整原則自訂功能區</span><span class="sxs-lookup"><span data-stu-id="e9dac-134">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 






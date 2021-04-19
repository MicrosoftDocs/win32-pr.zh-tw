---
title: SizeDefinition 元素
description: 代表功能區控制項的自訂版面配置範本。
ms.assetid: f90bb469-aee2-4bba-9efe-142a39a8c1ae
keywords:
- SizeDefinition 元素視窗功能區
topic_type:
- apiref
api_name:
- SizeDefinition
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7bfab87f01700f8f4d36f76cbcbfe3696acfbec2
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/11/2020
ms.locfileid: "106999791"
---
# <a name="sizedefinition-element"></a><span data-ttu-id="c2bc3-104">SizeDefinition 元素</span><span class="sxs-lookup"><span data-stu-id="c2bc3-104">SizeDefinition element</span></span>

<span data-ttu-id="c2bc3-105">代表功能區控制項的自訂版面配置範本。</span><span class="sxs-lookup"><span data-stu-id="c2bc3-105">Represents a custom layout template of Ribbon controls.</span></span>

## <a name="usage"></a><span data-ttu-id="c2bc3-106">使用方式</span><span class="sxs-lookup"><span data-stu-id="c2bc3-106">Usage</span></span>

``` syntax
<SizeDefinition
  Name = "xs:positiveInteger or xs:string or xs:token">
  child elements
</SizeDefinition>
```

## <a name="attributes"></a><span data-ttu-id="c2bc3-107">屬性</span><span class="sxs-lookup"><span data-stu-id="c2bc3-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c2bc3-108">屬性</span><span class="sxs-lookup"><span data-stu-id="c2bc3-108">Attribute</span></span></th>
<th><span data-ttu-id="c2bc3-109">類型</span><span class="sxs-lookup"><span data-stu-id="c2bc3-109">Type</span></span></th>
<th><span data-ttu-id="c2bc3-110">必要</span><span class="sxs-lookup"><span data-stu-id="c2bc3-110">Required</span></span></th>
<th><span data-ttu-id="c2bc3-111">描述</span><span class="sxs-lookup"><span data-stu-id="c2bc3-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c2bc3-112"><strong>名稱</strong></span><span class="sxs-lookup"><span data-stu-id="c2bc3-112"><strong>Name</strong></span></span><br/></td>
<td><span data-ttu-id="c2bc3-113">xs： positiveInteger 或 xs： string 或 xs： token</span><span class="sxs-lookup"><span data-stu-id="c2bc3-113">xs:positiveInteger or xs:string or xs:token</span></span><br/></td>
<td><span data-ttu-id="c2bc3-114">Yes</span><span class="sxs-lookup"><span data-stu-id="c2bc3-114">Yes</span></span><br/></td>
<td><span data-ttu-id="c2bc3-115">當 <a href="windowsribbon-element-ribbon-sizedefinitions.md"><strong>SizeDefinitions</strong></a> 是父系時，則為選擇性。</span><span class="sxs-lookup"><span data-stu-id="c2bc3-115">When <a href="windowsribbon-element-ribbon-sizedefinitions.md"><strong>Ribbon.SizeDefinitions</strong></a> is the parent, otherwise optional.</span></span><br/> <br/><span data-ttu-id="c2bc3-116">
<dt><span></span><span></span><strong></strong> (xs： positiveInteger 或 xs： string 或 xs： token) </span><span class="sxs-lookup"><span data-stu-id="c2bc3-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string or xs:token)</span></span><br/> </dt> <dd> <span data-ttu-id="c2bc3-117">介於2與59999（含）之間的字串或整數值，以及十六進位（含）之間的0xea5f。</span><span class="sxs-lookup"><span data-stu-id="c2bc3-117">A string or an integer value between 2 and 59999, inclusive, or 0x2 and 0xea5f in hexadecimal, inclusive.</span></span> <br/> <span data-ttu-id="c2bc3-118">值在功能區 XML 檔中必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="c2bc3-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="c2bc3-119">最大長度：100個字元。</span><span class="sxs-lookup"><span data-stu-id="c2bc3-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="c2bc3-120">子元素</span><span class="sxs-lookup"><span data-stu-id="c2bc3-120">Child elements</span></span>



| <span data-ttu-id="c2bc3-121">元素</span><span class="sxs-lookup"><span data-stu-id="c2bc3-121">Element</span></span>                                                                             | <span data-ttu-id="c2bc3-122">描述</span><span class="sxs-lookup"><span data-stu-id="c2bc3-122">Description</span></span>                                     |
|-------------------------------------------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="c2bc3-123">**ControlNameMap**</span><span class="sxs-lookup"><span data-stu-id="c2bc3-123">**ControlNameMap**</span></span>](windowsribbon-element-controlnamemap.md)<br/>           | <span data-ttu-id="c2bc3-124">最多可能發生一次</span><span class="sxs-lookup"><span data-stu-id="c2bc3-124">May occur at most once</span></span><br/> <br/>   |
| [<span data-ttu-id="c2bc3-125">**GroupSizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="c2bc3-125">**GroupSizeDefinition**</span></span>](windowsribbon-element-groupsizedefinition.md)<br/> | <span data-ttu-id="c2bc3-126">至少必須發生一次</span><span class="sxs-lookup"><span data-stu-id="c2bc3-126">Must occur at least once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="c2bc3-127">父元素</span><span class="sxs-lookup"><span data-stu-id="c2bc3-127">Parent elements</span></span>



| <span data-ttu-id="c2bc3-128">元素</span><span class="sxs-lookup"><span data-stu-id="c2bc3-128">Element</span></span>                                                                                   |
|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c2bc3-129">**Group**</span><span class="sxs-lookup"><span data-stu-id="c2bc3-129">**Group**</span></span>](windowsribbon-element-group.md)<br/>                                   |
| [<span data-ttu-id="c2bc3-130">**功能區. SizeDefinitions**</span><span class="sxs-lookup"><span data-stu-id="c2bc3-130">**Ribbon.SizeDefinitions**</span></span>](windowsribbon-element-ribbon-sizedefinitions.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="c2bc3-131">備註</span><span class="sxs-lookup"><span data-stu-id="c2bc3-131">Remarks</span></span>

<span data-ttu-id="c2bc3-132">選擇性。</span><span class="sxs-lookup"><span data-stu-id="c2bc3-132">Optional.</span></span>

<span data-ttu-id="c2bc3-133">每個 [**群組**](windowsribbon-element-group.md) 元素最多可能會發生一次。</span><span class="sxs-lookup"><span data-stu-id="c2bc3-133">May occur at most once for each [**Group**](windowsribbon-element-group.md) element.</span></span>

<span data-ttu-id="c2bc3-134">針對每個 [**SizeDefinitions**](windowsribbon-element-ribbon-sizedefinitions.md) 元素，可能會出現一次或多次。</span><span class="sxs-lookup"><span data-stu-id="c2bc3-134">May occur one or more times for each [**Ribbon.SizeDefinitions**](windowsribbon-element-ribbon-sizedefinitions.md) element.</span></span>

<span data-ttu-id="c2bc3-135">預先定義的功能區架構配置 [範本](windowsribbon-templates.md)是使用 [**Group**](windowsribbon-element-group.md)元素的 *SizeDefinition* 屬性來指定。</span><span class="sxs-lookup"><span data-stu-id="c2bc3-135">Predefined Ribbon framework [layout templates](windowsribbon-templates.md) are specified with the *SizeDefinition* attribute of the [**Group**](windowsribbon-element-group.md) element.</span></span>

<span data-ttu-id="c2bc3-136">如果未針對索引卷 [**標元素中的每**](windowsribbon-element-tab.md)個 [**群組**](windowsribbon-element-group.md)專案宣告對應的 [**ScalingPolicy IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md)元素，就會發生驗證錯誤。</span><span class="sxs-lookup"><span data-stu-id="c2bc3-136">If a corresponding [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) element is not declared for each [**Group**](windowsribbon-element-group.md) element in a [**Tab**](windowsribbon-element-tab.md) element, a validation error will occur.</span></span>

## <a name="examples"></a><span data-ttu-id="c2bc3-137">範例</span><span class="sxs-lookup"><span data-stu-id="c2bc3-137">Examples</span></span>

<span data-ttu-id="c2bc3-138">下列程式碼範例說明基本的自訂範本。</span><span class="sxs-lookup"><span data-stu-id="c2bc3-138">The following code example illustrates a basic custom template.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="c2bc3-139">項目資訊</span><span class="sxs-lookup"><span data-stu-id="c2bc3-139">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="c2bc3-140">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="c2bc3-140">Minimum supported system</span></span><br/> | <span data-ttu-id="c2bc3-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c2bc3-141">Windows 7</span></span> |
| <span data-ttu-id="c2bc3-142">可以是空的</span><span class="sxs-lookup"><span data-stu-id="c2bc3-142">Can be empty</span></span>                        | <span data-ttu-id="c2bc3-143">否</span><span class="sxs-lookup"><span data-stu-id="c2bc3-143">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="c2bc3-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c2bc3-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2bc3-145">透過大小定義和調整原則自訂功能區</span><span class="sxs-lookup"><span data-stu-id="c2bc3-145">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 






---
title: Scale 元素
description: 透過群組 SizeDefinition 組，表示一組控制項的大小和配置喜好設定。
ms.assetid: feef3721-c779-4c64-96c6-9d951ac32277
keywords:
- 縮放元素視窗功能區
topic_type:
- apiref
api_name:
- Scale
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3832d36a48b330b036fa287499f9db387335f87b
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/11/2020
ms.locfileid: "104374311"
---
# <a name="scale-element"></a><span data-ttu-id="e8036-104">Scale 元素</span><span class="sxs-lookup"><span data-stu-id="e8036-104">Scale element</span></span>

<span data-ttu-id="e8036-105">透過 {**Group**， [**SizeDefinition**](windowsribbon-element-sizedefinition.md)} 配對，表示一 [**組**](windowsribbon-element-group.md)控制項的大小和配置喜好設定。</span><span class="sxs-lookup"><span data-stu-id="e8036-105">Represents the size and layout preference of a [**Group**](windowsribbon-element-group.md) of controls through a {**Group**, [**SizeDefinition**](windowsribbon-element-sizedefinition.md)} pair.</span></span>

## <a name="usage"></a><span data-ttu-id="e8036-106">使用方式</span><span class="sxs-lookup"><span data-stu-id="e8036-106">Usage</span></span>

``` syntax
<Scale
  Size = "xs:string"
  Group = "xs:positiveInteger or xs:string"
/>
```

## <a name="attributes"></a><span data-ttu-id="e8036-107">屬性</span><span class="sxs-lookup"><span data-stu-id="e8036-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e8036-108">屬性</span><span class="sxs-lookup"><span data-stu-id="e8036-108">Attribute</span></span></th>
<th><span data-ttu-id="e8036-109">類型</span><span class="sxs-lookup"><span data-stu-id="e8036-109">Type</span></span></th>
<th><span data-ttu-id="e8036-110">必要</span><span class="sxs-lookup"><span data-stu-id="e8036-110">Required</span></span></th>
<th><span data-ttu-id="e8036-111">描述</span><span class="sxs-lookup"><span data-stu-id="e8036-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e8036-112"><strong>群組</strong></span><span class="sxs-lookup"><span data-stu-id="e8036-112"><strong>Group</strong></span></span><br/></td>
<td><span data-ttu-id="e8036-113">xs： positiveInteger 或 xs： string</span><span class="sxs-lookup"><span data-stu-id="e8036-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="e8036-114">Yes</span><span class="sxs-lookup"><span data-stu-id="e8036-114">Yes</span></span><br/></td>
<td><span data-ttu-id="e8036-115">必須對應至現有的 <a href="windowsribbon-element-group.md"><strong>群組</strong></a> <em>CommandName</em>。</span><span class="sxs-lookup"><span data-stu-id="e8036-115">Must correspond to an existing <a href="windowsribbon-element-group.md"><strong>Group</strong></a> <em>CommandName</em>.</span></span><br/> <br/><span data-ttu-id="e8036-116">
<dt><span></span><span></span><strong></strong> (xs： positiveInteger 或 xs： string) </span><span class="sxs-lookup"><span data-stu-id="e8036-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="e8036-117">介於2與59999（含）之間的字串或整數值，以及十六進位（含）之間的0xea5f。</span><span class="sxs-lookup"><span data-stu-id="e8036-117">A string or an integer value between 2 and 59999, inclusive, or 0x2 and 0xea5f in hexadecimal, inclusive.</span></span> <br/> <span data-ttu-id="e8036-118">值在功能區 XML 檔中必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="e8036-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="e8036-119">最大長度：100個字元。</span><span class="sxs-lookup"><span data-stu-id="e8036-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e8036-120"><strong>大小</strong></span><span class="sxs-lookup"><span data-stu-id="e8036-120"><strong>Size</strong></span></span><br/></td>
<td><span data-ttu-id="e8036-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="e8036-121">xs:string</span></span><br/></td>
<td><span data-ttu-id="e8036-122">Yes</span><span class="sxs-lookup"><span data-stu-id="e8036-122">Yes</span></span><br/></td>
<td><span data-ttu-id="e8036-123">此值應該對應至 [<em>群組</em>] 中指定之相關控制項<a href="windowsribbon-element-group.md"><strong>群組</strong></a>的 [ <em>SizeDefinition</em> ] 屬性的其中一個有效大小。</span><span class="sxs-lookup"><span data-stu-id="e8036-123">This value should correspond to one of the valid sizes for the <em>SizeDefinition</em> attribute of the associated <a href="windowsribbon-element-group.md"><strong>Group</strong></a> of controls specified in <em>Group</em>.</span></span> <br/> <span data-ttu-id="e8036-124">限制為下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="e8036-124">Restricted to one of the following values:</span></span> <br/> <br/><span data-ttu-id="e8036-125">
<dt><span></span><span></span><strong></strong> (快顯視窗) </span><span class="sxs-lookup"><span data-stu-id="e8036-125">
<dt><span></span><span></span><strong></strong> (Popup)</span></span><br/> </dt> <dd> <span data-ttu-id="e8036-126">相同的控制項版面 <code>Large</code> 配置，但裝載于快顯視窗或下拉式窗格中。</span><span class="sxs-lookup"><span data-stu-id="e8036-126">Identical control layout to <code>Large</code> but hosted in a pop-up or a drop-down pane.</span></span><br/> </dd> <span data-ttu-id="e8036-127"><dt><span></span><span></span><strong></strong> (Small) </span><span class="sxs-lookup"><span data-stu-id="e8036-127"><dt><span></span><span></span><strong></strong> (Small)</span></span><br/> </dt> <dd> <span data-ttu-id="e8036-128">Small <a href="windowsribbon-element-sizedefinition.md"><strong>SizeDefinition</strong></a> 範本。</span><span class="sxs-lookup"><span data-stu-id="e8036-128">Small <a href="windowsribbon-element-sizedefinition.md"><strong>SizeDefinition</strong></a> template.</span></span><br/> </dd> <span data-ttu-id="e8036-129"><dt><span></span><span></span><strong></strong> (中) </span><span class="sxs-lookup"><span data-stu-id="e8036-129"><dt><span></span><span></span><strong></strong> (Medium)</span></span><br/> </dt> <dd> <span data-ttu-id="e8036-130">中型 <a href="windowsribbon-element-sizedefinition.md"><strong>SizeDefinition</strong></a> 範本。</span><span class="sxs-lookup"><span data-stu-id="e8036-130">Medium <a href="windowsribbon-element-sizedefinition.md"><strong>SizeDefinition</strong></a> template.</span></span><br/> </dd> <span data-ttu-id="e8036-131"><dt><span></span><span></span><strong></strong> (大型) </span><span class="sxs-lookup"><span data-stu-id="e8036-131"><dt><span></span><span></span><strong></strong> (Large)</span></span><br/> </dt> <dd> <span data-ttu-id="e8036-132">大型 <a href="windowsribbon-element-sizedefinition.md"><strong>SizeDefinition</strong></a> 範本。</span><span class="sxs-lookup"><span data-stu-id="e8036-132">Large <a href="windowsribbon-element-sizedefinition.md"><strong>SizeDefinition</strong></a> template.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="e8036-133">子元素</span><span class="sxs-lookup"><span data-stu-id="e8036-133">Child elements</span></span>

<span data-ttu-id="e8036-134">沒有任何子項目。</span><span class="sxs-lookup"><span data-stu-id="e8036-134">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="e8036-135">父元素</span><span class="sxs-lookup"><span data-stu-id="e8036-135">Parent elements</span></span>



| <span data-ttu-id="e8036-136">元素</span><span class="sxs-lookup"><span data-stu-id="e8036-136">Element</span></span>                                                                                       |
|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e8036-137">**ScalingPolicy**</span><span class="sxs-lookup"><span data-stu-id="e8036-137">**ScalingPolicy**</span></span>](windowsribbon-element-scalingpolicy.md)<br/>                       |
| [<span data-ttu-id="e8036-138">**ScalingPolicy. IdealSizes**</span><span class="sxs-lookup"><span data-stu-id="e8036-138">**ScalingPolicy.IdealSizes**</span></span>](windowsribbon-element-scalingpolicy-idealsizes.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="e8036-139">備註</span><span class="sxs-lookup"><span data-stu-id="e8036-139">Remarks</span></span>

<span data-ttu-id="e8036-140">選擇性。</span><span class="sxs-lookup"><span data-stu-id="e8036-140">Optional.</span></span>

<span data-ttu-id="e8036-141">每個 [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) 或 ScalingPolicy 可能會發生一次或多次 [**IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md)。</span><span class="sxs-lookup"><span data-stu-id="e8036-141">May occur one or more times for each [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) or [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md).</span></span>

<span data-ttu-id="e8036-142">每個 (群組、*大小*) 屬性 *組* 都必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="e8036-142">Each (*Group*, *Size*) attribute pair must be unique.</span></span>

## <a name="examples"></a><span data-ttu-id="e8036-143">範例</span><span class="sxs-lookup"><span data-stu-id="e8036-143">Examples</span></span>

<span data-ttu-id="e8036-144">下列範例示範如何透過功能區 [**SizeDefinition**](windowsribbon-element-sizedefinition.md)範本的自我調整配置功能，自訂 [**群組**](windowsribbon-element-group.md)中控制項的外觀。</span><span class="sxs-lookup"><span data-stu-id="e8036-144">The following example demonstrates how the appearance of controls in a [**Group**](windowsribbon-element-group.md) can be customized through the adaptive layout functionality of Ribbon [**SizeDefinition**](windowsribbon-element-sizedefinition.md) templates.</span></span>

<span data-ttu-id="e8036-145">此範例中的 [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md)資訊清單會針對 [**主** 資料夾] 索引標籤上的四個控制項群組，指定 [**ScalingPolicy. IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**SizeDefinition**](windowsribbon-element-sizedefinition.md)喜好設定。此外，也會指定 **小** 數位數元素，以影響每個群組的折迭行為（依遞減大小排序）。</span><span class="sxs-lookup"><span data-stu-id="e8036-145">The [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) manifest in this example specifies a [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**SizeDefinition**](windowsribbon-element-sizedefinition.md) preference for each of four groups of controls on a **Home** tab. In addition, **Scale** elements are specified to influence the collapsing behavior, in descending size order, of each group.</span></span>


```XML
<Tab CommandName="Home">
  <Tab.ScalingPolicy>
    <ScalingPolicy>
      <ScalingPolicy.IdealSizes>
        <Scale Group="GroupClipboard" Size="Medium"/>
        <Scale Group="GroupView" Size="Large"/>
        <Scale Group="GroupFont" Size="Large"/>
        <Scale Group="GroupParagraph" Size="Large"/>
      </ScalingPolicy.IdealSizes>
      <Scale Group="GroupClipboard" Size="Small"/>
      <Scale Group="GroupClipboard" Size="Popup"/>
      <Scale Group="GroupFont" Size="Medium"/>
      <Scale Group="GroupParagraph" Size="Medium"/>
      <!-- 
        GroupView group is associated with the OneButton SizeDefinition.
        Since this template is constrained to one size (Large) there
        is no need to declare further scaling preferences.
      -->
    </ScalingPolicy>
  </Tab.ScalingPolicy>

  <Group CommandName="GroupClipboard" SizeDefinition="FourButtons">
    <Button CommandName="Paste"/>
    <Button CommandName="Cut"/>
    <Button CommandName="Copy"/>
    <Button CommandName="SelectAll"/>
  </Group>

  <Group CommandName="GroupFont"  ApplicationModes="1">
    <FontControl CommandName="Font" FontType="FontWithColor" />
  </Group>

  <Group CommandName="GroupParagraph"  ApplicationModes="1" SizeDefinition="ButtonGroups">
    <ControlGroup>
      <ControlGroup>
        <ToggleButton CommandName="Numbered" />
        <ToggleButton CommandName="Bulleted" />
      </ControlGroup>
    </ControlGroup>
    <ControlGroup>
      <ControlGroup>
        <ToggleButton CommandName="LeftJustify" />
        <ToggleButton CommandName="CenterJustify" />
        <ToggleButton CommandName="RightJustify" />
      </ControlGroup>
      <ControlGroup/>
      <ControlGroup>
        <Button CommandName="Outdent" />
        <Button CommandName="Indent" />
      </ControlGroup>
    </ControlGroup>
  </Group>

  <Group CommandName="GroupView" SizeDefinition="OneButton" >
    <ToggleButton CommandName="ViewSource"/>
  </Group>

</Tab>
```



## <a name="element-information"></a><span data-ttu-id="e8036-146">項目資訊</span><span class="sxs-lookup"><span data-stu-id="e8036-146">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="e8036-147">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="e8036-147">Minimum supported system</span></span><br/> | <span data-ttu-id="e8036-148">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e8036-148">Windows 7</span></span> |
| <span data-ttu-id="e8036-149">可以是空的</span><span class="sxs-lookup"><span data-stu-id="e8036-149">Can be empty</span></span>                        | <span data-ttu-id="e8036-150">Yes</span><span class="sxs-lookup"><span data-stu-id="e8036-150">Yes</span></span>       |



## <a name="see-also"></a><span data-ttu-id="e8036-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e8036-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8036-152">透過大小定義和調整原則自訂功能區</span><span class="sxs-lookup"><span data-stu-id="e8036-152">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 






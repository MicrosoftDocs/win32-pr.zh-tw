---
title: ScalingPolicy. IdealSizes 屬性
description: 代表慣用 SizeDefinition 範本的縮放規格容器（以功能區大小為基礎）。
ms.assetid: a4aa2642-160d-4d81-9df9-29277911aa5a
keywords:
- ScalingPolicy. IdealSizes 屬性 Windows 功能區
topic_type:
- apiref
api_name:
- ScalingPolicy.IdealSizes
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7bf62cd0388b523f444c4a9cca226b58187212b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967360"
---
# <a name="scalingpolicyidealsizes-property"></a><span data-ttu-id="e9cca-104">ScalingPolicy. IdealSizes 屬性</span><span class="sxs-lookup"><span data-stu-id="e9cca-104">ScalingPolicy.IdealSizes property</span></span>

<span data-ttu-id="e9cca-105">代表慣用 [**SizeDefinition**](windowsribbon-element-sizedefinition.md) 範本的縮放規格容器（以功能區大小為基礎）。</span><span class="sxs-lookup"><span data-stu-id="e9cca-105">Represents a container of scaling specifications for the preferred [**SizeDefinition**](windowsribbon-element-sizedefinition.md) template, based on Ribbon size.</span></span>

## <a name="usage"></a><span data-ttu-id="e9cca-106">使用方式</span><span class="sxs-lookup"><span data-stu-id="e9cca-106">Usage</span></span>

``` syntax
<ScalingPolicy.IdealSizes>
  child elements
</ScalingPolicy.IdealSizes>
```

## <a name="attributes"></a><span data-ttu-id="e9cca-107">屬性</span><span class="sxs-lookup"><span data-stu-id="e9cca-107">Attributes</span></span>

<span data-ttu-id="e9cca-108">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="e9cca-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="e9cca-109">子元素</span><span class="sxs-lookup"><span data-stu-id="e9cca-109">Child elements</span></span>



| <span data-ttu-id="e9cca-110">元素</span><span class="sxs-lookup"><span data-stu-id="e9cca-110">Element</span></span>                                                 | <span data-ttu-id="e9cca-111">描述</span><span class="sxs-lookup"><span data-stu-id="e9cca-111">Description</span></span>                                        |
|---------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="e9cca-112">**調整**</span><span class="sxs-lookup"><span data-stu-id="e9cca-112">**Scale**</span></span>](windowsribbon-element-scale.md)<br/> | <span data-ttu-id="e9cca-113">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="e9cca-113">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="e9cca-114">父元素</span><span class="sxs-lookup"><span data-stu-id="e9cca-114">Parent elements</span></span>



| <span data-ttu-id="e9cca-115">元素</span><span class="sxs-lookup"><span data-stu-id="e9cca-115">Element</span></span>                                                                 |
|-------------------------------------------------------------------------|
| [<span data-ttu-id="e9cca-116">**ScalingPolicy**</span><span class="sxs-lookup"><span data-stu-id="e9cca-116">**ScalingPolicy**</span></span>](windowsribbon-element-scalingpolicy.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="e9cca-117">備註</span><span class="sxs-lookup"><span data-stu-id="e9cca-117">Remarks</span></span>

<span data-ttu-id="e9cca-118">選擇性。</span><span class="sxs-lookup"><span data-stu-id="e9cca-118">Optional.</span></span>

<span data-ttu-id="e9cca-119">每個 [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md)最多可能會發生一次。</span><span class="sxs-lookup"><span data-stu-id="e9cca-119">May occur at most once for each [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md).</span></span>

<span data-ttu-id="e9cca-120">如果已定義 **ScalingPolicy** ，則必須在索引標籤 [**元素中的每**](windowsribbon-element-tab.md)個 [**群組**](windowsribbon-element-group.md)元素都有一個 [**小**](windowsribbon-element-scale.md)數位數專案。</span><span class="sxs-lookup"><span data-stu-id="e9cca-120">If **ScalingPolicy.IdealSizes** is defined, then a [**Scale**](windowsribbon-element-scale.md) entry for each [**Group**](windowsribbon-element-group.md) element in a [**Tab**](windowsribbon-element-tab.md) element must be present.</span></span>

<span data-ttu-id="e9cca-121">**ScalingPolicy** 是控制項 [**群組**](windowsribbon-element-group.md)的慣用 [**SizeDefinition**](windowsribbon-element-sizedefinition.md)版面配置。</span><span class="sxs-lookup"><span data-stu-id="e9cca-121">**ScalingPolicy.IdealSizes** are the preferred [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layouts for a [**Group**](windowsribbon-element-group.md) of controls.</span></span>

## <a name="examples"></a><span data-ttu-id="e9cca-122">範例</span><span class="sxs-lookup"><span data-stu-id="e9cca-122">Examples</span></span>

<span data-ttu-id="e9cca-123">下列範例示範如何透過功能區 [**SizeDefinition**](windowsribbon-element-sizedefinition.md)範本的自我調整配置功能，自訂 [**群組**](windowsribbon-element-group.md)中控制項的外觀。</span><span class="sxs-lookup"><span data-stu-id="e9cca-123">The following example demonstrates how the appearance of controls in a [**Group**](windowsribbon-element-group.md) can be customized through the adaptive layout functionality of Ribbon [**SizeDefinition**](windowsribbon-element-sizedefinition.md) templates.</span></span>

<span data-ttu-id="e9cca-124">此範例中的 [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md)資訊清單會針對 [**主** 資料夾] 索引標籤上的四個控制項群組，指定 **ScalingPolicy. IdealSizes** [**SizeDefinition**](windowsribbon-element-sizedefinition.md)喜好設定。此外，也會指定 [**小**](windowsribbon-element-scale.md)數位數元素，以影響每個群組的折迭行為（依遞減大小排序）。</span><span class="sxs-lookup"><span data-stu-id="e9cca-124">The [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) manifest in this example specifies a **ScalingPolicy.IdealSizes** [**SizeDefinition**](windowsribbon-element-sizedefinition.md) preference for each of four groups of controls on a **Home** tab. In addition, [**Scale**](windowsribbon-element-scale.md) elements are specified to influence the collapsing behavior, in descending size order, of each group.</span></span>


```C++
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



## <a name="requirements"></a><span data-ttu-id="e9cca-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="e9cca-125">Requirements</span></span>



| <span data-ttu-id="e9cca-126">需求</span><span class="sxs-lookup"><span data-stu-id="e9cca-126">Requirement</span></span> | <span data-ttu-id="e9cca-127">值</span><span class="sxs-lookup"><span data-stu-id="e9cca-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="e9cca-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e9cca-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e9cca-129">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e9cca-129">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="e9cca-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e9cca-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e9cca-131">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e9cca-131">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e9cca-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e9cca-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9cca-133">透過大小定義和調整原則自訂功能區</span><span class="sxs-lookup"><span data-stu-id="e9cca-133">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 






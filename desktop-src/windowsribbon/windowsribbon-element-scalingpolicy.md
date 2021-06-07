---
title: ScalingPolicy 項目
description: 表示用於調整規格的容器。
ms.assetid: 133e7994-9901-43e8-82b0-3d910cf8758e
keywords:
- ScalingPolicy 元素視窗功能區
topic_type:
- apiref
api_name:
- ScalingPolicy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 812256b0ff329073eb516c6ab2eb7501db8de40d
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444989"
---
# <a name="scalingpolicy-element"></a><span data-ttu-id="fc67e-104">ScalingPolicy 項目</span><span class="sxs-lookup"><span data-stu-id="fc67e-104">ScalingPolicy element</span></span>

<span data-ttu-id="fc67e-105">表示用於調整規格的容器。</span><span class="sxs-lookup"><span data-stu-id="fc67e-105">Represents a container for scaling specifications.</span></span>

## <a name="usage"></a><span data-ttu-id="fc67e-106">使用方式</span><span class="sxs-lookup"><span data-stu-id="fc67e-106">Usage</span></span>

``` syntax
<ScalingPolicy>
  child elements
</ScalingPolicy>
```

## <a name="attributes"></a><span data-ttu-id="fc67e-107">屬性</span><span class="sxs-lookup"><span data-stu-id="fc67e-107">Attributes</span></span>

<span data-ttu-id="fc67e-108">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="fc67e-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="fc67e-109">子元素</span><span class="sxs-lookup"><span data-stu-id="fc67e-109">Child elements</span></span>



| <span data-ttu-id="fc67e-110">元素</span><span class="sxs-lookup"><span data-stu-id="fc67e-110">Element</span></span>                                                                                       | <span data-ttu-id="fc67e-111">描述</span><span class="sxs-lookup"><span data-stu-id="fc67e-111">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="fc67e-112">**調整**</span><span class="sxs-lookup"><span data-stu-id="fc67e-112">**Scale**</span></span>](windowsribbon-element-scale.md)<br/>                                       | <span data-ttu-id="fc67e-113">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="fc67e-113">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="fc67e-114">**ScalingPolicy. IdealSizes**</span><span class="sxs-lookup"><span data-stu-id="fc67e-114">**ScalingPolicy.IdealSizes**</span></span>](windowsribbon-element-scalingpolicy-idealsizes.md)<br/> | <span data-ttu-id="fc67e-115">最多可能發生一次</span><span class="sxs-lookup"><span data-stu-id="fc67e-115">May occur at most once</span></span><br/> <br/>      |



## <a name="parent-elements"></a><span data-ttu-id="fc67e-116">父元素</span><span class="sxs-lookup"><span data-stu-id="fc67e-116">Parent elements</span></span>



| <span data-ttu-id="fc67e-117">元素</span><span class="sxs-lookup"><span data-stu-id="fc67e-117">Element</span></span>                                                                         |
|---------------------------------------------------------------------------------|
| [<span data-ttu-id="fc67e-118">**ScalingPolicy**</span><span class="sxs-lookup"><span data-stu-id="fc67e-118">**Tab.ScalingPolicy**</span></span>](windowsribbon-element-tab-scalingpolicy.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="fc67e-119">備註</span><span class="sxs-lookup"><span data-stu-id="fc67e-119">Remarks</span></span>

<span data-ttu-id="fc67e-120">必要。</span><span class="sxs-lookup"><span data-stu-id="fc67e-120">Required.</span></span>

<span data-ttu-id="fc67e-121">每個 [**ScalingPolicy**](windowsribbon-element-tab-scalingpolicy.md)都必須發生一次。</span><span class="sxs-lookup"><span data-stu-id="fc67e-121">Must occur once for each [**Tab.ScalingPolicy**](windowsribbon-element-tab-scalingpolicy.md).</span></span>

<span data-ttu-id="fc67e-122">**ScalingPolicy** 元素包含 [**ScalingPolicy**](windowsribbon-element-scalingpolicy-idealsizes.md)的資訊清單，並在調整大小功能區 [**時，指定**](windowsribbon-element-scale.md)一或多個 [**群組**](windowsribbon-element-group.md)元素的自我調整版面配置喜好設定。</span><span class="sxs-lookup"><span data-stu-id="fc67e-122">The **ScalingPolicy** element contains a manifest of [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) and [**Scale**](windowsribbon-element-scale.md) declarations that specify adaptive layout preferences for one or more [**Group**](windowsribbon-element-group.md) elements when the Ribbon is resized.</span></span>

<span data-ttu-id="fc67e-123">[**調整規模**](windowsribbon-element-scale.md)宣告的清單必須是有效大小的遞減順序， (大型、中型、小型、快顯視窗) 與 [**群組**](windowsribbon-element-group.md)專案相關聯的 [**SizeDefinition**](windowsribbon-element-sizedefinition.md) 。</span><span class="sxs-lookup"><span data-stu-id="fc67e-123">The list of [**Scale**](windowsribbon-element-scale.md) declarations must be in descending order of valid sizes (Large, Medium, Small, Popup) for the [**SizeDefinition**](windowsribbon-element-sizedefinition.md) associated with the [**Group**](windowsribbon-element-group.md) element.</span></span>

> [!Note]  
> <span data-ttu-id="fc67e-124">強烈建議您指定適當的調整原則詳細資料，讓功能區可以在調整大小為 300 96 圖元的寬度時，不需要捲軸， (DPI) 。</span><span class="sxs-lookup"><span data-stu-id="fc67e-124">It is highly recommended that adequate scaling policy detail be specified such that a Ribbon is able to render without scroll bars when resized to a width of 300 pixels at 96 dots per inch (dpi).</span></span>

 

## <a name="examples"></a><span data-ttu-id="fc67e-125">範例</span><span class="sxs-lookup"><span data-stu-id="fc67e-125">Examples</span></span>

<span data-ttu-id="fc67e-126">下列範例示範如何透過功能區 [**SizeDefinition**](windowsribbon-element-sizedefinition.md)範本的自我調整配置功能，自訂 [**群組**](windowsribbon-element-group.md)中控制項的外觀。</span><span class="sxs-lookup"><span data-stu-id="fc67e-126">The following example demonstrates how the appearance of controls in a [**Group**](windowsribbon-element-group.md) can be customized through the adaptive layout functionality of Ribbon [**SizeDefinition**](windowsribbon-element-sizedefinition.md) templates.</span></span>

<span data-ttu-id="fc67e-127">此範例中的 **ScalingPolicy** 資訊清單會針對 [**主** 資料夾] 索引標籤上的四個控制項群組，指定 [**ScalingPolicy. IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**SizeDefinition**](windowsribbon-element-sizedefinition.md)喜好設定。此外，也會指定 [**小**](windowsribbon-element-scale.md)數位數元素，以影響每個群組的折迭行為（依遞減大小排序）。</span><span class="sxs-lookup"><span data-stu-id="fc67e-127">The **ScalingPolicy** manifest in this example specifies a [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**SizeDefinition**](windowsribbon-element-sizedefinition.md) preference for each of four groups of controls on a **Home** tab. In addition, [**Scale**](windowsribbon-element-scale.md) elements are specified to influence the collapsing behavior, in descending size order, of each group.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="fc67e-128">項目資訊</span><span class="sxs-lookup"><span data-stu-id="fc67e-128">Element information</span></span>

- <span data-ttu-id="fc67e-129">**最低支援系統**： Windows 7</span><span class="sxs-lookup"><span data-stu-id="fc67e-129">**Minimum supported system**: Windows 7</span></span> 
- <span data-ttu-id="fc67e-130">**可以是空** 的：否</span><span class="sxs-lookup"><span data-stu-id="fc67e-130">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="fc67e-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fc67e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc67e-132">透過大小定義和調整原則自訂功能區</span><span class="sxs-lookup"><span data-stu-id="fc67e-132">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 






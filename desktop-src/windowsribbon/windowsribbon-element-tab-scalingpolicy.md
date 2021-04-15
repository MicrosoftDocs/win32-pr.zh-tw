---
title: ScalingPolicy 屬性
description: 表示索引標籤調整規格的容器。
ms.assetid: cc1e4a35-9348-459b-a2f1-25c34d49e5e8
keywords:
- ScalingPolicy 屬性視窗功能區
topic_type:
- apiref
api_name:
- Tab.ScalingPolicy
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c46528e7b5957415db55f1a51dd6dafed7e1da98
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466568"
---
# <a name="tabscalingpolicy-property"></a><span data-ttu-id="63b17-104">ScalingPolicy 屬性</span><span class="sxs-lookup"><span data-stu-id="63b17-104">Tab.ScalingPolicy property</span></span>

<span data-ttu-id="63b17-105">表示索引 [標籤調整規格的容器](windowsribbon-controls-tab.md) 。</span><span class="sxs-lookup"><span data-stu-id="63b17-105">Represents a container for [Tab](windowsribbon-controls-tab.md) scaling specifications.</span></span>

## <a name="usage"></a><span data-ttu-id="63b17-106">使用方式</span><span class="sxs-lookup"><span data-stu-id="63b17-106">Usage</span></span>

``` syntax
<Tab.ScalingPolicy>
  child elements
</Tab.ScalingPolicy>
```

## <a name="attributes"></a><span data-ttu-id="63b17-107">屬性</span><span class="sxs-lookup"><span data-stu-id="63b17-107">Attributes</span></span>

<span data-ttu-id="63b17-108">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="63b17-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="63b17-109">子元素</span><span class="sxs-lookup"><span data-stu-id="63b17-109">Child elements</span></span>



| <span data-ttu-id="63b17-110">元素</span><span class="sxs-lookup"><span data-stu-id="63b17-110">Element</span></span>                                                                 | <span data-ttu-id="63b17-111">描述</span><span class="sxs-lookup"><span data-stu-id="63b17-111">Description</span></span>                                    |
|-------------------------------------------------------------------------|------------------------------------------------|
| [<span data-ttu-id="63b17-112">**ScalingPolicy**</span><span class="sxs-lookup"><span data-stu-id="63b17-112">**ScalingPolicy**</span></span>](windowsribbon-element-scalingpolicy.md)<br/> | <span data-ttu-id="63b17-113">必須剛好發生一次</span><span class="sxs-lookup"><span data-stu-id="63b17-113">Must occur exactly once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="63b17-114">父元素</span><span class="sxs-lookup"><span data-stu-id="63b17-114">Parent elements</span></span>



| <span data-ttu-id="63b17-115">元素</span><span class="sxs-lookup"><span data-stu-id="63b17-115">Element</span></span>                                             |
|-----------------------------------------------------|
| [<span data-ttu-id="63b17-116">**索引標籤**</span><span class="sxs-lookup"><span data-stu-id="63b17-116">**Tab**</span></span>](windowsribbon-element-tab.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="63b17-117">備註</span><span class="sxs-lookup"><span data-stu-id="63b17-117">Remarks</span></span>

<span data-ttu-id="63b17-118">選擇性。</span><span class="sxs-lookup"><span data-stu-id="63b17-118">Optional.</span></span>

<span data-ttu-id="63b17-119">每個索引標籤最多可能會 [**發生一次**](windowsribbon-element-tab.md)。</span><span class="sxs-lookup"><span data-stu-id="63b17-119">May occur at most once for each [**Tab**](windowsribbon-element-tab.md).</span></span>

<span data-ttu-id="63b17-120">調整規格會描述在調整大小功能 [區時，](windowsribbon-controls-tab.md) 索引標籤中控制項的大小和版面配置行為。</span><span class="sxs-lookup"><span data-stu-id="63b17-120">Scaling specifications describe the size and layout behavior for the controls in a [Tab](windowsribbon-controls-tab.md) when the Ribbon is resized.</span></span>

## <a name="examples"></a><span data-ttu-id="63b17-121">範例</span><span class="sxs-lookup"><span data-stu-id="63b17-121">Examples</span></span>

<span data-ttu-id="63b17-122">下列程式碼範例會示範 [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md)資訊清單，該資訊清單會針對 [**主** 資料夾] 索引標籤上的四個控制項群組，指定 [**ScalingPolicy. IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**SizeDefinition**](windowsribbon-element-sizedefinition.md)喜好設定。此外，也會指定 [**小**](windowsribbon-element-scale.md)數位數元素，以影響每個群組的折迭行為（依遞減大小排序）。</span><span class="sxs-lookup"><span data-stu-id="63b17-122">The following code example demonstrates a [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) manifest that specifies a [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**SizeDefinition**](windowsribbon-element-sizedefinition.md) preference for each of four groups of controls on a **Home** tab. In addition, [**Scale**](windowsribbon-element-scale.md) elements are specified to influence the collapsing behavior, in descending size order, of each group.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="63b17-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="63b17-123">Requirements</span></span>



| <span data-ttu-id="63b17-124">需求</span><span class="sxs-lookup"><span data-stu-id="63b17-124">Requirement</span></span> | <span data-ttu-id="63b17-125">值</span><span class="sxs-lookup"><span data-stu-id="63b17-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="63b17-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="63b17-126">Minimum supported client</span></span><br/> | <span data-ttu-id="63b17-127">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="63b17-127">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="63b17-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="63b17-128">Minimum supported server</span></span><br/> | <span data-ttu-id="63b17-129">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="63b17-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="63b17-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="63b17-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63b17-131">透過大小定義和調整原則自訂功能區</span><span class="sxs-lookup"><span data-stu-id="63b17-131">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 






---
title: Row 元素
description: 代表自訂 SizeDefinition 版面配置範本中的一列控制項。
ms.assetid: c3dac35f-3537-4eb7-b378-501ea88813f5
keywords:
- 資料列元素視窗功能區
topic_type:
- apiref
api_name:
- Row
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7d642cd209b3e00e2c63f7376e321132a1c0e686
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111445019"
---
# <a name="row-element"></a><span data-ttu-id="c2951-104">Row 元素</span><span class="sxs-lookup"><span data-stu-id="c2951-104">Row element</span></span>

<span data-ttu-id="c2951-105">代表自訂 SizeDefinition 版面配置範本中的一列控制項。</span><span class="sxs-lookup"><span data-stu-id="c2951-105">Represents a row of controls in a custom SizeDefinition layout template.</span></span>

## <a name="usage"></a><span data-ttu-id="c2951-106">使用方式</span><span class="sxs-lookup"><span data-stu-id="c2951-106">Usage</span></span>

``` syntax
<Row>
  child elements
</Row>
```

## <a name="attributes"></a><span data-ttu-id="c2951-107">屬性</span><span class="sxs-lookup"><span data-stu-id="c2951-107">Attributes</span></span>

<span data-ttu-id="c2951-108">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="c2951-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="c2951-109">子元素</span><span class="sxs-lookup"><span data-stu-id="c2951-109">Child elements</span></span>



| <span data-ttu-id="c2951-110">元素</span><span class="sxs-lookup"><span data-stu-id="c2951-110">Element</span></span>                                                                                 | <span data-ttu-id="c2951-111">描述</span><span class="sxs-lookup"><span data-stu-id="c2951-111">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="c2951-112">**ControlGroup**</span><span class="sxs-lookup"><span data-stu-id="c2951-112">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>                   | <span data-ttu-id="c2951-113">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="c2951-113">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="c2951-114">**ControlSizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="c2951-114">**ControlSizeDefinition**</span></span>](windowsribbon-element-controlsizedefinition.md)<br/> | <span data-ttu-id="c2951-115">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="c2951-115">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="c2951-116">父元素</span><span class="sxs-lookup"><span data-stu-id="c2951-116">Parent elements</span></span>



| <span data-ttu-id="c2951-117">元素</span><span class="sxs-lookup"><span data-stu-id="c2951-117">Element</span></span>                                                                             |
|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="c2951-118">**GroupSizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="c2951-118">**GroupSizeDefinition**</span></span>](windowsribbon-element-groupsizedefinition.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="c2951-119">備註</span><span class="sxs-lookup"><span data-stu-id="c2951-119">Remarks</span></span>

<span data-ttu-id="c2951-120">選擇性。</span><span class="sxs-lookup"><span data-stu-id="c2951-120">Optional.</span></span>

<span data-ttu-id="c2951-121">每個 [**GroupSizeDefinition**](windowsribbon-element-groupsizedefinition.md) 專案可能會發生一次或多次。</span><span class="sxs-lookup"><span data-stu-id="c2951-121">May occur one or more times for each [**GroupSizeDefinition**](windowsribbon-element-groupsizedefinition.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="c2951-122">範例</span><span class="sxs-lookup"><span data-stu-id="c2951-122">Examples</span></span>

<span data-ttu-id="c2951-123">下列程式碼範例將示範具有各種資料 **列** 元素之自訂四按鈕 [**SizeDefinition**](windowsribbon-element-sizedefinition.md)版面配置範本的基本標記。</span><span class="sxs-lookup"><span data-stu-id="c2951-123">The following code example demonstrates the basic markup for a custom four-button [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layout template with various **Row** elements.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="c2951-124">項目資訊</span><span class="sxs-lookup"><span data-stu-id="c2951-124">Element information</span></span>




* <span data-ttu-id="c2951-125">**最低支援系統**： Windows 7</span><span class="sxs-lookup"><span data-stu-id="c2951-125">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="c2951-126">**可以是空** 的：否</span><span class="sxs-lookup"><span data-stu-id="c2951-126">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="c2951-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c2951-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2951-128">透過大小定義和調整原則自訂功能區</span><span class="sxs-lookup"><span data-stu-id="c2951-128">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 






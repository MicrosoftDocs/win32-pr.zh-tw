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
ms.openlocfilehash: 83a0a5a9e7908cc1c8cff688b3fefc1e8910b6a4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "106968874"
---
# <a name="row-element"></a><span data-ttu-id="7a75b-104">Row 元素</span><span class="sxs-lookup"><span data-stu-id="7a75b-104">Row element</span></span>

<span data-ttu-id="7a75b-105">代表自訂 SizeDefinition 版面配置範本中的一列控制項。</span><span class="sxs-lookup"><span data-stu-id="7a75b-105">Represents a row of controls in a custom SizeDefinition layout template.</span></span>

## <a name="usage"></a><span data-ttu-id="7a75b-106">使用方式</span><span class="sxs-lookup"><span data-stu-id="7a75b-106">Usage</span></span>

``` syntax
<Row>
  child elements
</Row>
```

## <a name="attributes"></a><span data-ttu-id="7a75b-107">屬性</span><span class="sxs-lookup"><span data-stu-id="7a75b-107">Attributes</span></span>

<span data-ttu-id="7a75b-108">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="7a75b-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="7a75b-109">子元素</span><span class="sxs-lookup"><span data-stu-id="7a75b-109">Child elements</span></span>



| <span data-ttu-id="7a75b-110">元素</span><span class="sxs-lookup"><span data-stu-id="7a75b-110">Element</span></span>                                                                                 | <span data-ttu-id="7a75b-111">描述</span><span class="sxs-lookup"><span data-stu-id="7a75b-111">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="7a75b-112">**ControlGroup**</span><span class="sxs-lookup"><span data-stu-id="7a75b-112">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>                   | <span data-ttu-id="7a75b-113">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="7a75b-113">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="7a75b-114">**ControlSizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="7a75b-114">**ControlSizeDefinition**</span></span>](windowsribbon-element-controlsizedefinition.md)<br/> | <span data-ttu-id="7a75b-115">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="7a75b-115">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="7a75b-116">父元素</span><span class="sxs-lookup"><span data-stu-id="7a75b-116">Parent elements</span></span>



| <span data-ttu-id="7a75b-117">元素</span><span class="sxs-lookup"><span data-stu-id="7a75b-117">Element</span></span>                                                                             |
|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="7a75b-118">**GroupSizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="7a75b-118">**GroupSizeDefinition**</span></span>](windowsribbon-element-groupsizedefinition.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="7a75b-119">備註</span><span class="sxs-lookup"><span data-stu-id="7a75b-119">Remarks</span></span>

<span data-ttu-id="7a75b-120">選擇性。</span><span class="sxs-lookup"><span data-stu-id="7a75b-120">Optional.</span></span>

<span data-ttu-id="7a75b-121">每個 [**GroupSizeDefinition**](windowsribbon-element-groupsizedefinition.md) 專案可能會發生一次或多次。</span><span class="sxs-lookup"><span data-stu-id="7a75b-121">May occur one or more times for each [**GroupSizeDefinition**](windowsribbon-element-groupsizedefinition.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="7a75b-122">範例</span><span class="sxs-lookup"><span data-stu-id="7a75b-122">Examples</span></span>

<span data-ttu-id="7a75b-123">下列程式碼範例將示範具有各種資料 **列** 元素之自訂四按鈕 [**SizeDefinition**](windowsribbon-element-sizedefinition.md)版面配置範本的基本標記。</span><span class="sxs-lookup"><span data-stu-id="7a75b-123">The following code example demonstrates the basic markup for a custom four-button [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layout template with various **Row** elements.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="7a75b-124">項目資訊</span><span class="sxs-lookup"><span data-stu-id="7a75b-124">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="7a75b-125">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="7a75b-125">Minimum supported system</span></span><br/> | <span data-ttu-id="7a75b-126">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7a75b-126">Windows 7</span></span> |
| <span data-ttu-id="7a75b-127">可以是空的</span><span class="sxs-lookup"><span data-stu-id="7a75b-127">Can be empty</span></span>                        | <span data-ttu-id="7a75b-128">否</span><span class="sxs-lookup"><span data-stu-id="7a75b-128">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="7a75b-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7a75b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a75b-130">透過大小定義和調整原則自訂功能區</span><span class="sxs-lookup"><span data-stu-id="7a75b-130">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 






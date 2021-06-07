---
title: ControlNameDefinition 元素
description: 表示自訂 SizeDefinition 版面配置範本中的控制項名稱。
ms.assetid: 94b724bd-a4e3-40e0-9cf0-3cc6a71100d2
keywords:
- ControlNameDefinition 元素視窗功能區
topic_type:
- apiref
api_name:
- ControlNameDefinition
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6b2dc1db251d4d657c3793d2a66a9add1d324c37
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443439"
---
# <a name="controlnamedefinition-element"></a><span data-ttu-id="959ab-104">ControlNameDefinition 元素</span><span class="sxs-lookup"><span data-stu-id="959ab-104">ControlNameDefinition element</span></span>

<span data-ttu-id="959ab-105">表示自訂 [**SizeDefinition**](windowsribbon-element-sizedefinition.md) 版面配置範本中的控制項名稱。</span><span class="sxs-lookup"><span data-stu-id="959ab-105">Represents a name of a control in a custom [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layout template.</span></span>

## <a name="usage"></a><span data-ttu-id="959ab-106">使用方式</span><span class="sxs-lookup"><span data-stu-id="959ab-106">Usage</span></span>

``` syntax
<ControlNameDefinition
  Name = "xs:positiveInteger or xs:string">
  child elements
</ControlNameDefinition>
```

## <a name="attributes"></a><span data-ttu-id="959ab-107">屬性</span><span class="sxs-lookup"><span data-stu-id="959ab-107">Attributes</span></span>



| <span data-ttu-id="959ab-108">屬性</span><span class="sxs-lookup"><span data-stu-id="959ab-108">Attribute</span></span>           | <span data-ttu-id="959ab-109">類型</span><span class="sxs-lookup"><span data-stu-id="959ab-109">Type</span></span>                                       | <span data-ttu-id="959ab-110">必要</span><span class="sxs-lookup"><span data-stu-id="959ab-110">Required</span></span>      | <span data-ttu-id="959ab-111">描述</span><span class="sxs-lookup"><span data-stu-id="959ab-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                           |
|---------------------|--------------------------------------------|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="959ab-112">**名稱**</span><span class="sxs-lookup"><span data-stu-id="959ab-112">**Name**</span></span><br/> | <span data-ttu-id="959ab-113">xs： positiveInteger 或 xs： string</span><span class="sxs-lookup"><span data-stu-id="959ab-113">xs:positiveInteger or xs:string</span></span><br/> | <span data-ttu-id="959ab-114">否</span><span class="sxs-lookup"><span data-stu-id="959ab-114">No</span></span><br/> | <span data-ttu-id="959ab-115"><dt> (xs： positiveInteger 或 xs： string) </span><span class="sxs-lookup"><span data-stu-id="959ab-115"><dt> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="959ab-116">字串、介於2與59999（含）之間的整數值，或介於0x2 與0xea5f （含）之間的十六進位值。</span><span class="sxs-lookup"><span data-stu-id="959ab-116">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="959ab-117">值在功能區 XML 檔中必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="959ab-117">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="959ab-118">最大長度：100個字元。</span><span class="sxs-lookup"><span data-stu-id="959ab-118">Maximum length: 100 characters.</span></span> <br/> </dd> </dl> |



## <a name="child-elements"></a><span data-ttu-id="959ab-119">子元素</span><span class="sxs-lookup"><span data-stu-id="959ab-119">Child elements</span></span>



| <span data-ttu-id="959ab-120">元素</span><span class="sxs-lookup"><span data-stu-id="959ab-120">Element</span></span>                              | <span data-ttu-id="959ab-121">描述</span><span class="sxs-lookup"><span data-stu-id="959ab-121">Description</span></span>                                        |
|--------------------------------------|----------------------------------------------------|
| <span data-ttu-id="959ab-122">**ControlNameDefinition**</span><span class="sxs-lookup"><span data-stu-id="959ab-122">**ControlNameDefinition**</span></span><br/> | <span data-ttu-id="959ab-123">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="959ab-123">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="959ab-124">父元素</span><span class="sxs-lookup"><span data-stu-id="959ab-124">Parent elements</span></span>



| <span data-ttu-id="959ab-125">元素</span><span class="sxs-lookup"><span data-stu-id="959ab-125">Element</span></span>                                                                   |
|---------------------------------------------------------------------------|
| [<span data-ttu-id="959ab-126">**ControlNameMap**</span><span class="sxs-lookup"><span data-stu-id="959ab-126">**ControlNameMap**</span></span>](windowsribbon-element-controlnamemap.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="959ab-127">備註</span><span class="sxs-lookup"><span data-stu-id="959ab-127">Remarks</span></span>

<span data-ttu-id="959ab-128">選擇性。</span><span class="sxs-lookup"><span data-stu-id="959ab-128">Optional.</span></span>

<span data-ttu-id="959ab-129">每個 [**ControlNameMap**](windowsribbon-element-controlnamemap.md) 專案可能會發生一次或多次。</span><span class="sxs-lookup"><span data-stu-id="959ab-129">May occur one or more times for each [**ControlNameMap**](windowsribbon-element-controlnamemap.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="959ab-130">範例</span><span class="sxs-lookup"><span data-stu-id="959ab-130">Examples</span></span>

<span data-ttu-id="959ab-131">下列程式碼範例示範具有四個 **ControlNameDefinition** 元素之自訂四個按鈕 [**SizeDefinition**](windowsribbon-element-sizedefinition.md)版面配置範本的基本標記。</span><span class="sxs-lookup"><span data-stu-id="959ab-131">The following code example demonstrates the basic markup for a custom four-button [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layout template with four **ControlNameDefinition** elements.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="959ab-132">項目資訊</span><span class="sxs-lookup"><span data-stu-id="959ab-132">Element information</span></span>

* <span data-ttu-id="959ab-133">**最低支援系統**： Windows 7</span><span class="sxs-lookup"><span data-stu-id="959ab-133">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="959ab-134">**可以是空** 的：否</span><span class="sxs-lookup"><span data-stu-id="959ab-134">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="959ab-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="959ab-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="959ab-136">透過大小定義和調整原則自訂功能區</span><span class="sxs-lookup"><span data-stu-id="959ab-136">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 






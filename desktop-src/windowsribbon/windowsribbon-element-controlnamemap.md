---
title: ControlNameMap 元素
description: 表示自訂 SizeDefinition 版面配置範本中控制項名稱的容器。
ms.assetid: b4bceb90-a9a3-42d7-a85b-bf6e4e02784b
keywords:
- ControlNameMap 元素視窗功能區
topic_type:
- apiref
api_name:
- ControlNameMap
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 42654af7f81730d01f9c699de7041ba24be185e9
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111442909"
---
# <a name="controlnamemap-element"></a><span data-ttu-id="a63a1-104">ControlNameMap 元素</span><span class="sxs-lookup"><span data-stu-id="a63a1-104">ControlNameMap element</span></span>

<span data-ttu-id="a63a1-105">表示自訂 [**SizeDefinition**](windowsribbon-element-sizedefinition.md) 版面配置範本中控制項名稱的容器。</span><span class="sxs-lookup"><span data-stu-id="a63a1-105">Represents a container for control names in a custom [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layout template.</span></span>

## <a name="usage"></a><span data-ttu-id="a63a1-106">使用方式</span><span class="sxs-lookup"><span data-stu-id="a63a1-106">Usage</span></span>

``` syntax
<ControlNameMap>
  child elements
</ControlNameMap>
```

## <a name="attributes"></a><span data-ttu-id="a63a1-107">屬性</span><span class="sxs-lookup"><span data-stu-id="a63a1-107">Attributes</span></span>

<span data-ttu-id="a63a1-108">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="a63a1-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="a63a1-109">子元素</span><span class="sxs-lookup"><span data-stu-id="a63a1-109">Child elements</span></span>



| <span data-ttu-id="a63a1-110">元素</span><span class="sxs-lookup"><span data-stu-id="a63a1-110">Element</span></span>                                                                                 | <span data-ttu-id="a63a1-111">描述</span><span class="sxs-lookup"><span data-stu-id="a63a1-111">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="a63a1-112">**ControlNameDefinition**</span><span class="sxs-lookup"><span data-stu-id="a63a1-112">**ControlNameDefinition**</span></span>](windowsribbon-element-controlnamedefinition.md)<br/> | <span data-ttu-id="a63a1-113">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="a63a1-113">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="a63a1-114">父元素</span><span class="sxs-lookup"><span data-stu-id="a63a1-114">Parent elements</span></span>



| <span data-ttu-id="a63a1-115">元素</span><span class="sxs-lookup"><span data-stu-id="a63a1-115">Element</span></span>                                                                   |
|---------------------------------------------------------------------------|
| [<span data-ttu-id="a63a1-116">**SizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="a63a1-116">**SizeDefinition**</span></span>](windowsribbon-element-sizedefinition.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="a63a1-117">備註</span><span class="sxs-lookup"><span data-stu-id="a63a1-117">Remarks</span></span>

<span data-ttu-id="a63a1-118">選擇性。</span><span class="sxs-lookup"><span data-stu-id="a63a1-118">Optional.</span></span>

<span data-ttu-id="a63a1-119">每個 [**SizeDefinition**](windowsribbon-element-sizedefinition.md) 元素最多可能會發生一次。</span><span class="sxs-lookup"><span data-stu-id="a63a1-119">May occur at most once for each [**SizeDefinition**](windowsribbon-element-sizedefinition.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="a63a1-120">範例</span><span class="sxs-lookup"><span data-stu-id="a63a1-120">Examples</span></span>

<span data-ttu-id="a63a1-121">下列程式碼範例示範具有 **ControlNameMap** 元素之自訂四個按鈕 [**SizeDefinition**](windowsribbon-element-sizedefinition.md)版面配置範本的基本標記。</span><span class="sxs-lookup"><span data-stu-id="a63a1-121">The following code example demonstrates the basic markup for a custom four-button [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layout template with a **ControlNameMap** element.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="a63a1-122">項目資訊</span><span class="sxs-lookup"><span data-stu-id="a63a1-122">Element information</span></span>

* <span data-ttu-id="a63a1-123">**最低支援系統**： Windows 7</span><span class="sxs-lookup"><span data-stu-id="a63a1-123">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="a63a1-124">**可以是空** 的：否</span><span class="sxs-lookup"><span data-stu-id="a63a1-124">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="a63a1-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a63a1-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a63a1-126">透過大小定義和調整原則自訂功能區</span><span class="sxs-lookup"><span data-stu-id="a63a1-126">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 






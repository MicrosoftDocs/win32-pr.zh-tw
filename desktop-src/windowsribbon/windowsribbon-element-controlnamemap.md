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
ms.openlocfilehash: 7ca5338978be7f9ddf3432cbe1a0fb8d243d8c00
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103841303"
---
# <a name="controlnamemap-element"></a><span data-ttu-id="f3135-104">ControlNameMap 元素</span><span class="sxs-lookup"><span data-stu-id="f3135-104">ControlNameMap element</span></span>

<span data-ttu-id="f3135-105">表示自訂 [**SizeDefinition**](windowsribbon-element-sizedefinition.md) 版面配置範本中控制項名稱的容器。</span><span class="sxs-lookup"><span data-stu-id="f3135-105">Represents a container for control names in a custom [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layout template.</span></span>

## <a name="usage"></a><span data-ttu-id="f3135-106">使用方式</span><span class="sxs-lookup"><span data-stu-id="f3135-106">Usage</span></span>

``` syntax
<ControlNameMap>
  child elements
</ControlNameMap>
```

## <a name="attributes"></a><span data-ttu-id="f3135-107">屬性</span><span class="sxs-lookup"><span data-stu-id="f3135-107">Attributes</span></span>

<span data-ttu-id="f3135-108">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="f3135-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="f3135-109">子元素</span><span class="sxs-lookup"><span data-stu-id="f3135-109">Child elements</span></span>



| <span data-ttu-id="f3135-110">元素</span><span class="sxs-lookup"><span data-stu-id="f3135-110">Element</span></span>                                                                                 | <span data-ttu-id="f3135-111">描述</span><span class="sxs-lookup"><span data-stu-id="f3135-111">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="f3135-112">**ControlNameDefinition**</span><span class="sxs-lookup"><span data-stu-id="f3135-112">**ControlNameDefinition**</span></span>](windowsribbon-element-controlnamedefinition.md)<br/> | <span data-ttu-id="f3135-113">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="f3135-113">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="f3135-114">父元素</span><span class="sxs-lookup"><span data-stu-id="f3135-114">Parent elements</span></span>



| <span data-ttu-id="f3135-115">元素</span><span class="sxs-lookup"><span data-stu-id="f3135-115">Element</span></span>                                                                   |
|---------------------------------------------------------------------------|
| [<span data-ttu-id="f3135-116">**SizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="f3135-116">**SizeDefinition**</span></span>](windowsribbon-element-sizedefinition.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="f3135-117">備註</span><span class="sxs-lookup"><span data-stu-id="f3135-117">Remarks</span></span>

<span data-ttu-id="f3135-118">選擇性。</span><span class="sxs-lookup"><span data-stu-id="f3135-118">Optional.</span></span>

<span data-ttu-id="f3135-119">每個 [**SizeDefinition**](windowsribbon-element-sizedefinition.md) 元素最多可能會發生一次。</span><span class="sxs-lookup"><span data-stu-id="f3135-119">May occur at most once for each [**SizeDefinition**](windowsribbon-element-sizedefinition.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="f3135-120">範例</span><span class="sxs-lookup"><span data-stu-id="f3135-120">Examples</span></span>

<span data-ttu-id="f3135-121">下列程式碼範例示範具有 **ControlNameMap** 元素之自訂四個按鈕 [**SizeDefinition**](windowsribbon-element-sizedefinition.md)版面配置範本的基本標記。</span><span class="sxs-lookup"><span data-stu-id="f3135-121">The following code example demonstrates the basic markup for a custom four-button [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layout template with a **ControlNameMap** element.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="f3135-122">項目資訊</span><span class="sxs-lookup"><span data-stu-id="f3135-122">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="f3135-123">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="f3135-123">Minimum supported system</span></span><br/> | <span data-ttu-id="f3135-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f3135-124">Windows 7</span></span> |
| <span data-ttu-id="f3135-125">可以是空的</span><span class="sxs-lookup"><span data-stu-id="f3135-125">Can be empty</span></span>                        | <span data-ttu-id="f3135-126">否</span><span class="sxs-lookup"><span data-stu-id="f3135-126">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="f3135-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f3135-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3135-128">透過大小定義和調整原則自訂功能區</span><span class="sxs-lookup"><span data-stu-id="f3135-128">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 






---
title: SplitButton. MenuGroups 屬性
description: 表示標準分割按鈕控制項中一組下拉式功能表專案的容器。
ms.assetid: 6328ad49-037b-4cd5-90f6-b91646e260ee
keywords:
- SplitButton. MenuGroups 屬性 Windows 功能區
topic_type:
- apiref
api_name:
- SplitButton.MenuGroups
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b8af4639040d6b6302b4d2b5761d750074389a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685898"
---
# <a name="splitbuttonmenugroups-property"></a><span data-ttu-id="c7351-104">SplitButton. MenuGroups 屬性</span><span class="sxs-lookup"><span data-stu-id="c7351-104">SplitButton.MenuGroups property</span></span>

<span data-ttu-id="c7351-105">表示標準 [分割按鈕](windowsribbon-controls-splitbutton.md) 控制項中一組下拉式功能表專案的容器。</span><span class="sxs-lookup"><span data-stu-id="c7351-105">Represents a container for a set of drop-down menu items in a standard [Split Button](windowsribbon-controls-splitbutton.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="c7351-106">使用方式</span><span class="sxs-lookup"><span data-stu-id="c7351-106">Usage</span></span>

``` syntax
<SplitButton.MenuGroups>
  child elements
</SplitButton.MenuGroups>
```

## <a name="attributes"></a><span data-ttu-id="c7351-107">屬性</span><span class="sxs-lookup"><span data-stu-id="c7351-107">Attributes</span></span>

<span data-ttu-id="c7351-108">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="c7351-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="c7351-109">子元素</span><span class="sxs-lookup"><span data-stu-id="c7351-109">Child elements</span></span>



| <span data-ttu-id="c7351-110">元素</span><span class="sxs-lookup"><span data-stu-id="c7351-110">Element</span></span>                                                         | <span data-ttu-id="c7351-111">描述</span><span class="sxs-lookup"><span data-stu-id="c7351-111">Description</span></span>                                     |
|-----------------------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="c7351-112">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="c7351-112">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/> | <span data-ttu-id="c7351-113">至少必須發生一次</span><span class="sxs-lookup"><span data-stu-id="c7351-113">Must occur at least once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="c7351-114">父元素</span><span class="sxs-lookup"><span data-stu-id="c7351-114">Parent elements</span></span>



| <span data-ttu-id="c7351-115">元素</span><span class="sxs-lookup"><span data-stu-id="c7351-115">Element</span></span>                                                             |
|---------------------------------------------------------------------|
| [<span data-ttu-id="c7351-116">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="c7351-116">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="c7351-117">備註</span><span class="sxs-lookup"><span data-stu-id="c7351-117">Remarks</span></span>

<span data-ttu-id="c7351-118">選擇性。</span><span class="sxs-lookup"><span data-stu-id="c7351-118">Optional.</span></span>

<span data-ttu-id="c7351-119">每個 [**SplitButton**](windowsribbon-element-splitbutton.md)最多可能會發生一次。</span><span class="sxs-lookup"><span data-stu-id="c7351-119">May occur at most once for each [**SplitButton**](windowsribbon-element-splitbutton.md).</span></span>

## <a name="examples"></a><span data-ttu-id="c7351-120">範例</span><span class="sxs-lookup"><span data-stu-id="c7351-120">Examples</span></span>

<span data-ttu-id="c7351-121">下列範例示範 [分割按鈕](windowsribbon-controls-splitbutton.md)的基本標記。</span><span class="sxs-lookup"><span data-stu-id="c7351-121">The following example demonstrates the basic markup for the [Split Button](windowsribbon-controls-splitbutton.md).</span></span>

<span data-ttu-id="c7351-122">這段程式碼會顯示 [**SplitButton**](windowsribbon-element-splitbutton.md)和 **SplitButton MenuGroups** 命令宣告，以及可作為 **SplitButton** 元素父容器的相關聯 [**群組**](windowsribbon-element-group.md)。</span><span class="sxs-lookup"><span data-stu-id="c7351-122">This section of code shows the [**SplitButton**](windowsribbon-element-splitbutton.md) and **SplitButton.MenuGroups** Command declarations, with an associated [**Group**](windowsribbon-element-group.md) that functions as the parent container for the **SplitButton** element.</span></span>


```XML
<!-- SplitButton -->
<Command Name="cmdSplitButtonGroup"
         Symbol="cmdSplitButtonGroup"
         Comment="SplitButton Group"
         LabelTitle="SplitButton"/>
<Command Name="cmdSplitButton"
         Symbol="cmdSplitButton"
         Comment="SplitButton"
         LabelTitle="SplitButton"/>
<Command Name="cmdSBButtonItem"
         Symbol="cmdSBButtonItem"
         Comment="SBButtonItem"
         LabelTitle="SB ButtonItem"/>
<Command Name="cmdSBButton1"
         Symbol="cmdSBButton1"
         Comment="SBButton1"
         LabelTitle="SB Button">
  <Command.LargeImages>
    <Image Source="res/copyL_32.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/copyS_16.bmp"/>
  </Command.SmallImages>
  <Command.LargeHighContrastImages>
    <Image Source="res/copyLHC_32.bmp"/>
  </Command.LargeHighContrastImages>
  <Command.SmallHighContrastImages>
    <Image Source="res/copySHC_16.bmp"/>
  </Command.SmallHighContrastImages>
</Command>
<Command Name="cmdSBMajorItems"
         Comment="Major Items Category"
         LabelTitle="Major Items"/>
<Command Name="cmdSBStandardItems"
         Comment="Standard Items Category"
         LabelTitle="Standard Items"/>
```



<span data-ttu-id="c7351-123">這段程式碼會顯示 [**SplitButton**](windowsribbon-element-splitbutton.md) 和 **SplitButton MenuGroups** 控制項宣告。</span><span class="sxs-lookup"><span data-stu-id="c7351-123">This section of code shows the [**SplitButton**](windowsribbon-element-splitbutton.md) and **SplitButton.MenuGroups** control declarations.</span></span>


```XML
<Group CommandName="cmdSplitButtonGroup">
  <SplitButton CommandName="cmdSplitButton">
    <SplitButton.ButtonItem>
      <Button CommandName="cmdSBButtonItem"/>
    </SplitButton.ButtonItem>
    <SplitButton.MenuGroups>
      <MenuGroup CommandName="cmdSBMajorItems" 
                 Class="MajorItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
      <MenuGroup CommandName="cmdSBStandardItems"
                 Class="StandardItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
      <MenuGroup Class="StandardItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
    </SplitButton.MenuGroups>
  </SplitButton>
</Group>
```



## <a name="requirements"></a><span data-ttu-id="c7351-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="c7351-124">Requirements</span></span>



| <span data-ttu-id="c7351-125">需求</span><span class="sxs-lookup"><span data-stu-id="c7351-125">Requirement</span></span> | <span data-ttu-id="c7351-126">值</span><span class="sxs-lookup"><span data-stu-id="c7351-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="c7351-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c7351-127">Minimum supported client</span></span><br/> | <span data-ttu-id="c7351-128">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c7351-128">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="c7351-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c7351-129">Minimum supported server</span></span><br/> | <span data-ttu-id="c7351-130">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c7351-130">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c7351-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c7351-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7351-132">分割按鈕控制項</span><span class="sxs-lookup"><span data-stu-id="c7351-132">Split Button control</span></span>](windowsribbon-controls-splitbutton.md)
</dt> </dl>

 

 






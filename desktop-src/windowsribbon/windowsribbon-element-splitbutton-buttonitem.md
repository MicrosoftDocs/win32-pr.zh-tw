---
title: SplitButton. ButtonItem 屬性
description: 代表按鈕或切換按鈕的容器，該按鈕會公開分割按鈕的預設命令。
ms.assetid: 3d46d606-238d-46d4-b92e-dfd759951770
keywords:
- SplitButton. ButtonItem 屬性 Windows 功能區
topic_type:
- apiref
api_name:
- SplitButton.ButtonItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bf1e1cb908ce9a86f23f75d17bf2e76797997db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464673"
---
# <a name="splitbuttonbuttonitem-property"></a><span data-ttu-id="22755-104">SplitButton. ButtonItem 屬性</span><span class="sxs-lookup"><span data-stu-id="22755-104">SplitButton.ButtonItem property</span></span>

<span data-ttu-id="22755-105">代表 [按鈕](windowsribbon-controls-button.md) 或 [切換按鈕](windowsribbon-controls-togglebutton.md) 的容器，該按鈕會公開 [分割按鈕](windowsribbon-controls-splitbutton.md)的預設命令。</span><span class="sxs-lookup"><span data-stu-id="22755-105">Represents a container for a [Button](windowsribbon-controls-button.md) or [Toggle Button](windowsribbon-controls-togglebutton.md) that exposes the default Command of a [Split Button](windowsribbon-controls-splitbutton.md).</span></span>

## <a name="usage"></a><span data-ttu-id="22755-106">使用方式</span><span class="sxs-lookup"><span data-stu-id="22755-106">Usage</span></span>

``` syntax
<SplitButton.ButtonItem>
  child elements
</SplitButton.ButtonItem>
```

## <a name="attributes"></a><span data-ttu-id="22755-107">屬性</span><span class="sxs-lookup"><span data-stu-id="22755-107">Attributes</span></span>

<span data-ttu-id="22755-108">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="22755-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="22755-109">子元素</span><span class="sxs-lookup"><span data-stu-id="22755-109">Child elements</span></span>



| <span data-ttu-id="22755-110">元素</span><span class="sxs-lookup"><span data-stu-id="22755-110">Element</span></span>                                                               | <span data-ttu-id="22755-111">描述</span><span class="sxs-lookup"><span data-stu-id="22755-111">Description</span></span>                                   |
|-----------------------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="22755-112">**Button**</span><span class="sxs-lookup"><span data-stu-id="22755-112">**Button**</span></span>](windowsribbon-element-button.md)<br/>             | <span data-ttu-id="22755-113">最多可能發生一次</span><span class="sxs-lookup"><span data-stu-id="22755-113">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="22755-114">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="22755-114">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)<br/> | <span data-ttu-id="22755-115">最多可能發生一次</span><span class="sxs-lookup"><span data-stu-id="22755-115">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="22755-116">父元素</span><span class="sxs-lookup"><span data-stu-id="22755-116">Parent elements</span></span>



| <span data-ttu-id="22755-117">元素</span><span class="sxs-lookup"><span data-stu-id="22755-117">Element</span></span>                                                             |
|---------------------------------------------------------------------|
| [<span data-ttu-id="22755-118">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="22755-118">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="22755-119">備註</span><span class="sxs-lookup"><span data-stu-id="22755-119">Remarks</span></span>

<span data-ttu-id="22755-120">選擇性。</span><span class="sxs-lookup"><span data-stu-id="22755-120">Optional.</span></span>

<span data-ttu-id="22755-121">每個 [**SplitButton**](windowsribbon-element-splitbutton.md)最多可能會發生一次。</span><span class="sxs-lookup"><span data-stu-id="22755-121">May occur at most once for each [**SplitButton**](windowsribbon-element-splitbutton.md).</span></span>

<span data-ttu-id="22755-122">每個 **SplitButton. ButtonItem** 只能包含一個 [**按鈕**](windowsribbon-element-button.md) 或 [**切換**](windowsribbon-element-togglebutton.md) 按鈕子項目。</span><span class="sxs-lookup"><span data-stu-id="22755-122">Each **SplitButton.ButtonItem** can contain only one [**Button**](windowsribbon-element-button.md) or [**ToggleButton**](windowsribbon-element-togglebutton.md) child element.</span></span>

## <a name="examples"></a><span data-ttu-id="22755-123">範例</span><span class="sxs-lookup"><span data-stu-id="22755-123">Examples</span></span>

<span data-ttu-id="22755-124">下列範例示範 [分割按鈕](windowsribbon-controls-splitbutton.md)的基本標記。</span><span class="sxs-lookup"><span data-stu-id="22755-124">The following example demonstrates the basic markup for the [Split Button](windowsribbon-controls-splitbutton.md).</span></span>

<span data-ttu-id="22755-125">這段程式碼會顯示 [**SplitButton**](windowsribbon-element-splitbutton.md)和 **SplitButton ButtonItem** 命令宣告，以及可作為 **SplitButton** 元素父容器的相關聯 [**群組**](windowsribbon-element-group.md)。</span><span class="sxs-lookup"><span data-stu-id="22755-125">This section of code shows the [**SplitButton**](windowsribbon-element-splitbutton.md) and **SplitButton.ButtonItem** Command declarations, with an associated [**Group**](windowsribbon-element-group.md) that functions as the parent container for the **SplitButton** element.</span></span>


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



<span data-ttu-id="22755-126">這段程式碼會顯示 [**SplitButton**](windowsribbon-element-splitbutton.md) 和 **SplitButton ButtonItem** 控制項宣告。</span><span class="sxs-lookup"><span data-stu-id="22755-126">This section of code shows the [**SplitButton**](windowsribbon-element-splitbutton.md) and **SplitButton.ButtonItem** control declarations.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="22755-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="22755-127">Requirements</span></span>



| <span data-ttu-id="22755-128">需求</span><span class="sxs-lookup"><span data-stu-id="22755-128">Requirement</span></span> | <span data-ttu-id="22755-129">值</span><span class="sxs-lookup"><span data-stu-id="22755-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="22755-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="22755-130">Minimum supported client</span></span><br/> | <span data-ttu-id="22755-131">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="22755-131">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="22755-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="22755-132">Minimum supported server</span></span><br/> | <span data-ttu-id="22755-133">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="22755-133">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="22755-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="22755-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22755-135">分割按鈕控制項</span><span class="sxs-lookup"><span data-stu-id="22755-135">Split Button control</span></span>](windowsribbon-controls-splitbutton.md)
</dt> </dl>

 

 






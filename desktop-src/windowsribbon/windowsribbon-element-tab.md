---
title: Tab 項目
description: 代表核心或內容索引標籤。
ms.assetid: 2e73a89c-4d31-4075-93c8-e43213a20791
keywords:
- Tab 元素視窗功能區
topic_type:
- apiref
api_name:
- Tab
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 410326961df84f6ae62d3c43bee3e651c9533066
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443879"
---
# <a name="tab-element"></a><span data-ttu-id="ff728-104">Tab 項目</span><span class="sxs-lookup"><span data-stu-id="ff728-104">Tab element</span></span>

<span data-ttu-id="ff728-105">代表[核心](windowsribbon-controls-tab.md)[或內容](windowsribbon-controls-tabgroup.md)索引標籤。</span><span class="sxs-lookup"><span data-stu-id="ff728-105">Represents a [core](windowsribbon-controls-tab.md) or [contextual](windowsribbon-controls-tabgroup.md) tab.</span></span>

## <a name="usage"></a><span data-ttu-id="ff728-106">使用方式</span><span class="sxs-lookup"><span data-stu-id="ff728-106">Usage</span></span>

``` syntax
<Tab
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string">
  child elements
</Tab>
```

## <a name="attributes"></a><span data-ttu-id="ff728-107">屬性</span><span class="sxs-lookup"><span data-stu-id="ff728-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ff728-108">屬性</span><span class="sxs-lookup"><span data-stu-id="ff728-108">Attribute</span></span></th>
<th><span data-ttu-id="ff728-109">類型</span><span class="sxs-lookup"><span data-stu-id="ff728-109">Type</span></span></th>
<th><span data-ttu-id="ff728-110">必要</span><span class="sxs-lookup"><span data-stu-id="ff728-110">Required</span></span></th>
<th><span data-ttu-id="ff728-111">描述</span><span class="sxs-lookup"><span data-stu-id="ff728-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ff728-112"><strong>ApplicationModes</strong></span><span class="sxs-lookup"><span data-stu-id="ff728-112"><strong>ApplicationModes</strong></span></span><br/></td>
<td><span data-ttu-id="ff728-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="ff728-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="ff728-114">否</span><span class="sxs-lookup"><span data-stu-id="ff728-114">No</span></span><br/></td>
<td><span data-ttu-id="ff728-115">只有在 <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> 是父元素時才有效。</span><span class="sxs-lookup"><span data-stu-id="ff728-115">Valid only if <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> is the parent element.</span></span><br/> <br/><span data-ttu-id="ff728-116">
<dt><span></span><span></span><strong></strong> (xs： string) </span><span class="sxs-lookup"><span data-stu-id="ff728-116">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="ff728-117">字串，其中包含0到31之間的整數清單（以逗號分隔）。</span><span class="sxs-lookup"><span data-stu-id="ff728-117">A string that contains a comma-separated list of integers between 0 and 31.</span></span><br/> <span data-ttu-id="ff728-118">空白字元是有效的，而且會被忽略。</span><span class="sxs-lookup"><span data-stu-id="ff728-118">White space is valid and ignored.</span></span><br/> <span data-ttu-id="ff728-119">最大長度：250個字元。</span><span class="sxs-lookup"><span data-stu-id="ff728-119">Maximum length: 250 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ff728-120"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="ff728-120"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="ff728-121">xs： positiveInteger 或 xs： string</span><span class="sxs-lookup"><span data-stu-id="ff728-121">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="ff728-122">否</span><span class="sxs-lookup"><span data-stu-id="ff728-122">No</span></span><br/></td>
<td><span data-ttu-id="ff728-123">將元素與 <a href="windowsribbon-element-command.md"><strong>命令</strong></a>產生關聯。</span><span class="sxs-lookup"><span data-stu-id="ff728-123">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="ff728-124">
<dt><span></span><span></span><strong></strong> (xs： positiveInteger 或 xs： string) </span><span class="sxs-lookup"><span data-stu-id="ff728-124">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="ff728-125">字串、介於2與59999（含）之間的整數值，或介於0x2 與0xea5f （含）之間的十六進位值。</span><span class="sxs-lookup"><span data-stu-id="ff728-125">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="ff728-126">值在功能區 XML 檔中必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="ff728-126">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="ff728-127">最大長度：100個字元。</span><span class="sxs-lookup"><span data-stu-id="ff728-127">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="ff728-128">子元素</span><span class="sxs-lookup"><span data-stu-id="ff728-128">Child elements</span></span>



| <span data-ttu-id="ff728-129">元素</span><span class="sxs-lookup"><span data-stu-id="ff728-129">Element</span></span>                                                                         | <span data-ttu-id="ff728-130">描述</span><span class="sxs-lookup"><span data-stu-id="ff728-130">Description</span></span>                                        |
|---------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="ff728-131">**組**</span><span class="sxs-lookup"><span data-stu-id="ff728-131">**Group**</span></span>](windowsribbon-element-group.md)<br/>                         | <span data-ttu-id="ff728-132">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="ff728-132">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="ff728-133">**ScalingPolicy**</span><span class="sxs-lookup"><span data-stu-id="ff728-133">**Tab.ScalingPolicy**</span></span>](windowsribbon-element-tab-scalingpolicy.md)<br/> | <span data-ttu-id="ff728-134">最多可能發生一次</span><span class="sxs-lookup"><span data-stu-id="ff728-134">May occur at most once</span></span><br/> <br/>      |



## <a name="parent-elements"></a><span data-ttu-id="ff728-135">父元素</span><span class="sxs-lookup"><span data-stu-id="ff728-135">Parent elements</span></span>



| <span data-ttu-id="ff728-136">元素</span><span class="sxs-lookup"><span data-stu-id="ff728-136">Element</span></span>                                                             |
|---------------------------------------------------------------------|
| <span data-ttu-id="ff728-137">[**功能區] 索引標籤**](windowsribbon-element-ribbon-tabs.md)</span><span class="sxs-lookup"><span data-stu-id="ff728-137">[**Ribbon.Tabs**](windowsribbon-element-ribbon-tabs.md)</span></span><br/> |
| [<span data-ttu-id="ff728-138">**TabGroup**</span><span class="sxs-lookup"><span data-stu-id="ff728-138">**TabGroup**</span></span>](windowsribbon-element-tabgroup.md)<br/>       |



## <a name="remarks"></a><span data-ttu-id="ff728-139">備註</span><span class="sxs-lookup"><span data-stu-id="ff728-139">Remarks</span></span>

<span data-ttu-id="ff728-140">必要。</span><span class="sxs-lookup"><span data-stu-id="ff728-140">Required.</span></span>

<span data-ttu-id="ff728-141">每個功能區都必須至少出現一次 [**。 tab**](windowsribbon-element-ribbon-tabs.md) 或 [**TabGroup**](windowsribbon-element-tabgroup.md) 元素。</span><span class="sxs-lookup"><span data-stu-id="ff728-141">Must occur at least once for each [**Ribbon.Tabs**](windowsribbon-element-ribbon-tabs.md) or [**TabGroup**](windowsribbon-element-tabgroup.md) element.</span></span>

<span data-ttu-id="ff728-142">**Tab** 支援 [應用程式模式](ribbon-applicationmodes.md)。</span><span class="sxs-lookup"><span data-stu-id="ff728-142">**Tab** supports [application modes](ribbon-applicationmodes.md).</span></span>

<span data-ttu-id="ff728-143">如果索引卷 **標元素有** [**ScalingPolicy IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) ，則 **ScalingPolicy. IdealSizes** 下需要每個 [**群組**](windowsribbon-element-group.md)元素的專案及其理想的大小。</span><span class="sxs-lookup"><span data-stu-id="ff728-143">If [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) is present for the **Tab** element, then an entry for each [**Group**](windowsribbon-element-group.md) element and its ideal size is required under **ScalingPolicy.IdealSizes**.</span></span>

## <a name="examples"></a><span data-ttu-id="ff728-144">範例</span><span class="sxs-lookup"><span data-stu-id="ff728-144">Examples</span></span>

<span data-ttu-id="ff728-145">下列範例將示範 **Tab** 元素的基本標記。</span><span class="sxs-lookup"><span data-stu-id="ff728-145">The following example demonstrates the basic markup for the **Tab** element.</span></span>

<span data-ttu-id="ff728-146">這一段程式碼會顯示 [**常用] 索引** 標籤的 [索引標籤命令聲明 **]** 。</span><span class="sxs-lookup"><span data-stu-id="ff728-146">This section of code shows the **Tab** Command declarations for a **Home** tab.</span></span>


```XML
<Command Name="cmdHomeTab"
         LabelTitle="Home"
         Keytip="H" />
<Command Name="cmdClipboardGroup"
         Symbol="IDR_CMD_CLIPBOARD"
         Id="10000"
         Comment="Command definition for clipboard group"
         LabelTitle="Clipboard"
         Keytip="CB" />
<Command Name="cmdCopy"
         Symbol="IDR_CMD_COPY"
         LabelTitle="Copy"
         LabelDescription="Copy"
         Keytip="C"
         TooltipTitle="Copy"
         TooltipDescription="Click to copy">
  <Command.SmallImages>
    <Image>res/copyS_16.bmp</Image>
  </Command.SmallImages>
  <Command.LargeImages>
    <Image>res/copyL_32.bmp</Image>
  </Command.LargeImages>
</Command>
<Command Name="cmdPaste"
         Symbol="IDR_CMD_PASTE" >
  <Command.LabelTitle>Paste</Command.LabelTitle>
  <Command.LabelDescription>
    <String Content="Paste contents of clipboard"
            Id="10001"
            Symbol="IDR_RES_LABELDESC_PASTE" />
  </Command.LabelDescription>
  <Command.Keytip>P</Command.Keytip>
  <Command.TooltipTitle>
    <String Content="Paste contents of clipboard"
            Id="10002"
            Symbol="IDR_RES_TOOLTIP_PASTE"/>
  </Command.TooltipTitle>
  <Command.TooltipDescription>
    <String Content="Click to paste contents of clipboard"/>
  </Command.TooltipDescription>
  <Command.SmallImages>
    <Image
      Id="10010"
      MinDPI="96"
      Symbol="IDR_RES_SMALL_IMAGE96">
      <Image.Source>res/pasteS_96bpp.bmp</Image.Source>
    </Image>
    <Image Source="res/pasteS_120bpp.bmp"
           Id="10011"
           MinDPI="120"
           Symbol="IDR_RES_SMALL_IMAGE120" />
  </Command.SmallImages>
  <Command.LargeImages>
    <Image>res/pasteL_32.bmp</Image>
  </Command.LargeImages>
</Command>
<Command Name="cmdMinimize"
         Symbol="IDR_CMD_MINIMIZE"
         Id="10001"
         LabelTitle="Minimize" />
```



<span data-ttu-id="ff728-147">這段程式碼會顯示 **選項卡** 控制項宣告。</span><span class="sxs-lookup"><span data-stu-id="ff728-147">This section of code shows the **Tab** control declarations.</span></span>


```XML
<Tab CommandName="cmdHomeTab">
  <Group CommandName="cmdClipboardGroup" 
         SizeDefinition="ThreeButtons">
    <Button CommandName="cmdCopy"/>
    <Button CommandName="cmdPaste"/>
    <ToggleButton CommandName="cmdMinimize"/>
  </Group>
</Tab>
```



## <a name="element-information"></a><span data-ttu-id="ff728-148">項目資訊</span><span class="sxs-lookup"><span data-stu-id="ff728-148">Element information</span></span>

- <span data-ttu-id="ff728-149">**最低支援系統**： Windows 7</span><span class="sxs-lookup"><span data-stu-id="ff728-149">**Minimum supported system**: Windows 7</span></span> 
- <span data-ttu-id="ff728-150">**可以是空** 的：否</span><span class="sxs-lookup"><span data-stu-id="ff728-150">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="ff728-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ff728-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff728-152">索引標籤控制項</span><span class="sxs-lookup"><span data-stu-id="ff728-152">Tab control</span></span>](windowsribbon-controls-tab.md)
</dt> <dt>

[<span data-ttu-id="ff728-153">Tab 群組控制項</span><span class="sxs-lookup"><span data-stu-id="ff728-153">Tab Group control</span></span>](windowsribbon-controls-tabgroup.md)
</dt> <dt>

[<span data-ttu-id="ff728-154">**SetModes**</span><span class="sxs-lookup"><span data-stu-id="ff728-154">**SetModes**</span></span>](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> </dl>

 


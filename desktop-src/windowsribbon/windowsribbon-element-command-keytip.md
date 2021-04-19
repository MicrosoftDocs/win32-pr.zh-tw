---
title: 命令提示屬性
description: 代表控制項的快速鍵提示。
ms.assetid: 214f69ae-dd35-4abf-b294-d898d7802aa6
keywords:
- 命令提示屬性 Windows 功能區
topic_type:
- apiref
api_name:
- Command.Keytip
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ab16b9b8e52094d6cdc85890dfc1cf8af63942c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966141"
---
# <a name="commandkeytip-property"></a><span data-ttu-id="1b80f-104">命令提示屬性</span><span class="sxs-lookup"><span data-stu-id="1b80f-104">Command.Keytip property</span></span>

<span data-ttu-id="1b80f-105">代表控制項的快速鍵提示。</span><span class="sxs-lookup"><span data-stu-id="1b80f-105">Represents the keytip for a control.</span></span>

## <a name="usage"></a><span data-ttu-id="1b80f-106">使用方式</span><span class="sxs-lookup"><span data-stu-id="1b80f-106">Usage</span></span>

``` syntax
<Command.Keytip>
  child elements
</Command.Keytip>
```

## <a name="attributes"></a><span data-ttu-id="1b80f-107">屬性</span><span class="sxs-lookup"><span data-stu-id="1b80f-107">Attributes</span></span>

<span data-ttu-id="1b80f-108">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="1b80f-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="1b80f-109">子元素</span><span class="sxs-lookup"><span data-stu-id="1b80f-109">Child elements</span></span>



| <span data-ttu-id="1b80f-110">元素</span><span class="sxs-lookup"><span data-stu-id="1b80f-110">Element</span></span>                                                   | <span data-ttu-id="1b80f-111">描述</span><span class="sxs-lookup"><span data-stu-id="1b80f-111">Description</span></span>                                   |
|-----------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="1b80f-112">**字串**</span><span class="sxs-lookup"><span data-stu-id="1b80f-112">**String**</span></span>](windowsribbon-element-string.md)<br/> | <span data-ttu-id="1b80f-113">最多可能發生一次</span><span class="sxs-lookup"><span data-stu-id="1b80f-113">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="1b80f-114">父元素</span><span class="sxs-lookup"><span data-stu-id="1b80f-114">Parent elements</span></span>



| <span data-ttu-id="1b80f-115">元素</span><span class="sxs-lookup"><span data-stu-id="1b80f-115">Element</span></span>                                                     |
|-------------------------------------------------------------|
| [<span data-ttu-id="1b80f-116">**命令**</span><span class="sxs-lookup"><span data-stu-id="1b80f-116">**Command**</span></span>](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="1b80f-117">備註</span><span class="sxs-lookup"><span data-stu-id="1b80f-117">Remarks</span></span>

<span data-ttu-id="1b80f-118">選擇性。</span><span class="sxs-lookup"><span data-stu-id="1b80f-118">Optional.</span></span>

<span data-ttu-id="1b80f-119">每個 [**命令**](windowsribbon-element-command.md) 元素最多可能會發生一次。</span><span class="sxs-lookup"><span data-stu-id="1b80f-119">May occur at most once for each [**Command**](windowsribbon-element-command.md) element.</span></span>

<span data-ttu-id="1b80f-120">**命令。快速鍵** 可以包含限制為任何 Unicode 字元序列（包括空白字元）的 *xs： string* 類型值。</span><span class="sxs-lookup"><span data-stu-id="1b80f-120">**Command.Keytip** can contain a value of type *xs:string* constrained to any sequence of Unicode characters, including white space.</span></span>

<span data-ttu-id="1b80f-121">**命令。** 只有在與索引卷 [標或](windowsribbon-controls-tab.md)[快速存取工具列](windowsribbon-controls-quickaccesstoolbar.md)內的控制項相關聯時，快速鍵才能以數位開頭。</span><span class="sxs-lookup"><span data-stu-id="1b80f-121">A **Command.Keytip** can begin with a number only when associated with a control within a [Tab](windowsribbon-controls-tab.md) or the [Quick Access Toolbar](windowsribbon-controls-quickaccesstoolbar.md).</span></span>

<span data-ttu-id="1b80f-122">若要顯示對功能區的目前狀態有效的按鍵提示，請按下 ALT 鍵。</span><span class="sxs-lookup"><span data-stu-id="1b80f-122">To display the keytips that are valid for the current state of the ribbon, press and hold the ALT key.</span></span> <span data-ttu-id="1b80f-123">下列螢幕擷取畫面顯示在 Windows 7 的 Microsoft 小畫家中顯示的初始或第一個層級按鍵提示。</span><span class="sxs-lookup"><span data-stu-id="1b80f-123">The following screen shot shows the initial, or first level, keytips that are displayed in Microsoft Paint for Windows 7.</span></span> <span data-ttu-id="1b80f-124">選取第一個層首鍵提示之後，只會顯示第二層的快速鍵提示。</span><span class="sxs-lookup"><span data-stu-id="1b80f-124">After a first-level keytip has been selected, only second-level keytips are displayed.</span></span>

![microsoft 油漆中適用于 windows 7 的第一層快速鍵提示](images/properties/ui-pkey-label-keytips.png)

<span data-ttu-id="1b80f-126">**命令。快速鍵** 可作為命令的鍵盤快速鍵，除非該命令是透過功能表項目公開。</span><span class="sxs-lookup"><span data-stu-id="1b80f-126">**Command.Keytip** acts as the keyboard accelerator for a command unless that command is exposed through a menu item.</span></span> <span data-ttu-id="1b80f-127">在此情況下，架構會忽略 **命令。 Keytip** 值，並改為使用 [**LabelTitle**](windowsribbon-element-command-labeltitle.md) 或 [UI \_ PKEY \_ 標籤](windowsribbon-reference-properties-uipkey-label.md)所指定的字元之前加上符號。</span><span class="sxs-lookup"><span data-stu-id="1b80f-127">In this case, the framework ignores the **Command.Keytip** value and instead uses a character preceded by an ampersand as specified by [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) or [UI\_PKEY\_Label](windowsribbon-reference-properties-uipkey-label.md).</span></span> <span data-ttu-id="1b80f-128">如果未指定 **LabelTitle** 或 UI \_ PKEY 標籤的連字號 \_ ，則不會公開任何快捷方式或鍵盤快速鍵。</span><span class="sxs-lookup"><span data-stu-id="1b80f-128">If no ampersand is specified by **Command.LabelTitle** or UI\_PKEY\_Label, no keytip or keyboard accelerator is exposed.</span></span>

<span data-ttu-id="1b80f-129">如果未提供 **命令提示** 字元的值，則需要 [**字串**](windowsribbon-element-string.md) 子項目。</span><span class="sxs-lookup"><span data-stu-id="1b80f-129">If no value is supplied for **Command.Keytip**, the [**String**](windowsribbon-element-string.md) child element is required.</span></span>

> [!Note]  
> <span data-ttu-id="1b80f-130">如果 **命令提示** 字元同時包含值和 [**字串**](windowsribbon-element-string.md) 子項目，則會優先使用 **字串** 。</span><span class="sxs-lookup"><span data-stu-id="1b80f-130">If **Command.Keytip** contains both a value and a [**String**](windowsribbon-element-string.md) child element, **String** takes precedence.</span></span>

 

<span data-ttu-id="1b80f-131">根據預設，架構會使用下列字母自動產生快速鍵提示：</span><span class="sxs-lookup"><span data-stu-id="1b80f-131">By default, the following letters are used by the framework to automatically generate keytips:</span></span>

-   <span data-ttu-id="1b80f-132">**F** 指派給 [應用程式功能表](windowsribbon-controls-applicationmenu.md)。</span><span class="sxs-lookup"><span data-stu-id="1b80f-132">**F** is assigned to the [Application Menu](windowsribbon-controls-applicationmenu.md).</span></span>
-   <span data-ttu-id="1b80f-133">**Y** 會指派給沒有應用程式所指定之快捷方式的任何命令。</span><span class="sxs-lookup"><span data-stu-id="1b80f-133">**Y** is assigned to any command that does not have a keytip specified by the application.</span></span>
-   <span data-ttu-id="1b80f-134">**Z** 會指派給每個 [群組](windowsribbon-controls-group.md) 控制項，而且無法自訂。</span><span class="sxs-lookup"><span data-stu-id="1b80f-134">**Z** is assigned to each [Group](windowsribbon-controls-group.md) control and cannot be customized.</span></span> <span data-ttu-id="1b80f-135">只有當控制項的 [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) 指定快顯大小選項時，才會顯示群組 **的快捷方式** 。</span><span class="sxs-lookup"><span data-stu-id="1b80f-135">A Group keytip is displayed only when the [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) for the control specifies a **Popup** size option.</span></span> <span data-ttu-id="1b80f-136">如需詳細資訊，請參閱 [透過大小定義自訂功能區和調整原則](windowsribbon-templates.md)。</span><span class="sxs-lookup"><span data-stu-id="1b80f-136">For more information, see [Customizing a Ribbon Through Size Definitions and Scaling Policies](windowsribbon-templates.md).</span></span>

> [!Note]  
> <span data-ttu-id="1b80f-137">架構不會保留這些字母。</span><span class="sxs-lookup"><span data-stu-id="1b80f-137">None of these letters are reserved by the framework.</span></span> <span data-ttu-id="1b80f-138">您可以視需要將每個命令指派給一或多個命令。</span><span class="sxs-lookup"><span data-stu-id="1b80f-138">Each can be assigned to one or more commands as required.</span></span>

 

<span data-ttu-id="1b80f-139">架構會以下列方式解決 keytip 衝突：</span><span class="sxs-lookup"><span data-stu-id="1b80f-139">The framework resolves keytip conflicts in the following ways:</span></span>

-   <span data-ttu-id="1b80f-140">如果有一或 [多個](windowsribbon-controls-tab.md) 索引標籤控制項與相同的 keytip 相關聯，則會將一個數位附加至每個 keytip，從1開始，然後依序 (2，3,... ) 針對宣告順序中的每個控制項。</span><span class="sxs-lookup"><span data-stu-id="1b80f-140">If one or more [Tab](windowsribbon-controls-tab.md) controls are associated with the same keytip, a number is appended to each keytip, starting at 1, and increasing sequentially (2, 3,...) for each control in the order of declaration.</span></span> <span data-ttu-id="1b80f-141">如果有任何索引標籤控制項被指派字母 F 作為按鍵提示，則會指派 [ [應用程式] 功能表](windowsribbon-controls-applicationmenu.md) ，並依所述調整其餘的按鍵提示。</span><span class="sxs-lookup"><span data-stu-id="1b80f-141">If any Tab controls are assigned the letter F as a keytip, the [Application Menu](windowsribbon-controls-applicationmenu.md) is assigned F1 with the remaining keytips adjusted as described.</span></span>
-   <span data-ttu-id="1b80f-142">當與索引標籤內的單一控制項相關聯 [時，快速鍵](windowsribbon-controls-tab.md)提示 F 對控制項和 [應用程式功能表](windowsribbon-controls-applicationmenu.md)都有效。</span><span class="sxs-lookup"><span data-stu-id="1b80f-142">When associated with a single control within a [Tab](windowsribbon-controls-tab.md), the keytip F is valid for both the control and the [Application Menu](windowsribbon-controls-applicationmenu.md).</span></span> <span data-ttu-id="1b80f-143">預設的應用程式功能表 keytip 不會變更，但會將優先順序提供給 [使用中] 索引標籤上的控制項。</span><span class="sxs-lookup"><span data-stu-id="1b80f-143">The default Application Menu keytip is not changed, but precedence is given to the control on the active tab.</span></span>
-   <span data-ttu-id="1b80f-144">如果索引標籤 [中的一](windowsribbon-controls-tab.md) 或多個控制項與相同的按鍵提示相關聯，則架構會自動重構這些控制項的按鍵提示，如先前所述。</span><span class="sxs-lookup"><span data-stu-id="1b80f-144">If one or more controls within a [Tab](windowsribbon-controls-tab.md) are associated with the same keytip, the framework automatically refactors the keytips of those controls, as described previously.</span></span>

> [!Note]  
> <span data-ttu-id="1b80f-145">文字色彩的些許變化是用來反白顯示標準功能區執行中重構的快速鍵。</span><span class="sxs-lookup"><span data-stu-id="1b80f-145">A slight variation in text color is used to highlight refactored keytips in a standard ribbon implementation.</span></span> <span data-ttu-id="1b80f-146">針對已自訂功能區色彩的非標準功能區執行，將會覆寫此架構行為，並以相同的文字色彩顯示所有快速鍵提示。</span><span class="sxs-lookup"><span data-stu-id="1b80f-146">For a nonstandard ribbon implementation where the ribbon color has been customized, this framework behavior is overridden and all keytips are displayed with the same text color.</span></span> <span data-ttu-id="1b80f-147">如需詳細資訊，請參閱 [自訂功能區色彩](ribbon-color.md)。</span><span class="sxs-lookup"><span data-stu-id="1b80f-147">For more information, see [Customizing Ribbon Colors](ribbon-color.md).</span></span>

 

<span data-ttu-id="1b80f-148">長度上限為未系結。</span><span class="sxs-lookup"><span data-stu-id="1b80f-148">The maximum length is unbounded.</span></span>

## <a name="examples"></a><span data-ttu-id="1b80f-149">範例</span><span class="sxs-lookup"><span data-stu-id="1b80f-149">Examples</span></span>

<span data-ttu-id="1b80f-150">下列範例示範 [**命令**](windowsribbon-element-command.md)專案的標記，以及 **命令提示。**</span><span class="sxs-lookup"><span data-stu-id="1b80f-150">The following example demonstrates the markup for a [**Command**](windowsribbon-element-command.md) element with a **Command.Keytip** declaration.</span></span>


```XML
<Command>
  <Command.Name>cmdSave</Command.Name>
  <Command.Symbol>ID_FILE_SAVE</Command.Symbol>
  <Command.Comment>Save</Command.Comment>
  <Command.Id>25003</Command.Id>
  <Command.LabelTitle>
    <String>
      <String.Content>Label for Save</String.Content>
      <String.Id>59999</String.Id>
      <String.Symbol>strSave</String.Symbol>
    </String>
  </Command.LabelTitle>
  <Command.TooltipTitle>Tooltip title with &amp;&amp; for Save Command</Command.TooltipTitle>
  <Command.TooltipDescription>Tooltip description for Save Command.</Command.TooltipDescription>
  <Command.Keytip>s1</Command.Keytip>
</Command>
```



## <a name="requirements"></a><span data-ttu-id="1b80f-151">規格需求</span><span class="sxs-lookup"><span data-stu-id="1b80f-151">Requirements</span></span>



| <span data-ttu-id="1b80f-152">需求</span><span class="sxs-lookup"><span data-stu-id="1b80f-152">Requirement</span></span> | <span data-ttu-id="1b80f-153">值</span><span class="sxs-lookup"><span data-stu-id="1b80f-153">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="1b80f-154">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1b80f-154">Minimum supported client</span></span><br/> | <span data-ttu-id="1b80f-155">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1b80f-155">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="1b80f-156">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1b80f-156">Minimum supported server</span></span><br/> | <span data-ttu-id="1b80f-157">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1b80f-157">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1b80f-158">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1b80f-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b80f-159">UI \_ PKEY \_ 按鍵提示</span><span class="sxs-lookup"><span data-stu-id="1b80f-159">UI\_PKEY\_Keytip</span></span>](windowsribbon-reference-properties-uipkey-keytip.md)
</dt> </dl>

 

 






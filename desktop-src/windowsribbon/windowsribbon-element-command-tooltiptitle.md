---
title: TooltipTitle 屬性
description: 表示工具提示標題。
ms.assetid: b06a7a6a-fbdd-464b-b804-e62912d6e176
keywords:
- TooltipTitle 屬性 Windows 功能區
topic_type:
- apiref
api_name:
- Command.TooltipTitle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c60f4ddea77fbf88a15d5d27e90ca5660bc0edb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466576"
---
# <a name="commandtooltiptitle-property"></a><span data-ttu-id="f0f28-104">TooltipTitle 屬性</span><span class="sxs-lookup"><span data-stu-id="f0f28-104">Command.TooltipTitle property</span></span>

<span data-ttu-id="f0f28-105">表示工具提示標題。</span><span class="sxs-lookup"><span data-stu-id="f0f28-105">Represents a tooltip title.</span></span>

## <a name="usage"></a><span data-ttu-id="f0f28-106">使用方式</span><span class="sxs-lookup"><span data-stu-id="f0f28-106">Usage</span></span>

``` syntax
<Command.TooltipTitle>
  child elements
</Command.TooltipTitle>
```

## <a name="attributes"></a><span data-ttu-id="f0f28-107">屬性</span><span class="sxs-lookup"><span data-stu-id="f0f28-107">Attributes</span></span>

<span data-ttu-id="f0f28-108">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="f0f28-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="f0f28-109">子元素</span><span class="sxs-lookup"><span data-stu-id="f0f28-109">Child elements</span></span>



| <span data-ttu-id="f0f28-110">元素</span><span class="sxs-lookup"><span data-stu-id="f0f28-110">Element</span></span>                                                   | <span data-ttu-id="f0f28-111">描述</span><span class="sxs-lookup"><span data-stu-id="f0f28-111">Description</span></span>                                   |
|-----------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="f0f28-112">**字串**</span><span class="sxs-lookup"><span data-stu-id="f0f28-112">**String**</span></span>](windowsribbon-element-string.md)<br/> | <span data-ttu-id="f0f28-113">最多可能發生一次</span><span class="sxs-lookup"><span data-stu-id="f0f28-113">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="f0f28-114">父元素</span><span class="sxs-lookup"><span data-stu-id="f0f28-114">Parent elements</span></span>



| <span data-ttu-id="f0f28-115">元素</span><span class="sxs-lookup"><span data-stu-id="f0f28-115">Element</span></span>                                                     |
|-------------------------------------------------------------|
| [<span data-ttu-id="f0f28-116">**命令**</span><span class="sxs-lookup"><span data-stu-id="f0f28-116">**Command**</span></span>](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="f0f28-117">備註</span><span class="sxs-lookup"><span data-stu-id="f0f28-117">Remarks</span></span>

<span data-ttu-id="f0f28-118">選擇性。</span><span class="sxs-lookup"><span data-stu-id="f0f28-118">Optional.</span></span>

<span data-ttu-id="f0f28-119">每個 [**命令**](windowsribbon-element-command.md)最多可能會發生一次。</span><span class="sxs-lookup"><span data-stu-id="f0f28-119">May occur at most once for each [**Command**](windowsribbon-element-command.md).</span></span>

<span data-ttu-id="f0f28-120">**TooltipTitle** 可以包含限制為任何字元序列之 *xs： string* 類型的值，包括空白字元和分行符號字元。</span><span class="sxs-lookup"><span data-stu-id="f0f28-120">**Command.TooltipTitle** can contain a value of type *xs:string* constrained to any sequence of characters, including white space and line-break characters.</span></span>

> [!Note]  
> <span data-ttu-id="f0f28-121">使用通用字元集 (UCS) XML 字元參考 `&#xA;` 來指定分行符號。</span><span class="sxs-lookup"><span data-stu-id="f0f28-121">Use the Universal Character Set (UCS) XML character reference `&#xA;` to specify a line break.</span></span>

 

<span data-ttu-id="f0f28-122">長度上限為未系結。</span><span class="sxs-lookup"><span data-stu-id="f0f28-122">The maximum length is unbounded.</span></span>

<span data-ttu-id="f0f28-123">如果未提供 **TooltipTitle** 的值，則需要 [**字串**](windowsribbon-element-string.md) 子項目。</span><span class="sxs-lookup"><span data-stu-id="f0f28-123">If no value is supplied for **Command.TooltipTitle**, the [**String**](windowsribbon-element-string.md) child element is required.</span></span>

> [!Note]  
> <span data-ttu-id="f0f28-124">如果 **TooltipTitle** 同時包含值和 [**字串**](windowsribbon-element-string.md) 子項目，則會優先使用 **字串** 。</span><span class="sxs-lookup"><span data-stu-id="f0f28-124">If **Command.TooltipTitle** contains both a value and a [**String**](windowsribbon-element-string.md) child element, **String** takes precedence.</span></span>

 

<span data-ttu-id="f0f28-125">**TooltipTitle** 只支援靠左對齊。</span><span class="sxs-lookup"><span data-stu-id="f0f28-125">**Command.TooltipTitle** only supports left alignment.</span></span>

## <a name="examples"></a><span data-ttu-id="f0f28-126">範例</span><span class="sxs-lookup"><span data-stu-id="f0f28-126">Examples</span></span>

<span data-ttu-id="f0f28-127">下列範例示範 [**命令**](windowsribbon-element-command.md) 專案的標記，以及 **TooltipTitle** 宣告。</span><span class="sxs-lookup"><span data-stu-id="f0f28-127">The following example demonstrates the markup for a [**Command**](windowsribbon-element-command.md) element with a **Command.TooltipTitle** declaration.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="f0f28-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="f0f28-128">Requirements</span></span>



| <span data-ttu-id="f0f28-129">需求</span><span class="sxs-lookup"><span data-stu-id="f0f28-129">Requirement</span></span> | <span data-ttu-id="f0f28-130">值</span><span class="sxs-lookup"><span data-stu-id="f0f28-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="f0f28-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f0f28-131">Minimum supported client</span></span><br/> | <span data-ttu-id="f0f28-132">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f0f28-132">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="f0f28-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f0f28-133">Minimum supported server</span></span><br/> | <span data-ttu-id="f0f28-134">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f0f28-134">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f0f28-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f0f28-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0f28-136">UI \_ PKEY \_ TooltipTitle</span><span class="sxs-lookup"><span data-stu-id="f0f28-136">UI\_PKEY\_TooltipTitle</span></span>](windowsribbon-reference-properties-uipkey-tooltiptitle.md)
</dt> </dl>

 

 






---
title: TooltipDescription 屬性
description: 表示工具提示描述。
ms.assetid: 2d3ea497-2d96-4420-8fcf-39ac2c472bf1
keywords:
- TooltipDescription 屬性 Windows 功能區
topic_type:
- apiref
api_name:
- Command.TooltipDescription
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 288578e74420912b7454be5037c4b2651918ac6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968374"
---
# <a name="commandtooltipdescription-property"></a><span data-ttu-id="0c91e-104">TooltipDescription 屬性</span><span class="sxs-lookup"><span data-stu-id="0c91e-104">Command.TooltipDescription property</span></span>

<span data-ttu-id="0c91e-105">表示工具提示描述。</span><span class="sxs-lookup"><span data-stu-id="0c91e-105">Represents a tooltip description.</span></span>

## <a name="usage"></a><span data-ttu-id="0c91e-106">使用方式</span><span class="sxs-lookup"><span data-stu-id="0c91e-106">Usage</span></span>

``` syntax
<Command.TooltipDescription>
  child elements
</Command.TooltipDescription>
```

## <a name="attributes"></a><span data-ttu-id="0c91e-107">屬性</span><span class="sxs-lookup"><span data-stu-id="0c91e-107">Attributes</span></span>

<span data-ttu-id="0c91e-108">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="0c91e-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="0c91e-109">子元素</span><span class="sxs-lookup"><span data-stu-id="0c91e-109">Child elements</span></span>



| <span data-ttu-id="0c91e-110">元素</span><span class="sxs-lookup"><span data-stu-id="0c91e-110">Element</span></span>                                                   | <span data-ttu-id="0c91e-111">描述</span><span class="sxs-lookup"><span data-stu-id="0c91e-111">Description</span></span>                                   |
|-----------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="0c91e-112">**字串**</span><span class="sxs-lookup"><span data-stu-id="0c91e-112">**String**</span></span>](windowsribbon-element-string.md)<br/> | <span data-ttu-id="0c91e-113">最多可能發生一次</span><span class="sxs-lookup"><span data-stu-id="0c91e-113">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="0c91e-114">父元素</span><span class="sxs-lookup"><span data-stu-id="0c91e-114">Parent elements</span></span>



| <span data-ttu-id="0c91e-115">元素</span><span class="sxs-lookup"><span data-stu-id="0c91e-115">Element</span></span>                                                     |
|-------------------------------------------------------------|
| [<span data-ttu-id="0c91e-116">**命令**</span><span class="sxs-lookup"><span data-stu-id="0c91e-116">**Command**</span></span>](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="0c91e-117">備註</span><span class="sxs-lookup"><span data-stu-id="0c91e-117">Remarks</span></span>

<span data-ttu-id="0c91e-118">選擇性。</span><span class="sxs-lookup"><span data-stu-id="0c91e-118">Optional.</span></span>

<span data-ttu-id="0c91e-119">每個 [**命令**](windowsribbon-element-command.md)最多可能會發生一次。</span><span class="sxs-lookup"><span data-stu-id="0c91e-119">May occur at most once for each [**Command**](windowsribbon-element-command.md).</span></span>

<span data-ttu-id="0c91e-120">**TooltipDescription** 可以包含限制為任何字元序列之 *xs： string* 類型的值，包括空白字元和分行符號字元。</span><span class="sxs-lookup"><span data-stu-id="0c91e-120">**Command.TooltipDescription** can contain a value of type *xs:string* constrained to any sequence of characters, including white space and line-break characters .</span></span>

> [!Note]  
> <span data-ttu-id="0c91e-121">使用通用字元集 (UCS) XML 字元參考 `&#xA;` 來指定分行符號。</span><span class="sxs-lookup"><span data-stu-id="0c91e-121">Use the Universal Character Set (UCS) XML character reference `&#xA;` to specify a line break.</span></span>

 

<span data-ttu-id="0c91e-122">長度上限為未系結。</span><span class="sxs-lookup"><span data-stu-id="0c91e-122">The maximum length is unbounded.</span></span>

<span data-ttu-id="0c91e-123">如果未提供 **TooltipDescription** 的值，則需要 [**字串**](windowsribbon-element-string.md) 子項目。</span><span class="sxs-lookup"><span data-stu-id="0c91e-123">If no value is supplied for **Command.TooltipDescription**, the [**String**](windowsribbon-element-string.md) child element is required.</span></span>

> [!Note]  
> <span data-ttu-id="0c91e-124">如果 **TooltipDescription** 同時包含值和 [**字串**](windowsribbon-element-string.md) 子項目，則會優先使用 **字串** 。</span><span class="sxs-lookup"><span data-stu-id="0c91e-124">If **Command.TooltipDescription** contains both a value and a [**String**](windowsribbon-element-string.md) child element, **String** takes precedence.</span></span>

 

<span data-ttu-id="0c91e-125">**TooltipDescription** 只支援靠左對齊。</span><span class="sxs-lookup"><span data-stu-id="0c91e-125">**Command.TooltipDescription** only supports left alignment.</span></span>

## <a name="examples"></a><span data-ttu-id="0c91e-126">範例</span><span class="sxs-lookup"><span data-stu-id="0c91e-126">Examples</span></span>

<span data-ttu-id="0c91e-127">下列範例示範 [**命令**](windowsribbon-element-command.md) 專案的標記，以及 **TooltipDescription** 宣告。</span><span class="sxs-lookup"><span data-stu-id="0c91e-127">The following example demonstrates the markup for a [**Command**](windowsribbon-element-command.md) element with a **Command.TooltipDescription** declaration.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="0c91e-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="0c91e-128">Requirements</span></span>



| <span data-ttu-id="0c91e-129">需求</span><span class="sxs-lookup"><span data-stu-id="0c91e-129">Requirement</span></span> | <span data-ttu-id="0c91e-130">值</span><span class="sxs-lookup"><span data-stu-id="0c91e-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="0c91e-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0c91e-131">Minimum supported client</span></span><br/> | <span data-ttu-id="0c91e-132">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0c91e-132">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="0c91e-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0c91e-133">Minimum supported server</span></span><br/> | <span data-ttu-id="0c91e-134">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0c91e-134">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0c91e-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0c91e-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c91e-136">UI \_ PKEY \_ TooltipDescription</span><span class="sxs-lookup"><span data-stu-id="0c91e-136">UI\_PKEY\_TooltipDescription</span></span>](windowsribbon-reference-properties-uipkey-tooltipdescription.md)
</dt> </dl>

 

 






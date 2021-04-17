---
title: LabelTitle 屬性
description: 表示標籤標題。
ms.assetid: 97378ec3-7988-4e39-9cf5-c382b246c5c9
keywords:
- LabelTitle 屬性 Windows 功能區
topic_type:
- apiref
api_name:
- Command.LabelTitle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed6d6c72ddd60cca63834fdcf21cf8f8b726ad22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509183"
---
# <a name="commandlabeltitle-property"></a><span data-ttu-id="e2e9b-104">LabelTitle 屬性</span><span class="sxs-lookup"><span data-stu-id="e2e9b-104">Command.LabelTitle property</span></span>

<span data-ttu-id="e2e9b-105">表示標籤標題。</span><span class="sxs-lookup"><span data-stu-id="e2e9b-105">Represents a label title.</span></span>

## <a name="usage"></a><span data-ttu-id="e2e9b-106">使用方式</span><span class="sxs-lookup"><span data-stu-id="e2e9b-106">Usage</span></span>

``` syntax
<Command.LabelTitle>
  child elements
</Command.LabelTitle>
```

## <a name="attributes"></a><span data-ttu-id="e2e9b-107">屬性</span><span class="sxs-lookup"><span data-stu-id="e2e9b-107">Attributes</span></span>

<span data-ttu-id="e2e9b-108">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="e2e9b-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="e2e9b-109">子元素</span><span class="sxs-lookup"><span data-stu-id="e2e9b-109">Child elements</span></span>



| <span data-ttu-id="e2e9b-110">元素</span><span class="sxs-lookup"><span data-stu-id="e2e9b-110">Element</span></span>                                                   | <span data-ttu-id="e2e9b-111">描述</span><span class="sxs-lookup"><span data-stu-id="e2e9b-111">Description</span></span>                                   |
|-----------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="e2e9b-112">**字串**</span><span class="sxs-lookup"><span data-stu-id="e2e9b-112">**String**</span></span>](windowsribbon-element-string.md)<br/> | <span data-ttu-id="e2e9b-113">最多可能發生一次</span><span class="sxs-lookup"><span data-stu-id="e2e9b-113">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="e2e9b-114">父元素</span><span class="sxs-lookup"><span data-stu-id="e2e9b-114">Parent elements</span></span>



| <span data-ttu-id="e2e9b-115">元素</span><span class="sxs-lookup"><span data-stu-id="e2e9b-115">Element</span></span>                                                     |
|-------------------------------------------------------------|
| [<span data-ttu-id="e2e9b-116">**命令**</span><span class="sxs-lookup"><span data-stu-id="e2e9b-116">**Command**</span></span>](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="e2e9b-117">備註</span><span class="sxs-lookup"><span data-stu-id="e2e9b-117">Remarks</span></span>

<span data-ttu-id="e2e9b-118">選擇性。</span><span class="sxs-lookup"><span data-stu-id="e2e9b-118">Optional.</span></span>

<span data-ttu-id="e2e9b-119">每個 [**命令**](windowsribbon-element-command.md)最多可能會發生一次。</span><span class="sxs-lookup"><span data-stu-id="e2e9b-119">May occur at most once for each [**Command**](windowsribbon-element-command.md).</span></span>

<span data-ttu-id="e2e9b-120">**LabelTitle** 可以包含限制為任何字元序列之 *xs： string* 類型的值，包括空白字元和分行符號字元。</span><span class="sxs-lookup"><span data-stu-id="e2e9b-120">**Command.LabelTitle** can contain a value of type *xs:string* constrained to any sequence of characters, including white space and line-break characters.</span></span>

> [!Note]  
> <span data-ttu-id="e2e9b-121">使用通用字元集 (UCS) XML 字元參考 `&#xA;` 來指定分行符號。</span><span class="sxs-lookup"><span data-stu-id="e2e9b-121">Use the Universal Character Set (UCS) XML character reference `&#xA;` to specify a line break.</span></span>

 

<span data-ttu-id="e2e9b-122">長度上限為未系結。</span><span class="sxs-lookup"><span data-stu-id="e2e9b-122">The maximum length is unbounded.</span></span>

<span data-ttu-id="e2e9b-123">如果未提供 **LabelTitle** 的值，則需要 [**字串**](windowsribbon-element-string.md) 子項目。</span><span class="sxs-lookup"><span data-stu-id="e2e9b-123">If no value is supplied for **Command.LabelTitle**, the [**String**](windowsribbon-element-string.md) child element is required.</span></span>

> [!Note]  
> <span data-ttu-id="e2e9b-124">如果 **LabelTitle** 同時包含值和 [**字串**](windowsribbon-element-string.md) 子項目，則會優先使用 **字串** 。</span><span class="sxs-lookup"><span data-stu-id="e2e9b-124">If **Command.LabelTitle** contains both a value and a [**String**](windowsribbon-element-string.md) child element, **String** takes precedence.</span></span>

 

<span data-ttu-id="e2e9b-125">**LabelTitle** 只支援靠左對齊。</span><span class="sxs-lookup"><span data-stu-id="e2e9b-125">**Command.LabelTitle** only supports left alignment.</span></span>

<span data-ttu-id="e2e9b-126">如果命令是透過功能表項目公開，而且 **LabelTitle** 或 [UI \_ PKEY \_ 標籤](windowsribbon-reference-properties-uipkey-label.md) 的值包含前面加上連字號的字母，如下列範例所示，則會將這個字母視為使用者介面的快速鍵，以及功能區架構的鍵盤對應鍵。</span><span class="sxs-lookup"><span data-stu-id="e2e9b-126">If a Command is exposed through a menu item and the value of **Command.LabelTitle** or [UI\_PKEY\_Label](windowsribbon-reference-properties-uipkey-label.md) contains a letter preceded by an ampersand, as shown in the following example, this letter is treated as both a keytip and a keyboard accelerator for that Command by the Ribbon framework.</span></span>


```XML
<Command Name="cmdNew"
         Symbol="ID_FILE_NEW"
         Comment="New"
         Id="25001"
         LabelTitle="&amp;New"/>
```



<span data-ttu-id="e2e9b-127">若要在標籤中顯示 & 符號，請將特殊字元指定換成雙符號 (`&&`) ，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="e2e9b-127">To display an ampersand in a label, escape the special character designation with a double ampersand (`&&`) as shown in the following example.</span></span>


```XML
<Command Name="cmdOpen"
         Symbol="ID_FILE_OPEN"
         Comment="Open"
         Id="25002"
         LabelTitle="&amp;&amp;Open"/>
```



## <a name="examples"></a><span data-ttu-id="e2e9b-128">範例</span><span class="sxs-lookup"><span data-stu-id="e2e9b-128">Examples</span></span>

<span data-ttu-id="e2e9b-129">下列範例示範 [**命令**](windowsribbon-element-command.md) 專案的標記，以及 **LabelTitle** 宣告。</span><span class="sxs-lookup"><span data-stu-id="e2e9b-129">The following example demonstrates the markup for a [**Command**](windowsribbon-element-command.md) element with a **Command.LabelTitle** declaration.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="e2e9b-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="e2e9b-130">Requirements</span></span>



| <span data-ttu-id="e2e9b-131">需求</span><span class="sxs-lookup"><span data-stu-id="e2e9b-131">Requirement</span></span> | <span data-ttu-id="e2e9b-132">值</span><span class="sxs-lookup"><span data-stu-id="e2e9b-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="e2e9b-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e2e9b-133">Minimum supported client</span></span><br/> | <span data-ttu-id="e2e9b-134">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e2e9b-134">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="e2e9b-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e2e9b-135">Minimum supported server</span></span><br/> | <span data-ttu-id="e2e9b-136">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e2e9b-136">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e2e9b-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e2e9b-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2e9b-138">UI \_ PKEY \_ 標籤</span><span class="sxs-lookup"><span data-stu-id="e2e9b-138">UI\_PKEY\_Label</span></span>](windowsribbon-reference-properties-uipkey-label.md)
</dt> </dl>

 

 






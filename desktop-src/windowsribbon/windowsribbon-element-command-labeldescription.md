---
title: LabelDescription 屬性
description: 表示標籤描述。
ms.assetid: 6c683e9e-0742-466e-9fdd-3d29f8ccb9ff
keywords:
- LabelDescription 屬性 Windows 功能區
topic_type:
- apiref
api_name:
- Command.LabelDescription
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f748425b4c8363feee737d18c750b3a1d91121b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934925"
---
# <a name="commandlabeldescription-property"></a><span data-ttu-id="707b4-104">LabelDescription 屬性</span><span class="sxs-lookup"><span data-stu-id="707b4-104">Command.LabelDescription property</span></span>

<span data-ttu-id="707b4-105">表示標籤描述。</span><span class="sxs-lookup"><span data-stu-id="707b4-105">Represents a label description.</span></span>

## <a name="usage"></a><span data-ttu-id="707b4-106">使用方式</span><span class="sxs-lookup"><span data-stu-id="707b4-106">Usage</span></span>

``` syntax
<Command.LabelDescription>
  child elements
</Command.LabelDescription>
```

## <a name="attributes"></a><span data-ttu-id="707b4-107">屬性</span><span class="sxs-lookup"><span data-stu-id="707b4-107">Attributes</span></span>

<span data-ttu-id="707b4-108">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="707b4-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="707b4-109">子元素</span><span class="sxs-lookup"><span data-stu-id="707b4-109">Child elements</span></span>



| <span data-ttu-id="707b4-110">元素</span><span class="sxs-lookup"><span data-stu-id="707b4-110">Element</span></span>                                                   | <span data-ttu-id="707b4-111">描述</span><span class="sxs-lookup"><span data-stu-id="707b4-111">Description</span></span>                                   |
|-----------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="707b4-112">**字串**</span><span class="sxs-lookup"><span data-stu-id="707b4-112">**String**</span></span>](windowsribbon-element-string.md)<br/> | <span data-ttu-id="707b4-113">最多可能發生一次</span><span class="sxs-lookup"><span data-stu-id="707b4-113">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="707b4-114">父元素</span><span class="sxs-lookup"><span data-stu-id="707b4-114">Parent elements</span></span>



| <span data-ttu-id="707b4-115">元素</span><span class="sxs-lookup"><span data-stu-id="707b4-115">Element</span></span>                                                     |
|-------------------------------------------------------------|
| [<span data-ttu-id="707b4-116">**命令**</span><span class="sxs-lookup"><span data-stu-id="707b4-116">**Command**</span></span>](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="707b4-117">備註</span><span class="sxs-lookup"><span data-stu-id="707b4-117">Remarks</span></span>

<span data-ttu-id="707b4-118">選擇性。</span><span class="sxs-lookup"><span data-stu-id="707b4-118">Optional.</span></span>

<span data-ttu-id="707b4-119">每個 [**命令**](windowsribbon-element-command.md)最多可能會發生一次。</span><span class="sxs-lookup"><span data-stu-id="707b4-119">May occur at most once for each [**Command**](windowsribbon-element-command.md).</span></span>

<span data-ttu-id="707b4-120">**LabelDescription** 可以包含限制為任何字元序列之 *xs： string 類型* 的值，包括空白字元和分行符號字元。</span><span class="sxs-lookup"><span data-stu-id="707b4-120">**Command.LabelDescription** can contain a value of *type xs:string* constrained to any sequence of characters, including white space and line-break characters.</span></span>

> [!Note]  
> <span data-ttu-id="707b4-121">使用通用字元集 (UCS) XML 字元參考 `&#xA;` 來指定分行符號。</span><span class="sxs-lookup"><span data-stu-id="707b4-121">Use the Universal Character Set (UCS) XML character reference `&#xA;` to specify a line break.</span></span>

 

<span data-ttu-id="707b4-122">長度上限為未系結。</span><span class="sxs-lookup"><span data-stu-id="707b4-122">The maximum length is unbounded.</span></span>

<span data-ttu-id="707b4-123">如果未提供 **LabelDescription** 的值，則需要 [**字串**](windowsribbon-element-string.md) 子項目。</span><span class="sxs-lookup"><span data-stu-id="707b4-123">If no value is supplied for **Command.LabelDescription**, the [**String**](windowsribbon-element-string.md) child element is required.</span></span>

> [!Note]  
> <span data-ttu-id="707b4-124">如果 **LabelDescription** 同時包含值和 [**字串**](windowsribbon-element-string.md) 子項目，則會優先使用 **字串** 。</span><span class="sxs-lookup"><span data-stu-id="707b4-124">If **Command.LabelDescription** contains both a value and a [**String**](windowsribbon-element-string.md) child element, **String** takes precedence.</span></span>

 

<span data-ttu-id="707b4-125">**LabelDescription** 只支援靠左對齊。</span><span class="sxs-lookup"><span data-stu-id="707b4-125">**Command.LabelDescription** only supports left alignment.</span></span>

## <a name="examples"></a><span data-ttu-id="707b4-126">範例</span><span class="sxs-lookup"><span data-stu-id="707b4-126">Examples</span></span>

<span data-ttu-id="707b4-127">下列範例顯示具有各種 **LabelDescription** 宣告之剪貼簿命令的資訊清單。</span><span class="sxs-lookup"><span data-stu-id="707b4-127">The following example shows a manifest of clipboard Commands with various **Command.LabelDescription** declarations.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="707b4-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="707b4-128">Requirements</span></span>



| <span data-ttu-id="707b4-129">需求</span><span class="sxs-lookup"><span data-stu-id="707b4-129">Requirement</span></span> | <span data-ttu-id="707b4-130">值</span><span class="sxs-lookup"><span data-stu-id="707b4-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="707b4-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="707b4-131">Minimum supported client</span></span><br/> | <span data-ttu-id="707b4-132">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="707b4-132">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="707b4-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="707b4-133">Minimum supported server</span></span><br/> | <span data-ttu-id="707b4-134">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="707b4-134">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="707b4-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="707b4-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="707b4-136">UI \_ PKEY \_ LabelDescription</span><span class="sxs-lookup"><span data-stu-id="707b4-136">UI\_PKEY\_LabelDescription</span></span>](windowsribbon-reference-properties-uipkey-labeldescription.md)
</dt> </dl>

 

 






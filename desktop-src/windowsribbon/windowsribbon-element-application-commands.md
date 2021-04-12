---
title: 應用程式. 命令屬性
description: 表示應用程式所定義之所有命令的容器。
ms.assetid: 160d7d28-2d64-4cbc-b2b9-2da6b2f5b3c8
keywords:
- 應用程式命令屬性視窗功能區
topic_type:
- apiref
api_name:
- Application.Commands
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8de2b88b97dda96636a9c5da3ad078f678091d8d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465276"
---
# <a name="applicationcommands-property"></a><span data-ttu-id="30f6b-104">應用程式. 命令屬性</span><span class="sxs-lookup"><span data-stu-id="30f6b-104">Application.Commands property</span></span>

<span data-ttu-id="30f6b-105">表示應用程式所定義之所有命令的容器。</span><span class="sxs-lookup"><span data-stu-id="30f6b-105">Represents a container for all the Commands that are defined by the application.</span></span>

## <a name="usage"></a><span data-ttu-id="30f6b-106">使用方式</span><span class="sxs-lookup"><span data-stu-id="30f6b-106">Usage</span></span>

``` syntax
<Application.Commands>
  child elements
</Application.Commands>
```

## <a name="attributes"></a><span data-ttu-id="30f6b-107">屬性</span><span class="sxs-lookup"><span data-stu-id="30f6b-107">Attributes</span></span>

<span data-ttu-id="30f6b-108">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="30f6b-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="30f6b-109">子元素</span><span class="sxs-lookup"><span data-stu-id="30f6b-109">Child elements</span></span>



| <span data-ttu-id="30f6b-110">元素</span><span class="sxs-lookup"><span data-stu-id="30f6b-110">Element</span></span>                                                     | <span data-ttu-id="30f6b-111">描述</span><span class="sxs-lookup"><span data-stu-id="30f6b-111">Description</span></span>                                        |
|-------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="30f6b-112">**命令**</span><span class="sxs-lookup"><span data-stu-id="30f6b-112">**Command**</span></span>](windowsribbon-element-command.md)<br/> | <span data-ttu-id="30f6b-113">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="30f6b-113">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="30f6b-114">父元素</span><span class="sxs-lookup"><span data-stu-id="30f6b-114">Parent elements</span></span>



| <span data-ttu-id="30f6b-115">元素</span><span class="sxs-lookup"><span data-stu-id="30f6b-115">Element</span></span>                                                             |
|---------------------------------------------------------------------|
| [<span data-ttu-id="30f6b-116">**應用程式**</span><span class="sxs-lookup"><span data-stu-id="30f6b-116">**Application**</span></span>](windowsribbon-element-application.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="30f6b-117">備註</span><span class="sxs-lookup"><span data-stu-id="30f6b-117">Remarks</span></span>

<span data-ttu-id="30f6b-118">選擇性。</span><span class="sxs-lookup"><span data-stu-id="30f6b-118">Optional.</span></span>

<span data-ttu-id="30f6b-119">每個 [**應用程式**](windowsribbon-element-application.md) 元素最多可能會發生一次。</span><span class="sxs-lookup"><span data-stu-id="30f6b-119">May occur at most once for each [**Application**](windowsribbon-element-application.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="30f6b-120">範例</span><span class="sxs-lookup"><span data-stu-id="30f6b-120">Examples</span></span>

<span data-ttu-id="30f6b-121">下列範例顯示的是包含剪貼簿命令之資訊清單的 **應用程式命令** 專案。</span><span class="sxs-lookup"><span data-stu-id="30f6b-121">The following example shows an **Application.Commands** element that contains a manifest of clipboard Commands.</span></span>


```C++
<Application.Commands>
```




```C++
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




```C++
</Application.Commands>
```



## <a name="requirements"></a><span data-ttu-id="30f6b-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="30f6b-122">Requirements</span></span>



| <span data-ttu-id="30f6b-123">需求</span><span class="sxs-lookup"><span data-stu-id="30f6b-123">Requirement</span></span> | <span data-ttu-id="30f6b-124">值</span><span class="sxs-lookup"><span data-stu-id="30f6b-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="30f6b-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="30f6b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="30f6b-126">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="30f6b-126">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="30f6b-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="30f6b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="30f6b-128">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="30f6b-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="30f6b-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="30f6b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30f6b-130">**應用程式。 Views**</span><span class="sxs-lookup"><span data-stu-id="30f6b-130">**Application.Views**</span></span>](windowsribbon-element-application-views.md)
</dt> </dl>

 

 






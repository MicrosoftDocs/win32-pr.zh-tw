---
title: LargeImages 屬性
description: 代表影像的容器;在此案例中為大型影像。
ms.assetid: 9fcd3694-7847-43e2-9877-47daf47aae9a
keywords:
- LargeImages 屬性 Windows 功能區
topic_type:
- apiref
api_name:
- Command.LargeImages
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf71557506d4b9cced21069473d1a6db9b208b8c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466584"
---
# <a name="commandlargeimages-property"></a><span data-ttu-id="80c56-104">LargeImages 屬性</span><span class="sxs-lookup"><span data-stu-id="80c56-104">Command.LargeImages property</span></span>

<span data-ttu-id="80c56-105">代表影像的容器;在此案例中為大型影像。</span><span class="sxs-lookup"><span data-stu-id="80c56-105">Represents a container of images; in this case, large images.</span></span>

## <a name="usage"></a><span data-ttu-id="80c56-106">使用方式</span><span class="sxs-lookup"><span data-stu-id="80c56-106">Usage</span></span>

``` syntax
<Command.LargeImages>
  child elements
</Command.LargeImages>
```

## <a name="attributes"></a><span data-ttu-id="80c56-107">屬性</span><span class="sxs-lookup"><span data-stu-id="80c56-107">Attributes</span></span>

<span data-ttu-id="80c56-108">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="80c56-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="80c56-109">子元素</span><span class="sxs-lookup"><span data-stu-id="80c56-109">Child elements</span></span>



| <span data-ttu-id="80c56-110">元素</span><span class="sxs-lookup"><span data-stu-id="80c56-110">Element</span></span>                                                 | <span data-ttu-id="80c56-111">描述</span><span class="sxs-lookup"><span data-stu-id="80c56-111">Description</span></span>                                        |
|---------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="80c56-112">**圖像**</span><span class="sxs-lookup"><span data-stu-id="80c56-112">**Image**</span></span>](windowsribbon-element-image.md)<br/> | <span data-ttu-id="80c56-113">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="80c56-113">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="80c56-114">父元素</span><span class="sxs-lookup"><span data-stu-id="80c56-114">Parent elements</span></span>



| <span data-ttu-id="80c56-115">元素</span><span class="sxs-lookup"><span data-stu-id="80c56-115">Element</span></span>                                                     |
|-------------------------------------------------------------|
| [<span data-ttu-id="80c56-116">**命令**</span><span class="sxs-lookup"><span data-stu-id="80c56-116">**Command**</span></span>](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="80c56-117">備註</span><span class="sxs-lookup"><span data-stu-id="80c56-117">Remarks</span></span>

<span data-ttu-id="80c56-118">選擇性。</span><span class="sxs-lookup"><span data-stu-id="80c56-118">Optional.</span></span>

<span data-ttu-id="80c56-119">每個 [**命令**](windowsribbon-element-command.md)最多可能會發生一次。</span><span class="sxs-lookup"><span data-stu-id="80c56-119">May occur at most once for each [**Command**](windowsribbon-element-command.md).</span></span>

<span data-ttu-id="80c56-120">影像資源必須符合 Windows 中所使用的標準點陣圖 (BMP) 圖形格式。</span><span class="sxs-lookup"><span data-stu-id="80c56-120">Image resources must conform to the standard bitmap (BMP) graphics format used in Windows.</span></span>

## <a name="examples"></a><span data-ttu-id="80c56-121">範例</span><span class="sxs-lookup"><span data-stu-id="80c56-121">Examples</span></span>

<span data-ttu-id="80c56-122">下列範例示範具有 [**MenuGroup**](windowsribbon-element-menugroup.md)元素之 [**SplitButton**](windowsribbon-element-splitbutton.md)的基本標記。</span><span class="sxs-lookup"><span data-stu-id="80c56-122">The following example demonstrates the basic markup for the [**SplitButton**](windowsribbon-element-splitbutton.md) with a [**MenuGroup**](windowsribbon-element-menugroup.md) element.</span></span>

<span data-ttu-id="80c56-123">這段程式碼會顯示具有大型和小型影像資源的 [**SplitButton**](windowsribbon-element-splitbutton.md) 和 [**MenuGroup**](windowsribbon-element-menugroup.md) 命令宣告。</span><span class="sxs-lookup"><span data-stu-id="80c56-123">This section of code shows the [**SplitButton**](windowsribbon-element-splitbutton.md) and [**MenuGroup**](windowsribbon-element-menugroup.md) Command declarations with a large and a small image resource.</span></span> <span data-ttu-id="80c56-124">也會宣告作為 **SplitButton** 專案父容器的相關聯 [**群組**](windowsribbon-element-group.md)。</span><span class="sxs-lookup"><span data-stu-id="80c56-124">An associated [**Group**](windowsribbon-element-group.md) that acts as the parent container for the **SplitButton** element is also declared.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="80c56-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="80c56-125">Requirements</span></span>



| <span data-ttu-id="80c56-126">需求</span><span class="sxs-lookup"><span data-stu-id="80c56-126">Requirement</span></span> | <span data-ttu-id="80c56-127">值</span><span class="sxs-lookup"><span data-stu-id="80c56-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="80c56-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="80c56-128">Minimum supported client</span></span><br/> | <span data-ttu-id="80c56-129">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="80c56-129">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="80c56-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="80c56-130">Minimum supported server</span></span><br/> | <span data-ttu-id="80c56-131">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="80c56-131">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="80c56-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="80c56-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80c56-133">指定功能區影像資源</span><span class="sxs-lookup"><span data-stu-id="80c56-133">Specifying Ribbon Image Resources</span></span>](windowsribbon-imageformats.md)
</dt> <dt>

[<span data-ttu-id="80c56-134">UI \_ PKEY \_ LargeImage</span><span class="sxs-lookup"><span data-stu-id="80c56-134">UI\_PKEY\_LargeImage</span></span>](windowsribbon-reference-properties-uipkey-largeimage.md)
</dt> </dl>

 

 






---
title: HelpButton 屬性
description: 代表 [說明] 按鈕的容器。
ms.assetid: a64239b2-2440-4bcf-8fd7-079003de6d8c
keywords:
- HelpButton 屬性視窗功能區
topic_type:
- apiref
api_name:
- Ribbon.HelpButton
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49e343a5181479ede5d428937908ed4bf37764f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686106"
---
# <a name="ribbonhelpbutton-property"></a><span data-ttu-id="b37ae-104">HelpButton 屬性</span><span class="sxs-lookup"><span data-stu-id="b37ae-104">Ribbon.HelpButton property</span></span>

<span data-ttu-id="b37ae-105">代表 [說明] [按鈕](windowsribbon-controls-helpbutton.md)的容器。</span><span class="sxs-lookup"><span data-stu-id="b37ae-105">Represents a container for the [Help Button](windowsribbon-controls-helpbutton.md).</span></span>

## <a name="usage"></a><span data-ttu-id="b37ae-106">使用方式</span><span class="sxs-lookup"><span data-stu-id="b37ae-106">Usage</span></span>

``` syntax
<Ribbon.HelpButton>
  child elements
</Ribbon.HelpButton>
```

## <a name="attributes"></a><span data-ttu-id="b37ae-107">屬性</span><span class="sxs-lookup"><span data-stu-id="b37ae-107">Attributes</span></span>

<span data-ttu-id="b37ae-108">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="b37ae-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="b37ae-109">子元素</span><span class="sxs-lookup"><span data-stu-id="b37ae-109">Child elements</span></span>



| <span data-ttu-id="b37ae-110">元素</span><span class="sxs-lookup"><span data-stu-id="b37ae-110">Element</span></span>                                                           | <span data-ttu-id="b37ae-111">描述</span><span class="sxs-lookup"><span data-stu-id="b37ae-111">Description</span></span>                                   |
|-------------------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="b37ae-112">**HelpButton**</span><span class="sxs-lookup"><span data-stu-id="b37ae-112">**HelpButton**</span></span>](windowsribbon-element-helpbutton.md)<br/> | <span data-ttu-id="b37ae-113">最多可能發生一次</span><span class="sxs-lookup"><span data-stu-id="b37ae-113">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="b37ae-114">父元素</span><span class="sxs-lookup"><span data-stu-id="b37ae-114">Parent elements</span></span>



| <span data-ttu-id="b37ae-115">元素</span><span class="sxs-lookup"><span data-stu-id="b37ae-115">Element</span></span>                                                   |
|-----------------------------------------------------------|
| [<span data-ttu-id="b37ae-116">**功能區**</span><span class="sxs-lookup"><span data-stu-id="b37ae-116">**Ribbon**</span></span>](windowsribbon-element-ribbon.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="b37ae-117">備註</span><span class="sxs-lookup"><span data-stu-id="b37ae-117">Remarks</span></span>

<span data-ttu-id="b37ae-118">選擇性。</span><span class="sxs-lookup"><span data-stu-id="b37ae-118">Optional.</span></span>

<span data-ttu-id="b37ae-119">每個 [**功能區**](windowsribbon-element-ribbon.md)最多可能會發生一次。</span><span class="sxs-lookup"><span data-stu-id="b37ae-119">May occur at most once for each [**Ribbon**](windowsribbon-element-ribbon.md).</span></span>

## <a name="examples"></a><span data-ttu-id="b37ae-120">範例</span><span class="sxs-lookup"><span data-stu-id="b37ae-120">Examples</span></span>

<span data-ttu-id="b37ae-121">下列範例將示範執行功能區說明按鈕所需的基本標記。</span><span class="sxs-lookup"><span data-stu-id="b37ae-121">The following example demonstrates the basic markup that is required to implement a Ribbon Help button.</span></span>

<span data-ttu-id="b37ae-122">這段程式碼會顯示 **HelpButton** 命令宣告。</span><span class="sxs-lookup"><span data-stu-id="b37ae-122">This section of code shows the **Ribbon.HelpButton** Command declaration.</span></span>


```XML
<Command Name="cmdHelp"
         Symbol="IDR_CMD_HELP">      
</Command>
```



<span data-ttu-id="b37ae-123">這段程式碼會顯示 **HelpButton** 控制項宣告。</span><span class="sxs-lookup"><span data-stu-id="b37ae-123">This section of code shows the **Ribbon.HelpButton** control declaration.</span></span>


```XML
<Ribbon.HelpButton>
  <HelpButton CommandName="cmdHelp"/>
</Ribbon.HelpButton>
```



## <a name="requirements"></a><span data-ttu-id="b37ae-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="b37ae-124">Requirements</span></span>



| <span data-ttu-id="b37ae-125">需求</span><span class="sxs-lookup"><span data-stu-id="b37ae-125">Requirement</span></span> | <span data-ttu-id="b37ae-126">值</span><span class="sxs-lookup"><span data-stu-id="b37ae-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="b37ae-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b37ae-127">Minimum supported client</span></span><br/> | <span data-ttu-id="b37ae-128">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b37ae-128">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="b37ae-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b37ae-129">Minimum supported server</span></span><br/> | <span data-ttu-id="b37ae-130">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b37ae-130">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 






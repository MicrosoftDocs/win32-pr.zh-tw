---
title: HelpButton 元素
description: 表示説明按鈕控制項。
ms.assetid: 24c709da-539e-4ea0-bd3e-d3fbd72dfb97
keywords:
- HelpButton 元素視窗功能區
topic_type:
- apiref
api_name:
- HelpButton
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9f34f04133b7628cce01ac0ce2808923b4f6bbdb
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111442839"
---
# <a name="helpbutton-element"></a><span data-ttu-id="84828-104">HelpButton 元素</span><span class="sxs-lookup"><span data-stu-id="84828-104">HelpButton element</span></span>

<span data-ttu-id="84828-105">表示 [説明按鈕](windowsribbon-controls-helpbutton.md) 控制項。</span><span class="sxs-lookup"><span data-stu-id="84828-105">Represents the [Help Button](windowsribbon-controls-helpbutton.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="84828-106">使用方式</span><span class="sxs-lookup"><span data-stu-id="84828-106">Usage</span></span>

``` syntax
<HelpButton
  CommandName = "xs:positiveInteger or xs:string"/>
```

## <a name="attributes"></a><span data-ttu-id="84828-107">屬性</span><span class="sxs-lookup"><span data-stu-id="84828-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="84828-108">屬性</span><span class="sxs-lookup"><span data-stu-id="84828-108">Attribute</span></span></th>
<th><span data-ttu-id="84828-109">類型</span><span class="sxs-lookup"><span data-stu-id="84828-109">Type</span></span></th>
<th><span data-ttu-id="84828-110">必要</span><span class="sxs-lookup"><span data-stu-id="84828-110">Required</span></span></th>
<th><span data-ttu-id="84828-111">描述</span><span class="sxs-lookup"><span data-stu-id="84828-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="84828-112"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="84828-112"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="84828-113">xs： positiveInteger 或 xs： string</span><span class="sxs-lookup"><span data-stu-id="84828-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="84828-114">否</span><span class="sxs-lookup"><span data-stu-id="84828-114">No</span></span><br/></td>
<td><span data-ttu-id="84828-115">將元素與 <a href="windowsribbon-element-command.md"><strong>命令</strong></a>產生關聯。</span><span class="sxs-lookup"><span data-stu-id="84828-115">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="84828-116">
<dt><span></span><span></span><strong></strong> (xs： positiveInteger 或 xs： string) </span><span class="sxs-lookup"><span data-stu-id="84828-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="84828-117">字串、介於2與59999（含）之間的整數值，或介於0x2 與0xea5f （含）之間的十六進位值。</span><span class="sxs-lookup"><span data-stu-id="84828-117">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="84828-118">值在功能區 XML 檔中必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="84828-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="84828-119">最大長度：100個字元。</span><span class="sxs-lookup"><span data-stu-id="84828-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="84828-120">子元素</span><span class="sxs-lookup"><span data-stu-id="84828-120">Child elements</span></span>

<span data-ttu-id="84828-121">沒有任何子項目。</span><span class="sxs-lookup"><span data-stu-id="84828-121">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="84828-122">父元素</span><span class="sxs-lookup"><span data-stu-id="84828-122">Parent elements</span></span>



| <span data-ttu-id="84828-123">元素</span><span class="sxs-lookup"><span data-stu-id="84828-123">Element</span></span>                                                                         |
|---------------------------------------------------------------------------------|
| [<span data-ttu-id="84828-124">**功能區. HelpButton**</span><span class="sxs-lookup"><span data-stu-id="84828-124">**Ribbon.HelpButton**</span></span>](windowsribbon-element-ribbon-helpbutton.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="84828-125">備註</span><span class="sxs-lookup"><span data-stu-id="84828-125">Remarks</span></span>

<span data-ttu-id="84828-126">選擇性。</span><span class="sxs-lookup"><span data-stu-id="84828-126">Optional.</span></span>

<span data-ttu-id="84828-127">每個功能區最多可能會發生一次 [**。 HelpButton**](windowsribbon-element-ribbon-helpbutton.md)。</span><span class="sxs-lookup"><span data-stu-id="84828-127">May occur at most once for each [**Ribbon.HelpButton**](windowsribbon-element-ribbon-helpbutton.md).</span></span>

<span data-ttu-id="84828-128">當您按一下時，會啟動應用程式說明對話方塊。</span><span class="sxs-lookup"><span data-stu-id="84828-128">Launches an application help dialog box when clicked.</span></span>

## <a name="examples"></a><span data-ttu-id="84828-129">範例</span><span class="sxs-lookup"><span data-stu-id="84828-129">Examples</span></span>

<span data-ttu-id="84828-130">下列範例將示範執行功能區說明 [按鈕](windowsribbon-controls-helpbutton.md) 控制項所需的基本標記。</span><span class="sxs-lookup"><span data-stu-id="84828-130">The following example demonstrates the basic markup that is required to implement a Ribbon [Help Button](windowsribbon-controls-helpbutton.md) control.</span></span>

<span data-ttu-id="84828-131">這段程式碼會顯示 **HelpButton** 命令宣告。</span><span class="sxs-lookup"><span data-stu-id="84828-131">This section of code shows the **HelpButton** Command declaration.</span></span>


```XML
<Command Name="cmdHelp"
         Symbol="IDR_CMD_HELP">      
</Command>
```



<span data-ttu-id="84828-132">這段程式碼會顯示 **HelpButton** 控制項宣告。</span><span class="sxs-lookup"><span data-stu-id="84828-132">This section of code shows the **HelpButton** control declaration.</span></span>


```XML
<Ribbon.HelpButton>
  <HelpButton CommandName="cmdHelp"/>
</Ribbon.HelpButton>
```



## <a name="element-information"></a><span data-ttu-id="84828-133">項目資訊</span><span class="sxs-lookup"><span data-stu-id="84828-133">Element information</span></span>

* <span data-ttu-id="84828-134">**最低支援系統**： Windows 7</span><span class="sxs-lookup"><span data-stu-id="84828-134">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="84828-135">**可以是空** 的：是</span><span class="sxs-lookup"><span data-stu-id="84828-135">**Can be empty**: Yes</span></span>



## <a name="see-also"></a><span data-ttu-id="84828-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="84828-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84828-137">說明按鈕控制項</span><span class="sxs-lookup"><span data-stu-id="84828-137">Help Button control</span></span>](windowsribbon-controls-helpbutton.md)
</dt> </dl>

 

 






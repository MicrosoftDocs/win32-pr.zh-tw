---
title: QuickAccessToolbar 元素
description: 代表快速存取工具列 (QAT) ，此為顯示功能區命令快速鍵的小工具欄。
ms.assetid: 59aa35c3-a844-46b3-b066-c9a321fb0891
keywords:
- QuickAccessToolbar 元素視窗功能區
topic_type:
- apiref
api_name:
- QuickAccessToolbar
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0076890a8d9858d4bf410ecfdd866bf4f48fdbb6
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/11/2020
ms.locfileid: "104374310"
---
# <a name="quickaccesstoolbar-element"></a><span data-ttu-id="bebfe-104">QuickAccessToolbar 元素</span><span class="sxs-lookup"><span data-stu-id="bebfe-104">QuickAccessToolbar element</span></span>

<span data-ttu-id="bebfe-105">代表 [快速存取工具列 (QAT) ](windowsribbon-controls-quickaccesstoolbar.md)，此為顯示功能區命令快速鍵的小工具欄。</span><span class="sxs-lookup"><span data-stu-id="bebfe-105">Represents the [Quick Access Toolbar (QAT)](windowsribbon-controls-quickaccesstoolbar.md), a small toolbar that displays shortcuts to Ribbon Commands.</span></span>

## <a name="usage"></a><span data-ttu-id="bebfe-106">使用方式</span><span class="sxs-lookup"><span data-stu-id="bebfe-106">Usage</span></span>

``` syntax
<QuickAccessToolbar
  CommandName = "xs:positiveInteger or xs:string"
  CustomizeCommandName = "xs:positiveInteger or xs:string">
  child elements
</QuickAccessToolbar>
```

## <a name="attributes"></a><span data-ttu-id="bebfe-107">屬性</span><span class="sxs-lookup"><span data-stu-id="bebfe-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bebfe-108">屬性</span><span class="sxs-lookup"><span data-stu-id="bebfe-108">Attribute</span></span></th>
<th><span data-ttu-id="bebfe-109">類型</span><span class="sxs-lookup"><span data-stu-id="bebfe-109">Type</span></span></th>
<th><span data-ttu-id="bebfe-110">必要</span><span class="sxs-lookup"><span data-stu-id="bebfe-110">Required</span></span></th>
<th><span data-ttu-id="bebfe-111">描述</span><span class="sxs-lookup"><span data-stu-id="bebfe-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bebfe-112"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="bebfe-112"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="bebfe-113">xs： positiveInteger 或 xs： string</span><span class="sxs-lookup"><span data-stu-id="bebfe-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="bebfe-114">No</span><span class="sxs-lookup"><span data-stu-id="bebfe-114">No</span></span><br/></td>
<td><span data-ttu-id="bebfe-115">將元素與 <a href="windowsribbon-element-command.md"><strong>命令</strong></a>產生關聯。</span><span class="sxs-lookup"><span data-stu-id="bebfe-115">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="bebfe-116">
<dt><span></span><span></span><strong></strong> (xs： positiveInteger 或 xs： string) </span><span class="sxs-lookup"><span data-stu-id="bebfe-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="bebfe-117">字串、介於2與59999（含）之間的整數值，或介於0x2 與0xea5f （含）之間的十六進位值。</span><span class="sxs-lookup"><span data-stu-id="bebfe-117">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="bebfe-118">值在功能區 XML 檔中必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="bebfe-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="bebfe-119">最大長度：100個字元。</span><span class="sxs-lookup"><span data-stu-id="bebfe-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bebfe-120"><strong>CustomizeCommandName</strong></span><span class="sxs-lookup"><span data-stu-id="bebfe-120"><strong>CustomizeCommandName</strong></span></span><br/></td>
<td><span data-ttu-id="bebfe-121">xs： positiveInteger 或 xs： string</span><span class="sxs-lookup"><span data-stu-id="bebfe-121">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="bebfe-122">No</span><span class="sxs-lookup"><span data-stu-id="bebfe-122">No</span></span><br/></td>
<td><span data-ttu-id="bebfe-123">在 [QAT] 功能表中插入其他命令專案。</span><span class="sxs-lookup"><span data-stu-id="bebfe-123">Inserts an additional Command item in the QAT menu.</span></span><br/> <br/><span data-ttu-id="bebfe-124">
<dt><span></span><span></span><strong></strong> (xs： positiveInteger 或 xs： string) </span><span class="sxs-lookup"><span data-stu-id="bebfe-124">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <img src="images/markup/qat-customizecommandname.png" alt="Screen shot of a QAT menu with the More commands... Command item." /><br/> <span data-ttu-id="bebfe-125">字串、介於2與59999（含）之間的整數值，或介於0x2 與0xea5f （含）之間的十六進位值。</span><span class="sxs-lookup"><span data-stu-id="bebfe-125">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="bebfe-126">值在功能區 XML 檔中必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="bebfe-126">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="bebfe-127">最大長度：100個字元。</span><span class="sxs-lookup"><span data-stu-id="bebfe-127">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="bebfe-128">子元素</span><span class="sxs-lookup"><span data-stu-id="bebfe-128">Child elements</span></span>



| <span data-ttu-id="bebfe-129">元素</span><span class="sxs-lookup"><span data-stu-id="bebfe-129">Element</span></span>                                                                                                                   | <span data-ttu-id="bebfe-130">描述</span><span class="sxs-lookup"><span data-stu-id="bebfe-130">Description</span></span>                                   |
|---------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="bebfe-131">**QuickAccessToolbar. s**</span><span class="sxs-lookup"><span data-stu-id="bebfe-131">**QuickAccessToolbar.ApplicationDefaults**</span></span>](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md)<br/> | <span data-ttu-id="bebfe-132">最多可能發生一次</span><span class="sxs-lookup"><span data-stu-id="bebfe-132">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="bebfe-133">父元素</span><span class="sxs-lookup"><span data-stu-id="bebfe-133">Parent elements</span></span>



| <span data-ttu-id="bebfe-134">元素</span><span class="sxs-lookup"><span data-stu-id="bebfe-134">Element</span></span>                                                                                         |
|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bebfe-135">**功能區. QuickAccessToolbar**</span><span class="sxs-lookup"><span data-stu-id="bebfe-135">**Ribbon.QuickAccessToolbar**</span></span>](windowsribbon-element-ribbon-quickaccesstoolbar.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="bebfe-136">備註</span><span class="sxs-lookup"><span data-stu-id="bebfe-136">Remarks</span></span>

<span data-ttu-id="bebfe-137">必要。</span><span class="sxs-lookup"><span data-stu-id="bebfe-137">Required.</span></span>

<span data-ttu-id="bebfe-138">每個 [**QuickAccessToolbar**](windowsribbon-element-ribbon-quickaccesstoolbar.md)都必須剛好發生一次。</span><span class="sxs-lookup"><span data-stu-id="bebfe-138">Must occur exactly once for each [**Ribbon.QuickAccessToolbar**](windowsribbon-element-ribbon-quickaccesstoolbar.md).</span></span>

<span data-ttu-id="bebfe-139">QAT 中的專案可以在執行時間加入或移除。</span><span class="sxs-lookup"><span data-stu-id="bebfe-139">Items in the QAT can be added or removed at run time.</span></span>

<span data-ttu-id="bebfe-140">為了在功能區應用程式之間保持一致性，建議 *CustomizeCommandName* 命令處理常式啟動 QAT 自訂對話方塊。</span><span class="sxs-lookup"><span data-stu-id="bebfe-140">For consistency across Ribbon applications, it is recommended that the *CustomizeCommandName* Command handler launch a QAT customization dialog.</span></span>

## <a name="examples"></a><span data-ttu-id="bebfe-141">範例</span><span class="sxs-lookup"><span data-stu-id="bebfe-141">Examples</span></span>

<span data-ttu-id="bebfe-142">下列範例示範 **QuickAccessToolbar** 的基本標記。</span><span class="sxs-lookup"><span data-stu-id="bebfe-142">The following example demonstrates the basic markup for the **QuickAccessToolbar**.</span></span>

<span data-ttu-id="bebfe-143">這段程式碼會顯示 **QuickAccessToolbar** 命令宣告。</span><span class="sxs-lookup"><span data-stu-id="bebfe-143">This section of code shows the **QuickAccessToolbar** Command declaration.</span></span>


```XML
<Command Name="cmdQAT"
         Symbol="ID_QAT"
         Id="40000"/>
<Command Name="cmdCustomizeQAT"
         Symbol="ID_CUSTOM_QAT"
         Id="40001"/>
```



<span data-ttu-id="bebfe-144">這段程式碼會顯示 **QuickAccessToolbar** 控制項宣告。</span><span class="sxs-lookup"><span data-stu-id="bebfe-144">This section of code shows the **QuickAccessToolbar** control declaration.</span></span>


```XML
      <Ribbon.QuickAccessToolbar>
        <QuickAccessToolbar CommandName="cmdQAT"
                            CustomizeCommandName="cmdCustomizeQAT">
          <QuickAccessToolbar.ApplicationDefaults>
            <Button CommandName="cmdButton1"/>
            <ToggleButton CommandName="cmdMinimize"
                          ApplicationDefaults.IsChecked="false"/>
          </QuickAccessToolbar.ApplicationDefaults>
        </QuickAccessToolbar>
      </Ribbon.QuickAccessToolbar>
```



## <a name="element-information"></a><span data-ttu-id="bebfe-145">項目資訊</span><span class="sxs-lookup"><span data-stu-id="bebfe-145">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="bebfe-146">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="bebfe-146">Minimum supported system</span></span><br/> | <span data-ttu-id="bebfe-147">Windows 7</span><span class="sxs-lookup"><span data-stu-id="bebfe-147">Windows 7</span></span> |
| <span data-ttu-id="bebfe-148">可以是空的</span><span class="sxs-lookup"><span data-stu-id="bebfe-148">Can be empty</span></span>                        | <span data-ttu-id="bebfe-149">否</span><span class="sxs-lookup"><span data-stu-id="bebfe-149">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="bebfe-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bebfe-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bebfe-151">快速存取工具列控制項</span><span class="sxs-lookup"><span data-stu-id="bebfe-151">Quick Access Toolbar control</span></span>](windowsribbon-controls-quickaccesstoolbar.md)
</dt> </dl>

 

 






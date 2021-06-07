---
title: TabGroup 元素
description: 代表一組內容相關的索引標籤控制項。
ms.assetid: f131efe1-b8c4-416e-997a-5e2d3bcc03ea
keywords:
- TabGroup 元素視窗功能區
topic_type:
- apiref
api_name:
- TabGroup
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6a4c18db72d6b0161842bfde9d5a836d14189c6a
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444059"
---
# <a name="tabgroup-element"></a><span data-ttu-id="c2482-104">TabGroup 元素</span><span class="sxs-lookup"><span data-stu-id="c2482-104">TabGroup element</span></span>

<span data-ttu-id="c2482-105">代表一組內容相關的 [選項卡](windowsribbon-controls-tabgroup.md) 控制項。</span><span class="sxs-lookup"><span data-stu-id="c2482-105">Represents a contextual set of [Tab](windowsribbon-controls-tabgroup.md) controls.</span></span>

## <a name="usage"></a><span data-ttu-id="c2482-106">使用方式</span><span class="sxs-lookup"><span data-stu-id="c2482-106">Usage</span></span>

``` syntax
<TabGroup
  CommandName = "xs:positiveInteger or xs:string">
  child elements
</TabGroup>
```

## <a name="attributes"></a><span data-ttu-id="c2482-107">屬性</span><span class="sxs-lookup"><span data-stu-id="c2482-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c2482-108">屬性</span><span class="sxs-lookup"><span data-stu-id="c2482-108">Attribute</span></span></th>
<th><span data-ttu-id="c2482-109">類型</span><span class="sxs-lookup"><span data-stu-id="c2482-109">Type</span></span></th>
<th><span data-ttu-id="c2482-110">必要</span><span class="sxs-lookup"><span data-stu-id="c2482-110">Required</span></span></th>
<th><span data-ttu-id="c2482-111">描述</span><span class="sxs-lookup"><span data-stu-id="c2482-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c2482-112"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="c2482-112"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="c2482-113">xs： positiveInteger 或 xs： string</span><span class="sxs-lookup"><span data-stu-id="c2482-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="c2482-114">否</span><span class="sxs-lookup"><span data-stu-id="c2482-114">No</span></span><br/></td>
<td><span data-ttu-id="c2482-115">將元素與 <a href="windowsribbon-element-command.md"><strong>命令</strong></a>產生關聯。</span><span class="sxs-lookup"><span data-stu-id="c2482-115">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="c2482-116">
<dt><span></span><span></span><strong></strong> (xs： positiveInteger 或 xs： string) </span><span class="sxs-lookup"><span data-stu-id="c2482-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="c2482-117">字串、介於2與59999（含）之間的整數值，或介於0x2 與0xea5f （含）之間的十六進位值。</span><span class="sxs-lookup"><span data-stu-id="c2482-117">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="c2482-118">值在功能區 XML 檔中必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="c2482-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="c2482-119">最大長度：100個字元。</span><span class="sxs-lookup"><span data-stu-id="c2482-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="c2482-120">子元素</span><span class="sxs-lookup"><span data-stu-id="c2482-120">Child elements</span></span>



| <span data-ttu-id="c2482-121">元素</span><span class="sxs-lookup"><span data-stu-id="c2482-121">Element</span></span>                                             | <span data-ttu-id="c2482-122">描述</span><span class="sxs-lookup"><span data-stu-id="c2482-122">Description</span></span>                                     |
|-----------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="c2482-123">**索引標籤**</span><span class="sxs-lookup"><span data-stu-id="c2482-123">**Tab**</span></span>](windowsribbon-element-tab.md)<br/> | <span data-ttu-id="c2482-124">至少必須發生一次</span><span class="sxs-lookup"><span data-stu-id="c2482-124">Must occur at least once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="c2482-125">父元素</span><span class="sxs-lookup"><span data-stu-id="c2482-125">Parent elements</span></span>



| <span data-ttu-id="c2482-126">元素</span><span class="sxs-lookup"><span data-stu-id="c2482-126">Element</span></span>                                                                                 |
|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="c2482-127">**功能區. CoNtextualTabs**</span><span class="sxs-lookup"><span data-stu-id="c2482-127">**Ribbon.ContextualTabs**</span></span>](windowsribbon-element-ribbon-contextualtabs.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="c2482-128">備註</span><span class="sxs-lookup"><span data-stu-id="c2482-128">Remarks</span></span>

<span data-ttu-id="c2482-129">必要。</span><span class="sxs-lookup"><span data-stu-id="c2482-129">Required.</span></span>

<span data-ttu-id="c2482-130">每個 [**CoNtextualTabs**](windowsribbon-element-ribbon-contextualtabs.md) 元素至少必須發生一次。</span><span class="sxs-lookup"><span data-stu-id="c2482-130">Must occur at least once for each [**Ribbon.ContextualTabs**](windowsribbon-element-ribbon-contextualtabs.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="c2482-131">範例</span><span class="sxs-lookup"><span data-stu-id="c2482-131">Examples</span></span>

<span data-ttu-id="c2482-132">下列範例示範 **TabGroup** 元素的基本標記。</span><span class="sxs-lookup"><span data-stu-id="c2482-132">The following example demonstrates the basic markup for the **TabGroup** element.</span></span>

<span data-ttu-id="c2482-133">這段程式碼會顯示具有兩個內容索引標籤的 **TabGroup** 命令宣告。</span><span class="sxs-lookup"><span data-stu-id="c2482-133">This section of code shows a **TabGroup** Command declaration with two contextual tabs.</span></span>


```XML
<!-- Contextual Tabs -->
<Command Name='cmdContextualTab1'
         LabelTitle='Contextual Tab 1'
         Symbol='ID_CONTEXTUALTAB1'/>
<Command Name='cmdContextualTab2'
         LabelTitle='Contextual Tab 2'
         Symbol='ID_CONTEXTUALTAB2'/>
<Command Name='cmdContextualTabGroup'
         LabelTitle='Contextual Tabs'
         Symbol='ID_CONTEXTUALTAB_GROUP'/>
```



<span data-ttu-id="c2482-134">這段程式碼會顯示對應的 **TabGroup** 控制項宣告。</span><span class="sxs-lookup"><span data-stu-id="c2482-134">This section of code shows corresponding **TabGroup** control declarations.</span></span>


```XML
      <Ribbon.ContextualTabs>
        <TabGroup CommandName='cmdContextualTabGroup'>
          <Tab CommandName='cmdContextualTab1'>
            <!--InRibbonGallery Group-->
            <Group CommandName='cmdInRibbonGalleryGroup'
                   SizeDefinition='OneInRibbonGallery'>
              <InRibbonGallery CommandName='cmdTextSizeGallery3'
                               HasLargeItems='true'
                               ItemHeight='32'
                               ItemWidth='32'
                               MaxColumns='3' >
                <InRibbonGallery.MenuLayout>
                  <FlowMenuLayout Columns='3'
                                  Gripper ='Corner'/>
                </InRibbonGallery.MenuLayout>
              </InRibbonGallery>
            </Group>
            <!--Command Galleries Group-->
            <Group CommandName='cmdCommandGalleriesGroup'
                   SizeDefinition='OneInRibbonGallery'>
              <InRibbonGallery CommandName='cmdCommandGallery1'
                               Type='Commands'
                               MaxRows='3'
                               MaxColumns='3'>
                <InRibbonGallery.MenuLayout>
                  <FlowMenuLayout Columns='3'
                                  Gripper ='Corner'/>
                </InRibbonGallery.MenuLayout>
              </InRibbonGallery>
            </Group>
          </Tab>
          <Tab CommandName='cmdContextualTab2'></Tab>
        </TabGroup>
      </Ribbon.ContextualTabs> 
```



## <a name="element-information"></a><span data-ttu-id="c2482-135">項目資訊</span><span class="sxs-lookup"><span data-stu-id="c2482-135">Element information</span></span>

- <span data-ttu-id="c2482-136">**最低支援系統**： Windows 7</span><span class="sxs-lookup"><span data-stu-id="c2482-136">**Minimum supported system**: Windows 7</span></span> 
- <span data-ttu-id="c2482-137">**可以是空** 的：否</span><span class="sxs-lookup"><span data-stu-id="c2482-137">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="c2482-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c2482-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2482-139">Tab 群組控制項</span><span class="sxs-lookup"><span data-stu-id="c2482-139">Tab Group control</span></span>](windowsribbon-controls-tabgroup.md)
</dt> <dt>

[<span data-ttu-id="c2482-140">索引標籤控制項</span><span class="sxs-lookup"><span data-stu-id="c2482-140">Tab control</span></span>](windowsribbon-controls-tab.md)
</dt> </dl>

 

 






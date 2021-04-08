---
title: CoNtextualTabs 屬性
description: 表示內容索引標籤的容器。
ms.assetid: 1f57a8d7-97ac-4007-8a36-c6aec5b85e6c
keywords:
- CoNtextualTabs 屬性視窗功能區
topic_type:
- apiref
api_name:
- Ribbon.ContextualTabs
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 790a7c93df71ab5117b591367c6b80fc0f8a748d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685666"
---
# <a name="ribboncontextualtabs-property"></a><span data-ttu-id="99a55-104">CoNtextualTabs 屬性</span><span class="sxs-lookup"><span data-stu-id="99a55-104">Ribbon.ContextualTabs property</span></span>

<span data-ttu-id="99a55-105">表示內容索引標籤的容器。</span><span class="sxs-lookup"><span data-stu-id="99a55-105">Represents a container for contextual tabs.</span></span>

## <a name="usage"></a><span data-ttu-id="99a55-106">使用方式</span><span class="sxs-lookup"><span data-stu-id="99a55-106">Usage</span></span>

``` syntax
<Ribbon.ContextualTabs>
  child elements
</Ribbon.ContextualTabs>
```

## <a name="attributes"></a><span data-ttu-id="99a55-107">屬性</span><span class="sxs-lookup"><span data-stu-id="99a55-107">Attributes</span></span>

<span data-ttu-id="99a55-108">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="99a55-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="99a55-109">子元素</span><span class="sxs-lookup"><span data-stu-id="99a55-109">Child elements</span></span>



| <span data-ttu-id="99a55-110">元素</span><span class="sxs-lookup"><span data-stu-id="99a55-110">Element</span></span>                                                       | <span data-ttu-id="99a55-111">描述</span><span class="sxs-lookup"><span data-stu-id="99a55-111">Description</span></span>                                     |
|---------------------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="99a55-112">**TabGroup**</span><span class="sxs-lookup"><span data-stu-id="99a55-112">**TabGroup**</span></span>](windowsribbon-element-tabgroup.md)<br/> | <span data-ttu-id="99a55-113">至少必須發生一次</span><span class="sxs-lookup"><span data-stu-id="99a55-113">Must occur at least once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="99a55-114">父元素</span><span class="sxs-lookup"><span data-stu-id="99a55-114">Parent elements</span></span>



| <span data-ttu-id="99a55-115">元素</span><span class="sxs-lookup"><span data-stu-id="99a55-115">Element</span></span>                                                   |
|-----------------------------------------------------------|
| [<span data-ttu-id="99a55-116">**功能區**</span><span class="sxs-lookup"><span data-stu-id="99a55-116">**Ribbon**</span></span>](windowsribbon-element-ribbon.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="99a55-117">備註</span><span class="sxs-lookup"><span data-stu-id="99a55-117">Remarks</span></span>

<span data-ttu-id="99a55-118">選擇性。</span><span class="sxs-lookup"><span data-stu-id="99a55-118">Optional.</span></span>

<span data-ttu-id="99a55-119">每個 [**功能區**](windowsribbon-element-ribbon.md)最多可能會發生一次。</span><span class="sxs-lookup"><span data-stu-id="99a55-119">May occur at most once for each [**Ribbon**](windowsribbon-element-ribbon.md).</span></span>

<span data-ttu-id="99a55-120">內容索引標籤適合用來顯示僅與特定應用程式內容相關的功能，例如文字編輯器中的 [影像格式設定] 索引標籤，只有在顯示影像時才會顯示。</span><span class="sxs-lookup"><span data-stu-id="99a55-120">Contextual tabs are useful for displaying functionality that is relevant only to a specific application context, such as an image formatting tab in a text editor that is displayed only when an image is highlighted.</span></span> <span data-ttu-id="99a55-121">一般而言，在特定應用程式內容發生之前，內容索引標籤不會顯示，而應用程式會通知功能區架構。</span><span class="sxs-lookup"><span data-stu-id="99a55-121">Typically, contextual tabs are not visible until a specific application context occurs, and the application notifies the Ribbon framework.</span></span>

<span data-ttu-id="99a55-122">顯示時，內容索引標籤會以色彩標示，以區別它們與一般索引標籤。</span><span class="sxs-lookup"><span data-stu-id="99a55-122">When displayed, contextual tabs are color coded to differentiate them from regular tabs.</span></span>

## <a name="examples"></a><span data-ttu-id="99a55-123">範例</span><span class="sxs-lookup"><span data-stu-id="99a55-123">Examples</span></span>

<span data-ttu-id="99a55-124">下列範例示範 **CoNtextualTabs** 元素的基本標記。</span><span class="sxs-lookup"><span data-stu-id="99a55-124">The following example demonstrates the basic markup for the **Ribbon.ContextualTabs** element.</span></span>

<span data-ttu-id="99a55-125">這段程式碼會顯示 [**TabGroup**](windowsribbon-element-tabgroup.md) 命令宣告和兩個內容索引卷 [**標命令宣告**](windowsribbon-element-tab.md) 。</span><span class="sxs-lookup"><span data-stu-id="99a55-125">This section of code shows a [**TabGroup**](windowsribbon-element-tabgroup.md) Command declaration and two contextual [**Tab**](windowsribbon-element-tab.md) Command declarations.</span></span>


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



<span data-ttu-id="99a55-126">這一節的程式碼會顯示 **CoNtextualTabs** 控制項宣告與 [**TabGroup**](windowsribbon-element-tabgroup.md) ，以及兩個內容相關的 [**選項卡**](windowsribbon-element-tab.md) 控制項。</span><span class="sxs-lookup"><span data-stu-id="99a55-126">This section of code shows the **Ribbon.ContextualTabs** control declaration with a [**TabGroup**](windowsribbon-element-tabgroup.md) and two contextual [**Tab**](windowsribbon-element-tab.md) controls.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="99a55-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="99a55-127">Requirements</span></span>



| <span data-ttu-id="99a55-128">需求</span><span class="sxs-lookup"><span data-stu-id="99a55-128">Requirement</span></span> | <span data-ttu-id="99a55-129">值</span><span class="sxs-lookup"><span data-stu-id="99a55-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="99a55-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="99a55-130">Minimum supported client</span></span><br/> | <span data-ttu-id="99a55-131">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="99a55-131">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="99a55-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="99a55-132">Minimum supported server</span></span><br/> | <span data-ttu-id="99a55-133">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="99a55-133">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="99a55-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="99a55-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="99a55-135">[**功能區] 索引標籤**](windowsribbon-element-ribbon-tabs.md)</span><span class="sxs-lookup"><span data-stu-id="99a55-135">[**Ribbon.Tabs**](windowsribbon-element-ribbon-tabs.md)</span></span>
</dt> </dl>

 

 






---
title: 顯示內容索引標籤
description: 在 Windows 功能區架構應用程式中，[內容] 索引標籤是隱藏的索引標籤控制項，會在應用程式工作區中的物件（例如影像）已選取或反白顯示時，顯示在索引標籤資料列中。
ms.assetid: 2059ca42-6a99-43a2-b1f5-ce5554156993
keywords:
- Windows 功能區，內容索引標籤
- 功能區，內容索引標籤
- 顯示 Windows 功能區的內容索引標籤
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8a1e81ac6587e39a04114fa2f938a6da0e9a4d1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682374"
---
# <a name="displaying-contextual-tabs"></a><span data-ttu-id="663a2-106">顯示內容索引標籤</span><span class="sxs-lookup"><span data-stu-id="663a2-106">Displaying Contextual Tabs</span></span>

<span data-ttu-id="663a2-107">在 Windows 功能區架構應用程式中，[內容] 索引標籤是隱藏的 [選項](windowsribbon-controls-tab.md) 卡控制項，會在應用程式工作區中的物件（例如影像）已選取或反白顯示時，顯示在索引標籤資料列中。</span><span class="sxs-lookup"><span data-stu-id="663a2-107">In a Windows Ribbon framework application, a contextual tab is a hidden [Tab](windowsribbon-controls-tab.md) control that is displayed in the tab row when an object in the application workspace, such as an image, is selected or highlighted.</span></span>

-   [<span data-ttu-id="663a2-108">簡介</span><span class="sxs-lookup"><span data-stu-id="663a2-108">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="663a2-109">執行內容相關索引標籤</span><span class="sxs-lookup"><span data-stu-id="663a2-109">Implementing Contextual Tabs</span></span>](#implementing-contextual-tabs)
    -   [<span data-ttu-id="663a2-110">標記</span><span class="sxs-lookup"><span data-stu-id="663a2-110">Markup</span></span>](#markup)
    -   [<span data-ttu-id="663a2-111">程式碼</span><span class="sxs-lookup"><span data-stu-id="663a2-111">Code</span></span>](#code)
-   [<span data-ttu-id="663a2-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="663a2-112">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="663a2-113">簡介</span><span class="sxs-lookup"><span data-stu-id="663a2-113">Introduction</span></span>

<span data-ttu-id="663a2-114">相較于包含各種常見命令的核心索引標籤（不論工作區內容為何），內容索引標籤通常會包含一或多個適用于所選或反白顯示物件的命令。</span><span class="sxs-lookup"><span data-stu-id="663a2-114">In contrast to core tabs, which contain various common Commands that are relevant regardless of workspace context, contextual tabs typically contain one or more Commands that are applicable to a selected or highlighted object only.</span></span>

<span data-ttu-id="663a2-115">在 [應用程式] 工作區中選取或反白顯示物件時，物件的類型和內容可能需要不同的命令，這些命令不會在某個內容索引標籤上進行組織或功能感知。在這些情況下，可能需要多個包含在索引標籤 [群組](windowsribbon-controls-tabgroup.md)內的內容索引標籤。</span><span class="sxs-lookup"><span data-stu-id="663a2-115">When an object is selected or highlighted in the application workspace, the type and context of the object might require disparate Commands that do not make organizational or functional sense on one contextual tab. In these cases, multiple contextual tabs, which are contained within a [Tab Group](windowsribbon-controls-tabgroup.md), may be required.</span></span> <span data-ttu-id="663a2-116">例如，選取資料表資料格中包含的影像可能需要兩個同時公開資料表和影像功能的內容索引標籤。</span><span class="sxs-lookup"><span data-stu-id="663a2-116">For example, selecting an image contained in a table cell might require two contextual tabs that expose both table and image functionality.</span></span>

> [!Note]  
> <span data-ttu-id="663a2-117">除了多個內容索引標籤之外，功能區架構也支援功能區中的多個索引標籤 [群組](windowsribbon-controls-tabgroup.md) 控制項。</span><span class="sxs-lookup"><span data-stu-id="663a2-117">In addition to multiple contextual tabs, the Ribbon framework also supports multiple [Tab Group](windowsribbon-controls-tabgroup.md) controls within a ribbon.</span></span>

 

<span data-ttu-id="663a2-118">顯示內容索引標籤時，功能區架構會強制執行一組基本的行為，包括：</span><span class="sxs-lookup"><span data-stu-id="663a2-118">When displaying contextual tabs, the Ribbon framework enforces a basic set of behaviors that include:</span></span>

-   <span data-ttu-id="663a2-119">內容索引標籤的定位順序是它們所宣告的順序，以及功能區索引標籤資料列中 [核心] 索引標籤右側的位置。</span><span class="sxs-lookup"><span data-stu-id="663a2-119">Contextual tabs are positioned in the order they are declared and to the right of core tabs in the ribbon tab row.</span></span>
-   <span data-ttu-id="663a2-120">調整功能區的大小時，會調整索引標籤，並在空間需要時截斷索引標籤標籤。</span><span class="sxs-lookup"><span data-stu-id="663a2-120">When the ribbon is resized, tabs are scaled and tab labels are truncated as space requires.</span></span> <span data-ttu-id="663a2-121">不過，可見的內容索引標籤會獲得較高的顯示優先順序，最後會將其調整和截斷。</span><span class="sxs-lookup"><span data-stu-id="663a2-121">However, visible contextual tabs are given a higher display priority in which they are scaled and truncated last.</span></span>
-   <span data-ttu-id="663a2-122">索引標籤 [群組](windowsribbon-controls-tabgroup.md) 的標籤會顯示在應用程式標題列中，並跨越所有相關聯的內容索引標籤。</span><span class="sxs-lookup"><span data-stu-id="663a2-122">The label for a [Tab Group](windowsribbon-controls-tabgroup.md) is displayed in the application title bar and spans all associated contextual tabs.</span></span>
-   <span data-ttu-id="663a2-123">同時顯示多個索引標籤 [群組](windowsribbon-controls-tabgroup.md) 控制項時，會在應用程式標題列的每個索引標籤群組的背景中，指派五種獨特的色彩之一。</span><span class="sxs-lookup"><span data-stu-id="663a2-123">When multiple [Tab Group](windowsribbon-controls-tabgroup.md) controls are displayed at the same time, one of five unique colors is assigned to the background of each Tab Group in the application title bar.</span></span> <span data-ttu-id="663a2-124">此色彩也可做為索引標籤群組中內容索引標籤的醒目提示色彩。</span><span class="sxs-lookup"><span data-stu-id="663a2-124">This color is also used as a highlight color for the contextual tabs in the Tab Group.</span></span>
-   <span data-ttu-id="663a2-125">索引標籤 [群組](windowsribbon-controls-tabgroup.md) 色彩指派是根據在標記中宣告索引標籤群組元素的順序。</span><span class="sxs-lookup"><span data-stu-id="663a2-125">The [Tab Group](windowsribbon-controls-tabgroup.md) color assignment is based on the order the Tab Group elements are declared in markup.</span></span> <span data-ttu-id="663a2-126">這些色彩是由架構所定義，且不能由應用程式指定。</span><span class="sxs-lookup"><span data-stu-id="663a2-126">The colors are defined by the framework and cannot be specified by the application.</span></span>
-   <span data-ttu-id="663a2-127">您可以透過[Framework Properties](windowsribbon-reference-properties-framework.md)屬性索引鍵，間接修改架構定義的索引標籤[群組](windowsribbon-controls-tabgroup.md)色彩。</span><span class="sxs-lookup"><span data-stu-id="663a2-127">The [Tab Group](windowsribbon-controls-tabgroup.md) colors defined by the framework can be modified indirectly through the [Framework Properties](windowsribbon-reference-properties-framework.md) property keys.</span></span> <span data-ttu-id="663a2-128">如需詳細資訊，請參閱 [自訂功能區色彩](ribbon-color.md)。</span><span class="sxs-lookup"><span data-stu-id="663a2-128">For more information, see [Customizing Ribbon Colors](ribbon-color.md).</span></span>
-   <span data-ttu-id="663a2-129">當任何一次都顯示五個以上的索引標籤 [群組](windowsribbon-controls-tabgroup.md) 控制項時，架構會迴圈相關聯的色彩。</span><span class="sxs-lookup"><span data-stu-id="663a2-129">When more than five [Tab Group](windowsribbon-controls-tabgroup.md) controls are displayed at any single time, the framework cycles the associated colors.</span></span>
-   <span data-ttu-id="663a2-130">功能區中的最大 [選項卡](windowsribbon-controls-tab.md) 控制項數目限制為100。</span><span class="sxs-lookup"><span data-stu-id="663a2-130">The maximum number of [Tab](windowsribbon-controls-tab.md) controls in a ribbon is limited to 100.</span></span> <span data-ttu-id="663a2-131">這包括內容索引標籤、可見或不可見。</span><span class="sxs-lookup"><span data-stu-id="663a2-131">This includes contextual tabs, visible or not.</span></span>

<span data-ttu-id="663a2-132">下列螢幕擷取畫面顯示 Windows 7 繪圖的內容索引標籤。</span><span class="sxs-lookup"><span data-stu-id="663a2-132">The following screen shot shows a contextual tab from Windows 7 Paint.</span></span>

![顯示內容索引標籤控制項的螢幕擷取畫面。](images/controls/contextualtab.png)

## <a name="implementing-contextual-tabs"></a><span data-ttu-id="663a2-134">執行內容相關索引標籤</span><span class="sxs-lookup"><span data-stu-id="663a2-134">Implementing Contextual Tabs</span></span>

<span data-ttu-id="663a2-135">本節將討論功能區內容索引標籤的執行詳細資料，並逐步解說如何將它們併入功能區應用程式中。</span><span class="sxs-lookup"><span data-stu-id="663a2-135">This section discusses the implementation details of Ribbon contextual tabs and walks through how to incorporate them in a Ribbon application.</span></span>

### <a name="markup"></a><span data-ttu-id="663a2-136">標記</span><span class="sxs-lookup"><span data-stu-id="663a2-136">Markup</span></span>

<span data-ttu-id="663a2-137">下列範例示範 [**TabGroup**](windowsribbon-element-tabgroup.md) 元素的基本標記，其中包含兩個內容索引標籤。</span><span class="sxs-lookup"><span data-stu-id="663a2-137">The following examples demonstrate the basic markup for a [**TabGroup**](windowsribbon-element-tabgroup.md) element that contains two contextual tabs.</span></span>

<span data-ttu-id="663a2-138">這段程式碼會顯示 [**TabGroup**](windowsribbon-element-tabgroup.md) 和 [Tab](windowsribbon-controls-tab.md) 命令宣告。</span><span class="sxs-lookup"><span data-stu-id="663a2-138">This section of code shows the [**TabGroup**](windowsribbon-element-tabgroup.md) and [Tab](windowsribbon-controls-tab.md) Command declarations.</span></span>


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



<span data-ttu-id="663a2-139">這一節的程式碼顯示在 [**TabGroup**](windowsribbon-element-tabgroup.md)內顯示兩個內容索引標籤所需的控制項宣告。</span><span class="sxs-lookup"><span data-stu-id="663a2-139">This section of code shows the control declarations required to display two contextual tabs within a [**TabGroup**](windowsribbon-element-tabgroup.md).</span></span>


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



### <a name="code"></a><span data-ttu-id="663a2-140">程式碼</span><span class="sxs-lookup"><span data-stu-id="663a2-140">Code</span></span>

<span data-ttu-id="663a2-141">[UI \_PKEY \_ CoNtextAvailable](windowsribbon-reference-properties-uipkey-contextavailable.md) 是架構定義的單一屬性索引鍵，用於指定內容索引標籤的可見度和狀態。</span><span class="sxs-lookup"><span data-stu-id="663a2-141">[UI\_PKEY\_ContextAvailable](windowsribbon-reference-properties-uipkey-contextavailable.md) is the single property key defined by the framework for specifying the visibility and state of contextual tabs.</span></span> <span data-ttu-id="663a2-142">在 [應用程式] 工作區中選取物件時，可以從 [**UI \_ CONTEXTAVAILABILITY**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_contextavailability) 列舉中指派三個值的其中一個，以定義內容索引標籤是否存在，如果存在，是否會顯示為使用中的索引標籤。</span><span class="sxs-lookup"><span data-stu-id="663a2-142">When an object is selected in the application workspace, this property can be assigned one of three values from the [**UI\_CONTEXTAVAILABILITY**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_contextavailability) enumeration that define whether a contextual tab exists and, if it does, whether it is shown as the active tab.</span></span>

<span data-ttu-id="663a2-143">應用程式會在工作區內容變更時，將[UI \_ PKEY \_ CoNtextAvailable](windowsribbon-reference-properties-uipkey-contextavailable.md)屬性設為失效和更新，藉以要求索引標籤[群組](windowsribbon-controls-tabgroup.md)更新。</span><span class="sxs-lookup"><span data-stu-id="663a2-143">An application requests a [Tab Group](windowsribbon-controls-tabgroup.md) update by invalidating and updating the [UI\_PKEY\_ContextAvailable](windowsribbon-reference-properties-uipkey-contextavailable.md) property when the workspace context changes.</span></span>

<span data-ttu-id="663a2-144">下列程式碼區段會示範如何在應用程式工作區中選取影像時，顯示內容相關索引標籤。</span><span class="sxs-lookup"><span data-stu-id="663a2-144">The follow sections of code demonstrate how to display a contextual tab when an image is selected in an application workspace.</span></span>


```C++
// Initialize the image tools contextual tab visibility setting.
UI_CONTEXTAVAILABILITY g_ImageTools = UI_CONTEXTAVAILABILITY_NOTAVAILABLE;

// Called when an image is selected in the application.
void SelectImage()
{
  ...
  g_ImageTools = UI_CONTEXTAVAILABILITY_ACTIVE;

  // Invalidate the UI_PKEY_ContextAvailable property of the image tools  
  // contextual tab Command and trigger the UpdatePropery callback function.
  pUIFramework->InvalidateUICommand(
                  cmdImageTabSet, 
                  UI_INVALIDATIONS_PROPERTY, 
                  UI_PKEY_ContextAvailable);
  ...
}

// Update Tab Group properties.
HRESULT MyTabGroupCommandHandler::UpdateProperty(
                                  UINT nCmdID,
                                  REFPROPERTYKEY key,
                                  const PROPVARIANT* ppropvarCurrentValue,
                                  PROPVARIANT* ppropvarNewValue)
{
  HRESULT hr = E_FAIL;

  if (key == UI_PKEY_ContextAvailable)
  {
    hr = UIInitPropertyFromUInt32(key, g_ImageTools, ppropvarNewValue);
  }
  ...
  return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="663a2-145">相關主題</span><span class="sxs-lookup"><span data-stu-id="663a2-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="663a2-146">功能區使用者體驗指導方針</span><span class="sxs-lookup"><span data-stu-id="663a2-146">Ribbon User Experience Guidelines</span></span>](https://msdn.microsoft.com/library/cc872782.aspx)
</dt> <dt>

[<span data-ttu-id="663a2-147">功能區設計流程</span><span class="sxs-lookup"><span data-stu-id="663a2-147">Ribbon Design Process</span></span>](https://msdn.microsoft.com/library/cc872781.aspx)
</dt> </dl>

 

 
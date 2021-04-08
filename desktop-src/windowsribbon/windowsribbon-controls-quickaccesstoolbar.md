---
title: 快速存取工具列
description: 快速存取工具列 (QAT) 是一個小型、可自訂的工具列，它會公開應用程式所指定的一組命令，或是由使用者選取的命令。
ms.assetid: b2adf4e9-0de1-4c4d-9293-693d0f7cf6fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20a50d562477e5c626d2d2bffa8ee5e0ecc84919
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023493"
---
# <a name="quick-access-toolbar"></a><span data-ttu-id="f549a-103">快速存取工具列</span><span class="sxs-lookup"><span data-stu-id="f549a-103">Quick Access Toolbar</span></span>

<span data-ttu-id="f549a-104">快速存取工具列 (QAT) 是一個小型、可自訂的工具列，它會公開應用程式所指定的一組命令，或是由使用者選取的命令。</span><span class="sxs-lookup"><span data-stu-id="f549a-104">The Quick Access Toolbar (QAT) is a small, customizable toolbar that exposes a set of Commands that are specified by the application or selected by the user.</span></span>

- [<span data-ttu-id="f549a-105">簡介</span><span class="sxs-lookup"><span data-stu-id="f549a-105">Introduction</span></span>](#introduction)
- [<span data-ttu-id="f549a-106">執行快速存取工具列</span><span class="sxs-lookup"><span data-stu-id="f549a-106">Implement the Quick Access Toolbar</span></span>](#implement-the-quick-access-toolbar)
  - [<span data-ttu-id="f549a-107">標記</span><span class="sxs-lookup"><span data-stu-id="f549a-107">Markup</span></span>](#markup)
  - [<span data-ttu-id="f549a-108">程式碼</span><span class="sxs-lookup"><span data-stu-id="f549a-108">Code</span></span>](#code)
- [<span data-ttu-id="f549a-109">QAT 持續性</span><span class="sxs-lookup"><span data-stu-id="f549a-109">QAT Persistence</span></span>](#qat-persistence)
- [<span data-ttu-id="f549a-110">快速存取工具列屬性</span><span class="sxs-lookup"><span data-stu-id="f549a-110">Quick Access Toolbar Properties</span></span>](#quick-access-toolbar-properties)
- [<span data-ttu-id="f549a-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="f549a-111">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="f549a-112">簡介</span><span class="sxs-lookup"><span data-stu-id="f549a-112">Introduction</span></span>

<span data-ttu-id="f549a-113">根據預設，快速存取工具列 (QAT) 位於應用程式視窗的標題列中，但可以設定為顯示在功能區下方。</span><span class="sxs-lookup"><span data-stu-id="f549a-113">By default, the Quick Access Toolbar (QAT) is located in the title bar of the application window but can be configured to display below the ribbon.</span></span> <span data-ttu-id="f549a-114">除了公開命令之外，快速存取工具列 (QAT) 也包含可自訂的下拉式功能表，其中包含一組完整的預設快速存取工具列 (QAT) 命令 (是否隱藏或顯示在快速存取工具列 (QAT) ) 和一組快速存取工具列 (QAT) 和功能區選項。</span><span class="sxs-lookup"><span data-stu-id="f549a-114">In addition to exposing Commands, the Quick Access Toolbar (QAT) also includes a customizable drop-down menu that contains the complete set of default Quick Access Toolbar (QAT) Commands (whether hidden or displayed in the Quick Access Toolbar (QAT)) and a set of Quick Access Toolbar (QAT) and ribbon options.</span></span>

<span data-ttu-id="f549a-115">下列螢幕擷取畫面顯示功能區快速存取工具列 (QAT) 的範例。</span><span class="sxs-lookup"><span data-stu-id="f549a-115">The following screen shot shows an example of the Ribbon Quick Access Toolbar (QAT).</span></span>

![microsoft 油漆功能區中 qat 的螢幕擷取畫面。](images/markup/qat-and-menu.png)

<span data-ttu-id="f549a-117">快速存取工具列 (QAT) 是由應用程式所指定的最多20個命令組合所組成 (稱為應用程式預設清單) 或由使用者選取。</span><span class="sxs-lookup"><span data-stu-id="f549a-117">The Quick Access Toolbar (QAT) consists of a combination of up to 20 Commands either specified by the application (known as the application defaults list) or selected by the user.</span></span> <span data-ttu-id="f549a-118">快速存取工具列 (QAT) 可以包含在功能區 UI 中其他位置無法使用的唯一命令。</span><span class="sxs-lookup"><span data-stu-id="f549a-118">The Quick Access Toolbar (QAT) can contain unique Commands that are not available elsewhere in the ribbon UI.</span></span>

> [!Note]
> <span data-ttu-id="f549a-119">雖然幾乎所有的功能區控制項都能將相關聯的命令新增至快速存取工具列 (QAT) 透過下列螢幕擷取畫面中所示的內容功能表，在 [內容快顯視窗](windowsribbon-controls-contextpopup.md) 中公開的命令不會提供此內容功能表。</span><span class="sxs-lookup"><span data-stu-id="f549a-119">While almost all ribbon controls allow their associated Command to be added to the Quick Access Toolbar (QAT) through the context menu shown in the following screen shot, Commands exposed in a [Context Popup](windowsribbon-controls-contextpopup.md) do not provide this context menu.</span></span>
>
> ![microsoft 油漆功能區中命令內容功能表的螢幕擷取畫面。](images/controls/qat-contextmenu-add.png) 

## <a name="implement-the-quick-access-toolbar"></a><span data-ttu-id="f549a-121">執行快速存取工具列</span><span class="sxs-lookup"><span data-stu-id="f549a-121">Implement the Quick Access Toolbar</span></span>

<span data-ttu-id="f549a-122">如同所有 Windows 功能區架構控制項，充分利用快速存取工具列 (QAT) 需要在功能區中控制其簡報的標記元件，以及控制其功能的程式碼元件。</span><span class="sxs-lookup"><span data-stu-id="f549a-122">As with all Windows Ribbon framework controls, taking full advantage of the Quick Access Toolbar (QAT) requires both a markup component that controls its presentation within the ribbon and a code component that governs its functionality.</span></span>

### <a name="markup"></a><span data-ttu-id="f549a-123">標記</span><span class="sxs-lookup"><span data-stu-id="f549a-123">Markup</span></span>

<span data-ttu-id="f549a-124">快速存取工具列 (QAT) 控制項，會透過 [QuickAccessToolbar](windowsribbon-element-quickaccesstoolbar.md) 專案在標記中宣告並與命令識別碼產生關聯。</span><span class="sxs-lookup"><span data-stu-id="f549a-124">The Quick Access Toolbar (QAT) control is declared, and associated with a Command ID, in markup through the [QuickAccessToolbar](windowsribbon-element-quickaccesstoolbar.md) element.</span></span> <span data-ttu-id="f549a-125">命令識別碼可用來識別快速存取工具列 (QAT) ，並將其系結至應用程式所定義的命令處理常式。</span><span class="sxs-lookup"><span data-stu-id="f549a-125">The Command ID is used to identify and bind the Quick Access Toolbar (QAT) to a Command handler defined by the application.</span></span>

<span data-ttu-id="f549a-126">除了主要快速存取工具列的基本命令處理常式 (QAT) 功能之外，宣告選擇性的 *CustomizeCommandName* [QuickAccessToolbar](windowsribbon-element-quickaccesstoolbar.md) 元素屬性也會導致架構將 **更多命令** 專案加入至快速存取工具列的命令清單中， (QAT) 下拉式功能表，需要定義次要的命令處理常式。</span><span class="sxs-lookup"><span data-stu-id="f549a-126">In addition to the basic Command handler for primary Quick Access Toolbar (QAT) functionality, declaring the optional *CustomizeCommandName* [QuickAccessToolbar](windowsribbon-element-quickaccesstoolbar.md) element attribute causes the framework to add a **More Commands** item to the Command list of the Quick Access Toolbar (QAT) drop-down menu that requires a secondary Command handler be defined.</span></span>

<span data-ttu-id="f549a-127">為了在功能區應用程式之間保持一致性，建議 *CustomizeCommandName* 命令處理常式啟動快速存取工具列 (QAT) 自訂對話方塊。</span><span class="sxs-lookup"><span data-stu-id="f549a-127">For consistency across Ribbon applications, it is recommended that the *CustomizeCommandName* Command handler launch a Quick Access Toolbar (QAT) customization dialog.</span></span> <span data-ttu-id="f549a-128">由於功能區架構只會提供 UI 中的啟動點，因此，應用程式會在收到此命令的回呼通知時，完全負責提供自訂對話方塊的執行。</span><span class="sxs-lookup"><span data-stu-id="f549a-128">Because the Ribbon framework only provides the launching point in the UI, the application is solely responsible for providing the customization dialog implementation when the callback notification for this Command is received.</span></span>

<span data-ttu-id="f549a-129">下列螢幕擷取畫面顯示使用 [ **更多命令** ] 命令專案 (QAT) 下拉式功能表的快速存取工具列。</span><span class="sxs-lookup"><span data-stu-id="f549a-129">The following screen shot shows a Quick Access Toolbar (QAT) drop-down menu with the **More Commands** Command item.</span></span>

![qat 功能表的螢幕擷取畫面，其中包含更多命令 .。。命令專案。](images/markup/qat-customizecommandname.png)

<span data-ttu-id="f549a-131">快速存取工具列 (QAT) 的 [應用程式預設值] 清單是透過 [QuickAccessToolbar s](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md) 屬性指定，此屬性會識別建議命令的預設清單，所有這些命令都列在快速存取工具列 (QAT) 下拉式功能表中。</span><span class="sxs-lookup"><span data-stu-id="f549a-131">The application defaults list for the Quick Access Toolbar (QAT) is specified through the [QuickAccessToolbar.ApplicationDefaults](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md) property which identifies a default list of recommended Commands, all of which are listed in the Quick Access Toolbar (QAT) drop-down menu.</span></span>

<span data-ttu-id="f549a-132">若要從快速存取工具列中的 [應用程式預設值] 清單顯示命令 (QAT) ] 工具列中，每個控制項專案的 *s. IsChecked* 屬性都必須具有值 `true` 。</span><span class="sxs-lookup"><span data-stu-id="f549a-132">To display Commands from the application defaults list in the Quick Access Toolbar (QAT) toolbar, the *ApplicationDefaults.IsChecked* attribute of each control element must have a value of `true`.</span></span> <span data-ttu-id="f549a-133">上述影像顯示將這個屬性設定為 `true` [ **儲存**]、[ **復原**] 和 [ **重做** ] 命令的結果。</span><span class="sxs-lookup"><span data-stu-id="f549a-133">The preceding images show the results of setting this attribute to `true` for the **Save**, **Undo**, and **Redo** Commands.</span></span>

<span data-ttu-id="f549a-134">[QuickAccessToolbar. s](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md) 支援三種類型的功能區控制項： [按鈕](windowsribbon-controls-button.md)、 [切換按鈕](windowsribbon-controls-togglebutton.md)和 [核取方塊](windowsribbon-controls-checkbox.md)。</span><span class="sxs-lookup"><span data-stu-id="f549a-134">[QuickAccessToolbar.ApplicationDefaults](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md) supports three types of Ribbon controls: [Button](windowsribbon-controls-button.md), [Toggle Button](windowsribbon-controls-togglebutton.md), and [Check Box](windowsribbon-controls-checkbox.md).</span></span>

> [!Note]
> <span data-ttu-id="f549a-135">Windows 8 和更新版本： ([ComboBox](windowsribbon-element-combobox.md)、 [InRibbonGallery](windowsribbon-element-inribbongallery.md)、 [SplitButtonGallery](windowsribbon-element-splitbuttongallery.md)和 [DropDownGallery](windowsribbon-element-dropdowngallery.md)) 都支援所有資源庫型控制項。</span><span class="sxs-lookup"><span data-stu-id="f549a-135">Windows 8 and newer: All gallery-based controls are supported ([ComboBox](windowsribbon-element-combobox.md), [InRibbonGallery](windowsribbon-element-inribbongallery.md), [SplitButtonGallery](windowsribbon-element-splitbuttongallery.md), and [DropDownGallery](windowsribbon-element-dropdowngallery.md)).</span></span>
>
> <span data-ttu-id="f549a-136">資源庫控制項中的專案可支援在停留時醒目提示。</span><span class="sxs-lookup"><span data-stu-id="f549a-136">Items in a gallery control can support highlighting on hover.</span></span> <span data-ttu-id="f549a-137">若要支援暫止醒目提示，資源庫必須是專案庫，並使用[VerticalMenuLayout](windowsribbon-element-verticalmenulayout.md)類型的[FlowMenuLayout](windowsribbon-element-flowmenulayout.md) 。</span><span class="sxs-lookup"><span data-stu-id="f549a-137">To support hover highlighting, the gallery must be an items gallery and use a [FlowMenuLayout](windowsribbon-element-flowmenulayout.md) of type [VerticalMenuLayout](windowsribbon-element-verticalmenulayout.md).</span></span>

<span data-ttu-id="f549a-138">下列範例示範 [QuickAccessToolbar](windowsribbon-element-quickaccesstoolbar.md) 元素的基本標記。</span><span class="sxs-lookup"><span data-stu-id="f549a-138">The following example demonstrates the basic markup for a [QuickAccessToolbar](windowsribbon-element-quickaccesstoolbar.md) element.</span></span>

<span data-ttu-id="f549a-139">這一節的程式碼顯示 [快速存取工具列 (QAT) ](windowsribbon-element-quickaccesstoolbar.md) 專案的命令宣告。</span><span class="sxs-lookup"><span data-stu-id="f549a-139">This section of code shows the Command declarations for a [Quick Access Toolbar (QAT)](windowsribbon-element-quickaccesstoolbar.md) element.</span></span>

```XML
<Command Name="cmdQAT"
         Symbol="ID_QAT"
         Id="40000"/>
<Command Name="cmdCustomizeQAT"
         Symbol="ID_CUSTOM_QAT"
         Id="40001"/>
```

<span data-ttu-id="f549a-140">這一節的程式碼顯示 [快速存取工具列 (QAT) ](windowsribbon-element-quickaccesstoolbar.md) 專案的控制項宣告。</span><span class="sxs-lookup"><span data-stu-id="f549a-140">This section of code shows the control declarations for a [Quick Access Toolbar (QAT)](windowsribbon-element-quickaccesstoolbar.md) element.</span></span>

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

### <a name="code"></a><span data-ttu-id="f549a-141">程式碼</span><span class="sxs-lookup"><span data-stu-id="f549a-141">Code</span></span>

<span data-ttu-id="f549a-142">功能區架構應用程式必須提供命令處理常式回呼方法，以操作快速存取工具列 (QAT) 。</span><span class="sxs-lookup"><span data-stu-id="f549a-142">The Ribbon framework application must provide a Command handler callback method to manipulate the Quick Access Toolbar (QAT).</span></span> <span data-ttu-id="f549a-143">此處理程式的運作方式類似于命令資源庫處理常式，不同之處在于快速存取工具列 (QAT) 不支援類別。</span><span class="sxs-lookup"><span data-stu-id="f549a-143">This handler works in a similar fashion to Command gallery handlers, except that the Quick Access Toolbar (QAT) does not support categories.</span></span> <span data-ttu-id="f549a-144">如需詳細資訊，請參閱 [使用資源庫](ribbon-controls-galleries.md)。</span><span class="sxs-lookup"><span data-stu-id="f549a-144">For more information, see [Working with Galleries](ribbon-controls-galleries.md).</span></span>

<span data-ttu-id="f549a-145">快速存取工具列 (QAT) 命令集合會透過[UI \_ PKEY \_ ItemsSource](windowsribbon-reference-properties-uipkey-itemssource.md)屬性索引鍵抓取為[IUICollection](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection)物件。</span><span class="sxs-lookup"><span data-stu-id="f549a-145">The Quick Access Toolbar (QAT) Command collection is retrieved as an [IUICollection](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) object through the [UI\_PKEY\_ItemsSource](windowsribbon-reference-properties-uipkey-itemssource.md) property key.</span></span> <span data-ttu-id="f549a-146">將命令新增至快速存取工具列 (在執行時間) QAT，可透過將 [IUISimplePropertySet](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) 物件新增至 **IUICollection** 來完成。</span><span class="sxs-lookup"><span data-stu-id="f549a-146">Adding Commands to the Quick Access Toolbar (QAT) at run time is accomplished by adding an [IUISimplePropertySet](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) object to the **IUICollection**.</span></span>

<span data-ttu-id="f549a-147">與命令庫不同的是，快速存取工具列 (QAT) [IUISimplePropertySet](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset)物件不需要命令類型屬性 ([UI \_ PKEY \_ CommandType](windowsribbon-reference-properties-uipkey-commandtype.md)) 。</span><span class="sxs-lookup"><span data-stu-id="f549a-147">Unlike Command galleries, a command type property ([UI\_PKEY\_CommandType](windowsribbon-reference-properties-uipkey-commandtype.md)) is not required for the Quick Access Toolbar (QAT) [IUISimplePropertySet](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) object.</span></span> <span data-ttu-id="f549a-148">不過，此命令必須存在於功能區或快速存取工具列 (QAT) 應用程式預設值清單;您無法在執行時間建立新的命令，並將其新增至快速存取工具列 (QAT) 。</span><span class="sxs-lookup"><span data-stu-id="f549a-148">However, the Command must exist in the ribbon or Quick Access Toolbar (QAT) application defaults list; a new Command cannot be created at run time and added to the Quick Access Toolbar (QAT).</span></span>

> [!Note]  
> <span data-ttu-id="f549a-149">功能區應用程式無法以衍生自 IEnumUnknown 的自訂集合物件來取代快速存取工具列 (QAT) [IUICollection](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) 。</span><span class="sxs-lookup"><span data-stu-id="f549a-149">The Ribbon application cannot replace the Quick Access Toolbar (QAT) [IUICollection](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) with a custom collection object derived from IEnumUnknown.</span></span>

<span data-ttu-id="f549a-150">下列範例示範基本的快速存取工具列 (QAT) 命令處理常式的執行。</span><span class="sxs-lookup"><span data-stu-id="f549a-150">The following example demonstrates a basic Quick Access Toolbar (QAT) Command handler implementation.</span></span>

```C++
/* QAT COMMAND HANDLER IMPLEMENTATION */
class CQATCommandHandler
      : public CComObjectRootEx<CComMultiThreadModel>
      , public IUICommandHandler
{
  public:
    BEGIN_COM_MAP(CQATCommandHandler)
      COM_INTERFACE_ENTRY(IUICommandHandler)
    END_COM_MAP()

    // QAT command handler's Execute method
    STDMETHODIMP Execute(UINT nCmdID,
                         UI_EXECUTIONVERB verb, 
                         const PROPERTYKEY* key,
                         const PROPVARIANT* ppropvarValue,
                         IUISimplePropertySet* pCommandExecutionProperties)
    {
      UNREFERENCED_PARAMETER(nCmdID);
      UNREFERENCED_PARAMETER(verb);
      UNREFERENCED_PARAMETER(ppropvarValue);
      UNREFERENCED_PARAMETER(pCommandExecutionProperties);

      // Do not expect Execute callback for a QAT command
      return E_NOTIMPL;
    }

    // QAT command handler's UpdateProperty method
    STDMETHODIMP UpdateProperty(UINT nCmdID,
                                REFPROPERTYKEY key,
                                const PROPVARIANT* ppropvarCurrentValue,
                                PROPVARIANT* ppropvarNewValue)
    {
      UNREFERENCED_PARAMETER(nCmdID);
      UNREFERENCED_PARAMETER(ppropvarNewValue);

      HRESULT hr = E_NOTIMPL;

      if (key == UI_PKEY_ItemsSource)
      {
        ATLASSERT(ppropvarCurrentValue->vt == VT_UNKNOWN);

        CComQIPtr<IUICollection> spCollection(ppropvarCurrentValue->punkVal);

        UINT nCount;
        if (SUCCEEDED(hr = spCollection->GetCount(&nCount)))
        {
          if (nCount == 0)
          {
            // If the current Qat list is empty, then we will add a few items here.
            UINT commands[] =  { cmdSave, cmdUndo};

            int count = _countof(commands);

            for (int i = 0; i < count; i++)
            {
              PROPERTYKEY keys[1] = {UI_PKEY_CommandId};
              CComObject<CItemProperties> *pItem = NULL;
              if (SUCCEEDED(CComObject<CItemProperties>::CreateInstance(&pItem)))
              {
                PROPVARIANT vars[1];

                InitPropVariantFromUInt32(commands[i], &vars[0]);

                pItem->Initialize(NULL, _countof(vars), keys, vars);

                CComPtr<IUnknown> spUnknown;
                pItem->QueryInterface(&spUnknown);
                spCollection->Add(spUnknown);
                            
                FreePropVariantArray(_countof(vars), vars);
              }
            }
          }
          else
          {
            // Do nothing if the Qat list is not empty.
            // Return S_FALSE to indicate the callback succeeded.
            return S_FALSE; 
          }
        }
      }
    return hr;
  }
};
```

## <a name="qat-persistence"></a><span data-ttu-id="f549a-151">QAT 持續性</span><span class="sxs-lookup"><span data-stu-id="f549a-151">QAT Persistence</span></span>

<span data-ttu-id="f549a-152">您可以使用 [IUIRibbon：： SaveSettingsToStream](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) 和 [IUIRibbon：： LoadSettingsFromStream](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) 函式，在應用程式會話之間保存快速存取工具列 (QAT) 命令專案和設定。</span><span class="sxs-lookup"><span data-stu-id="f549a-152">Quick Access Toolbar (QAT) Command items and settings can be persisted across application sessions using the [IUIRibbon::SaveSettingsToStream](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) and [IUIRibbon::LoadSettingsFromStream](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) functions.</span></span> <span data-ttu-id="f549a-153">如需詳細資訊，請參閱 [保存功能區狀態](ribbon-statepersistence.md)。</span><span class="sxs-lookup"><span data-stu-id="f549a-153">For more information, see [Persisting Ribbon State](ribbon-statepersistence.md).</span></span>

## <a name="quick-access-toolbar-properties"></a><span data-ttu-id="f549a-154">快速存取工具列屬性</span><span class="sxs-lookup"><span data-stu-id="f549a-154">Quick Access Toolbar Properties</span></span>

<span data-ttu-id="f549a-155">功能區架構會定義快速存取工具列 (QAT) 控制項的 [屬性索引鍵](windowsribbon-reference-properties.md) 集合。</span><span class="sxs-lookup"><span data-stu-id="f549a-155">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Quick Access Toolbar (QAT) control.</span></span>

<span data-ttu-id="f549a-156">一般而言，快速存取工具列 (QAT) 屬性會在功能區 UI 中更新，方法是透過呼叫 [IUIFramework：： InvalidateUICommand](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) 方法來使與控制項相關聯的命令失效。</span><span class="sxs-lookup"><span data-stu-id="f549a-156">Typically, a Quick Access Toolbar (QAT) property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [IUIFramework::InvalidateUICommand](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="f549a-157">[IUICommandHandler：： UpdateProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)回呼方法會處理失效事件，並定義屬性更新。</span><span class="sxs-lookup"><span data-stu-id="f549a-157">The invalidation event is handled, and the property updates defined, by the [IUICommandHandler::UpdateProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="f549a-158">[IUICommandHandler：： UpdateProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)回呼方法未執行，而且應用程式會查詢已更新的屬性值，直到架構需要該屬性為止。</span><span class="sxs-lookup"><span data-stu-id="f549a-158">The [IUICommandHandler::UpdateProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="f549a-159">例如，啟用索引標籤時，以及在功能區 UI 中顯示控制項，或顯示工具提示時。</span><span class="sxs-lookup"><span data-stu-id="f549a-159">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="f549a-160">在某些情況下，可以透過 [IUIFramework：： GetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) 方法抓取屬性，並使用 [IUIFramework：： SetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) 方法進行設定。</span><span class="sxs-lookup"><span data-stu-id="f549a-160">In some cases, a property can be retrieved through the [IUIFramework::GetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [IUIFramework::SetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

<span data-ttu-id="f549a-161">下表列出與快速存取工具列 (QAT) 控制項相關聯的屬性索引鍵。</span><span class="sxs-lookup"><span data-stu-id="f549a-161">The following table lists the property keys that are associated with the Quick Access Toolbar (QAT) control.</span></span>

| <span data-ttu-id="f549a-162">屬性索引鍵</span><span class="sxs-lookup"><span data-stu-id="f549a-162">Property Key</span></span> | <span data-ttu-id="f549a-163">備註</span><span class="sxs-lookup"><span data-stu-id="f549a-163">Notes</span></span> |
|---|---|
| [<span data-ttu-id="f549a-164">UI \_ PKEY \_ ItemsSource</span><span class="sxs-lookup"><span data-stu-id="f549a-164">UI\_PKEY\_ItemsSource</span></span>](windowsribbon-reference-properties-uipkey-itemssource.md) | <span data-ttu-id="f549a-165">支援 [IUIFramework：： GetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) (不支援 [IUIFramework：： SetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty)) 。[IUIFramework：： GetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) 會傳回 IUICollection 物件的指標，該物件代表 QAT 中的命令。</span><span class="sxs-lookup"><span data-stu-id="f549a-165">Supports [IUIFramework::GetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) (does not support [IUIFramework::SetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty)).[IUIFramework::GetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) returns a pointer to an IUICollection object that represents the commands in the QAT.</span></span> <span data-ttu-id="f549a-166">每個命令都是藉由呼叫 [IUISimplePropertySet：： GetValue](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) 方法來識別，並在屬性索引鍵 [UI \_ PKEY \_ CommandId](windowsribbon-reference-properties-uipkey-commandid.md)中傳遞，藉以取得命令識別碼。</span><span class="sxs-lookup"><span data-stu-id="f549a-166">Each Command is identified by its Command ID, which is obtained by calling the [IUISimplePropertySet::GetValue](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) method and passing in the property key [UI\_PKEY\_CommandId](windowsribbon-reference-properties-uipkey-commandid.md).</span></span> |

<span data-ttu-id="f549a-167">快速存取工具列的 [ **其他命令** ] 命令專案沒有相關聯的屬性索引鍵 (QAT) 下拉式功能表</span><span class="sxs-lookup"><span data-stu-id="f549a-167">There are no property keys associated with the **More Commands** Command item of the Quick Access Toolbar (QAT) drop-down menu</span></span>

## <a name="related-topics"></a><span data-ttu-id="f549a-168">相關主題</span><span class="sxs-lookup"><span data-stu-id="f549a-168">Related topics</span></span>

- [<span data-ttu-id="f549a-169">Windows 功能區架構控制項程式庫</span><span class="sxs-lookup"><span data-stu-id="f549a-169">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
- [<span data-ttu-id="f549a-170">QuickAccessToolbar 標記元素</span><span class="sxs-lookup"><span data-stu-id="f549a-170">QuickAccessToolbar markup element</span></span>](windowsribbon-element-quickaccesstoolbar.md)
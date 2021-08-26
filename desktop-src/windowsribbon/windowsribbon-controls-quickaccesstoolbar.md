---
title: 快速存取工具列
description: 快速存取工具列 (QAT) 是一個小型、可自訂的工具列，它會公開應用程式所指定的一組命令，或是由使用者選取的命令。
ms.assetid: b2adf4e9-0de1-4c4d-9293-693d0f7cf6fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d63eb3f7b1a2c1213430f86a9a12fe4517c738290ed736eb1d356420aa145cd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110721"
---
# <a name="quick-access-toolbar"></a>快速存取工具列

快速存取工具列 (QAT) 是一個小型、可自訂的工具列，它會公開應用程式所指定的一組命令，或是由使用者選取的命令。

- [簡介](#introduction)
- [執行快速存取工具列](#implement-the-quick-access-toolbar)
  - [標記](#markup)
  - [程式碼](#code)
- [QAT 持續性](#qat-persistence)
- [快速存取工具列屬性](#quick-access-toolbar-properties)
- [相關主題](#related-topics)

## <a name="introduction"></a>簡介

根據預設，快速存取工具列 (QAT) 位於應用程式視窗的標題列中，但可以設定為顯示在功能區下方。 除了公開命令之外，快速存取工具列 (QAT) 也包含可自訂的下拉式功能表，其中包含一組完整的預設快速存取工具列 (QAT) 命令 (是否隱藏或顯示在快速存取工具列 (QAT) ) 和一組快速存取工具列 (QAT) 和功能區選項。

下列螢幕擷取畫面顯示功能區快速存取工具列 (QAT) 的範例。

![microsoft 油漆功能區中 qat 的螢幕擷取畫面。](images/markup/qat-and-menu.png)

快速存取工具列 (QAT) 是由應用程式所指定的最多20個命令組合所組成 (稱為應用程式預設清單) 或由使用者選取。 快速存取工具列 (QAT) 可以包含在功能區 UI 中其他位置無法使用的唯一命令。

> [!Note]
> 雖然幾乎所有的功能區控制項都能將相關聯的命令新增至快速存取工具列 (QAT) 透過下列螢幕擷取畫面中所示的內容功能表，在 [內容快顯視窗](windowsribbon-controls-contextpopup.md) 中公開的命令不會提供此內容功能表。
>
> ![microsoft 油漆功能區中命令內容功能表的螢幕擷取畫面。](images/controls/qat-contextmenu-add.png) 

## <a name="implement-the-quick-access-toolbar"></a>執行快速存取工具列

如同所有 Windows 功能區 framework 控制項，充分利用快速存取工具列 (QAT) 同時需要在功能區中控制其簡報的標記元件，以及控制其功能的程式碼元件。

### <a name="markup"></a>標記

快速存取工具列 (QAT) 控制項，會透過 [QuickAccessToolbar](windowsribbon-element-quickaccesstoolbar.md) 專案在標記中宣告並與命令識別碼產生關聯。 命令識別碼可用來識別快速存取工具列 (QAT) ，並將其系結至應用程式所定義的命令處理常式。

除了主要快速存取工具列的基本命令處理常式 (QAT) 功能之外，宣告選擇性的 *CustomizeCommandName* [QuickAccessToolbar](windowsribbon-element-quickaccesstoolbar.md) 元素屬性也會導致架構將 **更多命令** 專案加入至快速存取工具列的命令清單中， (QAT) 下拉式功能表，需要定義次要的命令處理常式。

為了在功能區應用程式之間保持一致性，建議 *CustomizeCommandName* 命令處理常式啟動快速存取工具列 (QAT) 自訂對話方塊。 由於功能區架構只會提供 UI 中的啟動點，因此，應用程式會在收到此命令的回呼通知時，完全負責提供自訂對話方塊的執行。

下列螢幕擷取畫面顯示使用 [ **更多命令** ] 命令專案 (QAT) 下拉式功能表的快速存取工具列。

![qat 功能表的螢幕擷取畫面，其中包含更多命令 .。。命令專案。](images/markup/qat-customizecommandname.png)

快速存取工具列 (QAT) 的 [應用程式預設值] 清單是透過 [QuickAccessToolbar s](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md) 屬性指定，此屬性會識別建議命令的預設清單，所有這些命令都列在快速存取工具列 (QAT) 下拉式功能表中。

若要從快速存取工具列中的 [應用程式預設值] 清單顯示命令 (QAT) ] 工具列中，每個控制項專案的 *s. IsChecked* 屬性都必須具有值 `true` 。 上述影像顯示將這個屬性設定為 `true` [ **儲存**]、[ **復原**] 和 [ **重做** ] 命令的結果。

[QuickAccessToolbar. s](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md) 支援三種類型的功能區控制項： [按鈕](windowsribbon-controls-button.md)、 [切換按鈕](windowsribbon-controls-togglebutton.md)和 [核取方塊](windowsribbon-controls-checkbox.md)。

> [!Note]
> Windows 8 和更新版本： ([ComboBox](windowsribbon-element-combobox.md)、 [InRibbonGallery](windowsribbon-element-inribbongallery.md)、 [SplitButtonGallery](windowsribbon-element-splitbuttongallery.md)和[DropDownGallery](windowsribbon-element-dropdowngallery.md)) 都支援所有資源庫型控制項。
>
> 資源庫控制項中的專案可支援在停留時醒目提示。 若要支援暫止醒目提示，資源庫必須是專案庫，並使用[VerticalMenuLayout](windowsribbon-element-verticalmenulayout.md)類型的[FlowMenuLayout](windowsribbon-element-flowmenulayout.md) 。

下列範例示範 [QuickAccessToolbar](windowsribbon-element-quickaccesstoolbar.md) 元素的基本標記。

這一節的程式碼顯示 [快速存取工具列 (QAT) ](windowsribbon-element-quickaccesstoolbar.md) 專案的命令宣告。

```XML
<Command Name="cmdQAT"
         Symbol="ID_QAT"
         Id="40000"/>
<Command Name="cmdCustomizeQAT"
         Symbol="ID_CUSTOM_QAT"
         Id="40001"/>
```

這一節的程式碼顯示 [快速存取工具列 (QAT) ](windowsribbon-element-quickaccesstoolbar.md) 專案的控制項宣告。

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

### <a name="code"></a>程式碼

功能區架構應用程式必須提供命令處理常式回呼方法，以操作快速存取工具列 (QAT) 。 此處理程式的運作方式類似于命令資源庫處理常式，不同之處在于快速存取工具列 (QAT) 不支援類別。 如需詳細資訊，請參閱 [使用資源庫](ribbon-controls-galleries.md)。

快速存取工具列 (QAT) 命令集合會透過[UI \_ PKEY \_ ItemsSource](windowsribbon-reference-properties-uipkey-itemssource.md)屬性索引鍵抓取為[IUICollection](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection)物件。 將命令新增至快速存取工具列 (在執行時間) QAT，可透過將 [IUISimplePropertySet](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) 物件新增至 **IUICollection** 來完成。

與命令庫不同的是，快速存取工具列 (QAT) [IUISimplePropertySet](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset)物件不需要命令類型屬性 ([UI \_ PKEY \_ CommandType](windowsribbon-reference-properties-uipkey-commandtype.md)) 。 不過，此命令必須存在於功能區或快速存取工具列 (QAT) 應用程式預設值清單;您無法在執行時間建立新的命令，並將其新增至快速存取工具列 (QAT) 。

> [!Note]  
> 功能區應用程式無法以衍生自 IEnumUnknown 的自訂集合物件來取代快速存取工具列 (QAT) [IUICollection](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) 。

下列範例示範基本的快速存取工具列 (QAT) 命令處理常式的執行。

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

## <a name="qat-persistence"></a>QAT 持續性

您可以使用 [IUIRibbon：： SaveSettingsToStream](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) 和 [IUIRibbon：： LoadSettingsFromStream](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) 函式，在應用程式會話之間保存快速存取工具列 (QAT) 命令專案和設定。 如需詳細資訊，請參閱 [保存功能區狀態](ribbon-statepersistence.md)。

## <a name="quick-access-toolbar-properties"></a>快速存取工具列屬性

功能區架構會定義快速存取工具列 (QAT) 控制項的 [屬性索引鍵](windowsribbon-reference-properties.md) 集合。

一般而言，快速存取工具列 (QAT) 屬性會在功能區 UI 中更新，方法是透過呼叫 [IUIFramework：： InvalidateUICommand](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) 方法來使與控制項相關聯的命令失效。 [IUICommandHandler：： UpdateProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)回呼方法會處理失效事件，並定義屬性更新。

[IUICommandHandler：： UpdateProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)回呼方法未執行，而且應用程式會查詢已更新的屬性值，直到架構需要該屬性為止。 例如，啟用索引標籤時，以及在功能區 UI 中顯示控制項，或顯示工具提示時。

> [!Note]  
> 在某些情況下，可以透過 [IUIFramework：： GetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) 方法抓取屬性，並使用 [IUIFramework：： SetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) 方法進行設定。

下表列出與快速存取工具列 (QAT) 控制項相關聯的屬性索引鍵。

| 屬性索引鍵 | 備註 |
|---|---|
| [UI \_ PKEY \_ ItemsSource](windowsribbon-reference-properties-uipkey-itemssource.md) | 支援 [IUIFramework：： GetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) (不支援 [IUIFramework：： SetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty)) 。[IUIFramework：： GetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) 會傳回 IUICollection 物件的指標，該物件代表 QAT 中的命令。 每個命令都是藉由呼叫 [IUISimplePropertySet：： GetValue](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) 方法來識別，並在屬性索引鍵 [UI \_ PKEY \_ CommandId](windowsribbon-reference-properties-uipkey-commandid.md)中傳遞，藉以取得命令識別碼。 |

快速存取工具列的 [ **其他命令** ] 命令專案沒有相關聯的屬性索引鍵 (QAT) 下拉式功能表

## <a name="related-topics"></a>相關主題

- [Windows功能區架構控制項程式庫](windowsribbon-controls-entry.md)
- [QuickAccessToolbar 標記元素](windowsribbon-element-quickaccesstoolbar.md)
---
title: 使用資源庫
description: Windows 功能區架構為開發人員提供健全且一致的模型，以管理各種集合型控制項的動態內容。
ms.assetid: 447039f3-1428-4b6f-94cf-78cf81974041
keywords:
- Windows 功能區，資源庫
- 功能區，資源庫
- Windows 功能區，DropDownGallery 控制項
- 功能區，DropDownGallery 控制項
- Windows 功能區，SplitButtonGallery 控制項
- 功能區，SplitButtonGallery 控制項
- DropDownGallery 控制項
- SplitButtonGallery 控制項
- Windows 功能區的資源庫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 784c69b0cf23edad906fbb35ee9a2a45454eacea
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682840"
---
# <a name="working-with-galleries"></a>使用資源庫

Windows 功能區架構為開發人員提供健全且一致的模型，以管理各種集合型控制項的動態內容。 藉由調整並重新設定功能區 UI，這些動態控制項可讓架構在主應用程式和功能區本身中回應使用者互動，並提供彈性來處理各種執行時間環境。

-   [簡介](#introduction)
-   [畫廊](#working-with-galleries)
    -   [專案資源庫](#item-galleries)
    -   [命令資源庫](#command-galleries)
    -   [圖庫控制項](#working-with-galleries)
-   [如何執行資源庫](#how-to-implement-a-gallery)
    -   [基本元件](#the-basic-components)
    -   [在標記中宣告控制項](#declare-the-controls-in-markup)
    -   [建立命令處理常式](#create-a-command-handler)
    -   [系結命令處理常式](#bind-the-command-handler)
    -   [初始化集合](#initialize-a-collection)
    -   [處理收集事件](#handle-collection-events)
-   [相關主題](#related-topics)

## <a name="introduction"></a>簡介

功能區架構可動態適應執行時間條件、應用程式需求和使用者輸入的這項功能，強調架構的豐富 UI 功能，並為開發人員提供彈性來滿足廣泛的客戶需求。

本指南的重點在於描述架構所支援的動態資源庫控制項、說明其差異、討論其最適合的使用時間和位置，並示範如何將這些控制項併入功能區應用程式。

## <a name="galleries"></a>資源庫

資源庫是功能強大的清單方塊控制項。 資源庫的專案集合可以依分類來組織，這些類別會顯示在彈性資料行和資料列型配置中（以影像和文字表示），並視資源庫類型而定，支援即時預覽。

資源庫與其他動態功能區控制項的功能不同，原因如下：

-   資源庫會執行 [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) 介面，以定義各種操作主機庫專案集合的方法。
-   您可以在執行時間根據直接出現在功能區中的活動更新資源庫，例如，當使用者將命令新增至快速存取工具列時 (QAT) 。
-   您可以在執行時間根據在執行時間環境中間接發生的活動來更新資源庫，例如，當印表機驅動程式僅支援直向頁面配置時。
-   您可以在執行時間根據在主應用程式中間接發生的活動（例如，當使用者在檔中選取專案時）來更新資源庫。

功能區架構會公開兩種類型的資源庫：專案資源庫和命令資源庫。

### <a name="item-galleries"></a>專案資源庫

專案圖庫包含以索引為基礎的相關專案集合，其中每個專案都以影像、字串或兩者表示。 控制項系結至單一命令處理常式，該處理常式依賴 [UI \_ PKEY \_ SelectedItem](windowsribbon-reference-properties-uipkey-selecteditem.md) 屬性所識別的索引值。

專案圖庫支援即時預覽，這表示會根據滑鼠停駐或焦點顯示命令結果，而不需要認可或實際叫用命令。

> [!IMPORTANT]
> 此架構不支援在 [應用程式] 功能表中裝載專案資源庫。

 

### <a name="command-galleries"></a>命令資源庫

命令資源庫包含相異、非索引項目目的集合。 每個專案都是以透過命令識別碼系結至命令處理常式的單一控制項來表示。 就像獨立控制項一樣，命令資源庫中的每個專案都會將輸入事件路由傳送至相關聯的命令處理常式，而命令資源庫本身不會接聽事件。

命令資源庫不支援即時預覽。

### <a name="gallery-controls"></a>圖庫控制項

功能區架構中有四個資源庫控制項： [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)、 [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)、 [**InRibbonGallery**](windowsribbon-element-inribbongallery.md)和 [**ComboBox**](windowsribbon-element-combobox.md)。 **ComboBox** 以外的所有專案都可以實作為專案資源庫或命令資源庫。

### <a name="dropdowngallery"></a>DropDownGallery

[**DropDownGallery**](windowsribbon-element-dropdowngallery.md)是一個按鈕，顯示包含互斥專案或命令集合的下拉式清單。

下列螢幕擷取畫面說明 Windows 7 Microsoft 小畫家中的功能區 [下拉式圖庫](windowsribbon-controls-dropdowngallery.md) 控制項。

![適用于 windows 7 的 microsoft 油漆中，下拉式圖庫控制項的螢幕擷取畫面。](images/controls/dropdowngallery.png)

### <a name="splitbuttongallery"></a>SplitButtonGallery

[**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)是複合控制項，會在主要按鈕上從其集合公開單一預設專案或命令，並在按一下次要按鈕時顯示的互斥下拉式清單中顯示其他專案或命令。

下列螢幕擷取畫面說明 Windows 7 Microsoft 小畫家中的功能區 [分割按鈕資源庫](windowsribbon-controls-splitbuttongallery.md) 控制項。

![適用于 windows 7 的 microsoft 油漆中分割按鈕圖庫控制項的螢幕擷取畫面。](images/controls/splitbuttongallery.png)

### <a name="inribbongallery"></a>InRibbonGallery

[**InRibbonGallery**](windowsribbon-element-inribbongallery.md)是一個資源庫，可在功能區中顯示相關專案或命令的集合。 如果資源庫中有太多專案，則會提供展開箭號，以在展開的窗格中顯示集合的其餘部分。

下列螢幕擷取畫面說明 Windows 7 Microsoft 小畫家中功能區元件 [庫](windowsribbon-controls-inribbongallery.md) 控制項的功能區。

![microsoft 油漆功能區中功能區資源庫控制項的螢幕擷取畫面。](images/controls/inribbongallery.png)

### <a name="combobox"></a>ComboBox

[**ComboBox**](windowsribbon-element-combobox.md)是單一資料行清單方塊，其中包含具有靜態控制項或編輯控制項和下拉式箭號的專案集合。 當使用者按一下下拉式箭號時，就會顯示控制項的清單方塊部分。

下列螢幕擷取畫面說明 Windows Live Movie Maker 的功能區 [下拉式列示方塊](windowsribbon-controls-combobox.md) 控制項。

![microsoft 油漆功能區中 combobox 控制項的螢幕擷取畫面。](images/controls/combobox.png)

因為 [**ComboBox**](windowsribbon-element-combobox.md) 只是一個專案資源庫，所以不支援命令專案。 它也是唯一不支援命令空間的資源庫控制項。  (命令空間是在標記中宣告的命令集合，並列在專案庫或命令資源庫底部。 ) 

下列程式碼範例顯示在 [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)中宣告三個按鈕命令空間所需的標記。


```C++
<DropDownGallery 
  CommandName="cmdSizeAndColor" 
  TextPosition="Hide" 
  Type="Commands"
  ItemHeight="32"
  ItemWidth="32">
  <DropDownGallery.MenuLayout>
    <FlowMenuLayout Rows="2" Columns="3" Gripper="None"/>
  </DropDownGallery.MenuLayout>
  <Button CommandName="cmdCommandSpace1"/>
  <Button CommandName="cmdCommandSpace2"/>
  <Button CommandName="cmdCommandSpace3"/>
</DropDownGallery>
```



下列螢幕擷取畫面說明上述程式碼範例的三個按鈕命令空間。

![dropdowngallery 中三個按鈕命令空間的螢幕擷取畫面。](images/markup/gallerysample-commandspace.png)

## <a name="how-to-implement-a-gallery"></a>如何執行資源庫

本節將討論功能區元件庫的執行詳細資料，並逐步解說如何將它們併入功能區應用程式中。

### <a name="the-basic-components"></a>基本元件

本節說明在功能區架構中形成動態內容骨幹的一組屬性和方法，並支援在執行時間新增、刪除、更新和操作功能區圖庫的內容和視覺化配置。

### <a name="iuicollection"></a>IUICollection

資源庫需要一組基本的方法來存取和操作其集合中的個別專案。

[IEnumUnknown](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown)介面會定義這些方法，而架構會以 [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection)介面中所定義的其他方法來補充其功能。 **IUICollection** 是由功能區標記中每個資源庫宣告的架構所執行。

如果 [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) 介面未提供其他需要的功能，則由主應用程式所執行且衍生自 [IEnumUnknown](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown) 的自訂集合物件可以取代為架構集合。

### <a name="iuicollectionchangedevent"></a>IUICollectionChangedEvent

若要讓應用程式回應資源庫集合中的變更，則必須執行 [**IUICollectionChangedEvent**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollectionchangedevent) 介面。 應用程式可以透過 [**IUICollectionChangedEvent：： OnChanged**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicollectionchangedevent-onchanged)事件接聽程式，訂閱來自 [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection)物件的通知。

當應用程式將架構所提供的資源庫集合取代為自訂集合時，應用程式應該會執行 [IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) 介面。 如果未執行 [IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) ，則應用程式無法在需要動態更新資源庫控制項的自訂集合中通知架構變更。

在未執行 [IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) 的情況下，資源庫控制項只能透過 [**IUIFramework：： InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) 和 [**IUICommandHandler：： UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)的失效，或藉由呼叫 [**IUIFramework：： SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty)來更新。

### <a name="iuisimplepropertyset"></a>IUISimplePropertySet

應用程式必須針對資源庫集合中的每個專案或命令執行 IUISimplePropertySet。 但是，可使用 [**IUISimplePropertySet：： GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) 要求的屬性會有所不同。

專案會透過 [UI \_ PKEY \_ ItemsSource](windowsribbon-reference-properties-uipkey-itemssource.md) 屬性索引鍵來定義並系結至資源庫，並使用 [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) 物件來公開屬性。

下表描述專案圖庫中專案 ([**UI \_ COMMANDTYPE \_ 集合**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype)) 的有效屬性。

> [!Note]  
> 某些專案屬性（例如 [UI \_ PKEY \_ 標籤](windowsribbon-reference-properties-uipkey-label.md)）可以在標記中定義。 如需詳細資訊，請參閱 [屬性索引鍵](windowsribbon-reference-properties.md) 參考檔。

 



控制

屬性

[**ComboBox**](windowsribbon-element-combobox.md)

[UI \_PKEY \_ 標籤](windowsribbon-reference-properties-uipkey-label.md)， [UI \_ PKEY \_ 類別](windowsribbon-reference-properties-uipkey-categoryid.md)

[**DropDownGallery**](windowsribbon-element-dropdowngallery.md)

[UI \_PKEY \_ 標籤](windowsribbon-reference-properties-uipkey-label.md)、 [ui \_ PKEY \_ ItemImage](windowsribbon-reference-properties-uipkey-itemimage.md) 、 [ui \_ PKEY \_ 類別](windowsribbon-reference-properties-uipkey-categoryid.md)

[**InRibbonGallery**](windowsribbon-element-inribbongallery.md)

[UI \_PKEY \_ 標籤](windowsribbon-reference-properties-uipkey-label.md)、 [ui \_ PKEY \_ ItemImage](windowsribbon-reference-properties-uipkey-itemimage.md) 、 [ui \_ PKEY \_ 類別](windowsribbon-reference-properties-uipkey-categoryid.md)

[**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)

[UI \_PKEY \_ 標籤](windowsribbon-reference-properties-uipkey-label.md)、 [ui \_ PKEY \_ ItemImage](windowsribbon-reference-properties-uipkey-itemimage.md)、 [ui \_ PKEY \_ 類別](windowsribbon-reference-properties-uipkey-categoryid.md)

[UI \_PKEY \_ SelectedItem](windowsribbon-reference-properties-uipkey-selecteditem.md) 是專案資源庫的屬性。



 

下表說明命令資源庫 ([**UI \_ COMMANDTYPE \_ COMMANDCOLLECTION**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype)) 的有效專案屬性。



| 控制                                                                | 屬性                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)       | [UI \_PKEY \_ CommandId](windowsribbon-reference-properties-uipkey-commandid.md)、 [ui \_ PKEY \_ CommandType](windowsribbon-reference-properties-uipkey-commandtype.md) 、 [ui \_ PKEY \_ 類別](windowsribbon-reference-properties-uipkey-categoryid.md) |
| [**InRibbonGallery**](windowsribbon-element-inribbongallery.md)       | [UI \_PKEY \_ CommandId](windowsribbon-reference-properties-uipkey-commandid.md)、 [ui \_ PKEY \_ CommandType](windowsribbon-reference-properties-uipkey-commandtype.md) 、 [ui \_ PKEY \_ 類別](windowsribbon-reference-properties-uipkey-categoryid.md) |
| [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) | [UI \_PKEY \_ CommandId](windowsribbon-reference-properties-uipkey-commandid.md)、 [ui \_ PKEY \_ CommandType](windowsribbon-reference-properties-uipkey-commandtype.md)、 [ui \_ PKEY \_ 類別](windowsribbon-reference-properties-uipkey-categoryid.md)  |



 

類別目錄是用來組織資源庫中的專案與命令。 類別目錄會透過 [UI \_ PKEY \_](windowsribbon-reference-properties-uipkey-categories.md) category 屬性索引鍵來定義並系結至資源庫，並以類別特定的 [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) 物件來公開屬性。

類別沒有 CommandType，且不支援使用者互動。 例如，類別目錄不能成為專案資源庫中的 SelectedItem，而且它們不會系結至命令庫中的命令。 如同其他主機庫專案屬性，可以藉由呼叫 [**IUISimplePropertySet：： GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue)來取出類別目錄屬性，例如 [UI \_ PKEY \_ 標籤](windowsribbon-reference-properties-uipkey-label.md)和 [ui \_ PKEY \_](windowsribbon-reference-properties-uipkey-categoryid.md)類別目錄。

> [!IMPORTANT]
> 當針對沒有相關聯類別的專案要求 [ui \_ PKEY \_ 類別](windowsribbon-reference-properties-uipkey-categoryid.md)目錄時， [**IUISimplePropertySet：： GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue)應該會傳回 [**ui \_ 集合 \_ INVALIDINDEX**](/windows/desktop/windowsribbon/windowsribbon-ui-collection-invalidindex) 。

 

### <a name="declare-the-controls-in-markup"></a>在標記中宣告控制項

資源庫（例如所有功能區控制項）必須在標記中宣告。 資源庫會在標記中識別為專案資源庫或命令資源庫，並宣告各種展示詳細資料。 不同于其他控制項，資源庫需要在標記中宣告基底控制項或集合容器。 實際的集合會在執行時間填入。 在標記中宣告資源庫時，會使用 *Type* 屬性來指定資源庫是否為命令資源庫的專案圖庫。

這裡討論的每個控制項都有一些選擇性的版面配置屬性可用。 這些屬性會提供開發人員喜好設定，讓架構直接影響控制項在功能區中的填入和顯示方式。 標記中適用的喜好設定，與 [透過大小定義和調整原則自訂功能區](windowsribbon-templates.md)中所討論的顯示和版面配置範本和行為有關。

如果特定控制項不允許直接在標記中使用版面配置喜好設定，或未指定配置喜好設定，則架構會根據可用的螢幕空間量來定義控制項特定的顯示慣例。

下列範例示範如何將一組資源庫納入功能區中。

### <a name="command-declarations"></a>命令聲明

命令應該以用來將控制項或控制項集合與命令相關聯的 *CommandName* 屬性來宣告。

在編譯標記時，用來將命令系結至命令處理常式的 *CommandId* 屬性也可以在這裡指定。 如果未提供任何識別碼，則架構會產生一個識別碼。


```XML
<!-- ComboBox -->
<Command Name="cmdComboBoxGroup"
         Symbol="cmdComboBoxGroup"
         Comment="ComboBox Group"
         LabelTitle="ComboBox"/>
<Command Name="cmdComboBox"
         Symbol="cmdComboBox"
         Comment="ComboBox"
         LabelTitle="ComboBox"/>
```


```XML

<!-- DropDownGallery -->
<Command Name="cmdDropDownGalleryGroup"
         Symbol="cmdDropDownGalleryGroup"
         Comment="DropDownGallery Group"
         LabelTitle="DropDownGallery"/>
<Command Name="cmdDropDownGallery"
         Symbol="cmdDropDownGallery"
         Comment="DropDownGallery"
         LabelTitle="DropDownGallery"/>
```




```XML

<!-- InRibbonGallery -->
<Command Name="cmdInRibbonGalleryGroup"
         Symbol="cmdInRibbonGalleryGroup"
         Comment="InRibbonGallery Group"
         LabelTitle="InRibbonGallery"/>
<Command Name="cmdInRibbonGallery"
         Symbol="cmdInRibbonGallery"
         Comment="InRibbonGallery"
         LabelTitle="InRibbonGallery"
```



```XML

<!-- SplitButtonGallery -->
<Command Name="cmdSplitButtonGalleryGroup"
         Symbol="cmdSplitButtonGalleryGroup"
         Comment="SplitButtonGallery Group"
         LabelTitle="SplitButtonGallery"/>
<Command Name="cmdSplitButtonGallery"
         Symbol="cmdSplitButtonGallery"
         Comment="SplitButtonGallery"
         LabelTitle="SplitButtonGallery"
```



### <a name="control-declarations"></a>控制項宣告

本章節包含的範例會示範各種資源庫類型所需的基本控制項標記。 它們示範如何宣告資源庫控制項，並透過 *CommandName* 屬性將它們與命令建立關聯。

下列範例顯示 [**DropDownGallery**](windowsribbon-element-dropdowngallery.md) 的控制項宣告，其中 *Type* 屬性用來指定這是命令資源庫。


```XML
<!-- DropDownGallery -->
<Group CommandName="cmdDropDownGalleryGroup">
  <DropDownGallery CommandName="cmdDropDownGallery"
                   TextPosition="Hide"
                   Type="Commands"
                   ItemHeight="32"
                   ItemWidth="32">
    <DropDownGallery.MenuLayout>
      <FlowMenuLayout Rows="2"
                      Columns="3"
                      Gripper="None"/>
    </DropDownGallery.MenuLayout>
    <DropDownGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
       </MenuGroup>
       <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </DropDownGallery.MenuGroups>
  </DropDownGallery>
</Group>
```



下列範例顯示 [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)的控制項宣告。


```XML
<!-- SplitButtonGallery -->
<Group CommandName="cmdSplitButtonGalleryGroup">
  <SplitButtonGallery CommandName="cmdSplitButtonGallery">
    <SplitButtonGallery.MenuLayout>
      <FlowMenuLayout Rows="2"
                      Columns="3"
                      Gripper="None"/>
    </SplitButtonGallery.MenuLayout>
    <SplitButtonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </SplitButtonGallery.MenuGroups>
  </SplitButtonGallery>
</Group>
```



下列範例顯示 [**InRibbonGallery**](windowsribbon-element-inribbongallery.md)的控制項宣告。

> [!Note]  
> 由於 [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) 的設計是要在功能區中顯示其專案集合的子集，而不啟動下拉式功能表，所以它提供了一些選擇性屬性，可在功能區初始化時管理其大小和專案版面配置。 這些屬性對 **InRibbonGallery** 而言是唯一的，而且無法從其他動態控制項使用。

 


```XML
<!-- InRibbonGallery -->
<Group CommandName="cmdInRibbonGalleryGroup" SizeDefinition="OneInRibbonGallery">
  <InRibbonGallery CommandName="cmdInRibbonGallery"
                   MaxColumns="10"
                   MaxColumnsMedium="5"
                   MinColumnsLarge="5"
                   MinColumnsMedium="3"
                   Type="Items">
    <InRibbonGallery.MenuLayout>
      <VerticalMenuLayout Rows="2"
                          Gripper="Vertical"/>
    </InRibbonGallery.MenuLayout>
    <InRibbonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </InRibbonGallery.MenuGroups>            
  </InRibbonGallery>
</Group>
```



下列範例顯示 [**ComboBox**](windowsribbon-element-combobox.md)的控制項宣告。


```XML
<!-- ComboBox -->
<Group CommandName="cmdComboBoxGroup">
  <ComboBox CommandName="cmdComboBox">              
  </ComboBox>
</Group>
```



### <a name="create-a-command-handler"></a>建立命令處理常式

針對每個命令，功能區架構都需要主應用程式中對應的命令處理常式。 命令處理常式是由功能區主機應用程式所執行，並且衍生自 [**IUICommandHandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler) 介面。

> [!Note]  
> 多個命令可以系結至單一命令處理常式。

 

命令處理常式有兩個用途：

-   [**IUICommandHandler：： UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) 會回應屬性更新要求。 您可以透過呼叫 [**IUIFramework：： SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty)或 [**IUIFramework：： InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand)，將命令屬性的值（例如 [ui \_ PKEY \_ 啟用](windowsribbon-reference-properties-uipkey-enabled.md)或 [ui \_ PKEY \_ 標籤](windowsribbon-reference-properties-uipkey-label.md)）設定為。
-   [**IUICommandHandler：： execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) 會回應 execute 事件。 這個方法支援 [**UI \_ EXECUTIONVERB**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_executionverb) 參數所指定的下列三個執行狀態。
    -   執行狀態會執行或認可至處理常式所系結的任何命令。
    -   預覽狀態會預覽處理常式所系結的任何命令。 這基本上會執行命令，而不會認可結果。
    -   CancelPreview 狀態會取消任何預覽的命令。 這是支援透過功能表或清單進行遍歷的必要步驟，並可依需要順序預覽及復原結果。

下列範例示範資源庫命令處理常式。


```C++
/*
 * GALLERY COMMAND HANDLER IMPLEMENTATION
 */
class CGalleryCommandHandler
      : public CComObjectRootEx<CComMultiThreadModel>
      , public IUICommandHandler
{
public:
  BEGIN_COM_MAP(CGalleryCommandHandler)
    COM_INTERFACE_ENTRY(IUICommandHandler)
  END_COM_MAP()

  // Gallery command handler's Execute method
  STDMETHODIMP Execute(UINT nCmdID,
                       UI_EXECUTIONVERB verb, 
                       const PROPERTYKEY* key,
                       const PROPVARIANT* ppropvarValue,
                       IUISimplePropertySet* pCommandExecutionProperties)
  {
    HRESULT hr = S_OK;
        
    // Switch on manner of execution (Execute/Preview/CancelPreview)
    switch (verb)
    {
      case UI_EXECUTIONVERB_EXECUTE:
        if(nCmdID == cmdTextSizeGallery || 
           nCmdID == cmdTextSizeGallery2 || 
           nCmdID == cmdTextSizeGallery3)
        {
          if (pCommandExecutionProperties != NULL)
          {
            CItemProperties *pItem = 
              static_cast<CItemProperties *>(pCommandExecutionProperties);
            g_prevSelection = g_index = pItem->GetIndex();
            UpdateGallerySelectedItems();
            ::InvalidateRect(g_hWindowFrame, NULL, TRUE);
          }
          else
          {
            g_prevSelection = g_index = 0;
            UpdateGallerySelectedItems();
            ::InvalidateRect(g_hWindowFrame, NULL, TRUE);
          }
        }           
        break;
      case UI_EXECUTIONVERB_PREVIEW:
        CItemProperties *pItem = 
          static_cast<CItemProperties *>(pCommandExecutionProperties);
        g_index = pItem->GetIndex();
        ::InvalidateRect(g_hWindowFrame, NULL, TRUE);
        break;
      case UI_EXECUTIONVERB_CANCELPREVIEW:
        g_index = g_prevSelection;
        ::InvalidateRect(g_hWindowFrame, NULL, TRUE);
        break;
    }   
    return hr;
  }

  // Gallery command handler's UpdateProperty method
  STDMETHODIMP UpdateProperty(UINT nCmdID,
                              REFPROPERTYKEY key,
                              const PROPVARIANT* ppropvarCurrentValue,
                              PROPVARIANT* ppropvarNewValue)
  {
    UNREFERENCED_PARAMETER(ppropvarCurrentValue);

    HRESULT hr = E_NOTIMPL;         

    if (key == UI_PKEY_ItemsSource) // Gallery items requested
    {
      if (nCmdID == cmdTextSizeGallery || 
          nCmdID == cmdTextSizeGallery2 || 
          nCmdID == cmdTextSizeGallery3)
      {
        CComQIPtr<IUICollection> spCollection(ppropvarCurrentValue->punkVal);

        int count = _countof(g_labels);

        for (int i = 0; i < count; i++)
        {
          CComObject<CItemProperties> * pItem;
          CComObject<CItemProperties>::CreateInstance(&pItem);
                    
          pItem->AddRef();
          pItem->Initialize(i);

          spCollection->Add(pItem);
        }
        return S_OK;
      }
      if (nCmdID == cmdCommandGallery1)
      {
        CComQIPtr<IUICollection> spCollection(ppropvarCurrentValue->punkVal);

        int count = 12;
        int commands[] = {cmdButton1, 
                          cmdButton2, 
                          cmdBoolean1, 
                          cmdBoolean2, 
                          cmdButton1, 
                          cmdButton2, 
                          cmdBoolean1, 
                          cmdBoolean2, 
                          cmdButton1, 
                          cmdButton2, 
                          cmdBoolean1, 
                          cmdBoolean2};

        for (int i = 0; i < count; i++)
        {
          CComObject<CItemProperties> * pItem;
          CComObject<CItemProperties>::CreateInstance(&pItem);
                    
          pItem->AddRef();
          pItem->InitializeAsCommand(commands[i]);

          spCollection->Add(pItem);
        }
        return S_OK;
      }
    }        
    else if (key == UI_PKEY_SelectedItem) // Selected item requested
    {           
      hr = UIInitPropertyFromUInt32(UI_PKEY_SelectedItem, g_index, ppropvarNewValue);           
    }
    return hr;
  }
};

```



### <a name="bind-the-command-handler"></a>系結命令處理常式

在您定義命令處理常式之後，命令必須系結至處理常式。

下列範例示範如何將資源庫命令系結至特定的命令處理常式。 在此情況下， [**ComboBox**](windowsribbon-element-combobox.md) 和圖庫控制項都會系結至各自的命令處理常式。


```C++
// Called for each Command in markup. 
// Application will return a Command handler for each Command.
STDMETHOD(OnCreateUICommand)(UINT32 nCmdID,
                             UI_COMMANDTYPE typeID,
                             IUICommandHandler** ppCommandHandler) 
{   
  // CommandType for ComboBox and galleries
  if (typeID == UI_COMMANDTYPE_COLLECTION || typeID == UI_COMMANDTYPE_COMMANDCOLLECTION) 
  {
    switch (nCmdID)
    {
      case cmdComboBox:
        CComObject<CComboBoxCommandHandler> * pComboBoxCommandHandler;
        CComObject<CComboBoxCommandHandler>::CreateInstance(&pComboBoxCommandHandler);
        return pComboBoxCommandHandler->QueryInterface(IID_PPV_ARGS(ppCommandHandler));
      default:
        CComObject<CGalleryCommandHandler> * pGalleryCommandHandler;
        CComObject<CGalleryCommandHandler>::CreateInstance(&pGalleryCommandHandler);
        return pGalleryCommandHandler->QueryInterface(IID_PPV_ARGS(ppCommandHandler));
    }
    return E_NOTIMPL; // Command is not implemented, so do not pass a handler back.
  }
}
```



### <a name="initialize-a-collection"></a>初始化集合

下列範例示範針對專案和命令資源庫， [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) 的自訂執行。

此範例中的 CItemProperties 類別衍生自 [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset)。 除了所需的方法 [**IUISimplePropertySet：： GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue)之外，CItemProperties 類別還會執行一組 helper 函式來進行初始化和索引追蹤。


```C++
//
//  PURPOSE:    Implementation of IUISimplePropertySet.
//
//  COMMENTS:
//              Three gallery-specific helper functions included. 
//

class CItemProperties
  : public CComObjectRootEx<CComMultiThreadModel>
  , public IUISimplePropertySet
{
  public:

  // COM map for QueryInterface of IUISimplePropertySet.
  BEGIN_COM_MAP(CItemProperties)
    COM_INTERFACE_ENTRY(IUISimplePropertySet)
  END_COM_MAP()

  // Required method that enables property key values to be 
  // retrieved on gallery collection items.
  STDMETHOD(GetValue)(REFPROPERTYKEY key, PROPVARIANT *ppropvar)
  {
    HRESULT hr;

    // No category is associated with this item.
    if (key == UI_PKEY_CategoryId)
    {
      return UIInitiPropertyFromUInt32(UI_PKEY_CategoryId, 
                                       UI_COLLECTION_INVALIDINDEX, 
                                       pprovar);
    }

    // A Command gallery.
    // _isCommandGallery is set on initialization.
    if (_isCommandGallery)
    {           
      if(key == UI_PKEY_CommandId && _isCommandGallery)
      {
        // Return a pointer to the CommandId of the item.
        return InitPropVariantFromUInt32(_cmdID, ppropvar);
      }         
    }
    // An item gallery.
    else
    {
      if (key == UI_PKEY_Label)
      {
        // Return a pointer to the item label string.
        return UIInitPropertyFromString(UI_PKEY_Label, ppropvar);
      }
      else if(key == UI_PKEY_ItemImage)
      {
        // Return a pointer to the item image.
        return UIInitPropertyFromImage(UI_PKEY_ItemImage, ppropvar);
      }         
    }
    return E_NOTIMPL;
  }

  // Initialize an item in an item gallery collection at the specified index.
  void Initialize(int index)
  {
    _index = index;
    _cmdID = 0;
    _isCommandGallery = false;
  }

  // Initialize a Command in a Command gallery.
  void InitializeAsCommand(__in UINT cmdID)
  {
    _index = 0;
    _cmdID = cmdID;
    _isCommandGallery = true;
  }

  // Gets the index of the selected item in an item gallery.
  int GetIndex()
  {
    return _index;
  }

private:
  int _index;
  int _cmdID;
  bool _isCommandGallery;   
};
```



### <a name="handle-collection-events"></a>處理收集事件

下列範例示範 IUICollectionChangedEvent 的執行。


```C++
class CQATChangedEvent
  : public CComObjectRootEx<CComSingleThreadModel>
  , public IUICollectionChangedEvent
{
  public:

  HRESULT FinalConstruct()
  {
    _pSite = NULL;
    return S_OK;
  }

  void Initialize(__in CQATSite* pSite)
  {
    if (pSite != NULL)
    {
      _pSite = pSite;
    }
  }

  void Uninitialize()
  {
    _pSite = NULL;
  }

  BEGIN_COM_MAP(CQATChangedEvent)
    COM_INTERFACE_ENTRY(IUICollectionChangedEvent)
  END_COM_MAP()

  // IUICollectionChangedEvent interface
  STDMETHOD(OnChanged)(UI_COLLECTIONCHANGE action, 
                       UINT32 oldIndex, 
                       IUnknown *pOldItem, 
                       UINT32 newIndex, 
                       IUnknown *pNewItem)
  {
    if (_pSite)
    {
      _pSite->OnCollectionChanged(action, oldIndex, pOldItem, newIndex, pNewItem);
    }
    return S_OK;
  }

  protected:
  virtual ~CQATChangedEvent(){}

  private:
  CQATSite* _pSite; // Weak ref to avoid circular refcounts
};

HRESULT CQATHandler::EnsureCollectionEventListener(__in IUICollection* pUICollection)
{
  // Check if listener already exists.
  if (_spQATChangedEvent)
  {
    return S_OK;
  }

  HRESULT hr = E_FAIL;

  // Create an IUICollectionChangedEvent listener.
  hr = CreateInstanceWithRefCountOne(&_spQATChangedEvent);
    
  if (SUCCEEDED(hr))
  {
    CComPtr<IUnknown> spUnknown;
    _spQATChangedEvent->QueryInterface(IID_PPV_ARGS(&spUnknown));

    // Create a connection between the collection connection point and the sink.
    AtlAdvise(pUICollection, spUnknown, __uuidof(IUICollectionChangedEvent), &_dwCookie);
    _spQATChangedEvent->Initialize(this);
  }
  return hr;
}

HRESULT CQATHandler::OnCollectionChanged(
             UI_COLLECTIONCHANGE action, 
          UINT32 oldIndex, 
             IUnknown *pOldItem, 
          UINT32 newIndex, 
          IUnknown *pNewItem)
{
    UNREFERENCED_PARAMETER(oldIndex);
    UNREFERENCED_PARAMETER(newIndex);

    switch (action)
    {
      case UI_COLLECTIONCHANGE_INSERT:
      {
        CComQIPtr<IUISimplePropertySet> spProperties(pNewItem);
                
        PROPVARIANT var;
        if (SUCCEEDED(spProperties->GetValue(UI_PKEY_CommandId, &var)))
        {
          UINT tcid;
          if (SUCCEEDED(UIPropertyToUInt32(UI_PKEY_CommandId, var, &tcid)))
          {
            FireETWEvent(tcid, L"Added to QAT");
            PropVariantClear(&var);
          }
        }
      }
      break;
      case UI_COLLECTIONCHANGE_REMOVE:
      {
        CComQIPtr<IUISimplePropertySet> spProperties(pOldItem);
                
        PROPVARIANT var;
        if (SUCCEEDED(spProperties->GetValue(UI_PKEY_CommandId, &var)))
        {
          UINT tcid;
          if (SUCCEEDED(UIPropertyToUInt32(UI_PKEY_CommandId, var, &tcid)))
          {
            FireETWEvent(tcid, L"Removed from QAT");
            PropVariantClear(&var);
          }
        }
      }
      break;
    default:
  }
  return S_OK;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[集合屬性](windowsribbon-reference-properties-collection.md)
</dt> <dt>

[建立功能區應用程式](windowsribbon-stepbystep.md)
</dt> <dt>

[瞭解命令和控制項](windowsribbon-commandscontrols.md)
</dt> <dt>

[功能區使用者體驗指導方針](https://msdn.microsoft.com/library/cc872782.aspx)
</dt> <dt>

[功能區設計流程](https://msdn.microsoft.com/library/cc872781.aspx)
</dt> <dt>

[資源庫範例](windowsribbon-gallerysample.md)
</dt> </dl>

 

 
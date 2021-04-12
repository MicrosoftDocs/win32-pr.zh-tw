---
title: 字型控制項
description: 為了在需要文字處理和文字編輯功能的應用程式中簡化字型支援的整合和設定，Windows 功能區架構會提供特製化的字型控制項，以公開字型名稱、樣式、點大小和效果等範圍的字型屬性。
ms.assetid: 6052f2e3-2c9e-432e-9ed6-c1e3a50843d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e179296ae03163bf03e08d2fbf7287264792e6e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375832"
---
# <a name="font-control"></a>字型控制項

為了在需要文字處理和文字編輯功能的應用程式中簡化字型支援的整合和設定，Windows 功能區架構會提供特製化的字型控制項，以公開字型名稱、樣式、點大小和效果等範圍的字型屬性。

-   [簡介](#introduction)
-   [一致的體驗](#a-consistent-experience)
-   [輕鬆整合和設定](#easy-integration-and-configuration)
-   [與常用 GDI 文字結構對齊](#alignment-with-common-gdi-text-structures)
-   [新增 FontControl](#add-a-fontcontrol)
    -   [在標記中宣告 FontControl](#declaring-a-fontcontrol-in-markup)
    -   [字型控制項屬性](#font-control-properties)
-   [定義 FontControl 命令處理常式](#define-a-fontcontrol-command-handler)
-   [相關主題](#related-topics)

## <a name="introduction"></a>簡介

字型控制項是由按鈕、切換按鈕、下拉式清單方塊和下拉式方塊組成的複合控制項，它們全都是用來指定特定的字型屬性或格式選項。

下列螢幕擷取畫面顯示 Windows 7 的 WordPad 中的功能區字型控制項。

![fontcontrol 專案的螢幕擷取畫面，其中 richfont 屬性設定為 true。](images/controls/fontcontrol.png)

## <a name="a-consistent-experience"></a>一致的體驗

字型控制項是內建的功能區控制項，可改善整體字型管理、選取和格式化功能，並在所有功能區應用程式中提供豐富且一致的使用者體驗。

這種一致的體驗包括

-   跨功能區應用程式標準化格式化和選取字型。
-   跨功能區應用程式的標準化字型標記法。
-   自動，在 Windows 7 中，以字型 **[控制台]** 中每個字型的 [**顯示**] 或 [**隱藏**] 設定為基礎的字型啟用。 字型控制項只會顯示已設定為 **顯示** 的字型。
    > [!Note]  
    > 在 Windows Vista 中， **[字型** ] 控制台不提供 **顯示** 或 **隱藏** 功能，因此所有字型都會啟用。

     

-   可直接從控制項取得的字型管理。

    下列螢幕擷取畫面顯示可直接從 **字型控制項存取 [字型** ] 控制台。

    ![適用于 windows 7 之 wordpad 中的字型系列清單螢幕擷取畫面。](images/controls/fontcontrol-fontcpl.png)

-   支援自動預覽。
-   公開與使用者最相關的字型，例如
    -   國際使用者的當地語系化字型清單。
    -   以輸入裝置為基礎的字型清單。

    > [!Note]  
    > 在 Windows 7 之前的任何平臺上，都無法使用此功能的支援。

     

## <a name="easy-integration-and-configuration"></a>輕鬆整合和設定

藉由提供標準、可重複使用且容易使用的功能，功能區字型控制項可減輕將字型支援整合至應用程式的負擔。

字型選取和格式的詳細資料會包裝在一個獨立的邏輯元素中，

-   消除了字型控制項執行的複雜控制項相依性管理。
-   所有由字型控制項子控制項公開的功能，都需要單一的命令處理常式。

這個單一命令處理常式允許字型控制項在內部管理各種子控制項的功能;子控制項絕不會直接與應用程式互動，而不論其功能為何。

字型控制項的其他功能包括

-   自動、DPI 感知的 WYSIWYG 世代 (您所看到的內容，就是您在 [ **字型系列** ] 功能表中為每個字型取得) 點陣圖表示的結果。
-   [Windows 圖形裝置介面 (GDI) ](../gdi/windows-gdi.md) 整合。
-   當地語系化的字型系列點陣圖和工具提示。
-   用來管理和呈現字型的字型列舉、群組和中繼資料。
    > [!Note]  
    > 在 Windows 7 之前的任何平臺上，都無法使用此功能的支援。

     

-   反映功能區 [下拉式色彩選擇器](windowsribbon-controls-dropdowncolorpicker.md)行為的 **文字色彩** 和 **文字反白顯示** 色彩下拉式清單。
-   支援以所有字型控制項庫為基礎的子控制項進行自動預覽： **字型家族**、 **字型大小**、 **文字色彩** 和 **文字反白顯示色彩**。

## <a name="alignment-with-common-gdi-text-structures"></a>與常用 GDI 文字結構對齊

[Windows 圖形裝置介面 (GDI) ](../gdi/windows-gdi.md) 文字堆疊元件可用來透過功能區字型控制項來公開字型選取和格式化功能。 [LOGFONT 結構](/windows/win32/api/wingdi/ns-wingdi-logfonta)、 [CHOOSEFONT 結構](/windows/win32/api/commdlg/ns-commdlg-choosefonta)和[CHARFORMAT2 結構](/windows/win32/api/richedit/ns-richedit-charformat2a)所支援的各種字型功能都是透過字型控制項中所包含的子控制項來公開。

字型控制項中顯示的子控制項，取決於在功能區標記中宣告的 *FontType* 範本。 下節 (詳細討論的 *FontType* 範本，) 是設計來配合一般 [WINDOWS 圖形裝置介面 (GDI)](../gdi/windows-gdi.md) 文字結構。

## <a name="add-a-fontcontrol"></a>新增 FontControl

本節概述將字型控制項新增至功能區應用程式的基本步驟。

### <a name="declaring-a-fontcontrol-in-markup"></a>在標記中宣告 FontControl

如同其他功能區控制項，字型控制項是在具有 [**FontControl**](windowsribbon-element-fontcontrol.md) 專案的標記中宣告，並且透過命令識別碼與命令宣告相關聯。 當編譯應用程式時，會使用命令識別碼將命令系結至主應用程式中的命令處理常式。

> [!Note]  
> 如果未在標記中使用 [**FontControl**](windowsribbon-element-fontcontrol.md) 宣告任何命令 ID，則架構會產生一個識別碼。

 

由於不會直接公開字型控制項的子控制項，因此自訂字型控制項僅限於架構所定義的三個 *FontType* 版面配置範本。

將版面配置範本與 [**FontControl**](windowsribbon-element-fontcontrol.md) 屬性（例如 *IsHighlightButtonVisible*、 *IsStrikethroughButtonVisible* 和 *IsUnderlineButtonVisible*）結合，即可完成字型控制項的自訂。

> [!Note]  
> 除了標準字型控制項範本和屬性所公開的字型功能之外，還需要在本文討論範圍之外的自訂字型控制項執行。

 

下表列出字型控制項範本，以及每個範本對齊的編輯控制項類型。



| 範本      | 支援                                                                 |
|---------------|--------------------------------------------------------------------------|
| FontOnly      | [LOGFONT 結構](/windows/win32/api/wingdi/ns-wingdi-logfonta)     |
| FontWithColor | [CHOOSEFONT 結構](/windows/win32/api/commdlg/ns-commdlg-choosefonta)  |
| RichFont      | [CHARFORMAT2 結構](/windows/win32/api/richedit/ns-richedit-charformat2a) |



 

下表列出與每個範本相關聯的控制項，並識別相關聯範本的選擇性控制項。



控制項

範本

**RichFont**

**FontWithColor**

**FontOnly**

預設

選擇性

預設

選擇性

預設

選擇性

**字型大小** 下拉式方塊

是

否

是

否

是

否

**字型家族** 下拉式方塊

是

否

是

否

是

否

**放大字型** 按鈕

是

是

是

是

\-

\-

**壓縮字型** 按鈕

是

是

是

是

\-

\-

**粗體** 按鈕

是

否

是

否

是

否

**斜體** 按鈕

是

否

是

否

是

否

底線按鈕

是

否

是

是

是

是

**刪除線** 按鈕

是

否

是

是

是

是

注 **標** 按鈕

是

否

\-

\-

\-

\-

**上標** 按鈕

是

否

\-

\-

\-

\-

**文字反白顯示色彩** 按鈕

是

否

是

是

\-

\-

**文字色彩** 按鈕

是

否

是

否

\-

\-



 

當您宣告字型控制項的版面配置行為時，功能區架構會提供選擇性的 *SizeDefinition* 版面配置範本， `OneFontControl` 它會根據功能區大小和字型控制項可用的空間，定義兩個子控制項設定。 如需詳細資訊，請參閱 [透過大小定義自訂功能區和調整原則](windowsribbon-templates.md)。

### <a name="adding-a-fontcontrol-to-a-ribbon"></a>將 FontControl 新增至功能區

下列程式碼範例示範將字型控制項新增至功能區的基本標記需求：

這段程式碼會顯示 [**FontControl**](windowsribbon-element-fontcontrol.md)命令宣告標記，包括在 [**功能區**](windowsribbon-element-ribbon.md)中顯示控制項所需的 [**Tab**](windowsribbon-element-tab.md)和 [**Group**](windowsribbon-element-group.md)命令。


```C++
<Command Name="cmdTab1"
  Comment="These comments are optional and are inserted into the header file."
  Symbol="cmdTab1" Id="10000" >
  <Command.LabelTitle>Tab 1</Command.LabelTitle>
</Command>
<Command Name="cmdGroup1" Comment="Group #1" Symbol="cmdGroup1" Id="20000">
  <!-- This image is used when the group scales to a pop-up. -->
  <Command.SmallImages>
    <Image>res/Button_Image.bmp</Image>
  </Command.SmallImages>
</Command>
<Command Name="cmdFontControl" Symbol="cmdFontControl" Comment="FontControl" Id="25001" Keytip="F" />
```



這一節的程式碼顯示使用命令識別碼來宣告 [**FontControl**](windowsribbon-element-fontcontrol.md) 與 [**命令**](windowsribbon-element-command.md) 的必要標記。 此特定範例包括索引標籤和 [**群組**](windowsribbon-element-group.md)宣告 [**，以及縮放**](windowsribbon-element-tab.md)喜好設定。


```C++
<Ribbon.Tabs>
  <Tab CommandName="cmdTab1">
    <Tab.ScalingPolicy>
      <ScalingPolicy>
        <ScalingPolicy.IdealSizes>
          <Scale Group="cmdGroup1" Size="Large" />
        </ScalingPolicy.IdealSizes>
        <!-- Describe how the FontControl group scales. -->
        <Scale Group="cmdGroup1" Size="Medium" />
        <Scale Group="cmdGroup1" Size="Popup" />
      </ScalingPolicy>
    <Group CommandName="cmdGroup1" SizeDefinition="OneFontControl">
      <FontControl CommandName="cmdFontControl" FontType="RichFont" />
    </Group>
  </Tab>
</Ribbon.Tabs>
```



### <a name="adding-a-fontcontrol-to-a-contextpopup"></a>將 FontControl 新增至 CoNtextPopup

將字型控制項新增至 [內容快顯視窗](windowsribbon-controls-contextpopup.md) ，需要的程式類似于將字型控制項加入功能區。 不過， [**浮動工具列**](windowsribbon-element-minitoolbar.md) 中的字型控制項受限於所有字型控制項範本通用的預設子控制項集： **字型家族**、 **字型大小**、 **粗體** 和 **斜體**。

下列程式碼範例示範將字型控制項新增至 [內容快顯視窗](windowsribbon-controls-contextpopup.md)的基本標記需求：

這段程式碼會顯示在 [**CoNtextPopup**](windowsribbon-element-contextpopup.md)中顯示 **FontControl** 所需的 [**FontControl**](windowsribbon-element-fontcontrol.md)命令宣告標記。


```C++
<Command Name="cmdFontControl" Symbol="cmdFontControl" Comment="FontControl" Id="25001" />
```



這一節的程式碼顯示使用命令識別碼來宣告 [**FontControl**](windowsribbon-element-fontcontrol.md) 與命令的必要標記。


```C++
<ContextPopup.MiniToolbars>
  <MiniToolBar Name="MiniToolbar1">
    <MenuCategory Class="StandardItems">
      <FontControl CommandName="cmdFontControl" />
    </MenuCategory>
  </MiniToolBar>
</ContextPopup.MiniToolbars>
```



### <a name="keytips"></a>按鍵提示

功能區字型控制項中的每個子控制項都可以透過鍵盤快速鍵或 keytip 來存取。 此快捷方式已預先定義，並由架構指派給每個子控制項。

如果在標記中將 [ *快速鍵* ] 屬性值指派給 [**FontControl**](windowsribbon-element-fontcontrol.md) 元素，則會將此值新增為架構定義之 Keytip 的前置詞。

> [!Note]  
> 應用程式應該為此前置詞強制採用單一字元的規則。

 

下表列出由架構所定義的按鍵提示。 

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>子控制項</th>
<th>Keytip</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>字型家族</td>
<td>F</td>
</tr>
<tr class="even">
<td>字型樣式</td>
<td>T</td>
</tr>
<tr class="odd">
<td>字型大小</td>
<td>S</td>
</tr>
<tr class="even">
<td>成長字型</td>
<td>G</td>
</tr>
<tr class="odd">
<td>壓縮字型</td>
<td>K</td>
</tr>
<tr class="even">
<td>粗體</td>
<td>B</td>
</tr>
<tr class="odd">
<td>斜體</td>
<td>I</td>
</tr>
<tr class="even">
<td>Underline</td>
<td>U</td>
</tr>
<tr class="odd">
<td>刪除線</td>
<td>X</td>
</tr>
<tr class="even">
<td>標</td>
<td>Y 或 Z
<blockquote>
[!Note]<br />
如果 [ <em>快速鍵</em> ] 屬性未在標記中宣告，則預設的快速鍵提示為 Y;否則，預設的快速鍵提示會是 <em>keytip</em> + Z。
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>標</td>
<td>A</td>
</tr>
<tr class="even">
<td>字型色彩</td>
<td>C</td>
</tr>
<tr class="odd">
<td>字型醒目提示</td>
<td>H</td>
</tr>
</tbody>
</table>



 

多語系消費者介面 (MUI 的建議首碼) EN-US 功能區是 ' F '，如下列範例所示。


```C++
<Command Name="cmdFontControl" Symbol="cmdFontControl" Comment="FontControl" Id="25001" Keytip="F" />
```



下列螢幕擷取畫面說明字型控制項按鍵提示，因為它們是在上一個範例中定義的。

![適用于 windows 7 之 wordpad 中的 fontcontrol 按鍵提示螢幕擷取畫面。](images/controls/fontcontrol-keytips.png)

### <a name="the-ribbon-resource-file"></a>功能區資源檔

編譯標記檔案時，會產生包含功能區應用程式之所有資源參考的資源檔。

簡單資源檔的範例：


```C++
// ******************************************************************************
// * This is an automatically generated file containing the ribbon resource for *
// * your application.                                                          *
// ******************************************************************************

#include ".\ids.h"

STRINGTABLE 
BEGIN
  cmdTab1_LabelTitle_RESID L"Tab 1" 
    /* LabelTitle cmdTab1_LabelTitle_RESID: These comments are optional and are 
       inserted into the header file. */
END

cmdGroup1_SmallImages_RESID    BITMAP    "res\\Button_Image.bmp" 
  /* SmallImages cmdGroup1_SmallImages_RESID: Group #1 */
STRINGTABLE 
BEGIN
  cmdFontControl_Keytip_RESID L"F" /* Keytip cmdFontControl_Keytip_RESID: FontControl */
END

FCSAMPLE_RIBBON    UIFILE    "Debug\\FCSample.bml"

```



### <a name="font-control-properties"></a>字型控制項屬性

功能區架構會為字型控制項和其組成子控制項定義 [屬性索引鍵](windowsribbon-reference-properties.md) 的集合。

一般而言，字型控制項屬性會在功能區 UI 中更新，方法是透過呼叫 [**IUIFramework：： InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) 方法來使與控制項相關聯的命令失效。 [**IUICommandHandler：： UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)回呼方法會處理失效事件，並定義屬性更新。

[**IUICommandHandler：： UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)回呼方法未執行，而且應用程式會查詢已更新的屬性值，直到架構需要該屬性為止。 例如，啟用索引標籤時，以及在功能區 UI 中顯示控制項，或顯示工具提示時。

> [!Note]  
> 在某些情況下，可以透過 [**IUIFramework：： GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) 方法抓取屬性，並使用 [**IUIFramework：： SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) 方法進行設定。

 

下表列出與字型控制項相關聯的屬性索引鍵。



| 屬性索引鍵                                                                                                                  | 備註                                                                                                                                                                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [UI \_ PKEY \_ FontProperties](windowsribbon-reference-properties-uipkey-fontproperties.md)                                      | 將匯總中的 [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) 物件公開為所有字型控制項子控制項屬性。<br/> 當 `UI_INVALIDATIONS_VALUE` 做為 [**IUIFramework：： InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand)呼叫中的 *旗標* 值傳遞時，架構會查詢這個屬性。<br/> |
| [UI \_ PKEY \_ FontProperties \_ ChangedProperties](windowsribbon-reference-properties-uipkey-fontproperties-changedproperties.md) | 在匯總中公開為 [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) 物件，只有已變更的字型控制項子控制項屬性。<br/>                                                                                                                                                                                                        |
| [UI \_ PKEY \_ 按鍵提示](windowsribbon-reference-properties-uipkey-keytip.md)                                                      | 只能透過失效進行更新。                                                                                                                                                                                                                                                                                                                                                      |
| [UI \_ PKEY \_ 已啟用](windowsribbon-reference-properties-uipkey-enabled.md)                                                    | 支援 [**IUIFramework：： GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) 和 [**IUIFramework：： SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty)。                                                                                                                                                                  |



 

除了字型控制項本身所支援的屬性之外，功能區架構也會定義每個字型控制項子控制項的 [屬性索引鍵](windowsribbon-reference-properties.md) 。 架構會透過 [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) 介面執行來公開這些屬性索引鍵及其值，此介面會定義用來管理集合的方法，也稱為屬性包（名稱和值組）。

應用程式會將字型結構轉譯成可透過 [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) 介面方法存取的屬性。 此模型強調字型控制項和 Windows 圖形裝置介面 (GDI) 文字堆疊元件之間的差異， ([LOGFONT 結構](/windows/win32/api/wingdi/ns-wingdi-logfonta)、 [CHOOSEFONT 結構](/windows/win32/api/commdlg/ns-commdlg-choosefonta)，以及 Framework 所支援的 [CHARFORMAT2 結構](/windows/win32/api/richedit/ns-richedit-charformat2a)) 。

下表列出個別控制項與其相關聯的屬性索引鍵。



| 控制項                 | 屬性索引鍵                                                                                                                                                                                                                                                           | 備註                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **字型大小**            | [UI \_ PKEY \_ FontProperties \_ 大小](windowsribbon-reference-properties-uipkey-fontproperties-size.md)                                                                                                                                                                    | 反白顯示執行 heterogeneously 大小的文字時，功能區架構會將 **字型大小** 控制項設定為空白，並將 [UI \_ PKEY \_ FontProperties \_ 大小](windowsribbon-reference-properties-uipkey-fontproperties-size.md) 的值設定為0。 按一下 [ **成長字型** ] 或 [ **縮小字型** ] 按鈕時，會重設所有反白顯示的文字大小，但會保留文字大小的相對差異。                                                                                                                                                    |
| **字型家族**          | [UI \_ PKEY \_ FontProperties \_ 系列](windowsribbon-reference-properties-uipkey-fontproperties-family.md)                                                                                                                                                                | GDI 字型系列名稱會隨著系統地區設定而有所不同。 因此，如果在應用程式會話之間保留 [UI \_ PKEY \_ FontProperties \_ 系列](windowsribbon-reference-properties-uipkey-fontproperties-family.md) 的值，則應該在每個新的會話上取出該值。                                                                                                                                                                                                                                                                            |
| **成長字型**            | [UI \_ PKEY \_ FontProperties \_ 大小](windowsribbon-reference-properties-uipkey-fontproperties-size.md)                                                                                                                                                                    | 請參閱 **字型大小**。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **壓縮字型**          | [UI \_ PKEY \_ FontProperties \_ 大小](windowsribbon-reference-properties-uipkey-fontproperties-size.md)                                                                                                                                                                    | 請參閱 **字型大小**。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **粗體字**                 | [UI \_ PKEY \_ FontProperties \_ Bold](windowsribbon-reference-properties-uipkey-fontproperties-bold.md)                                                                                                                                                                    |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| **斜體**               | [UI \_ PKEY \_ FontProperties \_ 斜體](windowsribbon-reference-properties-uipkey-fontproperties-italic.md)                                                                                                                                                                |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| **Underline**            | [UI \_ PKEY \_ FontProperties \_ 波浪線](windowsribbon-reference-properties-uipkey-fontproperties-underline.md)                                                                                                                                                          |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| **刪除線**        | [UI \_ PKEY \_ FontProperties \_ 刪除線](windowsribbon-reference-properties-uipkey-fontproperties-strikethrough.md)                                                                                                                                                  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| **標**            | [UI \_ PKEY \_ FontProperties \_ VerticalPositioning](windowsribbon-reference-properties-uipkey-fontproperties-verticalpositioning.md)                                                                                                                                      | 如果設定了 [注 **標** ] 按鈕，則也無法設定 **上標** 。                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **標**          | [UI \_ PKEY \_ FontProperties \_ VerticalPositioning](windowsribbon-reference-properties-uipkey-fontproperties-verticalpositioning.md)                                                                                                                                      | 如果設定了 **上標** 按鈕，則也不能設定注 **標** 。                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **文字反白顯示色彩** | [UI \_PKEY \_ FontProperties \_ BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor)、 [UI \_ PKEY \_ FontProperties \_ BackgroundColorType](windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolortype.md) | 提供與 `HighlightColors` [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) 元素之範本相同的功能。<br/> 強烈建議您只設定應用程式所需的初始 **文字醒目提示色彩** 值。 當游標在檔內重新置放時，應該保留最後一個選取的值，而且不會設定。 這可讓使用者快速存取最後選取的專案，而不需要重新開啟色彩選擇器。<br/> 無法自訂色彩色板。<br/> |
| **文字色彩**           | [UI \_PKEY \_ FontProperties \_ ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md)、 [UI \_ PKEY \_ FontProperties \_ ForegroundColorType](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolortype.md)           | 提供與 `StandardColors` [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) 元素之範本相同的功能。<br/> 強烈建議您只設定應用程式所需的初始 **文字色彩** 值。 當游標在檔內重新置放時，應該保留最後一個選取的值，而且不會設定。 這可讓使用者快速存取最後選取的專案，而不需要重新開啟色彩選擇器。<br/> 無法自訂色彩色板。<br/>            |



 

## <a name="define-a-fontcontrol-command-handler"></a>定義 FontControl 命令處理常式

本節說明將字型控制項系結至命令處理常式所需的步驟。

> [!WARNING]
> 如果沒有與控制項相關聯的命令處理常式，嘗試從字型控制項的色彩選擇器選取色彩樣本，可能會造成存取違規。

 

下列程式碼範例示範如何將標記中宣告的命令系結至命令處理常式。


```C++
//
//  FUNCTION: OnCreateUICommand(UINT, UI_COMMANDTYPE, IUICommandHandler)
//
//  PURPOSE: Called by the Ribbon framework for each command specified in markup, to allow
//           the host application to bind a command handler to that command.
//
STDMETHODIMP CApplication::OnCreateUICommand(
  UINT nCmdID,
  __in UI_COMMANDTYPE typeID,
  __deref_out IUICommandHandler** ppCommandHandler)
{
  UNREFERENCED_PARAMETER(typeID);
  UNREFERENCED_PARAMETER(nCmdID);

  if (NULL == m_pCommandHandler)
  {
    HRESULT hr = CCommandHandler::CreateInstance(&m_pCommandHandler);
    if (FAILED(hr))
    {
      return hr;
    }
  }

  return m_pCommandHandler->QueryInterface(IID_PPV_ARGS(ppCommandHandler));
}
```



下列程式碼範例說明如何針對字型控制項來執行 [**IUICommandHandler：： Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) 方法。


```C++
//
//  FUNCTION: Execute()
//
//  PURPOSE: Called by the Ribbon framework when a command is executed 
//           by the user. For example, when a button is pressed.
//
STDMETHODIMP CCommandHandler::Execute(
  UINT nCmdID,
  UI_EXECUTIONVERB verb,
  __in_opt const PROPERTYKEY* key,
  __in_opt const PROPVARIANT* ppropvarValue,
  __in_opt IUISimplePropertySet* pCommandExecutionProperties)
{
  UNREFERENCED_PARAMETER(nCmdID);

  HRESULT hr = E_NOTIMPL;
  if ((key) && (*key == UI_PKEY_FontProperties))
  {
    // Font properties have changed.
    switch (verb)
    {
      case UI_EXECUTIONVERB_EXECUTE:
      {
        hr = E_POINTER;
        if (pCommandExecutionProperties != NULL)
        {
          // Get the changed properties.
          PROPVARIANT varChanges;
          hr = pCommandExecutionProperties->GetValue(UI_PKEY_FontProperties_ChangedProperties, &varChanges);
          if (SUCCEEDED(hr))
          {
            IPropertyStore *pChanges;
            hr = UIPropertyToInterface(UI_PKEY_FontProperties, varChanges, &pChanges);
            if (SUCCEEDED(hr))
            {
              // Using the changed properties, set the new font on the selection on RichEdit control.
              g_pFCSampleAppManager->SetValues(pChanges);
              pChanges->Release();
            }
            PropVariantClear(&varChanges);
          }
        }
        break;
      }
      case UI_EXECUTIONVERB_PREVIEW:
      {
        hr = E_POINTER;
        if (pCommandExecutionProperties != NULL)
        {
          // Get the changed properties for the preview event.
          PROPVARIANT varChanges;
          hr = pCommandExecutionProperties->GetValue(UI_PKEY_FontProperties_ChangedProperties, &varChanges);
          if (SUCCEEDED(hr))
          {
            IPropertyStore *pChanges;
            hr = UIPropertyToInterface(UI_PKEY_FontProperties, varChanges, &pChanges);
            if (SUCCEEDED(hr))
            {
              // Set the previewed values on the RichEdit control.
              g_pFCSampleAppManager->SetPreviewValues(pChanges);
              pChanges->Release();
            }
            PropVariantClear(&varChanges);
          }
        }
        break;
      }
      case UI_EXECUTIONVERB_CANCELPREVIEW:
      {
        hr = E_POINTER;
        if (ppropvarValue != NULL)
        {
          // Cancel the preview.
          IPropertyStore *pValues;
          hr = UIPropertyToInterface(UI_PKEY_FontProperties, *ppropvarValue, &pValues);
          if (SUCCEEDED(hr))
          {   
            g_pFCSampleAppManager->CancelPreview(pValues);
            pValues->Release();
          }
        }
        break;
      }
    }
  }

  return hr;
}
```



下列程式碼範例說明如何針對字型控制項來執行 [**IUICommandHandler：： UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) 方法。


```C++
//
//  FUNCTION: UpdateProperty()
//
//  PURPOSE: Called by the Ribbon framework when a command property (PKEY) needs to be updated.
//
//  COMMENTS:
//
//    This function is used to provide new command property values, such as labels, icons, or
//    tooltip information, when requested by the Ribbon framework.  
//    
//
STDMETHODIMP CCommandHandler::UpdateProperty(
  UINT nCmdID,
  __in REFPROPERTYKEY key,
  __in_opt const PROPVARIANT* ppropvarCurrentValue,
  __out PROPVARIANT* ppropvarNewValue)
{
  UNREFERENCED_PARAMETER(nCmdID);

  HRESULT hr = E_NOTIMPL;
  if (key == UI_PKEY_FontProperties)
  {
    hr = E_POINTER;
    if (ppropvarCurrentValue != NULL)
    {
      // Get the font values for the selected text in the font control.
      IPropertyStore *pValues;
      hr = UIPropertyToInterface(UI_PKEY_FontProperties, *ppropvarCurrentValue, &pValues);
      if (SUCCEEDED(hr))
      {
        g_pFCSampleAppManager->GetValues(pValues);

        // Provide the new values to the font control.
        hr = UIInitPropertyFromInterface(UI_PKEY_FontProperties, pValues, ppropvarNewValue);
        pValues->Release();
      }
    }
  }

  return hr;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows 功能區架構控制項程式庫](windowsribbon-controls-entry.md)
</dt> <dt>

[**FontControl 元素**](windowsribbon-element-fontcontrol.md)
</dt> <dt>

[字型控制項屬性](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[FontControl 範例](windowsribbon-fontcontrolsample.md)
</dt> </dl>

 


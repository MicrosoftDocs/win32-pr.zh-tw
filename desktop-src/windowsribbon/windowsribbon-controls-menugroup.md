---
title: 功能表群組
description: 功能表群組會在功能表或工具列中組織相關的命令和控制項。
ms.assetid: 5454f2a3-275b-47f4-ae97-d10dd12da5ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9862e78cbedf84b92c7540bec4de58288af5c9ef
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933506"
---
# <a name="menu-group"></a>功能表群組

功能表群組會在功能表或工具列中組織相關的命令和控制項。

-   [簡介](#introduction)
-   [功能表群組屬性](#menu-group-properties)
-   [相關主題](#related-topics)

## <a name="introduction"></a>簡介

透過 [**MenuGroup**](windowsribbon-element-menugroup.md) 標記專案公開的功能表群組控制項，是以功能表為基礎之控制項中的專案或命令群組的邏輯容器，包括 [內容快捷](windowsribbon-controls-contextpopup.md) 功能表迷你工具列。

您可以透過相關聯命令宣告的 *LabelTitle* 屬性或 [**LabelTitle**](windowsribbon-element-command-labeltitle.md) 屬性，為功能表群組指定標籤。 指派給 *LabelTitle* 的值會轉譯為分類標頭。

下列範例會示範 [分割按鈕](windowsribbon-controls-splitbutton.md) 控制項的命令標記，其中包含兩個功能表群組命令聲明。


```XML
<!-- SplitButton -->
<Command Name="cmdSplitButtonGroup"
         Symbol="cmdSplitButtonGroup"
         Comment="SplitButton Group"
         LabelTitle="SplitButton"/>
<Command Name="cmdSplitButton"
         Symbol="cmdSplitButton"
         Comment="SplitButton"
         LabelTitle="SplitButton"/>
<Command Name="cmdSBButtonItem"
         Symbol="cmdSBButtonItem"
         Comment="SBButtonItem"
         LabelTitle="SB ButtonItem"/>
<Command Name="cmdSBButton1"
         Symbol="cmdSBButton1"
         Comment="SBButton1"
         LabelTitle="SB Button">
  <Command.LargeImages>
    <Image Source="res/copyL_32.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/copyS_16.bmp"/>
  </Command.SmallImages>
  <Command.LargeHighContrastImages>
    <Image Source="res/copyLHC_32.bmp"/>
  </Command.LargeHighContrastImages>
  <Command.SmallHighContrastImages>
    <Image Source="res/copySHC_16.bmp"/>
  </Command.SmallHighContrastImages>
</Command>
<Command Name="cmdSBMajorItems"
         Comment="Major Items Category"
         LabelTitle="Major Items"/>
<Command Name="cmdSBStandardItems"
         Comment="Standard Items Category"
         LabelTitle="Standard Items"/>
```



下列範例示範具有三個 [**MenuGroup**](windowsribbon-element-menugroup.md)元素宣告的 [**SplitButton**](windowsribbon-element-splitbutton.md)元素所需的標記，其中兩個會與上一個範例中的功能表群組命令相關聯。 **MenuGroup** 元素的 *Class* 屬性可用來指定功能表項目的大小。


```XML
<Group CommandName="cmdSplitButtonGroup">
  <SplitButton CommandName="cmdSplitButton">
    <SplitButton.ButtonItem>
      <Button CommandName="cmdSBButtonItem"/>
    </SplitButton.ButtonItem>
    <SplitButton.MenuGroups>
      <MenuGroup CommandName="cmdSBMajorItems" 
                 Class="MajorItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
      <MenuGroup CommandName="cmdSBStandardItems"
                 Class="StandardItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
      <MenuGroup Class="StandardItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
    </SplitButton.MenuGroups>
  </SplitButton>
</Group>
```



下列螢幕擷取畫面說明功能表 (，其中包含三個功能表群組控制項，) 由上述範例中的標記所產生。

![具有三個功能表群組控制項之功能表的螢幕擷取畫面。](images/controls/menugroup.png)

## <a name="menu-group-properties"></a>功能表群組屬性

功能區架構會針對功能表群組控制項定義 [屬性索引鍵](windowsribbon-reference-properties.md) 的集合。

一般而言，功能區 UI 中的功能表群組屬性會透過呼叫 [**IUIFramework：： InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) 方法來使與控制項相關聯的命令失效，藉此更新。 [**IUICommandHandler：： UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)回呼方法會處理失效事件，並定義屬性更新。

[**IUICommandHandler：： UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)回呼方法未執行，而且應用程式會查詢已更新的屬性值，直到架構需要該屬性為止。 例如，啟用索引標籤時，以及在功能區 UI 中顯示控制項，或顯示工具提示時。

> [!Note]  
> 在某些情況下，可以透過 [**IUIFramework：： GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) 方法抓取屬性，並使用 [**IUIFramework：： SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) 方法進行設定。

 

下表列出與功能表群組控制項相關聯的屬性索引鍵。



| 屬性索引鍵                                                                                     | 備註                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [UI \_ PKEY \_ 已啟用](windowsribbon-reference-properties-uipkey-enabled.md)                       | 支援 [**IUIFramework：： GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) 和 [**IUIFramework：： SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty)。 |
| [UI \_ PKEY \_ 按鍵提示](windowsribbon-reference-properties-uipkey-keytip.md)                         | 只能透過失效進行更新。                                                                                                                                                                                     |
| [UI \_ PKEY \_ 標籤](windowsribbon-reference-properties-uipkey-label.md)                           | 只能透過失效進行更新。                                                                                                                                                                                     |
| [UI \_ PKEY \_ TooltipDescription](windowsribbon-reference-properties-uipkey-tooltipdescription.md) | 只能透過失效進行更新。                                                                                                                                                                                     |
| [UI \_ PKEY \_ TooltipTitle](windowsribbon-reference-properties-uipkey-tooltiptitle.md)             | 只能透過失效進行更新。                                                                                                                                                                                     |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows 功能區架構控制項程式庫](windowsribbon-controls-entry.md)
</dt> <dt>

[**MenuGroup 標記元素**](windowsribbon-element-menugroup.md)
</dt> </dl>

 

 
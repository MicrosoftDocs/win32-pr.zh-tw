---
title: 命令提示屬性
description: 代表控制項的快速鍵提示。
ms.assetid: 214f69ae-dd35-4abf-b294-d898d7802aa6
keywords:
- 命令提示屬性 Windows 功能區
topic_type:
- apiref
api_name:
- Command.Keytip
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ab16b9b8e52094d6cdc85890dfc1cf8af63942c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966141"
---
# <a name="commandkeytip-property"></a>命令提示屬性

代表控制項的快速鍵提示。

## <a name="usage"></a>使用方式

``` syntax
<Command.Keytip>
  child elements
</Command.Keytip>
```

## <a name="attributes"></a>屬性

沒有任何屬性。

## <a name="child-elements"></a>子元素



| 元素                                                   | 描述                                   |
|-----------------------------------------------------------|-----------------------------------------------|
| [**字串**](windowsribbon-element-string.md)<br/> | 最多可能發生一次<br/> <br/> |



## <a name="parent-elements"></a>父元素



| 元素                                                     |
|-------------------------------------------------------------|
| [**命令**](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a>備註

選擇性。

每個 [**命令**](windowsribbon-element-command.md) 元素最多可能會發生一次。

**命令。快速鍵** 可以包含限制為任何 Unicode 字元序列（包括空白字元）的 *xs： string* 類型值。

**命令。** 只有在與索引卷 [標或](windowsribbon-controls-tab.md)[快速存取工具列](windowsribbon-controls-quickaccesstoolbar.md)內的控制項相關聯時，快速鍵才能以數位開頭。

若要顯示對功能區的目前狀態有效的按鍵提示，請按下 ALT 鍵。 下列螢幕擷取畫面顯示在 Windows 7 的 Microsoft 小畫家中顯示的初始或第一個層級按鍵提示。 選取第一個層首鍵提示之後，只會顯示第二層的快速鍵提示。

![microsoft 油漆中適用于 windows 7 的第一層快速鍵提示](images/properties/ui-pkey-label-keytips.png)

**命令。快速鍵** 可作為命令的鍵盤快速鍵，除非該命令是透過功能表項目公開。 在此情況下，架構會忽略 **命令。 Keytip** 值，並改為使用 [**LabelTitle**](windowsribbon-element-command-labeltitle.md) 或 [UI \_ PKEY \_ 標籤](windowsribbon-reference-properties-uipkey-label.md)所指定的字元之前加上符號。 如果未指定 **LabelTitle** 或 UI \_ PKEY 標籤的連字號 \_ ，則不會公開任何快捷方式或鍵盤快速鍵。

如果未提供 **命令提示** 字元的值，則需要 [**字串**](windowsribbon-element-string.md) 子項目。

> [!Note]  
> 如果 **命令提示** 字元同時包含值和 [**字串**](windowsribbon-element-string.md) 子項目，則會優先使用 **字串** 。

 

根據預設，架構會使用下列字母自動產生快速鍵提示：

-   **F** 指派給 [應用程式功能表](windowsribbon-controls-applicationmenu.md)。
-   **Y** 會指派給沒有應用程式所指定之快捷方式的任何命令。
-   **Z** 會指派給每個 [群組](windowsribbon-controls-group.md) 控制項，而且無法自訂。 只有當控制項的 [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) 指定快顯大小選項時，才會顯示群組 **的快捷方式** 。 如需詳細資訊，請參閱 [透過大小定義自訂功能區和調整原則](windowsribbon-templates.md)。

> [!Note]  
> 架構不會保留這些字母。 您可以視需要將每個命令指派給一或多個命令。

 

架構會以下列方式解決 keytip 衝突：

-   如果有一或 [多個](windowsribbon-controls-tab.md) 索引標籤控制項與相同的 keytip 相關聯，則會將一個數位附加至每個 keytip，從1開始，然後依序 (2，3,... ) 針對宣告順序中的每個控制項。 如果有任何索引標籤控制項被指派字母 F 作為按鍵提示，則會指派 [ [應用程式] 功能表](windowsribbon-controls-applicationmenu.md) ，並依所述調整其餘的按鍵提示。
-   當與索引標籤內的單一控制項相關聯 [時，快速鍵](windowsribbon-controls-tab.md)提示 F 對控制項和 [應用程式功能表](windowsribbon-controls-applicationmenu.md)都有效。 預設的應用程式功能表 keytip 不會變更，但會將優先順序提供給 [使用中] 索引標籤上的控制項。
-   如果索引標籤 [中的一](windowsribbon-controls-tab.md) 或多個控制項與相同的按鍵提示相關聯，則架構會自動重構這些控制項的按鍵提示，如先前所述。

> [!Note]  
> 文字色彩的些許變化是用來反白顯示標準功能區執行中重構的快速鍵。 針對已自訂功能區色彩的非標準功能區執行，將會覆寫此架構行為，並以相同的文字色彩顯示所有快速鍵提示。 如需詳細資訊，請參閱 [自訂功能區色彩](ribbon-color.md)。

 

長度上限為未系結。

## <a name="examples"></a>範例

下列範例示範 [**命令**](windowsribbon-element-command.md)專案的標記，以及 **命令提示。**


```XML
<Command>
  <Command.Name>cmdSave</Command.Name>
  <Command.Symbol>ID_FILE_SAVE</Command.Symbol>
  <Command.Comment>Save</Command.Comment>
  <Command.Id>25003</Command.Id>
  <Command.LabelTitle>
    <String>
      <String.Content>Label for Save</String.Content>
      <String.Id>59999</String.Id>
      <String.Symbol>strSave</String.Symbol>
    </String>
  </Command.LabelTitle>
  <Command.TooltipTitle>Tooltip title with &amp;&amp; for Save Command</Command.TooltipTitle>
  <Command.TooltipDescription>Tooltip description for Save Command.</Command.TooltipDescription>
  <Command.Keytip>s1</Command.Keytip>
</Command>
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[UI \_ PKEY \_ 按鍵提示](windowsribbon-reference-properties-uipkey-keytip.md)
</dt> </dl>

 

 






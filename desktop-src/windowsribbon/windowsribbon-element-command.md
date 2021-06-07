---
title: Command 元素
description: 表示命令定義。
ms.assetid: f332423d-d258-488d-9233-71687288b462
keywords:
- 命令元素視窗功能區
topic_type:
- apiref
api_name:
- Command
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1e1df5b62c7b2d7c55345ba8d6da366d04697054
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443479"
---
# <a name="command-element"></a>Command 元素

表示命令定義。

## <a name="usage"></a>使用方式

``` syntax
<Command
  Name = "xs:string"
  Symbol = "xs:string"
  Id = "xs:positiveInteger union xs:string"
  Comment = "xs:string"
  LabelTitle = "xs:string"
  LabelDescription = "xs:string"
  TooltipTitle = "xs:string"
  TooltipDescription = "xs:string"
  Keytip = "xs:string">
  child elements
</Command>
```

## <a name="attributes"></a>屬性



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>屬性</th>
<th>類型</th>
<th>必要</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>註解</strong><br/></td>
<td>xs:string<br/></td>
<td>否<br/></td>
<td>用來批註命令元素。<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs： string) <br/> </dt> <dd> 由任何字元序列組成的字串，包括空白字元和分行符號字元。<br/> 最大長度：250個字元。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>識別碼</strong><br/></td>
<td>xs： positiveInteger union xs： string<br/></td>
<td>否<br/></td>
<td>唯一的資源識別碼。 <br/> <br/>
<dt><span></span><span></span><strong></strong> (xs： positiveInteger 和 xs： string 的聯集) <br/> </dt> <dd> 介於2和59999（含）之間的整數值，或以十六進位（含）表示的0xea5f。 <br/> 最大長度為10個字元，包括選擇性前置零。 <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>Keytip</strong><br/></td>
<td>xs:string<br/></td>
<td>否<br/></td>
<td>字串，表示 command 元素的鍵盤快速鍵。<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs： string) <br/> </dt> <dd> 由任何字元序列組成的字串，包含空白字元。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>LabelDescription</strong><br/></td>
<td>xs:string<br/></td>
<td>否<br/></td>
<td>字串，表示命令元素上顯示的文字。<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs： string) <br/> </dt> <dd> 由任何字元序列組成的字串，包括空白字元和分行符號字元。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>LabelTitle</strong><br/></td>
<td>xs:string<br/></td>
<td>否<br/></td>
<td>字串，表示命令元素上顯示的文字。<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs： string) <br/> </dt> <dd> 由任何字元序列組成的字串，包括空白字元和分行符號字元。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>名稱</strong><br/></td>
<td>xs:string<br/></td>
<td>否<br/></td>
<td><dt><span></span><span></span><strong></strong> (xs： string) <br/> </dt> <dd> 包含字母或底線的字串，後面接著任何數位、字母或底線序列。<br/> 最大長度：100個字元。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>符號</strong><br/></td>
<td>xs:string<br/></td>
<td>否<br/></td>
<td><dt><span></span><span></span><strong></strong> (xs： string) <br/> </dt> <dd> 包含字母或底線的字串，後面接著任何數位、字母或底線序列。<br/> 最大長度：100個字元。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>TooltipDescription</strong><br/></td>
<td>xs:string<br/></td>
<td>否<br/></td>
<td>字串，表示命令元素上顯示的文字。<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs： string) <br/> </dt> <dd> 由任何字元序列組成的字串，包括空白字元和分行符號字元。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>TooltipTitle</strong><br/></td>
<td>xs:string<br/></td>
<td>否<br/></td>
<td>字串，表示命令元素上顯示的文字。<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs： string) <br/> </dt> <dd> 由任何字元序列組成的字串，包括空白字元和分行符號字元。<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>子元素



| 元素                                                                                                     | 描述                                   |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| [**命令。批註**](windowsribbon-element-command-comment.md)<br/>                                 | 最多可能發生一次<br/> <br/> |
| [**Command.Id**](windowsribbon-element-command-id.md)<br/>                                           | 最多可能發生一次<br/> <br/> |
| [**命令。快速鍵**](windowsribbon-element-command-keytip.md)<br/>                                   | 最多可能發生一次<br/> <br/> |
| [**LabelDescription**](windowsribbon-element-command-labeldescription.md)<br/>               | 最多可能發生一次<br/> <br/> |
| [**LabelTitle**](windowsribbon-element-command-labeltitle.md)<br/>                           | 最多可能發生一次<br/> <br/> |
| [**LargeHighContrastImages**](windowsribbon-element-command-largehighcontrastimages.md)<br/> | 最多可能發生一次<br/> <br/> |
| [**LargeImages**](windowsribbon-element-command-largeimages.md)<br/>                         | 最多可能發生一次<br/> <br/> |
| [**Command.Name**](windowsribbon-element-command-name.md)<br/>                                       | 最多可能發生一次<br/> <br/> |
| [**SmallHighContrastImages**](windowsribbon-element-command-smallhighcontrastimages.md)<br/> | 最多可能發生一次<br/> <br/> |
| [**SmallImages**](windowsribbon-element-command-smallimages.md)<br/>                         | 最多可能發生一次<br/> <br/> |
| [**命令。符號**](windowsribbon-element-command-symbol.md)<br/>                                   | 最多可能發生一次<br/> <br/> |
| [**TooltipDescription**](windowsribbon-element-command-tooltipdescription.md)<br/>           | 最多可能發生一次<br/> <br/> |
| [**TooltipTitle**](windowsribbon-element-command-tooltiptitle.md)<br/>                       | 最多可能發生一次<br/> <br/> |



## <a name="parent-elements"></a>父元素



| 元素                                                                               |
|---------------------------------------------------------------------------------------|
| [**應用程式。命令**](windowsribbon-element-application-commands.md)<br/> |



## <a name="remarks"></a>備註

必要。

每個應用程式都可能會發生一次或多次 [**。命令**](windowsribbon-element-application-commands.md) 元素。

**Command** 元素的子項目可能會以任何順序出現。

通常，命令資源是在功能區標記中宣告，但也可以在執行時間透過呼叫 [**SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty)來設定。 例如，您可以設定命令的 [UI \_ PKEY \_ Keytip](windowsribbon-reference-properties-uipkey-keytip.md) 屬性，而不是使用 [**命令提示**](windowsribbon-element-command-keytip.md) 專案專案在標記中宣告值。

如果無法使用 [**SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) 設定命令屬性，例如標籤和影像，它們可能會在呼叫 [**InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand)時失效。 在失效之後，架構會查詢主機應用程式中的資源詳細資料。

> [!Note]  
> 無法從標記資源資料表復原資源，之後便無法復原。

 

在標記中宣告的每個 **命令** 的功能區標記標頭檔中，都會加入一個命令定義。

*快速鍵* 的值會作為命令的鍵盤快速鍵，除非該命令是透過功能表項目公開。 在這種情況下，架構會忽略 *Keytip* 值，並改為使用 *LabelTitle* 或 [UI \_ PKEY \_ 標籤](windowsribbon-reference-properties-uipkey-label.md)所指定的符號前面加上連字號。 如果 *LabelTitle* 或 UI PKEY 標籤未指定任何 & 符號 \_ \_ ，則不會公開任何快捷方式或鍵盤快速鍵。

## <a name="examples"></a>範例

下列範例顯示 [**首頁**] 索引標籤的 **命令** 專案資訊清單。


```XML
<Application.Commands>
```




```XML
<Command Name="cmdHomeTab"
         LabelTitle="Home"
         Keytip="H" />
<Command Name="cmdClipboardGroup"
         Symbol="IDR_CMD_CLIPBOARD"
         Id="10000"
         Comment="Command definition for clipboard group"
         LabelTitle="Clipboard"
         Keytip="CB" />
<Command Name="cmdCopy"
         Symbol="IDR_CMD_COPY"
         LabelTitle="Copy"
         LabelDescription="Copy"
         Keytip="C"
         TooltipTitle="Copy"
         TooltipDescription="Click to copy">
  <Command.SmallImages>
    <Image>res/copyS_16.bmp</Image>
  </Command.SmallImages>
  <Command.LargeImages>
    <Image>res/copyL_32.bmp</Image>
  </Command.LargeImages>
</Command>
<Command Name="cmdPaste"
         Symbol="IDR_CMD_PASTE" >
  <Command.LabelTitle>Paste</Command.LabelTitle>
  <Command.LabelDescription>
    <String Content="Paste contents of clipboard"
            Id="10001"
            Symbol="IDR_RES_LABELDESC_PASTE" />
  </Command.LabelDescription>
  <Command.Keytip>P</Command.Keytip>
  <Command.TooltipTitle>
    <String Content="Paste contents of clipboard"
            Id="10002"
            Symbol="IDR_RES_TOOLTIP_PASTE"/>
  </Command.TooltipTitle>
  <Command.TooltipDescription>
    <String Content="Click to paste contents of clipboard"/>
  </Command.TooltipDescription>
  <Command.SmallImages>
    <Image
      Id="10010"
      MinDPI="96"
      Symbol="IDR_RES_SMALL_IMAGE96">
      <Image.Source>res/pasteS_96bpp.bmp</Image.Source>
    </Image>
    <Image Source="res/pasteS_120bpp.bmp"
           Id="10011"
           MinDPI="120"
           Symbol="IDR_RES_SMALL_IMAGE120" />
  </Command.SmallImages>
  <Command.LargeImages>
    <Image>res/pasteL_32.bmp</Image>
  </Command.LargeImages>
</Command>
<Command Name="cmdMinimize"
         Symbol="IDR_CMD_MINIMIZE"
         Id="10001"
         LabelTitle="Minimize" />
```




```XML
</Application.Commands>
```



## <a name="element-information"></a>項目資訊

* **最低支援系統**： Windows 7
* **可以是空** 的：否



 


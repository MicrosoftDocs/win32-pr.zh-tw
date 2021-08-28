---
title: Tab 項目
description: 代表核心或內容索引標籤。
ms.assetid: 2e73a89c-4d31-4075-93c8-e43213a20791
keywords:
- Tab 元素 Windows 功能區
topic_type:
- apiref
api_name:
- Tab
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 349004f65713160acc75bdb6f77765ad9f0c3034
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2021
ms.locfileid: "122625954"
---
# <a name="tab-element"></a>Tab 項目

代表[核心](windowsribbon-controls-tab.md)[或內容](windowsribbon-controls-tabgroup.md)索引標籤。

## <a name="usage"></a>使用方式

``` syntax
<Tab
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string">
  child elements
</Tab>
```

## <a name="attributes"></a>屬性



<table>
<colgroup>
<col  />
<col  />
<col  />
<col  />
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
<td><strong>ApplicationModes</strong><br/></td>
<td>xs:string<br/></td>
<td>否<br/></td>
<td>只有在 <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> 是父元素時才有效。<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs： string) <br/> </dt> <dd> 字串，其中包含0到31之間的整數清單（以逗號分隔）。<br/> 空白字元是有效的，而且會被忽略。<br/> 最大長度：250個字元。 <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>CommandName</strong><br/></td>
<td>xs： positiveInteger 或 xs： string<br/></td>
<td>否<br/></td>
<td>將元素與 <a href="windowsribbon-element-command.md"><strong>命令</strong></a>產生關聯。<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs： positiveInteger 或 xs： string) <br/> </dt> <dd> 字串、介於2與59999（含）之間的整數值，或介於0x2 與0xea5f （含）之間的十六進位值。 <br/> 值在功能區 XML 檔中必須是唯一的。 <br/> 最大長度：100個字元。 <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>子元素



| 元素                                                                         | 描述                                        |
|---------------------------------------------------------------------------------|----------------------------------------------------|
| [**組**](windowsribbon-element-group.md)<br/>                         | 可能會發生一次或多次<br/> <br/> |
| [**ScalingPolicy**](windowsribbon-element-tab-scalingpolicy.md)<br/> | 最多可能發生一次<br/> <br/>      |



## <a name="parent-elements"></a>父元素



| 元素                                                             |
|---------------------------------------------------------------------|
| [**功能區] 索引標籤**](windowsribbon-element-ribbon-tabs.md)<br/> |
| [**TabGroup**](windowsribbon-element-tabgroup.md)<br/>       |



## <a name="remarks"></a>備註

必要。

每個功能區都必須至少出現一次 [**。 tab**](windowsribbon-element-ribbon-tabs.md) 或 [**TabGroup**](windowsribbon-element-tabgroup.md) 元素。

**Tab** 支援 [應用程式模式](ribbon-applicationmodes.md)。

如果索引卷 **標元素有** [**ScalingPolicy IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) ，則 **ScalingPolicy. IdealSizes** 下需要每個 [**群組**](windowsribbon-element-group.md)元素的專案及其理想的大小。

## <a name="examples"></a>範例

下列範例將示範 **Tab** 元素的基本標記。

這一段程式碼會顯示 [**常用] 索引** 標籤的 [索引標籤命令聲明 **]** 。


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



這段程式碼會顯示 **選項卡** 控制項宣告。


```XML
<Tab CommandName="cmdHomeTab">
  <Group CommandName="cmdClipboardGroup" 
         SizeDefinition="ThreeButtons">
    <Button CommandName="cmdCopy"/>
    <Button CommandName="cmdPaste"/>
    <ToggleButton CommandName="cmdMinimize"/>
  </Group>
</Tab>
```



## <a name="element-information"></a>項目資訊

- **最低支援系統**： Windows 7 
- **可以是空** 的：否



## <a name="see-also"></a>另請參閱

<dl> <dt>

[索引標籤控制項](windowsribbon-controls-tab.md)
</dt> <dt>

[Tab 群組控制項](windowsribbon-controls-tabgroup.md)
</dt> <dt>

[**SetModes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> </dl>

 


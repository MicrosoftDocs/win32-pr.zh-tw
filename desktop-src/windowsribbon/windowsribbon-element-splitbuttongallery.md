---
title: SplitButtonGallery 元素
description: 表示含有以圖庫為基礎之下拉式功能表的分割按鈕資源庫控制項。
ms.assetid: 65b6af50-6d9a-4285-b2d9-26dfb904d0b8
keywords:
- SplitButtonGallery 元素 Windows 功能區
topic_type:
- apiref
api_name:
- SplitButtonGallery
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c28c2f87a1d8fb165f02ad71c96b38bcbb381bb3590bd9bff98b3feb364044bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117850810"
---
# <a name="splitbuttongallery-element"></a>SplitButtonGallery 元素

表示含有以圖庫為基礎之下拉式功能表的 [分割按鈕資源庫](windowsribbon-controls-splitbuttongallery.md) 控制項。

## <a name="usage"></a>使用方式

``` syntax
<SplitButtonGallery
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string"
  HasLargeItems = "Boolean"
  ItemHeight = "xs:integer"
  ItemWidth = "xs:integer"
  TextPosition = "TextPositionType"
  Type = "xs:string">
  child elements
</SplitButtonGallery>
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
<td><strong>ApplicationModes</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td>只有在 <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> 是父元素時才有效。<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs： string) <br/> </dt> <dd> 字串，其中包含0到31之間的整數清單（以逗號分隔）。<br/> 空白字元是有效的，而且會被忽略。<br/> 最大長度：250個字元。 <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>CommandName</strong><br/></td>
<td>xs： positiveInteger 或 xs： string<br/></td>
<td>No<br/></td>
<td>將元素與 <a href="windowsribbon-element-command.md"><strong>命令</strong></a>產生關聯。<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs： positiveInteger 或 xs： string) <br/> </dt> <dd> 字串、介於2與59999（含）之間的整數值，或介於0x2 與0xea5f （含）之間的十六進位值。 <br/> 值在功能區 XML 檔中必須是唯一的。 <br/> 最大長度：100個字元。 <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>HasLargeItems</strong><br/></td>
<td>Boolean<br/></td>
<td>No<br/></td>
<td>決定是否要在資源庫控制項中顯示命令的大型或小型影像資源。 <br/>
<blockquote>
[!Note]<br />
僅適用于 <em>Type</em> 屬性值等於的資源庫 <code>Command</code> 。
</blockquote>
<br/> 限制為下列其中一個值 (0 和1不是有效的) ：<br/> <br/>
<dt><span></span><span></span><strong></strong> (true) <br/> </dt> <dd> 預設值。 <br/> </dd> <dt><span></span><span></span><strong></strong> (false) <br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><strong>ItemHeight</strong><br/></td>
<td>xs:integer<br/></td>
<td>No<br/></td>
<td><dt><span></span><span></span><strong></strong> (xs： integer) <br/> </dt> <dd> 預設值為 -1。 <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>ItemWidth</strong><br/></td>
<td>xs:integer<br/></td>
<td>No<br/></td>
<td><dt><span></span><span></span><strong></strong> (xs： integer) <br/> </dt> <dd> 預設值為 -1。 <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>TextPosition</strong><br/></td>
<td>TextPositionType<br/></td>
<td>No<br/></td>
<td>限制為下列其中一個值：<br/> <br/>
<dt><span></span><span></span><strong></strong> (底部) <br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> (隱藏) <br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> (左) <br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> (重迭) <br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> (右) <br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> (Top) <br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>類型</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td>限制為下列其中一個值：<br/> <br/>
<dt><span></span><span></span><strong></strong> (專案) <br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> (命令) <br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>子元素



| 元素                                                                                                 | 描述                                        |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| [**Button**](windowsribbon-element-button.md)<br/>                                               | 可能會發生一次或多次<br/> <br/> |
| [**CheckBox**](windowsribbon-element-checkbox.md)<br/>                                           | 可能會發生一次或多次<br/> <br/> |
| [**SplitButton**](windowsribbon-element-splitbutton.md)<br/>                                     | 可能會發生一次或多次<br/> <br/> |
| [**SplitButtonGallery.MenuGroups**](windowsribbon-element-splitbuttongallery-menugroups.md)<br/> | 必須剛好發生一次<br/> <br/>     |
| [**SplitButtonGallery.MenuLayout**](windowsribbon-element-splitbuttongallery-menulayout.md)<br/> | 最多可能發生一次<br/> <br/>      |
| [**ToggleButton**](windowsribbon-element-togglebutton.md)<br/>                                   | 可能會發生一次或多次<br/> <br/> |



## <a name="parent-elements"></a>父元素



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>元素</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="windowsribbon-element-controlgroup.md"><strong>ControlGroup</strong></a><br/></td>

</tr>
<tr class="even">
<td><a href="windowsribbon-element-group.md"><strong>Group</strong></a><br/></td>

</tr>
<tr class="odd">
<td><a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a><br/></td>
<td>包含在 <a href="windowsribbon-element-applicationmenu.md"><strong>ApplicationMenu</strong></a>中的。 只有第一個層級才支援這個元素，而且必須沒有任何子項目。<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar. s</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Windows 8 和更新版本。
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-element-splitbutton.md"><strong>SplitButton</strong></a><br/></td>

</tr>
</tbody>
</table>



## <a name="remarks"></a>備註

選擇性。

每個 [**ControlGroup**](windowsribbon-element-controlgroup.md)、 [**Group**](windowsribbon-element-group.md)、 [**MenuGroup**](windowsribbon-element-menugroup.md)或 [**SplitButton**](windowsribbon-element-splitbutton.md) 元素可能會發生一次或多次。

**SplitButtonGallery** 支援 [應用程式模式](ribbon-applicationmodes.md)。

[UI \_PKEY \_ BooleanValue](windowsribbon-reference-properties-uipkey-booleanvalue.md) 是由應用程式用來查詢 **SplitButtonGallery** 按鈕控制項的切換狀態。

下列螢幕擷取畫面說明 Windows 7 的 Microsoft 小畫家中的功能區[分割按鈕資源庫](windowsribbon-controls-splitbuttongallery.md)控制項。

![適用于 windows 7 的 microsoft 油漆中分割按鈕圖庫控制項的螢幕擷取畫面。](images/controls/splitbuttongallery.png)

## <a name="examples"></a>範例

下列範例示範 [分割按鈕圖庫](windowsribbon-controls-splitbuttongallery.md)的基本標記。

這段程式碼會顯示 **SplitButtonGallery** 命令宣告，以及可作為 **SplitButtonGallery** 元素之父容器的相關聯 [**群組**](windowsribbon-element-group.md)。


```XML
<!-- SplitButtonGallery -->
<Command Name="cmdSplitButtonGalleryGroup"
         Symbol="cmdSplitButtonGalleryGroup"
         Comment="SplitButtonGallery Group"
         LabelTitle="SplitButtonGallery"/>
<Command Name="cmdSplitButtonGallery"
         Symbol="cmdSplitButtonGallery"
         Comment="SplitButtonGallery"
         LabelTitle="SplitButtonGallery"/>
```



這段程式碼會顯示 **SplitButtonGallery** 控制項宣告。


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



## <a name="element-information"></a>項目資訊


- **最低支援系統**： Windows 7 
- **可以是空** 的：否



## <a name="see-also"></a>另請參閱

<dl> <dt>

[分割按鈕資源庫控制項](windowsribbon-controls-splitbuttongallery.md)
</dt> <dt>

[使用資源庫](ribbon-controls-galleries.md)
</dt> <dt>

[**SetModes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> <dt>

[資源庫範例](windowsribbon-gallerysample.md)
</dt> </dl>

 


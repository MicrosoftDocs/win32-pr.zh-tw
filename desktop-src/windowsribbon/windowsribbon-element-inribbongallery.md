---
title: InRibbonGallery 元素
description: 代表 In-Ribbon 資源庫，此為資源庫型控制項，可直接在功能區中公開專案的預設子集。 按一下下拉式功能表按鈕時，會顯示任何剩餘的專案。
ms.assetid: 07d035e2-e6db-49fa-b786-a37cbceb58f6
keywords:
- InRibbonGallery 元素視窗功能區
topic_type:
- apiref
api_name:
- InRibbonGallery
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a25b2ebb937d954adce58231fd8c6b3347a031a7
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443369"
---
# <a name="inribbongallery-element"></a>InRibbonGallery 元素

代表 [功能區元件庫](windowsribbon-controls-inribbongallery.md)，此為資源庫型控制項，可直接在功能區中公開專案的預設子集。 按一下下拉式功能表按鈕時，會顯示任何剩餘的專案。

## <a name="usage"></a>使用方式

``` syntax
<InRibbonGallery
  CommandName = "xs:positiveInteger or xs:string"
  HasLargeItems = "Boolean"
  ItemHeight = "xs:integer"
  ItemWidth = "xs:integer"
  MinColumnsLarge = "xs:integer"
  MaxColumnsMedium = "xs:integer"
  MinColumnsMedium = "xs:integer"
  MaxColumns = "xs:integer"
  MaxRows = "xs:integer"
  TextPosition = "TextPositionType"
  Type = "xs:string">
  child elements
</InRibbonGallery>
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
<td><strong>CommandName</strong><br/></td>
<td>xs： positiveInteger 或 xs： string<br/></td>
<td>否<br/></td>
<td>將元素與 <a href="windowsribbon-element-command.md"><strong>命令</strong></a>產生關聯。<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs： positiveInteger 或 xs： string) <br/> </dt> <dd> 字串、介於2與59999（含）之間的整數值，或介於0x2 與0xea5f （含）之間的十六進位值。 <br/> 值在功能區 XML 檔中必須是唯一的。 <br/> 最大長度：100個字元。 <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>HasLargeItems</strong><br/></td>
<td>Boolean<br/></td>
<td>否<br/></td>
<td>決定是否要在資源庫控制項中顯示命令的大型或小型影像資源。 <br/>
<blockquote>
[!Note]<br />
僅適用于 <em>Type</em> 屬性值等於的資源庫 <code>Command</code> 。
</blockquote>
<br/> 限制為下列其中一個值 (0 和1不是有效的) ：<br/> <br/>
<dt><span></span><span></span><strong></strong> (true) <br/> </dt> <dd> 預設值。 <br/> </dd> <dt><span></span><span></span><strong></strong> (false) <br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>ItemHeight</strong><br/></td>
<td>xs:integer<br/></td>
<td>否<br/></td>
<td>搭配 <em>ItemWidth</em>，可決定在資源庫控制項中顯示之專案影像的大小。 <br/>
<blockquote>
[!Note]<br />
只適用于 <em>類型</em> 屬性值等於的資源庫 <code>Item</code>.
</blockquote>
<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs： integer) <br/> </dt> <dd> 預設值為 -1。 <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>ItemWidth</strong><br/></td>
<td>xs:integer<br/></td>
<td>否<br/></td>
<td>搭配 <em>ItemHeight</em>，可決定在資源庫控制項中顯示之專案影像的大小。 <br/>
<blockquote>
[!Note]<br />
只適用于 <em>類型</em> 屬性值等於的資源庫 <code>Item</code>.
</blockquote>
<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs： integer) <br/> </dt> <dd> 預設值為 -1。 <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>MaxColumns</strong><br/></td>
<td>xs:integer<br/></td>
<td>否<br/></td>
<td>指定 <strong>InRibbonGallery</strong> 所顯示的最大資料行數目，例如，在 [ <em>大型</em> 群組版面配置] 下拉式清單中。<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs： integer) <br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><strong>MaxColumnsMedium</strong><br/></td>
<td>xs:integer<br/></td>
<td>否<br/></td>
<td>指定在切換至<em>大型</em>版面配置之前， <strong>InRibbonGallery</strong>顯示在<em>中等</em>群組配置中的最大資料行數目。 <br/> <br/>
<dt><span></span><span></span><strong></strong> (xs： integer) <br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>MaxRows</strong><br/></td>
<td>xs:integer<br/></td>
<td>否<br/></td>
<td>指定 <strong>InRibbonGallery</strong> 專案版面配置的最大資料列數。 <br/> <br/>
<dt><span></span><span></span><strong></strong> (xs： integer) <br/> </dt> <dd> 預設值是 1。 <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>MinColumnsLarge</strong><br/></td>
<td>xs:integer<br/></td>
<td>否<br/></td>
<td>在切換至<em>媒體</em>之前，指定<strong>InRibbonGallery</strong>在<em>大型</em>群組配置中顯示的最小資料行數目。<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs： integer) <br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>MinColumnsMedium</strong><br/></td>
<td>xs:integer<br/></td>
<td>否<br/></td>
<td>指定 <strong>InRibbonGallery</strong> 在 <em>中等</em> 群組配置中顯示的最小資料行數目，然後切換為 <em>小型</em>。<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs： integer) <br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><strong>TextPosition</strong><br/></td>
<td>TextPositionType<br/></td>
<td>否<br/></td>
<td>指定專案標籤顯示的位置（相對於影像）。 <br/> 限制為下列其中一個值：<br/> <br/>
<dt><span></span><span></span><strong></strong> (底部) <br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> (隱藏) <br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> (左) <br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> (重迭) <br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> (右) <br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> (Top) <br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>類型</strong><br/></td>
<td>xs:string<br/></td>
<td>否<br/></td>
<td>限制為下列其中一個值：<br/> <br/>
<dt><span></span><span></span><strong></strong> (專案) <br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> (命令) <br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>子元素



| 元素                                                                                           | 描述                                        |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------|
| [**相應**](windowsribbon-element-checkbox.md)<br/>                                     | 可能會發生一次或多次<br/> <br/> |
| [**InRibbonGallery.MenuGroups**](windowsribbon-element-inribbongallery-menugroups.md)<br/> | 必須剛好發生一次<br/> <br/>     |
| [**InRibbonGallery.MenuLayout**](windowsribbon-element-inribbongallery-menulayout.md)<br/> | 最多可能發生一次<br/> <br/>      |
| [**按鈕**](windowsribbon-element-button.md)<br/>                                       | 可能會發生一次或多次<br/> <br/> |
| [**SplitButton**](windowsribbon-element-splitbutton.md)<br/>                               | 可能會發生一次或多次<br/> <br/> |
| [**ToggleButton**](windowsribbon-element-togglebutton.md)<br/>                             | 可能會發生一次或多次<br/> <br/> |



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
<td><a href="windowsribbon-element-group.md"><strong>群組</strong></a><br/></td>

</tr>
<tr class="odd">
<td><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar. s</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Windows 8 和更新版本。
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>備註

選擇性。

每個 [**ControlGroup**](windowsribbon-element-controlgroup.md) 或 [**群組**](windowsribbon-element-group.md) 元素最多可能會發生一次。

下列螢幕擷取畫面說明 Windows 7 Microsoft 小畫家中功能區元件 [庫](windowsribbon-controls-inribbongallery.md) 控制項的功能區。

![microsoft 油漆功能區中功能區資源庫控制項的螢幕擷取畫面。](images/controls/inribbongallery.png)

## <a name="examples"></a>範例

下列範例會示範 [功能區元件庫](windowsribbon-controls-inribbongallery.md)的基本標記。

這段程式碼會顯示 **InRibbonGallery** 命令宣告，以及可做為 **InRibbonGallery** 元素之父容器的相關聯 [**群組**](windowsribbon-element-group.md)。


```XML
<!-- InRibbonGallery -->
<Command Name="cmdInRibbonGalleryGroup"
         Symbol="cmdInRibbonGalleryGroup"
         Comment="InRibbonGallery Group"
         LabelTitle="InRibbonGallery"/>
<Command Name="cmdInRibbonGallery"
         Symbol="cmdInRibbonGallery"
         Comment="InRibbonGallery"
         LabelTitle="InRibbonGallery"/>
```



這段程式碼會顯示 **InRibbonGallery** 控制項宣告。


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



## <a name="element-information"></a>項目資訊


* **最低支援系統**： Windows 7
* **可以是空** 的：否



## <a name="see-also"></a>另請參閱

<dl> <dt>

[功能區資源庫控制項](windowsribbon-controls-inribbongallery.md)
</dt> <dt>

[使用資源庫](ribbon-controls-galleries.md)
</dt> <dt>

[資源庫範例](windowsribbon-gallerysample.md)
</dt> </dl>

 

 






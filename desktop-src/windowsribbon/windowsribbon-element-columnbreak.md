---
title: ColumnBreak 元素
description: 表示自訂 SizeDefinition 版面配置範本中 (可見或隱藏) 的垂直分隔符號。
ms.assetid: 5979d3e6-366b-4c47-810f-90fb8039af8d
keywords:
- ColumnBreak 元素 Windows 功能區
topic_type:
- apiref
api_name:
- ColumnBreak
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: beaf97a34a062b3461cf2101cb436fb1ba131d00e8656186fd434045bdef30bc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119393078"
---
# <a name="columnbreak-element"></a>ColumnBreak 元素

表示自訂 [**SizeDefinition**](windowsribbon-element-sizedefinition.md) 版面配置範本中 (可見或隱藏) 的垂直分隔符號。

## <a name="usage"></a>使用方式

``` syntax
<ColumnBreak
  ShowSeparator = "Boolean"/>
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
<td><strong>ShowSeparator</strong><br/></td>
<td>Boolean<br/></td>
<td>No<br/></td>
<td>限制為下列其中一個值：<br/> <br/>
<dt><span></span><span></span><strong></strong> (true) <br/> </dt> <dd> 預設值。 <br/> </dd> <dt><span></span><span></span><strong></strong> (false) <br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>子元素

沒有任何子項目。

## <a name="parent-elements"></a>父元素



| 元素                                                                             |
|-------------------------------------------------------------------------------------|
| [**GroupSizeDefinition**](windowsribbon-element-groupsizedefinition.md)<br/> |



## <a name="remarks"></a>備註

選擇性。

每個 [**GroupSizeDefinition**](windowsribbon-element-groupsizedefinition.md) 專案可能會發生一次或多次。

## <a name="examples"></a>範例

下列範例示範自訂四按鈕 [**SizeDefinition**](windowsribbon-element-sizedefinition.md)版面配置範本中 **ColumnBreak** 元素的基本標記。 **ColumnBreak** 只會針對 `Large` 範本指定。


```XML
<Group CommandName="cmdButtonGroup2">
  <SizeDefinition>
    <ControlNameMap>
      <ControlNameDefinition Name="button1"/>
      <ControlNameDefinition Name="button2"/>
      <ControlNameDefinition Name="button3"/>
      <ControlNameDefinition Name="button4"/>
    </ControlNameMap>
    <GroupSizeDefinition Size="Large">
      <ControlGroup>
        <ControlSizeDefinition ControlName="button1"
                               ImageSize="Large"
                               IsLabelVisible="true" />
        <ControlSizeDefinition ControlName="button2"
                               ImageSize="Large"
                               IsLabelVisible="true" />
      </ControlGroup>
      <ColumnBreak ShowSeparator="true"/>
      <ControlGroup>
        <ControlSizeDefinition ControlName="button3"
                               ImageSize="Large"
                              IsLabelVisible="true" />
        <ControlSizeDefinition ControlName="button4"
                              ImageSize="Large"
                              IsLabelVisible="true" />
      </ControlGroup>
    </GroupSizeDefinition>
    <GroupSizeDefinition Size="Medium">
      <Row>
        <ControlSizeDefinition ControlName="button1"
                               ImageSize="Small"
                               IsLabelVisible="true" />
        <ControlSizeDefinition ControlName="button3"
                               ImageSize="Small"
                               IsLabelVisible="true" />
      </Row>
      <Row>
        <ControlSizeDefinition ControlName="button2"
                               ImageSize="Small"
                               IsLabelVisible="true" />
        <ControlSizeDefinition ControlName="button4"
                               ImageSize="Small"
                               IsLabelVisible="true" />
      </Row>
    </GroupSizeDefinition>
    <GroupSizeDefinition Size="Small">
      <Row>
        <ControlSizeDefinition ControlName="button1"
                               ImageSize="Small"
                               IsLabelVisible="true" />
        <ControlSizeDefinition ControlName="button3"
                               ImageSize="Small"
                               IsLabelVisible="false" />
      </Row>
      <Row>
        <ControlSizeDefinition ControlName="button2"
                               ImageSize="Small"
                               IsLabelVisible="true" />
        <ControlSizeDefinition ControlName="button4"
                               ImageSize="Small"
                               IsLabelVisible="false" />
      </Row>
    </GroupSizeDefinition>
  </SizeDefinition>
  <Button CommandName="cmdButtonG21"></Button>
  <Button CommandName="cmdButtonG22"></Button>
  <Button CommandName="cmdButtonG23"></Button>
  <Button CommandName="cmdButtonG24"></Button>
</Group>
<Group CommandName="cmdCheckBoxGroup">
  <CheckBox CommandName="cmdCheckBox"></CheckBox>
</Group>
<Group CommandName="cmdToggleButtonGroup"
       SizeDefinition="OneButton">
  <ToggleButton CommandName="cmdToggleButton"></ToggleButton>
</Group>
<Group CommandName="cmdButtonGroup"
       SizeDefinition="ThreeButtons">
  <Button CommandName="cmdButton1"></Button>
  <Button CommandName="cmdButton2"></Button>
  <Button CommandName="cmdButton3"></Button>
</Group>
```



## <a name="element-information"></a>項目資訊

* **最低支援系統**： Windows 7
* **可以是空** 的：是



## <a name="see-also"></a>另請參閱

<dl> <dt>

[透過大小定義和調整原則自訂功能區](windowsribbon-templates.md)
</dt> </dl>

 

 






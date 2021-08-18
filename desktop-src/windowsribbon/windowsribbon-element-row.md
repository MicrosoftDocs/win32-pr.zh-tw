---
title: Row 元素
description: 代表自訂 SizeDefinition 版面配置範本中的一列控制項。
ms.assetid: c3dac35f-3537-4eb7-b378-501ea88813f5
keywords:
- Windows 功能區的 Row 元素
topic_type:
- apiref
api_name:
- Row
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d59913d8a733e4186f2c00e35431d68ebdea839e67103a46873e6f3f64f3a72b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119449558"
---
# <a name="row-element"></a>Row 元素

代表自訂 SizeDefinition 版面配置範本中的一列控制項。

## <a name="usage"></a>使用量

``` syntax
<Row>
  child elements
</Row>
```

## <a name="attributes"></a>屬性

沒有任何屬性。

## <a name="child-elements"></a>子元素



| 元素                                                                                 | 描述                                        |
|-----------------------------------------------------------------------------------------|----------------------------------------------------|
| [**ControlGroup**](windowsribbon-element-controlgroup.md)<br/>                   | 可能會發生一次或多次<br/> <br/> |
| [**ControlSizeDefinition**](windowsribbon-element-controlsizedefinition.md)<br/> | 可能會發生一次或多次<br/> <br/> |



## <a name="parent-elements"></a>父元素



| 元素                                                                             |
|-------------------------------------------------------------------------------------|
| [**GroupSizeDefinition**](windowsribbon-element-groupsizedefinition.md)<br/> |



## <a name="remarks"></a>備註

選擇性。

每個 [**GroupSizeDefinition**](windowsribbon-element-groupsizedefinition.md) 專案可能會發生一次或多次。

## <a name="examples"></a>範例

下列程式碼範例將示範具有各種資料 **列** 元素之自訂四按鈕 [**SizeDefinition**](windowsribbon-element-sizedefinition.md)版面配置範本的基本標記。


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
* **可以是空** 的：否



## <a name="see-also"></a>另請參閱

<dl> <dt>

[透過大小定義和調整原則自訂功能區](windowsribbon-templates.md)
</dt> </dl>

 

 






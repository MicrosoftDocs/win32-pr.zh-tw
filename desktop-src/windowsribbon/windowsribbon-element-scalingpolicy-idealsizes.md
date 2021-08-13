---
title: ScalingPolicy. IdealSizes 屬性
description: 代表慣用 SizeDefinition 範本的縮放規格容器（以功能區大小為基礎）。
ms.assetid: a4aa2642-160d-4d81-9df9-29277911aa5a
keywords:
- ScalingPolicy. IdealSizes 屬性 Windows 功能區
topic_type:
- apiref
api_name:
- ScalingPolicy.IdealSizes
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 500f6193411ed72b8858506816d9af4f82b1219680fa0537bf54b3daa7735211
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118439523"
---
# <a name="scalingpolicyidealsizes-property"></a>ScalingPolicy. IdealSizes 屬性

代表慣用 [**SizeDefinition**](windowsribbon-element-sizedefinition.md) 範本的縮放規格容器（以功能區大小為基礎）。

## <a name="usage"></a>使用量

``` syntax
<ScalingPolicy.IdealSizes>
  child elements
</ScalingPolicy.IdealSizes>
```

## <a name="attributes"></a>屬性

沒有任何屬性。

## <a name="child-elements"></a>子元素



| 元素                                                 | 描述                                        |
|---------------------------------------------------------|----------------------------------------------------|
| [**調整**](windowsribbon-element-scale.md)<br/> | 可能會發生一次或多次<br/> <br/> |



## <a name="parent-elements"></a>父元素



| 元素                                                                 |
|-------------------------------------------------------------------------|
| [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md)<br/> |



## <a name="remarks"></a>備註

選擇性。

每個 [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md)最多可能會發生一次。

如果已定義 **ScalingPolicy** ，則必須在索引標籤 [**元素中的每**](windowsribbon-element-tab.md)個 [**群組**](windowsribbon-element-group.md)元素都有一個 [**小**](windowsribbon-element-scale.md)數位數專案。

**ScalingPolicy** 是控制項 [**群組**](windowsribbon-element-group.md)的慣用 [**SizeDefinition**](windowsribbon-element-sizedefinition.md)版面配置。

## <a name="examples"></a>範例

下列範例示範如何透過功能區 [**SizeDefinition**](windowsribbon-element-sizedefinition.md)範本的自我調整配置功能，自訂 [**群組**](windowsribbon-element-group.md)中控制項的外觀。

此範例中的 [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md)資訊清單會針對 [**主** 資料夾] 索引標籤上的四個控制項群組，指定 **ScalingPolicy. IdealSizes** [**SizeDefinition**](windowsribbon-element-sizedefinition.md)喜好設定。此外，也會指定 [**小**](windowsribbon-element-scale.md)數位數元素，以影響每個群組的折迭行為（依遞減大小排序）。


```C++
<Tab CommandName="Home">
  <Tab.ScalingPolicy>
    <ScalingPolicy>
      <ScalingPolicy.IdealSizes>
        <Scale Group="GroupClipboard" Size="Medium"/>
        <Scale Group="GroupView" Size="Large"/>
        <Scale Group="GroupFont" Size="Large"/>
        <Scale Group="GroupParagraph" Size="Large"/>
      </ScalingPolicy.IdealSizes>
      <Scale Group="GroupClipboard" Size="Small"/>
      <Scale Group="GroupClipboard" Size="Popup"/>
      <Scale Group="GroupFont" Size="Medium"/>
      <Scale Group="GroupParagraph" Size="Medium"/>
      <!-- 
        GroupView group is associated with the OneButton SizeDefinition.
        Since this template is constrained to one size (Large) there
        is no need to declare further scaling preferences.
      -->
    </ScalingPolicy>
  </Tab.ScalingPolicy>

  <Group CommandName="GroupClipboard" SizeDefinition="FourButtons">
    <Button CommandName="Paste"/>
    <Button CommandName="Cut"/>
    <Button CommandName="Copy"/>
    <Button CommandName="SelectAll"/>
  </Group>

  <Group CommandName="GroupFont"  ApplicationModes="1">
    <FontControl CommandName="Font" FontType="FontWithColor" />
  </Group>

  <Group CommandName="GroupParagraph"  ApplicationModes="1" SizeDefinition="ButtonGroups">
    <ControlGroup>
      <ControlGroup>
        <ToggleButton CommandName="Numbered" />
        <ToggleButton CommandName="Bulleted" />
      </ControlGroup>
    </ControlGroup>
    <ControlGroup>
      <ControlGroup>
        <ToggleButton CommandName="LeftJustify" />
        <ToggleButton CommandName="CenterJustify" />
        <ToggleButton CommandName="RightJustify" />
      </ControlGroup>
      <ControlGroup/>
      <ControlGroup>
        <Button CommandName="Outdent" />
        <Button CommandName="Indent" />
      </ControlGroup>
    </ControlGroup>
  </Group>

  <Group CommandName="GroupView" SizeDefinition="OneButton" >
    <ToggleButton CommandName="ViewSource"/>
  </Group>

</Tab>
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>              |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[透過大小定義和調整原則自訂功能區](windowsribbon-templates.md)
</dt> </dl>

 

 






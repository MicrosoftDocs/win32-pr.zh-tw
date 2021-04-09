---
title: ScalingPolicy 項目
description: 表示用於調整規格的容器。
ms.assetid: 133e7994-9901-43e8-82b0-3d910cf8758e
keywords:
- ScalingPolicy 元素視窗功能區
topic_type:
- apiref
api_name:
- ScalingPolicy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7f0d0f484ebded1233e3c64f6c7830882395b90a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678735"
---
# <a name="scalingpolicy-element"></a>ScalingPolicy 項目

表示用於調整規格的容器。

## <a name="usage"></a>使用方式

``` syntax
<ScalingPolicy>
  child elements
</ScalingPolicy>
```

## <a name="attributes"></a>屬性

沒有任何屬性。

## <a name="child-elements"></a>子元素



| 元素                                                                                       | 描述                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| [**調整**](windowsribbon-element-scale.md)<br/>                                       | 可能會發生一次或多次<br/> <br/> |
| [**ScalingPolicy. IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md)<br/> | 最多可能發生一次<br/> <br/>      |



## <a name="parent-elements"></a>父元素



| 元素                                                                         |
|---------------------------------------------------------------------------------|
| [**ScalingPolicy**](windowsribbon-element-tab-scalingpolicy.md)<br/> |



## <a name="remarks"></a>備註

必要。

每個 [**ScalingPolicy**](windowsribbon-element-tab-scalingpolicy.md)都必須發生一次。

**ScalingPolicy** 元素包含 [**ScalingPolicy**](windowsribbon-element-scalingpolicy-idealsizes.md)的資訊清單，並在調整大小功能區 [**時，指定**](windowsribbon-element-scale.md)一或多個 [**群組**](windowsribbon-element-group.md)元素的自我調整版面配置喜好設定。

[**調整規模**](windowsribbon-element-scale.md)宣告的清單必須是有效大小的遞減順序， (大型、中型、小型、快顯視窗) 與 [**群組**](windowsribbon-element-group.md)專案相關聯的 [**SizeDefinition**](windowsribbon-element-sizedefinition.md) 。

> [!Note]  
> 強烈建議您指定適當的調整原則詳細資料，讓功能區可以在調整大小為 300 96 圖元的寬度時，不需要捲軸， (DPI) 。

 

## <a name="examples"></a>範例

下列範例示範如何透過功能區 [**SizeDefinition**](windowsribbon-element-sizedefinition.md)範本的自我調整配置功能，自訂 [**群組**](windowsribbon-element-group.md)中控制項的外觀。

此範例中的 **ScalingPolicy** 資訊清單會針對 [**主** 資料夾] 索引標籤上的四個控制項群組，指定 [**ScalingPolicy. IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**SizeDefinition**](windowsribbon-element-sizedefinition.md)喜好設定。此外，也會指定 [**小**](windowsribbon-element-scale.md)數位數元素，以影響每個群組的折迭行為（依遞減大小排序）。


```XML
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



## <a name="element-information"></a>項目資訊



|                                     |           |
|-------------------------------------|-----------|
| 最低支援系統<br/> | Windows 7 |
| 可以是空的                        | 否        |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[透過大小定義和調整原則自訂功能區](windowsribbon-templates.md)
</dt> </dl>

 

 






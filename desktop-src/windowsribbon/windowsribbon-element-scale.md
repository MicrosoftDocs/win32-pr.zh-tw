---
title: Scale 元素
description: 透過群組 SizeDefinition 組，表示一組控制項的大小和配置喜好設定。
ms.assetid: feef3721-c779-4c64-96c6-9d951ac32277
keywords:
- 調整元素 Windows 功能區
topic_type:
- apiref
api_name:
- Scale
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 580cfad910a727f7e4392489adc8cb8baec9a0bc
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2021
ms.locfileid: "122630199"
---
# <a name="scale-element"></a>Scale 元素

透過 {**Group**， [**SizeDefinition**](windowsribbon-element-sizedefinition.md)} 配對，表示一 [**組**](windowsribbon-element-group.md)控制項的大小和配置喜好設定。

## <a name="usage"></a>使用方式

``` syntax
<Scale
  Size = "xs:string"
  Group = "xs:positiveInteger or xs:string"
/>
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
<td><strong>群組</strong><br/></td>
<td>xs： positiveInteger 或 xs： string<br/></td>
<td>是<br/></td>
<td>必須對應至現有的 <a href="windowsribbon-element-group.md"><strong>群組</strong></a> <em>CommandName</em>。<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs： positiveInteger 或 xs： string) <br/> </dt> <dd> 介於2與59999（含）之間的字串或整數值，以及十六進位（含）之間的0xea5f。 <br/> 值在功能區 XML 檔中必須是唯一的。 <br/> 最大長度：100個字元。 <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>大小</strong><br/></td>
<td>xs:string<br/></td>
<td>是<br/></td>
<td>此值應該對應至 [<em>群組</em>] 中指定之相關控制項<a href="windowsribbon-element-group.md"><strong>群組</strong></a>的 [ <em>SizeDefinition</em> ] 屬性的其中一個有效大小。 <br/> 限制為下列其中一個值： <br/> <br/>
<dt><span></span><span></span><strong></strong> (快顯視窗) <br/> </dt> <dd> 相同的控制項版面 <code>Large</code> 配置，但裝載于快顯視窗或下拉式窗格中。<br/> </dd> <dt><span></span><span></span><strong></strong> (Small) <br/> </dt> <dd> Small <a href="windowsribbon-element-sizedefinition.md"><strong>SizeDefinition</strong></a> 範本。<br/> </dd> <dt><span></span><span></span><strong></strong> (中) <br/> </dt> <dd> 中型 <a href="windowsribbon-element-sizedefinition.md"><strong>SizeDefinition</strong></a> 範本。<br/> </dd> <dt><span></span><span></span><strong></strong> (大型) <br/> </dt> <dd> 大型 <a href="windowsribbon-element-sizedefinition.md"><strong>SizeDefinition</strong></a> 範本。<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>子元素

沒有任何子項目。

## <a name="parent-elements"></a>父元素



| 元素                                                                                       |
|-----------------------------------------------------------------------------------------------|
| [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md)<br/>                       |
| [**ScalingPolicy. IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md)<br/> |



## <a name="remarks"></a>備註

選擇性。

每個 [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) 或 ScalingPolicy 可能會發生一次或多次 [**IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md)。

每個 (群組、*大小*) 屬性 *組* 都必須是唯一的。

## <a name="examples"></a>範例

下列範例示範如何透過功能區 [**SizeDefinition**](windowsribbon-element-sizedefinition.md)範本的自我調整配置功能，自訂 [**群組**](windowsribbon-element-group.md)中控制項的外觀。

此範例中的 [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md)資訊清單會針對 [**主** 資料夾] 索引標籤上的四個控制項群組，指定 [**ScalingPolicy. IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**SizeDefinition**](windowsribbon-element-sizedefinition.md)喜好設定。此外，也會指定 **小** 數位數元素，以影響每個群組的折迭行為（依遞減大小排序）。


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



* **最低支援系統**： Windows 7
* **可以是空** 的：是



## <a name="see-also"></a>另請參閱

<dl> <dt>

[透過大小定義和調整原則自訂功能區](windowsribbon-templates.md)
</dt> </dl>

 

 






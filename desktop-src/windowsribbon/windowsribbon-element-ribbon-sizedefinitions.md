---
title: SizeDefinitions 屬性
description: 代表功能區控制項之自訂版面配置範本的容器。
ms.assetid: 1f5fcffc-7f2e-4763-b0a7-4e8f46534da8
keywords:
- SizeDefinitions 屬性視窗功能區
topic_type:
- apiref
api_name:
- Ribbon.SizeDefinitions
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b8ffe5a3339b0f32e493a1f7ddc33789526695e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024678"
---
# <a name="ribbonsizedefinitions-property"></a>SizeDefinitions 屬性

代表功能區控制項之自訂版面配置範本的容器。

## <a name="usage"></a>使用方式

``` syntax
<Ribbon.SizeDefinitions>
  child elements
</Ribbon.SizeDefinitions>
```

## <a name="attributes"></a>屬性

沒有任何屬性。

## <a name="child-elements"></a>子元素



| 元素                                                                   | 描述                                        |
|---------------------------------------------------------------------------|----------------------------------------------------|
| [**SizeDefinition**](windowsribbon-element-sizedefinition.md)<br/> | 可能會發生一次或多次<br/> <br/> |



## <a name="parent-elements"></a>父元素



| 元素                                                   |
|-----------------------------------------------------------|
| [**功能區**](windowsribbon-element-ribbon.md)<br/> |



## <a name="remarks"></a>備註

選擇性。

每個 [**功能區**](windowsribbon-element-ribbon.md)最多可能會發生一次。

## <a name="examples"></a>範例

下列程式碼範例說明基本的自訂範本。


```
<Ribbon.SizeDefinitions>
  <SizeDefinition Name="CustomTemplate">
    <GroupSizeDefinition Size="Large">
      <ControlSizeDefinition ImageSize="Large" IsLabelVisible="true" />
    </GroupSizeDefinition>
    <GroupSizeDefinition Size="Medium">
      <ControlSizeDefinition ImageSize="Small" IsLabelVisible="false" />
    </GroupSizeDefinition>
    <GroupSizeDefinition Size="Small">
      <ControlSizeDefinition ImageSize="Small" IsLabelVisible="false" />
    </GroupSizeDefinition>
  </SizeDefinition>
</Ribbon.SizeDefinitions>
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[透過大小定義和調整原則自訂功能區](windowsribbon-templates.md)
</dt> </dl>

 

 






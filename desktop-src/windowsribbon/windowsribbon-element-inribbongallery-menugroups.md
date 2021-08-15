---
title: InRibbonGallery. MenuGroups 屬性
description: 代表 In-Ribbon 資源庫控制項之下拉式功能表專案集合的容器。
ms.assetid: 6b9ded25-4e8e-4e30-a349-f7c091dbfe7a
keywords:
- InRibbonGallery. MenuGroups 屬性 Windows 功能區
topic_type:
- apiref
api_name:
- InRibbonGallery.MenuGroups
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1722c8963b57256cf74f5911c8273539e10b5c6a6fef96dcfa1f0fec591bca04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119710478"
---
# <a name="inribbongallerymenugroups-property"></a>InRibbonGallery. MenuGroups 屬性

代表 [功能區資源庫控制項中](windowsribbon-controls-inribbongallery.md) ，一組下拉式功能表專案的容器。

## <a name="usage"></a>使用方式

``` syntax
<InRibbonGallery.MenuGroups>
  child elements
</InRibbonGallery.MenuGroups>
```

## <a name="attributes"></a>屬性

沒有任何屬性。

## <a name="child-elements"></a>子元素



| 元素                                                         | 描述                                     |
|-----------------------------------------------------------------|-------------------------------------------------|
| [**MenuGroup**](windowsribbon-element-menugroup.md)<br/> | 至少必須發生一次<br/> <br/> |



## <a name="parent-elements"></a>父元素



| 元素                                                                     |
|-----------------------------------------------------------------------------|
| [**InRibbonGallery**](windowsribbon-element-inribbongallery.md)<br/> |



## <a name="remarks"></a>備註

選擇性。

每個 [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) 元素最多可能會發生一次。

## <a name="examples"></a>範例

下列範例會示範 [功能區資源庫](windowsribbon-controls-inribbongallery.md) 控制項的基本標記。

這段程式碼會顯示 **InRibbonGallery MenuGroups** 控制項宣告。


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



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>              |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[功能區資源庫控制項](windowsribbon-controls-inribbongallery.md)
</dt> <dt>

[使用資源庫](ribbon-controls-galleries.md)
</dt> <dt>

[透過大小定義和調整原則自訂功能區](windowsribbon-templates.md)
</dt> </dl>

 

 






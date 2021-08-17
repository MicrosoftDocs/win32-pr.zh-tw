---
title: DropDownGallery. MenuGroups 屬性
description: 代表 Drop-Down 資源庫控制項中的一組下拉式功能表專案的容器。
ms.assetid: 594f6ae5-760e-456d-98cd-04ecae0bae99
keywords:
- DropDownGallery. MenuGroups 屬性 Windows 功能區
topic_type:
- apiref
api_name:
- DropDownGallery.MenuGroups
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffdc52877884ac3a6407a0c7ed9f511cf78f8bcb5c125beb5f2ed19e651b83da
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119393048"
---
# <a name="dropdowngallerymenugroups-property"></a>DropDownGallery. MenuGroups 屬性

代表下拉式清單資源 [庫](windowsribbon-controls-dropdowngallery.md) 控制項中一組下拉式功能表專案的容器。

## <a name="usage"></a>使用量

``` syntax
<DropDownGallery.MenuGroups>
  child elements
</DropDownGallery.MenuGroups>
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
| [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)<br/> |



## <a name="remarks"></a>備註

必要。

針對每個 [**DropDownGallery**](windowsribbon-element-dropdowngallery.md) 元素，必須剛好一次出現。

## <a name="examples"></a>範例

下列範例示範 **DropDownGallery. MenuGroups** 元素的基本標記。

這段程式碼會在 [下拉式清單庫](windowsribbon-controls-dropdowngallery.md)命令空間中顯示 **DropDownGallery. MenuGroups** 控制項宣告。


```XML
<!-- DropDownGallery -->
<Group CommandName="cmdDropDownGalleryGroup">
  <DropDownGallery CommandName="cmdDropDownGallery"
                   TextPosition="Hide"
                   Type="Commands"
                   ItemHeight="32"
                   ItemWidth="32">
    <DropDownGallery.MenuLayout>
      <FlowMenuLayout Rows="2"
                      Columns="3"
                      Gripper="None"/>
    </DropDownGallery.MenuLayout>
    <DropDownGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
       </MenuGroup>
       <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </DropDownGallery.MenuGroups>
  </DropDownGallery>
</Group>
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>              |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**下拉式圖庫控制項**](windowsribbon-element-dropdowngallery.md)
</dt> <dt>

[使用資源庫](ribbon-controls-galleries.md)
</dt> </dl>

 

 






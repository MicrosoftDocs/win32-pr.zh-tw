---
title: SplitButtonGallery. MenuGroups 屬性
description: 代表 SplitButtonGallery 控制項中一組下拉式功能表專案的容器。
ms.assetid: e30fcf9a-488b-423a-8bc4-fccbc78f74de
keywords:
- SplitButtonGallery. MenuGroups 屬性 Windows 功能區
topic_type:
- apiref
api_name:
- SplitButtonGallery.MenuGroups
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 931a66ffca192a1655f3eeffc405c4c02c8e298c28fe9cb9d0d8c6612e29d793
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119441717"
---
# <a name="splitbuttongallerymenugroups-property"></a>SplitButtonGallery. MenuGroups 屬性

代表 [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) 控制項中一組下拉式功能表專案的容器。

## <a name="usage"></a>使用量

``` syntax
<SplitButtonGallery.MenuGroups>
  child elements
</SplitButtonGallery.MenuGroups>
```

## <a name="attributes"></a>屬性

沒有任何屬性。

## <a name="child-elements"></a>子元素



| 元素                                                         | 描述                                     |
|-----------------------------------------------------------------|-------------------------------------------------|
| [**MenuGroup**](windowsribbon-element-menugroup.md)<br/> | 至少必須發生一次<br/> <br/> |



## <a name="parent-elements"></a>父元素



| 元素                                                                           |
|-----------------------------------------------------------------------------------|
| [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a>備註

必要。

針對每個 [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) 元素，必須剛好一次出現。

## <a name="examples"></a>範例

下列範例示範 **SplitButtonGallery. MenuGroups** 元素的基本標記。

這段程式碼會顯示 **SplitButtonGallery MenuGroups** 控制項宣告。


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



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>              |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[分割按鈕資源庫控制項](windowsribbon-controls-splitbuttongallery.md)
</dt> <dt>

[使用資源庫](ribbon-controls-galleries.md)
</dt> </dl>

 

 






---
title: SplitButtonGallery. MenuLayout 屬性
description: 代表分割按鈕庫下拉式功能表版面配置的容器。
ms.assetid: 4bebdff6-16ea-4cf3-adc7-9b86ea200e81
keywords:
- SplitButtonGallery. MenuLayout 屬性 Windows 功能區
topic_type:
- apiref
api_name:
- SplitButtonGallery.MenuLayout
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04428c14b5e47795da47e5c03970610cd08a6e8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967956"
---
# <a name="splitbuttongallerymenulayout-property"></a>SplitButtonGallery. MenuLayout 屬性

代表 [分割按鈕庫](windowsribbon-controls-splitbuttongallery.md) 下拉式功能表版面配置的容器。

## <a name="usage"></a>使用方式

``` syntax
<SplitButtonGallery.MenuLayout>
  child elements
</SplitButtonGallery.MenuLayout>
```

## <a name="attributes"></a>屬性

沒有任何屬性。

## <a name="child-elements"></a>子元素



| 元素                                                                           | 描述                                    |
|-----------------------------------------------------------------------------------|------------------------------------------------|
| [**FlowMenuLayout**](windowsribbon-element-flowmenulayout.md)<br/>         | 必須剛好發生一次<br/> <br/> |
| [**VerticalMenuLayout**](windowsribbon-element-verticalmenulayout.md)<br/> | 必須剛好發生一次<br/> <br/> |



## <a name="parent-elements"></a>父元素



| 元素                                                                           |
|-----------------------------------------------------------------------------------|
| [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a>備註

選擇性。

每個 [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) 元素最多可能會發生一次。

> [!Note]  
> 最多隻允許一個子項目 ([**VerticalMenuLayout**](windowsribbon-element-verticalmenulayout.md) 或 [**FlowMenuLayout**](windowsribbon-element-flowmenulayout.md)) 。

 

## <a name="examples"></a>範例

下列範例示範 [分割按鈕圖庫](windowsribbon-controls-splitbuttongallery.md)的基本標記。

這段程式碼會顯示 **SplitButtonGallery MenuLayout** 控制項宣告。


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
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[分割按鈕資源庫控制項](windowsribbon-controls-splitbuttongallery.md)
</dt> <dt>

[使用資源庫](ribbon-controls-galleries.md)
</dt> </dl>

 

 






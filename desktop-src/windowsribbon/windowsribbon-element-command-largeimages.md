---
title: LargeImages 屬性
description: 代表影像的容器;在此案例中為大型影像。
ms.assetid: 9fcd3694-7847-43e2-9877-47daf47aae9a
keywords:
- LargeImages 屬性 Windows 功能區
topic_type:
- apiref
api_name:
- Command.LargeImages
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf71557506d4b9cced21069473d1a6db9b208b8c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466584"
---
# <a name="commandlargeimages-property"></a>LargeImages 屬性

代表影像的容器;在此案例中為大型影像。

## <a name="usage"></a>使用方式

``` syntax
<Command.LargeImages>
  child elements
</Command.LargeImages>
```

## <a name="attributes"></a>屬性

沒有任何屬性。

## <a name="child-elements"></a>子元素



| 元素                                                 | 描述                                        |
|---------------------------------------------------------|----------------------------------------------------|
| [**圖像**](windowsribbon-element-image.md)<br/> | 可能會發生一次或多次<br/> <br/> |



## <a name="parent-elements"></a>父元素



| 元素                                                     |
|-------------------------------------------------------------|
| [**命令**](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a>備註

選擇性。

每個 [**命令**](windowsribbon-element-command.md)最多可能會發生一次。

影像資源必須符合 Windows 中所使用的標準點陣圖 (BMP) 圖形格式。

## <a name="examples"></a>範例

下列範例示範具有 [**MenuGroup**](windowsribbon-element-menugroup.md)元素之 [**SplitButton**](windowsribbon-element-splitbutton.md)的基本標記。

這段程式碼會顯示具有大型和小型影像資源的 [**SplitButton**](windowsribbon-element-splitbutton.md) 和 [**MenuGroup**](windowsribbon-element-menugroup.md) 命令宣告。 也會宣告作為 **SplitButton** 專案父容器的相關聯 [**群組**](windowsribbon-element-group.md)。


```XML
<!-- SplitButton -->
<Command Name="cmdSplitButtonGroup"
         Symbol="cmdSplitButtonGroup"
         Comment="SplitButton Group"
         LabelTitle="SplitButton"/>
<Command Name="cmdSplitButton"
         Symbol="cmdSplitButton"
         Comment="SplitButton"
         LabelTitle="SplitButton"/>
<Command Name="cmdSBButtonItem"
         Symbol="cmdSBButtonItem"
         Comment="SBButtonItem"
         LabelTitle="SB ButtonItem"/>
<Command Name="cmdSBButton1"
         Symbol="cmdSBButton1"
         Comment="SBButton1"
         LabelTitle="SB Button">
  <Command.LargeImages>
    <Image Source="res/copyL_32.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/copyS_16.bmp"/>
  </Command.SmallImages>
  <Command.LargeHighContrastImages>
    <Image Source="res/copyLHC_32.bmp"/>
  </Command.LargeHighContrastImages>
  <Command.SmallHighContrastImages>
    <Image Source="res/copySHC_16.bmp"/>
  </Command.SmallHighContrastImages>
</Command>
<Command Name="cmdSBMajorItems"
         Comment="Major Items Category"
         LabelTitle="Major Items"/>
<Command Name="cmdSBStandardItems"
         Comment="Standard Items Category"
         LabelTitle="Standard Items"/>
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[指定功能區影像資源](windowsribbon-imageformats.md)
</dt> <dt>

[UI \_ PKEY \_ LargeImage](windowsribbon-reference-properties-uipkey-largeimage.md)
</dt> </dl>

 

 






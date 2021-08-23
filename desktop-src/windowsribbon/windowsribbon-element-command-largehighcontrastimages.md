---
title: LargeHighContrastImages 屬性
description: 代表影像的容器;在此情況下，用於高對比系統設定的大型映射。
ms.assetid: e25f207f-ac3f-4a5f-8104-c928b38a52a8
keywords:
- LargeHighContrastImages 屬性 Windows 功能區
topic_type:
- apiref
api_name:
- Command.LargeHighContrastImages
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d59c1e760565443c286969cc92b3b0c4a6b83a2513587f424ebcda366b1b8a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119710508"
---
# <a name="commandlargehighcontrastimages-property"></a>LargeHighContrastImages 屬性

代表影像的容器;在此情況下，用於高對比系統設定的大型映射。

## <a name="usage"></a>使用方式

``` syntax
<Command.LargeHighContrastImages>
  child elements
</Command.LargeHighContrastImages>
```

## <a name="attributes"></a>屬性

沒有任何屬性。

## <a name="child-elements"></a>子元素



| 元素                                                 | 描述                                        |
|---------------------------------------------------------|----------------------------------------------------|
| [**映像**](windowsribbon-element-image.md)<br/> | 可能會發生一次或多次<br/> <br/> |



## <a name="parent-elements"></a>父元素



| 元素                                                     |
|-------------------------------------------------------------|
| [**命令**](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a>備註

選擇性。

每個 [**命令**](windowsribbon-element-command.md)最多可能會發生一次。

影像資源必須符合 Windows 中使用的標準點陣圖 (BMP) 圖形格式。

## <a name="examples"></a>範例

下列範例示範具有 [**MenuGroup**](windowsribbon-element-menugroup.md)元素之 [**SplitButton**](windowsribbon-element-splitbutton.md)的基本標記。

這段程式碼會顯示具有大型和小型高對比影像資源的 [**SplitButton**](windowsribbon-element-splitbutton.md) 和 [**MenuGroup**](windowsribbon-element-menugroup.md) 命令宣告。 也會宣告作為 **SplitButton** 專案父容器的相關聯 [**群組**](windowsribbon-element-group.md)。


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
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>              |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[指定功能區影像資源](windowsribbon-imageformats.md)
</dt> <dt>

[UI \_ PKEY \_ LargeHighContrastImage](windowsribbon-reference-properties-uipkey-largehighcontrastimage.md)
</dt> </dl>

 

 






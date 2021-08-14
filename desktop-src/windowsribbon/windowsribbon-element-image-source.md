---
title: Image. Source 屬性
description: 代表影像的目錄路徑。
ms.assetid: 174a518a-e9a3-4461-a9a3-d61b62d2b718
keywords:
- 影像。來源屬性 Windows 功能區
topic_type:
- apiref
api_name:
- Image.Source
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20612f0d25f914cb4c80ae77bb001a678af79e4605c3e1358ed7e33f6b19d805
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118202403"
---
# <a name="imagesource-property"></a>Image. Source 屬性

代表影像的目錄路徑。

## <a name="usage"></a>使用方式

``` syntax
<Image.Source/>
```

## <a name="attributes"></a>屬性

沒有任何屬性。

## <a name="child-elements"></a>子元素

沒有任何子項目。

## <a name="parent-elements"></a>父元素



| 元素                                                 |
|---------------------------------------------------------|
| [**映像**](windowsribbon-element-image.md)<br/> |



## <a name="remarks"></a>備註

選擇性。

每個 [**影像**](windowsribbon-element-image.md)最多可能會發生一次。

這個元素包含型別 *xs： anyURI* 的值，或代表 (URI) 之統一資源識別項的任何字元序列。 URI 值是功能區標記檔案的絕對或相對 (，) 點陣圖類型之影像資源的目錄路徑 (BMP) 。

## <a name="examples"></a>範例

下列程式碼範例會示範透過一組 [**影像**](windowsribbon-element-image.md) 元素來宣告所需的標記，此集合是設計用來支援四個特定螢幕 DPI 設定的影像資源集合。 **Image. Source** 屬性可用來指定影像資源的路徑。


```C++
<Command Name="cmdSizeAndColor" Symbol="IDR_CMD_SIZEANDCOLOR">
  <Command.LabelTitle>
    <String Id="250">Size and Color</String>
  </Command.LabelTitle>
  <Command.LargeImages>
    <Image Id="251" MinDPI="96">
      <Image.Source>res/sizeAndColor_96.bmp</Image.Source>
    </Image>
    <Image Id="252" MinDPI="120">
      <Image.Source>res/sizeAndColor_120.bmp</Image.Source>
    </Image>
    <Image Id="253" MinDPI="144">
      <Image.Source>res/sizeAndColor_144.bmp</Image.Source>
    </Image>
    <Image Id="254" MinDPI="192">
      <Image.Source>res/sizeAndColor_192.bmp</Image.Source>
    </Image>
  </Command.LargeImages>
</Command>
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>              |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/> |



 

 






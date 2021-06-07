---
title: " (Windows 功能區架構) 的 Image 元素"
description: 表示影像。
ms.assetid: 2c71bb16-93ac-484f-b81b-1b95842472b3
keywords:
- 影像元素視窗功能區
topic_type:
- apiref
api_name:
- Image
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fe0b9afb51697d50de9cb80886cf829b90c81262
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111442889"
---
# <a name="image-element"></a>Image 項目

表示影像。

## <a name="usage"></a>使用方式

``` syntax
<Image
  Source = "xs:anyURI"
  MinDPI = "xs:positiveInteger"
  Symbol = "xs:string"
  Id = "xs:positiveInteger union xs:string">
  child elements
</Image>
```

## <a name="attributes"></a>屬性



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>屬性</th>
<th>類型</th>
<th>必要</th>
<th>說明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>識別碼</strong><br/></td>
<td>xs： positiveInteger union xs： string<br/></td>
<td>否<br/></td>
<td>唯一的資源識別碼。 <br/> <br/>
<dt><span></span><span></span><strong></strong> (xs： positiveInteger 和 xs： string 的聯集) <br/> </dt> <dd> 介於2和59999（含）之間的整數值，或以十六進位（含）表示的0xea5f。 <br/> 最大長度為10個字元，包括選擇性前置零。 <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>MinDPI</strong><br/></td>
<td>xs:positiveInteger<br/></td>
<td>否<br/></td>
<td><dt><span></span><span></span><strong></strong> (xs： positiveInteger) <br/> </dt> <dd> 最小值為96的任何數位序列。 <br/> 如果省略 MinDPI，預設值為96。 <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>來源</strong><br/></td>
<td>xs:anyURI<br/></td>
<td>否<br/></td>
<td><dt><span></span><span></span><strong></strong> (xs： anyURI) <br/> </dt> <dd> 表示 URI 的任何字元序列。 URI 值是功能區標記檔案的絕對或相對 (，) 類型為 BMP 之影像資源的路徑。 <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>符號</strong><br/></td>
<td>xs:string<br/></td>
<td>否<br/></td>
<td>影像的資源符號。<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs： string) <br/> </dt> <dd> 由字母或底線組成的字串，後面接著字母、數位或底線的任意序列，最多100個字元。 <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>子元素



| 元素                                                               | 描述                                   |
|-----------------------------------------------------------------------|-----------------------------------------------|
| [**映射。來源**](windowsribbon-element-image-source.md)<br/> | 最多可能發生一次<br/> <br/> |



## <a name="parent-elements"></a>父元素



| 元素                                                                                                     |
|-------------------------------------------------------------------------------------------------------------|
| [**LargeHighContrastImages**](windowsribbon-element-command-largehighcontrastimages.md)<br/> |
| [**LargeImages**](windowsribbon-element-command-largeimages.md)<br/>                         |
| [**SmallHighContrastImages**](windowsribbon-element-command-smallhighcontrastimages.md)<br/> |
| [**SmallImages**](windowsribbon-element-command-smallimages.md)<br/>                         |



## <a name="remarks"></a>備註

選擇性。

每個 [**命令 SmallImages**](windowsribbon-element-command-smallimages.md)、 [**SmallHighContrastImages**](windowsribbon-element-command-smallhighcontrastimages.md)、 [**LargeImages**](windowsribbon-element-command-largeimages.md)或 [**LargeHighContrastImages**](windowsribbon-element-command-largehighcontrastimages.md) 元素都可能發生一次或多次。

當設計用來支援每英寸特定螢幕點的影像資源集合時 (DPI) 設定會透過一組 **影像** 元素提供給功能區架構，而架構會使用 *MinDPI* 屬性值符合目前螢幕 DPI 設定的 **影像**。

如果未使用符合目前螢幕 DPI 設定的 *MinDPI* 值來宣告 **影像** 元素，則架構會挑選最接近目前螢幕 DPI 設定的最接近 *MinDPI* 值的 **影像**，並向上調整影像資源。 否則，如果未使用 *MinDPI* 屬性值（小於目前的螢幕 DPI 設定）來宣告 **影像** 元素，則架構會挑選大於目前螢幕 DPI 設定的最接近 *MinDPI* 值，並將影像資源向下調整。

## <a name="examples"></a>範例

下列程式碼範例會示範透過一組 **影像** 元素來宣告所需的標記，此集合是設計用來支援四個特定螢幕 DPI 設定的影像資源集合。


```XML
<Command Name="cmdSizeAndColor" Symbol="IDR_CMD_SIZEANDCOLOR">
  <Command.LabelTitle>
    <String Id="250">Size and Color</String>
  </Command.LabelTitle>
  <Command.LargeImages>
    <Image Id="251" MinDPI="96">res/sizeAndColor_96.bmp</Image>
    <Image Id="252" MinDPI="120">res/sizeAndColor_120.bmp</Image>
    <Image Id="253" MinDPI="144">res/sizeAndColor_144.bmp</Image>
    <Image Id="254" MinDPI="192">res/sizeAndColor_192.bmp</Image>
  </Command.LargeImages>
</Command>
```



## <a name="element-information"></a>項目資訊

* **最低支援系統**： Windows 7
* **可以是空** 的：否



## <a name="see-also"></a>另請參閱

<dl> <dt>

[指定功能區影像資源](windowsribbon-imageformats.md)
</dt> </dl>

 

 






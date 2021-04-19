---
title: HelpButton 元素
description: 表示説明按鈕控制項。
ms.assetid: 24c709da-539e-4ea0-bd3e-d3fbd72dfb97
keywords:
- HelpButton 元素視窗功能區
topic_type:
- apiref
api_name:
- HelpButton
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5be084ff6fc92d4eac4bbaffb3c507142f91eba8
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/11/2020
ms.locfileid: "106966438"
---
# <a name="helpbutton-element"></a>HelpButton 元素

表示 [説明按鈕](windowsribbon-controls-helpbutton.md) 控制項。

## <a name="usage"></a>使用方式

``` syntax
<HelpButton
  CommandName = "xs:positiveInteger or xs:string"/>
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
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>CommandName</strong><br/></td>
<td>xs： positiveInteger 或 xs： string<br/></td>
<td>No<br/></td>
<td>將元素與 <a href="windowsribbon-element-command.md"><strong>命令</strong></a>產生關聯。<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs： positiveInteger 或 xs： string) <br/> </dt> <dd> 字串、介於2與59999（含）之間的整數值，或介於0x2 與0xea5f （含）之間的十六進位值。 <br/> 值在功能區 XML 檔中必須是唯一的。 <br/> 最大長度：100個字元。 <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>子元素

沒有任何子項目。

## <a name="parent-elements"></a>父元素



| 元素                                                                         |
|---------------------------------------------------------------------------------|
| [**功能區. HelpButton**](windowsribbon-element-ribbon-helpbutton.md)<br/> |



## <a name="remarks"></a>備註

選擇性。

每個功能區最多可能會發生一次 [**。 HelpButton**](windowsribbon-element-ribbon-helpbutton.md)。

當您按一下時，會啟動應用程式說明對話方塊。

## <a name="examples"></a>範例

下列範例將示範執行功能區說明 [按鈕](windowsribbon-controls-helpbutton.md) 控制項所需的基本標記。

這段程式碼會顯示 **HelpButton** 命令宣告。


```XML
<Command Name="cmdHelp"
         Symbol="IDR_CMD_HELP">      
</Command>
```



這段程式碼會顯示 **HelpButton** 控制項宣告。


```XML
<Ribbon.HelpButton>
  <HelpButton CommandName="cmdHelp"/>
</Ribbon.HelpButton>
```



## <a name="element-information"></a>項目資訊



|                                     |           |
|-------------------------------------|-----------|
| 最低支援系統<br/> | Windows 7 |
| 可以是空的                        | Yes       |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[說明按鈕控制項](windowsribbon-controls-helpbutton.md)
</dt> </dl>

 

 





